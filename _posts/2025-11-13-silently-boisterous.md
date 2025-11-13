---
title: Silently Boisterous
layout: post
date: 2025-11-13
comments: false
description: The work continues.
excerpt_separator: <!--more-->
---
The work continues.
<!--more-->

One of my favorite game series growing up was the "Dragon Quest" games. My introduction was with the ninth installment, "Sentinels of the Starry Skies". For those unfamiliar, these are classic adventure titles starring heroes seeking to go out to make the world a better place. And while I fell in love with the series protagonists for their nobility and general sense of do-gooding, I realized quite swiftly, I did NOT want to write that here, nor did it feel natural to me. I'm more interested in a protagonist that wants to do good amidst dysfunction, while not being part of an entirely benevolent world. Something gritty or grimy even. Like a slug pulling itself through a drain pipe. The goal is to make something harmoniously messy. It's what I like.  
  
Interestingly enough, writing this story has required me to revaluate how I perceive and interpret other work too. What do I like? What do I dislike? How do I think this could've been done better? What made it worse? All leading to a healthy dose of evaluation and refinement. The treatments so far have seen more than their fair share of revisions and edits. And I rest assured, that they'll continue to as the project progresses. And in making changes, I soon after discovered the importance of having a system in place that's **less annoying to change.**  
  
So what better to do in a state of increased encumbrance then to drop what's unnecessary. I swiftly got to work on replacing the old setup with a new, revamped one.  
  
This entry's going to be a bit more technical than previous ones. Below I'll run through an example of some of the ongoing changes.  
  
**Old Setup:**

In my original setup, each stat was a plain float stored in a TMap<TEnumAsByte<EStat>, float>, and behavior for each stat (like health reduction, focus decay, or regeneration) was handled by hardcoded, individual functions such as ReduceHealth, ReduceStamina, and RegenStamina. Clamping, delegate updates, and decay logic were implemented separately for each stat, resulting in repetitive code. Modifiers and temporary buffs were not supported, and any new stat or mechanic required adding new functions and switch statements. Enums were unscoped “legacy” types, which meant less type safety and occasionally awkward handling between C++ and Blueprints. Needless to say, this was quickly becoming a large time sink as more features were added to the game.

**New Setup:**

The new stat system is data-driven and generic. Stats are now strongly typed using a enum class EStat : uint8, which ensures type safety and cleaner syntax. All stats changes, including reductions, regeneration, and curve-based adjustments, go through generic functions such as SetStat(), AddToStat(), and RegenStat(), which automatically handle clamping, delegates, and modifiers. The FStatModifier struct allows for temporary buffs/debuffs with flat or percentage changes and durations, and regeneration or decay can be controlled with curves for smooth, time-based effects. Cooldowns for resource depletion (like Focus) are handled generically per stat, eliminating the need for one-off functions. These changes are intended to allow the system to be scalable, maintainable, and fully Blueprint & C++ compatible, enabling me to add new stats, modifiers, and mechanics without duplicating code.  
  
I've resolved to continue to making these sorts of improvements to spare myself more pain both now and later on.

![](/assets/images/Pews.jpg)

In the meantime, stay on the look out for some smaller narrative-driven tie-ins on the road to Gunmetal Ghost.
