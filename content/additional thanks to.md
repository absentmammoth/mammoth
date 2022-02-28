---
title: additional thanks to
date: 2020-02-25T20:01:24-07:00
lastmod: 2020-03-20T23:03:24-07:00
draft: false
layout: additional-thanks-to
---

* [Hank Ewbank](https://dribbble.com/hankewbank), for the cute lil shadow puppet mammoth display picture, as well as for showing me...
* Matthew Butterick's [practicaltypography.com](https://www.practicaltypography.com)[^1]
* Though I have rewritten the css from scratch, Jamie Tanna's [Hugo theme](https://gitlab.com/jamietanna/tale-hugo-jvt.me) was source of the original theme. Dissecting his site is how I learned almost everything I have used to write the actual css/html of Absent Mammoth. I still look at his newer site's code to better understand how Hugo works. It's great
* ⌃ click "Inspect Element"
* The [Hugo docs](https://gohugo.io/documentation/) (for the most part)
* Countless search results that led to various, occasionally contradictory, guides and examples that sometimes found their way into this site. Thank you, random guys on StackExchange and Medium. Some of you were helpful. Others of you could learn from some of you
* [IndieWeb.org](https://www.indieweb.org), which contains a significant amount of helpful information re: building your own website. (It's also how I found jvt.me in the first place!)
* The Wired article [How the Web Became Unreadable](https://www.wired.com/2016/10/how-the-web-became-unreadable/), which explains a misunderstanding surrounding contrast; the shift away from high contrast sites has caused developers to use harder to read font colors (e.g. grays in place of solid black[^2]) instead of dampening the harshness of bright white backgrounds[^3]
* Markdown
* Github (problematic)
* [RSCSS](https://rscss.io)
* The Boris album art below. I had played around with different purples and softer blacks until I saw it and all was clear to me. I didn't think I could get away with my `<a>` purple being quite that dark and also keep it from blending in with the default font color, but I did use a color picker and then fiddle with the hsl a bit to get it light enough. The art is by [Mami Saitou](https://mamisaitou.com)
![](/img/IMG_0072.jpeg)

[^1]:This site is exactly the kind of thing that I love -- clear, opinionated, and it explains the underlying theory and reasoning behind what he is advocating. While (because?) I am an absolute amateur, or less than, it helps me to have a resource like this to turn to. Even if it's completely wrong, it is at least complete! Worth the $9.
[^2]: These grays trade a problem with high contrast for one of not enough contrast. What seems to be more beneficial to readers is a non-white background, or a dimmer white, which I have experimented with on this site. The font is still a dark, DARK, purple (`$default-color: hsl(266, 1%, 29%);`), and the background barely indistguishable from white. But! I think that the soft purple and black makes the barely not-white seem less harsh.
[^3]: To quote from the article: 'To translate contrast, it uses a numerical model. If the text and background of a website are the same color, the ratio is 1:1. For black text on white background (or vice versa), the ratio is 21:1. The Initiative set 4.5:1 as the minimum ratio for clear type, while recommending a contrast of at least 7:1, to aid readers with impaired vision. The recommendation was designed as a suggested minimum contrast to designate the boundaries of legibility. Still, designers tend to treat it as as a starting point.' This is in contrast (sorry) to Butterick's approach: he says the only way to really design anything is to use your eyes and make tiny adjustments until something looks right. He may be wrong, but it makes sense to me.
