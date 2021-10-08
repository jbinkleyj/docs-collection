---json {"title":"pp::Instance Class Reference"} ---

[List of all members.](/docs/native-client/pepper_stable/cpp/classpp_1_1_instance-members/)

Public Member Functions
-----------------------

 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a398b1946805872334781dac993cfe704" class="el">Instance</a> (PP\_Instance instance)

virtual 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5e475ef135a235029bc0515e9e3ff832" class="el">~Instance</a> ()

PP\_Instance 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#aeb29ff4201f9ae0e356c5ed0bb4a2679" class="el">pp_instance</a> () const

virtual bool 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a4f915e70caaef514a49ef8afcddde30f" class="el">Init</a> (uint32\_t argc, const char \*argn\[\], const char \*argv\[\])

void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a9773263ee281405030548fc224eeec08" class="el">AddPerInstanceObject</a> (const std::string &interface\_name, void \*object)

void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a33c633189c7c321dac8e0c5dc6e67f5b" class="el">RemovePerInstanceObject</a> (const std::string &interface\_name, void \*object)

PPP\_Instance methods for the module to override:

virtual void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#ad952f05e42f0e036157beb216f12f3f3" class="el">DidChangeView</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_view/" class="el">View</a> &view)

virtual void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a72ac4ec0b62c4cd8dedae3cf0fc577c2" class="el">DidChangeView</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_rect/" class="el">Rect</a> &position, const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_rect/" class="el">Rect</a> &clip)

virtual void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a42c67b21f11bef29c5b341c78926bad3" class="el">DidChangeFocus</a> (bool has\_focus)

virtual bool 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a46aa2feb657fa14263a29375fe458b00" class="el">HandleInputEvent</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_input_event/" class="el">pp::InputEvent</a> &event)

virtual bool 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6cd99065ef0a55555647253442563225" class="el">HandleDocumentLoad</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_u_r_l_loader/" class="el">URLLoader</a> &url\_loader)

virtual void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5dce8c8b36b1df7cfcc12e42397a35e8" class="el">HandleMessage</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &message)

PPB\_Instance methods for querying the browser:

bool 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a147a1c1817a7a1fb2b76f5c87ab08899" class="el">BindGraphics</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_graphics2_d/" class="el">Graphics2D</a> &graphics)

bool 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#abcfd0eb0995e6273271b4ff4c3df16ae" class="el">BindGraphics</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_graphics3_d/" class="el">Graphics3D</a> &graphics)

bool 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a845a8736f87b78538c73c9f8d192b77a" class="el">BindGraphics</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_compositor/" class="el">Compositor</a> &compositor)

bool 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a451fb956e64fd3db891608148a044c01" class="el">IsFullFrame</a> ()

int32\_t 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a2e2d63280786c0cc41b7c6f656cc81b5" class="el">RequestInputEvents</a> (uint32\_t event\_classes)

int32\_t 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6341c14fc54427e45349f5158483e017" class="el">RequestFilteringInputEvents</a> (uint32\_t event\_classes)

void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a286bc22174e2f7b6e917c56aa5c7de86" class="el">ClearInputEventRequest</a> (uint32\_t event\_classes)

void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el">PostMessage</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &message)

int32\_t 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5b5b1a66eda2d0e6884de8f7e25e2346" class="el">RegisterMessageHandler</a> (<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_message_handler/" class="el">MessageHandler</a> \*message\_handler, const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_message_loop/" class="el">MessageLoop</a> &message\_loop)

void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5e37f26ebc58915574819542a41a6329" class="el">UnregisterMessageHandler</a> ()

PPB\_Console methods for logging to the console:

void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a192ab89f4acf2e1e25df14e22d0cff43" class="el">LogToConsole</a> (PP\_LogLevel level, const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &value)

void 

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a48286ccf1217b3ae02138049d00af48f" class="el">LogToConsoleWithSource</a> (PP\_LogLevel level, const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &source, const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &value)

Static Public Member Functions
------------------------------

<table><tbody><tr class="odd"><td style="text-align: right;">static void </td><td><a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#ad1b6c19954ff9446349a6fa5684eea2d" class="el">RemovePerInstanceObject</a> (const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance_handle/" class="el">InstanceHandle</a> &amp;instance, const std::string &amp;interface_name, void *object)</td></tr><tr class="even"><td style="text-align: right;">static void * </td><td><a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6dec498f1d49571be9fd40e23745327f" class="el">GetPerInstanceObject</a> (PP_Instance instance, const std::string &amp;interface_name)</td></tr></tbody></table>

------------------------------------------------------------------------

Constructor & Destructor Documentation
--------------------------------------

<span id="a398b1946805872334781dac993cfe704" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a398b1946805872334781dac993cfe704" class="el">pp::Instance::Instance</a></td><td>(</td><td>PP_Instance </td><td><em>instance</em></td><td>)</td><td><code> [explicit]</code></td></tr></tbody></table>

Default constructor.

Construction of an instance should only be done in response to a browser request in `Module::CreateInstance`. Otherwise, the instance will lack the proper bookkeeping in the browser and in the C++ wrapper.

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a4f915e70caaef514a49ef8afcddde30f" class="el" title="Init() initializes this instance with the provided arguments.">Init()</a> will be called immediately after the constructor. This allows you to perform initialization tasks that can fail and to report that failure to the browser.

<span id="a5e475ef135a235029bc0515e9e3ff832" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5e475ef135a235029bc0515e9e3ff832" class="el">pp::Instance::~Instance</a></td><td>(</td><td></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

Destructor.

When the instance is removed from the web page, the `pp::Instance` object will be deleted. You should never delete the `Instance` object yourself since the lifetime is handled by the C++ wrapper and is controlled by the browser's calls to the `PPP_Instance` interface.

The `PP_Instance` identifier will still be valid during this call so the instance can perform cleanup-related tasks. Once this function returns, the `PP_Instance` handle will be invalid. This means that you can't do any asynchronous operations such as network requests or file writes from this destructor since they will be immediately canceled.

**Note:** This function may be skipped in certain call so the instance can perform cleanup-related tasks. Once this function returns, the `PP_Instance` handle will be invalid. This means that you can't do any asynchronous operations such as network requests or file writes from this destructor since they will be immediately canceled.

------------------------------------------------------------------------

Member Function Documentation
-----------------------------

<span id="a9773263ee281405030548fc224eeec08" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a9773263ee281405030548fc224eeec08" class="el">pp::Instance::AddPerInstanceObject</a></td><td>(</td><td>const std::string &amp; </td><td><em>interface_name</em>,</td></tr><tr class="even"><td></td><td></td><td>void * </td><td><em>object</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a9773263ee281405030548fc224eeec08" class="el" title="AddPerInstanceObject() associates an instance with an interface, creating an object.">AddPerInstanceObject()</a> associates an instance with an interface, creating an object.

Many optional interfaces are associated with a plugin instance. For example, the find in PPP\_Find interface receives updates on a per-instance basis. This "per-instance" tracking allows such objects to associate themselves with an instance as "the" handler for that interface name.

In the case of the find example, the find object registers with its associated instance in its constructor and unregisters in its destructor. Then whenever it gets updates with a PP\_Instance parameter, it can map back to the find object corresponding to that given PP\_Instance by calling GetPerInstanceObject.

This lookup is done on a per-interface-name basis. This means you can only have one object of a given interface name associated with an instance.

If you are adding a handler for an additional interface, be sure to register with the module (AddPluginInterface) for your interface name to get the C calls in the first place.

Refer to <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a33c633189c7c321dac8e0c5dc6e67f5b" class="el" title="Refer to AddPerInstanceObject() for further information.">RemovePerInstanceObject()</a> and <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6dec498f1d49571be9fd40e23745327f" class="el" title="Look up an object previously associated with an instance.">GetPerInstanceObject()</a> for further information.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>interface_name</td><td>The name of the interface to associate with the instance</td></tr><tr class="even"><td>[in]</td><td>object</td><td></td></tr></tbody></table>

<span id="a147a1c1817a7a1fb2b76f5c87ab08899" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>bool <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a147a1c1817a7a1fb2b76f5c87ab08899" class="el">pp::Instance::BindGraphics</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_graphics2_d/" class="el">Graphics2D</a> &amp; </td><td><em>graphics</em></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a147a1c1817a7a1fb2b76f5c87ab08899" class="el" title="BindGraphics() binds the given graphics as the current display surface.">BindGraphics()</a> binds the given graphics as the current display surface.

The contents of this device is what will be displayed in the instance's area on the web page. The device must be a 2D or a 3D device.

You can pass an `is_null()` (default constructed) <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_graphics2_d/" class="el">Graphics2D</a> as the device parameter to unbind all devices from the given instance. The instance will then appear transparent. Re-binding the same device will return `true` and will do nothing.

Any previously-bound device will be released. It is an error to bind a device when it is already bound to another instance. If you want to move a device between instances, first unbind it from the old one, and then rebind it to the new one.

Binding a device will invalidate that portion of the web page to flush the contents of the new device to the screen.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>graphics</td><td>A <code>Graphics2D</code> to bind.</td></tr></tbody></table>

<!-- -->

**Returns:**  
true if bind was successful or false if the device was not the correct type. On success, a reference to the device will be held by the instance, so the caller can release its reference if it chooses.

<span id="abcfd0eb0995e6273271b4ff4c3df16ae" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>bool <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a147a1c1817a7a1fb2b76f5c87ab08899" class="el">pp::Instance::BindGraphics</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_graphics3_d/" class="el">Graphics3D</a> &amp; </td><td><em>graphics</em></td><td>)</td><td></td></tr></tbody></table>

Binds the given <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_graphics3_d/" class="el" title="This class represents a 3D rendering context in the browser.">Graphics3D</a> as the current display surface.

Refer to `BindGraphics(const Graphics2D& graphics)` for further information.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>graphics</td><td>A <code>Graphics3D</code> to bind.</td></tr></tbody></table>

<!-- -->

**Returns:**  
true if bind was successful or false if the device was not the correct type. On success, a reference to the device will be held by the instance, so the caller can release its reference if it chooses.

<span id="a845a8736f87b78538c73c9f8d192b77a" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>bool <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a147a1c1817a7a1fb2b76f5c87ab08899" class="el">pp::Instance::BindGraphics</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_compositor/" class="el">Compositor</a> &amp; </td><td><em>compositor</em></td><td>)</td><td></td></tr></tbody></table>

Binds the given <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_compositor/" class="el" title="The Compositor interface is used for setting CompositorLayer layers to the Chromium compositor for co...">Compositor</a> as the current display surface.

Refer to `BindGraphics(const Graphics2D& graphics)` for further information.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>compositor</td><td>A <code>Compositor</code> to bind.</td></tr></tbody></table>

<!-- -->

**Returns:**  
true if bind was successful or false if the device was not the correct type. On success, a reference to the device will be held by the instance, so the caller can release its reference if it chooses.

<span id="a286bc22174e2f7b6e917c56aa5c7de86" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a286bc22174e2f7b6e917c56aa5c7de86" class="el">pp::Instance::ClearInputEventRequest</a></td><td>(</td><td>uint32_t </td><td><em>event_classes</em></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a286bc22174e2f7b6e917c56aa5c7de86" class="el" title="ClearInputEventRequest() requests that input events corresponding to the given input classes no longe...">ClearInputEventRequest()</a> requests that input events corresponding to the given input classes no longer be delivered to the instance.

By default, no input events are delivered. If you have previously requested input events using <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a2e2d63280786c0cc41b7c6f656cc81b5" class="el" title="RequestInputEvents() requests that input events corresponding to the given input events are delivered...">RequestInputEvents()</a> or <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6341c14fc54427e45349f5158483e017" class="el" title="RequestFilteringInputEvents() requests that input events corresponding to the given input events are ...">RequestFilteringInputEvents()</a>, this function will unregister handling for the given instance. This will allow greater browser performance for those events.

**Note:** You may still get some input events after clearing the flag if they were dispatched before the request was cleared. For example, if there are 3 mouse move events waiting to be delivered, and you clear the mouse event class during the processing of the first one, you'll still receive the next two. You just won't get more events generated.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>event_classes</td><td>A combination of flags from <code>PP_InputEvent_Class</code> that identifies the classes of events the instance is no longer interested in.</td></tr></tbody></table>

<span id="a42c67b21f11bef29c5b341c78926bad3" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a42c67b21f11bef29c5b341c78926bad3" class="el">pp::Instance::DidChangeFocus</a></td><td>(</td><td>bool </td><td><em>has_focus</em></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a42c67b21f11bef29c5b341c78926bad3" class="el" title="DidChangeFocus() is called when an instance has gained or lost focus.">DidChangeFocus()</a> is called when an instance has gained or lost focus.

Having focus means that keyboard events will be sent to the instance. An instance's default condition is that it will not have focus.

The focus flag takes into account both browser tab and window focus as well as focus of the plugin element on the page. In order to be deemed to have focus, the browser window must be topmost, the tab must be selected in the window, and the instance must be the focused element on the page.

**Note:**Clicks on instances will give focus only if you handle the click event. Return `true` from `HandleInputEvent` in `PPP_InputEvent` (or use unfiltered events) to signal that the click event was handled. Otherwise, the browser will bubble the event and give focus to the element on the page that actually did end up consuming it. If you're not getting focus, check to make sure you're either requesting them via `RequestInputEvents()`` (which implicitly marks all input events as consumed) or via ``RequestFilteringInputEvents()` and returning true from your event handler.

``` `

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>has_focus</td><td>Indicates the new focused state of the instance.</td></tr></tbody></table>

<span id="ad952f05e42f0e036157beb216f12f3f3" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#ad952f05e42f0e036157beb216f12f3f3" class="el">pp::Instance::DidChangeView</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_view/" class="el">View</a> &amp; </td><td><em>view</em></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#ad952f05e42f0e036157beb216f12f3f3" class="el" title="DidChangeView() is called when the view information for the Instance has changed.">DidChangeView()</a> is called when the view information for the <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance/" class="el">Instance</a> has changed.

See the `View` object for information.

Most implementations will want to check if the size and user visibility changed, and either resize themselves or start/stop generating updates.

You should not call the default implementation. For backwards-compatibility, it will call the deprecated version of DidChangeView below.

<span id="a72ac4ec0b62c4cd8dedae3cf0fc577c2" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#ad952f05e42f0e036157beb216f12f3f3" class="el">pp::Instance::DidChangeView</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_rect/" class="el">Rect</a> &amp; </td><td><em>position</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_rect/" class="el">Rect</a> &amp; </td><td><em>clip</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td><code> [virtual]</code></td></tr></tbody></table>

Deprecated backwards-compatible version of `DidChangeView()`.

New code should derive from the version that takes a `ViewChanged` object rather than this version. This function is called by the default implementation of the newer `DidChangeView` function for source compatibility with older code.

A typical implementation will check the size of the `position` argument and reallocate the graphics context when a different size is received. Note that this function will be called for scroll events where the size doesn't change, so you should always check that the size is actually different before doing any reallocations.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>position</td><td>The location on the page of the instance. The position is relative to the top left corner of the viewport, which changes as the page is scrolled. Generally the size of this value will be used to create a graphics device, and the position is ignored (most things are relative to the instance so the absolute position isn't useful in most cases).</td></tr><tr class="even"><td>[in]</td><td>clip</td><td>The visible region of the instance. This is relative to the top left of the instance's coordinate system (not the page). If the instance is invisible, <code>clip</code> will be (0, 0, 0, 0).</td></tr></tbody></table>

It's recommended to check for invisible instances and to stop generating graphics updates in this case to save system resources. It's not usually worthwhile, however, to generate partial updates according to the clip when the instance is partially visible. Instead, update the entire region. The time saved doing partial paints is usually not significant and it can create artifacts when scrolling (this notification is sent asynchronously from scrolling so there can be flashes of old content in the exposed regions).

<span id="a6dec498f1d49571be9fd40e23745327f" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>static void* <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6dec498f1d49571be9fd40e23745327f" class="el">pp::Instance::GetPerInstanceObject</a></td><td>(</td><td>PP_Instance </td><td><em>instance</em>,</td></tr><tr class="even"><td></td><td></td><td>const std::string &amp; </td><td><em>interface_name</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td><code> [static]</code></td></tr></tbody></table>

Look up an object previously associated with an instance.

Returns NULL if the instance is invalid or there is no object for the given interface name on the instance.

Refer to <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a9773263ee281405030548fc224eeec08" class="el" title="AddPerInstanceObject() associates an instance with an interface, creating an object.">AddPerInstanceObject()</a> for further information.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>instance</td><td></td></tr><tr class="even"><td>[in]</td><td>interface_name</td><td>The name of the interface to associate with the instance.</td></tr></tbody></table>

<span id="a6cd99065ef0a55555647253442563225" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual bool <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6cd99065ef0a55555647253442563225" class="el">pp::Instance::HandleDocumentLoad</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_u_r_l_loader/" class="el">URLLoader</a> &amp; </td><td><em>url_loader</em></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6cd99065ef0a55555647253442563225" class="el" title="HandleDocumentLoad() is called after Init() for a full-frame instance that was instantiated based on ...">HandleDocumentLoad()</a> is called after <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a4f915e70caaef514a49ef8afcddde30f" class="el" title="Init() initializes this instance with the provided arguments.">Init()</a> for a full-frame instance that was instantiated based on the MIME type of a DOMWindow navigation.

This situation only applies to modules that are pre-registered to handle certain MIME types. If you haven't specifically registered to handle a MIME type or aren't positive this applies to you, your implementation of this function can just return false.

The given url\_loader corresponds to a `URLLoader` object that is already opened. Its response headers may be queried using GetResponseInfo(). If you want to use the `URLLoader` to read data, you will need to save a copy of it or the underlying resource will be freed when this function returns and the load will be canceled.

This method returns false if the module cannot handle the data. In response to this method, the module should call ReadResponseBody() to read the incoming data.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>url_loader</td><td>An open <code>URLLoader</code> instance.</td></tr></tbody></table>

<!-- -->

**Returns:**  
true if the data was handled, false otherwise.

<span id="a46aa2feb657fa14263a29375fe458b00" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual bool <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a46aa2feb657fa14263a29375fe458b00" class="el">pp::Instance::HandleInputEvent</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_input_event/" class="el">pp::InputEvent</a> &amp; </td><td><em>event</em></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a46aa2feb657fa14263a29375fe458b00" class="el" title="HandleInputEvent() handles input events from the browser.">HandleInputEvent()</a> handles input events from the browser.

The default implementation does nothing and returns false.

In order to receive input events, you must register for them by calling <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a2e2d63280786c0cc41b7c6f656cc81b5" class="el" title="RequestInputEvents() requests that input events corresponding to the given input events are delivered...">RequestInputEvents()</a> or <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6341c14fc54427e45349f5158483e017" class="el" title="RequestFilteringInputEvents() requests that input events corresponding to the given input events are ...">RequestFilteringInputEvents()</a>. By default, no events are delivered.

If the event was handled, it will not be forwarded to any default handlers. If it was not handled, it may be dispatched to a default handler. So it is important that an instance respond accurately with whether event propagation should continue.

Event propagation also controls focus. If you handle an event like a mouse event, typically the instance will be given focus. Returning false from a filtered event handler or not registering for an event type means that the click will be given to a lower part of the page and your instance will not receive focus. This allows an instance to be partially transparent, where clicks on the transparent areas will behave like clicks to the underlying page.

In general, you should try to keep input event handling short. Especially for filtered input events, the browser or page may be blocked waiting for you to respond.

The caller of this function will maintain a reference to the input event resource during this call. Unless you take a reference to the resource to hold it for later, you don't need to release it.

**Note:** If you're not receiving input events, make sure you register for the event classes you want by calling `RequestInputEvents` or `RequestFilteringInputEvents`. If you're still not receiving keyboard input events, make sure you're returning true (or using a non-filtered event handler) for mouse events. Otherwise, the instance will not receive focus and keyboard events will not be sent.

Refer to `RequestInputEvents` and `RequestFilteringInputEvents` for further information.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>event</td><td>The event to handle.</td></tr></tbody></table>

<!-- -->

**Returns:**  
true if the event was handled, false if not. If you have registered to filter this class of events by calling `RequestFilteringInputEvents`, and you return false, the event will be forwarded to the page (and eventually the browser) for the default handling. For non-filtered events, the return value will be ignored.

<span id="a5dce8c8b36b1df7cfcc12e42397a35e8" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5dce8c8b36b1df7cfcc12e42397a35e8" class="el">pp::Instance::HandleMessage</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>message</em></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5dce8c8b36b1df7cfcc12e42397a35e8" class="el" title="HandleMessage() is a function that the browser calls when PostMessage() is invoked on the DOM element...">HandleMessage()</a> is a function that the browser calls when <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el" title="PostMessage() asynchronously invokes any listeners for message events on the DOM element for the give...">PostMessage()</a> is invoked on the DOM element for the instance in JavaScript.

Note that <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el" title="PostMessage() asynchronously invokes any listeners for message events on the DOM element for the give...">PostMessage()</a> in the JavaScript interface is asynchronous, meaning JavaScript execution will not be blocked while <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5dce8c8b36b1df7cfcc12e42397a35e8" class="el" title="HandleMessage() is a function that the browser calls when PostMessage() is invoked on the DOM element...">HandleMessage()</a> is processing the message.

When converting JavaScript arrays, any object properties whose name is not an array index are ignored. When passing arrays and objects, the entire reference graph will be converted and transferred. If the reference graph has cycles, the message will not be sent and an error will be logged to the console.

**Example:**

The following JavaScript code invokes `HandleMessage`, passing the instance on which it was invoked, with `message` being a string `Var` containing "Hello world!"

     {.html}

     <body>
       <object id="plugin"
               type="application/x-ppapi-postMessage-example"/>
       <script type="text/javascript">
         document.getElementById('plugin').postMessage("Hello world!");
       </script>
     </body>

Refer to <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el" title="PostMessage() asynchronously invokes any listeners for message events on the DOM element for the give...">PostMessage()</a> for sending messages to JavaScript.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>message</td><td>A <code>Var</code> which has been converted from a JavaScript value. JavaScript array/object types are supported from Chrome M29 onward. All JavaScript values are copied when passing them to the plugin.</td></tr></tbody></table>

<span id="a4f915e70caaef514a49ef8afcddde30f" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual bool <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a4f915e70caaef514a49ef8afcddde30f" class="el">pp::Instance::Init</a></td><td>(</td><td>uint32_t </td><td><em>argc</em>,</td></tr><tr class="even"><td></td><td></td><td>const char * </td><td><em>argn</em>[],</td></tr><tr class="odd"><td></td><td></td><td>const char * </td><td><em>argv</em>[] </td></tr><tr class="even"><td></td><td>)</td><td></td><td><code> [virtual]</code></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a4f915e70caaef514a49ef8afcddde30f" class="el" title="Init() initializes this instance with the provided arguments.">Init()</a> initializes this instance with the provided arguments.

This function will be called immediately after the instance object is constructed.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>argc</td><td>The number of arguments contained in <code>argn</code> and <code>argv</code>.</td></tr><tr class="even"><td>[in]</td><td>argn</td><td>An array of argument names. These argument names are supplied in the &lt;embed&gt; tag, for example: <code>&lt;embed id="nacl_module" dimensions="2"&gt;</code> will produce two argument names: "id" and "dimensions".</td></tr><tr class="odd"><td>[in]</td><td>argv</td><td>An array of argument values. These are the values of the arguments listed in the &lt;embed&gt; tag, for example <code>&lt;embed id="nacl_module" dimensions="2"&gt;</code> will produce two argument values: "nacl_module" and "2". The indices of these values match the indices of the corresponding names in <code>argn</code>.</td></tr></tbody></table>

<!-- -->

**Returns:**  
true on success. Returning false causes the instance to be deleted and no other functions to be called.

<span id="a451fb956e64fd3db891608148a044c01" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>bool <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a451fb956e64fd3db891608148a044c01" class="el">pp::Instance::IsFullFrame</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a451fb956e64fd3db891608148a044c01" class="el" title="IsFullFrame() determines if the instance is full-frame (repr).">IsFullFrame()</a> determines if the instance is full-frame (repr).

Such an instance represents the entire document in a frame rather than an embedded resource. This can happen if the user does a top-level navigation or the page specifies an iframe to a resource with a MIME type registered by the module.

**Returns:**  
true if the instance is full-frame, false if not.

<span id="a192ab89f4acf2e1e25df14e22d0cff43" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a192ab89f4acf2e1e25df14e22d0cff43" class="el">pp::Instance::LogToConsole</a></td><td>(</td><td>PP_LogLevel </td><td><em>level</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>value</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

Logs the given message to the JavaScript console associated with the given plugin instance with the given logging level.

The name of the plugin issuing the log message will be automatically prepended to the message. The value may be any type of <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el" title="A generic type used for passing data types between the module and the page.">Var</a>.

<span id="a48286ccf1217b3ae02138049d00af48f" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a48286ccf1217b3ae02138049d00af48f" class="el">pp::Instance::LogToConsoleWithSource</a></td><td>(</td><td>PP_LogLevel </td><td><em>level</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>source</em>,</td></tr><tr class="odd"><td></td><td></td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>value</em> </td></tr><tr class="even"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

Logs a message to the console with the given source information rather than using the internal PPAPI plugin name.

The name must be a string var.

The regular log function will automatically prepend the name of your plugin to the message as the "source" of the message. Some plugins may wish to override this. For example, if your plugin is a Python interpreter, you would want log messages to contain the source .py file doing the log statement rather than have "python" show up in the console.

<span id="a67e888a4e4e23effe7a09625e73ecae9" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el">pp::Instance::PostMessage</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>message</em></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el" title="PostMessage() asynchronously invokes any listeners for message events on the DOM element for the give...">PostMessage()</a> asynchronously invokes any listeners for message events on the DOM element for the given instance.

A call to <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el" title="PostMessage() asynchronously invokes any listeners for message events on the DOM element for the give...">PostMessage()</a> will not block while the message is processed.

**Example:**

     {.html}

     <body>
       <object id="plugin"
               type="application/x-ppapi-postMessage-example"/>
       <script type="text/javascript">
         var plugin = document.getElementById('plugin');
         plugin.addEventListener("message",
                                 function(message) { alert(message.data); },
                                 false);
       </script>
     </body>

The instance then invokes <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a67e888a4e4e23effe7a09625e73ecae9" class="el" title="PostMessage() asynchronously invokes any listeners for message events on the DOM element for the give...">PostMessage()</a> as follows:

      PostMessage(pp::Var("Hello world!"));

The browser will pop-up an alert saying "Hello world!"

When passing array or dictionary `PP_Var`s, the entire reference graph will be converted and transferred. If the reference graph has cycles, the message will not be sent and an error will be logged to the console.

Listeners for message events in JavaScript code will receive an object conforming to the HTML 5 `MessageEvent` interface. Specifically, the value of message will be contained as a property called data in the received `MessageEvent`.

This messaging system is similar to the system used for listening for messages from Web Workers. Refer to `http://www.whatwg.org/specs/web-workers/current-work/` for further information.

Refer to <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5dce8c8b36b1df7cfcc12e42397a35e8" class="el" title="HandleMessage() is a function that the browser calls when PostMessage() is invoked on the DOM element...">HandleMessage()</a> for receiving events from JavaScript.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>message</td><td>A <code>Var</code> containing the data to be sent to JavaScript. Message can have a numeric, boolean, or string value. Array/Dictionary types are supported from Chrome M29 onward. All var types are copied when passing them to JavaScript.</td></tr></tbody></table>

<span id="aeb29ff4201f9ae0e356c5ed0bb4a2679" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>PP_Instance <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#aeb29ff4201f9ae0e356c5ed0bb4a2679" class="el">pp::Instance::pp_instance</a></td><td>(</td><td></td><td>)</td><td>const<code> [inline]</code></td></tr></tbody></table>

This function returns the `PP_Instance` identifying this object.

**Returns:**  
A `PP_Instance` identifying this object.

<span id="a5b5b1a66eda2d0e6884de8f7e25e2346" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5b5b1a66eda2d0e6884de8f7e25e2346" class="el">pp::Instance::RegisterMessageHandler</a></td><td>(</td><td><a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_message_handler/" class="el">MessageHandler</a> * </td><td><em>message_handler</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_message_loop/" class="el">MessageLoop</a> &amp; </td><td><em>message_loop</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

Dev-Channel Only.

Registers a handler for receiving messages from JavaScript. If a handler is registered this way, it will replace the <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance/" class="el">Instance</a>'s HandleMessage method, and all messages sent from JavaScript via postMessage and postMessageAndAwaitResponse will be dispatched to `message_handler`.

The function calls will be dispatched via `message_loop`. This means that the functions will be invoked on the thread to which `message_loop` is attached, when `message_loop` is run. It is illegal to pass the main thread message loop; RegisterMessageHandler will return PP\_ERROR\_WRONG\_THREAD in that case. If you quit `message_loop` before calling Unregister(), the browser will not be able to call functions in the plugin's message handler any more. That could mean missing some messages or could cause a leak if you depend on Destroy() to free hander data. So you should, whenever possible, Unregister() the handler prior to quitting its event loop.

Attempting to register a message handler when one is already registered will cause the current <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_message_handler/" class="el" title="MessageHandler is an abstract base class that the plugin may implement if it wants to receive message...">MessageHandler</a> to be unregistered and replaced. In that case, no messages will be sent to the "default" message handler (<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5dce8c8b36b1df7cfcc12e42397a35e8" class="el" title="HandleMessage() is a function that the browser calls when PostMessage() is invoked on the DOM element...">pp::Instance::HandleMessage()</a>). Messages will stop arriving at the prior message handler and will begin to be dispatched at the new message handler.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>message_handler</td><td>The plugin-provided object for handling messages. The instance does not take ownership of the pointer; it is up to the plugin to ensure that |message_handler| lives until its WasUnregistered() function is invoked.</td></tr><tr class="even"><td>[in]</td><td>message_loop</td><td>Represents the message loop on which <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_message_handler/" class="el" title="MessageHandler is an abstract base class that the plugin may implement if it wants to receive message...">MessageHandler</a>'s functions should be invoked.</td></tr></tbody></table>

<!-- -->

**Returns:**  
PP\_OK on success, or an error from pp\_errors.h.

<span id="a33c633189c7c321dac8e0c5dc6e67f5b" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a33c633189c7c321dac8e0c5dc6e67f5b" class="el">pp::Instance::RemovePerInstanceObject</a></td><td>(</td><td>const std::string &amp; </td><td><em>interface_name</em>,</td></tr><tr class="even"><td></td><td></td><td>void * </td><td><em>object</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

Refer to <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a9773263ee281405030548fc224eeec08" class="el" title="AddPerInstanceObject() associates an instance with an interface, creating an object.">AddPerInstanceObject()</a> for further information.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>interface_name</td><td>The name of the interface to associate with the instance</td></tr><tr class="even"><td>[in]</td><td>object</td><td></td></tr></tbody></table>

<span id="ad1b6c19954ff9446349a6fa5684eea2d" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>static void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a33c633189c7c321dac8e0c5dc6e67f5b" class="el">pp::Instance::RemovePerInstanceObject</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance_handle/" class="el">InstanceHandle</a> &amp; </td><td><em>instance</em>,</td></tr><tr class="even"><td></td><td></td><td>const std::string &amp; </td><td><em>interface_name</em>,</td></tr><tr class="odd"><td></td><td></td><td>void * </td><td><em>object</em> </td></tr><tr class="even"><td></td><td>)</td><td></td><td><code> [static]</code></td></tr></tbody></table>

Static version of AddPerInstanceObject that takes an <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance_handle/" class="el" title="An instance handle identifies an instance in a constructor for a resource.">InstanceHandle</a>.

As with all other instance functions, this must only be called on the main thread.

<span id="a6341c14fc54427e45349f5158483e017" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6341c14fc54427e45349f5158483e017" class="el">pp::Instance::RequestFilteringInputEvents</a></td><td>(</td><td>uint32_t </td><td><em>event_classes</em></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6341c14fc54427e45349f5158483e017" class="el" title="RequestFilteringInputEvents() requests that input events corresponding to the given input events are ...">RequestFilteringInputEvents()</a> requests that input events corresponding to the given input events are delivered to the instance for filtering.

By default, no input events are delivered. In most cases you would register to receive events by calling <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a2e2d63280786c0cc41b7c6f656cc81b5" class="el" title="RequestInputEvents() requests that input events corresponding to the given input events are delivered...">RequestInputEvents()</a>. In some cases, however, you may wish to filter events such that they can be bubbled up to the DOM. In this case, register for those classes of events using this function instead of <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a2e2d63280786c0cc41b7c6f656cc81b5" class="el" title="RequestInputEvents() requests that input events corresponding to the given input events are delivered...">RequestInputEvents()</a>. Keyboard events must always be registered in filtering mode.

Filtering input events requires significantly more overhead than just delivering them to the instance. As such, you should only request filtering in those cases where it's absolutely necessary. The reason is that it requires the browser to stop and block for the instance to handle the input event, rather than sending the input event asynchronously. This can have significant overhead.

**Example:**

       RequestInputEvents(PP_INPUTEVENT_CLASS_MOUSE);
       RequestFilteringInputEvents(
           PP_INPUTEVENT_CLASS_WHEEL | PP_INPUTEVENT_CLASS_KEYBOARD);

**Parameters:**  
<table><tbody><tr class="odd"><td>event_classes</td><td>A combination of flags from <code>PP_InputEvent_Class</code> that identifies the classes of events the instance is requesting. The flags are combined by logically ORing their values.</td></tr></tbody></table>

<!-- -->

**Returns:**  
`PP_OK` if the operation succeeded, `PP_ERROR_BADARGUMENT` if instance is invalid, or `PP_ERROR_NOTSUPPORTED` if one of the event class bits were illegal. In the case of an invalid bit, all valid bits will be applied and only the illegal bits will be ignored.

<span id="a2e2d63280786c0cc41b7c6f656cc81b5" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a2e2d63280786c0cc41b7c6f656cc81b5" class="el">pp::Instance::RequestInputEvents</a></td><td>(</td><td>uint32_t </td><td><em>event_classes</em></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a2e2d63280786c0cc41b7c6f656cc81b5" class="el" title="RequestInputEvents() requests that input events corresponding to the given input events are delivered...">RequestInputEvents()</a> requests that input events corresponding to the given input events are delivered to the instance.

By default, no input events are delivered. Call this function with the classes of events you are interested in to have them be delivered to the instance. Calling this function will override any previous setting for each specified class of input events (for example, if you previously called <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a6341c14fc54427e45349f5158483e017" class="el" title="RequestFilteringInputEvents() requests that input events corresponding to the given input events are ...">RequestFilteringInputEvents()</a>, this function will set those events to non-filtering mode).

Input events may have high overhead, so you should only request input events that your plugin will actually handle. For example, the browser may do optimizations for scroll or touch events that can be processed substantially faster if it knows there are no non-default receivers for that message. Requesting that such messages be delivered, even if they are processed very quickly, may have a noticeable effect on the performance of the page.

When requesting input events through this function, the events will be delivered and *not* bubbled to the page. This means that even if you aren't interested in the message, no other parts of the page will get the message.

**Example:**

       RequestInputEvents(PP_INPUTEVENT_CLASS_MOUSE);
       RequestFilteringInputEvents(
           PP_INPUTEVENT_CLASS_WHEEL | PP_INPUTEVENT_CLASS_KEYBOARD);

**Parameters:**  
<table><tbody><tr class="odd"><td>event_classes</td><td>A combination of flags from <code>PP_InputEvent_Class</code> that identifies the classes of events the instance is requesting. The flags are combined by logically ORing their values.</td></tr></tbody></table>

<!-- -->

**Returns:**  
`PP_OK` if the operation succeeded, `PP_ERROR_BADARGUMENT` if instance is invalid, or `PP_ERROR_NOTSUPPORTED` if one of the event class bits were illegal. In the case of an invalid bit, all valid bits will be applied and only the illegal bits will be ignored.

<span id="a5e37f26ebc58915574819542a41a6329" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5e37f26ebc58915574819542a41a6329" class="el">pp::Instance::UnregisterMessageHandler</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

Unregisters the current message handler for this instance if one is registered.

After this call, the message handler (if one was registered) will have "WasUnregistered" called on it and will receive no further messages. After that point, all messages sent from JavaScript using postMessage() will be dispatched to <a href="/docs/native-client/pepper_stable/cpp/classpp_1_1_instance#a5dce8c8b36b1df7cfcc12e42397a35e8" class="el" title="HandleMessage() is a function that the browser calls when PostMessage() is invoked on the DOM element...">pp::Instance::HandleMessage()</a> on the main thread. Attempts to call postMessageAndAwaitResponse() from JavaScript after that point will fail.

Attempting to unregister a message handler when none is registered has no effect.

------------------------------------------------------------------------

The documentation for this class was generated from the following file:

-   <a href="/docs/native-client/pepper_stable/cpp/instance_8h/" class="el">instance.h</a>