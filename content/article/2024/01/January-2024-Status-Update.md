---
title: "January 2024 Status Update"
date: 2024-01-03T04:54:21-05:00
categories: [business, technology, etc]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

It's the first week of the month, it is time for a monthly status update! 🚀

### Happy New Year 🎉

Happy New Year out there to all!  I hope this new year finds you healthy and that 2024 will be a prosperous year for us all. 🙏👍

### Microsoft for Startups Level 4

I am happy to announce that we have been accepted into the fourth and final level of the Microsoft for Startups program.  This means another year of benefits and most importantly Azure credits.  As Azure hosting is by far and away our greatest cost at the moment this will help us stay afloat for the next year.

And yes this means we have one more year to find a way to generate enough revenue to pay the bills.  The pressure is on. 😬

### Solution + Azure Improvements

I have been preparing for vNext of our favorite publishing starship.  Part of that work can also benefit our existing version, so I have been adjusting accordingly.  Mostly, this involves simplifying the solution to make it easier to work with the code and all its deployed applications.  It also means reducing the amount of said applications which are ultimately deployed to Azure.

Along those lines, I am also wanting to get our environments templated so that it's easier to deploy our environments and test them without much hassle.  As it stands, when I add a new component I have to modify four different environments (development, testing, staging, and production) to get this incorporated and it is a lot of work, not to mention error-prone.

Additionally, when onboarding a new developer they will also be able to standup their own dedicated environment via a template.

Getting everything templated will make all of this much, much easier.  It will also reduce costs with testing, as it means we will only have an environment deployed for when we need it, rather than having it deployed 24/7 as it is now.  Further, it will also mean we will have an environment that can copy/use production data from a previous point in time which will improve testing.  Currently we have a staging environment but it uses it's own database and the amount of data in it pales in comparison with what is in production.  Using a template, we could deploy a testing environment, copy previous production data, and test with that, thereby improving confidence in the code being tested.

### Stand-up & Shine (& Shill)

That does it for this month's update.  For more information around our current state of our starship, I direct you to the latest Stand-up & Shine (& Shill):

<iframe width="560" height="315" src="https://www.youtube.com/embed/O0fitpFn7Xg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="margin-bottom: 2em"></iframe>
