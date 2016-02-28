---
layout: post
title:  "Moving to Jekyll"
date:   2016-02-09
img: headers/jekyll.png
category: General, Development
tags: [jekyll, github, blog, wordpress, static]
---

Keeping in line with my apparent inability to stand still with this blog, I've decided to move it from [Wordpress](https://wordpress.org/){:target="_blank"} to [Jekyll](https://jekyllrb.com/){:target="_blank"}.

Wordpress is web software primarily used to create blogs, although it can pretty much power any type of website these days. Jekyll is a creation from the folks at Github, and it is meant as a tool to create static websites rather than rely on backend code and databases (which is one of the benefits).

## Why?
There are two main reasons for choosing to do this...

### Self Development
I've glanced at Jekyll before, and I was a little intimidated. Now I'm a bit more experienced I decided to take another look, and a better look at that. 

I wanted to develop my blog using Jekyll to improve my own knowledge and to learn a different type of development, and I'm quite happy with what I've discovered, even if I've only really just scratched the surface.

I plan to keep delving into Jekyll not to only improve my personal site but also to potentially use it for client sites, granted that they don't need a CMS to manage content themselves.

### Speed
As great as Wordpress is, it does come with a lot of dependencies that my blog simply doesn't need. Jekyll creates static content, almost as lightweight as it can get minus the loading of font awesome and google fonts.

I ran tests on my Wordpress blog and my new Jekyll blog using [GTMetrix](https://gtmetrix.com/){:target="_blank"} and [Pingdom](http://tools.pingdom.com/fpt/){:target="_blank"} which are both high up in the first 10 Google results when you search for 'Website Performance'.

- GTMetrix WordPress Test
![GTMetrix WordPress Test](/img/posts/performance_wordpress1.png)

- GTMetrix Jekyll Test
![GTMetrix Jekyll Test](/img/posts/performance_jekyll1.png)

- Pingdom WordPress Test
![Pingdom WordPress Test](/img/posts/performance_wordpress2.png)

- Pingdom WordPress Test
![Pingdom Jekyll Test](/img/posts/performance_jekyll2.png)

As you can see, the biggest difference after switching to Jekyll is page load time, shaving about 85% off the Wordpress page load time. Page size has increased from Wordpress to Jekyll as I had more posts on the Jekyll version compared to Wordpress at time of testing.

The number of requests has also decreased from 36/35 to 21, which also speeds things up.

## Where Now?
I still want to be involved with Wordpress development, developing some themes this year and I'll also have clients that Wordpress would make sense for, but for me Jekyll is the way forward.

I'm going to keep working on the performance of my blog, as it's an area of web development that I'd like to study and gain a greater understanding of. Also, I currently use a lot of large image files for post headers and on the home page too where posts are listed. These obviously put a big load on the server so I'm going to look into image compression to improve that or I might just get rid of the images all together... maybe yet another theme? I have a problem...

