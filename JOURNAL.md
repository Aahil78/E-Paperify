---
title: "E-Paperify"
github: "https://github.com/Aahil78/E-Paperify"
description: "An E-Ink LCD based Spotify/Media dashboard! (Brought in from half-life, not shipped yet, reason to bring here is because I wasn't able to complete before the deadline :( )"
created_at: "2026-11-02"
total_time: "9h 42m"
---

# November 2, 2026: 2026-10-26 - Project Planning!
<!-- fabricate:entry 1827 -->

Hi! Today I planned out the project and made a general circuit diagram so that I have an idea laid out in my mind for all the parts im gonna use. I've decided on using a:

- Grayscale E-Ink Display (4.2inches)
- ESP32-S3-WROOM-1-N16R8
- INMP441 MEMS Microphone
- SK6812 LED Strip
- 3-5x MX Switches
- EC11 Encoder
I might add other parts later but this is all I have planned for now, obviously theres gonna be an LDO, some passives, and a type c port but yeah this is my general plan. I timelapsed 0.4hrs out of 0.7 bcz the 0.3hrs was just me planning out stuff and asking Google AI for part recommendations. Bye!!

![](https://fabricate.hackclub-assets.com/ff53a9cc3018e9fde6592e493f986c43554266748f05e4554dd9036c79084536/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/lGPklF0X025v

**Total time spent: 42m**

# November 2, 2026 (entry 2): 2026-10-28 - First steps in the schematic!!!
<!-- fabricate:entry 1828 -->

Hi! Today I started off my schematic and completed almost all of the ESP32-S3 circuitry. Now I need to add the LDO, Type-C Connections, then the other stuff like Mic RGB and E-Ink Screen. I don't know what else to say lol cz I'm sleep deprived and I think the Lapse shows it all lol. Anyways bye!!!

![](https://fabricate.hackclub-assets.com/d546f1c4952c635be3f4c3cbdf17349e758b6643556b28b5b27bae606933065d/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/8Z4j6GUEIz5H

**Total time spent: 36m**

# November 2, 2026 (entry 3): 2026-11-1 - Schematic done!!!
<!-- fabricate:entry 1829 -->

Hi! Today I completed the schematic, changed some parts, added some stuff to the BOM, got some help from AI and more!!

My schematic is finally done! I used AI for some help because I'm really trying to make the project successful but for programming I def won't use AI. Idk what else to say, oh yeah I decided to use 5 MX Switches (w/hotswap sockets) and an EC11 Encoder w/SW. Additionally I'm also using SK6812MINI-Es under the switches so the Switch backlight syncs with the cover art, there's an RGB Connector at the end of the SK6812s for a nice underglow as well. Not sure if the USB-C power will be enough. Actually I'll add a 2pin Power connector so I can use a PD Module if the power dosen't work out and only use the USB Port for programming and such. If I'll have to use the PD Module then I'm gonna use Bluetooth for the data of spotify and any music playing, same for controls then. I'll try to complete the PCB by today asw!

![](https://fabricate.hackclub-assets.com/e3c7be4a6041127a243267fcf46311af6f060ccbd8db0049c48a757d21714829/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/mqmZ2hQ0Xujg

**Total time spent: 2h 6m**

# November 2, 2026 (entry 4): 2026-11-01 - PCB Done!! Huge Lock in sesh
<!-- fabricate:entry 1830 -->

I completed the PCB!!! Yayyyyyy, huge lock in session. I had to make my own footprint for the INMP441 Microphone cz there were none online. Now I just gotta make the case and write the code.

![](https://fabricate.hackclub-assets.com/9aab4a0ee22cadeb4aa5b3af85b9e1209f17a72f13a7415ef684b20085d4d634/image-png/image.png)
![](https://fabricate.hackclub-assets.com/20ad8dd7004a2c12d211c04b623a81ab0505f59cd69c6cc88cc93a6957a17e70/image-png/image.png)
![](https://fabricate.hackclub-assets.com/93a65562ad6616ad37f5af382f16fbad82e231274f440fd65cee2c79d144e2fc/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/CJD2GgsOcqSl

**Total time spent: 2h 48m**

# November 2, 2026 (entry 5): Did lots of CAD and some minor changes in the PCB
<!-- fabricate:entry 1831 -->

Hiii!!! Today I faced lots of hurdles, one being that I wasn't able to complete b4 the deadline of half-life, another being that I just wasn't able to figure out how to do the case. And like I spent so much time just making CAD just for it to not look good or not work out properly, anyways, I FINALLY figured out a design that may not win a beauty competition but it'll be functional, and after all I can make more revisions of the case later on.

Some challenges I faced during the CAD:
- The [E-Ink screen](https://lapse.hackclub.com/timelapse/CJD2GgsOcqSl) that I'm buying is a very thin glass and very fragile, so I needed a way to get it in the case without putting too much force so it doesn't crack, but I needed the case to be tight enough on the screen that the screen doesn't flop around.
- I wasn't able to find a design where I could make everything work together, initially I thought of a design where the PCB would be right behind the screen but then I remembered that I have 5 switches and an encoder that needed to be accessible too so I scrapped that, then I came up with an L Shape design where the screen was standing up and the PCB is laying on the base, but then I wasn't able to make the USB-C Port accessible. So then I thought of adding a hole to make a cable pass-through to the PCB but that wouldn't allow the cable to be disconnected easily, so to overcome this, I simply moved the USB-C port to the right edge instead of the top.
- After making the L-Shaped case, I realized that I might have made the PCB area and Screen a bit too far apart, functionally it wasn't an issue but aesthetically it was, well I didn't wanna redesign all over again so I just thought fuck it we'll find a way to make it work.

And yeah I silently crashed out a LOT, was working at 3AM, but then my skin peeled off of my foot so the pain was too bad for me to work, wasn't able to sleep either, then somehow I fell asleep with the pain, woke up and told my parents that I ain't going to school, then got to work again. So yeah I worked a lot but made very little progress for the time that I worked. I hope to get the case done soon cz now I just need to make the plate for the PCB. Wait, yeah speaking abt the plate, the walls are not thick enough for me to use heatset inserts and screw the plate into the base, so instead I'm just gonna hope that the MX Switches can keep the plate sturdy enough. Sorta like a sandwich mount but not a sandwich mount. Anyways byee!!

Oh yeah everything is timelapsed but in 2 different parts so I'll link lapse part 1 here and make a second journal with lapse part 2.

Timelapse: https://lapse.hackclub.com/timelapse/ck8AiRKkK4BU

**Total time spent: 2h**

# November 2, 2026 (entry 6): SECOND JOURNAL FOR CAD LAPSE PART 2
<!-- fabricate:entry 1832 -->

Yeah uhh second journal for my part 2 of the timelapse for all the CAD I did.

Timelapse: https://lapse.hackclub.com/timelapse/46FK6jK4c_tb

**Total time spent: 1h 30m**
