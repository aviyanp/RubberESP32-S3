<img width="866" height="861" alt="image" src="https://github.com/user-attachments/assets/0505dcc0-fb47-4acc-9ca2-db93ddaf2d4c" />---
title: "RubberESP32-S3"
author: "Aviyan Panday"
description: "A custom devboard based on the ESP32-S3 to be used as a rubber ducky!"
created_at: "2025-07-19"
---

Total Time Spent: 20 hours

Note: I started tracking progress on July 15th but forgot to make a Repo and upload everything, so I'm just going to copy paste my logs from those days and upload the pictures in a bit.

## **Day One: 7/15/2025**
Spent a while trying to figure out what the best MCU to create a devboard would be for. I want to get better at PCB design not just for robotics (like RoboCup), but also to just make cool projects that I actually enjoy using.
Saw Cyao and other people in the Slack talk about how easy the RP2040/RP2350 is to design for, and decided to take a look at it, but decided against it after watching a tutorial on building a board for it.
I spent a long time going back into the MilkV docs because I really wanted to see if I could integrate any of their modules, but the SMD modules were all out of stock. And I don't think they have KiCad files so I can't do anything about it.
Went back through my old Discord and iMessages chats to see what MCUs both my team and other teams have built around. Decide against the Teensy because it seems insanely difficult to program a Cortex M7 chip by myself and it was really unreliable.
Finally decided on using the ESP32-S3-WROOM-1U module after remembering the team captain of Andy's Geese talk about how it was a lot more reliable than other MCUs and enough for competition.
Spent some time looking at STM32H7 MCUs before that, because STLink seemed a bit simpler than NXP's Cortex M7 core.
Started to make a list of materials I could read/learn from in order to figure out how to make a devboard.

Time Spent: 4 hours

---

## **Day Two: 7/16/2025**
Tried to read through the module's datasheet, and found that it has reprogrammable GPIO pins, which seems really convenient considering the number of times I've realized I can't route things a certain way because I blocked the pins I needed with my genius wiring but had useless pins free.
Spent more time digging through Instructables and other websites trying to figure out how to make a devboard, but they were too vague, used protoboards instead of actual EDA software, or not for my module.
Finally found a YouTube video that explained the core functions of the ESP32-S3 module and demonstrated how it works/boots and why capacitors/buttons are necessary.
Drew up the initial schematic and failed multiple times before eventually getting no ERC errors.

I don't have the image of the original schematic but the Day Three one is the same except for the swapped out symbols for USBC and the SD card socket.

Time Spent: 5 hours

---

## **Day Three: 7/17/2025**
Realized that in order to be a good/effective rubber ducky, I need a micro SD card reader in order to quickly load scripts onto the ducky. Went on LCSC, found a TF card reader as well as a SMD USB-C female port, and debugged EasyEDA2KiCad before placing it into my schematic.
However, I started getting a bunch of DRC errors because the footprints themselves seemed to be faulty. Asked for help in Slack but got none :(
I tried to rectify this by using different footprints, but it turned out that the it was bugging with every single footprint. I tested out PCBA on JLCPCB's website and the render showed all of the components in the right places, so I assumed it was completely fine to go ahead.
I built a complete LCSC BOM with all the part numbers, trying to make it as cheap as possible. I did notice that ESP32-S3 modules were more expensive on LCSC and prices for PCBA were insane. Considering adding a hotplate/other things to the BOM.

![DRC Errors](https://i.ibb.co/PvFGS3QK/image-5.png)
![Schematic](https://i.ibb.co/FkXCtZ3n/image-3.png)
![PCB](https://i.ibb.co/hJ24VtV7/image-2.png)

Time Spent: 4 hours

---

## **Day Four/Five: 7/18-19/2025**
This was by far the most hellish day - I'm up at 2:00AM and I *think* that I'm finally done. I have been up for 20 hours, 7 of which I spent on this :sob:. I spent a lot of time trying to design the actual board. I started out with a spacious 4 layer board with everything evenly aligned/distributed because I thought it looked nice.
Little did I know, it was a mess trying to route anything new because of all the space I took up. Furthermore, I realized that I needed to use differential pairs for USB, and couldn't for the life of me figure out how to route it because D+ and D- on the module were ever so slightly off, meaning that I had to 
However, a guy on the KiCad Discord told me that my differential pair was actually not the problem and I should use ground planes. Tried to use this autorouter called Quilter, and spent an hour trying to debug all of it's so-called "perfect" work because it gave me drill holes smaller than JLCPCB could make.
Additionally, I decided to add header sockets for I2C as well as Serial and like 8 open pins if I want to interact with something else (like an accelerometer I forgot I had in my pocket from robotics).
Finally gave up and decided to shrink the board to 50x50mm with 6 layers. Spent more time trying and trying to perfect the board and finally did (I think)! I'm really woozy and really want to go to sleep. I'm currently chatting with The Grass because I made a new channel and he joined.

![PCB](https://i.ibb.co/20d9pXVy/Screenshot-2025-07-19-at-9-59-24-AM.png)
![Schematic](https://i.ibb.co/VWwzHV19/Screenshot-2025-07-19-at-9-57-54-AM.png)

Time Spent: 7 hours
