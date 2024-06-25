---
layout: post
title: <div class="text-center"> CHOMP! </div>
tags: []
date: 2024-06-11
author: Kashish Jaswani
mathjax: true
---
In this post, I am going to show you something really unconventional - something really unintuitive. By the end, I will convince you
that there are games you can win, without telling you how to win them ;)

Many games in game throy require very long and complex analysis to come up with a winning startegy. But what if I tell you that 
there are some games where you can win by simply - stealing your opponents startegy?

Let's look at a classic example - CHOMP.

<center>
<img src = "/assets/img/PENUP_20240621_220232.png" style = "width: 600px;"/>
</center>

Here are the rules - 

1. There is a rectangular chocolate bar with the bottom right piece poisoned.

2. You are allowed to bite any piece, but all pieces to the right and above the chosen piece also disappear.

3. The person who has to eat the poisoned piece loses.

How do you win in such a game?

Here's how, and pay careful attention to this proof - for it is not giving you a winning strategy anywhere, just a guarantee that you will win.

The first player starts with biting any piece. If this was a winning move, they win! If not, the second player (who we now assume has a winning strategy bites the next piece.
But this piece was available to the first player too (in his initial chance), hence the first player can just steal the 
winning strategy of the seocnd player and win. 

Let the craziness of this proof sink in! Just the absurdity of this proof, its non constructive nature, points at how beautiful maths is!

Such proofs are very common in context of strategy stealing, this type of game theory technique does not usually give a explicit strategy. To explore more, check out Lessons in Play
by David Wolfe, Michael H. Albert, and Richard J. Nowakowski.










