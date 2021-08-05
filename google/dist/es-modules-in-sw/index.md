<span class="w-tooltip w-tooltip--left">Open menu</span>

<a href="/" class="header-default__logo-link gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="header-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="header-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="header-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="header-default__link gc-analytics-event">Blog</a> <a href="/about/" class="header-default__link gc-analytics-event">About</a>

<span class="w-tooltip">Close</span>

<a href="/" class="gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="drawer-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="drawer-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="drawer-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="drawer-default__link gc-analytics-event">Blog</a> <a href="/about/" class="drawer-default__link gc-analytics-event">About</a>

<img src="https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format" alt="Modular, abstract architecture." class="w-hero w-hero--cover" sizes="100vw" srcset="https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=200 200w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=228 228w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=260 260w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=296 296w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=338 338w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=385 385w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=439 439w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=500 500w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=571 571w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=650 650w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=741 741w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=845 845w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=964 964w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=1098 1098w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=1252 1252w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=1428 1428w,     https://web-dev.imgix.net/image/FNkVSAX8UDTTQWQkKftSgGe9clO2/JobkNOB1V5C9bp7x4Jur.jpg?auto=format&amp;w=1600 1600w" width="1600" height="480" />

## <a href="#es-modules-in-service-workers" class="w-toc__header--link">ES modules in service workers</a>

- [Background](#background)
- [Use cases](#use-cases)
- [Current limitations](#current-limitations)
- [Static imports only](#static-imports-only)
- [No support for import maps](#no-support-for-import-maps)
- [Browser support](#browser-support)
- [Example code](#example-code)
- [Backwards compatibility](#backwards-compatibility)

Share <a href="/newsletter/" class="w-actions__fab w-actions__fab--subscribe gc-analytics-event"><span>subscribe</span></a>

- <a href="/" class="w-breadcrumbs__link w-breadcrumbs__link--left-justify gc-analytics-event">Home</a>
- <a href="/blog" class="w-breadcrumbs__link gc-analytics-event">All articles</a>

# ES modules in service workers

A modern alternative to importScripts().

May 13, 2021

[<img src="https://web-dev.imgix.net/image/admin/uskKSRCW1HyOTCjtdMdo.jpg?auto=format&amp;fit=crop&amp;h=64&amp;w=64" alt="Jeff Posnick" class="w-author__image" sizes="(min-width: 64px) 64px, calc(100vw - 48px)" srcset="https://web-dev.imgix.net/image/admin/uskKSRCW1HyOTCjtdMdo.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=1&amp;q=75 1x,     https://web-dev.imgix.net/image/admin/uskKSRCW1HyOTCjtdMdo.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=2&amp;q=50 2x,     https://web-dev.imgix.net/image/admin/uskKSRCW1HyOTCjtdMdo.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=3&amp;q=35 3x,     https://web-dev.imgix.net/image/admin/uskKSRCW1HyOTCjtdMdo.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=4&amp;q=23 4x,     https://web-dev.imgix.net/image/admin/uskKSRCW1HyOTCjtdMdo.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=5&amp;q=20 5x" width="64" height="64" />](/authors/jeffposnick/)

<a href="/authors/jeffposnick/" class="w-author__name-link">Jeff Posnick</a>

- <a href="https://twitter.com/jeffposnick" class="w-author__link">Twitter</a>
- <a href="https://github.com/jeffposnick" class="w-author__link">GitHub</a>
- <a href="https://glitch.com/@jeffposnick" class="w-author__link">Glitch</a>
- <a href="https://twitter.com/jeffposnick" class="w-author__link">Blog</a>

## Background <a href="#background" class="w-headline-link">#</a>

[ES modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) have been a developer favorite for a while now. In addition to a [number of other benefits](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/), they offer the promise of a universal module format where shared code can be released once and run in browsers and in alternative runtimes like [Node.js](https://nodejs.org/en/). While [all modern browsers](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#import) offer some ES module support, they don't all offer support _everywhere_ that code can be run. Specifically, support for importing ES modules inside of a browser's [service worker](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API/Using_Service_Workers) is just starting to become more widely available.

This article details the current state of ES module support in service workers across common browsers, along with some gotchas to avoid, and best practices for shipping backwards-compatible service worker code.

## Use cases <a href="#use-cases" class="w-headline-link">#</a>

The ideal use case for ES modules inside of service workers is for loading a modern library or configuration code that's shared with other runtimes that support ES modules.

Attempting to share code in this way prior to ES modules entailed using older "universal" module formats like [UMD](https://github.com/umdjs/umd) that include unneeded boilerplate, and writing code that made changes to globally exposed variables.

Scripts imported via ES modules can trigger the service worker [update](https://developers.google.com/web/fundamentals/primers/service-workers/lifecycle#updates) flow if their contents change, matching the [behavior](https://developers.google.com/web/updates/2019/09/fresher-sw#checks_for_updates_to_imported_scripts) of `importScripts()`.

## Current limitations <a href="#current-limitations" class="w-headline-link">#</a>

### Static imports only <a href="#static-imports-only" class="w-headline-link">#</a>

ES modules can be imported in one of two ways: either [statically](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import), using the `import ... from '...'` syntax, or [dynamically](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import#dynamic_imports), using the `import()` method. Inside of a service worker, only the static syntax is currently supported.

This limitation is analogous to a [similar restriction](https://developers.google.com/web/updates/2018/10/tweaks-to-addAll-importScripts) placed on `importScripts()` usage. Dynamic calls to `importScripts()` do not work inside of a service worker, and all `importScripts()` calls, which are inherently synchronous, must complete before the service worker completes its `install` phase. This restriction ensures that the browser knows about, and is able to implicitly cache, all JavaScript code needed for a service worker's implementation during installation.

Eventually, this restriction might be lifted, and dynamic ES module imports [may be allowed](https://github.com/w3c/ServiceWorker/issues/1356#issuecomment-783220858). For now, ensure that you only use the static syntax inside of a service worker.

#### What about other workers? <a href="#what-about-other-workers" class="w-headline-link">#</a>

Support for [ES modules in "dedicated" workers](https://web.dev/module-workers/)—those constructed with `new Worker('...', {type: 'module'})`—is more widespread, and has been supported in Chrome and Edge since [version 80](https://chromestatus.com/feature/5761300827209728), as well as [recent versions](https://bugs.webkit.org/show_bug.cgi?id=164860) of Safari. Both static and dynamic ES module imports are supported in dedicated workers.

Chrome and Edge have supported ES modules in [shared workers](https://developer.mozilla.org/en-US/docs/Web/API/SharedWorker) since [version 83](https://chromestatus.com/feature/5169440012369920), but no other browser offers support at this time.

### No support for import maps <a href="#no-support-for-import-maps" class="w-headline-link">#</a>

[Import maps](https://github.com/WICG/import-maps/blob/main/README.md) allow runtime environments to rewrite module specifiers, to, for example, prepend the URL of a preferred CDN from which the ES modules can be loaded.

While Chrome and Edge [version 89](https://www.chromestatus.com/feature/5315286962012160) and above support import maps, they currently [cannot be used](https://github.com/WICG/import-maps/issues/2) with service workers.

## Browser support <a href="#browser-support" class="w-headline-link">#</a>

ES modules in service workers are supported in Chrome and Edge starting with [version 91](https://chromestatus.com/feature/4609574738853888).

Safari added support in the [Technology Preview 122 Release](https://webkit.org/blog/11577/release-notes-for-safari-technology-preview-122/#:~:text=Added%20support%20for%20modules%20in%20Service%20Workers), and developers should expect to see this functionality released in the stable version of Safari in the future.

Firefox does not currently support this functionality, and updates on their position can be found in this [GitHub issue](https://github.com/mozilla/standards-positions/issues/499).

## Example code <a href="#example-code" class="w-headline-link">#</a>

This is a basic example of using a shared ES module in a web app's `window` context, while also registering a service worker that uses the same ES module:

    // Inside config.js:
    export const cacheName = 'my-cache';

    // Inside your web app:
    <script type="module">
      import {cacheName} from './config.js';
      // Do something with cacheName.

      await navigator.serviceWorker.register('es-module-sw.js', {
        type: 'module',
      });
    </script>

    // Inside es-module-sw.js:
    import {cacheName} from './config.js';

    self.addEventListener('install', (event) => {
      event.waitUntil((async () => {
        const cache = await caches.open(cacheName);
        // ...
      })());
    });

### Backwards compatibility <a href="#backwards-compatibility" class="w-headline-link">#</a>

The above example would work fine if all browsers supported ES modules in service workers, but as of this writing, that's not the case.

To accommodate browsers that don't have built-in support, you can run your service worker script through an [ES module-compatible bundler](https://bundlers.tooling.report/) to create a service worker that includes all of the module code inline, and will work in older browsers. Alternatively, if the modules you're attempting to import are already available bundled in [IIFE](https://developer.mozilla.org/en-US/docs/Glossary/IIFE) or [UMD](https://github.com/umdjs/umd) formats, you can import them using `importScripts()`.

Once you have two versions of your service worker available—one that uses ES modules, and the other that doesn't—you'll need to detect what the current browser supports, and register the corresponding service worker script. The best practices for detecting support are currently in flux, but you can follow the discussion in this [GitHub issue](https://github.com/w3c/ServiceWorker/issues/1582) for recommendations.

_Photo by [Vlado Paunovic](https://unsplash.com/@vlado?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/@vlado?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)_

<a href="/tags/service-worker/" class="w-chip">Service Worker</a>

<span class="w-mr--sm"> Last updated: May 13, 2021 </span> [Improve article](https://github.com/GoogleChrome/web.dev/blob/master/src/site/content/en/blog/es-modules-in-sw/index.md)

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