---json {"title":"pp::MessageHandler Class Reference"} ---

[List of all members.](/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler-members/)

Public Member Functions
-----------------------

<table><tbody><tr class="odd"><td style="text-align: right;">virtual </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#a7dca8d4b899382782aaa163fb2654b83" class="el">~MessageHandler</a> ()</td></tr><tr class="even"><td style="text-align: right;">virtual void </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#a1040f95297420067a69000612bbe6c06" class="el">HandleMessage</a> (<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">pp::InstanceHandle</a> instance, const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp;message_data)=0</td></tr><tr class="odd"><td style="text-align: right;">virtual <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">pp::Var</a> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#a37212226dba86f1bf900016116fabdfe" class="el">HandleBlockingMessage</a> (<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">pp::InstanceHandle</a> instance, const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp;message_data)=0</td></tr><tr class="even"><td style="text-align: right;">virtual void </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#ac19edb6318796c337865e39d764ed322" class="el">WasUnregistered</a> (<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">pp::InstanceHandle</a> instance)=0</td></tr></tbody></table>

------------------------------------------------------------------------

<span id="details" class="anchor" style="margin: 0;"></span>

Detailed Description
--------------------

`MessageHandler` is an abstract base class that the plugin may implement if it wants to receive messages from JavaScript on a background thread when JavaScript invokes postMessage() or postMessageAndAwaitResponse().

See <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance#a5b5b1a66eda2d0e6884de8f7e25e2346" class="el" title="Dev-Channel Only.">pp::Instance::RegisterMessageHandler()</a> for usage.

------------------------------------------------------------------------

Constructor & Destructor Documentation
--------------------------------------

<span id="a7dca8d4b899382782aaa163fb2654b83" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#a7dca8d4b899382782aaa163fb2654b83" class="el">pp::MessageHandler::~MessageHandler</a></td><td>(</td><td></td><td>)</td><td><code> [inline, virtual]</code></td></tr></tbody></table>

------------------------------------------------------------------------

Member Function Documentation
-----------------------------

<span id="a37212226dba86f1bf900016116fabdfe" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">pp::Var</a> <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#a37212226dba86f1bf900016116fabdfe" class="el">pp::MessageHandler::HandleBlockingMessage</a></td><td>(</td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">pp::InstanceHandle</a> </td><td><em>instance</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>message_data</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td><code> [pure virtual]</code></td></tr></tbody></table>

Invoked as a result of JavaScript invoking postMessageAndAwaitResponse() on the plugin's DOM element.

NOTE: JavaScript execution is blocked during the duration of this call. Hence, the plugin should respond as quickly as possible. For this reason, blocking completion callbacks are disallowed while handling a blocking message.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>instance</td><td>An <code>InstanceHandle</code> identifying one instance of a module.</td></tr><tr class="even"><td>[in]</td><td>message_data</td><td>A copy of the parameter that JavaScript provided to postMessage().</td></tr></tbody></table>

<!-- -->

**Returns:**  
Returns a <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el" title="A generic type used for passing data types between the module and the page.">pp::Var</a> that is then copied to a JavaScript object which is returned as the result of JavaScript's call of postMessageAndAwaitResponse().

<span id="a1040f95297420067a69000612bbe6c06" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual void <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#a1040f95297420067a69000612bbe6c06" class="el">pp::MessageHandler::HandleMessage</a></td><td>(</td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">pp::InstanceHandle</a> </td><td><em>instance</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>message_data</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td><code> [pure virtual]</code></td></tr></tbody></table>

Invoked as a result of JavaScript invoking postMessage() on the plugin's DOM element.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>instance</td><td>An <code>InstanceHandle</code> identifying one instance of a module.</td></tr><tr class="even"><td>[in]</td><td>message_data</td><td>A copy of the parameter that JavaScript provided to postMessage().</td></tr></tbody></table>

<span id="ac19edb6318796c337865e39d764ed322" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual void <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler#ac19edb6318796c337865e39d764ed322" class="el">pp::MessageHandler::WasUnregistered</a></td><td>(</td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">pp::InstanceHandle</a> </td><td><em>instance</em></td><td>)</td><td><code> [pure virtual]</code></td></tr></tbody></table>

Invoked when this <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_message_handler/" class="el" title="MessageHandler is an abstract base class that the plugin may implement if it wants to receive message...">MessageHandler</a> is no longer needed.

After this, no more calls will be made to this object.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>instance</td><td>An <code>InstanceHandle</code> identifying one instance of a module.</td></tr></tbody></table>

------------------------------------------------------------------------

The documentation for this class was generated from the following file:

-   <a href="/docs/native-client/pepper_beta/cpp/message__handler_8h/" class="el">message_handler.h</a>