---
layout: post

title: Common problems 3D printing with PLA
subtitle: "lessons learned printing with PLA"
cover_image: blog-cover.jpg
excerpt: "This is an ongoing collection of lessons learned using PLA on 3D printers (specifically, the Lulzbot TAZ4). Hopefully my befuddlement, and eventual solutions, to some of the most common issues such as Heat Creep, Extruder Clogging, and Filament Leaking/Pooling will benefit others."
category: "3D Printing"
image: perils-of-pla.jpg

author:
  name: Joe Norton
  twitter: joenorton
  gplus: 104323171291289633724
  bio: "Founder & Chief Dreamer"
  image: jn.png
---  
Having problems printing with PLA? I know I've had my fair share (and will continue to have them, I am sure). Right now, as of this writing, I'm about 2 weeks into ownership of a Lulzbot TAZ4 3D Printer. It's a great machine, but not without it's challenges. There are things I've had to take apart, things I've had to clean with potent chemicals, or seal with thread tape, and even standard parts of the TAZ4 that I had to replace with improved versions. Definitely not a 'set it and forget it' type of deal (but hey, that's to be expected on the bleeding edge right?).

Now that I have 25+ prints under my belt - I feel theres a few things I can share here for the benefit of others. Hopefully my befuddlement, and eventual solutions to issues, will benefit others who are trying to figure out how to keep their new expensive toy running and making quality objects. Think of this post as a 'lessons learned' when printing with PLA on the Lulzbot TAZ4 (but it probably goes for most other 'consumer grade' 3D printers on the market as well).

> PLA printing requires modifications!!

The good printers can do PLA, ABS, and all kinds of other space age filaments. They advertise this quite heavily. What they don't tell you as openly is that actually using PLA is going to run into a few more quirks than ABS would, and in-fact the TAZ4 is not "out of the box" ready to print PLA (maybe a couple prints, but eventually you WILL run into issues unless you do certain upgrades/changes to your rig). In fact, if I were doing it all over again and buying my printer and initial batch of filament, I would just get ABS -- it may be less eco-friendly, but it also isn't going to have the _heat creep_ issues that you may encounter with PLA. All that said, I currently am printing all PLA - and have learned a few things about it that you may benefit from hearing!

**What makes PLA such a pain in the butt?**  
PLA has a lower melting temperature than ABS, and also has a higher viscosity when it is melted. PLA also holds onto, and conducts, heat more so than ABS. 

This all seems like random trivia, but what it means is that PLA is much more prone to 2 major issues:

1. __Filament Pooling / Leaking__   
PLA becomes so thin and runny when heated (more so than ABS) that it will seep out of tiny cracks and crevices that ABS won't. What this means is that if you haven't sealed your nozzle off with PFTE tape or high-temp thread seal then you can and should expect liquid PLA to flow 'upwards' thru the threads of your nozzle during your prints. This is the issue with my Budaschnozzle 2.0, the default extruder and nozzle for the Lulzbot TAZ4. 

__Fixing Filament Pooling__  
<a href="https://www.lulzbot.com/support/budaschnozzle-20-pla-solution">Lulzbot has shared a few solutions to this issue</a> - all of which involve taking apart your budaschnozzle and either applying PFTE tape or High-Temp Thread Locker.  

I personally haven't yet fixed this on my machine. It's not pretty having filament pooling, but it's not really having any kind of negative impact on my prints (that I know of).

2. __Heat Creep & Extruder Clogging__  
Since PLA conducts heat so well what happens is that heat travels up the filament. This is bad. The heat travels up out of the melting chamber and starts to 'cook' the filament above the extruder itself! This is particularly an issue when you are using temperatures too high (like above 185ish) and if you do not have adequate cooling of your extruder above the heating block. So.. what happens when that filament starts to cook is the heated filament starts to expand, and contort, and becomes very hard and brittle. Once this happens your extruder will not be able to push the filament into the melting chamber anymore. It just jams up. At that point, you are stuck - no more printing is going to happen until you open up that extruder assembly and perform surgery and manually get that cooked PLA filament out of there so that you can get back to melting plastic as usual.

__Symptoms of Heat Creep:__
* nothing coming out of extruder when you 'warm up' (usually a tiny bit oozes out the end as you come to temperature on the nozzle)
* nothing coming out of extruder when you run the extruder motor (you see the gear turning, but no filament comes out of the nozzle)
* filament being ground down by the hobbed bolt but not pushed/pulled by it (also note, there could be plastic filament all gummed up in the hobbed bolt too - it helps to clean it out when this happens)

> Fixing Heat Creep
I'm still trying to figure that out. Just when I thought I had a permanent fix to this, then I experienced another extruder clog. It's a bummer when you find your 3D Printer has been 'ghost printing' for the past hour, and you realize you will be spending the next 2 hours taking apart and fiddling with the extruder assembly before you can set up a new print. So I haven't PLA proofed the 3D Printer just yet, but I will tell you what I have done so far that has helped the heat creep breakdowns become less numerois.  

1. __STAY LOW-TEMP__  
When printing PLA it's very important not to run at too high a temperature. I preferred printing at 200 degrees, my prints were finishing well, however this was leading to heat creep and constant clogging issues. Now I try to stay between 180-185.

2. __ACTIVELY COOL ABOVE THE HEAT BLOCK__  
One issue with the TAZ4 is that the fan comes with a duct that is pointed directly at the nozzle, leaving the area above the heat block completely uncooled. Since we are using PLA, it is extremely important that we not let the heat from the extruder climb up the apparatus and start warping our filament above the melting chamber. What we want to do is focus a bit on the area above the heat block to help prevent the heat creep. 

To fix this on the TAZ4, you will want to replace the existing fan duct with <a href="http://www.thingiverse.com/thing:374906">this great 'dual' fan duct</a> created by another TAZ4 user. This duct will focus more cooling on the area above the heat block.

<a href="https://www.flickr.com/photos/126939770@N02/15252953945" title="dual-fan-duct by Joe Norton, on Flickr"><img src="https://farm4.staticflickr.com/3882/15252953945_d824131f9d_n.jpg" width="320" height="241" alt="dual-fan-duct"></a>

I have made one of these myself, it is an easy print and it self-taps with the original screws that come with the TAZ4. It works nicely. Much better at directing air above the heat block, and thus preventing heat creep to some degree.

Lastly, now that you have your new fan duct you will want to make sure you keep that fan running all the time!  

That's it. Hopefully with these tips you can keep heat creep to a minimum and keep that printer running!

__UPDATE (9/29):  Unfortunately, my problems persisted and I eventually ended up having to my extruder head replaced by the manufacturer! So far, Lulzbot support has been excellent!__