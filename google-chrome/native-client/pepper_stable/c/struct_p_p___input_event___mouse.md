---json {"title":"PP\_InputEvent\_Mouse Struct Reference"} ---

Data Fields
-----------

<table><tbody><tr class="odd"><td style="text-align: right;">uint32_t </td><td><a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#ade5934096b842e08d4a2b5361efde0ba" class="el">modifier</a></td></tr><tr class="even"><td style="text-align: right;"><a href="/docs/native-client/pepper_stable/c/group___enums#ga25113f3c8d33e863fd38b3f70f8a5e6e" class="el">PP_InputEvent_MouseButton</a> </td><td><a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#a09969e4a48363691517970cd8b374e84" class="el">button</a></td></tr><tr class="odd"><td style="text-align: right;">float </td><td><a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#a12569a7a8bff2107c2a2d67376d26c07" class="el">x</a></td></tr><tr class="even"><td style="text-align: right;">float </td><td><a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#a19be12e2e7b9007209594ce85912b398" class="el">y</a></td></tr><tr class="odd"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#ad608b42b29ff4f93f63e7dee287ad1d9" class="el">click_count</a></td></tr></tbody></table>

------------------------------------------------------------------------

<span id="details" class="anchor" style="margin: 0;"></span>

Detailed Description
--------------------

The `PP_InputEvent_Mouse` struct represents all mouse events except mouse wheel events.

------------------------------------------------------------------------

Field Documentation
-------------------

<span id="a09969e4a48363691517970cd8b374e84" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_stable/c/group___enums#ga25113f3c8d33e863fd38b3f70f8a5e6e" class="el">PP_InputEvent_MouseButton</a> <a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#a09969e4a48363691517970cd8b374e84" class="el">PP_InputEvent_Mouse::button</a></td></tr></tbody></table>

This value represents the button that changed for mouse down or up events.

This value will be `PP_EVENT_MOUSEBUTTON_NONE` for mouse move, enter, and leave events.

<span id="ad608b42b29ff4f93f63e7dee287ad1d9" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#ad608b42b29ff4f93f63e7dee287ad1d9" class="el">PP_InputEvent_Mouse::click_count</a></td></tr></tbody></table>

<span id="ade5934096b842e08d4a2b5361efde0ba" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>uint32_t <a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#ade5934096b842e08d4a2b5361efde0ba" class="el">PP_InputEvent_Mouse::modifier</a></td></tr></tbody></table>

This value is a bit field combination of the `PP_InputEvent_Modifier` flags.

<span id="a12569a7a8bff2107c2a2d67376d26c07" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>float <a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#a12569a7a8bff2107c2a2d67376d26c07" class="el">PP_InputEvent_Mouse::x</a></td></tr></tbody></table>

This values represents the x coordinate of the mouse when the event occurred.

In most, but not all, cases these coordinates will just be integers. For example, the plugin element might be arbitrarily scaled or transformed in the DOM, and translating a mouse event into the coordinate space of the plugin will give non-integer values.

<span id="a19be12e2e7b9007209594ce85912b398" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>float <a href="/docs/native-client/pepper_stable/c/struct_p_p___input_event___mouse#a19be12e2e7b9007209594ce85912b398" class="el">PP_InputEvent_Mouse::y</a></td></tr></tbody></table>

This values represents the y coordinate of the mouse when the event occurred.

In most, but not all, cases these coordinates will just be integers. For example, the plugin element might be arbitrarily scaled or transformed in the DOM, and translating a mouse event into the coordinate space of the plugin will give non-integer values.

------------------------------------------------------------------------

The documentation for this struct was generated from the following file:

-   <a href="/docs/native-client/pepper_stable/c/pp__input__event_8h/" class="el">pp_input_event.h</a>