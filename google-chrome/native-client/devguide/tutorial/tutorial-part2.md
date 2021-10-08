---json {"title":"C++ Tutorial: Getting Started (Part 2)"} ---

{% include 'partials/nacl-warning.njk' %}

------------------------------------------------------------------------

-   <a href="#overview" id="id1" class="reference internal">Overview</a>
-   <a href="#using-the-native-client-sdk-build-system" id="id2" class="reference internal">Using the Native Client SDK build system</a>

    -   <a href="#simplifying-the-makefile" id="id3" class="reference internal">Simplifying the Makefile</a>
    -   <a href="#choosing-valid-toolchains-and-including-common-mk" id="id4" class="reference internal">Choosing valid toolchains, and including common.mk</a>
    -   <a href="#configuring-your-project" id="id5" class="reference internal">Configuring your project</a>
    -   <a href="#build-macros" id="id6" class="reference internal">Build macros</a>

-   <a href="#making-index-html-work-for-chrome-apps" id="id7" class="reference internal">Making index.html work for Chrome Apps</a>

    -   <a href="#csp-rules" id="id8" class="reference internal">CSP rules</a>
    -   <a href="#making-index-html-csp-compliant" id="id9" class="reference internal">Making index.html CSP-compliant</a>
    -   <a href="#making-index-html-support-different-toolchains-and-configurations" id="id10" class="reference internal">Making index.html support different toolchains and configurations</a>

-   <a href="#sharing-common-code-with-common-js" id="id11" class="reference internal">Sharing common code with common.js</a>

    -   <a href="#loading-the-page-and-creating-the-module" id="id12" class="reference internal">Loading the page and creating the module</a>

-   <a href="#example-specific-behavior-with-example-js" id="id13" class="reference internal">Example-specific behavior with example.js</a>
-   <a href="#compile-the-native-client-module-and-run-the-application-again" id="id14" class="reference internal">Compile the Native Client module and run the application again</a>

Overview
--------

This tutorial shows how to convert the finished PNaCl web application from <a href="/docs/native-client/devguide/tutorial/tutorial-part1" class="reference internal"><em>Part 1</em></a> to use the Native Client SDK build system and common JavaScript files. It also demonstrates some techniques to make your web application <a href="/apps/contentSecurityPolicy" class="reference external">Content Security Policy (CSP)-compliant</a>, which is necessary for <a href="/apps" class="reference external">Chrome Apps</a>.

Using the Native Client SDK build system makes it easy to build with all of the SDK toolchains, and switch between the Debug and Release configurations. It also simplifies the makefiles for your project, as we’ll see in the next section. Finally, it adds some useful commands for <a href="/docs/native-client/sdk/examples#running-the-sdk-examples" class="reference internal"><em>running</em></a> and <a href="/docs/native-client/sdk/examples#debugging-the-sdk-examples" class="reference internal"><em>debugging</em></a> your application.

The finished code for this example can be found in the `pepper_$(VERSION)/getting_started/part2` directory in the Native Client SDK download.

Using the Native Client SDK build system
----------------------------------------

This section describes how to use the SDK build system. To do so, we’ll make changes in the makefile. Because the makefile in part1 and part2 are so different, it is easier to start from scratch. Here is the contents of the new makefile. The following sections will describe it in more detail.

### Simplifying the Makefile

The makefile from part1 only supports one toolchain (PNaCl) and one configuration (Release). It also only supports one source file. It’s relatively simple, but if we want to add support for multiple toolchains, configurations, source files, or build steps, it would grow increasingly complex. The SDK build system uses a set of variables and macros to make this possible, without significantly increasing the complexity of the makefile.

Here is the new makefile, supporting three toolchains (PNaCl, Newlib NaCl, Glibc NaCl) and two configurations (Debug, Release).

    VALID_TOOLCHAINS := pnacl clang-newlib glibc

    NACL_SDK_ROOT ?= $(abspath $(CURDIR)/../..)
    include $(NACL_SDK_ROOT)/tools/common.mk

    TARGET = part2
    LIBS = ppapi_cpp ppapi

    CFLAGS = -Wall
    SOURCES = hello_tutorial.cc

    # Build rules generated by macros from common.mk:

    $(foreach src,$(SOURCES),$(eval $(call COMPILE_RULE,$(src),$(CFLAGS))))

    # The PNaCl workflow uses both an unstripped and finalized/stripped binary.
    # On NaCl, only produce a stripped binary for Release configs (not Debug).
    ifneq (,$(or $(findstring pnacl,$(TOOLCHAIN)),$(findstring Release,$(CONFIG))))
    $(eval $(call LINK_RULE,$(TARGET)_unstripped,$(SOURCES),$(LIBS),$(DEPS)))
    $(eval $(call STRIP_RULE,$(TARGET),$(TARGET)_unstripped))
    else
    $(eval $(call LINK_RULE,$(TARGET),$(SOURCES),$(LIBS),$(DEPS)))
    endif

    $(eval $(call NMF_RULE,$(TARGET),))

### Choosing valid toolchains, and including common.mk

The makefile begins by specifying the toolchains that are valid for this project. The Native Client SDK build system supports multi-toolchain projects for its examples and libraries, but generally you will choose one toolchain when you begin your project and never change it. Please see the <a href="/docs/native-client/overview#toolchains" class="reference internal"><em>Toolchains section of the Native Client overview</em></a> for more information.

For this example, we support the `pnacl`, `clang-newlib` and `glibc` toolchains.

    VALID_TOOLCHAINS := pnacl clang-newlib glibc

Next, as a convenience, we specify where to find `NACL_SDK_ROOT`. Because this example is located in `pepper_$(VERSION)/getting_started/part2`, the root of the SDK is two directories up.

    NACL_SDK_ROOT ?= $(abspath $(CURDIR)/../..)

In your own projects, you can use the absolute path to your installed SDK here. You can also override this default by setting the `NACL_SDK_ROOT` environment variable. See <a href="/docs/native-client/devguide/tutorial/tutorial-part1#tutorial-step-5" class="reference internal"><em>Step 5 of Part 1 of this tutorial</em></a> for more details.

Next, we include the file `tools/common.mk`. This file provides the functionality for the Native Client SDK build system, including new build rules to compile and link a project, which we’ll use below.

    include $(NACL_SDK_ROOT)/tools/common.mk

### Configuring your project

After including `tools/common.mk`, we configure the project by specifying its name, the sources and libraries it uses:

    TARGET = part2
    LIBS = ppapi_cpp ppapi

    CFLAGS = -Wall
    SOURCES = hello_tutorial.cc

These variable names are not required and not used by the SDK build system; they are only used in the rules described below. By convention, all SDK makefiles use the following variables:

TARGET  
The name of the project to build. This variable determines the name of the library or executable that will be generated. In the above example, we call the target `part2`, which will generate an executable called `part2.pexe` for PNaCl. For NaCl toolchains, the executable’s file name will be given a suffix for its architecture. For example, the ARM executable is called `part2_arm.nexe`.

LIBS  
A list of libraries that this executable needs to link against. The library search path is already set up to only look in the directory for the current toolchain and architecture. In this example, we link against `ppapi_cpp` and `ppapi`. `ppapi_cpp` is needed to use the <a href="/docs/native-client/pepper_stable/cpp/" class="reference external">Pepper C++ interface</a>. `ppapi` is needed for communicating with the browser.

CFLAGS  
A list of extra flags to pass to the compiler. In this example, we pass `-Wall`, which turns on all warnings.

LDFLAGS  
A list of additional flags to pass to the linker. This example does not need any special linker flags, so this variable is omitted.

SOURCES  
A list of C or C++ sources to compile, separated by spaces. If you have a long list of sources, it may be easier to read if you put each file on its own line, and use `\` as a line-continuation character. Here’s an example:

<!-- -->

    SOURCES = foo.cc \
              bar.cc \
              baz.cc \
              quux.cc

### Build macros

For many projects, the following build macros do not need to be changed; they will use the variables we’ve defined above.

    $(foreach src,$(SOURCES),$(eval $(call COMPILE_RULE,$(src),$(CFLAGS))))

    ifneq (,$(or $(findstring pnacl,$(TOOLCHAIN)),$(findstring Release,$(CONFIG))))
    $(eval $(call LINK_RULE,$(TARGET)_unstripped,$(SOURCES),$(LIBS),$(DEPS)))
    $(eval $(call STRIP_RULE,$(TARGET),$(TARGET)_unstripped))
    else
    $(eval $(call LINK_RULE,$(TARGET),$(SOURCES),$(LIBS),$(DEPS)))
    endif

    $(eval $(call NMF_RULE,$(TARGET),))

The first line defines rules to compile each source in `SOURCES`, using the flags in `CFLAGS`:

    $(foreach src,$(SOURCES),$(eval $(call COMPILE_RULE,$(src),$(CFLAGS))))

The next six lines define rules to link the object files into one or more executables. When `TOOLCHAIN` is `pnacl`, there is only one executable generated: in the example above, `part2.pexe`. When using a NaCl toolchain, there will be three executables generated, one for each architecture: in the example above, `part2_arm.nexe`, `part2_x86_32.nexe` and `part2_x86_64.nexe`.

When `CONFIG` is `Release`, each executable is also stripped to remove debug information and reduce the file size. Otherwise, when the `TOOLCHAIN` is `pnacl`, the workflow involves creating an unstripped binary for debugging and then finalizing it and stripping it for publishing.

    ifneq (,$(or $(findstring pnacl,$(TOOLCHAIN)),$(findstring Release,$(CONFIG))))
    $(eval $(call LINK_RULE,$(TARGET)_unstripped,$(SOURCES),$(LIBS),$(DEPS)))
    $(eval $(call STRIP_RULE,$(TARGET),$(TARGET)_unstripped))
    else
    $(eval $(call LINK_RULE,$(TARGET),$(SOURCES),$(LIBS),$(DEPS)))
    endif

Finally, the NMF rule generates a NaCl manifest file (`.nmf`) that references each executable generated in the previous step:

    $(eval $(call NMF_RULE,$(TARGET),))

Making index.html work for Chrome Apps
--------------------------------------

This section describes the changes necessary to make the HTML and JavaScript in part1 CSP-compliant. This is required if you want to build a <a href="/apps" class="reference external">Chrome App</a>, but is not necessary if you want to use PNaCl on the open web.

### CSP rules

<a href="/apps/contentSecurityPolicy#what" class="reference external">Chrome Apps CSP</a> restricts you from doing the following:

-   You can’t use inline scripting in your Chrome App pages. The restriction bans both `<script>` blocks and event handlers (`<button onclick="...">`).
-   You can’t reference any external resources in any of your app files (except for video and audio resources). You can’t embed external resources in an iframe.
-   You can’t use string-to-JavaScript methods like `eval()` and `new Function()`.

### Making index.html CSP-compliant

To make our application CSP-compliant, we have to remove inline scripting. As described above, we can’t use inline `<script>` blocks or event handlers. This is easy to do—we’ll just reference some new files from our script tag, and remove all of our inlined scripts:

    <head>
      ...
      <script type="text/javascript" src="common.js"></script>
      <script type="text/javascript" src="example.js"></script>
    </head>

`common.js` has shared code used by all SDK examples, and is described later in this document. `example.js` is a script that has code specific to this example.

We also need to remove the inline event handler on the body tag:

    <body onload="pageDidLoad()">
    ...

This logic is now handled by `common.js`.

### Making index.html support different toolchains and configurations

Finally, there are a few changes to `index.html` that are not necessary for CSP-compliance, but help make the SDK examples more generic.

First, we add some <a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_data_attributes" class="reference external">data attributes</a> to the body element to specify the name, supported toolchains, supported configurations, and path to the `.nmf` file:

    <body data-name="part2"
        data-tools="clang-newlib glibc pnacl"
        data-configs="Debug Release"
        data-path="{tc}/{config}">
    ...

`common.js` will read these data attributes to allow you to load the same example with different toolchains by changing the URL’s <a href="http://en.wikipedia.org/wiki/Query_string" class="reference external">query string</a>. For example, you can load the glibc Debug version of this example by navigating to `index.html?tc=glibc&config=Debug`. Path URI’s such as `../`, for example do not work for either the data-path parameter or its corresponding query string.

Next, we remove the `embed` element that is described in HTML. This will be automatically added for us by `common.js`, based on the current toolchain/configuration combination:

    <!--
    Just as in part1, the <embed> element will be wrapped inside the <div>
    element with the id "listener". In part1, the embed was specified in HTML,
    here the common.js module creates a new <embed> element and adds it to the
    <div> for us.
    -->
    <div id="listener"></div>

Sharing common code with common.js
----------------------------------

`common.js` contains JavaScript code that each example uses to create a NaCl module, handle messages from that module and other common tasks like displaying the module load status and logging messages. Explaining all of `common.js` is outside the scope of this document, but please look at the documentation in that file for more information.

### Loading the page and creating the module

Since we’ve added `<script>` tags for `common.js` and `example.js` to the `head` element, they will be loaded and executed before the rest of the document has been parsed. As a result, we have to wait for the page to finish loading before we try to create the embed element and add it to the page.

We can do that by calling `addEventListener` and listening for the `DOMContentLoaded` event:

    // Listen for the DOM content to be loaded. This event is fired when parsing of
    // the page's document has finished.
    document.addEventListener('DOMContentLoaded', function() {
      ...
    });

Inside this function, we parse the URL query string, and compare that to the data attributes:

    // From https://developer.mozilla.org/en-US/docs/DOM/window.location
    var searchVars = {};
    if (window.location.search.length > 1) {
      var pairs = window.location.search.substr(1).split('&');
      for (var key_ix = 0; key_ix < pairs.length; key_ix++) {
        var keyValue = pairs[key_ix].split('=');
        searchVars[unescape(keyValue[0])] =
            keyValue.length > 1 ? unescape(keyValue[1]) : '';
      }
    }

    ...

    var toolchains = body.dataset.tools.split(' ');
    var configs = body.dataset.configs.split(' ');

    ...

    var tc = toolchains.indexOf(searchVars.tc) !== -1 ?
        searchVars.tc : toolchains[0];

    // If the config value is included in the search vars, use that.
    // Otherwise default to Release if it is valid, or the first value if
    // Release is not valid.
    if (configs.indexOf(searchVars.config) !== -1)
      var config = searchVars.config;
    else if (configs.indexOf('Release') !== -1)
      var config = 'Release';
    else
      var config = configs[0];

Then `domContentLoaded` is called, which performs some checks to see if the browser supports Native Client, then creates the NaCl module.

    function domContentLoaded(name, tool, path, width, height, attrs) {
      updateStatus('Page loaded.');
      if (!browserSupportsNaCl(tool)) {
        updateStatus(
            'Browser does not support NaCl (' + tool + '), or NaCl is disabled');
      } else if (common.naclModule == null) {
        updateStatus('Creating embed: ' + tool);

        // We use a non-zero sized embed to give Chrome space to place the bad
        // plug-in graphic, if there is a problem.
        width = typeof width !== 'undefined' ? width : 200;
        height = typeof height !== 'undefined' ? height : 200;
        attachDefaultListeners();
        createNaClModule(name, tool, path, width, height, attrs);
      } else {
        // It's possible that the Native Client module onload event fired
        // before the page's onload event.  In this case, the status message
        // will reflect 'SUCCESS', but won't be displayed.  This call will
        // display the current message.
        updateStatus('Waiting.');
      }
    }

`attachDefaultListeners` is added before the creation of the module, to make sure that no messages are lost. Note that `window.attachListeners` is also called; this is the way that `common.js` allows each example to configure itself differently. If an example defines the `attachListeners` function, it will be called by `common.js`.

    function attachDefaultListeners() {
      var listenerDiv = document.getElementById('listener');
      listenerDiv.addEventListener('load', moduleDidLoad, true);
      listenerDiv.addEventListener('message', handleMessage, true);
      listenerDiv.addEventListener('crash', handleCrash, true);
      if (typeof window.attachListeners !== 'undefined') {
        window.attachListeners();
      }
    }

Finally, `createNaClModule` actually creates the `embed`, and appends it as a child of the element with id `listener`:

    function createNaClModule(name, tool, path, width, height, attrs) {
      var moduleEl = document.createElement('embed');
      moduleEl.setAttribute('name', 'nacl_module');
      moduleEl.setAttribute('id', 'nacl_module');
      moduleEl.setAttribute('width', width);
      moduleEl.setAttribute('height', height);
      moduleEl.setAttribute('path', path);
      moduleEl.setAttribute('src', path + '/' + name + '.nmf');

      ...

      var mimetype = mimeTypeForTool(tool);
      moduleEl.setAttribute('type', mimetype);

      var listenerDiv = document.getElementById('listener');
      listenerDiv.appendChild(moduleEl);
      ...
    }

When the module finishes loading, it will dispatch a `load` event, and the event listener function that was registered above (`moduleDidLoad`) will be called. Note that `common.js` allows each example to define a `window.moduleDidLoad` function, that will be called here as well.

    function moduleDidLoad() {
      common.naclModule = document.getElementById('nacl_module');
      updateStatus('RUNNING');

      if (typeof window.moduleDidLoad !== 'undefined') {
        window.moduleDidLoad();
      }
    }

Example-specific behavior with example.js
-----------------------------------------

As described in the previous section, `common.js` will call certain functions during the module loading process. This example only needs to respond to two: `moduleDidLoad` and `handleMessage`.

    // This function is called by common.js when the NaCl module is
    // loaded.
    function moduleDidLoad() {
      // Once we load, hide the plugin. In this example, we don't display anything
      // in the plugin, so it is fine to hide it.
      common.hideModule();

      // After the NaCl module has loaded, common.naclModule is a reference to the
      // NaCl module's <embed> element.
      //
      // postMessage sends a message to it.
      common.naclModule.postMessage('hello');
    }

    // This function is called by common.js when a message is received from the
    // NaCl module.
    function handleMessage(message) {
      var logEl = document.getElementById('log');
      logEl.textContent += message.data;
    }

Compile the Native Client module and run the application again
--------------------------------------------------------------

1.  Compile the Native Client module by running the `make` command again.

2.  Start the SDK web server by running `make server`.

3.  Re-run the application by reloading `http://localhost:5103/part2` in Chrome.

    After Chrome loads the Native Client module, you should see the message sent from the module.