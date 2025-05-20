---
title: Rusted Pride
layout: post
date: 2025-04-29
comments: false
---
Hello again.

Life just seems to get busier and busier—much like it will be for our future operatives. But before that can happen, there's still a lot of work ahead.

This past month has been heavy on programming. After finishing some C++ game programming coursework and a few forays into side projects, I'm feeling much more confident in using C++ within Unreal.

I've begun converting my base character scripts from Blueprints to C++. While I've gained a new appreciation for Blueprints, they're becoming less practical as the systems grow more complex.

I'm hoping this early groundwork pays off later, when the game logic inevitably becomes more intricate. Ideally, I'll spend more time iterating and testing with less time untangling. I also want to lean more into Unreal's component-based design, breaking off non-specific functionality from the base character into smaller, more modular pieces. Right now, the base character handles everything—from Health and Movement to Combat features like Flinching and Dodging. That's been fine so far, but not every character will need all of that.

Enemy aggression is another area I've been experimenting with. It's tricky to strike the right balance—making enemies feel assertive without being unfair. This will undoubtedly need continual tweaking as more enemy types are added. Narratively, figuring how enemy categorization has been a task more fun than I anticipated.

On another note, learning about **AnimationNotifies** has been an exceptional asset. Both the Deluge enemy and the player character use notifies and montages to trigger animation-based events, which has streamlined a lot of behavior syncing.

![Attack Montages on Animation Graph](/assets/images/deluge_attack_montage_an.png)

Looking ahead, I want to expand this system with a hitbox visualization tool—ideally one that's adjustable in the animation preview itself. Right now, I use notifies to set a hitbox's location, radius, and optionally attach it to a skeletal bone. Since the attack animations can vary so much, it would be great to tweak these values without having to jump into a full playtest every time—especially for minor adjustments.