---
title: "December 2023 Status Update"
date: 2023-12-05T06:01:43-05:00
categories: [business, life, etc]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Hello to all out there, and I hope this finds your holiday season well. 🦌⛄🎅❄

It's the first Tuesday of the month, it is time for a monthly status update! 🚀

### Welcome to Beta III

I am very happy to announce that today we have [Beta III](https://starbeam.one).  This is mostly a quality release, addressing a lot of issues for administration and user account management.

### It's v1 -- Sorta 🎉

With this monthly update, I am going to take some time here and reflect where we are here after four years of development, with (at present) another year of runway to make something of it in a viable way.

### The Good

To start, I am beyond proud of what I have built thus far.  Comprised of 170,000 lines of C#, 48,000 lines of Razor, and only 150 (yes! you read that right -- 150) lines of custom JavaScript, this is by far and away the best freaking thing I have ever developed in my life *without question*.

What I am most enamored with is quality.  Usually when my codebases evolve they turn into a pool of buggy disaster (should I admit this? 🤣💥).  However, with this one, I landed on a style circa 2017 that has only been refined since.  It is based on a combination of C# and F# concepts + principles and has worked really well with both the approach, structure, and maintenance of this system.

For a little additional technical context, there are 12,508 C# files in my solution, *which means the average file has ~13.5 lines of code in it*.  That means opening a typical file has 13-14 lines in it, which implies each file does very little, which further means there is very little that can go wrong in it. 🤞

This is unlike a lot of C# projects you see out there, where typical files have 100s if not 1000s of lines of code in them.  As you can probably imagine that means a lot of surface area per file where something can (and will) go wrong with them.

Additionally, it should go without saying that I have been able to develop a system exactly how I would like to do so, and the results of which are pretty great and meaningful to me.  At the time of writing, [we have processed nearly $10,000 of sales + resales of digitally owned products in a completely centralized manner](https://starbeam.one/dashboard).  I wanted to prove that this could be done, and feel this has been accomplished.  Those $10,000 of volume are comprised of 6,145 sales which means 6,145 times that something could have gone wrong but didn't.

Further, we are able to accept payments and pay people out, all via trusted 3rd party providers like Coinbase and PayPal.   All of this is hosted on Azure which also has its own tremendous learning curve (which painfully still goes on today).  This is all new territory for me and I feel that it has been accomplished in a viable manner.  The code is very stable and works consistently well, and for the most part, I want to call it v1.  

However, before doing so, [there are some considerations](https://twitter.com/Mike_E_angelo/status/1731616441281958062).

### The Bad

Even at v1 quality, everything is unicorns and rainbows here.  Despite having built something that I am super proud of, along with it being functional and stable, it is ultimately missing the mark for long-term viability (read: profitability).

To start, what I started out to build was a publishing system, and while what we have does do this in a sense, what it ultimately has created is a centralized version of an NFT-marketplace, which is not what I wanted to build.

At its heart, what I wanted to build initially was a system where artists sell their products to many people at lower price points, i.e., *lower prices at higher quantities*.  NFTs are the inverse of this with *higher price points at lower quantity*.

How did we get here?  We actually were pretty close to what I wanted to achieve a year ago.  We were selling products at $.25 a piece per day and while it worked for some, other artists wanted higher price points more like NFTs.  I should have stuck to my guns but relented (as I was curious too how we could fare).

The world does not need another NFT marketplace, even if that NFT marketplace is not an NFT marketplace and is a centralized equivalent.  However, all is not lost with the effort for the past year.  In addition to improving fundamental pieces of the system, I was able to closely analyze the system we suddenly found ourselves competing against.  

In particular I started tracking and analyzing a few "successful" NFT accounts, and IMO they are not all that.  It turns out that the NFT experience is inefficient and requires a lot of energy and maintenance.  People will take interest and purchase for a while, but after long, unless you have an extensive network (many do not), collectors lose interest.  Even artists who do have an extensive network + following suffer from this, going many days or even weeks without a sale.

On top of this, it turns out that an overwhelming amount of activity is from artists purchasing from other artists.  This is neither viable nor successful, as money is basically recycled back in the system, passed back and forth between artists and only benefitting the network in the form of fees.

Finally, it is worth noting that the typical "successful" NFT artist will only have a handful of collectors purchasing from them -- a dozen at the very most.  It is very rare to see anything above this, and this does not really signal a large+growing market to me.

On the collector side, there is this small problems of limits.  People only have so much money, and at higher price points, they quickly exhaust their budget and resulting interest + participation.

All of this has me calling back to the original heart and soul of starbeam.one: *higher quantity and lower prices*.

### The Next:  Beta IV & Subscriptions

I have a year left of runway, and now I have to prove that I can make enough money with what I built that can at least pay the bills.  How will I do this?  Subscriptions.  However, this term is an approximation and I continue to search for a better word that best describe the process, which I will describe below.

Essentially, what we want is a simple (that does exist, right? 😏) way to commit a monthly amount to an artist, say $10/mo.  This is roughly $.33/day taken over 365 days of the year ($10x12/365).  We want to return to the process we had a year ago where an artist can supply one (*and only one*) image per day, and allow collectors to subscribe to this channel via an ideal 1-click method, thereby securing payment on a monthly-ish basis in a *low-cost, low-risk, and low-effort* sort of a way.

As an artist produces a work, it is automatically purchased by any existing subscribers, and available for any others that want to join (work can also be purchased one-off for a higher price point).  As a subscriber pays for that day's work, their $10 commitment is gradually reduced and then topped off again when it goes below a certain threshold (e.g. $1).  If an artist does not produce for a day, no money is paid by the collector.

In my view, this is a much more efficient model.  I also feel this is a better price point for AI in particular where the ability to produce art is so easy and plentiful, and truly lends itself to daily art.  Additionally, by restraining the channel to one-and-only-one image per day, we art-(😏)-ificially place scarcity on the product, improving its value.

To end, having a committed daily cycle not only improves efficiency, but engagement.  Now we have a daily reason to contact collectors, and provide them with upsell of the existing markets (higher price points) to purchase.

In all, I hope this will get us on our way to profitability.  I have a few more ideas around this to help get us there, but they will have to wait until next update. ✌

I hope to have subscription channels (aka "commitments" or "allotments" -- still kicking these around) by Beta IV, slated for February 6th.

### Stand-up & Shine (& Shill)

That does it for this month's update.  For more information around our current state of our starship, I direct you to the latest Stand-up & Shine (& Shill):

<iframe width="560" height="315" src="https://www.youtube.com/embed/dLh5S1DcNFg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="margin-bottom: 2em"></iframe>
