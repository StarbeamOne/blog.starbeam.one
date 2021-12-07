---
title: "December 2021 Status Update"
date: 2021-12-05T06:13:09-05:00
categories: [business, technology, life]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Greetings and Happy Holidays.  Here is your next installment of starbeam.one monthly updates.

I feel the need to say this each time, but yes, I am still alive. 😊  I am also a bit late this time around, having skipped the November update.  Originally, I was aiming for the middle of November, but the final feature task that I was working on took way longer than I anticipated... *again*. 😅😭

With that, I took the few weeks to round out that final story and decided to round out to the next month, and here we are.  Going forward, I will aim for the first Tuesday of every month with an update.  So with that, let's get on with the show here.

#### Marketplace Application Feature Complete!

I am pleased to announce that after many *many* months of refactoring and delays with "perfection," the marketplace application is feature complete and ready for deployment.  [I know I know, I shouldn't be spending so much time being "perfect,"](https://www.amazon.com/37-Days-Launch-Ryan-Duques/dp/142765137X) but when I say "perfect" I really mean "doesn't obviously break."

In other words, it works on my machine and is ready for testing on another.

This last leg has been *especially* brutal.  In addition to a few fundamental [refactorings with the data access and a re-write of the identity system](https://blog.starbeam.one/2021/10/october-2021-status-update/), the last final feature was more involved than anticipated.  I had it pegged for 10 days and it ended up being 20.  To refresh, my days are 10-12 hours, no weekends, so it has been a slog.  I finished on December 2nd and have been attending to minor tasks since then, taking a "break" of sorts.

#### What's Next?

What a great question.  Two days ago I had one answer for you ("Primordial Alpha"), but now that I have had some time to think, I have another one ("Playground Alpha").  Let's explore.

#### Primordial Alpha

What is the Primordial Alpha?  Well, I've gone back and forth on exactly what this is.  Initially, I envisioned having a very well-secured application that is only accessible via Allowed List.  However, there are some "chicken-egg" challenges with doing so.

First is how do creators onboard their potential customers?  We have to Allow List them as well, and that becomes challenging.  Either I have to create a mechanism that enabled them to do so and/or they have to go through a process that may or may not be intuitive/rewarding/positive.

We're wanting a good first impression here.  Plus we're also wanting to see what breaks, which may be *everything*.

Hopefully we'll have everyone onboard that is long-term focused and sees the bigger picture despite the initial friction.

In addition to getting customers, there are other problems.  First is legal.  It's easier to have something deployed to show when I have lawyers look at something.  Sure, again, I could have sign-in/security mechanisms but historically I have never had much luck with them and end up being more trouble than its worth.

Also, those sign-in/security mechanisms are an issue of their own.  Authentication into starbeam.one is handled exclusively by Oauth2 providers, courtesy of ASP.NET Core's built-in security providers and the [aspnet-contrib package](https://github.com/aspnet-contrib/AspNet.Security.OAuth.Providers) (of which [I am a contributor](https://github.com/aspnet-contrib/AspNet.Security.OAuth.Providers/commit/014ef58416b9f6dca6ec88a4b7f4e5936ebb2acf#diff-97022d3ec3825bb5f18eb629bf5a25e0baf9db076c3ba296f13839061e7096c0)! 🎉).  Each one of those goes through a review process, and the review team requires access to the application to verify it conforms to their individual established policies.  Giving access to these teams has been a challenging riddle to me for some time.  Again, doing a security wall is challenging and there always seems to be a problem.  So what's the best way of providing access while getting approval?

Finally, there is the issue of onramp and exit ramps with fiat currency.  I am using PayPal for both, and Coinbase for onramping.  There is currently no exit ramp for Coinbase, and I am very irritated with that, [as Coinbase appears to have very little to no support for their development offerings](https://github.com/coinbase/coinbase-ios-sdk/issues/54).

So, I have been looking at [BitPay](https://bitpay.com/online-payments) instead.  They offer a promising solution, but it has revenue requirements.  Again, I would like to show them the working product and show them what I have in mind.

#### The Solution: The Playground Alpha

So what is the solution?  It wasn't until yesterday that I thought of something: why not simply deploy the application in all its (potentially broken 😁) operational glory with the exception of "live" deposit and withdrawal functionality?  Deposit and withdrawal will still be "available" but they will be "no-op," meaning they really do not do anything consequential.

To clarify further, the deposit will be a "faucet" where you can debit (fake/system-provided) money into your account, and the withdrawal will credit your account but will not actually send it anywhere.

So, everything *appears* to be working and is fully functional as deployed, but no actual "real" money will be utilized.

This way, the application can be viewed by all and I can start collecting all the valuable feedback immediately -- including and especially what breaks.  I can also start pointing dependent parties towards the location and having reviews done to further proceed with chicken-egg scenarios.

Boom.  I then anticipate a 2-3 month period where I tackle obvious problems while implementing BitPay/other on/off-ramps and get this to a deployable alpha where it can be used for real in a "live money" setting.

#### Schedule

All told, this is what I currently have in mind:

- **December 2021:** Playground Alpha Preparation
- **January 2022:** Deployment to Azure/Video Tour
- **February 2022:** Playground Alpha (No-op Deposit/Withdrawal)
- **April 2022:** Alpha (Live Deposit/Withdrawal)

Note that there is a chance that the schedule might accelerate, based on all sorts of conditions, primarily that of the quality of code and how well it reacts once under test.

And, of course, There is also a chance the schedule could slip.  I do not operate well under pressure. 🙃

But, we're getting closer here.  This is feeling more and more real every day and I am having to deal with the stress of such.  In a good way, I swear! 😅

That's it for this month's installment.  Until next time, stay bright. ✌✨
