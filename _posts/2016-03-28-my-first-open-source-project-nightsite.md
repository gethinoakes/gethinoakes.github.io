---
layout: post
title:  "My first open source project: NightSite"
date:   2016-03-28
tags: [Development]
desc: ""
keywords: "NightSite, GitHub, open source, flux, javascript, css, jquery"
---

Even though this is extremely simple, it's pretty exciting. My first open source 'project' on GitHub. I put project in single quotes because as I said it is extremely simple, and I'm unsure at this point if there's anything more I can add to it (although I do have some ideas, I'm not sure if they are achievable).

I wanted to make this site easier on the eyes for anyone visiting between the hours of 7pm and 7am. As this site is mainly white, my first thought was to create a dark theme that would be applied during those hours.

So I tried this, but I wasn't happy with the result. Then I remembered [Flux](https://justgetflux.com/){:target="_blank"}. Flux is great app that warms your computer screen at night and into early morning so that you're not staring at bright blue light.

So instead of having a dark theme that would modify several styles and add load, I implemented on simple style to add a low opacity orange overlay to the entire site and reduce some of the strain to the users eyes.

You can try it out here:

<button onclick="enableNightSite()" class="blue">Enable NightSite</button>
<button onclick="disableNightSite()" class="red">Disable NightSite</button>

I thought others might appreciate this, so I published it to [GitHub](https://github.com/gethinoakes/NightSite){:target="_blank"}.

<script>
var enableNightSite = function() {
    $('head').append('<link rel="stylesheet" type="text/css" href="{{ "/css/nightsite.css" | prepend: site.baseurl }}">');
}

var disableNightSite = function() {
    $('link[rel=stylesheet][href="/css/nightsite.css"]').remove();
}
</script>
