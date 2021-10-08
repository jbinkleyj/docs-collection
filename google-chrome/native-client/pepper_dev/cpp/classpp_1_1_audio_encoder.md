---json {"title":"pp::AudioEncoder Class Reference"} ---

Inheritance diagram for pp::AudioEncoder:

![Inheritance graph](/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder__inherit__graph.png)

<span class="legend">\[[legend](/docs/native-client/pepper_dev/cpp/graph_legend/)\]</span>

[List of all members.](/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder-members/)

Public Member Functions
-----------------------

<table><tbody><tr class="odd"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#afaf804d519fc0f2370c2d011b4e68378" class="el">AudioEncoder</a> ()</td></tr><tr class="even"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a1b5126d5112082bfa782bf5423715030" class="el">AudioEncoder</a> (const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_instance_handle/" class="el">InstanceHandle</a> &amp;instance)</td></tr><tr class="odd"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#ac4a116ff790ce5dc1cc4847118aabc9d" class="el">AudioEncoder</a> (const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder/" class="el">AudioEncoder</a> &amp;other)</td></tr><tr class="even"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a34b94c7bb1f509f4b56bfe7349560669" class="el">GetSupportedProfiles</a> (const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback_with_output/" class="el">CompletionCallbackWithOutput</a>&lt; std::vector&lt; PP_AudioProfileDescription &gt; &gt; &amp;cc)</td></tr><tr class="odd"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a28aa43f8c92b387b81e7cf63219c2933" class="el">Initialize</a> (uint32_t channels, PP_AudioBuffer_SampleRate input_sample_rate, PP_AudioBuffer_SampleSize input_sample_size, PP_AudioProfile output_profile, uint32_t initial_bitrate, PP_HardwareAcceleration acceleration, const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp;cc)</td></tr><tr class="even"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a706b305dae8bc5f5e0bca4491c991d59" class="el">GetNumberOfSamples</a> ()</td></tr><tr class="odd"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a113d4a018e987f2f5227c6e0dc8a7687" class="el">GetBuffer</a> (const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback_with_output/" class="el">CompletionCallbackWithOutput</a>&lt; <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_buffer/" class="el">AudioBuffer</a> &gt; &amp;cc)</td></tr><tr class="even"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a75278dc12dfcc3d000e47e17f014be19" class="el">Encode</a> (const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_buffer/" class="el">AudioBuffer</a> &amp;buffer, const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp;cc)</td></tr><tr class="odd"><td style="text-align: right;">int32_t </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#ad1a2c96562e2baa7a61d63fbb8a49999" class="el">GetBitstreamBuffer</a> (const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback_with_output/" class="el">CompletionCallbackWithOutput</a>&lt; PP_AudioBitstreamBuffer &gt; &amp;cc)</td></tr><tr class="even"><td style="text-align: right;">void </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a9c5b90b6dbfd81154b28f402197184bc" class="el">RecycleBitstreamBuffer</a> (const PP_AudioBitstreamBuffer &amp;bitstream_buffer)</td></tr><tr class="odd"><td style="text-align: right;">void </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#aa64ea3b0313335817833a72ceed96114" class="el">RequestBitrateChange</a> (uint32_t bitrate)</td></tr><tr class="even"><td style="text-align: right;">void </td><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a5f5f533624660ca8561fea403da85f5b" class="el">Close</a> ()</td></tr></tbody></table>

------------------------------------------------------------------------

<span id="details" class="anchor" style="margin: 0;"></span>

Detailed Description
--------------------

<a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio/" class="el" title="An audio resource.">Audio</a> encoder interface.

Typical usage:

-   Call Create() to create a new audio encoder resource.
-   Call GetSupportedFormats() to determine which codecs and profiles are available.
-   Call <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a28aa43f8c92b387b81e7cf63219c2933" class="el" title="Initializes a audio encoder resource.">Initialize()</a> to initialize the encoder for a supported profile.
-   Call <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a113d4a018e987f2f5227c6e0dc8a7687" class="el" title="Gets a blank audio frame which can be filled with audio data and passed to the encoder.">GetBuffer()</a> to get a blank frame and fill it in, or get an audio frame from another resource, e.g. `PPB_MediaStreamAudioTrack`.
-   Call <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a75278dc12dfcc3d000e47e17f014be19" class="el" title="Encodes an audio buffer.">Encode()</a> to push the audio buffer to the encoder. If an external buffer is pushed, wait for completion to recycle the frame.
-   Call <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#ad1a2c96562e2baa7a61d63fbb8a49999" class="el" title="Gets the next encoded bitstream buffer from the encoder.">GetBitstreamBuffer()</a> continuously (waiting for each previous call to complete) to pull encoded buffers from the encoder.
-   Call <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a9c5b90b6dbfd81154b28f402197184bc" class="el" title="Recycles a bitstream buffer back to the encoder.">RecycleBitstreamBuffer()</a> after consuming the data in the bitstream buffer.
-   To destroy the encoder, the plugin should release all of its references to it. Any pending callbacks will abort before the encoder is destroyed.

Available audio codecs vary by platform. All: opus.

------------------------------------------------------------------------

Constructor & Destructor Documentation
--------------------------------------

<span id="afaf804d519fc0f2370c2d011b4e68378" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#afaf804d519fc0f2370c2d011b4e68378" class="el">pp::AudioEncoder::AudioEncoder</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

Default constructor for creating an <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_resource#a859068e34cdc2dc0b78754c255323aa9" class="el" title="This functions determines if this resource is invalid or uninitialized.">is_null()</a> `AudioEncoder` object.

<span id="a1b5126d5112082bfa782bf5423715030" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#afaf804d519fc0f2370c2d011b4e68378" class="el">pp::AudioEncoder::AudioEncoder</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_instance_handle/" class="el">InstanceHandle</a> &amp; </td><td><em>instance</em></td><td>)</td><td><code> [explicit]</code></td></tr></tbody></table>

A constructor used to create a `AudioEncoder` and associate it with the provided `Instance`.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>instance</td><td>The instance with which this resource will be associated.</td></tr></tbody></table>

<span id="ac4a116ff790ce5dc1cc4847118aabc9d" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#afaf804d519fc0f2370c2d011b4e68378" class="el">pp::AudioEncoder::AudioEncoder</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder/" class="el">AudioEncoder</a> &amp; </td><td><em>other</em></td><td>)</td><td></td></tr></tbody></table>

The copy constructor for `AudioEncoder`.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>other</td><td>A reference to a <code>AudioEncoder</code>.</td></tr></tbody></table>

------------------------------------------------------------------------

Member Function Documentation
-----------------------------

<span id="a5f5f533624660ca8561fea403da85f5b" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a5f5f533624660ca8561fea403da85f5b" class="el">pp::AudioEncoder::Close</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

Closes the audio encoder, and cancels any pending encodes.

Any pending callbacks will still run, reporting `PP_ERROR_ABORTED` . It is not valid to call any encoder functions after a call to this method. **Note:** Destroying the audio encoder closes it implicitly, so you are not required to call <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a5f5f533624660ca8561fea403da85f5b" class="el" title="Closes the audio encoder, and cancels any pending encodes.">Close()</a>.

<span id="a75278dc12dfcc3d000e47e17f014be19" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a75278dc12dfcc3d000e47e17f014be19" class="el">pp::AudioEncoder::Encode</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_buffer/" class="el">AudioBuffer</a> &amp; </td><td><em>buffer</em>,</td></tr><tr class="even"><td></td><td></td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp; </td><td><em>cc</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

Encodes an audio buffer.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>audio_buffer</td><td>The <code>AudioBuffer</code> to be encoded.</td></tr><tr class="even"><td>[in]</td><td>callback</td><td>A <code>CompletionCallback</code> to be called upon completion. Plugins that pass <code>AudioBuffer</code> resources owned by other resources should wait for completion before reusing them.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`. Returns PP\_ERROR\_FAILED if <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a28aa43f8c92b387b81e7cf63219c2933" class="el" title="Initializes a audio encoder resource.">Initialize()</a> has not successfully completed.

<span id="ad1a2c96562e2baa7a61d63fbb8a49999" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#ad1a2c96562e2baa7a61d63fbb8a49999" class="el">pp::AudioEncoder::GetBitstreamBuffer</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback_with_output/" class="el">CompletionCallbackWithOutput</a>&lt; PP_AudioBitstreamBuffer &gt; &amp; </td><td><em>cc</em></td><td>)</td><td></td></tr></tbody></table>

Gets the next encoded bitstream buffer from the encoder.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>callback</td><td>A <code>CompletionCallbackWithOutput</code> to be called upon completion with the next bitstream buffer. The plugin can call GetBitstreamBuffer from the callback in order to continuously "pull" bitstream buffers from the encoder.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`. Returns PP\_ERROR\_FAILED if <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a28aa43f8c92b387b81e7cf63219c2933" class="el" title="Initializes a audio encoder resource.">Initialize()</a> has not successfully completed. Returns PP\_ERROR\_INPROGRESS if a prior call to <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#ad1a2c96562e2baa7a61d63fbb8a49999" class="el" title="Gets the next encoded bitstream buffer from the encoder.">GetBitstreamBuffer()</a> has not completed.

<span id="a113d4a018e987f2f5227c6e0dc8a7687" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a113d4a018e987f2f5227c6e0dc8a7687" class="el">pp::AudioEncoder::GetBuffer</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback_with_output/" class="el">CompletionCallbackWithOutput</a>&lt; <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_buffer/" class="el">AudioBuffer</a> &gt; &amp; </td><td><em>cc</em></td><td>)</td><td></td></tr></tbody></table>

Gets a blank audio frame which can be filled with audio data and passed to the encoder.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>callback</td><td>A <code>CompletionCallbackWithOutput</code> to be called upon completion with the blank <code>AudioBuffer</code> resource.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`.

<span id="a706b305dae8bc5f5e0bca4491c991d59" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a706b305dae8bc5f5e0bca4491c991d59" class="el">pp::AudioEncoder::GetNumberOfSamples</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

Gets the number of audio samples per channel that audio buffers must contain in order to be processed by the encoder.

This will be the number of samples per channels contained in buffers returned by <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a113d4a018e987f2f5227c6e0dc8a7687" class="el" title="Gets a blank audio frame which can be filled with audio data and passed to the encoder.">GetBuffer()</a>.

**Returns:**  
An int32\_t containing the number of samples required, or an error code from `pp_errors.h`. Returns PP\_ERROR\_FAILED if <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a28aa43f8c92b387b81e7cf63219c2933" class="el" title="Initializes a audio encoder resource.">Initialize()</a> has not successfully completed.

<span id="a34b94c7bb1f509f4b56bfe7349560669" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a34b94c7bb1f509f4b56bfe7349560669" class="el">pp::AudioEncoder::GetSupportedProfiles</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback_with_output/" class="el">CompletionCallbackWithOutput</a>&lt; std::vector&lt; PP_AudioProfileDescription &gt; &gt; &amp; </td><td><em>cc</em></td><td>)</td><td></td></tr></tbody></table>

Gets an array of supported audio encoder profiles.

These can be used to choose a profile before calling <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a28aa43f8c92b387b81e7cf63219c2933" class="el" title="Initializes a audio encoder resource.">Initialize()</a>.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>callback</td><td>A <code>CompletionCallbackWithOutput</code> to be called upon completion with the PP_AudioProfileDescription structs.</td></tr></tbody></table>

<!-- -->

**Returns:**  
If &gt;= 0, the number of supported profiles returned, otherwise an error code from `pp_errors.h`.

<span id="a28aa43f8c92b387b81e7cf63219c2933" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>int32_t <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a28aa43f8c92b387b81e7cf63219c2933" class="el">pp::AudioEncoder::Initialize</a></td><td>(</td><td>uint32_t </td><td><em>channels</em>,</td></tr><tr class="even"><td></td><td></td><td>PP_AudioBuffer_SampleRate </td><td><em>input_sample_rate</em>,</td></tr><tr class="odd"><td></td><td></td><td>PP_AudioBuffer_SampleSize </td><td><em>input_sample_size</em>,</td></tr><tr class="even"><td></td><td></td><td>PP_AudioProfile </td><td><em>output_profile</em>,</td></tr><tr class="odd"><td></td><td></td><td>uint32_t </td><td><em>initial_bitrate</em>,</td></tr><tr class="even"><td></td><td></td><td>PP_HardwareAcceleration </td><td><em>acceleration</em>,</td></tr><tr class="odd"><td></td><td></td><td>const <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_completion_callback/" class="el">CompletionCallback</a> &amp; </td><td><em>cc</em> </td></tr><tr class="even"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

Initializes a audio encoder resource.

This should be called after <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a34b94c7bb1f509f4b56bfe7349560669" class="el" title="Gets an array of supported audio encoder profiles.">GetSupportedProfiles()</a> and before any functions below.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>channels</td><td>The number of audio channels to encode.</td></tr><tr class="even"><td>[in]</td><td>input_sampling_rate</td><td>The sampling rate of the input audio buffer.</td></tr><tr class="odd"><td>[in]</td><td>input_sample_size</td><td>The sample size of the input audio buffer.</td></tr><tr class="even"><td>[in]</td><td>output_profile</td><td>A <code>PP_AudioProfile</code> specifying the codec profile of the encoded output stream.</td></tr><tr class="odd"><td>[in]</td><td>initial_bitrate</td><td>The initial bitrate for the encoder.</td></tr><tr class="even"><td>[in]</td><td>acceleration</td><td>A <code>PP_HardwareAcceleration</code> specifying whether to use a hardware accelerated or a software implementation.</td></tr><tr class="odd"><td>[in]</td><td>callback</td><td>A <code>CompletionCallback</code> to be called upon completion.</td></tr></tbody></table>

<!-- -->

**Returns:**  
An int32\_t containing an error code from `pp_errors.h`. Returns PP\_ERROR\_NOTSUPPORTED if audio encoding is not available, or the requested codec profile is not supported. Returns PP\_ERROR\_NOMEMORY if bitstream buffers can't be created.

<span id="a9c5b90b6dbfd81154b28f402197184bc" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#a9c5b90b6dbfd81154b28f402197184bc" class="el">pp::AudioEncoder::RecycleBitstreamBuffer</a></td><td>(</td><td>const PP_AudioBitstreamBuffer &amp; </td><td><em>bitstream_buffer</em></td><td>)</td><td></td></tr></tbody></table>

Recycles a bitstream buffer back to the encoder.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>bitstream_buffer</td><td>A<code>PP_AudioBitstreamBuffer</code> that is no longer needed by the plugin.</td></tr></tbody></table>

<span id="aa64ea3b0313335817833a72ceed96114" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_dev/cpp/classpp_1_1_audio_encoder#aa64ea3b0313335817833a72ceed96114" class="el">pp::AudioEncoder::RequestBitrateChange</a></td><td>(</td><td>uint32_t </td><td><em>bitrate</em></td><td>)</td><td></td></tr></tbody></table>

Requests a change to the encoding bitrate.

This is only a request, fulfilled on a best-effort basis.

**Parameters:**  
<table><tbody><tr class="odd"><td>[in]</td><td>audio_encoder</td><td>A <code>PP_Resource</code> identifying the audio encoder.</td></tr></tbody></table>

------------------------------------------------------------------------

The documentation for this class was generated from the following file:

-   <a href="/docs/native-client/pepper_dev/cpp/audio__encoder_8h/" class="el">audio_encoder.h</a>