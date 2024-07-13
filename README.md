<picture align="center">
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/TOTEM_logo_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/TOTEM_logo_bright.svg">
  <img alt="TOTEM logo" src="/docs/images/TOTEM_logo_dark.svg">
</picture>

<h1 align="center">T O T E M</h1>
<h2 align="center">Plus 1</h2>

TOTEM Plus 1 is a modified version of the TOTEM keyboard, with an extra pinky key.
It is a 40 key column-staggered choc split keyboard. It is meant to be used with a SEEED XIAO BLE or RP2040.
The build process is pretty much identical, except you need electronics for two more keys.
(Sockets, diodes, switches, and keycaps)
[Here](https://www.hackster.io/geist/totem-a-tiny-splitkeyboard-with-splay-cb2e43) you can read about the process of making it.

I will also be modifying the case to be able to fit into a magnetic travel case, like the one
made by [Compression Keyboards](https://compressionkeyboards.com/products/4c-3d-printed-case-kit).

While the layout is pretty much identical to the [KLOR KONRAD](https://github.com/GEIGEIGEIST/KLOR),
I prefer the æsthetics of the TOTEM, and I have no need for a rotary encoder on this keyboard.
Also, I wanted to dip my toes into PCB editing, and this seemed like a slightly bigger challenge
(it was) than removing the rotary encoder from the KLOR.

This fork incorporates the [Tenting fork](https://github.com/BertPlasschaert/TOTEM-Tenting).

THIS IS UNDER DEVELOPMENT, THIS LINE WILL BE REMOVED WHEN I HAVE A WORKING KEYBOARD IN MY HANDS

I MAY OR MAY NOT MODIFY PICTURES HERE OR IN THE BUILD GUIDE. IF I DO THIS LINE WILL BE REMOVED.
UNTIL THEN, ALL PICTURES ARE FROM THE ORIGINAL BUILD / THE TENTING FORK.

I AM PRIMARILY DOING THIS FOR A DONGLE + BLE SETUP. IF I END UP MAKING CHANGES TO THE WIRED VERSIONS
OF THE CASES, I WILL REMOVE THIS LINE.

### Additional features:
- [x] I like the idea of using a switch (like the on/off one) as a way to turn a layer on/off,
      especially for a usecase like gaming. Since I'm going to use this wirelessly, I might add
      another switch (same as the power on/off switch) on top of where where the TRRS
      jack would go. I can probably add the footprint without even removing the TRRS footprints.
      This would mean another row or column from one of the UART pins
        - If I'm using the UART pins for something else, like trackpoint support, this won't work
          (or only on one side of the keyboard, ie 'gaming mode' switch on left side, trackpoint on right)
        - In implementing this **I swapped the poles of the TRRS jack** (GND <-> VCC), so take note
          if you do end up using the wired version and need to debug the TTRS cable (for some reason).
        - There is a lot of overlap with the TRRS through holes - while it might be harder to solder
          due to the conduction, there is plenty of space to solder the switch leads.
    - Alternatively I can add an I/O expander (MCP23017), which is already supported in ZMK
- [ ] Trackpoint support: ([see this pull request / fork](https://github.com/zmkfirmware/zmk/pull/1751))
      This would be a replacement for the TRRS jacks, since it uses UART.
      I have ordered [this module](https://www.aliexpress.com/item/1005004696754100.html),
      so I'll see if/how I can use it.
***

(The Plus in the 'totem pole' logo is (supposed to be) a hammerhead)

## LAYOUT

![TOTEM layout](/docs/images/TOTEM_layout.svg)

***

## PCB

[Here](/PCB/) you can find the KiCad files and Gerbers for the TOTEM.

***

## CASE

You can use the TOTEM without a case, but [here](/case/) you can find one I made for it.

***

## BUILD GUIDE
  
The build guide for the TOTEM can be found [here](/docs/buildguide.md).

***

## FIRMWARE

[QMK config](https://github.com/GEIGEIGEIST/qmk-config-totem) for the TOTEM (wired using the XIAO RP2040)\
[ZMK config](https://github.com/GEIGEIGEIST/zmk-config-totem) for the TOTEM (wireless using the XIAO BLE)

***

## PHOTOS

This is the TOTEM in a black resin case

![TOTEM black resin](/docs/images/TOTEM_black_perspective.jpg)\
![TOTEM black resin](/docs/images/TOTEM_black_top.jpg)\
![TOTEM black resin](/docs/images/TOTEM_black_bottom.jpg)

This is the TOTEM with a black resin tenting bottom plate

![TOTEM black resin tenting](/docs/images/TOTEM_black_tenting_example.jpg)\
![TOTEM black resin tenting](/docs/images/TOTEM_black_tenting_bottom.jpg)

***

## BUY 

You can buy TOTEM kits and finished builds on [keeb.supply](https://keeb.supply/products/geist-totem) (unfortunately Europe only for now)

***

## CREDITS

### INSPIRATION

I've added the additional pinky key to make the TOTEM compatible with the layout boards like the [Balbuzard](https://github.com/brow/balbuzard) by [Tom Brow](https://github.com/brow) and the [Osprette](https://github.com/smores56/osprette) by [Sam Mohr](https://github.com/smores56) use, where you put the keybinding of the top left and right keys on an outer pinky key.

### HELP FIXING THINGS

People who helped me create this board and fix stuff

#### PCB
- [Marco "Bob"](https://github.com/GroooveBob)

#### CASE
- [Freya](https://github.com/freya-irl)
- [Bubbleology](https://github.com/bubbleology)

#### FIRMWARE
- [Cem Aksoylar](https://github.com/caksoylar)
- [Grinnie](https://github.com/regicidalplutophage)
- [Alaa Saad Mansour](https://github.com/AlaaSaadAbdo)
- [pekudzu](https://github.com/pekudzu)


If you build a TOTEM I would be pretty happy to see some pictures. And if you want to leave me a tip you can do this [here](https://ko-fi.com/geigeigeist) (but please don't feel pressured)

