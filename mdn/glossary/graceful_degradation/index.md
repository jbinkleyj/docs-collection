--- title: Graceful degradation slug: Glossary/Graceful\_degradation tags: - Design - Glossary - graceful degradation ---

**Graceful degradation** is a design philosophy that centers around trying to build a modern web site/application that will work in the newest browsers, but falls back to an experience that while not as good still delivers essential content and functionality in older browsers.

{{Glossary("Polyfill","Polyfills")}} can be used to build in missing features with JavaScript, but acceptable alternatives to features like styling and layout should be provided where possible, for example by using the CSS cascade, or HTML fallback behavior. Some good examples can be found in [Handling common HTML and CSS problems](/en-US/docs/Learn/Tools_and_testing/Cross_browser_testing/HTML_and_CSS).

It is a useful technique that allows Web developers to focus on developing the best possible websites, given that those websites are accessed by multiple unknown user-agents. {{Glossary("Progressive enhancement")}} is related but different — often seen as going in the opposite direction to graceful degradation. In reality both approaches are valid and can often complement one another.

1.  {{Interwiki("wikipedia", "Graceful degradation")}} on Wikipedia
2.  [Handling common HTML and CSS problems](/en-US/docs/Learn/Tools_and_testing/Cross_browser_testing/HTML_and_CSS)
3.  [Implementing feature detection](/en-US/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection)
4.  [MDN Web Docs Glossary](/en-US/docs/Glossary)
    1.  {{Glossary("Graceful degradation")}}
    2.  {{Glossary("Polyfill")}}
    3.  {{Glossary("Progressive enhancement")}}