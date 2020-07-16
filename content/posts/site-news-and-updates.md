---
title: 'site changes & updates'
date: 2020-07-15T22:11:00-06:00
draft: false
tags:
- housekeeping
---

I have made additions and adjustments to the site in a few places. Why?! Well,

<!--more-->

The changes, and some whys:

- I have adjusted what was once the 'Media List' page. It is now the 'Link List' page! Before, my goal was to have a Media List page that I would update regularly with links to whatever, then archive at the end of the month. In hindsight, this does not make sense because this site is for me, and I see now that I am not going to either bother with or gain from doing that. (And if it was for other people, it would be an even worse idea.) So, I now have what I want to keep as an endless scroll of links (the 'Link List'), which I  will add to over time. When I make updates to this list, I will add the date of the most recent links.
- I have changed my h-card job description in the site footer. I was, at one point, a copywriter. No more! I am now a kind of *consultant*? I don't want or care to get into the specifics of my work, but it is there, for now, in case I decide to make more use of my h-card.
- I fixed a social medial profile link that was out of date.
- I fixed old css that was scaling images poorly, which is why [Hank's](https://dribbble.com/hankewbank) site icon may have looked wobbly or egg-shaped in the past. Sorry! 
- A while back, I added a 'garden' page to the site header. This page runs off Gatsby, rather than Hugo, and was a pain to configure. I will fix the bright green link font. If you click '<a href="https://garden.absentmammoth.org">garden</a>', you can learn more about its purpose. (This is a much longer term project. I regret that I don't have more time to give it right now.)
- I noticed that my prior implementation of the site's css for tags in the post meta areas allowed the grids the tag sections belonged to to become out of sync in some situations. I have implemented a (maybe temporary) solution, which is to change them from `justify-self: end` to `justify-self: stretch` with some `margin-left` action to prevent them from crowding the post titles and timestamps. I may need to make further tweaks here if I ever end up using an unusually long tag, or if I ever make use of the (currently hidden) table of contents display I have designed.
- I added a 'now' tag to the <a href="/now">/now</a> page. I'm trying to decide how I want to handle this page -- should I delete outdated parts of it, have it on a long scroll like the Link Lists page, or create an archive for past updates? Another option might be to release an outdated /now page into the entire pool of posts. This probably makes the most sense, as it will put the out of date /now page in its chronological rightful place in the list of posts and a new /now page can take its place. 

If you like having fun, you can always [go to the site's repo](https://github.com/absentmammoth/absentmammoth.github.io) and see what's changed with your own two (give or take) eyeballs. This page should also show the site readme, containing past and planned changes.

### What's next?

Anyone with a website will tell you they wish they used it more. (A fact I have made up.) That's true for me. I have a few drafts sitting around in my `content` folder that I have not gotten around to fleshing out. They're both bigger projects that I want to feel happy with when I am done.