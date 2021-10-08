---
title: "October 2021 Status Update"
date: 2021-10-08T03:50:07-04:00
categories: [technology, etc]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Goodness, has it been two months already?  I have been in a total coding slog since the last checkin, having to battle two coding fronts that address technical debt concerns:

- Identity System (95% complete)
- Entity Framework Data Access Refactor (65% complete)

The Entity Framework story is a bit further along than it suggests.  Part of the issue is that currently all worker processes run in session scope, which makes sense.  I am not too keen on rocking the boat there.  The major task for this story was to get `DbContext`s and all their related components to be singleton in the gateway marketplace ("web app") application.

For all intents and purposes, this is complete.  The only sections that remain are the resales and withdrawals.  I should have that done in the next week.

I am super happy with the data access story now.  So, worth it?  It took about 6 weeks along with the identity system.  But, everything is now net6.0 and feels so much better.  There is no longer that nagging sensation that I will "have to get around to it someday."

Besides that, it's a mad rush here.  I am still circling February for some sort of announcement.  It'll be a close shave at this point, however.  I will have to get those marketing videos done after the announcement.  Also, there is one other refactor story hidden in here and that is the distributions.  They need to be improved.

Here's the current breakdown of remaining major stories.

- **October:** Entity Framework/Identity System/Distributions
- **November:** Distributions/Administration
- **December:** Administration application (for running things behind the scenes)
- **January:** Deployments to Azure
- **February:** MVP Primordial Alpha Announcement 
