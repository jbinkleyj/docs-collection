---json {"title":"PPB_OpenGLES2Query Struct Reference"} ---

## Data Fields

<table><tbody><tr class="odd"><td style="text-align: right;">void(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#ae2f6e8510804ee551ee9edee69aa2c01" class="el">GenQueriesEXT</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a9289d5b99dc1f27f01480360f2e18ae0" class="el">GLsizei</a> n, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> *queries)</td></tr><tr class="even"><td style="text-align: right;">void(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#ae49c996941b28dda03b9b1b20a12221b" class="el">DeleteQueriesEXT</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a9289d5b99dc1f27f01480360f2e18ae0" class="el">GLsizei</a> n, const <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> *queries)</td></tr><tr class="odd"><td style="text-align: right;"><a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa010a67382116caf29c29318251ccb6c" class="el">GLboolean</a>(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a2cac26bbb7738ced3d8e117856eeda50" class="el">IsQueryEXT</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> id)</td></tr><tr class="even"><td style="text-align: right;">void(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a5ba50bc0dc933e9e20233656610287df" class="el">BeginQueryEXT</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> target, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> id)</td></tr><tr class="odd"><td style="text-align: right;">void(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a8eb817ad4a0aa902a18acae5891dd66c" class="el">EndQueryEXT</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> target)</td></tr><tr class="even"><td style="text-align: right;">void(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#aaf9d9f118b872b8f1905eeb09a86b6da" class="el">GetQueryivEXT</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> target, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> pname, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a5ac0f3c4d7fafd42b284b5487a791017" class="el">GLint</a> *params)</td></tr><tr class="odd"><td style="text-align: right;">void(* </td><td><a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a25c570a8514e53f01b224731fbcd8244" class="el">GetQueryObjectuivEXT</a> )(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> id, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> pname, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> *params)</td></tr></tbody></table>

---

## Field Documentation

<span id="a5ba50bc0dc933e9e20233656610287df" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a5ba50bc0dc933e9e20233656610287df" class="el">PPB_OpenGLES2Query::BeginQueryEXT</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> target, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> id)</td></tr></tbody></table>

<span id="ae49c996941b28dda03b9b1b20a12221b" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#ae49c996941b28dda03b9b1b20a12221b" class="el">PPB_OpenGLES2Query::DeleteQueriesEXT</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a9289d5b99dc1f27f01480360f2e18ae0" class="el">GLsizei</a> n, const <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> *queries)</td></tr></tbody></table>

<span id="a8eb817ad4a0aa902a18acae5891dd66c" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a8eb817ad4a0aa902a18acae5891dd66c" class="el">PPB_OpenGLES2Query::EndQueryEXT</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> target)</td></tr></tbody></table>

<span id="ae2f6e8510804ee551ee9edee69aa2c01" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#ae2f6e8510804ee551ee9edee69aa2c01" class="el">PPB_OpenGLES2Query::GenQueriesEXT</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a9289d5b99dc1f27f01480360f2e18ae0" class="el">GLsizei</a> n, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> *queries)</td></tr></tbody></table>

<span id="aaf9d9f118b872b8f1905eeb09a86b6da" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#aaf9d9f118b872b8f1905eeb09a86b6da" class="el">PPB_OpenGLES2Query::GetQueryivEXT</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> target, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> pname, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a5ac0f3c4d7fafd42b284b5487a791017" class="el">GLint</a> *params)</td></tr></tbody></table>

<span id="a25c570a8514e53f01b224731fbcd8244" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td>void(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a25c570a8514e53f01b224731fbcd8244" class="el">PPB_OpenGLES2Query::GetQueryObjectuivEXT</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> id, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#a7efd7809e1632cdae75603fd1fee61c0" class="el">GLenum</a> pname, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> *params)</td></tr></tbody></table>

<span id="a2cac26bbb7738ced3d8e117856eeda50" class="anchor" style="margin: 0;"></span>

<table><tbody><tr class="odd"><td><a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa010a67382116caf29c29318251ccb6c" class="el">GLboolean</a>(* <a href="/docs/native-client/pepper_beta/c/struct_p_p_b___open_g_l_e_s2_query__1__0#a2cac26bbb7738ced3d8e117856eeda50" class="el">PPB_OpenGLES2Query::IsQueryEXT</a>)(<a href="/docs/native-client/pepper_beta/c/group___typedefs#gafdc3895ee80f4750d0d95ae1b677e9b7" class="el">PP_Resource</a> context, <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h#aa311c7f0d6ec4f1a33f9235c3651b86b" class="el">GLuint</a> id)</td></tr></tbody></table>

---

The documentation for this struct was generated from the following file:

- <a href="/docs/native-client/pepper_beta/c/ppb__opengles2_8h/" class="el">ppb_opengles2.h</a>