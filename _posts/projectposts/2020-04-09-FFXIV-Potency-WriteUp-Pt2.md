---
layout: single
title:  "FFXIV Potency Design Analysis Pt. 2"
date:   2020-02-18 16:32:56 -0600
categories: [projects] 
author_profile: true
author: "Shrinath Rao"
permalink: /:categories/:title
---
While FFXIV might not be unique (systems like MHW’s bloat vs. raw damage are very similar), it does it's potency system very right. Every job, and every class you play deals (to my knowledge) just one of two kinds of damage: magic or physical. Additionally, while ~22 stat are in the game, they themselves are abstracted, so unless you really want to delve and dive into serious number crunching, you really don’t need to worry about all of this. Your gear, the abilities you use, the order in which you use them will all handle itself or be extremely obvious. For the most part, you don’t have to worry about it to succeed unless you’re playing with a high-level static trying to break DPS records. Well, it isn’t just the fact that they abstract it, it’s the design language behind the abstraction that’s the most fun to think about to me. 

Do I really need to look at my abilities and say, “Oh this does 20% of your weapon damage, and 50% of magic damage”? How truly relevant is that to my experience with the game? If I was playing another MMO, I’d probably have to dig, find out what my weapon damage was (a stat), check the magic damage (a stat) and calculate that, add the two up just to get the damage of a single ability. That doesn’t even tell me if it's effective yet. 

Let’s just say for a second that while my weapon damage is solid, my magic damage stat is abysmal. All of a sudden, even though the number “50” is larger than “20”, it could be that more of the abilities' damage is coming from my weapon than my ability. Being a weapon damage focused character, or having a weapon- focused “build”, this ability could actually be worse than the other 4 options I could be using in my rotation (the sequence of abilities a player uses in a fight). There are resources to manage, this ability might just be a waste of time and mana (an ability usually will require “x” amount of mana to be able to be used) and, without telling my friends to wait for 30 minutes while I crunch the numbers on all my abilities, I wouldn’t be any wiser. While some people might find that fun, how much of that is relevant to the average player? 

Now let's take a look at an FFXIV ability for Ninja (Aeolian Edge):

Delivers an attack with a potency of 100.
160 when executed from a target's rear.
Combo Action: Gust Slash
Combo Potency: 420
Rear Combo Potency: 480
Combo Bonus: Increases Ninki Gauge by 10

There are still numbers and they are large, but they are simple. I can get an ability, not ever look at my gear, and immediately know it has to be used after “wind slash,” and while my player is behind an enemy. No questions asked. It assures the non-number cruncher that, if ability X has a greater potency than ability Y, it will do more when compared in appropriate situations. If you noticed, FFXIV uses the word “potency”, and I absolutely adore this word. I actually used it long before I played this game, especially when looking to design kits, skills, and other things that would have to be balanced–things that would have to have stat numbers associated with them. 

For those number crunchers and gamers in the readership, potency describes the effectiveness of an ability relative to others, the formulas and number crunching absolutely still exist and are all online and are mined by the game’s community!

It might seem obvious but the language is kind of really apt as well. Potency not only describes the actual stat, but how potent, or how effective, that ability is on the field. It describes how much influence (another word I use constantly) that ability gives the player in a situation, at least numerically. Realistically, that’s really what you want to know from that tooltip! You’ll still have to choose things like “Hey, do I hit all the enemies in a room for 100 potency, or just one for 200 potency,” but the word, the arbitrary unit system that was used solely for comparing abilities, has been given it’s appropriate meaning, and I think that language, and that system, is pretty beautiful! 

I’ve always said whenever working on a stats system in a game, the numbers have to mean something and they have to be relevant. A lot about video games is quantification–to assign numerical value to a rather abstract concept. When a system gets cluttered, you really lose sight of what numbers represent–what those numbers are abstracting. In turn you can demean both your design language, philosophy, and the feel of your game. Sometimes, I don’t want to have to roll the dice for myself, the computer is there to do that job for me–I’d rather be playing the game. Of course there are caveats to that design philosophy. There always are, because at the end of the day, it’s design. 

Sometimes quality games and experiences can be rated on how deep a system like this lets you dive, or how complex it can be. To me, a complex system doesn’t have to be convoluted or cluttered. Not only that, there is something to be said about the versatility of a system. I’m not going to say that understanding the numerous stats in FFXIV isn’t cluttered, but because of how it’s implemented it isn’t required to be successful. The barrier for entry is lowered considerably. In an age where the amount of gamers are increasing rapidly and our medium of art is growing faster than ever, I’d always check if the system or game is still accessible to those who don’t want to dive too deep into it?

Thanks for reading!
- Kshaya