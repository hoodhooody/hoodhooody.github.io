---
layout: post
title: "Chaos Goblin: An approach to Unity development"
date: 2023-07-06
description: "Dive into the world of game development with the Chaos Goblin approach. This guide explains how to navigate through challenges, innovate through trickery, and deliver an unforgettable user experience. Gain insights into best practices and game development solutions that work. Perfect read for budding game developers!"
tags: [gamedev,unity,guide]
---
One of the most paralyzing feelings when starting any game development project is the one you get right after you've finished your initial game design, whether that might be a few ideas jotted down on napkins for a game jam or the traditional 10-page design document.

Because after you've decided that your game is going to be a ROGUELITE-RTS-MMORPG, you actually have to build the thing, see?

And let's say you decided the first thing you're going to build is the RTS portion of it. So you jot down the user story, tasks, or whatever unit of work you use to organize yourself.

Then let's say that the first item in that list is "Implement Scrollable Map".

And oops! You've never implemented an scrollable map. But no bother, Google to the rescue, am I right?

But what happens if the solution you find online doesn't do exactly what you need? Or the solution you find is 15 years old? Or there are loads of comments underneath saying how bad of a solution it is but without a single one specifying a better one[^0]?

So, you can't find a code reference for whatever it is you're trying to build. What's a game developer to do?

The answer is to enter Chaos Goblin mode.

For those of you unfamiliar with goblins, they're an oft-featured race in several works of fantasy, typically depicted as a smaller cousin to the more serious orc or hobgoblin. In some other properties, they're depicted as being mechanically proficient in a very specific way. And that way is unreliably. Meaning that things goblins make sometimes work, not so much because they're well designed or made, but rather from sheer ingenuity and hard-headedness.

And that is the essence of the Chaos Goblin approach to game development. Now, I'm sure I'm starting to lose you a bit here, so let me come back around and summarize the essence of Chaos Goblin:

*The only thing that matters is what the user experiences. How it works is no one's business.*

To further illustrate this point let me tell you about Fallout 3's Presidential Metro Head. You can read the full story [here](https://www.eurogamer.net/you-wore-fallout-3s-metro-on-your-head). The gist of it is that during a scene in the game where the player thinks they're standing inside a metro, the player's headgear has actually been replaced with the model for a metro car, and it's the player's own model who is moving on a predetermined track.

Some players might read this and think that the developers were being lazy. But the truth of the matter is that developers do this kind of thing all the time.

And it is precisely those kind of practices that form the tenets of Chaos Goblin mode, which are as follows.

### What the player doesn't know can't hurt them

Let's say that in a portion of your game the player is standing inside a castle tower and is firing arrows at a dragon that's flying outside. Every now and again the dragon comes close and pushes its head through the window to try and bite the player.

Now, as far as the player is concerned the dragon is actually flying out there. But we, as game developers, might have employed a few tricks to help with this illusion and to optimize the situation. Some things that could be done are as follows:

* Use different models depending on how far the dragon is from the player. The player can only see the dragon's details when it's close, so why not replace the dragon's 3D model with something that has less detail, but will also occupy less space in memory?
* Shut off the dragon when the player isn't looking at it. By keeping track of where the player is looking, we can selectively turn 3D models on and off to save on rendering.
* Prevent the player from seeing unfinished work. Let's say that for whatever reason, the art for the environment outside the tower is unfinished. So if the player ever steps out onto the ledge of the window they will see nothing. To help with this, the game designers decided that the ledge of the window will become an instant death spot. So when the player stands on the ledge, a 3-second sound of a dragon's roar will play and the player's screen will start to darken. Once the 3-second sound is over, we play a quick animation of the dragon eating the player (perhaps reusing one we already had). As far as the player is concerned, the ledge is just a place where the dragon can pick them off; they don't need to know it was done to prevent them from seeing unfinished work.
* Perhaps when the dragon puts its head through the window we replace the full dragon model with a smaller but more detailed head model. This would allow us to free memory from a model we're not using, while letting us give the player an improved experience.

If you've been in the games industry for any length of time, you probably recognize the above as standard practices, but there was a time when these techniques were considered clever trickery and quite innovative.

It's now up to you to come up with new ways to trick your players into thinking there is far more to what they're seeing.

### The best solution is the one that is currently working

A lot of game developers get stuck because they try to come up with solutions that cover all possible future scenarios.

This attitude can be valuable under the right circumstances, but when you're in Chaos Goblin mode, the objective is to get something working as fast as possible.

An addendum to this:

#### A flawed prototype is more valuable than any unfinished masterpiece

Similar to the point above, many developers become frozen when trying to implement a feature because they try to optimize too early.

Optimization should be left until the project has a need to run on machines outside of the developers' control[^1].

### How much do I need to know before I do X? The answer is, whatever amount of knowledge you have right now is enough

This is another stumbling block that many beginner game developers come across. They will put off implementing a feature so that they can take just one more course, one more online tutorial, watch one more video, and then they'll be ready to implement their game.

I'm particularly guilty of this, and know how insidious it can be.

To give you a more concrete example, let's say that you have been tasked with programming a Pong game from scratch.

Depending on what you know or don't know, there could be different approaches to take for this:

* If you're familiar with Unity's Physics system, it's a relatively simple endeavor. You can just use a couple of rigid bodies, colliders, apply forces and velocities, use a physics material for the ball's bounciness and that's it. A barebones Pong clone.
* But let's say that you're not familiar with Unity's collision system, you only know how to use Unity's transform components, so all you can get is an object's position and size.
  * But! That is enough to implement Pong, you could write a script that keeps track of the ball's position and size,and compares it with the paddle's position and size to check if there's a collision.
* Or perhaps you don't even know Unity, all you know is C++ and how to print to the console.
  * But that's also enough! You can use terminal trickery to print rows and columns of symbols to represent the ball, paddles, and playing area. That, along with the concept of a game loop, is enough to program a refreshing UI that responds to input.
* Or you don't even come from a Computer Science background or didn't take a C++ class, and only know Javascript?
  * No problem! You can use [Phaser](https://github.com/photonstorm/phaser) which uses JS as its main language and comes with both rendering and physics components.
* Can't even program? Absolutely no problem.
  * [Gamemaker](https://gamemaker.io/en) is a commercial game engine with a free version, and it has a no-code option.
  * [GDevelop](https://gdevelop.io/) is a free open-source game engine with a no-code option as well.

I believe you've figured out where I'm going with this, right?

### There are no failed projects, just piles of scrap waiting to be re-used

Most game developers usually have one or two (or 10,000) abandoned projects lying around somewhere. No sense in wasting them. If there is code in there like a pause System, re-use it. No sense in re-writing the same thing. Even if you remember exactly how to write it, copy it; if it's hard to adapt then re-iterate on it so it will be easier next time.

Perhaps you even have a workshop project[^2] that has several bits of code you can re-use.

### See a shiny thing? Take a shiny thing

Need a dialogue system? Locate an open-source one and repurpose it. Does it fulfill all your requirements? No? Does it meet over 50%? Yes? Then it's worth using that instead of creating a new one from scratch.

Inventory System? Find an open-source game on itch.io and adopt their system.

Need a first-person camera? Utilize a prebuilt asset to handle it[^3].

There are many brilliant game developers out there, undoubtedly more proficient than you or me. So, unless you have a particular reason, everything should be considered a candidate for using a prebuilt system. However, sensible exceptions do exist, such as: Don't use code you've merely copy-pasted as the backbone of your game (at least ensure you understand it, clean it up, and comment on it), and avoid using a module that's a decade old, with its author presumably lounging somewhere tropical, sipping Mai Tais with Elvis, Tupac, and Marilyn Monroe in a paparazzi-free paradise.

### When in doubt, copy

If you're uncertain about implementing a feature, find a game that has done something similar to what you want and imitate it.

By "copy," I mean the design aspects like control handling, camera views, and mechanics, rather than the art style, story, or characters.

For instance, how fast should the scroll be in our now forgotten hypothetical ROGUELIKE-RTS-MMORPG?

Instead of guessing, you could see how another RTS has managed it. Suppose you observe Age Of Empires II (an historically significant RTS), and discover that it allows users to control the speed of their cursor movement. You might even place your game side by side with AoEII and adjust your cursor until it feels equivalent. You'd be amazed at how many developers rely on simple, low-tech solutions like this to accomplish their goals.

### Parting Thoughts

So, what should you do after you've concluded your Chaos Goblin antics? Well, take a breather, make yourself a cuppa, and return to your code later.

After allowing your code to rest (under a damp towel if the weather is too dry), you should spruce it up a bit and share it. Yes! Share it, ideally with a senior developer, a colleague, a fellow student or, in the worst case, with an online community[^4].

Why are you sharing it? Because being a Chaos Goblin isn't about creating something durable or optimal; it's about building something that WORKS. It doesn't have to function perfectly or look beautiful, it just has to WORK. This type of development produces results, but results that are rarely immediately ready for production. Thus, consulting with someone to provide feedback is critically important.

Depending on the stage of your project, you might not have the time to implement this person's comments immediately. If that's the case, you should at least document those comments in the code[^5].

And that's it! You now possess the #1 technique used by professional game developers worldwide to solve problems.

I'd suggest it's time for a second cuppa, wouldn't you?

## Notes

[^0] - This is a surprisingly common phenomenom and it's denominated "The Denver Parable", for more information, refer to the following [scholarly article](https://xkcd.com/979).
[^1] - This is a bit of a generalization, and like most generalizations, it may not be as helpful as a thorough analysis of your project's requirements. However, it's a good rule of thumb to postpone optimization until it's genuinely needed. These days, optimizing video games is considerably less daunting than it used to be. Some game engine companies, like Unity, might even offer to assist you with complimentary consultations. After all, it's in their best interest for you to successfully launch your game.
[^2] - The workshop is one of the katas or practices I use to increase my understading of Unity. You can read more about it and other techniques [here](https://hackernoon.com/katas-for-unity-deepen-your-understanding-of-unity-or-any-other-game-engine).
[^3] - You can find a really good FPS controller package alongside other useful tools in this [article](https://hackernoon.com/5-unity-extensions-that-you-will-actually-use)
[^4] - This carries a caveat that approximately 95% of comments you'll receive online might be pointless, incomplete, out-of-date, or reflect the author's deeply personal beliefs, whatever they may be. Therefore, always approach such feedback with a degree of skepticism. Try to seek out the useful comments, disregard or eliminate the rest, and make a genuine effort to find someone with whom you can share your code.
[^5] - Different teams uphold different norms regarding where they maintain their code documentation, and you should adhere to that. However, generally, I'd advocate for the code's documentation to reside adjacent to the code itself. If that's not feasible, consider using a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) or its equivalent in your chosen code versioning system. If documentation can't be in the main repository, it should at least reside in the git submodule.
