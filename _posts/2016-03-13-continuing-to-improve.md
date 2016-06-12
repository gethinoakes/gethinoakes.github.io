---
layout: post
title:  "Continuing to Improve"
date:   2016-03-13
tags: [development]
desc: "Optimizing Jekyll and decreasing page size by 98% and decreased the amount of HTTP requests by 13"
keywords: "jekyll, image optimisation, page size, page speed, page load, wordpress, GTMetrix, Pingdom, WebPageTest"
---

Just under a month ago I moved my blog from using Wordpress to Jekyll and described how in doing so I vastly increased the speed of my website, cutting about 85% off the page load time and decreasing server requests.

I still wasn't happy though, mainly because my page size was was still massive at around 6mb. This is because I was using a large image file for each post, as well as on the home page where each post was listed resulting in a maximum of 10 high-res images having to be loaded to list 10 posts per page.

Not only that, the design wasn't as clean as I'd hoped it would be. There was far too much going on, and also not that it's a big issue but I didn't want to worry about searching for an image relative to the post any longer.

And so, I've refreshed this blog once again! I seem to spend more time doing that than I do actual blogging - I'll try to work on that. I've gone for a super clean and minimilistic look and simplified the styling overall, especially the css using just 3 colours (if you don't include black).

And with these changes, I've again drastically increased speed 😃 You can see the comparisons below, but the result is that I decreased page size by 98%(!!!) and decreased the amount of HTTP requests by 13. I'm very happy with that. I think I've caught the 'optimization' bug though... 😂

## GTMetrix

### V1
![GTMetrix Jekyll Test](/assets/img/posts/performance_jekyll1.png)

### V2
![GTMetrix Jekyll Test v2](/assets/img/posts/v2-gtmetrix.png)

## Pingdom

### V1
![Pingdom Jekyll Test](/assets/img/posts/performance_jekyll2.png)

### V2
![Pingdom Jekyll Test v2](/assets/img/posts/v2-pingdom.png)

## WebPageTest

### V1
![WebPageTest v1](/assets/img/posts/v1-webpagetest.png)

### V2
![WebPageTest v2](/assets/img/posts/v2-webpagetest.png)

## Pretty graphs
![pagesize](/assets/img/posts/v2-pagesize.png)
![pageload](/assets/img/posts/v2-pageload.png)
![pagespeed](/assets/img/posts/v2-pagespeed.png)
