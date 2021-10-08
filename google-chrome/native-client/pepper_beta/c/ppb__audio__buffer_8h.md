---json {"title":"ppb\_audio\_buffer.h File Reference"} ---

Include dependency graph for ppb\_audio\_buffer.h:

![](/docs/native-client/pepper_beta/c/ppb__audio__buffer_8h__incl.png)

Data Structures
---------------

<table><tbody><tr class="odd"><td style="text-align: right;">struct  </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___audio_buffer__0__1/" class="el">PPB_AudioBuffer</a></td></tr></tbody></table>

Defines
-------

<table><tbody><tr class="odd"><td style="text-align: right;">#define </td><td><a href="/docs/native-client/pepper_beta/c/ppb__audio__buffer_8h#a4fddf6d285021552ba11f4460ba47445" class="el">PPB_AUDIOBUFFER_INTERFACE</a>   "PPB_AudioBuffer;0.1"</td></tr><tr class="even"><td style="text-align: right;">#define </td><td><a href="/docs/native-client/pepper_beta/c/ppb__audio__buffer_8h#a97463b49d90a036ddcb00968c33a8dfa" class="el">PPB_AUDIOBUFFER_INTERFACE</a>   <a href="/docs/native-client/pepper_beta/c/ppb__audio__buffer_8h#a4fddf6d285021552ba11f4460ba47445" class="el">PPB_AUDIOBUFFER_INTERFACE</a></td></tr></tbody></table>

Typedefs
--------

<table><tbody><tr class="odd"><td style="text-align: right;">typedef struct <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___audio_buffer__0__1/" class="el">PPB_AudioBuffer</a> </td><td><a href="/docs/native-client/pepper_beta/c/group___interfaces#gab91267a49328e3664e2e9d3410fbf624" class="el">PPB_AudioBuffer</a></td></tr></tbody></table>

Enumerations
------------

<table><tbody><tr class="odd"><td style="text-align: right;">enum  </td><td><a href="/docs/native-client/pepper_beta/c/group___enums#ga78757d4be14d14d17708071a9466afbd" class="el">PP_AudioBuffer_SampleRate</a> {<br />
  <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbdace5d37815e444b494434d9418a8dfb81" class="el">PP_AUDIOBUFFER_SAMPLERATE_UNKNOWN</a> = 0, <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbda7a10ada2c776cf2ca4fa5a220ab23f4f" class="el">PP_AUDIOBUFFER_SAMPLERATE_8000</a> = 8000, <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbdaa3205a867c6b7f54a735ba1e5e602839" class="el">PP_AUDIOBUFFER_SAMPLERATE_16000</a> = 16000, <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbda934a834bf3ac58e69a7df1abc41a57ea" class="el">PP_AUDIOBUFFER_SAMPLERATE_22050</a> = 22050,<br />
  <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbda439854e1f66e4e92af5d257b93da5483" class="el">PP_AUDIOBUFFER_SAMPLERATE_32000</a> = 32000, <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbdaef0fd009c55740284bcf6e60344395ac" class="el">PP_AUDIOBUFFER_SAMPLERATE_44100</a> = 44100, <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbda09d65e0a6d8ed28ae2fc784569b9123a" class="el">PP_AUDIOBUFFER_SAMPLERATE_48000</a> = 48000, <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbdaf52f1115d22dfbf1cc4a24f20b9e664b" class="el">PP_AUDIOBUFFER_SAMPLERATE_96000</a> = 96000,<br />
  <a href="/docs/native-client/pepper_beta/c/group___enums#gga78757d4be14d14d17708071a9466afbda18d94d8af683f06d4d7718fb788b7361" class="el">PP_AUDIOBUFFER_SAMPLERATE_192000</a> = 192000<br />
}</td></tr><tr class="even"><td style="text-align: right;">enum  </td><td><a href="/docs/native-client/pepper_beta/c/group___enums#ga2ba5c3a8eed23fa49a73b218b1bce044" class="el">PP_AudioBuffer_SampleSize</a> { <a href="/docs/native-client/pepper_beta/c/group___enums#gga2ba5c3a8eed23fa49a73b218b1bce044a1bc7fa3874cd1ccee3cfa00e23bea379" class="el">PP_AUDIOBUFFER_SAMPLESIZE_UNKNOWN</a> = 0, <a href="/docs/native-client/pepper_beta/c/group___enums#gga2ba5c3a8eed23fa49a73b218b1bce044a0cc6b2d53c4c3bc5d3f19f809a1ce6c8" class="el">PP_AUDIOBUFFER_SAMPLESIZE_16_BITS</a> = 2 }</td></tr></tbody></table>

------------------------------------------------------------------------

<span id="details" class="anchor" style="margin: 0;"></span>

Detailed Description
--------------------

Defines the `PPB_AudioBuffer` interface.

------------------------------------------------------------------------

Define Documentation
--------------------

<span id="a97463b49d90a036ddcb00968c33a8dfa" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>#define <a href="/docs/native-client/pepper_beta/c/ppb__audio__buffer_8h#a97463b49d90a036ddcb00968c33a8dfa" class="el">PPB_AUDIOBUFFER_INTERFACE</a>   <a href="/docs/native-client/pepper_beta/c/ppb__audio__buffer_8h#a4fddf6d285021552ba11f4460ba47445" class="el">PPB_AUDIOBUFFER_INTERFACE</a></td></tr></tbody></table>

<span id="a4fddf6d285021552ba11f4460ba47445" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>#define <a href="/docs/native-client/pepper_beta/c/ppb__audio__buffer_8h#a4fddf6d285021552ba11f4460ba47445" class="el">PPB_AUDIOBUFFER_INTERFACE</a>   "PPB_AudioBuffer;0.1"</td></tr></tbody></table>