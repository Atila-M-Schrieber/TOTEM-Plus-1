# TOTEM BUILD GUIDE

## PART LIST

### REQUIRED PARTS

| Part name       | Count | Remarks |
| :-------------- | :---: | :------ |
| TOTEM PCB       | 01 | You can find the files for it [here](/PCB/) |
| Seeed XIAO      | 02 | You can choose between the BLE version (wireless) or the RP2040 version (wired) |
| Choc key switch | 40 | Kailh Choc low profile key switches |
| diodes 1N4148W  | 40 | These are surface mount diodes in SOD123 package |
| 1u Choc keycaps | 40 | You can use the black or white keycaps from Kailh, but I recommend MBK, LDSA or CFX keycaps |
| reset button    | 02 | Alps SKHLLCA010 |
| USB-C cable     | 01 | For connecting the keyboard to your PC |
| power switch    | 02 | MSK12C02 (only required for the Bluetooth build) |
| Lipo battery    | 02 | There is space for a 15 x 22 x 7.5 mm battery (only required for the Bluetooth build) |
| TRRS jack       | 02 | MJ-4PP-9 or PJ320A (only required for the wired build)|
| TRRS cable      | 01 | Alternatively, you can use a TRS cable for [half-duplex](https://github.com/qmk/qmk_firmware/blob/master/docs/serial_driver.md#usart-half-duplex) (only required for the wired build)|


### OPTIONAL PARTS

| Part name              | Count | Remarks |
| :--------------------- | :---: | :------ |
| switch socket          | 40 | Switch sockets for Kailh choc switches |
| toggle switch          | 1/2 | Extra toggle switch(es) to act as layer switch(es) MSK12C02 (same as power switch), only compatible with the Bluetooth build |
| diodes 1N4148W         | 1/2 | Extra diode(s) for layer switch(es) SOD123, only compatible with the Bluetooth build |


### 3DP CASE PARTS

| Part name              | Count | Remarks |
| :--------------------- | :---: | :------ |
| 3D printed case        | 02 | Find the case files [here](/case/Plus 1) |
| 6mm M2 standoffs       | 08 | 6mm round standoffs for screwing the top and bottom of the case together |
| 6mm M2 countersunk screws | 16 ||
| 6x3mm magnets (optional) | 40 | For magnetically attaching the two halves for travel |
| 3D printed travel case (optional) | 1 | For securing the two halves for travel |
| 8.5mm rubber feet (optional) | 8 | they can also be smaller |
| Anti-Slip adhesive sheet (optional) | 1 | As alternative to rubber feet, example source [here](https://aliexpress.com/item/1005005377684110.html) |
| Tenting feet | 4 | Example source [here](https://aliexpress.com/item/1005005605228469.html) |

### DONGLE PARTS
| Part name              | Count | Remarks |
| :--------------------- | :---: | :------ |
| Seeed XIAO      | 01 | (3 total) as a dongle |
| Seeed XIAO case      | 01 | optional, for aesthetics |


## INTRODUCTION

Here is an overview of where and on which side each component needs to be soldered (click on the image to see a larger version).
This is pretty much the same for the Plus 1, except for the extra key.

![TOTEM solder guide](/docs/images/TOTEM_solderguide.png)


***

## BREAK OFF HALVES

The PCB comes in one piece. You need to break it into two halves.

![TOTEM PCB](/docs/images/buildguide/pcb_top.jpg)

After breaking them apart, you're left with some sprue marks, which you can remove with a file if you like, but you don't need to.

> **Warning**
> You should wear a mask while doing this since the FR4 dust is considered to be toxic.

![PCB sprue marks](/docs/images/buildguide/side_01.jpg)

I paint the edges black using a sharpie, so they fit better with the top and bottom, but that's optional too. This is unnecessary for use in the case.

![PCB edges](/docs/images/buildguide/side_02.jpg)


***

## DIODES

The diodes need to be soldered on the top of the PCB. Pay attention to their orientation:  They have a small line on one side, which should be on the side the arrow on the PCB is facing to.

<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/buildguide/diodes_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/buildguide/diodes_bright.svg">
  <img alt="diode orientation" src="/docs/images/buildguide/diodes_dark.svg">
</picture>
</p>

Apply a small amount of solder on one pad.

![Solder on one pad](/docs/images/buildguide/diode_01.jpg)


Then use tweezers to place the diode on the pads and reheat the solder to secure the diode.

![Solder diode](/docs/images/buildguide/diode_02.jpg)


Now you can solder the second pad.

***

## SWITCH SOCKETS (optional)

Here you can apply the same technique as used for the diodes: Apply some solder on one of the pads first.

![switch sockets pad](/docs/images/buildguide/hotswap_01.jpg)

Then place the switch socket in the silk screen markings. The orientation matters here too. Especially if you plan on using the case.

<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/buildguide/socket_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/buildguide/socket_bright.svg">
  <img alt="hotswap socket orientation" src="/docs/images/buildguide/socket_dark.svg">
</picture>
</p>


![hotswap socket right and wrong orientation](/docs/images/buildguide/hotswap_02.jpg)


Then reheat the solder.
Apply some pressure with a pair of tweezers to make sure the socket is fully seated.\
Now solder the second pad.

![switch socket soldered](/docs/images/buildguide/hotswap_03.jpg)

***

## POWER SWITCHES (only required for Bluetooth build)

(Also applies to the layer switches included in the Plus 1 design.)

Apply a tiny bit of solder on the bigger, outer pads on top of the PCB.

![power switch pads](/docs/images/buildguide/power_01.jpg)

The power switch has some tiny knobs on its bottom, which fit into the PCB holes. Hold it in place with tweezers and then reheat the solder on the pad. After this, you can solder the other pad and the three pins.

![power switch](/docs/images/buildguide/power_02.jpg)


***

## RESET SWITCHES

Insert the switch into the top of the PCB.

![reset switch](/docs/images/buildguide/reset_01.jpg)

I placed the footprint a bit more towards the edge, than it's meant to be, to integrate it better into the case. Therefore the tiny stabilizer on the bottom of the switch doesn't touch the PCB anymore. Make sure it is aligned with the PCB vertically, so it's oriented correctly.

![reset switch orientation](/docs/images/buildguide/reset_02.jpg)

Then solder the four pins on the bottom to the PCB

![reset switch solder](/docs/images/buildguide/reset_03.jpg)


***

## TRRS JACKS (optional)

> **Warning**
> You don't need the TRRS jacks for running the TOTEM with ZMK. Actually, you can damage your board when connecting it through TRRS, while also connected to a battery.

Install the TRRS jack on the bottom side of the PCB. The place where you should insert it is marked with a white line.

![TRRS jack](/docs/images/buildguide/trrs_01.jpg)

You may want to use some masking tape to hold it in place since you need to solder it on the bottom.

![TRRS jack taped](/docs/images/buildguide/trrs_02.jpg)

Then solder the pins on the bottom to the PCB.

![TRRS jack soldered](/docs/images/buildguide/trrs_03.jpg)


***

## MICROCONTROLLER

> **Warning**
> First flash the microcontroller to make sure it works, before soldering it in. Especially since you can't use sockets.

Place the microcontroller in its place.

> **Note**
> If you're struggling with keeping it in place you can use the headers, which came with it, and some double-sided tape. But make sure it sits flat on the PCB. Otherwise, the case won't fit.

Apply some flux and try to hold the iron at an angle where you touch the pads of the microcontroller and the PCB while adding solder.

![soldering MCU](/docs/images/buildguide/MCU_01.jpg)

The pads on the back are a bit fiddly to solder, so you should add a lot of flux to the pads on the microcontroller first. Then apply the same technique as on the front: Try to touch the pads on the microcontroller and the PCB before adding solder.

![soldering MCU back](/docs/images/buildguide/MCU_02.jpg)



***

## BATTERY (optional)

> **Warning**
> You don't need the battery for running the TOTEM with QMK. Actually, you can damage your board when connecting it through TRRS, while also connected to a battery.

You probably need to shorten the cables and tin them, since the length needs to be pretty short, to fit. I've also plasti dipped mine.

![shorten battery cables](/docs/images/buildguide/battery_01.jpg)

> **Warning**
> Before attaching the battery in any way to the PCB set the power switch to off (right on both sides).

You can see which cable needs to go in which eye by the silkscreen below the eyes. Red is + / Black is -.

![battery face](/docs/images/buildguide/batt_face.jpg)

Attach the wires of the battery to the pads and solder them in.

![Ouch](/docs/images/buildguide/it_stings.jpg)


***

## CLEANING

You can use an old toothbrush and some isopropanol to clean it from residues.


***

## FIRMWARE

If you have not already flashed the firmware to the microcontroller you should do it now.\
[Here](https://github.com/Atila-M-Schrieber/zmk-config) you can find the ZMK firmware for the TOTEM Plus 1.\

Probably a good idea to also install switches to make sure all of them work, before inserting the board into the case.

![PCB with switches](/docs/images/buildguide/pcb_switches.jpg)


***

## CASE

The case is made up of three parts: top, middle, and bottom.
The top holds the magnets, and hides most of the electronics,
the middle surrounds the switches and protects the thumb cluster,
and the bottom protects the switch sockets.
The 6mm spacers go through the top and middle sections,
and the case is held together by screws inserted into the spacers from the bottom and top sections.

1. Press the PCBs into the bottom section of the case. Don't be afraid to apply some force until the bottom is firmly in place.
2. Screw in the bottom 4 screws - they will self-tap here.
3. From the top, screw the spacers onto the screws, until their bottoms are flush with the PCB.
   It should look like this:
   ![Bottom attached, with spacers](/docs/images/buildguide/1_bottom_and_spacers.png)
4. Next, align the middle section with the four spacers, and push it down evenly until it is flush with the PCB.
   ![Middle aligned](/docs/images/buildguide/2_middle.png)
   You might want to use a small blunt object to make sure it is flush at all points.
   Make sure the 'skirt' around the thumb cluster is fully down by squeezing the middle and bottom sections together there.
5. (Optional, if you want to use the travel case.) Insert one 6x3mm magnet into each hole in the top sections.
   They should all face the same direction,
   and the two top sections should snap together with no opposite polarities.
   If some magnets are hard to insert, you can use a small blunt object to press them in.
   If some magnets are too loose, use superglue.
   ![Top with magnets](/docs/images/buildguide/3_top_magnets.png)
6. Align the top section with the spacers, and push it down until its perimeter is flush with the bottom.
   I recommend flipping the board upside down, and pushing from the bottom section's edges,
   as some less supported bits can get bent out if done carelessly.
   ![Top aligned on spacers](/docs/images/buildguide/4_top.png)
7. Insert the top screws until flush with the case, and alternating top and bottom tighten the screws.
8. Apply the tenting feet to the bottom of the cases.
   I recommend spacing them so when tented, the edge of the case at the pinky keys lays flat.
   In the image, I applied the feet so I don't cover any screws, but this is slightly less stable than it could have been.
   ![Applying the feet](/docs/images/buildguide/5_feet.jpg)
9. Apply a thin strip of the adhesive rubber mat to prevent slipping.
   ![Applying the rubber mat](/docs/images/buildguide/6_rubber.jpg)

That completes the case!

For the travel case, insert two 6x3mm magnets in each hole. (Or one 6x6mm magnet.)
I recommend tuning your printer by cutting out one hole and printing it at very slightly different scales.
Once you find the perfect press-fit scale, you can use Blender to modify the holes:
Open the travel case stl in Blender, go into edit mode, press 1 to select vertices,
go into wireframe mode, click the z-axis on the compass to get a top-down view,
select all vertices associated with the holes with any selection tool,
and scale them using "Individual Origins" **excluding the Z-axis** using shift-z to the setting you found.

I used a woodworking clamp to press the magnets into place, but any sort of vice should work.

Alternatively, you can glue them in with superglue.

![Travel case](/docs/images/buildguide/7_travel_case.jpg)
