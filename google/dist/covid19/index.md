<span class="w-tooltip w-tooltip--left">Open menu</span>

<a href="/" class="header-default__logo-link gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="header-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="header-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="header-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="header-default__link gc-analytics-event">Blog</a> <a href="/about/" class="header-default__link gc-analytics-event">About</a>

<span class="w-tooltip">Close</span>

<a href="/" class="gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="drawer-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="drawer-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="drawer-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="drawer-default__link gc-analytics-event">Blog</a> <a href="/about/" class="drawer-default__link gc-analytics-event">About</a>

<img src="https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format" alt="Hero Image" class="w-hero w-hero--cover" sizes="100vw" srcset="https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=200 200w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=228 228w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=260 260w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=296 296w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=338 338w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=385 385w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=439 439w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=500 500w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=571 571w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=650 650w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=741 741w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=845 845w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=964 964w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=1098 1098w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=1252 1252w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=1428 1428w,     https://web-dev.imgix.net/image/admin/LH3VwpI4GW1lW51Ns5ab.jpg?auto=format&amp;w=1600 1600w" width="1600" height="480" />

## <a href="#ensure-your-website-is-available-and-usable-for-everyone-during-covid-19" class="w-toc__header--link">Ensure your website is available and usable for everyone during COVID-19</a>

- [Guidance](#guidance)
- [Availability, reliability, resilience, and stability](#availability)
- [Accessibility](#accessibility)
- [Identity, security, and privacy](#PII)
- [Usability, UI, and UX](#usability)
- [SEO](#seo)
- [Performance](#performance)

Share <a href="/newsletter/" class="w-actions__fab w-actions__fab--subscribe gc-analytics-event"><span>subscribe</span></a>

- <a href="/" class="w-breadcrumbs__link w-breadcrumbs__link--left-justify gc-analytics-event">Home</a>
- <a href="/blog" class="w-breadcrumbs__link gc-analytics-event">All articles</a>

# Ensure your website is available and usable for everyone during COVID-19

How to ensure that the core functionality of your website is always available, accessible, secure, usable, discoverable, and fast.

Apr 3, 2020 <span class="w-author__separator">•</span> Updated Apr 6, 2020

This page provides guidance to help ensure your website is available, accessible, secure, and usable for everyone at all times.

If you're building or maintaining a health organization website that qualifies as a national health ministry or US state-level agency, you can request to join the COVID-19 Google Search technical support group. Visit [Helping health organizations make COVID-19 information more accessible](https://webmasters.googleblog.com/2020/03/health-organizations-covid19.html) to learn more.

The guidance on this page comes from a cross-functional collection of teams within Google that are shifting their short-term focus to support websites that are helping people stay safe during the COVID-19 situation. These Googlers have seen that sites are facing unprecedented increases in demand from people looking for critical information, many of whom have rarely or never used the web before. It can be a challenge to ensure sites are available during this time and accessible to all.

## Guidance <a href="#guidance" class="w-headline-link">#</a>

This guidance is a work in progress and will be updated frequently. If you have any suggestions, please [file an issue](https://github.com/GoogleChrome/web.dev/issues/new/choose), or [edit this page](https://github.com/GoogleChrome/web.dev/blob/master/src/site/content/en/blog/covid19/index.md) and then open a pull request.

### Availability, reliability, resilience, and stability <a href="#availability" class="w-headline-link">#</a>

If your site is seeing traffic spikes and it's failing, or you want to prevent it from failing, the guidance below can help you quickly fix problems or detect them before they become major issues.

- Read [Fix an overloaded server](/overloaded-server) to learn how to detect, mitigate, and prevent traffic spike issues.
- Remove unnecessary images, videos, scripts, and fonts. Ensure each page focuses on just delivering the functionality that the people using your site really need.
- [Optimizing your images](/fast/#optimize-your-images) may significantly reduce your server bandwidth usage because [images are the number one source of bloat on the web](https://images.guide/#introduction).
- Offload as much of your static content to CDNs as possible. More details from common providers: [AWS](https://aws.amazon.com/cloudfront/), [Azure](https://azure.microsoft.com/en-us/services/cdn/), [Cloudflare](https://www.cloudflare.com/cdn/), [Google Cloud](https://cloud.google.com/cdn), [Firebase](https://firebase.google.com/docs/hosting).
- Check if your CDN has any optimizations that are easy to turn on, such as dynamic image compression, text compression, or automatic minification of JS and CSS resources.
- Optimizing HTTP caching can significantly reduce demands on your servers with minimal code change. Check out [The HTTP cache: your first line of defense](/http-cache/) for an overview and [HTTP caching](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching) and [Caching best practices](https://jakearchibald.com/2016/caching-best-practices/) for specific recommendations. The [Serve static assets with an efficient cache policy](/uses-long-cache-ttl/) audit in Lighthouse can help you quickly detect resources that aren't being cached. Keep in mind that different types of resources will have different freshness requirements and will therefore require different caching strategies.
- [Service workers](/service-workers-cache-storage/) are another way to significantly reduce demands on your servers but may require significant technical investment. They also enable your website to work [offline](https://developers.google.com/web/fundamentals/codelabs/offline), enabling you to present opening hours, phone numbers, and other information to returning users without a connection. [Workbox](/workbox/) is the recommended approach for adding service workers to websites because it automates a lot of boilerplate, makes it easier to follow best practices, and prevents subtle bugs that are common when using the low-level `ServiceWorker` API directly.
- If your site is seeing major increased usage, check whether you have adequate protection against [DDoS attacks](https://en.wikipedia.org/wiki/Denial-of-service_attack) because your site may now be a more attractive target. More details from common providers: [AWS](https://aws.amazon.com/answers/networking/aws-ddos-attack-mitigation/), [Azure](https://azure.microsoft.com/en-us/services/ddos-protection/), [Cloudflare](https://www.cloudflare.com/learning/ddos/ddos-mitigation/), [Google Cloud](https://cloud.google.com/files/GCPDDoSprotection-04122016.pdf).

See [Network reliability](/reliable/) for more guidance.

### Accessibility <a href="#accessibility" class="w-headline-link">#</a>

Focusing on accessibility is more important than ever because more people with a variety of needs are probably accessing your site. Follow the guidelines below to ensure that the core functionality of your website is accessible for everyone.

- Accessibility is a team effort and everyone has a role to play. Start by reviewing Google's [Accessibility for Teams guide](https://developers.google.com/web/fundamentals/accessibility/a11y-for-teams) as well as [the team guide from the U.S. Digital Service](https://accessibility.digital.gov/). These guides explain what each team member (product managers, engineers, designers, QA, and so on) can contribute.
- Do an [Accessibility Review](https://developers.google.com/web/fundamentals/accessibility/how-to-review) to determine what's working well, and what needs improvement. The [WAVE browser extensions](https://wave.webaim.org/extension/) can help guide you through a manual accessibility audit of your site.
- Read through the [Accessibility Guides](/accessible) to better understand specific topics like keyboard navigation and screen reader support.
- [Run a Lighthouse audit](https://developers.google.com/web/tools/lighthouse#devtools) to catch common accessibility issues. The report also provides a list of manual checks that you can perform to improve the operability of your site. Note that an Accessibility score of 100 does not guarantee that your site is accessible. There are many important issues that Lighthouse can't test for in an automated fashion so it's still important to do manual reviews. Other automated auditing tools include the [WAVE API](https://wave.webaim.org/api/) and the [AXE extension](https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd).
- Complete the [Start Building Accessible Web Applications Today course on egghead.io](https://egghead.io/courses/start-building-accessible-web-applications-today) course or check out the [Web Accessibility course on Udacity](https://www.udacity.com/course/web-accessibility--ud891).
- Watch the [A11ycast playlist](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) for more quick tips on specific accessibility topics.

### Identity, security, and privacy <a href="#PII" class="w-headline-link">#</a>

It can be tempting to take shortcuts to get critical fixes out the door, but always be careful that you are not opening up security holes in doing so. People need to access content on topics that are extremely private. Websites need to protect this sensitive user data at all costs and convince people that their [personally identifiable information](https://en.wikipedia.org/wiki/Personal_data) (PII) is safe.

- Understand [why all websites should be protected with HTTPS](https://developers.google.com/web/fundamentals/security/encrypt-in-transit/why-https), not just those that handle sensitive PII data.
- Switch to a hosting provider that uses HTTPS by default, or use [Let's Encrypt](https://letsencrypt.org/getting-started/) or similar services to enable HTTPS on your servers.
- Review [SameSite cookies explained](/samesite-cookies-explained/) to learn how to make your use of cookies more secure. Note that [the enforcement of SameSite cookie labeling has been temporarily rolled back](https://blog.chromium.org/2020/04/temporarily-rolling-back-samesite.html).

See [Safe and secure](/secure/) for more guidance.

### Usability, UI, and UX <a href="#usability" class="w-headline-link">#</a>

People are relying more heavily on the web to fulfill basic needs. Many of these people don't use the web frequently. It's worthwhile to audit the usability of your site's core functionality and make sure it's as simple and easy to use as possible.

- Consider adding a prominent banner (that can be removed with an **X** button) to the top of your website that clearly communicates service updates. Use a call-to-action in the banner to direct people to more specific resources. Consider using distinct colors and fonts that stand out from the rest of your page content. Keep your writing empathetic, focused on people's needs, and transparent about what kind of service to expect.
- Look for opportunities to minimize physical interactions in your [critical user journeys](https://www.nngroup.com/articles/journey-mapping-101/) (CUJs) and suggest those changes to your product team. For example, if your delivery service usually requires a signature, see if there's any way to work around that.
- Double-check that your CUJs are as simple and intuitive as possible and suggest changes to your product team if you see any opportunities to improve.
- Review the [principles of good mobile design](https://developers.google.com/web/fundamentals/design-and-ux/principles) and try out your CUJs on various mobile devices to make sure there aren't any glaring issues. The people who don't use the web often and are suddenly finding themselves having to rely on the web more are probably accessing your site from mobile devices.
- Refactor your site to use [responsive design patterns](https://developers.google.com/web/fundamentals/design-and-ux/responsive) as much as possible.
- Ensure that your forms are [efficient](https://www.smashingmagazine.com/2017/06/designing-efficient-web-forms/) and [well-designed](https://developers.google.com/web/fundamentals/design-and-ux/input/forms).

### SEO <a href="#seo" class="w-headline-link">#</a>

People are looking for critical health- and job-related information. It's important to ensure that your sites are discoverable by all search engines. The [Lighthouse SEO audits](/lighthouse-seo/) can help you detect basic problems. Follow the official blogs of search engines for the latest guidance and updates: [Google](https://webmasters.googleblog.com/), [Bing](https://blogs.bing.com/webmaster/), [Baidu](http://research.baidu.com/Blog), [DuckDuckGo](https://spreadprivacy.com/tag/duckduckgo/), [Yandex](https://yandex.com/blog/yacompany-com). Recent COVID-19-related posts:

- [How to change your online activities while minimizing impact on your Google Search presence](https://webmasters.googleblog.com/2020/03/how-to-pause-your-business-online-in.html)
- [New properties for virtual, postponed, and canceled events](https://webmasters.googleblog.com/2020/03/new-properties-virtual-or-canceled-events.html)
- [Bing adopts schema.org markup for special announcements for COVID-19](https://blogs.bing.com/webmaster/march-2020/Bing-adopts-schema-org-mark-up-for-Special-Announcements-about-COVID-19)
- [Add structured data to COVID-19 announcements](https://developers.google.com/search/docs/data-types/special-announcements)
- [Helping health organizations make COVID-19 information more accessible](https://webmasters.googleblog.com/2020/03/health-organizations-covid19.html)
- [General best practices for Search for health & government sites](https://support.google.com/webmasters/answer/9781983)

See [Discoverable](/discoverable/) for more guidance.

### Performance <a href="#performance" class="w-headline-link">#</a>

Some ISPs ([in India for example](https://economictimes.indiatimes.com/tech/internet/brace-yourself-for-slower-data-speeds/articleshow/74702264.cms)) are seeing a [sharp increase in home internet usage](https://www.npr.org/2020/03/17/817154787/internet-traffic-surges-as-companies-and-schools-send-people-home) and don't have the infrastructure to meet the increased demand. In situations like this your website speed may be getting slower through no fault of your own. Optimizing your load performance could be a way to offset the headwind of reduced bandwidth. In other words, by reducing the number of bytes that need to be sent over the network in order to load your pages, you can offset the performance impact of reduced bandwidth.

- Images are the [number one cause of bloat on the web](https://images.guide/#introduction). You might be able to significantly reduce your website's bandwidth usage by [optimizing your images](/fast/#optimize-your-images). [Squoosh](https://squoosh.app) is a simple open source image compression tool that can help you quickly compress your images.
- Run [WebPageTest](https://webpagetest.org/easy) or [Lighthouse](https://developers.google.com/web/tools/lighthouse/#get-started) to discover your top performance improvement opportunities.
- [Enable text compression](/uses-text-compression/) to reduce the network size of text resources. This is often an easy performance win that requires minimal technical investment.
- Read [Fixing website speed cross-functionally](/fixing-website-speed-cross-functionally/) to learn how to collaborate with and get buy-in from other departments.
- [Use standardized lazy-loading for images](/browser-level-image-lazy-loading/) to minimize requests for images that people may never actually see. [Browser compatibility](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#Browser_compatibility) is not 100% but the feature can be treated as a progressive enhancement. In other words, if a certain browser doesn't support standardized lazy-loading, the image should load as it normally does.
- Check if your site has any A/B testing or personalization scripts that can be loaded more asynchronously or if there's any non-critical functionality in the scripts that can be disabled. A/B testing and personalization scripts usually can't be loaded _completely_ asynchronously because they need to run before the page content loads, but there may be some opportunity to load parts of the scripts more asynchronously. See [Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path) to understand the fundamental tradeoff between synchronous scripts (also known as render-blocking scripts) in general and page load time, and then decide whether you need to prioritize the render-blocking scripts over page load time, or vice versa.
- Third-party code constitutes [around half of all requests](https://almanac.httparchive.org/en/2019/third-parties) for most websites. Consider [optimizing](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript) or temporarily removing or disabling third-party code that isn't fundamental to running your site.
- If feature releases are deprioritized, this might be the perfect time to clean up. Remove tags from your tag managers, clean up bloated CSS and JS, and remove deprecated features or code. The [Coverage tab](https://developers.google.com/web/tools/chrome-devtools/coverage) in Chrome DevTools and the [`Coverage`](https://pptr.dev/#?product=Puppeteer&version=v2.1.1&show=api-class-coverage) class in Puppeteer can help you detect unused code.

See [Fast load times](/fast/) for more guidance.

[Hero image](https://unsplash.com/photos/Q1p7bh3SHj8) by [NASA](https://unsplash.com/@nasa) on [Unsplash](https://unsplash.com/s/photos/earth)

<a href="/tags/accessibility/" class="w-chip">Accessibility</a> <a href="/tags/performance/" class="w-chip">Performance</a> <a href="/tags/seo/" class="w-chip">SEO</a> <a href="/tags/ux/" class="w-chip">UX</a> <a href="/tags/security/" class="w-chip">Security</a> <a href="/tags/mobile/" class="w-chip">Mobile</a> <a href="/tags/forms/" class="w-chip">Forms</a> <a href="/tags/images/" class="w-chip">Images</a> <a href="/tags/css/" class="w-chip">CSS</a> <a href="/tags/javascript/" class="w-chip">JavaScript</a> <a href="/tags/lighthouse/" class="w-chip">Lighthouse</a> <a href="/tags/media/" class="w-chip">Media</a> <a href="/tags/devtools/" class="w-chip">DevTools</a>

<span class="w-mr--sm"> Last updated: Apr 6, 2020 </span> [Improve article](https://github.com/GoogleChrome/web.dev/blob/master/src/site/content/en/blog/covid19/index.md)

<a href="/blog" class="w-article-navigation__link w-article-navigation__link--back w-article-navigation__link--single gc-analytics-event">Return to all articles</a>

- ### Contribute

  - <a href="https://github.com/GoogleChrome/web.dev/issues/new?assignees=&amp;labels=bug&amp;template=bug_report.md&amp;title=" class="w-footer__linkbox-link">File a bug</a>
  - <a href="https://github.com/googlechrome/web.dev" class="w-footer__linkbox-link">View source</a>

- ### Related content

  - <a href="https://blog.chromium.org/" class="w-footer__linkbox-link">Chrome updates</a>
  - <a href="https://developers.google.com/web/" class="w-footer__linkbox-link">Web Fundamentals</a>
  - <a href="https://developers.google.com/web/showcase/" class="w-footer__linkbox-link">Case studies</a>
  - <a href="https://devwebfeed.appspot.com/" class="w-footer__linkbox-link">DevWeb Content Firehose</a>
  - <a href="/podcasts/" class="w-footer__linkbox-link">Podcasts</a>
  - <a href="/shows/" class="w-footer__linkbox-link">Shows</a>

- ### Connect

  - <a href="https://www.twitter.com/@ChromiumDev" class="w-footer__linkbox-link">Twitter</a>
  - <a href="https://www.youtube.com/user/ChromeDevelopers" class="w-footer__linkbox-link">YouTube</a>

<a href="https://developers.google.com/" class="w-footer__utility-logo-link"><img src="/images/lockup-color.png" alt="Google Developers" class="w-footer__utility-logo" width="185" height="33" /></a>

- <a href="https://developer.chrome.com/home" class="w-footer__utility-link">Chrome</a>
- <a href="https://firebase.google.com/" class="w-footer__utility-link">Firebase</a>
- <a href="https://cloud.google.com/" class="w-footer__utility-link">Google Cloud Platform</a>
- <a href="https://developers.google.com/products" class="w-footer__utility-link">All products</a>

<!-- -->

- <a href="https://policies.google.com/" class="w-footer__utility-link">Terms &amp; Privacy</a>
- <a href="/community-guidelines/" class="w-footer__utility-link">Community Guidelines</a>

Except as otherwise noted, the content of this page is licensed under the [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/), and code samples are licensed under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0). For details, see the [Google Developers Site Policies](https://developers.google.com/site-policies).
