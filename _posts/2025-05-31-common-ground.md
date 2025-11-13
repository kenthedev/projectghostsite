---
title: Common Ground
layout: post
date: 2025-05-31
comments: false
excerpt_separator: <!--more-->
---
Lots of fighting with Common UI...
<!--more-->

Using a gamepad with Unreal's Enhanced Input Actions has been relatively smooth sailing for the most part, but adding Keyboard & Mouse controls has been grating to say the least.  
  
Ran into a nasty 'Assertion failed' bug with the CommonUISubsystem that's causing a crash. So far I've had minimal luck with determining its exact cause. Wouldn't hurt to spend more time cleaning up the UI, now that I can do it more sensibly.  
  
On the brighter side, I'm feeling a lot better about how the story's progressing. I've gotten a stronger idea of the exact mood and atmosphere I'm wanting for the story. Not planning to go full splatterpunk with the writing, but I don't want to shy away from including murkier and grimy parts. This is still an action-*horror* game mind you.  
  
My experiments with the visuals have started shaping up nicely.

<p style="text-align: center"><br><img src="/assets/images/Atmosphere.png" alt="Survival Horror Atmosphere"></p>

Portions of the game will involve elements of classic survival horror games. Think fixed cameras, tank controls, puzzle solving, hiding...The goal is to offer a different type of intensity than our standard rescue ops would permit.  
  
I've learned a ton about lighting and way more about cameras than I ever expected to. My work has always given me a new interest in tech art and I may have went down a few rabbit holes into the world of shader programming. It'll never stop blowing my mind just how much you can do with math.  
  
Now that I've cleaned up saving and loading, I've moved back to continuing work on the dialogue system too. It's built off of the Defender Animated Dialogue System and is in charge of handling calls to push dialogue widgets on and off screen, keeping track of their references, and setting input behavior between game and UI modes.

<p style="text-align: center"><img src="/assets/images/Dialogue.png"></p>

There's a ton that goes into something like a dialogue system. Showing speaker names, portraits, skipping text, branching choices, and so much more. I've been expanding the system with a radio call style of messaging for the player to hear additional info and conversations from teammates while on missions. I really appreciated how much personality the characters gained in Dynasty Warriors: Gundam and Persona 5 Royal, just through the addition of field calls and Metaverse conversations. It's an minimally intrusive way to engage players with the feelings and emotions of the characters, while making the world feel more alive.

<p style="text-align: center"><img src="/assets/images/MementosConvo.png"></p>

Never thought I'd be this excited by being able to make custom UI prompt messages, but I guess that's where we are now.

![](/assets/images/SaveDataMessage.png)
