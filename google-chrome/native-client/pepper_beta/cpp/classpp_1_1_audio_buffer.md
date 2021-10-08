---json {"title":"pp::AudioBuffer Class Reference"} ---

Inheritance diagram for pp::AudioBuffer:

![Inheritance graph](/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer__inherit__graph.png)

<span class="legend">\[[legend](/docs/native-client/pepper_beta/cpp/graph_legend/)\]</span>

[List of all members.](/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer-members/)

## Public Member Functions

<table><tbody><tr class="odd"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ae5a21e1df405d530d9280de36791dbbf" class="el">AudioBuffer</a> ()</td></tr><tr class="even"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a8f51aeb6d98ff9d926ee1e2fcee4f712" class="el">AudioBuffer</a> (const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer/" class="el">AudioBuffer</a> &amp;other)</td></tr><tr class="odd"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a96db6e6a05eb834ed8b04ef8c3f6647a" class="el">AudioBuffer</a> (const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_resource/" class="el">Resource</a> &amp;resource)</td></tr><tr class="even"><td style="text-align: right;"> </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ad80595164aba1e9fbe1ccc71793c48f9" class="el">AudioBuffer</a> (<a href="/docs/native-client/pepper_beta/cpp/namespacepp#a339083c1beec620267bf8b3c55decaa5" class="el">PassRef</a>, PP_Resource resource)</td></tr><tr class="odd"><td style="text-align: right;">virtual </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#aa47da494df014dd6dba16053f914ce34" class="el">~AudioBuffer</a> ()</td></tr><tr class="even"><td style="text-align: right;">PP_TimeDelta </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a08f55c4a972677114bb0c0e1ceb13661" class="el">GetTimestamp</a> () const</td></tr><tr class="odd"><td style="text-align: right;">void </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a2882ec7147f4efddf3cefc6378f11f78" class="el">SetTimestamp</a> (PP_TimeDelta timestamp)</td></tr><tr class="even"><td style="text-align: right;">PP_AudioBuffer_SampleRate </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a650c3a1abc424e21fa56997c9d55b76f" class="el">GetSampleRate</a> () const</td></tr><tr class="odd"><td style="text-align: right;">PP_AudioBuffer_SampleSize </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ac3846435b70b49392dec120716e0cfd5" class="el">GetSampleSize</a> () const</td></tr><tr class="even"><td style="text-align: right;">uint32_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a3061bf5fc031ad6854d2b06ef6f6736a" class="el">GetNumberOfChannels</a> () const</td></tr><tr class="odd"><td style="text-align: right;">uint32_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ad588d83a59d151fb8448ea59f6f9039e" class="el">GetNumberOfSamples</a> () const</td></tr><tr class="even"><td style="text-align: right;">void * </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#aad0cdf64f6fc99ebbad26725ba17df65" class="el">GetDataBuffer</a> ()</td></tr><tr class="odd"><td style="text-align: right;">uint32_t </td><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a5548630a163439b2c811ab40d7cd64a0" class="el">GetDataBufferSize</a> () const</td></tr></tbody></table>

---

## Constructor & Destructor Documentation

<span id="ae5a21e1df405d530d9280de36791dbbf" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ae5a21e1df405d530d9280de36791dbbf" class="el">pp::AudioBuffer::AudioBuffer</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

Default constructor for creating an <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_resource#a859068e34cdc2dc0b78754c255323aa9" class="el" title="This functions determines if this resource is invalid or uninitialized.">is_null()</a> `AudioBuffer` object.

<span id="a8f51aeb6d98ff9d926ee1e2fcee4f712" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ae5a21e1df405d530d9280de36791dbbf" class="el">pp::AudioBuffer::AudioBuffer</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer/" class="el">AudioBuffer</a> &amp; </td><td><em>other</em></td><td>)</td><td></td></tr></tbody></table>

The copy constructor for `AudioBuffer`.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>other</td><td>A reference to an <code>AudioBuffer</code>.</td></tr></tbody></table>

<span id="a96db6e6a05eb834ed8b04ef8c3f6647a" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ae5a21e1df405d530d9280de36791dbbf" class="el">pp::AudioBuffer::AudioBuffer</a></td><td>(</td><td>const <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_resource/" class="el">Resource</a> &amp; </td><td><em>resource</em></td><td>)</td><td><code> [explicit]</code></td></tr></tbody></table>

Constructs an `AudioBuffer` from a `Resource`.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>resource</td><td>A <code>PPB_AudioBuffer</code> resource.</td></tr></tbody></table>

<span id="ad80595164aba1e9fbe1ccc71793c48f9" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ae5a21e1df405d530d9280de36791dbbf" class="el">pp::AudioBuffer::AudioBuffer</a></td><td>(</td><td><a href="/docs/native-client/pepper_beta/cpp/namespacepp#a339083c1beec620267bf8b3c55decaa5" class="el">PassRef</a> </td><td>,</td></tr><tr class="even"><td></td><td></td><td>PP_Resource </td><td><em>resource</em> </td></tr><tr class="odd"><td></td><td>)</td><td></td><td></td></tr></tbody></table>

A constructor used when you have received a `PP_Resource` as a return value that has had 1 ref added for you.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>resource</td><td>A <code>PPB_AudioBuffer</code> resource.</td></tr></tbody></table>

<span id="aa47da494df014dd6dba16053f914ce34" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>virtual <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#aa47da494df014dd6dba16053f914ce34" class="el">pp::AudioBuffer::~AudioBuffer</a></td><td>(</td><td></td><td>)</td><td><code> [virtual]</code></td></tr></tbody></table>

---

## Member Function Documentation

<span id="aad0cdf64f6fc99ebbad26725ba17df65" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void* <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#aad0cdf64f6fc99ebbad26725ba17df65" class="el">pp::AudioBuffer::GetDataBuffer</a></td><td>(</td><td></td><td>)</td><td></td></tr></tbody></table>

Gets the data buffer containing the audio buffer samples.

**Returns:**  
A pointer to the beginning of the data buffer.

<span id="a5548630a163439b2c811ab40d7cd64a0" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>uint32_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a5548630a163439b2c811ab40d7cd64a0" class="el">pp::AudioBuffer::GetDataBufferSize</a></td><td>(</td><td></td><td>)</td><td>const</td></tr></tbody></table>

Gets the size of data buffer in bytes.

**Returns:**  
The size of the data buffer in bytes.

<span id="a3061bf5fc031ad6854d2b06ef6f6736a" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>uint32_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a3061bf5fc031ad6854d2b06ef6f6736a" class="el">pp::AudioBuffer::GetNumberOfChannels</a></td><td>(</td><td></td><td>)</td><td>const</td></tr></tbody></table>

Gets the number of channels in the audio buffer.

**Returns:**  
The number of channels in the audio buffer.

<span id="ad588d83a59d151fb8448ea59f6f9039e" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>uint32_t <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ad588d83a59d151fb8448ea59f6f9039e" class="el">pp::AudioBuffer::GetNumberOfSamples</a></td><td>(</td><td></td><td>)</td><td>const</td></tr></tbody></table>

Gets the number of samples in the audio buffer.

**Returns:**  
The number of samples in the audio buffer. For example, at a sampling rate of 44,100 Hz in stereo audio, a buffer containing 4,410 \* 2 samples would have a duration of 100 milliseconds.

<span id="a650c3a1abc424e21fa56997c9d55b76f" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>PP_AudioBuffer_SampleRate <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a650c3a1abc424e21fa56997c9d55b76f" class="el">pp::AudioBuffer::GetSampleRate</a></td><td>(</td><td></td><td>)</td><td>const</td></tr></tbody></table>

Gets the sample rate of the audio buffer.

**Returns:**  
The sample rate of the audio buffer.

<span id="ac3846435b70b49392dec120716e0cfd5" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>PP_AudioBuffer_SampleSize <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#ac3846435b70b49392dec120716e0cfd5" class="el">pp::AudioBuffer::GetSampleSize</a></td><td>(</td><td></td><td>)</td><td>const</td></tr></tbody></table>

Gets the sample size of the audio buffer in bytes.

**Returns:**  
The sample size of the audio buffer in bytes.

<span id="a08f55c4a972677114bb0c0e1ceb13661" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>PP_TimeDelta <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a08f55c4a972677114bb0c0e1ceb13661" class="el">pp::AudioBuffer::GetTimestamp</a></td><td>(</td><td></td><td>)</td><td>const</td></tr></tbody></table>

Gets the timestamp of the audio buffer.

**Returns:**  
A `PP_TimeDelta` containing the timestamp of the audio buffer. Given in seconds since the start of the containing audio stream.

<span id="a2882ec7147f4efddf3cefc6378f11f78" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void <a href="/docs/native-client/pepper_beta/cpp/classpp_1_1_audio_buffer#a2882ec7147f4efddf3cefc6378f11f78" class="el">pp::AudioBuffer::SetTimestamp</a></td><td>(</td><td>PP_TimeDelta </td><td><em>timestamp</em></td><td>)</td><td></td></tr></tbody></table>

Sets the timestamp of the audio buffer.

**Parameters:**

<table><tbody><tr class="odd"><td>[in]</td><td>timestamp</td><td>A <code>PP_TimeDelta</code> containing the timestamp of the audio buffer. Given in seconds since the start of the containing audio stream.</td></tr></tbody></table>

---

The documentation for this class was generated from the following file:

- <a href="/docs/native-client/pepper_beta/cpp/audio__buffer_8h/" class="el">audio_buffer.h</a>