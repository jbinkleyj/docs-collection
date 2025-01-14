<span class="w-tooltip w-tooltip--left">Open menu</span>

<a href="/" class="header-default__logo-link gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="header-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="header-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="header-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="header-default__link gc-analytics-event">Blog</a> <a href="/about/" class="header-default__link gc-analytics-event">About</a>

<span class="w-tooltip">Close</span>

<a href="/" class="gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="drawer-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="drawer-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="drawer-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="drawer-default__link gc-analytics-event">Blog</a> <a href="/about/" class="drawer-default__link gc-analytics-event">About</a>

<img src="https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format" alt="A black-on-white printed sign saying Private, on a wooden wall." class="w-hero w-hero--cover" sizes="100vw" srcset="https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=200 200w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=228 228w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=260 260w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=296 296w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=338 338w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=385 385w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=439 439w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=500 500w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=571 571w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=650 650w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=741 741w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=845 845w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=964 964w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=1098 1098w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=1252 1252w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=1428 1428w,     https://web-dev.imgix.net/image/admin/5F89q0kLUOLWvYtNJeWZ.jpg?auto=format&amp;w=1600 1600w" width="1600" height="480" />

## <a href="#digging-into-the-privacy-sandbox" class="w-toc__header--link">Digging into the Privacy Sandbox</a>

- [Summary](#summary)
- [The current state of privacy on the web](#background)
- [Introducing the Privacy Sandbox](#introduction)
- [The Privacy Sandbox proposals](#proposals)
- [Use cases and goals](#use-cases-and-goals)
- [Measure conversion](#measure-conversion)
- [Select ads](#select-ads)
- [Combat fingerprinting](#combat-fingerprinting)
- [IP address security](#ip-address-security)
- [Combat spam, fraud and denial-of-service attacks](#combat-spam-fraud-and-denial-of-service-attacks)
- [Enable domains to belong to the same first party](#enable-domains-to-belong-to-the-same-first-party)
- [Find out more](#find-out-more)
- [Privacy Sandbox proposal explainers](#explainers)
- [The Privacy Sandbox](#the-privacy-sandbox)
- [Use cases, policies, and requirements](#use-cases-policies-requirements)
- [Appendix: Glossary of terms used in the proposal explainers](#glossary)
- [Click-through rate (CTR)](#glossary-ctr)
- [Click-through-conversion (CTC)](#glossary-ctc)
- [Conversion](#conversion)
- [Differential privacy](#differential-privacy)
- [Domain](#domain)
- [eTLD, eTLD+1](#glossary-etld)
- [Entropy](#entropy)
- [Fingerprinting](#glossary-fingerprinting)
- [Fingerprinting surface](#glossary-fingerprinting-surface)
- [First-party](#glossary-first-party)
- [Impression](#glossary-impression)
- [k-anonymity](#k-anonymity)
- [Nonce](#nonce)
- [Origin](#origin)
- [Passive surface](#glossary-passive-surface)
- [Publisher](#publisher)
- [Reach](#reach)
- [Remarketing](#remarketing)
- [Site](#site)
- [Surface](#surface)
- [Third-party](#glossary-third-party)
- [Top-level domain (TLD)](#glossary-tld)
- [.well-known](#.well-known)

Share <a href="/newsletter/" class="w-actions__fab w-actions__fab--subscribe gc-analytics-event"><span>subscribe</span></a>

- <a href="/" class="w-breadcrumbs__link w-breadcrumbs__link--left-justify gc-analytics-event">Home</a>
- <a href="/blog" class="w-breadcrumbs__link gc-analytics-event">All articles</a>

# Digging into the Privacy Sandbox

The Privacy Sandbox is a series of proposals to satisfy third-party use cases without third-party cookies or other tracking mechanisms.

Apr 8, 2020 <span class="w-author__separator">•</span> Updated Dec 21, 2020

<span class="w-post-signpost__title">Appears in:</span> <a href="/secure" class="w-post-signpost__link">Safe and secure</a>

[<img src="https://web-dev.imgix.net/image/admin/wPss4TJX9IJ1CJza7iFY.jpg?auto=format&amp;fit=crop&amp;h=64&amp;w=64" alt="Sam Dutton" class="w-author__image" sizes="(min-width: 64px) 64px, calc(100vw - 48px)" srcset="https://web-dev.imgix.net/image/admin/wPss4TJX9IJ1CJza7iFY.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=1&amp;q=75 1x,     https://web-dev.imgix.net/image/admin/wPss4TJX9IJ1CJza7iFY.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=2&amp;q=50 2x,     https://web-dev.imgix.net/image/admin/wPss4TJX9IJ1CJza7iFY.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=3&amp;q=35 3x,     https://web-dev.imgix.net/image/admin/wPss4TJX9IJ1CJza7iFY.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=4&amp;q=23 4x,     https://web-dev.imgix.net/image/admin/wPss4TJX9IJ1CJza7iFY.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=5&amp;q=20 5x" width="64" height="64" />](/authors/samdutton/)

<a href="/authors/samdutton/" class="w-author__name-link">Sam Dutton</a>

- <a href="https://twitter.com/sw12" class="w-author__link">Twitter</a>
- <a href="https://github.com/samdutton" class="w-author__link">GitHub</a>

## Summary <a href="#summary" class="w-headline-link">#</a>

- This post outlines APIs and concepts from the [Privacy Sandbox](https://www.chromium.org/Home/chromium-privacy/privacy-sandbox) proposals.
- The proposals are looking for feedback from the community, particularly from those in the advertising space (publishers, advertisers, and ad tech companies), to suggest missing use cases and share information about how to support your business use cases.
- You can comment on the proposals by filing issues on [the repositories linked to below](#proposals).
- There's a [glossary](#glossary) for the proposals at the end of this post.

---

## The current state of privacy on the web <a href="#background" class="w-headline-link">#</a>

Websites use services from other companies to provide analytics, serve video and do lots of other useful stuff. Composability is one of the web's [superpowers](https://youtu.be/WnCKlNE52tc?t=930). Most notably, ads are included in web pages via third-party JavaScript and iframes. Ad views, clicks and conversions are tracked via third-party cookies and scripts.

However, when you visit a website you may not be aware of the third parties involved and what they're doing with your data. Even publishers and web developers may not understand the entire third-party supply chain.

Ad selection, conversion measurement, and other use cases currently rely on establishing stable cross-site user identity. Historically this has been done with [third-party cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Third-party_cookies), but browsers have begun to restrict access to these cookies. There has also been an [increase in the use of other mechanisms](https://github.com/bslassey/privacy-budget/issues/6) for cross-site user tracking, such as covert browser storage, device fingerprinting, and requests for personal information such as email addresses.

This is a dilemma for the web. How can legitimate third-party use cases be supported without enabling users to be tracked across sites?

In particular, how can websites fund content by enabling third parties to show ads and measure ad performance—but not allow individual users to be profiled? How can advertisers and site owners evaluate a user's authenticity without resorting to dark patterns such as device fingerprinting?

The way things work at the moment can be problematic for the entire web ecosystem, not just users. For publishers and advertisers, tracking identity and using a variety of non-standard third-party solutions can add to technical debt, code complexity, and data risk. Users, developers, publishers, and advertisers should be confident that the web is protecting user privacy choices.

Advertising is a core web business model for the internet, but advertising has to work for everyone. Which brings us to the Privacy Sandbox's mission: to create a thriving web ecosystem that is respectful of users and private by default.

## Introducing the Privacy Sandbox <a href="#introduction" class="w-headline-link">#</a>

The [Privacy Sandbox](https://www.blog.google/products/chrome/building-a-more-private-web/) introduces a set of privacy-preserving APIs to support business models that fund the open web in the absence of tracking mechanisms like third-party cookies.

The Privacy Sandbox APIs require web browsers to take on a new role. Rather than working with limited tools and protections, the APIs enable the user's browser to act on the user's behalf—locally, on their device—to protect the user's identifying information as they navigate the web. The APIs enable use cases such as ad selection and conversion measurement, without revealing individual private and personal information. In engineering terms a [sandbox](/browser-sandbox) is a protected environment; a key principle of the Privacy Sandbox is that a user's personal information should be protected and not shared in a way that lets the user be identified across sites.

This is a shift in direction for browsers. The Privacy Sandbox's vision of the future has browsers providing specific tools to satisfy specific use cases, while preserving user privacy. [A Potential Privacy Model for the Web](https://github.com/michaelkleber/privacy-model) sets out core principles behind the APIs:

- To establish the range of web activity across which the user's browser can let websites treat a person as having a single identity.
- To identify the ways in which information can move across identity boundaries without compromising that separation.

### The Privacy Sandbox proposals <a href="#proposals" class="w-headline-link">#</a>

In order to successfully transition away from third-party cookies the Privacy Sandbox initiative needs your support. The proposal [explainers](https://blog.chromium.org/2019/08/potential-uses-for-privacy-sandbox.html) need feedback from developers as well as publishers, advertisers, and ad technology companies, to suggest missing use cases and share information about how to accomplish their goals in a privacy-safe way.

You can comment on the proposal explainers by filing issues against each repository:

- [Privacy Model for the Web](https://github.com/michaelkleber/privacy-model)  
  Establish the range of web activity across which the user's browser can let websites treat a person as having a single identity. Identify the ways in which information can move across identity boundaries without compromising that separation.
- [Privacy Budget](https://github.com/bslassey/privacy-budget)  
  Limit the total amount of potentially identifiable data that sites can access. Update APIs to reduce the amount of potentially identifiable data revealed. Make access to potentially identifiable data measurable.
- [Willful IP Blindness](https://github.com/bslassey/ip-blindness)  
  Enable sites to 'blind' themselves to IP addresses so they can avoid consuming privacy budget.
- [Trust Token API](https://github.com/dvorak42/trust-token-api)  
  Enable an origin that trusts a user to issue them with cryptographic tokens which are stored by the user's browser so they can be used in other contexts to evaluate the user's authenticity.
- [First-Party Sets](https://github.com/krgovind/first-party-sets/)  
  Allow related domain names owned by the same entity to declare themselves as belonging to the same first party.
- [Aggregated Reporting](https://github.com/csharrison/aggregate-reporting-api)  
  Provide privacy preserving mechanisms to support a variety of use cases such as view-through-conversion, brand, lift, and reach measurement.
- [Click Through Conversion Measurement Event-Level](https://github.com/csharrison/conversion-measurement-api)  
  Provide privacy preserving [click-through-conversion](#glossary-ctc) measurement.
- [Federated Learning of Cohorts](https://github.com/jkarlin/floc)  
  The browser groups together many users with similar browsing histories into a group (or "cohort"). Advertisers can select ads for this large group based on mass observations, but cannot recognize individual people in it.
- [TURTLEDOVE](https://github.com/michaelkleber/turtledove)  
  Enable some form of on-device 'auction' to choose the most relevant ads which would include ads that remarket an advertiser based on a prior expression of interest by the user.

You can dive into the API proposal explainers right away, and over the coming months we'll be publishing posts about each proposal individually.

## Use cases and goals <a href="#use-cases-and-goals" class="w-headline-link">#</a>

### Measure conversion <a href="#measure-conversion" class="w-headline-link">#</a>

**Goal:** Enable advertisers to measure ad performance.

There are two proposals for APIs where information about ad impressions and conversions stays inside the browser, and which only offer carefully controlled, privacy-safe ways for that information to get back to advertisers. This controlled, privacy-safe reporting is done in a way that does not enable linking of identities across sites or collection of user browsing history:

- [Click Through Conversion Measurement Event-Level](https://github.com/csharrison/conversion-measurement-api) allows advertisers to determine which ad clicks later turned into conversions. (API name suggestions welcome!)
- [Aggregated Reporting](https://github.com/csharrison/aggregate-reporting-api) aggregates browsing data for multiple sites and multiple users in a single report, while preserving privacy by only allowing aggregate reporting on things that a lot of different people did.

Other companies have been investigating similar ideas, such as Facebook's [Cross-Browser Anonymous Conversion Reporting](https://github.com/w3c/web-advertising/blob/master/cross-browser-anonymous-conversion-reporting.md), Apple's [Ad Click Attribution API](https://webkit.org/blog/8943/privacy-preserving-ad-click-attribution-for-the-web/) and Brave's [ad conversion attribution](https://github.com/brave/brave-browser/issues/6536).

### Select ads <a href="#select-ads" class="w-headline-link">#</a>

**Goal:** Enable advertisers to display ads relevant to users.

Relevant ads are [more favorable to users and more profitable for publishers](https://services.google.com/fh/files/misc/disabling_third-party_cookies_publisher_revenue.pdf) (the people running ad-supported websites). Third party ad selection tools make ad space more valuable to advertisers (the people who purchase ad space on websites) which in turn increases revenue for ad-supported websites and enables content to get created and published.

There are many ways to make ads relevant to the user, including the following:

- **First-party-data**: Show ads relevant to topics a person has told a website they have an interest in, or content a person has looked at previously on the current website.
- **Contextual**: Choose where to display ads based on site content. For example, 'Put this ad next to articles about knitting.'
- **Remarketing**: Advertise to people who've already visited your site, while they are not on your site. For example, 'Show this ad for discount wool to people who visited your store and left knitting items in their shopping cart—while they're visiting craft sites.'
- **Interest-based**: Select ads based on a user's browsing history. For example, 'Show this ad to users whose browsing behaviour indicates they might be interested in knitting'.

First-party-data and contextual ad selection can be achieved without knowing anything about the user other than their activity within a site. These techniques don't require cross-site tracking.

[Remarketing](#remarketing) is usually done by using cookies or some other way to recognize people across websites: adding users to lists and then selecting specific ads to show them.

Interest-based ad selection currently uses cookies to track user behaviour across as many sites as possible. Many people are concerned about the privacy implications of ad selection. The Privacy Sandbox proposes two alternatives, for remarketing and for interest-based selection:

- [TURTLEDOVE](https://github.com/michaelkleber/turtledove): **for remarketing**.  
  The API enables the final ad "auction" to choose the most relevant ads to be moved to the browser. The API leverages information which is only stored in the user's browser itself, about advertisers the user had previously expressed an interest in, along with information about the current page. Two requests are sent for ads: one to retrieve an ad based on contextual data, and one to retrieve an ad based on an advertiser-defined interest. The browser has the responsibility of ensuring these requests are independent and _uncorrelated_ so they can't be linked together to let an ad network know that the requests are from the same person. An "auction" is then conducted by the browser to choose the most relevant ad, using JavaScript code provided by the advertiser. This code _can only be used to choose between ads_: it cannot make network requests, or access the DOM or external state.

- [FLoC](https://github.com/jkarlin/floc): **for interest-based audiences**.  
  The API generates clusters of similar people, known as "cohorts". Data is generated locally on the user's browser, not by a third party. The browser shares the generated cohort data, but this cannot be used to identify or track individual users. This enables companies to select ads based on the behavior of people with similar browsing behaviour, while preserving privacy.

### Combat fingerprinting <a href="#combat-fingerprinting" class="w-headline-link">#</a>

**Goal:** Reduce the amount of potentially identifiable data revealed by APIs and make access to potentially identifiable data controllable by users, and measurable.

Browsers have taken steps to [deprecate third-party cookies](https://blog.chromium.org/2020/01/building-more-private-web-path-towards.html), but techniques to identify and track the behaviour of individual users, known as fingerprinting, have continued to evolve. Fingerprinting uses mechanisms that users aren't aware of and can't control.

- The [Privacy Budget](https://github.com/bslassey/privacy-budget) proposal aims to limit the potential for fingerprinting by identifying how much fingerprint data is exposed by JavaScript APIs or other 'surfaces' (such as HTTP request headers) and setting a limit on how much of this data can be accessed.

- Fingerprinting surfaces such as the [User-Agent](https://github.com/WICG/ua-client-hints) header will be reduced in scope, and the data made available by alternative mechanisms such as [Client Hints](https://wicg.github.io/ua-client-hints/) will be subject to Privacy Budget limits. Other surfaces, such as the [device orientation](https://bugs.chromium.org/p/chromium/issues/detail?id=1018180) and [battery-level](https://bugs.chromium.org/p/chromium/issues/detail?id=661792) APIs, will be updated to keep the information exposed to a minimum.

### IP address security <a href="#ip-address-security" class="w-headline-link">#</a>

**Goal:** Control access to IP addresses to reduce covert fingerprinting, and allow sites to opt out of seeing IP addresses in order to not consume [privacy budget](https://github.com/bslassey/privacy-budget).

A user's IP address is the public 'address' of their computer on the internet, which in most cases is dynamically assigned by the network through which they connect to the internet. However, even dynamic IP addresses may remain stable over a significant period of time. Not surprisingly, this means that IP addresses are a significant source of fingerprint data.

- The [Willful IP Blindness](https://github.com/bslassey/ip-blindness) proposal is an attempt to provide a privacy-preserving approach that avoids consuming privacy budget.

### Combat spam, fraud and denial-of-service attacks <a href="#combat-spam-fraud-and-denial-of-service-attacks" class="w-headline-link">#</a>

**Goal:** Verify user authenticity without fingerprinting.

Anti-fraud protection is crucial for keeping users safe, and to ensure that advertisers and site owners can get accurate ad performance measurements. Advertisers and site owners must be able to distinguish between malicious bots and authentic users. If advertisers can't reliably tell which ad clicks are from real humans, they spend less, so site publishers get less revenue. Many third party services currently use techniques such as [device fingerprinting](#fingerprinting) to combat fraud.

Unfortunately, the techniques used to identify legitimate users and block spammers, fraudsters, and bots work in ways similar to [fingerprinting](#glossary-fingerprinting) techniques that damage privacy.

- The [Trust Tokens API](https://github.com/dvorak42/trust-token-api) proposes an alternative approach, allowing authenticity established for a user in one context, such as a social media site, to be conveyed to another context, such as an ad running on a news site—without identifying the user or linking the two identities.

### Enable domains to belong to the same first party <a href="#enable-domains-to-belong-to-the-same-first-party" class="w-headline-link">#</a>

**Goal:** Enable entities to declare that related domain names are owned by the same first party.

Many organizations own sites across multiple domains. This can become a problem if restrictions are imposed on tracking user identity across sites that are seen as 'third-party' but actually belong to the same organization.

- [First Party Sets](https://github.com/krgovind/first-party-sets/) aims to make the web's concept of first and third parties more closely aligned with the real world's by enabling multiple domains to declare themselves as belonging to the same first party.

## Find out more <a href="#find-out-more" class="w-headline-link">#</a>

### Privacy Sandbox proposal explainers <a href="#explainers" class="w-headline-link">#</a>

The Privacy Sandbox initiative needs your support. The API proposal [explainers](https://blog.chromium.org/2019/08/potential-uses-for-privacy-sandbox.html) need feedback, in particular to suggest missing use cases and more-private ways to accomplish their goals.

- [Privacy Budget](https://github.com/bslassey/privacy-budget)
- [Trust Token API](https://github.com/dvorak42/trust-token-api)
- [Willful IP Blindness](https://github.com/bslassey/ip-blindness)
- [Aggregated Reporting API](https://github.com/csharrison/aggregate-reporting-api)
- [Conversion measurement](https://github.com/csharrison/conversion-measurement-api)
- [Federated Learning of Cohorts](https://github.com/jkarlin/floc)
- [TURTLEDOVE](https://github.com/michaelkleber/turtledove)

[A Potential Privacy Model for the Web](https://github.com/michaelkleber/privacy-model) sets out the core principles underlying the APIs.

### The Privacy Sandbox <a href="#the-privacy-sandbox" class="w-headline-link">#</a>

- [The Privacy Sandbox](https://www.chromium.org/Home/chromium-privacy/privacy-sandbox)
- Privacy Sandbox overview: [Building a more private web](https://www.blog.google/products/chrome/building-a-more-private-web/)
- Google AI Blog: [Federated Learning: Collaborative Machine Learning without Centralized Training Data](https://ai.googleblog.com/2017/04/federated-learning-collaborative.html)
- [The future of third-party cookies](https://blog.chromium.org/2019/10/developers-get-ready-for-new.html)

### Use cases, policies, and requirements <a href="#use-cases-policies-requirements" class="w-headline-link">#</a>

- [Advertising Use Cases](https://github.com/w3c/web-advertising/blob/master/support_for_advertising_use_cases.md)
- [Mozilla anti-tracking policy](https://wiki.mozilla.org/Security/Anti_tracking_policy)
- [WebKit tracking prevention policy](https://webkit.org/tracking-prevention-policy/)
- [Privacy Preserving Ad Click Attribution For the Web](https://webkit.org/blog/8943/privacy-preserving-ad-click-attribution-for-the-web/)
- [Brave, Fingerprinting, and Privacy Budgets](https://brave.com/brave-fingerprinting-and-privacy-budgets/)

---

## Appendix: Glossary of terms used in the proposal explainers <a href="#glossary" class="w-headline-link">#</a>

### Click-through rate (CTR) <a href="#glossary-ctr" class="w-headline-link">#</a>

The ratio of users who click on an ad, having seen it. (See also [impression](#glossary-impression).)

### Click-through-conversion (CTC) <a href="#glossary-ctc" class="w-headline-link">#</a>

A conversion attributed to an ad that was 'clicked'.

### Conversion <a href="#conversion" class="w-headline-link">#</a>

The completion of an action on an advertiser's website by a user who has previously interacted with an ad from that advertiser. For example, purchase of a product or sign-up for a newsletter after clicking an ad that links to the advertiser's site.

### Differential privacy <a href="#differential-privacy" class="w-headline-link">#</a>

Share information about a dataset to reveal patterns of behaviour without revealing private information about individuals or whether they belong to the dataset.

### Domain <a href="#domain" class="w-headline-link">#</a>

See [Top-Level Domain](#glossary-tld) and [eTLD](#glossary-etld).

### eTLD, eTLD+1 <a href="#glossary-etld" class="w-headline-link">#</a>

'Effective' top level domains are defined by the [Public Suffix List](https://publicsuffix.org/list/). For example:

    co.uk
    appspot.com
    glitch.me

Effective TLDs are what enable foo.appspot.com to be a different site from bar.appspot.com. The effective top-level domain (**eTLD**) in this case is appspot.com, and the whole **site** name (foo.appspot.com, bar.appspot.com) is known as the **eTLD+1**.

See also [Top-Level Domain](#glossary-tld).

### Entropy <a href="#entropy" class="w-headline-link">#</a>

A measure of how much an item of data reveals individual identity.

Data entropy is measured in bits. The more that data reveals identity, the higher its entropy value.

Data can be combined to identify an individual, but it can be difficult to work out whether new data adds to entropy. For example, knowing a person is from Australia doesn't reduce entropy if you already know the person is from Kangaroo Island.

### Fingerprinting <a href="#glossary-fingerprinting" class="w-headline-link">#</a>

Techniques to identify and track the behaviour of individual users. Fingerprinting uses mechanisms that users aren't aware of and can't control. Sites such as [Panopticlick](https://panopticlick.eff.org) and [amiunique.org](https://amiunique.org/) show how fingerprint data can be combined to identify you as an individual.

### Fingerprinting surface <a href="#glossary-fingerprinting-surface" class="w-headline-link">#</a>

Something that can be used (probably in combination with other surfaces) to identify a particular user or device. For example, the `navigator.userAgent()` JavaScript method and the `User-Agent` HTTP request header provide access to a fingerprinting surface (the user agent string).

### First-party <a href="#glossary-first-party" class="w-headline-link">#</a>

Resources from the site you're visiting. For example, the page you're reading is on the site web.dev and includes resources from that site. See also [Third-party](#glossary-third-party).

### Impression <a href="#glossary-impression" class="w-headline-link">#</a>

View of an ad. (See also [click-through rate](#glossary-ctr).)

### k-anonymity <a href="#k-anonymity" class="w-headline-link">#</a>

A measure of anonymity within a data set. If you have _k_ anonymity, you can't be distinguished from _k-1_ other individuals in the data set. In other words, _k_ individuals have the same information (including you).

### Nonce <a href="#nonce" class="w-headline-link">#</a>

Arbitrary number used once only in cryptographic communication.

### Origin <a href="#origin" class="w-headline-link">#</a>

The origin of a request, including the server name but no path information. For example: `https://web.dev`.

### Passive surface <a href="#glossary-passive-surface" class="w-headline-link">#</a>

Some fingerprinting surfaces, such as user agent strings, IP addresses and accept-language headers, are available to every website whether the site asks for them or not. That means passive surfaces can easily consume a site's privacy budget.

The Privacy Sandbox initiative proposes replacing passive surfaces with active ways to get specific information, for example using Client Hints a single time to get the user's language rather than having an accept-language header for every response to every server.

### Publisher <a href="#publisher" class="w-headline-link">#</a>

The Privacy Sandbox proposal explainers are mostly about ads, so the kinds of publishers referred to are ones that put ads on their websites.

### Reach <a href="#reach" class="w-headline-link">#</a>

The total number of people who see an ad.

### Remarketing <a href="#remarketing" class="w-headline-link">#</a>

Advertising to people who've already visited your site. For example, an online store could show ads for a toy sale to people who previously viewed toys on their site.

### Site <a href="#site" class="w-headline-link">#</a>

See [Top-Level Domain](#glossary-tld) and [eTLD](#glossary-etld).

### Surface <a href="#surface" class="w-headline-link">#</a>

See [Fingerprinting surface](#glossary-fingerprinting-surface) and [Passive surface](#glossary-passive-surface).

### Third-party <a href="#glossary-third-party" class="w-headline-link">#</a>

Resources served from a domain that's different from the website you're visiting. For example, a website foo.com might use analytics code from google-analytics.com (via JavaScript), fonts from use.typekit.net (via a link element) and a video from vimeo.com (in an iframe). See also [First-party](#glossary-first-party).

### Top-level domain (TLD) <a href="#glossary-tld" class="w-headline-link">#</a>

Top-level domains such as .com and .org are listed in the [Root Zone Database](https://www.iana.org/domains/root/db).

Note that some 'sites' are actually just subdomains. For example, translate.google.com and maps.google.com are just subdomains of google.com (which is the [eTLD + 1](#glossary-etld)).

### .well-known <a href="#.well-known" class="w-headline-link">#</a>

It can be useful to access policy or other information about a host _before_ making a request. For example, robots.txt tells web crawlers which pages to visit and which pages to ignore. IETF [RFC8615](https://tools.ietf.org/html/rfc8615) outlines a standardized way to make site-wide metadata accessible in standard locations in a /.well-known/ subdirectory. You can see a list of these at [iana.org/assignments/well-known-uris/well-known-uris.xhtml](https://www.iana.org/assignments/well-known-uris/well-known-uris.xhtml).

---

Thanks to all those who helped with writing and reviewing this post.

Photo by [Pierre Bamin](https://unsplash.com/@bamin?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText).

<a href="/tags/privacy/" class="w-chip">Privacy</a> <a href="/tags/security/" class="w-chip">Security</a>

<span class="w-mr--sm"> Last updated: Dec 21, 2020 </span> [Improve article](https://github.com/GoogleChrome/web.dev/blob/master/src/site/content/en/blog/digging-into-the-privacy-sandbox/index.md)

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
