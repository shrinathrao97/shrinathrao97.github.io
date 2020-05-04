---
layout: single
title:  "WIP: Astral Chain Perfect Dodge 2"
date:   2020-04-28 16:32:56 -0600
categories: [blog] 
author_profile: true
author: "Shrinath Rao"
permalink: /:categories/:title
---
Today I polished up the movement system a bit, and I got to work on the animations working. I actually am having a slightly hard time finding good animation for this character- I want him to feel fast and zippy much like warframe’s character do but I don’t want him sliding all over the place. I managed to pick up a ninja animation pack on sale today- a lot of the animations are super cool, I just don’t know how much of it vibes with the character I’m trying to make. There is a shuriken throw animation with a shuriken model and skeleton so that saves me some time! The walk animation doesn’t fit well.

I’m currently using a mixamo character (it’s free…), and there's a lot of “cheating” going on with this. I don’t know how much I enjoy doing the bone mapping from the mixamo ninja skeleton to the unreal mannequin (ninja animations). Even with me double-checking the mapping and matching the T-pose properly, the animations are slightly off and my character's fingers grow in size every time they do an animation meant for the unreal mannequin skeleton. I do, however, have a sweet 3 step attack combo from mixamo though that fits the character very well, the only problem is that the mixamo skeleton doesn’t exactly do root motion well, meaning this animation is probably quite useless to me. I don’t think I’ve had this issue before (not exactly finding assets) as Mixamo works pretty well with Unity3D and Mechanim.

Overall though, I have working animations (albeit excessively clunky), but more importantly, working blendspaces and a working animation blueprint. Today I also had to make some important decisions about root motion vs. in-place animations since the Ninja pack off of the Unreal store actually gave me both. As an animator, and from a quality and polish perspective, root motion seems fantastic. It allows the animation to breathe life into the game, but as a coder, working with in place (puppet in a collider box) just seems far too easy. I also want to go for that super-fast warframe feel for this character and the easiest way to encourage that is to move the collider with code. I decided to use in place. There probably will come a time in this game where root motion will be better- we’ll cross that bridge when we get there.

Update @ 1 am: I can’t shake the feeling that I should just use the unreal mannequin for this. I love this ninja model- it fits the theme of the game, but the mixamo skeleton and animation not working just make using this thing a chore. I’ve updated the skeleton mesh, the anim blueprints, and the animations to all use the unreal mannequin. Hopefully, this solves the issues

Update @ 2 am: Can confirm- the skeletons from mixamo were the culprits of practically all the problems for me. Unfortunate, but at least the game doesn’t look atrocious now. I'll have to find attack animations to replace the mixamo ones now… Tentatively, I’ll just use the fisticuff animations given to me by my $4.99 ninja animation pack! I’m still using some weird mixamo mangled animations for movement but at least they work now. Now for a good night's rest…

-Kshaya
