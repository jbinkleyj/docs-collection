---json {"title":"PPB_MouseInputEvent Struct Reference"} ---

## Data Fields

<table><tbody><tr class="odd"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a>(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a3bde5af35e13f10a3472132e82b8bb45" class="el">Create</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#ga89b662403e6a687bb914b80114c0d19d" class="el">PP_Instance</a> instance, <a href="/docs/native-client/pepper_beta/c/group___enums#gaca7296cfec99fcb6646b7144d1d6a0c5" class="el">PP_InputEvent_Type</a> type, <a href="/docs/native-client/pepper_beta/c/group___typedefs#ga71cb1042cdeb38d7881b121f3b09ce94" class="el">PP_TimeTicks</a> time_stamp, uint32_t modifiers, <a href="/docs/native-client/pepper_beta/c/group___enums#ga25113f3c8d33e863fd38b3f70f8a5e6e" class="el">PP_InputEvent_MouseButton</a> mouse_button, const struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a> *mouse_position, int32_t click_count, const struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a> *mouse_movement)</td></tr><tr class="even"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/c/group___enums#ga4f272d99be14aacafe08dfd4ef830918" class="el">PP_Bool</a>(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a4cf50f1f5527cf7e66788d4b47ae1638" class="el">IsMouseInputEvent</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> resource)</td></tr><tr class="odd"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/c/group___enums#ga25113f3c8d33e863fd38b3f70f8a5e6e" class="el">PP_InputEvent_MouseButton</a>(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a7a90bf6abb794ca5c42af76d8fd71d22" class="el">GetButton</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)</td></tr><tr class="even"><td style="text-align: right;">struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a>(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#ab7c3f20bd61bec3db563a7956fdeb7e0" class="el">GetPosition</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)</td></tr><tr class="odd"><td style="text-align: right;">int32_t(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a2850b783ad0136b5818d876a1a01af22" class="el">GetClickCount</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)</td></tr><tr class="even"><td style="text-align: right;">struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a>(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a043229000d9f7d9436ae8a963bb6aca1" class="el">GetMovement</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)</td></tr></tbody></table>

---

<span id="details" class="anchor" style="margin: 0;"></span>

## Detailed Description

The `PPB_MouseInputEvent` interface contains pointers to several functions related to mouse input events.

---

## Field Documentation

<span id="a3bde5af35e13f10a3472132e82b8bb45" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a>(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a3bde5af35e13f10a3472132e82b8bb45" class="el">PPB_MouseInputEvent::Create</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#ga89b662403e6a687bb914b80114c0d19d" class="el">PP_Instance</a> instance, <a href="/docs/native-client/pepper_beta/c/group___enums#gaca7296cfec99fcb6646b7144d1d6a0c5" class="el">PP_InputEvent_Type</a> type, <a href="/docs/native-client/pepper_beta/c/group___typedefs#ga71cb1042cdeb38d7881b121f3b09ce94" class="el">PP_TimeTicks</a> time_stamp, uint32_t modifiers, <a href="/docs/native-client/pepper_beta/c/group___enums#ga25113f3c8d33e863fd38b3f70f8a5e6e" class="el">PP_InputEvent_MouseButton</a> mouse_button, const struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a> *mouse_position, int32_t click_count, const struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a> *mouse_movement)</td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a3bde5af35e13f10a3472132e82b8bb45" class="el" title="Create() creates a mouse input event with the given parameters.">Create()</a> creates a mouse input event with the given parameters.

Normally you will get a mouse event passed through the `HandleInputEvent` and will not need to create them, but some applications may want to create their own for internal use. The type must be one of the mouse event types.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>instance</td><td>The instance for which this event occurred.</td></tr><tr class="even"><td>[in]</td><td>type</td><td>A <code>PP_InputEvent_Type</code> identifying the type of input event.</td></tr><tr class="odd"><td>[in]</td><td>time_stamp</td><td>A <code>PP_TimeTicks</code> indicating the time when the event occurred.</td></tr><tr class="even"><td>[in]</td><td>modifiers</td><td>A bit field combination of the <code>PP_InputEvent_Modifier</code> flags.</td></tr><tr class="odd"><td>[in]</td><td>mouse_button</td><td>The button that changed for mouse down or up events. This value will be <code>PP_EVENT_MOUSEBUTTON_NONE</code> for mouse move, enter, and leave events.</td></tr><tr class="even"><td>[in]</td><td>mouse_position</td><td>A <code>Point</code> containing the x and y position of the mouse when the event occurred.</td></tr><tr class="odd"><td>[in]</td><td>mouse_movement</td><td>The change in position of the mouse.</td></tr></tbody></table>

<!-- -->

**Returns:**  
A `PP_Resource` containing the new mouse input event.

<span id="a7a90bf6abb794ca5c42af76d8fd71d22" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/c/group___enums#ga25113f3c8d33e863fd38b3f70f8a5e6e" class="el">PP_InputEvent_MouseButton</a>(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a7a90bf6abb794ca5c42af76d8fd71d22" class="el">PPB_MouseInputEvent::GetButton</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)</td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a7a90bf6abb794ca5c42af76d8fd71d22" class="el" title="GetButton() returns the mouse button that generated a mouse down or up event.">GetButton()</a> returns the mouse button that generated a mouse down or up event.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>mouse_event</td><td>A <code>PP_Resource</code> corresponding to a mouse event.</td></tr></tbody></table>

<!-- -->

**Returns:**  
The mouse button associated with mouse down and up events. This value will be `PP_EVENT_MOUSEBUTTON_NONE` for mouse move, enter, and leave events, and for all non-mouse events.

<span id="a2850b783ad0136b5818d876a1a01af22" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a2850b783ad0136b5818d876a1a01af22" class="el">PPB_MouseInputEvent::GetClickCount</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)</td></tr></tbody></table>

<span id="a043229000d9f7d9436ae8a963bb6aca1" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a>(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a043229000d9f7d9436ae8a963bb6aca1" class="el">PPB_MouseInputEvent::GetMovement</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)<code> [read]</code></td></tr></tbody></table>

Returns the change in position of the mouse.

When the mouse is locked, although the mouse position doesn't actually change, this function still provides movement information, which indicates what the change in position would be had the mouse not been locked.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>mouse_event</td><td>A <code>PP_Resource</code> corresponding to a mouse event.</td></tr></tbody></table>

<!-- -->

**Returns:**  
The change in position of the mouse, relative to the previous position.

<span id="ab7c3f20bd61bec3db563a7956fdeb7e0" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>struct <a href="/docs/native-client/pepper_beta/c/struct_p_p___point/" class="el">PP_Point</a>(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#ab7c3f20bd61bec3db563a7956fdeb7e0" class="el">PPB_MouseInputEvent::GetPosition</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> mouse_event)<code> [read]</code></td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#ab7c3f20bd61bec3db563a7956fdeb7e0" class="el" title="GetPosition() returns the pixel location of a mouse input event.">GetPosition()</a> returns the pixel location of a mouse input event.

When the mouse is locked, it returns the last known mouse position just as mouse lock was entered.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>mouse_event</td><td>A <code>PP_Resource</code> corresponding to a mouse event.</td></tr></tbody></table>

<!-- -->

**Returns:**  
The point associated with the mouse event, relative to the upper- left of the instance receiving the event. These values can be negative for mouse drags. The return value will be (0, 0) for non-mouse events.

<span id="a4cf50f1f5527cf7e66788d4b47ae1638" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/c/group___enums#ga4f272d99be14aacafe08dfd4ef830918" class="el">PP_Bool</a>(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a4cf50f1f5527cf7e66788d4b47ae1638" class="el">PPB_MouseInputEvent::IsMouseInputEvent</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> resource)</td></tr></tbody></table>

<a href="/docs/native-client/pepper_beta/c/struct_p_p_b___mouse_input_event__1__1#a4cf50f1f5527cf7e66788d4b47ae1638" class="el" title="IsMouseInputEvent() determines if a resource is a mouse event.">IsMouseInputEvent()</a> determines if a resource is a mouse event.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>resource</td><td>A <code>PP_Resource</code> corresponding to an event.</td></tr></tbody></table>

<!-- -->

**Returns:**  
`PP_TRUE` if the given resource is a valid mouse input event, otherwise `PP_FALSE`.

---

The documentation for this struct was generated from the following file:

- <a href="/docs/native-client/pepper_beta/c/ppb__input__event_8h/" class="el">ppb_input_event.h</a>