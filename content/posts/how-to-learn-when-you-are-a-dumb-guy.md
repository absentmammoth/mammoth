---
title: "How to Learn a Dumb Guy"
date: 2020-04-06T23:34:50-06:00
lastmod: 2020-04-06T23:34:50-06:00
draft: true
tags:
- personal
- css
---

I have worked on this website for the last month and a half. Couldn't tell you why I started on it, initially, but building it has become a legit interest and I have learned so much along the way. It doesn't hurt that it's also been a distraction from the news.

<!--more-->

This uses the free static generator [Hugo](https://www.gohugo.io) and is hosted on a free Github repo. The URL, the name of a [Mount Eerie song](https://www.youtube.com/watch?v=VN9Fugvy7wI), cost me $12. For hours of use/cost, this project has been one of my wiser investments. 

Part of that is because I am not a smart guy, and I'm not a 'quick study.' Going into this, my knowledge of CSS and HTML was limited -- to say nothing of how little I knew about Hugo, Git, ssh, VS Code, and basic 'Does this site hurt to look at?' type stuff. Do I have my four year degree in all of this stuff now? Heck nah, but I'm confident I now understand just a little bit more than when I began. 

For my first post, I'd like to share how I taught myself about the tools I used to make this site. Hopefully there's something here of value to other dumb guys. 

### Pick the coolest-seeming middle of the road option

I was toying with the idea of getting a website going for the last few months. But every time I got close to biting the bullet, I thought, 'What would I put on a website?' Then I stumbled on the whole [IndieWeb](https://www.indieweb.org) scene and began reading articles on their wiki. At that point, it became clear to me that I could play around with making a site behind the scenes, rather than just stare at a hosted CMS's blank page wondering, What goes here? 

The Indie Web wiki gave my first set of choices:

1) I can repurpose an old laptop into an Ubuntu server and learn about making a website at the same time as learning how to run a server (dirt cheap, time consuming, potentially brain-damaging, no GUI hardmode)
2) I can use a free repository on a site like Github or Gitlab to host a website made with a static site generator, and having my own domain name would be optional (dirt cheap to free, time cost: unknown at point of decision)
3) I can buy a domain name and use a service like AWS to host the site (cost of a domain name, but free AWS for 12 months and least time consuming)

I started with option one. It fuckin' sucked. Yes, it feels cool as hell to sit in the terminal and enter strings you find through Google, trying to synthesize various forum posts into a coherent end result for the server.

LAMP stack? Sure, okay. Ubuntu comes with an Apache server, so you start out halfway done. But wait -- this post says to use Nginx instead of Apache. Should I? Darn, I already have the Apache server setup and MySQL is finally working... but okay, if I'm going to do this, I'm going to do it right, the way some random guy online said to. Well, hold on, I've completely removed Apache, right? Why won't Nginx work then? Did I just spend all that time messing with Composer to get MySQL working *for nothing*? Better wipe the harddrive and start over.

After a few nights of fun/extreme frustration with the server, I gave up and decided I would have to pick between options two and three. Option three seemed easiest, but also least 'cool' and most involved with Google and Amazon. And they're bad, right? So I went with option two, Github (Microsoft, like 2% less bad) and a static site generator. After a few days of playing around with the most Github-compatible generator, Jekyll, I decided to get my own domain name because absentmammoth.github.io is not cool.

>Step back: This first section is not about explaining any of the technical stuff I mostly failed to do during this part of the adventure. I am in no way equipped to talk about reverse proxies, all of the docs for using a Github pages Jekyll site are very clear, and there's no reason to talk about Vim now. This section is chronologically the start of the adventure, but it is the least important part and going forward I will be jumping around a lot.

In hindsight, the biggest takeaway here is that I maximized my fun quadrant by taking the middle of the road option. The server was *hard*. I figured out enough of the basics to have it work over the LAN, but I was terrified of opening ports, reverse proxies, etc. I didn't possess any of the underlying theory to understand most of what I was doing and it quickly became unfulfilling. The third option would use some of what I had learned with the first, but would generally be the least challenging, most expensive, and not particularly 'I own my data-y.' By process of elimination, I ended up where I am now: a private repository that hosts the site files, a public repository that hosts the outward-facing site, and a domain name of my choosing. I have decided not to use an additional service like Netlify to, theoretically, make managing site updates easier. Instead, I use a simple script, but that's getting ahead of things. The point is: Don't start with the hardest option -- not because it will make you feel dumb, but because the water is so deep you have to really love swimming in it to stick with the project. And don't pick the uncoolest option, because then you'll come to increasingly loathe what you're doing; no one likes doing something uncool.

A final note: Coolness is important, and how I made a lot of decisions relating to the site over the last few weeks. I picked Hugo because their community-made themes looked the best. It sounds superficial, but this kind of cool factor can signal some actually useful things:

1) The community has existed long enough to make decent looking stuff for itself, which means it likely has a good enough set of documentation and forum posts to get you where you're going
2) The generator itself is capable of doing cool things, which means it probably has some depth to it. Some static site generators I came across are very basic, which is great, but an aesthetic statement I take to have its own intention and meaning. As I have since found out, Hugo's depth is... it has been overwhelming to me.
3) Using something cool is exciting and gives you a little thrill when you use it. I have done almost all of the site development on a 2012 MBP -- a fuckin' cool laptop. It's ragged, dented, and showing its processor's age, but when I'm just starting to use it and the aluminum still feels cold... and when I hit the keys and they feel so responsive and loud... baby, that's cool. And it makes me happy. Hugo, git, using the terminal, etc. all feel fun to me, and that makes the process rewarding even when I am just noodling around or taking a step back.

### Organize what you take in, keep an eye out for theory

If you're a dumb guy like me, you're going to have spent as much time googling and reading often wrong forum posts as you will working on your project. This is act of succumbing to your ignorance -- sobbing, 'I yield!' -- and trying to find a stranger with the same problem as you, hoping against hope the stranger gets a working answer, is easily the least enjoyable part of all of this. You're going to read so much garbage. You're going to read stuff that doesn't work, either because it just doesn't work or because your configuration is different. You're going to read assholes telling the person with the question (basically, you), 'This is so basic. What are you, stupid or something? Is that your problem?' Yeah, man, it is. That's why I'm here. You're going to read reply after reply saying, 'Hmm, I don't have that problem. Bye!' You're going to see more 'foo bar baz' bullshit than you even knew was possible. You're going to have the same problem more than once, because you forgot you had it in the first place. And when you type the beginning of your question into google and it autocompletes, you will think, 'Oh no, which of these purple links has the right answer?'

There are a huge number of note-taking, bookmarking, organizational tools out there. I have experimented with many over the course of all this and settled on: [Pocket](https://www.getpocket.com) for saving webpages and a markdown app for saving notes. Markdown is fun to use -- *cool* compared to Word, but also much less of a headache -- and the files are easy to use wherever you want. MacOS/iOS/iPadOS's [Bear](https://bear.app) is the best-looking of the bunch and its tagging system is the most well-rounded for organizing content. It's a native app, which is fantastic. Obviously, with that said, there's no Windows version and the web app is still in development. My second choice here is [Notable](https://notable.md). Notable is quick for an Electron app and capable of more advanced markdown than Bear, but doesn't look quite as nice (mostly it's the icon; I cannot get over the icon) and, for the most part, you actually have to know markdown for it to be more useful than comparatively user-friendly apps/Word. For something more old-school, [iawriter](https://ia.net) is great. I won't talk about the couple days I thought emacs would be fun.

Take a lot of notes. Even if you never look at them again, it's okay. It just helps to have seen it, written it down, and be able to return to it easily if need be. One thing I've been doing more and more of: interactive notes. Instead of writing, 'x is a problem how I fix? will try later i guess,' I'm using little checkboxes to help me keep track of what I am doing and want to be doing. Here's an example from the to-do list I have for this site:

```
## Site To Do List

#### For sure:
- [ ] Clean up CSS, especially font-related, to reduce redundant/unnecessary lines
  - [x] additional-thanks-to scss
  - [x] media-list scss
- [x] Fix pagination arrows so that the number/word is always in the center of the arrows
```

Note-taking apps like Bear that allow you to link between notes are so helpful because they add this type of interactivity. It's not just tagging and folders at that point, but the wiki-style links that let you mention one note in another and keep track of things from there. 

Finally, if you're working on one thing, like building a website or trying to understand how to do something with git, file away anything theory-related that might be useful for later. It may not be something you're going to need now, but it'll color future encounters and decisions. For example, [here's a plainly worded and great set of concepts regarding git](https://sethrobertson.github.io/GitBestPractices/) that I found while trying to find something else, and I have retained much more of Git Best Practices than I have of whatever I was actually trying to find the answer to.

### Identify reliable sites to trawl and good types of advice-givers online

Google results have been terrible for me for ages. I cannot find what I want through Google. Either every result is the same thing from an interchangeable bunch of clickfarms or there are like two results in all of the e-archives for the question I have. So, I've learned I have to actually go to individual websites now, like back when I was 12, and use their search bars instead. Depending on what you're doing, you'll be seeing a lot of places like StackExchange, reddit, css-tricks, discourse.gohugo.io, some website with a guy's full name for the url (extra credible if he's not American/British), whatever. But you gotta use individual sites instead of Google now, which is a hassle, but also **The Way Things Used to Be**.

There are characteristics of more trustworthy advice-givers. One of the first things I found when reading the Indie Web wiki was Jamie Tanna's personal blog, [jvt.me](https://jvt.me). He has credentials, isn't a jerk, and using his site's search I was able to find some really informative posts about microformats and web development. This makes it easy to 'trust but verify.' That's one type of guy -- a known quantity. But most of the time, you're gonna be getting advice from non-entities who are saying whatever they want into a faceless user-generated content mill like reddit or StackExchange. My go-to 'I'll try this guy's advice first' sign is when he/she/they takes time at the beginning or end of the post to explain *why* you need to do what they're telling you to do. This is often more useful than the help itself, even, because it gives you another jumping off point for questions you may have later or are still battling somewhere else! Unfortunately, most of what you read online is going to be gibberish, not applicable to your problem, a solution that breaks something else, or wrong. When a post starts out with 'its easy' or indicates with the first sentence it is not actually going to answer the question at hand, just peace out.

And talk to your pals, too. 