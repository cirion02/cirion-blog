---
layout: post
title: Is the New Arena Draft Mode Worth It?
date: 2026-05-23 18:19:00 +1000
tags:
  - mtg
  - math
  - retail-limited
edited: 2026-05-23 19:05:00 +1000
---
In the latest arena announcement, Wizards unveiled a new draft mode, "Contender Draft". This costs more to enter, but has higher rewards for doing well. In this article I'll be evaluating if it is worth it to play that mode instead of Premier Draft.

For the methodology of this article, I will be assuming you enter drafts by paying gems, and that booster packs do not matter to you, as that seems to be the consensus among strong drafters I know.

Let's start with the reward table for both events (adjusted for their different entry costs.)

|                 | 0-3   | 1-3   | 2-3   | 3-3   | 4-3  | 5-3  | 6-3   | 7-X*  |
| --------------- | ----- | ----- | ----- | ----- | ---- | ---- | ----- | ----- |
| Premier Draft   | -1450 | -1400 | -1250 | -500  | -100 | +100 | +300  | +700  |
| Contender Draft | -3000 | -3000 | -3000 | -1600 | -200 | +200 | +1200 | +4200 |
\*Note that 7-0, 7-1 & 7-2 all pay the same in both modes.  

From this chart we can see a couple of things. It is a lot easier to offset bad results with good ones in contender draft, as a 7-X pays for almost 1.5 0-3's. Whereas in premier it pays for less than half. premier draft does make an even 3-3 record sting a lot less. The numbers in contender are also obviously bigger, which makes it likely that anyone with a low winrate should stay away from contender draft. But let's get into the hard math.

I will be performing the math in two ways, in the theoretical world, where I just calculate the EV for any given winrate. (This assumes your winrate is the same at 0-2 as it is at 6-0, which might be untrue, since your decks are obviously different power levels, but I expect the opponents decks to broadly cancel out that effect.) Secondly I will be testing it directly again a sample of ~250 drafts from one of my friends, who is an excellent drafter. 

First, the winrate data, the graph looks like this, the X-axis being your winrate in %, and the Y-axis being your expected gems divided by 100. (This is done to make the graph look nicer.)
![Graph of winrate vs reward]({{site.baseurl}}/assets/img/DraftRewardGraph.png)
The red line is for premier draft, the Purple line is for contender draft.

From this we can see that contender breaks even much faster, and is better than premier even before that. The exact breakpoint is that contender has a higher return is at 57.86% winrate. Contender breaks even at 60.7% winrate, while premier only breaks even at a 67.8% winrate. So from these metrics all strong drafters should shift over.

Now let's compare our real world data. My friend has an overall record of 1189-662 over the course of 266 drafts.[^1] That means a 64.2% winrate. The formula above expects him to have lost an average of 145 gems per draft, he actually averaged losing 119, which is better but close to the expected value, so the math is probably reasonably accurate. However if he had been earning the rewards of contender draft, he would've earned 565 gems per draft on average. That's a total of 182k gems lost, which would cost over 900 dollars to buy.

Overall, contender draft is rewarded excellently, but there is one final hurdle. The average player in a contender draft is probably better at the game. This can be accounted for by modeling the player's winrate as going down in contender vs premier. Modeling this as a 3% drop moves the crossover point to a 62.1% (premier) winrate. However the exact numbers here are hard to guess as there is no data to work with. Overall I do expect strong drafters will probably make more gems in this new gamemode.



[1]: This data is from between 2024-1-1 and 2026-5-23, and the friend considered his skill to be pretty stable in that timeframe.