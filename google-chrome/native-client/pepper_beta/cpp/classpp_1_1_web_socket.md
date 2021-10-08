---json {"title":"pp::WebSocket Class Reference"} ---

Inheritance diagram for pp::WebSocket:

![Inheritance graph](/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket__inherit__graph.png)

<span class="legend">\[[legend](/docs/native-client/pepper_beta/cpp/graph_legend/)\]</span>

[List of all members.](/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket-members/)

Public Member Functions
-----------------------

<table><tbody><tr class="odd"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#aeaac3a412a9015a9378beec9f42d5809" class="el">WebSocket</a> (const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">InstanceHandle</a> &amp;instance)</td></tr><tr class="even"><td style="text-align: right;">virtual </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#aa4810e4b945c1fc92493dc206eb35c09" class="el">~WebSocket</a> ()</td></tr><tr class="odd"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ad8471399bfca7df23b87ded733d53141" class="el">Connect</a> (const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp;url, const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> protocols[], uint32_t protocol_count, const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp;callback)</td></tr><tr class="even"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ae7913ea4019cc2a10c9a0390c5959071" class="el">Close</a> (uint16_t code, const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp;reason, const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp;callback)</td></tr><tr class="odd"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el">ReceiveMessage</a> (<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> *message, const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp;callback)</td></tr><tr class="even"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a276b1aae76ba9d899475aaf9c2cd4f28" class="el">SendMessage</a> (const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp;message)</td></tr><tr class="odd"><td style="text-align: right;">uint64_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#aee920e33ef266c51ffdaeba8d6924e19" class="el">GetBufferedAmount</a> ()</td></tr><tr class="even"><td style="text-align: right;">uint16_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab1bb565b7800fd3c147177e4e3a3466f" class="el">GetCloseCode</a> ()</td></tr><tr class="odd"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a27c9cf6d130706fcc5e6fe2f9ed51a7b" class="el">GetCloseReason</a> ()</td></tr><tr class="even"><td style="text-align: right;">bool </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a092b63f716b3e02fc8ec0696ac58df84" class="el">GetCloseWasClean</a> ()</td></tr><tr class="odd"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab22093b22b7ceea6957047e1cb5967d2" class="el">GetExtensions</a> ()</td></tr><tr class="even"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1c4b81bb05d30fdef67a07ac904abf0f" class="el">GetProtocol</a> ()</td></tr><tr class="odd"><td style="text-align: right;">PP_WebSocketReadyState </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#afa09ce5acb5f7f168f17b8b3f5939317" class="el">GetReadyState</a> ()</td></tr><tr class="even"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab76ccebfe20facff03464e71f4af7719" class="el">GetURL</a> ()</td></tr></tbody></table>

------------------------------------------------------------------------

<span id="details" class="anchor" style="margin: 0;"></span>

Detailed Description
--------------------

The `WebSocket` class providing bi-directional, full-duplex, communications over a single TCP socket.

------------------------------------------------------------------------

Constructor & Destructor Documentation
--------------------------------------

<span id="aeaac3a412a9015a9378beec9f42d5809" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#aeaac3a412a9015a9378beec9f42d5809" class="el">pp::WebSocket::WebSocket</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_instance_handle/" class="el">InstanceHandle</a> &amp; </td><td><em>instance</em></td><td>)</td><td><code> [explicit]</code></td></tr></tbody></table>

Constructs a <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> object.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>instance</td><td>The instance with which this resource will be associated.</td></tr></tbody></table>

<span id="aa4810e4b945c1fc92493dc206eb35c09" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#aa4810e4b945c1fc92493dc206eb35c09" class="el">pp::WebSocket::~WebSocket</a></td><td>(</td><td></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

Destructs a <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> object.

------------------------------------------------------------------------

Member Function Documentation
-----------------------------

<span id="ae7913ea4019cc2a10c9a0390c5959071" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ae7913ea4019cc2a10c9a0390c5959071" class="el">pp::WebSocket::Close</a></td><td>(</td><td>uint16_t </td><td><em>code</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>reason</em>,</td></tr><tr class="odd"><td></td><td></td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp; </td><td><em>callback</em> </td></tr><tr class="even"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ae7913ea4019cc2a10c9a0390c5959071" class="el" title="Close() closes the specified WebSocket connection by specifying code and reason.">Close()</a> closes the specified <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection by specifying `code` and `reason`.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>code</td><td>The <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> close code. This is ignored if it is 0. <code>PP_WEBSOCKETSTATUSCODE_NORMAL_CLOSURE</code> must be used for the usual case. To indicate some specific error cases, codes in the range <code>PP_WEBSOCKETSTATUSCODE_USER_REGISTERED_MIN</code> to <code>PP_WEBSOCKETSTATUSCODE_USER_REGISTERED_MAX</code>, and in the range <code>PP_WEBSOCKETSTATUSCODE_USER_PRIVATE_MIN</code> to <code>PP_WEBSOCKETSTATUSCODE_USER_PRIVATE_MAX</code> are available.</td></tr><tr class="even"><td>[in]</td><td>reason</td><td>A <code>Var</code> of string type representing the close reason. This is ignored if it is an undefined type.</td></tr><tr class="odd"><td>[in]</td><td>callback</td><td>A <code>CompletionCallback</code> called when the connection is closed or an error occurs in closing the connection.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`. Returns `PP_ERROR_BADARGUMENT` if `reason` contains an invalid character as a UTF-8 string, or is longer than 123 bytes. `PP_ERROR_BADARGUMENT` corresponds to a JavaScript SyntaxError in the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> API specification. Returns `PP_ERROR_NOACCESS` if the code is not an integer equal to 1000 or in the range 3000 to 4999. `PP_ERROR_NOACCESS` corresponds to an InvalidAccessError in the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> API specification. Returns `PP_ERROR_INPROGRESS` if a previous call to <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ae7913ea4019cc2a10c9a0390c5959071" class="el" title="Close() closes the specified WebSocket connection by specifying code and reason.">Close()</a> is not finished.

<span id="ad8471399bfca7df23b87ded733d53141" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ad8471399bfca7df23b87ded733d53141" class="el">pp::WebSocket::Connect</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>url</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> </td><td><em>protocols</em>[],</td></tr><tr class="odd"><td></td><td></td><td>uint32_t </td><td><em>protocol_count</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp; </td><td><em>callback</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ad8471399bfca7df23b87ded733d53141" class="el" title="Connect() connects to the specified WebSocket server.">Connect()</a> connects to the specified <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> server.

You can call this function once for an object.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>url</td><td>A <code>Var</code> of string type representing a <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> server URL.</td></tr><tr class="even"><td>[in]</td><td>protocols</td><td>A pointer to an array of <code>Var</code> of string type specifying sub-protocols. Each <code>Var</code> represents one sub-protocol. This argument can be null only if <code>protocol_count</code> is 0.</td></tr><tr class="odd"><td>[in]</td><td>protocol_count</td><td>The number of sub-protocols in <code>protocols</code>.</td></tr><tr class="even"><td>[in]</td><td>callback</td><td>A <code>CompletionCallback</code> called when a connection is established or an error occurs in establishing connection.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`. Returns `PP_ERROR_BADARGUMENT` if specified `url`, or `protocols` contains invalid string as defined in the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> API specification. `PP_ERROR_BADARGUMENT` corresponds to a SyntaxError in the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> API specification. Returns `PP_ERROR_NOACCESS` if the protocol specified in the `url` is not a secure protocol, but the origin of the caller has a secure scheme. Also returns `PP_ERROR_NOACCESS` if the port specified in the `url` is a port that the user agent is configured to block access to because it is a well-known port like SMTP. `PP_ERROR_NOACCESS` corresponds to a SecurityError of the specification. Returns `PP_ERROR_INPROGRESS` if this is not the first call to <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ad8471399bfca7df23b87ded733d53141" class="el" title="Connect() connects to the specified WebSocket server.">Connect()</a>.

<span id="aee920e33ef266c51ffdaeba8d6924e19" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>uint64_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#aee920e33ef266c51ffdaeba8d6924e19" class="el">pp::WebSocket::GetBufferedAmount</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#aee920e33ef266c51ffdaeba8d6924e19" class="el" title="GetBufferedAmount() returns the number of bytes of text and binary messages that have been queued for...">GetBufferedAmount()</a> returns the number of bytes of text and binary messages that have been queued for the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection to send, but have not been transmitted to the network yet.

**Returns:**  
Returns the number of bytes.

<span id="ab1bb565b7800fd3c147177e4e3a3466f" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>uint16_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab1bb565b7800fd3c147177e4e3a3466f" class="el">pp::WebSocket::GetCloseCode</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab1bb565b7800fd3c147177e4e3a3466f" class="el" title="GetCloseCode() returns the connection close code for the WebSocket connection.">GetCloseCode()</a> returns the connection close code for the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection.

**Returns:**  
Returns 0 if called before the close code is set.

<span id="a27c9cf6d130706fcc5e6fe2f9ed51a7b" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a27c9cf6d130706fcc5e6fe2f9ed51a7b" class="el">pp::WebSocket::GetCloseReason</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a27c9cf6d130706fcc5e6fe2f9ed51a7b" class="el" title="GetCloseReason() returns the connection close reason for the WebSocket connection.">GetCloseReason()</a> returns the connection close reason for the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection.

**Returns:**  
Returns a `Var` of string type. If called before the close reason is set, the return value contains an empty string. Returns a `PP_VARTYPE_UNDEFINED` if called on an invalid resource.

<span id="a092b63f716b3e02fc8ec0696ac58df84" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>bool <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a092b63f716b3e02fc8ec0696ac58df84" class="el">pp::WebSocket::GetCloseWasClean</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a092b63f716b3e02fc8ec0696ac58df84" class="el" title="GetCloseWasClean() returns if the connection was closed cleanly for the specified WebSocket connectio...">GetCloseWasClean()</a> returns if the connection was closed cleanly for the specified <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection.

**Returns:**  
Returns `false` if called before the connection is closed, called on an invalid resource, or closed for abnormal reasons. Otherwise, returns `true` if the connection was closed cleanly.

<span id="ab22093b22b7ceea6957047e1cb5967d2" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab22093b22b7ceea6957047e1cb5967d2" class="el">pp::WebSocket::GetExtensions</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab22093b22b7ceea6957047e1cb5967d2" class="el" title="GetExtensions() returns the extensions selected by the server for the specified WebSocket connection...">GetExtensions()</a> returns the extensions selected by the server for the specified <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection.

**Returns:**  
Returns a `Var` of string type. If called before the connection is established, the `Var`'s data is an empty string. Returns a `PP_VARTYPE_UNDEFINED` if called on an invalid resource. Currently the `Var`'s data for valid resources are always an empty string.

<span id="a1c4b81bb05d30fdef67a07ac904abf0f" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1c4b81bb05d30fdef67a07ac904abf0f" class="el">pp::WebSocket::GetProtocol</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1c4b81bb05d30fdef67a07ac904abf0f" class="el" title="GetProtocol() returns the sub-protocol chosen by the server for the specified WebSocket connection...">GetProtocol()</a> returns the sub-protocol chosen by the server for the specified <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection.

**Returns:**  
Returns a `Var` of string type. If called before the connection is established, the `Var` contains the empty string. Returns a code&gt;PP\_VARTYPE\_UNDEFINED if called on an invalid resource.

<span id="afa09ce5acb5f7f168f17b8b3f5939317" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>PP_WebSocketReadyState <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#afa09ce5acb5f7f168f17b8b3f5939317" class="el">pp::WebSocket::GetReadyState</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#afa09ce5acb5f7f168f17b8b3f5939317" class="el" title="GetReadyState() returns the ready state of the specified WebSocket connection.">GetReadyState()</a> returns the ready state of the specified <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection.

**Returns:**  
Returns `PP_WEBSOCKETREADYSTATE_INVALID` if called before <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ad8471399bfca7df23b87ded733d53141" class="el" title="Connect() connects to the specified WebSocket server.">Connect()</a> is called, or if this function is called on an invalid resource.

<span id="ab76ccebfe20facff03464e71f4af7719" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab76ccebfe20facff03464e71f4af7719" class="el">pp::WebSocket::GetURL</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#ab76ccebfe20facff03464e71f4af7719" class="el" title="GetURL() returns the URL associated with specified WebSocket connection.">GetURL()</a> returns the URL associated with specified <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> connection.

**Returns:**  
Returns a `Var` of string type. If called before the connection is established, the `Var` contains the empty string. Returns a `PP_VARTYPE_UNDEFINED` if this function is called on an invalid resource.

<span id="a1eb972115700589ebf6998db4f411c56" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el">pp::WebSocket::ReceiveMessage</a></td><td>(</td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> * </td><td><em>message</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp; </td><td><em>callback</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el" title="ReceiveMessage() receives a message from the WebSocket server.">ReceiveMessage()</a> receives a message from the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> server.

This interface only returns a single message. That is, this interface must be called at least N times to receive N messages, no matter the size of each message.

**Parameters:**  
<table><tbody><tr class="odd"><td>[out]</td><td>message</td><td>The received message is copied to provided <code>message</code>. The <code>message</code> must remain valid until <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el" title="ReceiveMessage() receives a message from the WebSocket server.">ReceiveMessage()</a> completes. Its received <code>Var</code> will be of string or ArrayBuffer type.</td></tr><tr class="even"><td>[in]</td><td>callback</td><td>A <code>CompletionCallback</code> called when <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el" title="ReceiveMessage() receives a message from the WebSocket server.">ReceiveMessage()</a> completes. This callback is ignored if <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el" title="ReceiveMessage() receives a message from the WebSocket server.">ReceiveMessage()</a> completes synchronously and returns <code>PP_OK</code>.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`. If an error is detected or connection is closed, <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el" title="ReceiveMessage() receives a message from the WebSocket server.">ReceiveMessage()</a> returns `PP_ERROR_FAILED` after all buffered messages are received. Until buffered message become empty, <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a1eb972115700589ebf6998db4f411c56" class="el" title="ReceiveMessage() receives a message from the WebSocket server.">ReceiveMessage()</a> continues to return `PP_OK` as if connection is still established without errors.

<span id="a276b1aae76ba9d899475aaf9c2cd4f28" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a276b1aae76ba9d899475aaf9c2cd4f28" class="el">pp::WebSocket::SendMessage</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_var/" class="el">Var</a> &amp; </td><td><em>message</em></td><td>)</td><td></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket#a276b1aae76ba9d899475aaf9c2cd4f28" class="el" title="SendMessage() sends a message to the WebSocket server.">SendMessage()</a> sends a message to the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> server.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>message</td><td>A message to send. The message is copied to an internal buffer, so the caller can free <code>message</code> safely after returning from the function. This <code>Var</code> must be of string or ArrayBuffer types.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`. Returns `PP_ERROR_FAILED` if the ReadyState is `PP_WEBSOCKETREADYSTATE_CONNECTING`. `PP_ERROR_FAILED` corresponds to a JavaScript InvalidStateError in the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> API specification. Returns `PP_ERROR_BADARGUMENT` if the provided `message` contains an invalid character as a UTF-8 string. `PP_ERROR_BADARGUMENT` corresponds to a JavaScript SyntaxError in the <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_web_socket/" class="el" title="The WebSocket class providing bi-directional, full-duplex, communications over a single TCP socket...">WebSocket</a> API specification. Otherwise, returns `PP_OK`, but it doesn't necessarily mean that the server received the message.

------------------------------------------------------------------------

The documentation for this class was generated from the following file:

-   <a href="/docs/native-client/pepper_beta/cpp/websocket_8h/" class="el">websocket.h</a>