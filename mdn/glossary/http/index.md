--- title: HTTP slug: Glossary/HTTP tags: - Beginner - Glossary - HTTP - Infrastructure - Web Performance - 'l10n:priority' ---

The HyperText Transfer Protocol (**HTTP**) is the underlying network {{glossary("protocol")}} that enables transfer of hypermedia documents on the {{glossary("World Wide Web","Web")}}, typically between a browser and a server so that humans can read them. The current version of the HTTP specification is called {{glossary("HTTP\_2", "HTTP/2")}}.

As part of a {{glossary("URI")}}, the "http" within "http://example.com/" is called a "scheme". Resources using the "http" schema are typically transported over unencrypted connections using the HTTP protocol. The "https" scheme (as in "https://developer.mozilla.org") indicates that a resource is transported using the HTTP protocol, but over a secure {{glossary("TLS")}} channel.

HTTP is textual (all communication is done in plain text) and stateless (no communication is aware of previous communications). This property makes it ideal for humans to read documents (web sites) on the world wide web. However, HTTP can also be used as a basis for {{glossary("REST")}} web services from server to server or {{glossary("AJAX")}} requests within web sites to make them more dynamic.

Learn more
----------

-   [HTTP on MDN](/en-US/docs/Web/HTTP)
-   {{interwiki("wikipedia", "Hypertext Transfer Protocol", "HTTP")}} on Wikipedia