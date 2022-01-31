---
title: "February 2022 Status Update"
date: 2022-01-29T13:40:16-05:00
categories: [business, technology, life, etc]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Welcome to the next installment of monthly starbeam.one updates.

### Playground Alpha Deployed to Azure

[In the last status update](https://blog.starbeam.one/2022/01/january-2022-status-update/), I mentioned that my focus for this month was getting the Playground Alpha [deployed to Azure](https://portal.azure.com/#home).  I am pleased to announce that this was accomplished after much configuration and trial+error (and much more error!).

The Playground Alpha is deployed and available for use, and will be made officially available later this month.  Before I do so, I am planning a marketing video tour (below), and once that is done, I will be making the official announcement (on the 22nd if all goes well).

### Azure DevOps

In addition to learning Azure and all of its challenges, I also integrated [Azure DevOps](https://dev.azure.com/) and have enabled continuous integration, or at least, a mild form of it.  Every code commit now creates a build that can further be deployed via release pipeline.  This is probably something that should have done from the outset, but I decided against doing so as it would incur hosting costs every month.  Seeing on how it took two years to get to this place, I am OK with that decision and tackling all this at once.

### Secured to Azure

But that's not all. :)  After getting both deployments and developer operations in place, I learned that the default configuration for Azure is "publicly available" which means it is not as secure as it could be, or at least for my tastes.  So, I took most of this past week to fix that issue, learning how to setup a private virtual network in Azure and get all the pieces talking to one another in this new configuration.

While this new configuration is more secure (in *theory* 😅) it also turns out to be more expensive.  This totally irks me, but is nonetheless the way things are done with the cloud and will have to accept it for now, hoping to generate enough revenue to pay for the hosting costs (and more as I discuss next).

### Gust Compliance

From Azure, I swung back around to my [Gust account](https://.gust.com/) and started to take care of some compliance issues, now that I have a deployed MVP and am a few months from starting to actually generate revenue.  

All I can say is, starting a business is expensive!  You have franchise fees, bookkeeping, taxes, and more.  This is definitely a different mode for me as my burn rate for the past several years of operation has been $5k/year (a business acquaintance affectionately calls me "Tiny Developer" per "[Tiny House](https://www.hgtv.com/shows/tiny-house-big-living)" franchising).  We are already looking at that amount with the compliance alone, yikes.

### Founders Hub

Finally, I put in an application for the new [Microsoft for Startups Founders Hub](https://startups.microsoft.com/).  I am really hoping to make the cut as there are Azure credits in the mix.  That would really help out with some of the costs that I am facing now.

### Time to Record

With all of that out of the way, it's time for the main event: recording my pretty face for the world to see.  This is two years of research and development for me, and I want to get my findings captured in these videos.  These videos are to be short and sweet, targeting about 3-4 minutes a piece.

I have two sets of videos in mind: one that outlines the publishing "system" I have based on [Kevin Kelly's 1,000 True Fans essay](https://kk.org/thetechnium/1000-true-fans/), and then an actual tour of the product where I record myself using the different parts of the application.

### Schedule

Believe it or not, there is at present no remaining formal schedule.  The videos are the final remaining task until the Playground Alpha announcement on the 22nd.  After that, it is onto the races for the actual alpha deployment which I originally scheduled for June but with all these costs I am sliding it to April.  

Let's just say a 🔥 has been lit under me, or a bigger one that was already there.  Once the videos are completed and the Playground Alpha announcement is made, I will then create a new schedule for this new phase.

That's it for this month's status update.  See you on the 22nd. 🤞✌✨
