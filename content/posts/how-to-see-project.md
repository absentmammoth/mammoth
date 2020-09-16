---
title: "How to See Through Fog: A Project"
date: 2020-09-09T21:09:05-06:00
lastmod: 2020-09-09T21:09:05-06:00
draft: true
description: "A series on nice things during a bad time, finding a project edition."
tags:
- fog series
- housekeeping
---

https://www.absentmammoth.org began in a much different form all the way back in January. Getting it to where it is today took dozens of hours and occupied most of my free time for several months. Making this website gave me something positive to focus on and has been a sick learning experience. I pushed myself more while working on it than I have with anything else in ages. I need a new project now, and I encourage everyone to find their own!

<!--more-->

In January, I got it into my head that self-hosting a server would be fun. 'Why not put Ubuntu Server on an old laptop. I'll make a little website on it and do some local network stuff with it, just to prove I can. And I'll do it all without a GUI, duh.' 

Everything I read about self-hosting made it sound easy. You just get your LAMP stack going and then you do a reverse proxy and throw Nextcloud and Ghost on it. Unfortunately, the fun of computers is that there is often more than one way to do things, which left me confused. LAMP stack... but then I learned about nginx. Do I use that or Apache? Why is composer not working out of the box for me? There are like a bazillion ways to setup a reverse proxy and I have no idea which one to do! Are they interchangeable? Actually, no! I reinstalled Ubuntu multiple times, because a clean slate was easier than trying to figure out whatever bullshit I had brought on myself. *But*, it wasn't all bad. I learned a bunch of terminal commands, the file structure of Linux, ssh keys, and... Vim (just kidding, I used nano). I also gained some insight into how I learn best. Still, setting up my own server became more of a headache than it seemed to be worth. Every time I would get Nextcloud working, going forward one step beyond would break it. Half the guides I found are for only one piece of the puzzle -- there are few all-in-one guides online that aren't either hundreds of pages long textbooks or software developer docs that only apply to their own software (and, duh, of course that would be the case). And, because of how Google works, clicking on a site's bad guide means you just get more bullshit from that site later when you try to find the solution to another problem.
 
So, I gave up after a few nights and many hours trying to figure all of this out.
 
Part of what pushed me to try self-hosting was [https://indieweb.org](https://indieweb.org). IndieWeb is not a huge community. It's a few dozen nerds very passionate about controlling their identities online. And, in looking around their community, it seemed like one difficulty level lower would be to use Github Pages to host a website made with a static site generator. The easiest generator to use with Pages is called Jekyll. But Jekyll's user-made themes just... look old, like they originated on Blogger. When I first looked at static site generators, I figured I would just use someone else's theme and maybe make a couple small changes if I felt like it. Trying to find a cool look for a site meant trying out *many* different static site generators. I settled on Hugo, because I saw Jamie Tanna's site [https://jvt.me](https://jvt.me) and thought it looked really good. It didn't hurt that Hugo is much simpler than something like Gatsby. (That said, my goofy digital garden placeholder @ [https://garden.absentmammoth.org](https://garden.absentmammoth.org) is made with Gatsby. However, I did not play around with Gatsby until I had my main site about where I wanted it, and I found it incredibly frustrating to work with as a novice.)
 
So, at this point, I've got something I think looks pretty and no idea what to do next. I didn't know how to use git (and even now I only understand the basics), how Hugo works or what it was even doing when it 'generated' a site, and what I remembered of CSS from my teens felt so dated when I would look at Jamie's site in vscode. It took me weeks of trial and error to even develop the language necessary to walk through what I wanted to do with the site in my head, not to mention how to verbalize the questions I had about git, CSS, and Hugo when prowling Google for help.
 
At this point, we're in early to mid-February. I was in the process of starting a new job after coming off of what felt like a humiliating job loss and eyeing news about the coronavirus, which looked awfully bleak. (And hey, wouldn't you know it...) But spending time on the website was fulfilling. I was learning things and able to see if not improvements, at least *changes* when adjust the site's HTML and CSS.
 
I have always enjoyed working with my hands and seeing the Fruits of My Labor, but I had somehow forgotten making something was even a thing you could do. Working on the site brought back the nostalgia of simple things like Lego blocks to building a barn and running fence for a horse pasture. Like, damn, you can just go out and make stuff? Wild. I always forget that I once put a new roof on a duck shed until I am making something else and remember, 'Oh yeah, that was fulfilling and I should make more stuff.' 
 
At some point, probably around mid-February, I became completely enthralled with working on the site. I understood enough about git and Github Pages that I could spend more of my time on the actual project. While I had initially planned to use Jamie's theme (he now has a new one and I am not going to dig through his Gitlab to find the old one right now), I came to realize it did *so much* that I both did not need or understand. The site I had taken from him included various possible copyright licenses on each post, a whole bunch of IndieWeb features I did not know what to do with, and html and css I did not know the purpose of. 

In my hubris, I thought I could just delete whole swaths of the site and anything I did happen to break would be easy enough to fix. Not so! It's not easy to fix something whose fundamentals you don't understand.

###### The Fundamentals of Hugo

Hugo renders markdown as html. This is simple. When I write a post called how-to-see-project.md (this one) and run the `hugo` command, this will turn into an html page on this website. What I did not understand at the time is... anything else about how Hugo works. The really important stuff, from a presentation perspective, is in the layouts folder. The layouts folder is like the giant felt board of your site and its files and subdirectories are like little pieces of felt you can stick on your site in different places. For example, [https://www.absentmammoth.org](https://www.absentmammoth.org) draws on the baseof.html, which says:

```css
<!DOCTYPE html>
<html lang='{{ .Site.LanguageCode | default "en" }}'>
    {{ partial "head.html" . }}
    <body>
        {{ partial "header.html" . }}
        {{ block "main" . }}{{ end }}
        {{ partial "footer.html" . }}
    </body>
</html>
 ```

The squiggly stuff is asking Hugo to grab the felt pieces (called 'partials') header.html and footer.html and place them at the top and bottom of the site, respectively. `{{ block "main" . }}` is the type of bullshit I just did not understand about Hugo for the longest time. In this case, `"main"` is a block defined in other html files and stands in for all the content on the main page that isn't in the header or footer. The ` . ` is an element in a range. If I remove it from the code, the site will not even load, because... no elements in the range.

(And, really, just about everything I learned in making this site came from 'removing a line of code and seeing what happens.')

These few lines are very simple, which is why I got so frustrated with Hugo again and again. It's very simple, period! But it has all these little intricacies that literally meant *nothing* to me going in. `{{ block "main" . }}` is a day at the beach compared to this total bullshit from head.html:

```css
{{- if .IsHome }}
	<meta name="description" content="{{ .Site.Params.Description }}">
		{{- else if .Description }}
	<meta name="description" content="{{ .Description }}">
{{- end }}

<title>
	{{- if .IsHome }}{{ .Site.Title }}{{- else }}{{ .Title }} &middot; {{ .Site.Title }}{{- end }}
</title>
```

Even now, I only vaguely understand what the various functions and variables being used here are saying. I have read through the docs multiple times and am still relying on context clues to piece together what's happening. 

I avoid Hugo's functions and variables as much as possible, but I had to get the basics to understand how to make the css and html changes I wanted.

Hugo's layouts folder makes managing the site's css and html easy, because you can play with one piece of felt at a time. For example, my [thank you page](https://www.absentmammoth.org/additional-thanks-to/) is a markdown file shaped by the additional-thanks-to.html file:

```css
{{ define "main" }}

<div class="credits-style">
    {{ partial "additional-thanks-to.html" . }}
        {{ .Content }}
</div>

{{ end }}
```

The div class here allows me to style the text 'this site is made possible with support from' on the additional-thanks-to page. That's it! The `{{ .Content }}` line is handled elsewhere, largely by the credits.scss file. credits.scss lets me put in all the fancy arrows and make other adjustments specific to this page, so that other parts of the site don't have to have the same rules. Some of that file can be seen below:

```css
.credits-style {
	> .creditsh2 {
		font: 500 1.6rem 'Vollkorn SC';
		text-align: center;
		font-variant-caps: all-small-caps;
	}

	> ul {
		list-style-type: none;
		sup:before {
			content: '[';
		}

		sup:after {
			content: ']';
		}

		sup {
			font: 100 0.7rem $header;
		}
	}

	> ul > li {
		margin-bottom: 0.4rem;
	}

	> ul > li:before {
		content: '\232A';
		vertical-align: text-top;
	}
}
```