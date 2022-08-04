---
title: "August 2022 Status Update"
date: 2022-08-04T07:42:32-04:00
categories: [business, technology, life]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Welcome!  It's the first Tuesday of every month, and that means the latest starbeam.one Status Update!  Let's begin here.

### Program Notes

Astute readers will realize that I am posting this on a Thursday, and not a Tuesday.  While I was able to record the latest Stand-up & Shine (and Shill) on Tuesday, [I was not able to post it until this morning](https://youtu.be/aJ0wyH5B2Nk).  There were a few issues with post-video production that took quite a bit of time and retakes.  Turns out video processing is very intensive when you apply certain filters to it, and there were a lot of retakes involved in making sure the sensitive information I was providing during the demonstrations were adequately scrubbed.

This is what I get for running live demonstrations in the production environment!

Past that, there were also a few issues/bugs unveiled during recording the demonstrations.  I took some time to get these addressed, deployed, and ready for the world to see.

With that, let's move into the good stuff.

### Announcing the Friends & Family  Alpha... Twitter Edition™

Back in June [I announced the Friends & Family alpha](https://blog.starbeam.one/2022/06/june-2022-status-update/), and then immediately spent the next two weeks fixing bugs discovered during said announcement and subsequent recording.  It was a bit of a bummer, and I never got to announce it on Twitter, where I feel you have to really have your [ducks in a row](https://www.btb.termiumplus.gc.ca/tpv2guides/guides/wrtps/index-eng.html?lang=eng&lettr=indx_catlog_i&page=9vF-dOfBT0jI.html#:~:text=To%20get%20your%20ducks%20in,the%20origin%20of%20this%20expression.) when you put something "out there."

There was also the slight detail that I was accepting monetary value without an efficient way of viewing and managing it if necessary.  Yes, I can see everything using Sql Server, but that is a bit informal (and error-prone) for my tastes).  

I needed to flesh out my already half-developed Administration Application to get it to a place where I could feel a little more comfortable accepting (and managing) funds.  What if someone asked for a refund?  I didn't even have a policy in place, let alone the ability to quickly provide one.

So after fixing bugs, I spent more time on the Administration Application and getting core features in place to feel a little more in control of this baby that I have birthed (I am sure that parents will be quick to tell you that you are never in control, however!).

Let's discuss some key features now in place with the latest alpha version.

### Administration Application

As mentioned, starbeam.one now features an Administration Application that administrators (read: me :)) can use to view and administer certain aspects of the system.  If a process fails, for instance, it can easily be restarted.  User accounts can also be disabled, if needed (hopefully this will not be needed any time soon, of course!), and other such tasks.

But more importantly, it introduces workflow processes such as approval/rejection for features such as withdrawals and/or refunds.  Speaking of which...

### Refunds!

starbeam.one now features self-managed refunds for purchases made with PayPal and Stripe ([Coinbase is on the way next](https://forums.coinbasecloud.dev/t/refunds-for-coinbase-commerce-beta/1014)).  Refunds can be made with unspent credits within 30 days of purchase.  Please read the [refund policy for full details](https://alpha.starbeam.one/policies/refunds).

### (Coinbase) Withdrawals!

In addition to making withdrawals from PayPal, starbeam.one now allows you to do the same via your Coinbase Retail account.  That means not only one but *two* ways of receiving value from your starbeam.one account when you deem appropriate.  This not only provides options for users of the system, but also redundancy in case one of the off ramps go down for any reason.

Note that restrictions are in place with withdrawals while the system is under test and confidence is gained with this functionality.  Please see the [withdrawals policy for the details](https://alpha.starbeam.one/policies/withdrawals).

### Stand-up & Shine (& Shill)

So many new features!  So much amaze!  I am super happy with where things are now as opposed to June.  The horse feels put in front of the cart now and I start talking about this project in earnest on Twitter (and more).

If you are interested in watching me talk for 40 minutes+ about these features while also showing them off, you should check out the latest version of Stand-up & Shine (& Shill) which can be seen below:

<iframe width="560" height="315" src="https://www.youtube.com/embed/aJ0wyH5B2Nk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="margin-bottom: 2em"></iframe>

### Thank you!

A quick shout out to all the support and appreciation that you all continue to show out there.  [starbeam.one's YouTube Channel](https://www.youtube.com/channel/UCe06CeIw3-YUqiXLQZMbiSA/) now features 15 subscribers. This which may not seem a lot, but it is a tremendous accomplishment to me as I didn't think I was going to get even one. :)  I very much appreciate all the support in any form it arrives.

Until next time, stay bright! ✨
