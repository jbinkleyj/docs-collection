--- title: HTTP/2 slug: Glossary/HTTP\_2 tags: - Glossary - HTTP - Infrastructure - Reference - Web Performance - 'l10n:priority' ---

<span class="seoSummary">**HTTP/2** is a major revision of the [HTTP network protocol](/en-US/docs/Web/HTTP/Basics_of_HTTP)</span>. The primary goals for HTTP/2 are to reduce {{glossary("latency")}} by enabling full request and response multiplexing, minimize protocol overhead via efficient compression of HTTP header fields, and add support for request prioritization and server push.

HTTP/2 does not modify the application semantics of HTTP in any way. All the core concepts found in HTTP 1.1, such as HTTP methods, status codes, URIs, and header fields, remain in place. Instead, HTTP/2 modifies how the data is formatted (framed) and transported between the client and server, both of which manage the entire process, and hides application complexity within the new framing layer. As a result, all existing applications can be delivered without modification.

1.  General knowledge
    1.  [HTTP on MDN](/en-US/docs/Web/HTTP)
    2.  {{interwiki("wikipedia", "HTTP/2", "HTTP/2")}} on Wikipedia
2.  [Glossary](/en-US/docs/Glossary)
    1.  {{glossary("HTTP")}}
    2.  {{glossary("Latency")}}