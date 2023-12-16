---
title: "PayPal Payout Fee Adjustments"
date: 2023-12-16T12:06:19-05:00
categories: [business, etc]
tags: [documentation, features]
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

### What's New?

We have supported PayPal Payouts since the market opened in June 2022.  At that time, my impression and understanding was that fees for this service were $0.25 for each payout.  It turns out this is accurate, but only for US-only payouts.  International payouts are 2%.

This misunderstanding was caught pretty quickly when we started to process international payouts, which comprise a majority of our payouts.

While it has been known for sometime, I am just now getting around to fixing it.  For 2023, the average fee was $0.30, which means I have paid $.05 for each payout made.  As I designed the system to pass on fees to the customer, this has been a costly issue that has only increased with time.

This was a tricky problem to solve, as I didn't want to onboard more user data that I would ultimately have to manage. 

It turns out the fix was easy, and I wish I would have thought of it sooner.

### What's Changing?

The fix is easy and obvious: PayPal knows the user country and it is provided when you update their Oauth2 application registration with the appropriate permissions.  So that is what is now requested with each connection request for a withdrawal.

**If your country is known**: For USA customers your fee is $0.25 and for all other countries the fee is 2% of the payout total.

**If your country is not known**: You are charged $0.35 for the withdrawal, which is higher for the past year's average and plus some to serve as an actual fee.  Please reconnect with your PayPal account (next section) so that your country can be determined an fees appropriately reflected.

### What to Do

*You only have to do something if your country is not known*.  We present a message denoting this along with a Connect with PayPal button to reconnect your connection with the country permission.  Upon refresh we will know your country and the fee will be reflected appropriately.  Look for the button below on *[the Withdrawal Request page](https://starbeam.one/profile/account/withdraw)* and press it:

![Connect with PayPal](https://blog.starbeam.one/images/paypal.png)

Upon completion you will return to the Withdrawal Request Page with the appropriate fees applied.
