---
layout: post
title: Anonymous Drawing as a Solution to Tournament cEDH draws
date: 2026-07-09 17:17:00 +1000
tags:
  - mtg
  - game-theory
  - cedh
---
In tournament level cEDH[^1] there is an unfavorable strategy revolving around drawing the game, which I believe can be solved with a small tweak to the rules used in such a tournament. I will describe this change in this article, but first, a short primer on the problem.[^2] 

The strategy revolves around intentional draws. If all players agree to a draw, the game ends in a draw. Traditionally you get 5 points for winning, 1 for drawing, and 0 for losing. A game can intentionally end in a draw if agreed to by all players [(source)](https://www.cedheurope.com/rules/mtr-addendum#2-5-conceding-or-intentionally-drawing-games-or-matches). Now that raises a potential strategy: Player A can say to Player B, "If you don't agree to a draw, I'll let Player C win.", then say the opposite to Player C. Thereby forcing a draw, as if either player disagrees, the other player wins. Now this specific level of coercion is generally not allowed [(source)](https://www.cedheurope.com/rules/mtr-addendum#5-4-unsporting-conduct). However the general principle still happens in the form of "I have a counterspell and I could stop you, but then the next player wins. Let's draw instead." Now whether this outcome is desirable or not is subjective, but I personally would say it is not.

There are a number of possible ways to stop this. From a tournament perspective, you can make draws worth 0 points. Alternatively from a player perspective, you can choose to personally announce you'll never accept draws like this. But ultimately if this practice is considered undesirable, I believe it should be removed using rules, not by making players make suboptimal decisions[^3]. But making draws worth 0 punishes slower games which may not be a desirable side effect. So I'll propose an alternative solution that only affects the intentional drawing procedure.

Anonymous draw voting: Each player is given a "yes" and "no" card, and when a draw is proposed, each player picks one of the cards. After everyone has picked a card, the pile is shuffled and then revealed. If all four cards are "yes", the game is a draw. 

This system removes the primary incentive to draw from the players who are ahead. As they cannot be punished for their vote. The player with a counterspell cannot know if the player attempting to win right now or the player after them stopped the draw vote. Which means they will have to make their choice on in game metrics. (This does force players to be capable of lying sufficiently well to keep the votes secret, but I do not expect that to be a problem.)

A possible problem with this solution is that this system of draws may be considered preferable to the alternative where players pick whether they stop someone from winning based on out of game metrics. If a player believes themselves to have a 0% chance to win the game and a 0% chance to draw the game, their behavior from a game theory perspective becomes unpredictable. Said player may now take actions considered unfavorable. (Like letting the player they like more win.) Doing this would be against currently existing rules [(source)](https://www.cedheurope.com/rules/mtr-addendum#5-4-unsporting-conduct). However, this may be hard to enforce. Ultimately, while I feel this problem is worth noting, I will not field a solution at this moment, as I cannot predict whether it would actually be a serious issue.

[^1]: cEDH stands for competitive EDH, or competitive commander, a 4 player multiplayer format.
[^2]: As I am personally not a tournament cEDH player, it could be possible that what I see as a problem is actually considered desirable, in which case no changes should be made.
[^3]: Suboptimal in the context of this single game, it could be advantageous over a longer period of multiple games. 