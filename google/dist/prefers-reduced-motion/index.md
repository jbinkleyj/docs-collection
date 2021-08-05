<span class="w-tooltip w-tooltip--left">Open menu</span>

<a href="/" class="header-default__logo-link gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="header-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="header-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="header-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="header-default__link gc-analytics-event">Blog</a> <a href="/about/" class="header-default__link gc-analytics-event">About</a>

<span class="w-tooltip">Close</span>

<a href="/" class="gc-analytics-event"><img src="/images/lockup.svg" alt="web.dev" class="drawer-default__logo" width="125" height="30" /></a>

<a href="/learn/" class="drawer-default__link gc-analytics-event">Learn</a> <a href="/measure/" class="drawer-default__link gc-analytics-event">Measure</a> <a href="/blog/" class="drawer-default__link gc-analytics-event">Blog</a> <a href="/about/" class="drawer-default__link gc-analytics-event">About</a>

<img src="https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format" alt="Time-lapse of woman in a train" class="w-hero w-hero--cover" sizes="100vw" srcset="https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=200 200w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=228 228w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=260 260w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=296 296w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=338 338w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=385 385w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=439 439w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=500 500w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=571 571w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=650 650w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=741 741w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=845 845w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=964 964w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=1098 1098w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=1252 1252w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=1428 1428w,     https://web-dev.imgix.net/image/admin/LI2vYKZwQ98w3MLtUF8V.jpg?auto=format&amp;w=1600 1600w" width="1600" height="480" />

## <a href="#prefers-reduced-motion:-sometimes-less-movement-is-more" class="w-toc__header--link">prefers-reduced-motion: Sometimes less movement is more</a>

- [Too much motion in real life and on the web](#too-much-motion-in-real-life-and-on-the-web)
- [Animation on the web](#animation-on-the-web)
- [Motion-triggered vestibular spectrum disorder](#motion-triggered-vestibular-spectrum-disorder)
- [Remove motion on operating systems](#remove-motion-on-operating-systems)
- [Remove motion on the web](#remove-motion-on-the-web)
- [Working with the media query](#working-with-the-media-query)
- [Demo](#demo)
- [Conclusions](#conclusions)
- [(Bonus) Forcing reduced motion on all websites](<#(bonus)-forcing-reduced-motion-on-all-websites>)
- [Related Links](#related-links)
- [Acknowledgements](#acknowledgements)

Share <a href="/newsletter/" class="w-actions__fab w-actions__fab--subscribe gc-analytics-event"><span>subscribe</span></a>

- <a href="/" class="w-breadcrumbs__link w-breadcrumbs__link--left-justify gc-analytics-event">Home</a>
- <a href="/blog" class="w-breadcrumbs__link gc-analytics-event">All articles</a>

# prefers-reduced-motion: Sometimes less movement is more

The prefers-reduced-motion media query detects whether the user has requested the operating system to minimize the amount of animation or motion it uses.

Mar 11, 2019 <span class="w-author__separator">•</span> Updated Dec 10, 2019

<span class="w-post-signpost__title">Appears in:</span> <a href="/animations" class="w-post-signpost__link">Animations</a>

[<img src="https://web-dev.imgix.net/image/admin/8PLpVmFef6mj72MVWeiN.jpg?auto=format&amp;fit=crop&amp;h=64&amp;w=64" alt="Thomas Steiner" class="w-author__image" sizes="(min-width: 64px) 64px, calc(100vw - 48px)" srcset="https://web-dev.imgix.net/image/admin/8PLpVmFef6mj72MVWeiN.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=1&amp;q=75 1x,     https://web-dev.imgix.net/image/admin/8PLpVmFef6mj72MVWeiN.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=2&amp;q=50 2x,     https://web-dev.imgix.net/image/admin/8PLpVmFef6mj72MVWeiN.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=3&amp;q=35 3x,     https://web-dev.imgix.net/image/admin/8PLpVmFef6mj72MVWeiN.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=4&amp;q=23 4x,     https://web-dev.imgix.net/image/admin/8PLpVmFef6mj72MVWeiN.jpg?fit=crop&amp;h=64&amp;w=64&amp;auto=format&amp;dpr=5&amp;q=20 5x" width="64" height="64" />](/authors/thomassteiner/)

<a href="/authors/thomassteiner/" class="w-author__name-link">Thomas Steiner</a>

- <a href="https://twitter.com/tomayac" class="w-author__link">Twitter</a>
- <a href="https://github.com/tomayac" class="w-author__link">GitHub</a>
- <a href="https://glitch.com/@tomayac" class="w-author__link">Glitch</a>
- <a href="https://blog.tomayac.com/" class="w-author__link">Blog</a>

Not everyone likes decorative animations or transitions, and some users outright experience motion sickness when faced with parallax scrolling, zooming effects, and so on. Chrome 74 supports a user preference media query `prefers-reduced-motion` that lets you design a motion-reduced variant of your site for users who have expressed this preference.

## Too much motion in real life and on the web <a href="#too-much-motion-in-real-life-and-on-the-web" class="w-headline-link">#</a>

The other day, I was ice skating with my kids. It was a lovely day, the sun was shining, and the ice rink was crammed with people ⛸. The only issue with that: I don't cope with crowds well. With so many moving targets, I fail to focus on anything, and end up lost and with a feeling of complete visual overload, almost like staring at an anthill 🐜.

<figure><img src="https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format" alt="Visual overload in real life." sizes="(min-width: 580px) 580px, calc(100vw - 48px)" srcset="https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=200 200w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=228 228w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=260 260w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=296 296w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=338 338w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=385 385w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=439 439w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=500 500w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=571 571w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=650 650w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=741 741w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=845 845w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=964 964w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=1098 1098w,     https://web-dev.imgix.net/image/admin/JA5v1s8gSBk70eJBB8xW.jpg?auto=format&amp;w=1160 1160w" width="580" height="320" /><figcaption>Visual overload in real life.</figcaption></figure>Occasionally, the same can happen on the web: with flashing ads, fancy parallax effects, surprising reveal animations, autoplaying videos, and so on, *the web sometimes can be quite overwhelming*… Happily, unlike in real life, there is a solution to that. The CSS media query `prefers-reduced-motion` lets developers create a variant of a page for users who, well, prefer reduced motion. This can comprise anything from refraining from having autoplaying videos to disabling certain purely decorative effects, to completely redesigning a page for certain users.

Before I dive into the feature, let's take one step back and think of what animations are used for on the web. If you want, you can also skip the background information and [jump right into the technical details](#working_with_the_media_query) below.

## Animation on the web <a href="#animation-on-the-web" class="w-headline-link">#</a>

Animation is oftentimes used to provide _feedback_ to the user, for example, to let them know that an action was received and is being processed. For example, on a shopping website, a product could be animated to "fly" into a virtual shopping cart, depicted as an icon in the top-right corner of the site.

Another use case involves using motion to [hack user perception](https://medium.com/dev-channel/hacking-user-perception-to-make-your-websites-and-apps-feel-faster-922636b620e3) by using a mixture of skeleton screens, contextual metadata, and low quality image previews to occupy a lot of the user's time and make the whole experience _feel faster_. The idea is to give context to the user of what's coming and meanwhile load in things as quickly as possible.

Finally, there are _decorative_ effects like animated gradients, parallax scrolling, background videos, and several others. While many users enjoy such animations, some users dislike them because they feel distracted or slowed down by them. In the worst case, users may even suffer from motion sickness as if it were a real life experience, so for these users reducing animations is a _medical necessity_.

## Motion-triggered vestibular spectrum disorder <a href="#motion-triggered-vestibular-spectrum-disorder" class="w-headline-link">#</a>

Some users experience [distraction or nausea from animated content](https://www.w3.org/WAI/WCAG21/Understanding/animation-from-interactions.html). For example, scrolling animations can cause vestibular disorders when elements other than the main element associated with the scrolling move around a lot. For example, parallax scrolling animations can cause vestibular disorders because background elements move at a different rate than foreground elements. Vestibular (inner ear) disorder reactions include dizziness, nausea, and migraine headaches, and sometimes require bed rest to recover.

## Remove motion on operating systems <a href="#remove-motion-on-operating-systems" class="w-headline-link">#</a>

Many operating systems have had accessibility settings for specifying a preference for reduced motion for a long time. The screenshots below show macOS Mojave's **Reduce motion** preference and Android Pie's **Remove animations** preference. When checked, these preferences cause the operating system to not use decorative effects like app launching animations. Applications themselves can and should honor this setting, too, and remove all unnecessary animations.

<figure><img src="https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format" sizes="(min-width: 398px) 398px, calc(100vw - 48px)" srcset="https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=200 200w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=228 228w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=260 260w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=296 296w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=338 338w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=385 385w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=439 439w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=500 500w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=571 571w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=650 650w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=741 741w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/KwuLNPefeDzUfR17EUtr.png?auto=format&amp;w=796 796w" width="398" height="300" /></figure><figure><img src="https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format" sizes="(min-width: 287px) 287px, calc(100vw - 48px)" srcset="https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=200 200w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=228 228w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=260 260w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=296 296w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=338 338w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=385 385w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=439 439w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=500 500w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=571 571w,     https://web-dev.imgix.net/image/tcFciHGuF3MxnTr1y5ue01OGLBn2/qed7yE6FKVQ5YXHn0TbJ.png?auto=format&amp;w=574 574w" width="287" height="300" /></figure>

## Remove motion on the web <a href="#remove-motion-on-the-web" class="w-headline-link">#</a>

[Media Queries Level 5](https://drafts.csswg.org/mediaqueries-5/) brings the reduced motion user preference to the web as well. Media queries allow authors to test and query values or features of the user agent or display device independent of the document being rendered. The media query [`prefers-reduced-motion`](https://drafts.csswg.org/mediaqueries-5/#prefers-reduced-motion) is used to detect if the user has set an operating system preference to minimize the amount of animation or motion it uses. It can take two possible values:

- `no-preference`: Indicates that the user has made no preference in the underlying operating system. This keyword value evaluates as `false` in the boolean context.
- `reduce`: Indicates that the user has set an operating system preference indicating that interfaces should minimize movement or animation, preferably to the point where all non-essential movement is removed.

## Working with the media query <a href="#working-with-the-media-query" class="w-headline-link">#</a>

See [Can I use prefers-reduced-motion media query?](https://caniuse.com/#feat=prefers-reduced-motion) to find out which browsers support `prefers-reduced-motion`.

As with all media queries, `prefers-reduced-motion` can be checked from a CSS context and from a JavaScript context.

To illustrate both, let's say I have an important sign-up button that I want the user to click. I could define an attention-catching "vibrate" animation, but as a good web citizen I will only play it for those users who are explicitly OK with animations, but not everyone else, which can be users who have opted out of animations, or users on browsers that don't understand the media query.

    /*
      If the user has expressed their preference for
      reduced motion, then don't use animations on buttons.
    */
    @media (prefers-reduced-motion: reduce) {
      button {
        animation: none;
      }
    }

    /*
      If the browser understands the media query and the user
      explicitly hasn't set a preference, then use animations on buttons.
    */
    @media (prefers-reduced-motion: no-preference) {
      button {
        /* `vibrate` keyframes are defined elsewhere */
        animation: vibrate 0.3s linear infinite both;
      }
    }

If you have a lot of animation-related CSS, you can spare your opted-out users from downloading it by outsourcing all animation-related CSS into a separate stylesheet that you only load conditionally via the `media` attribute on the `link` element 😎:

    <link rel="stylesheet" href="animations.css"
          media="(prefers-reduced-motion: no-preference)">

To illustrate how to work with `prefers-reduced-motion` with JavaScript, let's imagine I have defined a complex animation with the [Web Animations API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API). While CSS rules will be dynamically triggered by the browser when the user preference changes, for JavaScript animations I have to listen for changes myself, and then manually stop my potentially in-flight animations (or restart them if the user lets me):

    const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)');
    mediaQuery.addEventListener('change', () => {
      console.log(mediaQuery.media, mediaQuery.matches);
      // Stop JavaScript-based animations.
    });

Note that the parentheses around the actual media query are obligatory:

Don't

    window.matchMedia('prefers-reduced-motion: reduce')

Do

    window.matchMedia('(prefers-reduced-motion: reduce)')

## Demo <a href="#demo" class="w-headline-link">#</a>

I have created a little demo based on Rogério Vicente's amazing [🐈 HTTP status cats](https://http.cat/). First, take a moment to appreciate the joke, it's hilarious and I'll wait. Now that you're back, let me introduce the [demo](https://prefers-reduced-motion.glitch.me). When you scroll down, each HTTP status cat alternatingly appears from either the right or the left side. It's a buttery smooth 60 FPS animation, but as outlined above, some users may dislike it or even get motion sick by it, so the demo is programmed to respect `prefers-reduced-motion`. This even works dynamically, so users can change their preference on-the-fly, no reload required. If a user prefers reduced motion, the non-necessary reveal animations are gone, and just the regular scrolling motion is left. The screencast below shows the demo in action:

Video of the [`prefers-reduced-motion` demo](https://prefers-reduced-motion.glitch.me) app

## Conclusions <a href="#conclusions" class="w-headline-link">#</a>

Respecting user preferences is key for modern websites, and browsers are exposing more and more features to enable web developers to do so. Another launched example is [`prefers-color-scheme`](https://drafts.csswg.org/mediaqueries-5/#prefers-color-scheme), which detects if the user prefers a light or dark color scheme. You can read everything about `prefers-color-scheme` in my article [Hello Darkness, My Old Friend](/prefers-color-scheme) 🌒.

The CSS Working Group is currently standardizing more [user preference media queries](https://drafts.csswg.org/mediaqueries-5/#mf-user-preferences) like [`prefers-reduced-transparency`](https://drafts.csswg.org/mediaqueries-5/#prefers-reduced-transparency) (detects if the user prefers reduced transparency), [`prefers-contrast`](https://drafts.csswg.org/mediaqueries-5/#prefers-contrast) (detects if the user has requested the system to increase or decrease the amount of contrast between adjacent colors), and [`inverted-colors`](https://drafts.csswg.org/mediaqueries-5/#inverted) (detects if the user prefers inverted colors). 👀 Watch this space, we will definitely let you know once they launch in Chrome!

## (Bonus) Forcing reduced motion on all websites <a href="#(bonus)-forcing-reduced-motion-on-all-websites" class="w-headline-link">#</a>

Not every site will use `prefers-reduced-motion`, or maybe not significantly enough for your taste. If you, for whatever reason, want to stop motion on all websites, you actually can. One way to make this happen is to inject a stylesheet with the following CSS into every web page you visit. There are several [browser extensions](https://chrome.google.com/webstore/search/user%20stylesheets?_category=extensions) out there (use at your own risk!) that allow for this.

    @media (prefers-reduced-motion: reduce) {
      *, ::before, ::after {
        animation-delay: -1ms !important;
        animation-duration: 1ms !important;
        animation-iteration-count: 1 !important;
        background-attachment: initial !important;
        scroll-behavior: auto !important;
        transition-duration: 0s !important;
        transition-delay: 0s !important;
      }
    }

The way this works is that the CSS above overrides the durations of all animations and transitions to such a short time that they are not noticeable anymore. As some websites depend on an animation to be run in order to work correctly (maybe because a certain step depends on the firing of the [`animationend` event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/animationend_event)), the more radical `animation: none !important;` approach wouldn't work. Even the above hack is not guaranteed to succeed on all websites (for example, it can't stop motion that was initiated via the [Web Animations API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API)), so be sure to deactivate it when you notice breakage.

## Related Links <a href="#related-links" class="w-headline-link">#</a>

- Latest Editor's Draft of the [Media Queries Level 5](https://drafts.csswg.org/mediaqueries-5/#prefers-reduced-motion) spec.
- `prefers-reduced-motion` on [Chrome Platform Status](https://www.chromestatus.com/feature/5597964353404928).
- `prefers-reduced-motion` [Chromium bug](http://crbug.com/722548).
- Blink [Intent to Implement posting](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/NZ3c9d4ivA8/BIHFbOj6DAAJ).

## Acknowledgements <a href="#acknowledgements" class="w-headline-link">#</a>

Massive shout-out to [Stephen McGruer](https://github.com/stephenmcgruer) who has implemented `prefers-reduced-motion` in Chrome and—together with [Rob Dodson](https://twitter.com/rob_dodson)—has also reviewed this article. [Hero image](https://unsplash.com/photos/im7Tiw1OY7c) by Hannah Cauhepe on Unsplash.

<a href="/tags/media-queries/" class="w-chip">Media Queries</a> <a href="/tags/css/" class="w-chip">CSS</a>

<span class="w-mr--sm"> Last updated: Dec 10, 2019 </span> [Improve article](https://github.com/GoogleChrome/web.dev/blob/master/src/site/content/en/blog/prefers-reduced-motion/index.md)

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