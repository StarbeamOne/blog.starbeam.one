---
title: "June 2021 Status Update"
date: 2021-06-12T03:56:12-04:00
categories: [etc]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Well, alright.  [After all the commotion of last month](https://blog.starbeam.one/2021/05/startup-battlefield-2021-application/), I've been finding it quite difficult to settle down and get back into the development groove.  

What I find interesting is that my life is quite perfect right now for development (ala no emails, etc.), and even then it takes several days if not a full week to get me back in the zone for the 10-12 hour day slog.

Naturally, such a long time-to-focus process gives me a lot of concern for when things get "busy" (ala the email train) again.  However, I will cross that bridge when I get to it.

Although, I shouldn't say that.  Really [I am up against my good friend analysis lately](https://blog.starbeam.one/2020/11/analysis-is-the-most-difficult/), and that's really been my huge struggle point.  Whenever something takes a great deal of analysis, I find that it takes an inordinate amount of time to digest and process and get into a consistent flow.

What I keep focused on is that this is the last major analysis project before MVP.  Namely, user identification and authentication.  Up until now, I have had very basic identification and it has worked extremely well, because it's been so simple.  I have been using the [ASP.NET Core Identity SDK](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity-api-authorization?view=aspnetcore-5.0) which has been great.

Unfortunately, I have used it in a way that is constrictive, and that is you can only have one-identity-per-user.  It actually allows many identities (or logins) per user, but the way that I have used it doesn't allow for that, not without breaking a lot of my code.  I have known about this for a year -- it was a decision I made when I started starbeam.one, actually -- and I have struggled with keeping it as MVP approaches.  

I cannot see myself making a legitimate application with this design, so I have been busting out the walls and essentially re-writing the identity component for starbeam.one.

So this requires a tremendous amount of analysis and subsequent work.  All while being hustled by a deadline.  Gotta keep things moving, right?

However, I am making some progress and should be able to complete this by next month.  Identity touches a LOT of code if not all of it in some way, so it's been a challenge to grapple this and attending to all the ramifications.  Add to this the fact that this is one of the first areas I built for starbeam.one, you can probably imagine the emotional friction I encounter as I destroy some of what I love in hopes of improving it. 😅

From a design perspective, rather than having activities being attached to a user object, they are now being attached to an identification object which in turn references a user object.  Identifications are captured upon authentication with a provider.  Whereas before it was one provider (Twitter, MSFT, GOOG, PayPal) per user, now a user can have many providers and then select the one they want for an activity (sales, resales, etc.).

The tricky part is "linking" the providers that provide the identification.  After signing in, you can add/remove identity providers to your user (account).  This essentially links them to your user, creating an identity "chain."  However, if you sign out and sign back in with an identity provider that is not linked with a previous user, this creates a new user altogether.  At this point, we now have a problem, as you cannot add an identity provider to a user account that is already associated with another one.  In this case the user has created two by signing in with two different providers (rather than signing in with one, and then linking another).

To resolve this issue outright (before any further activity is performed on the provider identity), the creating user would have to add yet another provider to the new user account to "free" up the original login that created it, remove the original, and then add that original login provider to the first user account created.

More complicated than I would like, and I have been studying this problem for a while now to simplify and make it long-term viable.

Consider now that you have two user accounts, one of which was probably created by mistake as the user was not aware of how this all works (very very likely).  In order to link two users to make them back into one, you will have to "merge" them somehow (the one with the lower number wins).  This functionality does not exist with ASP.NET Core Identity SDK, and is something I will have to build at some point, although I am not sure yet if this will make it into the MVP because it will involve also adding 2FA for the user to verify/allow it.

As you can probably glean from the details, identity is *so so very difficult*.  It's no wonder so many applications and systems struggle with it.   But, if you do it right it can be extremely rewarding and beneficial, and become a feature point.  In my case, I do not want to saddle the user with yet another username/password (as a lot if not all of NFT platforms do), nor do I want to store another set of credentials in my database that can get hacked and be sold on the dark web.

Identity providers are ubiquitous and abundant.  Just look at [this comprehensive list that is supported by aspnetcontrib](https://github.com/aspnet-contrib/AspNet.Security.OAuth.Providers#providers).  They even [added Coinbase support](https://github.com/aspnet-contrib/AspNet.Security.OAuth.Providers/issues/544) for me (and because of this I will be supporting Coinbase in the MVP. ♥)!

Anyways, that should give you an idea of what I am working on now through July. [As I mentioned](https://blog.starbeam.one/2021/05/may-2021-status-update/), I am taking a bit of a break in July and then getting back into things full tilt to get the MVP ready by October 12th.

So the plan & schedule as it sits now is:

- **October 12th, 2021**: Primordial Alpha/MVP (friends/family)
- **February 2nd, 2022**: Private Alpha ([invites from signup list](https://starbeam.one/))
- **August 2nd, 2022**: Public Beta

Back to the grind. ✌
