---
layout: single
title:  "FFXIV Ninja Platformer"
date:   2020-03-25 16:32:56 -0600
categories: [blog] 
author_profile: true
author: "Shrinath Rao"
permalink: /:categories/:title
---

After playing FFXIV for a while, I’ve settled on Ninja as my main job. I find the pacing, the complexity, and the utility of the class very enjoyable, and I have a hard time shifting out of it. There’s a set time interval in rotations where you double down and burn all available resources and then when that’s over you can sit back reposition and take it easy for a bit. The most interesting part of the job to me though is the real-time spell crafting system that involves signing a series of mudras in a specific order to cast different spells. Let’s say I mapped the keys “1”, “2”, “3”, “4” to “Ten”, “Chi”, “Jin”, and “Cast” respectively. If I entered in the combination “1, 3, 2, 4” it would cast “Doton”, an AOE DoT ability, while “1, 2, 4” would cast “Raiton”, a single target nuke. I have two stacks of mudras, and each stack refills at around every 10s.

![image-center](../_img/Ninja/FFXIVNinjaCasting.gif){: .align-center}

Its a really enjoyable casting system, I feel like a ninja casting ninjutsu and the memorization of all the possible spells raises the skill floor for the class a considerable amount while still keeping it accessible. At first, my biggest doubt with this roguish class was how reactive it would be, and the input lag was just a part of it. A rogue having to sit in one place while signing mudras to cast a spell seems a little bit counterproductive, since as a rogue, I’d like to be incredibly fast-paced and reactionary. I’d like to be able to react to my friends or the boss's callouts or moves, and the potential of being caught off guard seemed like a poor choice for this specific class. The ninja thankfully didn’t feel like that, and the only times I've been caught very off guard was when I failed as a player, the job has never failed me. It maintains its speed and fasts paced combat while having a healthy dose of utility.

How would this system be in a platformer? How robust would this feel elsewhere, outside of an MMO? I decided to craft a platformer to find out how it would hold up in a completely different genre and I had quite a bit of fun doing it. I used Unity’s latest LWRP (Lightweight rendering pipeline) for the 2D lighting and some free assets from itch.io and made a quick sandbox that toyed with the ninja’s real-time spell crafting system.

To start, I first needed a test station to work with- an environment to work on I worked with the LWRP for some lighting and the above mentioned itch.io assets to get a basic test setup/level going. Having an appropriate level or setup always helps me get into the zone for how a class or a game is supposed to feel. After the test level, I started writing a basic movement controller with Unity2D. I spent quite a bit of time on this basic step since getting the speed, the jump heights, and even how much gravity affects a character all help make a game feel unique even if it isn’t polished just yet. To give jumps a basic and quick feel polish I looked up some other famous platformers and noticed that for a lot of these games, there were almost twice as many frames in the +y axis than there were in the -y-axis. Jumping was slower than falling. This was very very easy to accomplish just by editing the gravity values on the downwards portion of the jump via the Rigidbody2D and animation events in C#.
![image-center](../_img/Ninja/Background.PNG){: .align-center}

After the basic movement, I got started on animation. Working with animation state machines in Unity is made a breeze thanks to being able to provide animation events. It means the engine will call a given callback function on a specific frame. This is used and is incredibly useful in almost every game- it helps time physics and particle effects to character animations. There are a couple of parts to this animator. The first being that I made a general animator for movement, the others are two child state diagrams- one for the attacking, and the other for the casting. In the attacking diagram, I made a basic 3 step combo and in the casting diagram, I made a general one hand cast animation state (can be triggered via a boolean), and other specialized states for the doton (ground AOE), and the katon (throw an explosion down).

![image-center](../_img/Ninja/animatorBase.PNG){: .align-center}
![image-center](../_img/Ninja/animatorAttacking.PNG){: .align-center}
![image-center](../_img/Ninja/animatorCasting.PNG){: .align-center}

Now that I had some basic animations, a movement controller, and a sandbox, it was time to make the backend of the mechanic work. I made a separate script that would hold and be responsible for handling all the casting and got to work. I made two enums, one for representing the actual mudras, and one for representing the spell they would result in. To represent the spells themselves, I used lists since I knew they had a handy “list.SequenceEquals(list1)” function. I had a total of 5 lists, one which I called the spell queue, and one representing each of the abilities I was going to implement. The ability lists were initialized to their appropriate mudra sequence, for example:

```
Raiton = new List<int> {(int)Mudras.ten, (int)Mudras.chi};
```

Whenever a player entered a mudra, it would be appended to my spell queue. Whenever a player hit the cast button, it would call a function that would evaluate the spell queue by comparing it to the other lists! This way, if I ever wanted to implement another ability, it would be very easy in the backend. Also, if the mudra didn’t line up with any of the checked abilities, by default the evaluate function will return “(int)Spells.bunnyHat”. Nothing is currently done with this, but in the future since it returns (int)Spells.bunnyHat, we can punish the player for bad input, much like the MMO does.

All that was missing was the particle effects. I spent some time making the lightning shuriken, modifying some other particle effects using some existing Unity particle effects I had left over from Cypher. I made some prefabs out of them, and setup the physics for each one of the projectile attacks. Katon was a fun one to make since it technically isn’t just a particle effect. The spell feels like throwing down a grenade and it exploding on impact, so that’s what I did! I attached a small collider to a sprite I had laying around and on contact with either an enemy class (future proofing) or anything labled ground, it would explode in a brilliant fireball!

After getting the animations working relatively smoothly, I hooked them up to the character. Here I think I stumbled on a lot of fun with Katon- in FFXIV, the ninja has a spell called Katon where he blows fire in an AOE, but an override of that spell is called Goka Mekkyaku where the animation is the player jumping into the air and raining a fireball down on the ground. That seemed more interesting than Katon, so I tried to replicate that in 2D and it resulted in this:

![image-center](../_img/Ninja/katon.gif){: .align-center}



You might notice that I used cinemachine and some perlin noise to make the camera feel a little bit more alive and polished, but other than that, that was where I stopped! I had a working sandbox ready to be taken to the next level! This would be a project I wouldn’t mind continuing if I had some more time.

-Kshaya
