---
title: "Trying to fix a dehumidifier"
date: 2026-10-26T11:42:07.569Z
draft: false
---
This past weekend I spotted a dehumidifier on my local [Freecyle.org](https://freecycle.org/) page. It was listed as broken, and the owner didn't provide any more details on what "broken" actually meant. Any average scroller probably would have scrolled past, wondering why someone would give away something that doesn't work.

As an engineer by trade and a monthly volunteer at the local [Repair Café](https://www.repaircafe.org/en/), I couldn't help myself but wonder: what was actually broken? Is it a simple fix? To nobody's surprise, I was on my way to pick it up from the owner's porch the next day.

[image of whole unit]

So there it is. A HOMCOM 20L/Day 6000mL dehumidifier. I had actually been thinking of getting one, as now it's becoming a bit nippy in the UK, and it might probably help when drying clothes indoors. And this one cost over £100 when new! Lucky me (if it works...)!

Before even powering it on, I went for the first most obvious check: the fuse. After popping open the little compartment, I tested it by holding my finger on one side and tap around on my phone screen with the other side. My phone responded to the touches, meaning the fuse was okay. While replacing the fuse would've been an easy fix, I was almost looking forward to having a dive around the internal electronics. But, before dismantling the unit, I plugged it into the wall to see if it actually did work or how it was actually broken (something I have been guilty of forgetting to do at Repair Cafés).

[image of top screen turning on]

Success? Was the previous owner doing something wrong, or does it just magically work again? It's something I see often at Repair Cafés, where devices start magically working after being threatened with disassembly. Sort of like humans, I suppose. 

I decided to leave it running for over an hour in a room with damp washing. The display appeared to show a value which is probably the humidity; I had no way to check if the value was correct, but it seemed plausible. I switched between "DRY" mode, which was somehow best for drying clothes, and the standard dehumidify mode, which defaults to 40%RH. After over an hour, there was not a single drop of water collected. Time to open it up.

[images?]

By removing the screws around the frame, I was able to pry off the front plastic panel and a few plastic clips enjoyed it so much they decided to thank me by pinging under my desk, never to be seen again. 

[image of bare front]

Et voilà. I hadn't ever thought how a dehumidifier actually works, however after looking at the insides and consulting some YouTube videos it is surprisingly simple. The big black sphere at the bottom is the compressor; it uses refrigerant gas to perform cooling, which is key for dehumidification. We all know when you blow warm air on a cold surface it creates condensation. A dehumidifier does that at a large scale by cooling the heat-sink stack so much that the surrounding air forms condensation, even if the air is only 10°C. The condensation is then collected in a tank at the bottom of the unit, which must be emptied periodically.

[image of circuit board]

My first port of call is to have a rummage around the electronics to see if anything looks bad or if any connections are loose. Having a little feel around the components, nothing appears to be broken or falling off (note: **unplug the unit before doing any disassembly or fiddling**). Turning on the unit again doesn't present anything obvious on the electronics either.

After the unit is on for a minute or two, I hear a click and a low hum/rumble from the compressor and a few seconds later it clicks off again. Okay, sounds like a relay is in control. There are relays on the board, one of which connects the compressor to mains. To check if it's the controller board incorrectly switching off the compressor, I soldered the switching terminals together as a way to continuously run the compressor.

Upon reconnecting the unit to mains, the compressor turns on after a few minutes but shuts off again after a few seconds, just like before. A search of the compressor on the label quickly shows that it is [this](https://www.bossgoo.com/product-detail/r290-1-4hp-chest-freezer-refrigerator-64962443.html) model, using R290 refrigerant gas. Inside a little black box on the side is an overload protector, a starting relay, and potentially a capacitor. 

[image of compressor diagram and of the compressor in the unit]

That internal relay must be the one that is switching off the compressor before it can start properly working. I would love to get inside to check it out and maybe replace some components, but it is in such an awkward location I can't get to it. There is no way to remove the plastic housing around it without disassembling the whole refrigeration loop. Annoying.

Another common issue with refrigeration is that the internal refrigerant gas can slowly leak, leading to poor or even no refrigeration after some time. The previous owner said they have used it for almost two years without issue so maybe a slow leak could be the culprit. But surely if the gas in the loop was low, the compressor can still run without shutting off? 

Wrong. Maybe. The compressor gets warm during operation and the internet tells me it is normal. How warm for how normal? It could be an internal temperature switch that shuts off the power; is the temperature switch faulty or is the compressor actually overheating? In a way I hope it is the (inaccessible) temperature switch that is causing the issues, as the refrigerant gas can be quite expensive considering that new dehumidifiers aren't much more.

[comparison picture of R134a and R290 gases prices eBay]

The internet suggests that low refrigerant can not only cause poor performance, but also cause overheating in the compressor as the refrigerant plays a role in lubrication and cooling of the mechanical components.

Is it worth it?
