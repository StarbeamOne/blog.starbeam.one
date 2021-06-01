---
title: "Your Private Key Can Be Guessed"
date: 2021-06-01T07:40:25-04:00
categories: [business, technology]
tags: []
author: Mike-E-angelo
authors: [Mike-E-angelo]
featuredImage: ''
draft: false
---

One final thought here and I'll finish.  I promise. 😁

In addition to [some of the risks I outlined earlier in this article](/2021/05/decentralization-is-a-foreign-land/) with regards to cryptocurrency, there's one in particular that I feel needs extra mention.  Namely, the private key that keeps your value safe is simply a number: a very very very large number.

That conceivably means that if someone guesses that number, they have access to your wallet.

[There is even a site that is dedicated to you trying this out](https://keys.lol/).

Now, the number is *really* large, and that is of course by design and what makes this "secure."  To give you an idea how large, if you were somehow able to get a 1,000 machines in place that could each guess 1 trillion times a second each (for a total of [1 quadrillion guesses a second](https://www.quora.com/What-is-a-trillion-times-a-thousand)), it would take you roughly ~46,343,912,903,694,300 years to guess one address, assuming there are 1 billion ETH addresses on the network ([there are currently 175M](https://etherscan.io/chart/address), so it would take even longer today).

At first blush, this appears to be not a problem.  And it *probably* isn't, but it's definitely something to be aware of when deciding if the decentralized space is suitable for you and your use.  Because it's decentralized, there's no "authority" to appeal to if someone guesses that number -- as unlikely that it is to occur.

Keep in mind that if someone *does* guess your address, no amount of cold storage or [device protection](https://www.ledger.com/) will stop someone utilizing it.  The only protection you do have is if you have [multi-sig configured](https://www.innominds.com/blog/securing-ethereum-wallet-with-multisig) on your wallet.  

This, of course, only doubles the amount of complexity to a system that is already facing problems with usability and adoption.

What gives me pause about all this is something that I feel doesn't get a fair shake here, and that is the the whole notion of random number generation.  We can think of guessing a series of numbers either in linear (sequential) order, or by randomly generating a set of them (or somewhere in between).  To me, it would seem that if you put enough randomness in there, the propensity to land on an address would be more likely than if you sequentially shoot through the set, starting at zero.

Seems like a nice project idea to that find out.  In fact, I almost did *exactly* that at one point, but I started think:

If I landed on an address, I would be put into an ethical/moral quandary.  Do I take the money (become a thief) or do I report it (become an activist for something I am basically exploiting).  Neither of these options seemed very appealing to me, so I ultimately took a pass.  

I am glad I did, too, because it wasn't long thereafter that I realized I could build starbeam.one instead. ✌
