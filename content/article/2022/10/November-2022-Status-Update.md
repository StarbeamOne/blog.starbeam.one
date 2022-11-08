---
title: "November 2022 Status Update"
date: 2022-11-08T06:05:21-05:00
categories: [business, technology, life, etc]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Welcome to the *second* Tuesday of the month, which means we're way overdue for a monthly status update!

### A Week Off

It is indeed the second Tuesday of the month.  I usually aim for the first Tuesday, but I have recently been running into troubles with my recording software [and they have been thankfully resolved](https://twitter.com/StarbeamOne/status/1588566148349501440).  So today we are back on track, recording today and again in two weeks from now on the 22nd.  Thankfully November is a 5-week month and I was able to slide up the 3 week interval to the front of the month.

From here on, it should be back to business as usual. 🙏🤞

### Alpha II Is Underway

I've really been spending a lot of time implementing features of the publishing system.  We've had a lot of artists join up and a lot of feedback has arisen as such.  There's a story capturing all the tasks here:

https://github.com/StarbeamOne/home/issues/2

This morning, I deployed the storefront cover adjustment which allows artists to update the storefront cover after deployment.  This seems like a "duh" in hindsight but as I created the system 3 years ago it was all meant to be immutable like the blockchain (and actual real-life publishing at that).  That is, if you published a record album/CD cover and it had a mistake in it, well that mistake gets sent out (or you have to redo it).

Since then, I have cooled on this idea and it's back to your typical web application where if you made a mistake or want to change something, you can do this.  Hence, this feature (and general direction).

### Up Next: More Artist Features + Improvements

There are two outstanding tasks from this story: issuance recalls and purchase recognitions.

1. **Recall issuances**: In the case of new artists especially, we want to provide a way of being able to recall (destroy) and issuance, allow the artist to modify/correct it, and then re-issue.
2. **Purchase Recognition**.  This is the final task but it's also a bigger one as it introduces a CRM (customer relationship management) into the system.  Basically, when a purchase is made, [we want to provide the artist with the opportunity to thank the purchaser](https://github.com/StarbeamOne/home/issues/6).  Since I have access to all the information at present, I have been personally thanking each and every purchase that has occurred on the system (and will continue to do so until this feature is complete! 😁).  However, once this feature is done, artists will be passed on the baton to thank purchasers directly.

### Up Further: What's Next?

Really, we're focusing on artist improvements at the moment.  Once that is done I want to work on [improving how the StarVault collection is displayed](https://github.com/StarbeamOne/home/issues/1) to the user (as well as products on the front page).  

Finally, after that, I want to introduce [the concept of publishing streams](https://github.com/StarbeamOne/home/issues/27) which will formally delineate between AI (daily) art and traditional (weekly/monthly) art, as well as introduce this cool concept we're calling treasure streams. 💎✨

Then after that, it is time for The Broadcaster which I feel is the last remaining component of starbeam.one to reach beta level.  [The Broadcaster is the marketing coolness](https://github.com/StarbeamOne/home/issues/17) which will help gain some more awareness and activity with our system, and help forward traffic to existing artist storefronts.

### Stand-up & Shine

That's it for this month's update.  More can be seen below with our latest Stand-up & Shine:

<iframe width="560" height="315" src="https://www.youtube.com/embed/BKBoJ4_DGkg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="margin-bottom: 2em"></iframe>

Until next time, stay bright out there. ✨✌
