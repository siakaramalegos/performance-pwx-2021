---
theme: style.css
highlightTheme: github
revealOptions:
  transition: none
---

<!-- .slide: data-background="./images/hero_bg.jpg" -->
<h1 class="title dark-background"><span class="translucent">The Future of</span> Front-End Performance</h1>
<h2 class="subtitle">Sia Karamalegos</h2>

---

## hi, i'm sia

[sia.codes](https://sia.codes/)

<img src="./images/champagne_sia.jpg" alt="Sia dressed up as a champagne bottle at Mardi Gras" height="450px" class="no-outline">

---

## [bit.ly/perf-90](http://bit.ly/perf-90)

---

## Take out a piece of paper...

<img src="./images/Notes_caps.jpg" alt="Note paper with three columns of implement, research, or seek assistance" height="500px">

---

<!-- .slide: data-background="./images/elevator2.jpg" -->
<h1 class="dark-background">
  <span class="highlighter">Why do elevators have mirrors?</span>
</h1>

---

# Why Should I Care?

---

> Pinterest reduced load times by 40% and saw a 15% increase in sign ups.

<small>https://wpostats.com/</small>

---

> Starbucks implemented a 2x faster time to interactive resulting in a 65% increase in rewards registrations.

<small>[Chrome Dev Summit 2018](https://www.youtube.com/watch?v=Xryhxi45Q5M&t=1113s&index=6&list=PLNYkxOF6rcIDjlCx1PcphPpmf43aKOAdF )</small>

---

> AliExpress reduced load by 36% and saw a 10.5% increase in orders.

<small>https://wpostats.com/</small>

---

> Speed is now used as a ranking factor for mobile searches.

<small>https://developers.google.com/web/updates/2018/07/search-ads-speed</small>

Note: In 2016, Doubleclick by Google released a report saying that 53% of mobile sites are abandoned if pages take longer than 3 seconds to load.

---

<img src="./images/shame.png" alt="Message on slower sites to users saying 'Usually loads slow'" height="500px" style="border:none;box-shadow:none;">

<small>[Moving towards a faster web](https://blog.chromium.org/2019/11/moving-towards-faster-web.html)</small>

---

The internet consumes 416.2 TWh of electricity per year. A 10% savings would be equivalent to:

- 6.2 million fewer cars on the road 🚗 <!-- .element: class="fragment fade-in-then-semi-out" -->
- 32 billion less pounds of coal being burned 💨 <!-- .element: class="fragment fade-in-then-semi-out" -->
- 486 million tree seedlings grown for 10 years 🌳 <!-- .element: class="fragment fade-in-then-semi-out" -->

<small>[How is your website impacting the planet?](https://www.websitecarbon.com/), [Greenhouse Gas Equivalencies Calculator](https://www.epa.gov/energy/greenhouse-gas-equivalencies-calculator)</small>

Note: Most of the energy is consumed by the network and data center, not users' devices.

---

<h1 style="font-size:2.4em;"> 🧪 Test Environments 🧪 </h1>

---

## Testing Environments

<br>

<table class="fixed-two-column" id="invisible-gridlines">
  <thead>
    <tr>
      <th>Lab/Synthetic</th>
      <th>Field/Real User Monitoring (RUM)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <ul class="plus-minus" style="display:inline;">
          <li class="plus">Controlled environment</li>
          <li class="plus">Predefined network and device settings</li>
          <li class="plus">Reproducible for better performance debugging</li>
          <li class="minus">May not capture real-world bottlenecks</li>
        </ul>
      </td>
      <td>
        <ul class="plus-minus" style="display:inline;">
          <li class="plus">Performance data from <strong>real user page loads</strong> and interactions</li>
          <li class="minus">Limited data and performance debugging capability</li>
      </td>
    </tr>
  </tbody>
</table>

---

## New Lab Testing Tools/Features

- [Render-blocking JS and CSS flags](https://sia.codes/posts/render-blocking-resources/#how-do-i-test-my-website-for-render-blocking-resources%3F) in Webpagetest
- [Lighthouse Treemap](https://sia.codes/posts/lighthouse-treemap/)
- [Lighthouse user flows](https://web.dev/lighthouse-user-flows/)
- Chrome Dev Tools [recorder panel](https://developer.chrome.com/blog/new-in-devtools-97/#recorder) ([video](https://twitter.com/addyosmani/status/1465221489209319428))

---

## More focus on real user data

- [Web Vitals Report](https://web-vitals-report.web.app/) + [web-vitals npm package](https://github.com/GoogleChrome/web-vitals)
- Many analytics vendors ([Speedcurve](https://www.speedcurve.com/), [Calibre](https://calibreapp.com/))
- Starting to be bundled in more general analytics/deployment products like [Layer 0](https://www.layer0.co/performance-monitor)
- [Reporting API](https://developer.mozilla.org/en-US/docs/Web/API/Reporting_API)

---

# 📈 Metrics 📈

---

> When optimizing for speed, <br>**user experience** should always <br>be your primary metric.

---

## User experience

1. When can I see the page? <!-- .element: class="fragment fade-in-then-semi-out" -->
2. When can I interact with it? <!-- .element: class="fragment fade-in-then-semi-out" -->
3. Is it delightful? <!-- .element: class="fragment fade-in-then-semi-out" -->

---

## Core Web Vitals

<img src="./images/core_web_vitals.png" class="plain">

<small>[Web Vitals](https://web.dev/vitals/), [The Science Behind Web Vitals](https://blog.chromium.org/2020/05/the-science-behind-web-vitals.html)</small>

Note: Target is 75% of loads. "Core Web Vitals are the subset of Web Vitals that apply to all web pages, should be measured by all site owners, and will be surfaced across all Google tools. Each of the Core Web Vitals represents a distinct facet of the user experience, is measurable in the field, and reflects the real-world experience of a critical user-centric outcome." Note modifications over time to improve.

---

## New metrics under evaluation

*Provide feedback now!*

- [Smoothness/animation metric](https://web.dev/smoothness/)
- [Better responsiveness metric](https://web.dev/better-responsiveness-metric/)

---

<!-- .slide: data-background="./images/yellow-camera.jpg" -->
<h1 class="title" style="text-align:left;color: rgb(214, 61, 31);">Images</h1>

---

Images account for 45% of the bytes <br>on average needed to load a webpage.

<small>[httparchive.org](https://httparchive.org), October 2021</small>

Note: actually down from 50% - maybe due to increased use of lazy loading

---

<img src="./images/timeseries-of-image-byte.png" alt="HTTPArchive chart of image bytes transferred over time" style="border:none">

<small>[httparchive.org](https://httparchive.org), October 2021</small>

---

## kB by Percentile

<img src="./images/chart.svg" alt="" style="border:none">

<small>[httparchive.org](https://httparchive.org), October 2021</small>

---

<!-- .slide: data-background="./images/disk-drive.jpg" class="dark-highlighter" -->

# File Format <!-- .element: class="dark-background" style="color:#fecf16" -->

---

> Choosing the right image format... can be far more important than any flashy new “responsive image” technique.

<small>Mat Marquis, [Image Performance](https://abookapart.com/products/image-performance)</small>

Note: Responsive Issues Community Group (RICG) chair. Getting the right image format is more important than any responsive image technique.

---

## WEBP: Increased cross-browser availability

<img class="plain" src="./images/caniuse-webp.png" alt="caniuse page for webp showing not much safari support">

<small>[caniuse](https://caniuse.com/#feat=webp)</small>

Note: WEBP is a new format available on most modern browsers (I'm looking at you, Safari) that combines the best of JPG and PNG with smaller sizes. It's lossy or lossless and supports transparency.

---

## AVIF: The future

<img class="plain" src="./images/caniuse_avif.png" alt="caniuse page for avif showing limited support">

<small>[Equal file sizes demo](https://jakearchibald.com/2020/avif-has-landed/#at-equal-file-sizes) by Jake Archibald, [caniuse](https://caniuse.com/avif)</small>

Note: AVIF is an extraction from the keyframes of the now popular video format AV1. Best compression, supports transparency and more.

---

## JPEG XL: The way future

<img class="plain" src="./images/caniuse-jpegxl.png" alt="caniuse page for jpeg xl showing no support">

<small>[caniuse](https://caniuse.com/jpegxl)</small>

---

## Cheatsheet

- ✅ SVG: logos and icons <!-- .element: class="fragment fade-in-then-semi-out no-bullet" -->
- ❌ GIF: don't. use jpg for a still or video for animation. <!-- .element: class="fragment fade-in-then-semi-out no-bullet" -->
- ✅ PNG: photo-like images with transparency <!-- .element: class="fragment fade-in-then-semi-out no-bullet" -->
- ✅ JPG: photo-like images with no transparency <!-- .element: class="fragment fade-in-then-semi-out no-bullet" -->
- ✅ WEBP: smaller, but need to serve fallbacks <!-- .element: class="fragment fade-in-then-semi-out no-bullet" -->
- ✅ AVIF: EVEN SMALLER, but need to serve fallbacks <!-- .element: class="fragment fade-in-then-semi-out no-bullet" -->

<small>[Responsive Doggos Demo](https://projects.sia.codes/responsive-images-demo/)</small>

Note: Raster file formats are really just different compression methods. **SVG**: Can style and animate with CSS or make basic edits in XML. **GIF**: huge file sizes for animation, use video instead. svg or jpg are better for stills. Twitter converts GIF to video.  **PNG**: Use jpg if don't need transparency. **JPG**: much better compression algos.

---

# 📺 Size &amp; Resolution 📺

---

## `srcset` & `sizes`

```html
<img
  src="https://placekitten.com/300/200"
  srcset="
    https://placekitten.com/300/200 300w,
    https://placekitten.com/600/400 600w,
    https://placekitten.com/900/500 900w
  "
  sizes="(max-width: 320px) 280px,
         (max-width: 640px) 580px,
         1000px"
  alt="cute random kitten"
/>
```

---

<!-- .slide: data-background="./images/elder-phone.jpg" -->
<h1 style="text-align:right;">🤔</h1>

Note: How many different resolutions? Science suggests humans can see 720ppi 1 foot from a screen. The iPhone 11 is 326ppi (MBP is 227) so in most cases, you're safe providing only 1x and 2x. You might consider 4x in cases of high-resolution projectors or art.

---

<img src="./images/gov-uk-screen-data.jpeg" alt="Chart showing preponderance of 2x and 3x DPR for mobile and 1x for desktop" class="nooutline" width="55%">

<small><a href="https://twitter.com/TheRealNooshu/status/1397862141894529027">Tweet thread</a> with GOV.UK screen width and DPR data, <a href="https://jakearchibald.com/2021/serving-sharp-images-to-high-density-screens/">Halve the size of images by optimising for high density displays</a></small>

Note: Furthermore, nowadays most mobile screens are 2x and 3x so we can simplify by not providing 1x options at those screen sizes

---

## Bleeding-Edge File Formats

```html
<picture>
  <source type="image/avif" srcset="pug_life.avif" />
  <source type="image/webp" srcset="pug_life.webp" />
  <img src="pug_life.jpg" alt="pug wearing a striped t-shirt like a boss" />
</picture>
```

---

## `webp`, `srcset`, &amp; `sizes`, oh my!

```html
<picture>
  <source srcset="./images/sofa_pug_400.avif 400w,
                  ./images/sofa_pug_800.avif 800w"
          sizes="(max-width: 320px) 280px, 400px"
          type="image/avif" />
  <source srcset="./images/sofa_pug_400.webp 400w,
                  ./images/sofa_pug_800.webp 800w"
          sizes="(max-width: 320px) 280px, 400px"
          type="image/webp" />
  <img src="./images/sofa_pug_400.jpg"
        srcset="./images/sofa_pug_400.jpg 400w,
                ./images/sofa_pug_800.jpg 800w"
        sizes="(max-width: 320px) 280px, 400px"
        width="400px"
        alt="pug on a sofa looking sad" />
</picture>
```

---

## Paid Services 💰

For example, [Cloudinary](https://cloudinary.com/) supports AVIF, and you can optionally sign up for the beta to use it with `f_auto`.

```bash
[baseUrl]/eeeps/image/upload/f_auto,q_70,w_512/photo.jpg
```

<small>[What to know about AVIF on Cloudinary](https://sia.codes/posts/avif-on-cloudinary/)</small>

---

## More tools created & more packaged into popular frameworks for DX

- Simple `<img>` and server/serverless function selects best image to serve
- Build tools and integrated frameworks (but `sizes` not always supported)
  - [next/image](https://nextjs.org/docs/api-reference/next/image)
  - [responsive-loader](https://github.com/herrstucki/responsive-loader)
  - [gatsby-image](https://www.gatsbyjs.org/packages/gatsby-image/) and [gatsby-transformer-sharp](https://image-processing.gatsbyjs.org/)
  - [Eleventy image plugin](https://www.11ty.dev/docs/plugins/image/)


Note: (1) Many people have their server hijack the request and serve the best image to minimize markup. Could also use a serverless function. (2) Cost money. (3) So many options - both create your srcset code and process the images

---

<!-- .slide: data-background="./images/falling-mountains.jpg" class="dark-highlighter" -->

# Layout Shift

---

<video controls width="800" autoplay loop>
  <source src="./images/layout-shift.mp4" type="video/mp4">
  Sorry, your browser doesn't support embedded videos.
</video>

---

```html
<img
  src="/img/show-money/show-money.jpg"
  alt="Man's hand holding out a fist full of dollars toward the viewer"
  height="383"
  width="680"
/>
```

```css
img {
  height: auto;
  max-width: 100%;
}
```

<small>[Do This to Improve Image Loading on Your Website](https://www.youtube.com/watch?v=4-d_SoCHeWE&feature=youtu.be) - video by Jen Simmons</small>

Note: Setting the height and width on the image sets an aspect ratio, and then the CSS is respected.

---

<video controls width="800" autoplay loop>
  <source src="./images/fixed-layout-shift.mp4" type="video/mp4">
  Sorry, your browser doesn't support embedded videos.
</video>

---

## New aspect-ratio for beyond images

```css
aspect-ratio: 1 / 1;
aspect-ratio: 16 / 9;
aspect-ratio: 0.5;
```

<img src="./images/caniuse-aspect-ratio.png" alt="Can I Use shows high implementation of aspect ratio across modern browsers" width="80%" class="no-outline">

<small>[caniuse](https://caniuse.com/aspect-ratio), [Setting Height And Width On Images Is Important Again](https://www.smashingmagazine.com/2020/03/setting-height-width-images-important-again/#fixing-the-resizing-problem)</small>

---

## ⚡🦄🌈⚡ Native lazy-loading ⚡🦄🌈⚡

```html
<!-- Lazy-load offscreen image when user scrolls near -->
<img src="./hotlanta.jpg" loading="lazy" alt="...">

<!-- Load an image immediately -->
<img src="./hotlanta.jpg" loading="eager" alt="...">
```

<small>[addyosmani.com/blog/lazy-loading/](https://addyosmani.com/blog/lazy-loading/)</small>

---

# ⚡🦄🐈🌈🐼🍕🎂🍾🎉🐶🦄🐈🌈🐼🍕🎂🍾🎉🐶⚡🐈🌈🐼🍕🎂🍾🎉🐶⚡🦄🌈🐼🍕🎂🍾🎉🐶⚡🦄🐈

---

## Finally coming to Safari Tech Preview!

<img src="./images/caniuse-loading.png" alt="Can I Use shows 60.9% compatibility with loading attr" width="80%" class="no-outline">

<small>[caniuse](https://caniuse.com/loading-lazy-attr)</small>

Note: It's getting closer! Last time I checked, it was around 60%

---

# ⌚ Latency ⌚

---


> Bandwidth is the width of the tube and latency is its length.

<small>[A brief guide to using WebpageTest](https://davidea.st/articles/a-brief-guide-to-webpagetest)</small>

---

For large or content-heavy sites like Netflix, bandwidth is critical. For everyone else, it's the **latency**.

---

<iframe src="https://player.vimeo.com/video/14439742" width="640" height="480" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<small><a href="https://vimeo.com/14439742">Packet Flight: HTTP request @ 40X</a> from <a href="https://vimeo.com/carlosb">Carlos Bueno</a> on <a href="https://vimeo.com">Vimeo</a>. [TCP congestion control](https://en.wikipedia.org/wiki/TCP_congestion_control)</small>

---

<img class="plain" src="./images/tcp-slow-start.webp">

<small>[What Is TCP Slow Start](https://www.keycdn.com/support/tcp-slow-start)</small>


---

## 103 Early Hints

> 103s are served to clients while a 200 OK (or error) response is being prepared (the so-called “server think time”), and contain hints on which assets will likely be needed to fully render the web page.

<small>[Early Hints: How Cloudflare Can Improve Website Load Times by 30%](https://blog.cloudflare.com/early-hints/), [Chrome Status: Feature: 103 Early Hints for Navigation](https://www.chromestatus.com/feature/5207422375297024)</small>


Note: "the page load could have been accelerated had the browser known, prior to receiving the full response, that the stylesheet and the four subsequent scripts will be needed to render the page. Early Hints avoids these issues by “hinting” (vs. push being dictatorial) to clients which assets they should load, allowing them to prioritize resource loads with more complete information about what they will likely need to render a page, what they have cached, and other heuristics."

---

<img class="plain" src="./images/Early-hints-diagram-1.png">

---

## Priority Hints

```html
<!-- Manage in-viewport priorities -->
<img src="lcp-image.jpg" importance="high">
<img src="/images/in_viewport_but_not_important.svg" importance="low">
<ul class="carousel">
  <img src="img/carousel-1.jpg" importance="high">
  <img src="img/carousel-2.jpg" importance="low">
  <img src="img/carousel-3.jpg" importance="low">
  <img src="img/carousel-4.jpg" importance="low">
</ul>

<!-- Initiate an early fetch for a resource, but also deprioritize it -->
<link rel="preload" href="/js/script.js" as="script" importance="low">
```

<small>[Optimizing resource loading with Priority Hints](https://web.dev/priority-hints/)</small>

---

"18% of global Android Chrome users have Lite Mode enabled (aka Save-Data)"

<img src="./images/save-data-usage.jpg" alt="" style="border:none">

<small>https://twitter.com/colinbendell/status/1265675813204172810</small>

Note: true numbers higher https://twitter.com/addyosmani/status/1265677876608655361

---

## `prefers-reduced-data`...<br> is still experimental

<img src="./images/caniuse-reduced-data.png" alt="Can I Use shows no compatibility with prefers reduced data" width="80%" class="no-outline">

<small>[caniuse](https://caniuse.com/mdn-css_at-rules_media_prefers-reduced-data)</small>

---

<!-- .slide: data-background="./images/AA-font.jpg" -->

---

## FOUT

<video autoplay loop>
  <source src="./images/fout.mp4" type="video/mp4">
  Oops, video not supported
</video>

---

> The style doesn’t matter so much, it’s that it has to flow the same way.

— Tim Brown, Twitter

---

## Font Style-Matcher by Monica Dinculescu

[meowni.ca/font-style-matcher/](https://meowni.ca/font-style-matcher/)

---

## Enter CSS font descriptors

```css
@font-face {
  font-family: 'Lato';
  src: url('/static/fonts/Lato.woff2') format('woff2');
  font-weight: 400;
}

@font-face {
    font-family: "Lato-fallback";
    size-adjust: 97.38%;
    ascent-override: 99%;
    src: local("Arial");
}

h1 {
    font-family: Lato, Lato-fallback, sans-serif;
}
```

<small>[A New Way To Reduce Font Loading Impact: CSS Font Descriptors](https://www.smashingmagazine.com/2021/05/reduce-font-loading-impact-css-descriptors/), [Automatic Font Matching](https://deploy-preview-15--upbeat-shirley-608546.netlify.app/perfect-ish-font-fallback/?font=Montserrat). caniuse: [size-adjust](https://caniuse.com/mdn-css_at-rules_font-face_size-adjust), [ascent-override](https://caniuse.com/mdn-css_at-rules_font-face_ascent-override), [descent-override](https://caniuse.com/mdn-css_at-rules_font-face_descent-override), [line-gap-override](https://caniuse.com/mdn-css_at-rules_font-face_line-gap-override)</small>

---

<img class="no-outline" src="./images/Jimmie-Durhan-Installation.jpeg" alt="Sculpture of a boulder crushing a car with words crudely pasted over - JS is in large letters over the boulder and 'user just wanting to read a blog post' is in smaller letters over the car'" width="80%">

<small>Original art by [Jimmie Durhan](https://hirshhorn.si.edu/explore/jimmie-durham-still-life-spirit-xitle/), please forgive the meme I created over it</small>

---

## New trends for managing 3rd parties

<img class="no-outline" src="./images/tweet-third-parties.png" alt="Third-party JavaScript can have a heavy impact on page load performance. *When* you load such scripts can make a big difference (e.g. during idle time vs. asap). To help, we built a Script Component for Next.js: http://bit.ly/nextscript. Any feedback on it is welcome." width="50%">

<small>https://twitter.com/addyosmani/status/1467033429988429826</small>

---

<!-- .slide: data-background="./images/baggage_claim.jpg" -->
<h1 class="dark-background">
  <span class="highlighter">Houston's Baggage Claim Complaints</span>
</h1>

<small>http://www.nytimes.com/2012/08/19/opinion/sunday/why-waiting-in-line-is-torture.html</small>

Note: “Often the psychology of queuing is more important than the statistics of the wait itself,” notes the M.I.T. operations researcher Richard Larson. Occupied time (walking to baggage claim) feels shorter than unoccupied time (standing at the carousel).

---

> Are you better off making the site load faster or ensuring that users complete their tasks?

<small>Christine Perfetti, [The Truth About Download Time](https://articles.uie.com/download_time/) 2006</small>

---

<!-- .slide: data-background="./images/hero_bg.jpg" -->
<h1 class="title dark-background">Thanks!</h1>
Slides, resources, and more at <a href="https://bit.ly/siaspeaks" class="dark-background">bit.ly/siaspeaks</a>

