# The Future of Front-End Performance (long-format)

- [Abstract](#abstract)
- [Prerequisites](#prerequisites)
- [About the trainer](#about-the-trainer)
- [Slides and controls](#slides-and-controls)
- [Resources](#resources)

## Abstract

Are you losing revenue to performance? 53% of mobile site visits are abandoned if a page takes longer than 3 seconds to load. Pinterest reduced load times by 40% and saw a 15% increase in sign ups. Starbucks implemented a 2x faster time to interactive resulting in a 65% increase in rewards registrations. AliExpress reduced load by 36% and saw a 10.5% increase in orders.

Performance is important. Tooling can be hard. Do flame charts intimidate you? Come learn about the various tools and metrics for measuring web application performance. We'll also deep-dive into the most common offenders so you can learn how to spot and fix them. During this talk, you will learn:

- The difference between lab/synthetic testing and field testing, or real user monitoring
- Which metrics matter and how they relate to user experience
- Latency and loading: HTTP2, code splitting, caching and service workers, resource and priority hints, progressive rendering and lazy loading, third party scripts
- Reducing code: tree shaking, responsible imports, performance budgets, differential serving
- Assets: responsive images, font loading, network client hints
- Perceived performance and UX

## Prerequisites

To get the most out of this talk, you should have a working understanding of JavaScript, HTML, and CSS. A basic understanding of webpack would be helpful but is not required.

## About the trainer

**Sia Karamalegos** is a web developer passionate about performance as well as an international conference speaker and writer. She is a Google Developer Expert in Web Technologies and a Women Techmakers ambassador. She co-organizes #FrontEndParty, GDG New Orleans, and NOLA Hack Night in the New Orleans area. She is the founder and lead developer for Clio + Calliope Web Development and was recognized in the Silicon Bayou 100, the 100 most influential and active people in tech and entrepreneurship in Louisiana. When she's not coding, speaking, or consulting, Sia likes to write stories and dabble in charcoal figure drawing. She's also an avid endurance athlete.

[Twitter](https://twitter.com/thegreengreek) | [Website](https://siakaramalegos.github.io/) | [Github](https://github.com/siakaramalegos) | [Blog](https://medium.com/@thegreengreek) | [StackOverflow](https://stackoverflow.com/users/5049215/sia?tab=profile) | [LinkedIn](https://www.linkedin.com/in/karamalegos)

## Slides and Controls

The slides are deployed [here](https://creative-narwhal-bf6c5f.netlify.app/#/). To advance the slides, use `n` for next and `p` for previous. The right arrow jumps to the next section (and left for previous section). Up and down to advance through slides within a section.

## Resources

Want to learn more about how to measure and improve performance? Here you go:

- [Modern DevTools course](https://moderndevtools.com/) by Umar Hansa
- [/dev tips](https://umaar.com/dev-tips/) by Umar Hansa
- [Optimize Website Speed with Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) by Kayce Basques
- [Assessing Loading Performance in Real Life with Navigation and Resource Timing](https://developers.google.com/web/fundamentals/performance/navigation-and-resource-timing/) by Jeremy Wagner
- [User Timing API ??? Measuring User Experience Performance](https://www.keycdn.com/blog/user-timing/) by Cody Arsenault
- [Measure Performance with the RAIL Model](https://developers.google.com/web/fundamentals/performance/rail) by Meggin Kearney, et. al.
- [Reduce JavaScript Payloads with Tree Shaking](https://developers.google.com/web/fundamentals/performance/optimizing-javascript/tree-shaking/) by Jeremy Wagner
- [Reduce JavaScript Payloads with Code Splitting](https://developers.google.com/web/fundamentals/performance/optimizing-javascript/code-splitting/) by Jeremy Wagner and Addy Osmani
- [Lazy Loading Images and Video](https://developers.google.com/web/fundamentals/performance/lazy-loading-guidance/images-and-video/) by Jeremy Wagner
- [The Cost of JavaScript in 2018](https://medium.com/@addyosmani/the-cost-of-javascript-in-2018-7d8950fbb5d4) by Addy Osmani
- [The Cost of JavaScript](https://medium.com/dev-channel/the-cost-of-javascript-84009f51e99e) by Addy Osmani
- [Why Web Developers Need to Care about Interactivity](https://philipwalton.com/articles/why-web-developers-need-to-care-about-interactivity/) by Philip Walton
- [Preload, Prefetch And Priorities in Chrome](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf) by Addy Osmani
- [Webpack build analysis](https://survivejs.com/webpack/optimizing/build-analysis/) on SurviveJS by Juho Veps??l??inen
- [https://www.webpagetest.org/easy](https://www.webpagetest.org/easy) easy no configuration set up for a slow-3G connection and mid-level phone, specifically Chrome on a Motorola G (gen 4) tested from Dulles, Virginia on a 400 Kbps 3G connection with 400ms of latency.
- [Responsive Images](https://developers.google.com/web/fundamentals/design-and-ux/responsive/images) by Pete LePage
- [Responsive Images Udacity Course](https://www.udacity.com/course/responsive-images--ud882) by Google
- [Optimizing Images](https://survivejs.com/webpack/loading/images/#optimizing-images) in Webpack on SurviveJS by Juho Veps??l??inen
- [Can You Afford It?: Real-world Web Performance Budgets](https://infrequently.org/2017/10/can-you-afford-it-real-world-web-performance-budgets/) by Alex Russell
- [Deploying ES2015+ Code in Production Today](https://philipwalton.com/articles/deploying-es2015-code-in-production-today/) by Philip Walton
- [HTTP Caching](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching) by Ilya Grigorik
- [Take a (Client) Hint!](https://www.youtube.com/watch?v=md7Ua82fPe4&list=PLe9psSNJBf75O6abYvvjxhm36_QU9H-f2&index=16) by Jeremy Wagner
- [To push, or not to push?! - The future of HTTP/2 server push](https://www.youtube.com/watch?v=ga_-zsTHRm8&list=PLe9psSNJBf75O6abYvvjxhm36_QU9H-f2&index=24) by Patrick Hamann
- [The Future is Fast](https://jlengstorf.github.io/presentations/the-future-is-fast/#/) on performance and Gatsby.js by Jason Lengstorf
- If you have the chance, attend one of [Harry Robert's talks or workshops](https://csswizardry.com/workshops/) on performance
- [Does my site need HTTPS?](https://doesmysiteneedhttps.com/)
- [Deploying ES2015+ Code in Production Today](https://philipwalton.com/articles/deploying-es2015-code-in-production-today/) by Philip Walton
- [Doing Differential Serving in 2019](https://calendar.perfplanet.com/2018/doing-differential-serving-in-2019/) by Jeremy Wagner and [repo](https://github.com/malchata/diff-serving)
- [Serve modern code to modern browsers for faster page loads](https://web.dev/fast/serve-modern-code-to-modern-browsers) by Houssein Djirdeh (and click through for codelab)

Other sources:

- [Speed is now a landing page factor for Google Search and Ads](https://developers.google.com/web/updates/2018/07/search-ads-speed) by Addy Osmani and Ilya Grigorik
- [WPO Stats](https://wpostats.com/) - Case studies and experiments demonstrating the impact of web performance optimization (WPO) on user experience and business metrics
- [Why performance matters](https://developers.google.com/web/fundamentals/performance/why-performance-matters/) by Jeremy Wagner
- [End to End Apps with Polymer (Polymer Summit 2017)](https://www.youtube.com/watch?v=0A-2BhEZiM4) talk by Kevin Schaaf which also shows the time to interactive video
- [This is why I prefer Progressive Rendering + Bootstrapping.](https://twitter.com/aerotwist/status/729712502943174657) tweet by Paul Lewis with graphic comparing progressing rendering with SSR and CSR
- [Why Waiting Is Torture](http://www.nytimes.com/2012/08/19/opinion/sunday/why-waiting-in-line-is-torture.html) by Alex Stone
- [The Truth About Download Time](https://articles.uie.com/download_time/) by Christine Perfetti
- [The need for mobile speed: How mobile latency impacts publisher revenue](https://www.doubleclickbygoogle.com/articles/mobile-speed-matters/) report by DoubleClick by Google
