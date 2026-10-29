---
title: "Larper-2 \"Teddyy\" Rocket Motor"
author: "Karaya1__."
description: "Largest amateur KNSB rocket motor in all of Indonesia produced by an individual. This is a J-Class rocket motor producing around 1068 Ns of impulse and 710 Newtons of thrust. "
created_at: "2026-08-31"
---

# 2026-10-29: Nozzle Revision

**Total time spent: 0.4 hours**

JLCCNC cannot manufacture such a complex nozzle. Looking at rocketry forums, the original aluminium and steel nozzle should work and I will just state I cannot get it done. The original reason why they believe a steel only nozzle closure is safer is because they never tested such a combo. I guess I’ll be their first lol.

![Screenshot_2026-10-20_193200.png](https://cdn.hackclub.com/01a18731-6872-7d8e-b951-473639457b20/Screenshot_2026-10-20_193200.png)

# 2026-10-28: Meeting with BRIN and the Larper-2 test variant

**Total time spent: 4 hours**

After a long cat and mouse game with the Indonesian government, I finally had a Zoom meeting with the body of rocket research. Here we mainly discussed about the characteristics of the rocket motor such as the simulated data, construction material, and the experimental PET-CF17 liner. 

The main takeaway from this meeting is that they want me to make the entire nozzle closure one piece and to make it out of 304 stainless steel. They said before I begin experimenting with dual-material nozzles and add complexity to make the rocket motor lightweight, I should make a test nozzle first to confirm that my geometry and such work. So, in order to get technical data for the time being, I made the nozzle closure out of 304 stainless steel.

![Screenshot_2026-10-28_180027.png](https://cdn.hackclub.com/01a1822d-150a-7a20-a5a8-36fea75a64cd/Screenshot_2026-10-28_180027.png)

Here is a picture of the Zoom meeting where I am with my physics teacher (the goat).

![Screenshot_2026-10-27_131210.png](https://cdn.hackclub.com/01a1822d-f6ff-7edd-b38e-2fdad071a0e6/Screenshot_2026-10-27_131210.png)


# 2026-10-20: Manufacturing Nightmare

**Total time spent: 10 hours**

I tried reaching out to countless CNC manufacturers in Indonesia and it has been genuine hell. It feels like they're allergic to getting new companies. The people that sell aluminium pipes as well. I just can’t seem to find anyone in Indonesia that will manufacture my parts. You might be asking, why not just outsource to China? The answer is tax. Forge won’t cover the cost of import taxes so I need to pay it myself and I’ve been trying everything to avoid it but alas with my current deadline for a competition, I decided to just spend the extra cash. I have a money reserve with about 200 CAD to cover for parts but I guess I’ll just use it for this. The estimated tax is around 114 USD.

Both the aluminium pipe and machined parts are coming from China. Additionally, I decided to swap my graphite insert for a steel one temporarily because I do not have the time to manufacture a graphite one in the 3 weeks I have. This is only temporary and any future firings for this motor will use a graphite one. Finally after 3 weeks of searching for a manufacturer, I can finally submit my project to Forge.

This has genuinely led me down a path of pure frustration and I am so glad this is soon to be over.

![Screenshot_2026-10-20_192847.png](https://cdn.hackclub.com/01a1594a-8be2-7cc6-ace4-0bd59a6f8f91/Screenshot_2026-10-20_192847.png)

![Screenshot_2026-10-20_193200.png](https://cdn.hackclub.com/01a1594c-7126-78bc-adb7-33696da6ae5d/Screenshot_2026-10-20_193200.png)

# 2026-10-04: Larper-2 v2

**Total time spent: 10 hours**

So my local CNC machinist says he can’t machine a non standard internal diameter for a rocket motor. Now I’m sure if you’re reading this and you have any basic knowledge with amateur rocketry, you’re usually supposed to use an aluminium 6061-T6 pipe and then drill holes into it for the casing. The only problem with this is that in Indonesia, I can’t seem to find pipes of this aluminium type, only raw metal blocks. This is why my rocket motors use a weird diameter, it allows for really interesting experimentation. 

My CNC machinist told me that the machines they operate don’t reliably produce an even internal diameter meaning the o-rings might not seal. He asked me if he could shrink the internal diameter of the casing to 60 mm instead of my irregular 68.5 mm as they somehow have 60 mm 6061-T6 pipes. I hesitated mainly because I really didn’t want to go through the whole calculation process again and I am behind schedule on this project but alas I spent the entire day recalculating the whole rocket motor with this new constraint. Alongside recalculation, I decided to optimize a few parts that plagued the previous design. I was surprised to see that this smaller diameter made my rocket motor better in many ways. Additionally, I didn’t need to spend too much time fixing as all I had to do was edit a few numbers in OnShape. 

![Screenshot_2026-10-04_150550.png](https://cdn.hackclub.com/01a10625-ad1c-71a9-b3d6-a12ba9cf38fa/Screenshot_2026-10-04_150550.png)

Calculation was pretty straightforward, basically doing the same thing as shown in page 1-3 but this time I was surprised to see that a 2.5:1 ratio worked as well. For future rocket motors, I will definitely use this as my starting point.

The output really shocked me. I gained 4 seconds in Isp (133 seconds) which is insane for KNSB. The max theoretical Isp of KNSB is around 155 seconds (at 1000 psi) but in reality, it lands around 129 which my two other designs showcase. Even though 4 seconds may not seem like much, it is actually really good. Though, this is simulated data and the real data will still probably put it around 129 seconds sadly. But still, this is quite cool. 

My hypothesis for why the efficiency is high is due to the balance of internal chamber pressure. Looking at design attempt 1, we can see an average PSI of 688 and a peak PSI of 921. Looking at the Larper-2 v1, we can see an average PSI of 633 and a peak PSI of 734. Both motors have an Isp of around 128-129 seconds most likely due to their internal pressure. An important piece of information is that KNSB burns most efficiently at 1000 PSI. The following paragraph is only an  assumption and is not backed with math but rather just observation.

Design attempt 1 has too much surface area and leads to a massive pressure spike. This made the pressure non uniform leading to a relatively low average pressure but really high thrust and a low burn time (1.47 seconds). Larper-2 v1 is thick in the diameter meaning most of the propellant is not really that exposed. This leads to a longer burn time but since there isn’t a lot of stuff burning at once, there is a longer burn time (2.13 seconds) and a low average pressure. The v2 is efficient most likely because it balances the best of both worlds. There is just enough surface area to maintain a relatively high average pressure of 837 PSI but not enough for all the propellant to just burn all at once really quickly leading to stable pressures and thrust. This stable high pressure leads to higher efficiency. This is most visible in the graphs, design attempt 1 peaks really aggressively, v1 tapers off, and v2 has a very stable and smooth graph.

Additionally, v2 has superior thrust compared to v1 with a peak thrust of around 700 ish Newtons. This can also be seen in the total impulse value being higher at 1068 Ns.

Another main difference in the v2 is the nozzle design. I decided to change the convergence half angle to 40 degrees as opposed to 30 degrees. I did this to shrink the total length of the nozzle closure to remove as much dead weight as possible. It also allows me to create a simple graphite insert. Additionally the graphite insert has a small amount of outer material removed. Watching a video made by AeroPropulsions, he explained that aluminium and graphite expand at different rates when exposed to heat. Adding in empty space allows the aluminium to expand without pushing the insert upwards.

![Screenshot_2026-10-04_155000.png](https://cdn.hackclub.com/01a10625-efef-7cdd-862e-520b09a29a91/Screenshot_2026-10-04_155000.png)

Other than this, there isn’t really any significant change in the other parts besides size. Here is the full cross-sectional view of the new and improved Larper-2 v2.

![Screenshot_2026-10-04_154944.png](https://cdn.hackclub.com/01a10626-28f1-7f4a-8108-b79a43adfdb1/Screenshot_2026-10-04_154944.png)

Finally, here are the safety calculations for the new design as well.

![IMG_2545.JPG](https://cdn.hackclub.com/01a10626-652b-7a92-a9ac-732795edac62/IMG_2545.JPG)
![IMG_2539.JPG](https://cdn.hackclub.com/01a10626-63e2-71b9-9cea-b1e8207c99f0/IMG_2539.JPG)
![IMG_2541.JPG](https://cdn.hackclub.com/01a10626-62af-73e0-8890-495dadf2e3d6/IMG_2541.JPG)
![IMG_2542.JPG](https://cdn.hackclub.com/01a10626-6440-7f21-9cf2-78265d017ba8/IMG_2542.JPG)
![IMG_2543.JPG](https://cdn.hackclub.com/01a10626-626c-7795-8563-d95ae6519b14/IMG_2543.JPG)
![IMG_2544.JPG](https://cdn.hackclub.com/01a10626-62d4-79fc-9f46-611353d123c8/IMG_2544.JPG)

# 2026-09-08: Rocket Motor Design Final

**Total time spent: 5 hours**

Nothing too interesting happened here besides just streamlining the design and removing numbers with more than 3 decimal places. I also simplified the geometry of the KNSB grains making them ever so slightly longer and making the core ever so slightly smaller. Turned the diameter from 76.3 to 76.5 mm and the core from 22.2 to 20 mm. This somehow increased efficiency by 0.7-0.8 seconds, and increased burn time to 2.13 seconds only at the cost of slightly lowering thrust from 620 ish Newtons to 580. 

![Screenshot_2026-09-07_184648.png](https://cdn.hackclub.com/01a07ff1-5544-71bd-8366-45d381dcd84d/Screenshot_2026-09-07_184648.png)

In terms of the actual, all I did was simply remove some material around the bulkhead and nozzle screws. Reading the paper, I saw that if the thickness is below 2 times the screw major diameter I needed to compensate for that by having a large safety factor. Considering the thickness of the closures are much larger than the casing, I still maintained a safety factor of 8 for both closures while removing around 20-30% material. Here are the final completed drawings for every part except for the graphite insert.

![Screenshot_2026-09-08_143319.png](https://cdn.hackclub.com/01a07ff1-98b4-711c-9867-c441462c78d1/Screenshot_2026-09-08_143319.png)

![Screenshot_2026-09-08_143256.png](https://cdn.hackclub.com/01a07ff1-b5ac-73a1-bd7e-796d8491c88b/Screenshot_2026-09-08_143256.png)

![Screenshot_2026-09-08_143233.png](https://cdn.hackclub.com/01a07ff1-cb26-7a6b-a915-6e451967f2be/Screenshot_2026-09-08_143233.png)

# 2026-09-07: Rocket Motor Optimization (Safety Correction)

**Total time spent: 0.3 hours**

I realised just why the safety factor for the nozzle and the bulkhead is so high, it’s the wrong formula. The paper I’m using to calculate these safety factors has a unique closure design which is incompatible with my design. I decided to use the casing shear and bearing formulas, simply changing the thickness of the material to how deep the screw inserts into the closure. This method gives me MUCH more realistic results.

![Screenshot_2026-10-04_160349.png](https://cdn.hackclub.com/01a10628-15b1-7ec4-8325-1017dda9c9ca/Screenshot_2026-10-04_160349.png)

I already began optimizing the design of the bulkhead and decided to confirm my measurements. I noticed that following the formula from the paper, a thickness of 6 mm would give me a safety factor of 12. This is physically impossible because the screw itself is 6 mm in diameter. I immediately decided to use my own method.

![Screenshot_2026-10-04_160356.png](https://cdn.hackclub.com/01a10628-4de7-7761-aeec-9df779bbbe8d/Screenshot_2026-10-04_160356.png)

Here I did a test calculation of the bulkhead using the bearing and shearing formula. This gave me much more realistic results, and only possible results. Now I can properly optimize this rocket motor.

# 2026-09-07: Rocket Motor Optimization (Safety)

**Total time spent: 8 hours**

To ensure that the rocket motor will not choose to become an explosive device rather than a propulsion device, we must make sure that the points that experience high stress will withstand the stress. These points are where the screws hold the casing and closures in place, with these screws being subjected to around 115 MPa of pressure. Safety calculations are also important to optimize the design of the rocket motor by showing parts that may have too much material that it’s useless. 

In these calculations, a safety factor of 2-3 is a good number to aim for but considering strength reduces when temperatures are increased (especially for aluminium), I decided to aim for a safety factor of 5-6 on aluminium parts to ensure that even if the aluminium reaches 100℃ , it should still hold and also because this is my first ever high-power rocket motor.

A description of the calculations is provided below the image.

![Screenshot_2026-09-07_161612.png](https://cdn.hackclub.com/01a07b28-85e0-798d-b69c-e1d4b5f822ce/Screenshot_2026-09-07_161612.png)

Here I am calculating the shear strength of each M6x14 304 steel screw and then determining the safety factor. Here, I got a safety factor of 3.58 which is more than enough to hold. Considering this is steel and not aluminium, it has far better thermal resistance than aluminium. At 100℃ , steel only loses 7-8% of UTS (ultimate tensile strength) while aluminium loses 50-53%. 

![Screenshot_2026-09-07_161620.png](https://cdn.hackclub.com/01a07b29-9198-7c09-bc7b-889335437784/Screenshot_2026-09-07_161620.png)

Here I am calculating the casing tear-out safety factor. Considering my bolt holes have about 1.2 cm of aluminium on the edges and a thickness of 2.5 mm, we get a safety factor of about 5.7, which is right in my wanted range. Even if the casing reaches 100℃, it should still hold.

![Screenshot_2026-09-07_161627.png](https://cdn.hackclub.com/01a07b2a-e252-7752-93ed-33e4970318ba/Screenshot_2026-09-07_161627.png)

Here, I am calculating the point of deformation or the max tensile strength of the screw holes. Later this same formula will be used to determine the yield strength of the holes in the aft and forward closure. Inputting the numbers, I get a safety factor of 5.97 which is well within my wanted range.

![Screenshot_2026-09-07_161633.png](https://cdn.hackclub.com/01a07b29-e384-7aac-a4e5-77a94db5ebc4/Screenshot_2026-09-07_161633.png)

![Screenshot_2026-09-07_161641.png](https://cdn.hackclub.com/01a07b29-f13a-7833-8f44-af0580698375/Screenshot_2026-09-07_161641.png)

Here I am calculating the bearing capacity of where the graphite insert pushes on the aluminium housing. Now I’m sure this isn’t a smart decision, but I’m not called HighCortisolRocketry for no reason. If you see in the finished nozzle, there are two primary points of contact near the throat. This calculation only covers the one with a larger surface area (the furthest one down). Considering the safety factor is well above 6, my assumption is that for the smaller lip, it would have a safety factor 10-20% lower than the larger one due to it having a surface area around 19% smaller. Hi, this is me after lunch. I decided to actually run the calculations because I was imagining my motor exploding due to this and I’m honestly surprised how spot on my assumption was. It was around 13% weaker, and still within my safety margin.

![Screenshot_2026-09-07_161647.png](https://cdn.hackclub.com/01a07b2b-9acd-7c97-97e0-2a048cb27e53/Screenshot_2026-09-07_161647.png)

Here I am calculating the yield strength of the bulkhead. The bulkhead experiences a lot of pressure during the burn, really angry and stubborn pressure that pushes. This calculation makes sure that the bulkhead can withstand that push. This is not about the screw holes but rather the bulkhead as a whole. Just by looking at the bulkhead and how thick it is, I was already pretty certain it was not gonna deform and my calculations confirm it. A 31.8 safety factor, honestly way too much but this will be fixed later in the optimization stage. I now know I can remove quite a bit of material without worrying.

![Screenshot_2026-09-07_161653.png](https://cdn.hackclub.com/01a07b2b-d553-7299-970a-a0191031cce7/Screenshot_2026-09-07_161653.png)

Here, I am calculating the yield strength of the bulkhead screw holes. Now as you can see, the safety factor is far too large but just as before, it will be fixed later.

![Screenshot_2026-09-07_161659.png](https://cdn.hackclub.com/01a07b2c-00c1-74fe-83b6-ead3b587f615/Screenshot_2026-09-07_161659.png)

Here, I am calculating the yield strength of the nozzle screw holes. Now as you can see, the safety factor is far too large but just as before, it will be fixed later.

# 2026-09-07: Rocket Motor Designing (Liner)

**Total time spent: 0.2 hours**

In terms of the liner, the thickness is currently just a wild guess based on one crude test with a completely different goal. This will be updated soon when I conduct proper controlled tests on the liner material itself to ensure that 3D printing a liner will not cause my motor to CATO. The tests will be simple burn tests to ensure it can actually insulate the casing and bending tests to ensure structural integrity when exposed to hot flames. I’ll also consider adding a small layer of high temperature epoxy for more charring and structure. Currently, it has a thickness of 2.5 mm.

![Screenshot_2026-09-07_120223.png](https://cdn.hackclub.com/01a1062a-4789-719c-9f84-a96993bfb538/Screenshot_2026-09-07_120223.png)

# 2026-09-06: Rocket Motor Designing (Bulkhead)

**Total time spent: 1.1 hours**

Just like the casing, this part is relatively simple with it only needing a few complexities around the O-ring and liner sleeve. Also like the casing, the current dimensions are just assumptions based on my research on amateur rocket motors. These will be properly adjusted during the safety calculations.

![Screenshot_2026-09-06_215100.png](https://cdn.hackclub.com/01a10629-f518-7d4a-8d34-b85e6426439d/Screenshot_2026-09-06_215100.png)

# 2026-09-06: Rocket Motor Designing (Casing)

**Total time spent: 1 hour**

This part is relatively simple with it basically being a glorified aluminium pipe. I decided to use a thicker 2.5 mm wall instead of the usual 1.5 - 2 mm used in amateur rocketry simply because I wanted to be extra safe in terms of pressure containment and shear strength on the screws. Most of the values here are honestly just eye-balled based on my research. I will do the safety calculations afterwards. The reason I do safety after is because all the calculations need to have an assumed value as you’ll soon see. 

![Screenshot_2026-10-04_160542.png](https://cdn.hackclub.com/01a10629-890e-7715-8636-806311900b1e/Screenshot_2026-10-04_160542.png)

# 2026-09-05: Rocket Motor Designing (Nozzle)

**Total time spent: 9 hours**

Now that I have all the dimensions I decided to design everything in OnShape to have a finished rocket motor design. I started working on the nozzle because I believe it is the coolest part of the rocket motor. At first I was simply going to recreate what I did on the Larper-1 rocket motor which uses 303 stainless steel as the nozzle. Even though 303 steel is considerably heavy I really did not care about performance. I cared mainly about learning the fundamentals of amateur rocketry and maximum safety and simplicity. 

The problem with using steel on the nozzle with this rocket motor is the sheer size of the nozzle block would make using steel stupid. If I were to only use steel, the nozzle itself would have a mass of 620 grams which is not ideal if I want to maximise performance on this rocket. I decided to do a similar nozzle method used on AeroPropulsion’s MEGAx rocket motor where he used a graphite for the convergent and throat while the main housing was made of 6061 aluminum. This brought down the total mass down to 292 grams, a whopping 212% reduction. After this decision, I made multiple iterations where I was trying to find the best ratio of graphite to aluminum.

![Screenshot_2026-09-05_212709.png](https://cdn.hackclub.com/01a071f7-b794-7c73-830c-c02022efa8cb/Screenshot_2026-09-05_212709.png)

![Screenshot_2026-09-05_212719.png](https://cdn.hackclub.com/01a071f7-c775-71e6-b688-dfba4a4bdcc9/Screenshot_2026-09-05_212719.png)

# 2026-09-05: Rocket Motor Design Attempt 1.5 and 2

**Total time spent: 5 hours**

From attempt 1, it can be concluded that I need to increase the diameter of the rocket motor to ensure the spread of the propellant is horizontal rather than vertical. Looking at local suppliers, all I could find was an aluminium pipe with an outer diameter of 76.2mm. So I tried using this diameter but the problem was, it was a bit too thick. It would give me a L/D ratio of 2.3:1 which is way  too small. I tried again but to no avail, it gave the exact same problem. This would lead attempt 1.5 to another failure.

![Screenshot_2026-10-04_160709.png](https://cdn.hackclub.com/01a1062a-fe62-765d-a78e-56c3533194fa/Screenshot_2026-10-04_160709.png)

So then I decided it would be a better idea to find a pipe outside of Indonesia to get more specific dimensions. Eventually I landed on a Chinese company called ZZLSteel that could get me custom dimensions. The usual L/D ratio of an amateur KNSB rocket motor is around 5-8:1 so since 76.2mm gave me around 2.3 and 50.8mm gave me around 10, I decided to make an educated guess on the diameter of 66mm with 2.5 mm of thickness to ensure a large safety margin for pressure. My first attempt had a 2.5:1 grain diameter and core diameter length ratio. The spreadsheet and OpenMotor gave me a very solid rocket motor. It has an impulse of 1030 Ns with a max internal pressure of 920 PSI. The only problem I found with it was the exit pressure velocity was a bit high at 19 PSI, though it is much better than my first attempt with it being a lot flatter. This flatness is probably due to the less surface area compared to the longer motor.

![Screenshot_2026-10-04_160743.png](https://cdn.hackclub.com/01a1062b-7057-77ac-abd0-30abf1751394/Screenshot_2026-10-04_160743.png)

After this attempt, I tried a few smaller ratios such as 2.1:1 all the way down to 1.8:1. The problem was the SRM spreadsheet only gave me an ideal Pe - Po (expansion ratio) of 0 when my ratio was 1.8:1. This web thickness is far too low and can lead to cracking or possibly large scale chipping which would turn this rocket motor into a pipe bomb. What I decided to do was actually go back to the 2.5:1 ratio and do something known as “throwing crap at the wall to see what sticks” with the nozzle. Since the exit pressure was too high, I tried different combinations of increasing the nozzle throat diameter and exit diameter before eventually finding these values. This gave me relatively optimal expansion with the most critical part of the burn being in the 14-15 PSI range. Sadly because of the low surface area, the peak thrust is much lower at around 620 Newtons.

![Screenshot_2026-10-04_160812.png](https://cdn.hackclub.com/01a1062b-d648-7dbc-bb73-d178c4957947/Screenshot_2026-10-04_160812.png)

![Screenshot_2026-10-04_160833.png](https://cdn.hackclub.com/01a1062c-2110-7156-a82e-02839ec650d4/Screenshot_2026-10-04_160833.png)

# 2026-09-05: Rocket Motor Design Attempt 1

**Total time spent: 9 hours**

Calculation of the rocket BATES grain geometry started with determining how much mass is required. We can use the propellant mass formula by inputting the wanted It (total impulse). Since I wanted this rocket motor to be special but also be in a safe, I decided on a nice round number of 1000 Ns (Newton seconds). Looking online, I found the typical Isp (specific impulse) of a J-class KNSB rocket motor at 1000 PSI is around 120 seconds. All of those values give me a mass of around 845 grams. Afterwards I calculated the volume (dividing the propellant mass by the density, around 1.841 g/cm3) allowing me to determine the length of the motor casing, core diameter, and number of grain segments.

The next part involves a period of trial and error between core diameter and the length of the casing and the usage of Richard Nakka’s SRM spreadsheet and OpenMotor. I find the dimensions by first finding the face area of the grain by removing h from the formula to find a hollow cylinder. Afterwards, I divide the volume with the area to find the height. Now the trial and error part comes in when making the core diameter. 

![Screenshot_2026-09-05_211106.png](https://cdn.hackclub.com/01a071e9-843b-7814-9271-531c4d78799c/Screenshot_2026-09-05_211106.png)

I first chose a usual ratio of dividing the total grain diameter by 3 (1:3). This gives me a core diameter of 14.2 mm. I took all this information and imputed it into the SRM spreadsheet to give me nozzle geometry and used OpenMotor to tell me if my rocket motor is going to instead operate in “pipe-bomb mode”, which it was. OpenMotor told me 2 things: the mass flux (the amount of high pressure gasses flowing down the motor core divided by the core surface area) was too large and the port to throat ratio was too low (the ratio between the throat diameter and core diameter). These two things would have led to a CATO but thankfully, they are an easy fix. All I needed to do was increase the grain to core diameter ratio to ensure enough space for gases to flow and to ensure a safe port to throat ratio.

In the next calculation, I increased the ratio to 2.5:1. This gave me a core diameter of 17.2 mm. After inputting everything through the simulation software, I eliminated the port to throat area issue but the mass flux was still too high. I made 2 more calculations that both eliminated the mass flux and port to throat problem but both of them were below my target impulse of 1000 Ns. Looking back, this underperformance was due to a misinput in the nozzle efficiency value.

In the final calculation, I used a ratio of 2.45:1. Even though the actual core diameter was 17.47 mm, I decided to round it to 17.4. Why I decided to round down was due to wanting a total impulse as close to 1000 Ns. Rounding to .5 would have made it 1015 Ns rather than the 1010 Ns rounding to .4 (I know this is quite petty but I just wanted the satisfaction of knowing I’m in control of this rocket motor). Now even though my previous two calculations were technically usable, I still would have gone with this calculation due to how much rounder the dimensions are compared to the other 2. The final geometry gives me a final impulse of 1010 Ns with an average thrust of around 920 Newtons.

![Screenshot_2026-09-05_211118.png](https://cdn.hackclub.com/01a071e9-b888-7a8a-ac82-7d036b0df9c6/Screenshot_2026-09-05_211118.png)

Now after getting all the dimensions, I decided it was time to get a look at it in OnShape and to hopefully see flaws in the design, and I definitely found one. The rocket motor is far too long for the diameter. It has an L/D ratio of 8:1 which can cause a lot of erosive burning leading to uncontrolled pressure spikes. In fact, I think the really long design is also the reason why my pressure is slowly peaking (as you’ll see in attempt 2). This makes the first attempt a failure.

![Screenshot_2026-09-05_211131.png](https://cdn.hackclub.com/01a071e9-d439-7938-bf07-8a91d18e719c/Screenshot_2026-09-05_211131.png)

