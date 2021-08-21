---
title: "August 2021 Status Update"
date: 2021-08-21T07:30:55-04:00
categories: [technology, etc]
tags: [status]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

Well I am still kicking and coding here.  I wanted to take a breath here and check in with progress.  Not that there is much of any. 😅😭

While I have been plugging some insane hours lately, I have recently been ambushed by the identity system.  It was basically like writing a whole new application.  What I have built, however, is pretty neat and I am happy with it.  Unfortunately, it has pushed my schedule out further, however, so I am trying to deal with the anxiety that goes along with it.

Outside of that, I have been spending the past week or so upgrading to .NET6 and Visual Studio 2022, which has been impressively stable, alongside [the new R# EAP](https://resharper-support.jetbrains.com/hc/en-us/articles/4404930135570).  Trying out the new environment has been remarkable and refreshing.  Access to new memory makes things much more fast and responsive and I no longer fight with the IDE (or wait for frustrating amounts of time) for the simplest of code changes.

While upgrading, I have also been taking time to upgrade parts of my framework that I am not exactly happy with, namely the EntityFramework portions.  Actually, I am very happy with what I have built, but unfortunately (to get technical) all of its components are designed to be scoped-per-user rather than as a singleton factory service.  That is, when a user creates a session with the application, it gets one `DbContext` to service them for that entire session.  This has its own set of problems, but the one I am focused on is memory utilization and state management.

To further illustrate the issue, with each `DbContext` created, there is also all the other components that go along with it, namely the `IQueryable` instances and components that are needed to pull all the data throughout the system.  Again for every session the user creates, each and every one of those components also get instantiated and stored per session along with that `DbContext`, adding to the memory utilization.

As such, switching to an `IDbContextFactory` pattern is recommended as there is one singleton factory and as many `DbContext`s can be made as per-unit-of-work and then disposed immediately.  This is a completely different way of doing business, however, and I am wrestling with the best way of moving forward with it,  currently.

This is technical debt in the most basic of terms.  However, it's really the only one I want to pick at with my codebase, which, at roughly 5,500 files at present is not a bad thing.

So that's a little of my world.  With all of the delays from upgrading and identity system, the alpha launch has been pushed back a bit.  We'll see if I can make up ground but February looks like a good spot now to have everything deployed, use, and documented.

Let's see how it goes. 🤞
