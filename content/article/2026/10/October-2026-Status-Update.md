---
title: "October 2026 Status Update"
date: 2026-10-30T00:00:00-04:00
categories: [business, life, etc]
tags: [v2]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: true
---

### Welcome Back?

Wow —yes, hello there, everyone. I am still alive and very much kicking -- and screaming? -- here on our favorite starship starbeam.one.  You could say we had some issues in 2024 -- both financial and technical -- that sidelined blog activity, and it never got settled until now.  Truth be told, blogging is a bit... antiquated?  [I have been doing daily updates on X for over two years now](https://x.com/Mike_E_angelo), starting in September of 2024.  So, if you'd like to keep up to the very latest, that is probably the way to do so.

Nonetheless, now that the technical issues have been resolved, along with a worthy impetus to write a long-form post, I thought it would be a good idea to brush off the dust here and catch everyone up to date.

### What's Going On Now?

The last we heard, I was working on the New Publishing Wizard for the v2 rewrite.  Oh, yes, we also had a v2 rewrite.  Sort of like finishing an entire pint of gourmet ice cream, it didn't start that way, but it sure did end up that way.  

July 2024 was also when a very real problem struck me: after nearly 5 years of living off savings and Pandemic Unemployment Assistance, I was running out of money, and starbeam.one wasn't really making any.  That meant I had to find an investor or another way to finance our operations.  I spent about 3 months investigating options and landing some potential opportunities, but nothing really clicked.

Thankfully, after some time, I found part-time work with another startup, and that is how I have managed to keep the lights on during this time. 🙏

All the while, I have been working on it, and after 2.5+ years since the first commit on March 24th, 2024, I am oh so very happy to say we have a new version available for starbeam.one. 🥳✨🚀

Yes, 2.5 years of full-time and part-time effort to finally produce a version we can deploy and our users can use.  All the while, I fretted about money and whether it was all worth it.  I will not lie: there were times I wanted to quit—I actually considered it twice, one of those very seriously—but I somehow persevered and got the chance to share this announcement with you.

### Welcome to starbeam.one v2

[We're here.  v2](https://starbeam.one).  Well, it may not look radically different outside a few color changes, but the underlying code and model are so, so, so much better.  I could spend two years on this post alone talking about all the ways we have improved the starbeam.one marketplace, but I'll keep it to high-level points to maximize time and efficiency.

#### v1 Challenges

Before I get into the new, shiny parts of v2, it might help to contrast them with v1's challenges.

Did I mention I ran out of money in 2024?  Yeah, oops!  In hindsight, I feel v1 was the science fair experiment in a local competition that could: I wanted to build something, and I wanted to be ambitious, but I didn't know exactly what that was and how it would make money.  Also, because of my previous startup experience, I assumed/hoped/dreamed that somewhere, somehow, someway, we would land an investor and they would know how to make the money—it is their money, after all, right?  Well, I am glad we did not land said investor in hindsight because with all of the stress of the v2 rewrite I could not possibly, conceivably add the chore of having to explain my decisions to someone who was paying me to do so in the hopes of having some sort of return at some point.

They would have essentially poured their entire budget into me spending 2+ years rewriting an application. 💥  So, in hindsight and for the long term, better me than them.

Beyond not making much money, the huge oversight with v1 was that the only revenue stream I accounted for—pulling a % from every sale—was woefully insufficient to pay the bills.  This oversight was founded on a faulty assumption that a community of collectors -- much like our elusive unicorn investor -- would somehow find their way to our marketplace and continuously purchase products and feed money into the system.

This never happened.

#### Revenue Streams, Let Me Count the Ways

You can say that I had an overzealous fixation on revenue streams for v2.  We have not one but six of them for v2.  Whereas v1 focused on collectors who never showed (doh), v2 focuses on the artists who use it every day.  Additionally, I am happy to say my hatred of charging a monthly subscription fee continues, so all of these streams remain transaction-based, supporting the vision of *ownership, not rent*.

##### Data Hosting

Probably the biggest addition to our publishing process is that we now charge for data hosting and subsequent serving of files.  Whereas all products were 100% free in v1 for artists to publish, this is again a good way for the business hosting that content to become poor fast.  sb1 charges $0.05 per MB, which is intended to host the content for a "lifetime" (100 years) while also paying for data transfer during that time.  Yes, our service provider (Microsoft Azure) charges us to host data *and to transfer it whenever it leaves storage*.  $0.05 might not even be enough to cover those costs, but based on my estimations, it's a good first stab going forward, and certainly better than the bleeding we have had to endure to this point.  We are currently responsible for 100GB of v1 data with zero payments, so that's a consideration, too.  I would rather overestimate a charge and dial back than undercharge and increase rates later.

##### Network Gratuity

This is a carryover from the lone revenue stream of v1.  Whereas v1 charged a % of the transaction value, we now charge an (*optional*) fixed recommended gratuity of $0.15 per transaction.  Additionally, whereas we only charged network gratuities for sales and resales for v1, v2 now asks for a network gratuity on the following transactions:

- Issuances
- Sales
- Resales
- Listings
- Transfers -- yes, we have transfers now!
- Withdrawals

##### Network Gratuity Accounts

Building on the concept of network gratuity, when a new issuance is being produced by our New Publishing Wizard, we add starbeam.one as a beneficiary with an *optional* 3%, meaning 3% of any sales and resales of the product go to starbeam.one directly.  Again, optional is emphasized as this account can be reduced (or increased if you so wish! 🙏) or removed altogether.

##### Extra Licenses

For v1, we did not charge for licenses. For v2, we are now charging for licenses made after the first for all issuances.  The first license of every product issuance is free; each additional one is $0.25. 

##### Command Tokens

Another artist feature introduced in v2 -- and one that I am very proud of -- is the ability to generate images from Azure AI for product content within the New Publishing Wizard.  Covers, Backgrounds, and even the Featured Image of an Image product can all be generated by Azure AI using the GPT Image 1.5 model.  Each image generated costs 1 "Command Token," and each account gets 10 Command Tokens for free to try out the features.  After this, it's $0.05 for each Command Token, or 20 for $1.  Command Tokens will be used for any future AI-involved features.

##### Announcement Bot

Finally, a late and final addition made was yet another service made for free in v1: our valued Announcement Bot.  This is another feature I am proud of, and it's been upgraded for v2.  For v1, all major events in our application were broadcast to the following social media channels:

- Facebook
- Instagram
- Pinterest
- LinkedIn
- Discord
- X (Twitter)

That last one is a stickler and a point of contention, but it was the driving force here in making our Announcement Bot a revenue stream.  X started charging for their posts.  First, they started at $0.01 per post (yay), but then "slyly" [started charging $0.20 shortly thereafter for all posts with a URL](https://devcommunity.x.com/t/concern-about-url-posting-cost/264451) (boo).  I could get by paying $0.01, but not $0.20.  What to do?  Well, pass the cost onto the customer while adding a bit of margin for our bills, of course.  Yes, a good exercise in upgrading a science fair experiment to an actual business. ✌️

### Features

Well, it's not all about money, of course, but we are building a business, and that's what it takes.  The other half is providing value to the customers of said business, and v2 has plenty of these.  Let's go through them now with a proper introduction.

#### New Publishing Wizard

<img src="https://i.imgur.com/IE3xvzP.png" style="zoom:50%;" />

By far and away the biggest feature of v2 is the New Publishing Wizard.  It completely destroys the ... wonky?  yes, *wonky* ... publishing system of v1, where it involved creating a definition followed by creating an issuance of the definition.

Both of those concepts still exist in v2, but it's much more streamlined and optimized for the user.  The New Publishing Wizard is a wizard of 6 major steps, carefully guiding the user through all the important parts of publishing a product:

- Content: Provide -- or generate! -- files used in your product; the topic/sub-topic (theme) is also defined here
- Describe: Words and descriptions used to give detail on what is being sold
- Method: Storefront properties and options to best sell your product.  You can even send your products as a gift to other sb1 users
- Beneficiaries: Carrying over from v1, define who gets a % of your proceeds from sales and resales
- Review: A page devoted to seeing how your product will look both as a storefront and final purchased product
- Pay: The important part, right?  A checkout page showing how much is due to finalize the order 

I estimate that about 50% of the time over the past 2.5 years was spent on the New Publishing Wizard, either in initial design or in the identified defects arising from it.  I am incredibly proud of the final result and hope others enjoy its improved experience over the v1 counterpart.

##### Generated Images

![](https://i.imgur.com/KhxwAR7.png)

You can now generate images during the content definition step.  Yes, this goes for the featured image as well if you select it as such.  Covers and Backgrounds, too.  All are generated via Azure AI and the Chat GPT Image 1.5 model.  Each generation costs 1 Command Token and every account gets 10 of them free to try.  Additional Command Tokens are available for purchase at 20 for $1.

##### Preview Images

![](https://i.imgur.com/m49Lwv6.png)

Another major feature here that I am very proud of, as well as relieved, due to how much trouble we have had with properly solving this issue.  As you may know, starbeam.one is completely different from other marketplaces, where we protect content and source files from public viewing by default.  You cannot view the source files until you purchase the product.  This is a marked difference from NFTs, where it's public by default, so you don't even need to purchase to possess the content that is being sold.  Seems like a design defect, doesn't it?  

Not here.  We protect that content and ensure that only someone who purchases your product can access source files.  Turns out, doing this is way more complicated than you might think.  For starters, how exactly do you protect these images, and how do you do this for non-image files like text files and PDFs?  Sure, you can watermark the files (also non-trivial), but you still need to protect the content and only provide a *preview* of the file, without exposing the entire file for free download on the internet.

I'm proud to say we have finally addressed this satisfactorily in v2.  For each product type, we do the following:

- Image: Easiest one; slap a watermark over it and cap its dimensions
- Video: Take a customizable snapshot at a particular time in the video, slap a watermark over it upon completion
- Text/Markdown File: Take a customizable screenshot of the file via [Puppeteer](https://pptr.dev/)
- PDF: Same as text file, use Puppeteer to take a customizable screenshot
- Audio File: This is the odd one out as it cannot be translated visually.  However, we aggressively prompt and suggest the user to create/generate a cover to serve as the visual representation

##### Signatures

But that's not all!  We've also added signatures.  You can now apply signatures to "scopes" (discussed next), which will feature the signature under all products created under them.  Signatures are completely customizable in position and padding, and can differ between source and preview:

![](https://i.imgur.com/l2lBmPp.png)

#### Topics and Sub-topics, Global Scope

Moving on from the New Publishing Wizard, we have introduced the notion of Topics, Sub-topics, and a Global "scope" that can be used to define common features and properties for all products described under them.  Global is used everywhere, and can be overridden by topics and sub-topic. Topics and sub-topics can be used to organize your content.  Each can be viewed as a "template" for properties to save time without having to constantly re-type them each and every time you publish a product.

#### Content Tagging

You can now define tags for your product to help with searching.  Yes, we have searching now and that is discussed a bit below.

#### Storefronts (Public and Private)

In v1 we have the ability to create a resale listing as private or public. Product storefronts were not able to do this, but they are now in v2!  You can now create a private storefront so that only those you share the link with can see it.

#### Transfers and Gifting

You can now transfer a license directly to another user in starbeam.one.  Similarly, for publishing a product, you can gift a license directly to another user as well as producing additional licenses for sale.  For instance, you can produce 3 licenses, and gift 1 while publishing the other two, or publishing 1 while gifting they other two, or any variation of this.

#### Searching + Filtering

![](https://i.imgur.com/rmuvkjR.png)

We now have a consistent search and filtering experience across all catalogs in our application.  Type a search term, and it will search artist name, product name, product tags, and descriptions to find results.  You can also filter on product file type and content flags.

#### Restricted Market

You might have noticed that we now feature a Restricted market for PG-13 material.  This is for non-general market material such as political content or tasteful nudity.  We have to abide by payment processor policies, and we cannot publish anything more explicit than this.  In the next version of starbeam.one, we will feature AI-assisted content categorization to help with this process.

#### Streamlined Account Transfer Process + Automatic Transfers

Moving on to more ancillary features, we have streamlined the account transfer process, which was a little involved in v1.  Now transferring value from accounts to your primary account for spending and withdrawals is much more streamlined, often involving one press of a button.  Additionally, for purchases, we now prompt the user for automatic transfers, and it all happens seamlessly with a progress indicator showing what is happening.  As a result, the user never leaves the purchase screen, and everything is handled inline without much friction.

#### Ordering System

This is more of a non-user experience, but we completely rewrote the ordering system.  For v1, we only had sales and resales.  Now, in v2, we have a much more robust ordering system that can be customized for any number of products sold.  For instance, for v2, we added Data Hosting, Command Tokens, and Announcement Bot promotions.  Each one of these has its own SKU in the ordering system, along with several others.  Going forward, we can easily add additional products/SKUs for purchase and sale in the system.

#### Framework Improvements

Finally, massive work and improvements have been done on [the underlying open-source framework](https://github.com/dragonspark/framework) used to build starbeam.one v2.  I have been working on this framework in one form or another since 2005.  Difficult to believe it's been over 2 full decades now. 🤯  Of primary note and interest has been the rewrite of the Blazor rendering engine and the introduction of operation cancellation.  Every process can now be canceled, which helps out with resource management.  Yes, v1 didn't have this, and every process ran to completion, regardless of whether the user was still on the page.  This is no longer the case in v2; when the user navigates away from the page, any in-progress operations are canceled.

### Onto V3... Market Safety

Well, that does it for the v2 tour. What is next for v3?  I'm really working toward v4, and v3 helps put key pieces in place to make it a reality.  To start, with v2 features in place now, I hope no more major rewrites are necessary.  I hope to have v3 in place within the year easily.  The focus for v3 is Market Safety, and I hope to have this in place before working on v4:

- Login Refresh + Passkey support: I would like to improve our login system and add passkey support for improved security
- KYC (Know Your Customer): We want to get our users verified and only allow resale listings and withdrawals if you are verified
- Content Analysis: Enable AI-based content analysis to better gauge your content before publishing, prohibiting any content from being published if it does not fit our content policy
- Reporting System: In the case that content does get through and published, provide a reporting system that allows users to report products violating our content policy
- Crypto-withdrawals: Finally, with KYC in place, we will be able to provide payouts to users in countries that do not support PayPal or Coinbase accounts.  This is a major onboarding pain point right now, and I hope to address it in the next version.
