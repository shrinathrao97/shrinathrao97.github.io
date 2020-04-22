---
layout: single
title:  "FFXIV Potency Design Analysis"
date:   2020-02-15 16:32:56 -0600
categories: [projects] 
author_profile: true
author: "Shrinath Rao"
permalink: /:categories/:title
---
The following is a long write up I did after getting interested in the potency system from FFXIV. I analyze raw vs. potency values and why I think that FFXIV's system is well designed.

Today I’d like to talk about RPG (role-playing game) stat systems. These systems come in many shapes and sizes, but their purpose mostly remains the same philosophically. They aim to represent and quantify a player character’s familiarity with different worldly skills, and allow the player to gauge the impact of certain actions. Now that I’m sitting at ~500 hours of in-game time with FFXIV, I’ve begun noticing interesting things about it, like the very interesting and well implemented potency system the game uses. 

But before I dive into the nitty-gritty, let’s take five. A lot of people have played D&D (Dungeons & Dragons) or other role-playing tabletop games. A lot of these games, because of their history and intimate connections to designer’s lives serve as sources of inspiration for different games and systems. In fact, I had a professor who once said “Most systems for video games are an abstraction of other traditional tabletop systems.” The more I thought about this, I actually couldn’t think of a counter example without it feeling like something to which my professor could rightfully respond, “I did say most, and even then that is such a technicality... you get what I mean to say.”

As a quick brief, since a lot of the readers might be friends or family who aren’t gaming oriented, D&D is a tabletop game–there are no computer screens involved (think of a board game, but sometimes without the board). You and your friends create characters, sit around a table, and role-playing as your newly-created personalities. You go on adventures and quests together in a world run by a DM (Dungeon Master)– someone who creates, enforces, and manages with the causality of the world. 

Now, a lot of the interesting portions of D&D come from its stat system. Each character has their own stats called “Ability Scores” in 6 catagories: Strength, Dexterity, Constitution, Intelligence, Wisdom, and Charisma. 

I use the term “abstraction” to describe game systems like this. The system is abstracting a normal, multifaceted personality into 6 broad categories or stats. Abstraction in programming is the idea of hiding and sometimes removing details that face the user to reduce unnecessary complexity and to make life easier. It’s about showing relevant information rather than all the information. I’d like to think that the object oriented programming principle is just as important to modern game design as it is to engineering.

Anyway, whenever your character wants to accomplish a certain task that isn’t mundane (one that your character might fail at if you aren’t skilled at that task), your DM might ask you to roll a d20 (a 20 sided dice) and add a portion of a specific ability score to see if your attempt fails his/her predetermined pass/fail threshold. 

As an example, Dustin (a D&D player) might say, “Hey, Hudson, my character tries to pick up this super heavy obelisk”. 

To this Hudson (the DM) might respond, “Alright, make a Strength Check to see if you can lift it.” 

In Hudson’s mind, Dustin has to pass a DC 15 (Difficulty Class, or the number Dustin has to roll more than or equal to) check to succeed, anything else is a failure and Dustincan’t lift the stone. Dustin would roll his d20 and add his predetermined Strength Ability Modifier (an attribute of your character) to see what happens. The situation plays out differently, depending on how the dice rolls, and how good Dustin’s character is at the Strength stat (obviously, the higher the stat, the better). As you can glean, statistics plays a great role in D&D and other tabletop RPG systems. At a high level, they directly affect your influence on the world you’re in. 

Now with that in the back of your mind, let’s think about today's video game stat systems. Like my professor once said, a lot of video game systems are just abstracted versions of traditional tabletop systems. When we look at games like League of Legends, Diablo, Dota 2, or other RPGs we can sometimes see our characters attack an enemy and miss. I’d wager, at least in principle, the concept is the same. Instead of the player physically rolling a die, adding an ability score modifier to it, and then telling the computer, “hey I rolled this number, this is my modifier, make the attack hit,” the computer rolls the dice and does all the math for you in real time. The animation and physics all happen in real time, nice and smooth, giving way to a nice-feeling bout of fisticuffs with that evil zombie attacking a village. Along the same vein, pickpocketing is a fun little mechanic in many video games. If your character is good at a specific stat, the odds of pickpocketing successfully increases greatly and you can often get special items that you normally wouldn’t otherwise be able to procure. 

All that’s happening in either of these situations is that, instead of letting the player deal with all these numbers and dice rolling while a fight is happening, or while the player is in an instance, the computer plays the role of DM in a lot of ways, abstracting the entire role of the DM, for the player. The player doesn’t have to see rolling dice, it just isn’t relevant to the experience the designers are giving to the players. It isn’t any less or more complex than traditional tabletop systems, don’t get me wrong. The experiences just place emphasis on different things. While D&D places a lot of importance on statistics, video games place more importance on, for example, fast-paced decision making, accurate positioning on a field, or deep team play or strategy.

Now back to FFXIV. I love the stat system in this game. MMOs, on top of their social and mechanical complexity, are often known to be very statistics and number heavy games–there are a lot of numbers to crunch. So much so, that many players parse. They use a special third-party plugin or software to see how much damage their abilities do and appropriately choose and level up their stats to function better for their teams. Players in FFXIV fall into one of three roles: damage dealers, damage takers, and damage healers. All of these roles make use of different stats or ability scores in different ways. Now, as with anything pertaining to any media, this number crunching and “min/maxing” (a game design term for players who optimize their characters) mentality is either loved or hated.

Why? Abstraction. A lot of people might want to jump onto a game, play with friends, and enjoy an experience together while sitting in the comfort of their home after a long day’s work. It is a game after all, not statistics 101. Sometimes, I don’t want to apply a formula just to see if I’m doing a good at a game. These systems can encourage, and a lot of times require so much of a deep and rabbit-hole oriented thought process, that for some people, even if they might enjoy the art, the story, the feel and the community of a game, playing it becomes a chore where you sit and look at menus and numbers more than playing a game with friends on a Friday night. It’s a very fair criticism for most MMOs, but this is why I love FFXIV. 

While FFXIV might not be unique in this regard (systems like MHW’s bloat vs. raw damage are very similar), it does it very right. Every job, every class you play deals (to my knowledge) just one of two kinds of damage: magic or physical. Additionally, while ~22 stat are in the game, they themselves are abstracted, so unless you really want to delve and dive into serious number crunching, you really don’t need to worry about all of this. Your gear, the abilities you use, the order in which you use them will handle itself or be extremely obvious. For the most part, you don’t have to worry about it to succeed unless you’re playing with a high-level static trying to break DPS records. Well, it isn’t just the fact that they abstract it, it’s the design language behind the abstraction that’s the most fun to think about to me. 

Think about it. Do I really need to look at my abilities and say, “Oh this does 20% of your weapon damage, and 50% of magic damage”? How truly relevant is that to my experience with the game? If I was playing another MMO, I’d probably have to dig, find out what my weapon damage was (a stat), check the magic damage (a stat) and calculate that, add the two up just to get the damage of a single ability. That doesn’t even tell me if it's effective yet. 

Let’s just say for a second that while my weapon damage is solid, my magic damage stat is abysmal. All of a sudden, even though the number “50” is larger than “20”, it could be that more of the abilities' damage is coming from my weapon than my ability. Being a weapon damage focused character, or having a weapon- focused “build”, this ability could actually be worse than the other 4 options I could be using in my rotation (the sequence of abilities a player uses in a fight). There are resources to manage, this ability might just be a waste of time and mana (an ability usually will require “x” amount of mana to be able to be used) and, without telling my friends to wait for 30 minutes while I crunch the numbers on all my abilities, I wouldn’t be any wiser. While some people might find that fun, how much of that is relevant to the average player? 

Now let's take a look at an FFXIV  ability for Ninja (Aeolian Edge):

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





