---
title: "Repairing an abandoned HD TV"
date: 2017-04-16
excerpt: "One man's trash is another man's treasure"
---

Imagine my surprise when I find a 42" TV in the box of its replacement, sitting right by my apartment's dumpster.

Curiosity having gotten the better of me, I lug that beast into my apartment.

I promptly plug it in - and was not surprised when it didn't work. But I was not deterred.

As a Biomedical Engineering graduate, I'm no stranger to working with circuits, having taken three electronics courses, with a whole lot of labwork. I'm also no stranger to soldering.

The TV would periodically screech - about once every two seconds. To my ears, it sounded like there was a problem in the power supply.

<figure class="align-center">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/televisionRepair/tv-floor.jpg" alt="Back cover removed from the TV">
  <figcaption>Back cover removed from the TV</figcaption>
</figure> 

I take the back cover off the TV, and peer into where the logic and power supply boards sit.

<figure class="half">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/televisionRepair/tv-psu-board.jpg" alt="The power supply board">
	<img src="{{ site.url }}{{ site.baseurl }}/assets/images/televisionRepair/tv-controller-board.jpg" alt="The logic board">
  <figcaption>The boards in question</figcaption>
</figure> 

I've previously had an LCD monitor go bad on me, and the fix was to replace the capacitors in the power supply, which had started to swell. So I take the same approach.

I don't see any visibly swelling capacitors, so I unsolder one leg of each capacitor, and test their capacitance. Unfortunately for me, the farad readings were accurate.

I plugged the PSU board back in, and listen again, more intently, for where the screeching was coming from.

I was able to trace it to one transformer, the one responsible for downconverting high to low voltage, and providing power to the low voltage circuit.

That was worrying, because it meant that something was shorted on the low voltage circuit.

When I disconnected the ribbon cable connecting the PSU to the logic board, the issue stopped occuring... which, is fair, because now there's nothing the power supply needs to power.

I proceeded to unsolder a leg of each diode on the PSU board just to check that they are working properly - which they were.

At that point, I knew the problem was on the logic board.

It would be difficult to pinpoint the problem on the logic board, because so many components are surface mounted, and very tiny.

Luckily, I found a schematic online for a similar model TV. It turns out that the logic boards between many TVs aren't that different.

I looked for any connections to ground, and looked at components connected near the ground.

I was eventually able to trace the problem to one surface mounted capacitor, part of a signal filtering circuit, which had shorted.

<figure class="align-center">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/televisionRepair/tv-smt-capacitor.jpg" alt="The shorted SMT capacitor">
  <figcaption>The issue was this problem child of a capacitor</figcaption>
</figure>

I was able to acquire a replacement capacitor, 50 nanofarads. It was too small to solder with my personal soldering iron, but thankfully, there is an electronics lab at work.

After placing the newly fixed logic board and the PSU back into the TV and hooking everything up...

<figure class="align-center">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/televisionRepair/tv-working.jpg" alt="The tv is fixed!">
  <figcaption>Guess who's got a brand new tv?</figcaption>
</figure>

The screen lit up. The last test was to connect my laptop to the TV with HDMI to test that the logic board still worked, and that sound would be channeled from my laptop to the TV.

To my relief, everything worked fine. The only with this giant TV was this one, tiny thing, practically indistinguishable from a grain of coarse sand.

In the end, I discovered that this TV was a Black Friday model from two years ago, sold at the price of $250.

It's amazing what people will throw away. However, I cannot blame them, because our consumer culture practically encourages such a thing.


