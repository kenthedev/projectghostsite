---
title: Scorched Earth
layout: post
date: 2025-09-17
comments: false
image: /assets/images/sinkingbug.png
---
This summer’s been a real scorcher.  
  
And not just because of the weather. These last few months I’ve battling a mental heatwave: too many ideas, not enough time.

There’s an old X-Men comic that’s been in the back in my mind lately. It’s of Cyclops sharing that he had dozens of contingency plans in place, just in case something went sideways. I’ve always found that sort of thing amusing, cool even. But there’s something about that concept that’s been nagging at me. You could say I’m in that mode right now: planning, reevaluating goals, and realigning where and what I want to focus on.

I absolutely love brainstorming. Holding all these grandiose scenarios and plots in my head, bursting at the seems to be made real. It’s addictive. But what sucks about it is that I can’t magically make all those ideas appear overnight.

It’s so easy for things to sound great on paper. Lately, I’ve been learning to get a better sense of what’s actually possible, something that ironically hasn’t really been helped by how much more comfortable I’ve gotten with Unreal Engine. The more capable I feel technically, the more ideas flood in, but that doesn’t mean they’re all doable right now, if even necessary.

Which brings me back to the main thing I’ve been wrestling with: not letting myself get swayed by my own thoughts and ideas. It’s tough, though, because there’s a part of me that’s always wanting to do and know everything. But if I really want to move as quickly as I can, I have to know when to hit the brakes. And so that's what I did.  
  
The game saw an engine change from 5.3 to 5.5 to take advantage of some of the newer animation retargeting features. This went abysmally. I got stuck for a few weeks, unable to compile the project and desperately trying to figure out what went wrong. Thankfully, the issue ended up being tied to a tooling incompatibility between Unreal Engine 5.5 and Visual Studio Tools.  
  
Since then, I've been spending a lot of time converting my blueprints' parent classes to C++ as a multifaceted effort. Both to improve performance and get more comfortable working with C++ in Unreal.  
  
One of the largest changes was to the UI system. I had been primarily using UserWidget blueprints, but was running into challenges when needing to make changes across the whole game. Rather than repeating things, I opted into to invest time into setting up text styles and take better advantage of CommonUI. Any heads up displays or button prompts now adhere to a data-driven UI pipeline, as I've implemented a push/pull layer stack. The widget layers broken up into four layers, with widget template base classes in C++.  
  
I spent tons of time studying through [BenUI's guides over at unreal-garden](https://unreal-garden.com/tutorials/ui-cpp-uuserwidget/) and [Vince Petrelli's Frontend UI course](https://www.udemy.com/share/10doTD3@rI_63dCrHw0TEtDPuhGxZ9CLl_EYa4EKbZevOWARspaXIvwvc5mjZaxKcxcMIFpg/	), both of which informed much of my decision making through the process.  
  
My character controllers and logic have seen full rewrites in C++ along with other systems like Saving & Loading being stripped from Character classes to their own subsystems.  
  
In the long run, this has been an experience of trial and error. Lately though, I'm looking to seeing how much better I can get.