---
layout: post

title: Adding A Second Fan Targeting Heat Creep
subtitle: "how I stopped PLA extruder jams by adding a 2nd fan"
cover_image: blog-cover.jpg
excerpt: "In order to finally stop extruder jams caused by heat creep with PLA I added a 2nd fan; here's how."
category: "3D Printing"
image: 2nd-fan-mounted.png

author_name: Joe Norton
---     
There are a couple ways to integrate a 2nd fan into your 3D printing system. This is how I did it.     

First, you need to get a second fan; you can get them from many places online. Just be sensitive to the voltage needs of your fan. I went with a 24V, because I wanted to move some serious air -- but that also means you need to supply that much more power.

Now, it's time to figure out how to power it and make it run. You always could plug this into your main power supply for the 3d printer; the TAZ4 comes with space for these kinds of additions. Personally, I decided to NOT plug it into my 3D printer controller for power, and instead I choose to run that fan on it's own separate power supply.

I had a 19V power adapter laying around so I used that instead. It does not allow the fan to go it's fastest possible speed; it is perhaps around 80% of it's potential speed. This has worked good so far - especially since I keep it running alot, it feels like it makes sense for it not to be hauling ass all the time but to run at a slightly less than full capacity speed. Note: I first tested a 12V adapter, and the fan was not moving fast enough to be useful. It didn't pass the 'tissue test', so I upgraded it to the 19V supply and that did much better with the 'tissue test'. (Tissue test: if you put a tissue in front of the fan while running full blast, does it actually move the tissue around?)  

I like this particular setup because I can keep that fan running at it's top speed (based on our power supply) for the entire print very easily. I don't need to make any changes to my 3d printer settings, or to my print settings, in order to add in extra gcode into my prints to make that fan run. It just runs when I have it plugged it.  

Next, we need a new fan mount for this 'heat creep fan'. Due to the positioning of the budaschnozzle, the leftside of the extruder has less space than the right does wrt the fan so you will need a fan mount that takes this into account.  

<a href="http://www.thingiverse.com/thing:368303" target="_blank"><img src="/images/heat-creep-fan-mount.png" style="float:right;"></a>I looked at a bunch on thingiverse, printed a few, and finally settled on this one: <a href="http://www.thingiverse.com/thing:368303" target="_blank">Fan shroud for Lulzbot TAZ 4 hotend</a>  (Seen on right)

It prints easily, self-taps, and best of all - is a good design for the task.   

Since I added my 2nd fan I have not had any extruder jams. I will admit, on occasion I hear grinding -- but so far so good on the jams. The grinding always stops and works itself out without any kind of issue or intervention on my part -- and most importantly, I am not seeing the finish issues I had with the heat creep going on. I used to see lots of streaking, and patchiness in my print finishes, but that is gone for the moment.  

So far, that's my best advice for preventing heat creep - get a 2nd fan!