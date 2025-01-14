---json {"title":"Progress Events"} ---

{% include 'partials/nacl-warning.njk' %}

---

- <a href="#module-loading-and-progress-events" id="id3" class="reference internal">Module loading and progress events</a>
- <a href="#handling-progress-events" id="id4" class="reference internal">Handling progress events</a>
- <a href="#displaying-load-status" id="id5" class="reference internal">Displaying load status</a>
- <a href="#the-lasterror-attribute" id="id6" class="reference internal">The <code>lastError</code> attribute</a>
- <a href="#the-readystate-attribute" id="id7" class="reference internal">The <code>readyState</code> attribute</a>
- <a href="#the-exitstatus-attribute" id="id8" class="reference internal">The <code>exitStatus</code> attribute</a>

There are five types of events that developers can respond to in Native Client: progress, message, view change, focus, and input events (each described in the glossary below). This section describes how to monitor progress events (events that occur during the loading and execution of a Native Client module). This section assumes you are familiar with the material presented in the <a href="/docs/native-client/overview" class="reference internal"><em>Technical Overview</em></a>.

The load*progress example illustrates progress event handling. You can find this code in the `/pepper*<version>/examples/tutorial/load_progress/` directory in the Native Client SDK download.

## Module loading and progress events

The Native Client runtime reports a set of state changes during the module loading process by means of DOM progress events. This set of events is a direct port of the proposed W3C <a href="http://www.w3.org/TR/progress-events/" class="reference external">Progress Events</a> standard (except for the `crash` event which is an extension of the W3C standard). The following table lists the events types reported by the Native Client runtime:

<table><colgroup><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /></colgroup><thead><tr class="header"><th>Event</th><th>Times triggered</th><th>When triggered</th><th>How you might respond</th></tr></thead><tbody><tr class="odd"><td><dl><dt><code>loadstart</code></dt><dd>Native Client has started to load a Native Client module.</dd></dl></td><td>once</td><td>The first progress event after the Native Client module is instantiated and initialized.</td><td>Display a status message, such as “Loading...”</td></tr><tr class="even"><td><dl><dt><code>progress</code></dt><dd>Part of the module has been loaded.</dd></dl></td><td>zero or more</td><td>After <code>loadstart</code> has been dispatched.</td><td>Display a progress bar.</td></tr><tr class="odd"><td><dl><dt><code>error</code></dt><dd>The Native Client module failed to start execution (includes any error before or during initialization of the module). The <code>lastError</code> attribute (mentioned later) provides details on the error (initialization failed, sel_ldr did not start, and so on).</dd></dl></td><td>zero or once</td><td>After the last <code>progress</code> event has been dispatched, or after <code>loadstart</code> if no <code>progress</code> event was dispatched.</td><td>Inform user that the application failed to load.</td></tr><tr class="even"><td><dl><dt><code>abort</code></dt><dd>Loading of the NativeClient module was aborted by the user.</dd></dl></td><td>zero or once</td><td>After the last <code>progress</code> event has been dispatched, or after <code>loadstart</code> if no <code>progress</code> event was dispatched.</td><td>It’s not likely you will want to respond to this event.</td></tr><tr class="odd"><td><dl><dt><code>load</code></dt><dd>The Native Client module was successfully loaded, and execution was started. (The module was initialized successfully.)</dd></dl></td><td>zero or once</td><td>After the last <code>progress</code> event has been dispatched, or after <code>loadstart</code> if no <code>progress</code> event was dispatched.</td><td>Remove the progress bar.</td></tr><tr class="even"><td><dl><dt><code>loadend</code></dt><dd>Loading of the Native Client module has stopped. Load succeeded (<code>load</code>), failed (<code>error</code>), or was aborted (<code>abort</code>).</dd></dl></td><td>once</td><td>After an <code>error</code>, <code>abort</code>, or <code>load</code> event was dispatched.</td><td>Indicate loading is over (regardless of failure or not).</td></tr><tr class="odd"><td><dl><dt><code>crash</code></dt><dd>The Native Client module is not responding (died on an <code>assert()</code> or <code>exit()</code>) after a successful load. This event is unique to Native Client and is not part of the W3C Progress Events standard. The <code>exitStatus</code> attribute provides the numeric exit status.</dd></dl></td><td>zero or once</td><td>After a <code>loadend</code>.</td><td>Notify user that the module did something illegal.</td></tr></tbody></table>

The sequence of events for a successful module load is as follows:

<table><thead><tr class="header"><th>Event is dispatched</th><th>... then this task is attempted</th></tr></thead><tbody><tr class="odd"><td><code>loadstart</code></td><td>load the manifest file</td></tr><tr class="even"><td><code>progress</code> (first time)</td><td>load the module</td></tr><tr class="odd"><td><code>progress</code> (subsequent times)</td><td> </td></tr><tr class="even"><td><code>load</code></td><td>start executing the module</td></tr><tr class="odd"><td><code>loadend</code></td><td> </td></tr></tbody></table>

Errors that occur during loading are logged to the JavaScript console in Google Chrome (select the menu icon ![menu-icon](/docs/native-client/images/menu-icon.png) &gt; Tools &gt; JavaScript console).

## Handling progress events

You should add event listeners in a `<script>` element to listen for these events before the `<embed>` element is parsed. For example, the following code adds a listener for the `load` event to a parent `<div>` element that also contains the Native Client `<embed>` element. First, the listener is attached. Then, when the listener `<div>` receives the `load` event, the JavaScript `moduleDidLoad()` function is called. The following code is excerpted from the example in `getting_started/part1/`:

    <!--
    Load the published pexe.
    Note: Since this module does not use any real-estate in the browser, its
    width and height are set to 0.

    Note: The <embed> element is wrapped inside a <div>, which has both a 'load'
    and a 'message' event listener attached.  This wrapping method is used
    instead of attaching the event listeners directly to the <embed> element to
    ensure that the listeners are active before the NaCl module 'load' event
    fires.  This also allows you to use PPB_Messaging.PostMessage() (in C) or
    pp::Instance.PostMessage() (in C++) from within the initialization code in
    your module.
    -->
    <div id="listener">
      <script type="text/javascript">
        var listener = document.getElementById('listener');
        listener.addEventListener('load', moduleDidLoad, true);
        listener.addEventListener('message', handleMessage, true);
      </script>

      <embed id="hello_tutorial"
             width=0 height=0
             src="hello_tutorial.nmf"
             type="application/x-pnacl" />
    </div>

Event listeners can be added to any DOM object. Since listeners set at the outermost scope capture events for their contained elements, you can set listeners on outer elements (including the `<body>` element) to handle events from inner elements. For more information, see the W3 specifications for <a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html#Events-flow-capture" class="reference external">event flow capture</a> and <a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html#Events-registration" class="reference external">event listener registration</a>.

## Displaying load status

One common response to progress events is to display the percentage of the module that has been loaded. In the load_progress example, when the `progress` event is triggered the `moduleLoadProgress` function is called. This function uses the `lengthComputable`, `loaded`, and `total` attributes (described in the proposed W3C <a href="http://www.w3.org/TR/progress-events/" class="reference external">Progress Events</a> standard) of the event to calculate the percentage of the module that has loaded.

    function moduleLoadProgress(event) {
      var loadPercent = 0.0;
      var loadPercentString;
      if (event.lengthComputable && event.total > 0) {
        loadPercent = event.loaded / event.total * 100.0;
        loadPercentString = loadPercent + '%';
        common.logMessage('progress: ' + event.url + ' ' + loadPercentString +
                         ' (' + event.loaded + ' of ' + event.total + ' bytes)');
      } else {
        // The total length is not yet known.
        common.logMessage('progress: Computing...');
      }
    }

## The `lastError` attribute

The `<embed>` element has a `lastError` attribute that is set to an informative string whenever a load failure (an `error` or `abort` event) occurs.

The following code adds an event listener before the `<embed>` element to capture and handle an error in loading the Native Client module. The `handleError()` function listens for an `error` event. When an error occurs, this function prints the contents of the `lastError` attribute (`embed_element.lastError`) as an alert.

    function domContentLoaded(name, tc, config, width, height) {
      var listener = document.getElementById('listener');
      ...
      listener.addEventListener('error', moduleLoadError, true);
      ...
      common.createNaClModule(name, tc, config, width, height);
    }

    function moduleLoadError() {
      common.logMessage('error: ' + common.naclModule.lastError);
    }

## The `readyState` attribute

You can use the `readyState` attribute to monitor the loading process. This attribute is particularly useful if you don’t care about the details of individual progress events or when you want to poll for current load state without registering listeners. The value of `readyState` progresses as follows for a successful load:

<table><thead><tr class="header"><th>Event</th><th><code>readyState</code> value</th></tr></thead><tbody><tr class="odd"><td>(before any events)</td><td><code>undefined</code></td></tr><tr class="even"><td><code>loadstart</code></td><td>1</td></tr><tr class="odd"><td><code>progress</code></td><td>3</td></tr><tr class="even"><td><code>load</code></td><td>4</td></tr><tr class="odd"><td><code>loadend</code></td><td>4</td></tr></tbody></table>

The following code demonstrates how to monitor the loading process using the `readyState` attribute. As before, the script that adds the event listeners precedes the `<embed>` element so that the event listeners are in place before the progress events are generated.

    <html>
    ...
      <body id="body">
        <div id="status_div">
        </div>
        <div id="listener_div">
          <script type="text/javascript">
             var stat = document.getElementById('status_div');
             function handleEvent(e) {
               var embed_element = document.getElementById('my_embed');
               stat.innerHTML +=
               '<br>' + e.type + ': readyState = ' + embed_element.readyState;
             }
             var listener_element = document.getElementById('listener_div');
             listener_element.addEventListener('loadstart', handleEvent, true);
             listener_element.addEventListener('progress', handleEvent, true);
             listener_element.addEventListener('load', handleEvent, true);
             listener_element.addEventListener('loadend', handleEvent, true);
          </script>
          <embed
            name="naclModule"
            id="my_embed"
            width=0 height=0
            src="my_example.nmf"
            type="application/x-pnacl" />
        </div>
      </body>
    </html>

## The `exitStatus` attribute

This read-only attribute is set if the application calls `exit(n)`, `abort()`, or crashes. Since NaCl modules are event handlers, there is no need to call `exit(n)` in normal execution. If the module does exit or crash, the `crash` progress event is issued and the `exitStatus` attribute will contain the numeric value of the exit status:

- In the case of explicit calls to `exit(n)`, the numeric value will be `n` (between 0 and 255).
- In the case of crashes and calls to `abort()`, the numeric value will be non-zero, but the exact value will depend on the chosen libc and the target architecture, and may change in the future. Applications should not rely on the `exitStatus` value being stable in these cases, but the value may nevertheless be useful for temporary debugging.
