---
layout: post
title: Your Corpse Is A Container
---

A huge part of RPGs revolves around killing monsters and collecting loot. Skyrim is no different and you will spend a lot of time looting corpses. When it comes to handling corpses in RPGs, or any game for that matter, there is a simple trick you should take into consideration. Skyrim actually reveals this trick of how its underlying game system handles looting so let’s take a look:

###Fox is Empty###
Basically when you kill something in Skyrim it turns into a treasure chest. Don’t believe me, try killing something, take all the loot and you are presented with “X is Empty”. This is especially funny when you kill an animal or anything that was previously living. You would think that the developers would have different language for living vs inanimate objects but they don’t. So now that we know this track we can use the same simple mechanic to help you with making your own looting system. The key is to move any drop/pickup look logic inside of your monster or the classes these monsters extend from and place that logic in what I call a “corpse chests”.

###Spawning Corpse Treasure Chests###
When the player kills something, simply spawn a new instance of treasure chest after the death animation at the exact same place where the entity dies. These treasure chests basically look like the corpse of what you killed but act exactly like a normal treasure chest. One of the best examples of this happening in Skyrim was after I killed a dragon in a town the left only to find that every time I returned to the same town a dragon corpse would fall from the sky containing all the loot I stored inside of it. I was even able to put items too heavy to carry back into the dragon corpse treasure chest.

In the end, this is a common technique in RPGs and can save you from having to have loot distribution/management logic in your monster entities and instead can simply pass off any rewarded items to the corpse treasure chest. Plus there are optimization benefits from removing a entity with a lot of logic and replacing it with something that has a much smaller set of functionality.