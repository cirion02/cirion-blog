---
layout: post
title: How good is Lutri?
date: 2025-10-01 19:36:00 +1000
tags:
  - mtg
  - cube
  - math
---

![Lutri, the Spellchaser](https://cards.scryfall.io/large/front/f/b/fb1189c9-7842-466e-8238-1e02677d8494.jpg?1628801771)

Lutri, the Spellchaser is a unique card when it comes to cube. It is the only "free" card you get in most cubes. (As long as the cube is singleton. (And doesn't have conspiracies.)) Which makes it a very different card to try and evaluate, in this post I'm not going to answer how good a Dualcaster Mage that can't combo is. But I will try to provide a framework for evaluating Lutri in a deck, in a mathematical sense.

The framework I'll be using revolves around `game win probability added` this is not a value I will be giving actual numbers for, but it will be used to compare cards abstractly. From now on i will shorten this to just %, so Lutri% is the percentage your winrate improves if you have Lutri.

Now the first thing to consider is the cost of picking Lutri, which is that you're not picking anything else. Which amounts to replacing whatever card you could've picked with the 23rd best card in your final pool. From now on I will be referring to the card you could've picked instead of Lutri as the `Missed` card, and the 23rd best card in your final pool as the `Replacement` card. 

When evaluating the power of the missed card, we must compare it to the replacement card. Effectively the power of picking the missed card is `Missed%-Replacement%`. Lutri is different, since Lutri is not replacing a card in your deck, it is always an extra piece, so it can just be evaluated as `Lutri%-0`. This is the first factor making Lutri strong.

The second is that well, you don't have to draw Lutri. There will be some amount of games where the Missed card is not drawn. In which case the GW%+ is 0.

The math here is fairly simple, the chance any given card is in the first `X` cards you draw is `X/40`.
So lets consider a one drop which specifically wants to be drawn on turn one, for an example, consider it to be [Ragavan](https://cards.scryfall.io/large/front/a/9/a9738cda-adb1-47fb-9f4c-ecd930228c4d.jpg?1681963138). On turn one you'll have drawn 7.5 cards. So the chance you draw Ragavan on turn 1 is `7.5/40~=19%`. (This is underestimating, see footnote[^1]) If we take this at face value, we should ask if Ragavan is not just 5 times as good as Lutri, but if the difference between Ragavan% and Replacement% is 5 times as high as Lutri%.

Now most games, even in vintage cube, are longer than 1 turn. So lets consider a more general case, if we draw `X` cards over the course of a game. You divide the WP+% of the Missed card by `40/X` to adjust for the chance the card is not drawn. If a card only matter before a certain turn, just pick an `X` that excludes any later turns.

So to put it as a formula


{% highlight xml %}

L = Win chance of Lutri
M = Win chance of the missed card
R = Win chance of the replacement card
# = Number of cards drawn in a game

IF  L > (# * (M-R)/40) THEN [pick Lutri]
ELSE [pick missed card]

{% endhighlight %}


Lets do one full example before I end this post. The numbers here will be fully pulled out of my ass, I will leave finding the correct powerlevel to actual good cube players. We'll be comparing Lutri to [Fatal Push](https://cards.scryfall.io/normal/front/b/5/b5e81649-9954-424c-89d1-f87d73b66047.jpg?1595869185), and our replacement card is what I consider the weakest black removal spell in the current vintage cube, [Baleful Mastery](https://cards.scryfall.io/normal/front/3/5/35f1a6ba-e46f-44fb-93f4-fb883d677b36.jpg?1624590749).
My estimate that Lutri wins you a game you would not otherwise have won at about 1/20, and I expect an random vintage cube deck to draw 15 cards in a game. That makes the math
`0.05 > (15 * (M-R)/40)`
`0.05/15 > (M-R)/40`
`(0.05/15)*40 > (M-R)`
`2/15 > M-R`
So that comes out to, does Balefull Mastery lose you a game Fatal Push would've won 2 out of 15 times it's in your hand. And well, I do not know. I also don't know if Lutri's win rate is actually 1/20. But I hope overall this math can be used by people with better card evaluation skills to pick Lutri at correct times.

[^1]: This assumes mulligans are not important, this is reasonable if you assume Ragavan is not relevant to the chance of a hand being a mulligan. This is false, both in a positive sense, a hand containing Ragavan is more likely to contain 0 lands; and in a negative sense, Ragavan is a really good card and makes opening hands it is in better and thus more likely to be kept.