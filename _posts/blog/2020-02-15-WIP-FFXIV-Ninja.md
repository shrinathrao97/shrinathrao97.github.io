---
layout: single
title:  "WIP: FFXIV Ninja Platformer"
date:   2020-03-25 16:32:56 -0600
categories: [blog] 
author_profile: true
author: "Shrinath Rao"
permalink: /:categories/:title
---

After playing FFXIV for a while, I've settled on Ninja as my main job. I find the pacing, the complexity and the utility of the class very enjoyable, and I have a hard time shifting out of it. There's a set time interval in rotations where you double down and burn all available resources and then when that's over you can sit back reposition and take it easy for a bit. The most interesting part of the job to me though, is the real time spell crafting system that involves signing a series of mudras in a specific order to cast different spells. Let's say I mapped the keys "1", "2", "3", "4" to "Ten", "Chi", "Jin", and "Cast" respectively. If I entered in the combination "1, 3, 2, 4" it would cast "Doton", an AOE DoT ability, while "1, 2, 4" would cast "Raiton", a single target nuke. I have two stacks of mudras, and each stack refills at around every 10s.

Its a really enjoyable casting system, I feel like a ninja casting a ninjustsu and the memorization of all the possible spells raises the skill floor for the class a considerable amount while still keeping it accessible. At first, my biggest doubt with this rougish class was how reactive it would be, and input lag was just a part of it. A rogue having to sit in one place while signing mudras to cast a spell seems a little bit counter productive, since as a rogue, I'd like to be incredibly fast paced and reactionary. I'd like to be able to react to my friends or the bosses callouts or moves, and the potential of being caught of guard seemed like a poor choice for this specific class. The ninja, thankfully didn't feel like that, and the only times ive been caught very off guard was when I failed as a player, the job has never failed me. It maintains its speed and fast paced combat while having a healthy dose of utility. 

How would this system be in a platformer, how robust would this feel elsewhere, outside of an MMO? I decided to craft a platformer to find out how it would hold up in a completely different genre and I had quite a bit of fun doing it. I used Unity's latest LWRP (Light weight rendering pipeline) for the 2D lighting and some free assets from itch.io and made a quick sandbox that toyed with the ninja's real time spell crafting system.

To start off, I first needed a test station to work with- an environment to work on I worked with the LWRP for some lighting and the above mentioned itch.io assets to get a basic test setup/level going. Having an appropriate level or setup always helps me get into the zone for how a class or a game is supposed to feel. After the test level, I started writing a basic movement controller with Unity2D. I actually spent quite a bit of time on this basic step since getting the speed, the jump heights and even how much gravity affects a character all help make a game feel unique even if it isn't polished just yet. To give jumps a basic and quick feel polish I looked up some other famous platformers and noticed that for a lot of these games,there were almost twice as many frames in the +y axis than there were in the -y axis. Jumping was slower than falling. This was very very easy to accomplish just by editing the gravity values on the downwards portion of the jump.

After basic movement, I got started on animation. Working with animation state machines in Unity is made a breeze thanks to being able to provide animation events. It means that the engine will take a given callback function and call it on a specific frame. This is used and is incredibly useful in most every game- it helps time physics and particle effects to character animations. 
