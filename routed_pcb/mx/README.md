left | right | outline
-|-|-
![left](images/board-front.png) | ![right](images/board-back.png) | ![outline](images/display_all_rotated.svg)

# Build Guide

## 1. PCB
1. Take 2 pcbs and flip them to the **back** side
![flip to back](images/20260411_170405.jpg)

1. Solder the jumper pads for the controller so that the two sides of the pads can be connected together.
![solder jumper pads](images/20260411_170654.jpg)

1. Still on the back side, put solder on the pads for the hotswap sockets
![hotswap sockets](images/20260411_171538.jpg)

1. Melt the solder and press the hotswap sockets down, one side at a time. Use tweezers if that helps.
![hotswap sockets 3](images/20260411_171915.jpg)

1. Still on the back side, put down the reset switch and solder it in. Depending on what switch you're using, it might help to bend the pins a bit down so it'll go inside the hole.
![](images/20260411_173355.jpg)

1. Flip over to the **front** side. Place the on/off switch and solder it in
![](images/20260411_173540.jpg)

1. (Optional) align the JST connectors with the + sign. This may be different from the rectangle drawn on the pcb depending on where you order the right angle JST connectors from, or how the male connector on the battery looks. What's important is that the red wire aligns with the + sign. 
![](images/20260411_173910.jpg)
1. Solder the JST connector from the back. Alternatively, solder the battery wires directly.
![](images/20260411_174348.jpg)

1. Back on the front side, place the controller **with the components side down**. The markings for which pin is what aligns on the **back** side, not the front. The two pins closest to the USBC port are **empty** and not used. Those are for Battery + and -, which are the same thing as RAW and GND.
![](images/20260411_182838.jpg)
optionally, but highly recommended, follow [this](https://www.40percent.club/p/socketing-pro-micro.html) or [this alternative](https://docs.splitkb.com/product-guides/aurora-series/build-guide/microcontrollers) guide on how to socket the controller (see [here](https://docs.splitkb.com/frequently-asked-questions/about-split-keyboards/microcontrollers/sockets) for why you would want to).

1.  The finished PCB should look like this, with the battery slotted under the controller.
![](images/20260411_183401.jpg)

1.  Alternatively, if the battery does not fit under the controller, you can also put it on the side like this:
![](images/20260411_212405.jpg)

## 2. Case

Before printing, measure the distance from the top of the usbc port to the bottom of the pcb:
![](images/20260411_223246.jpg)
If this value is between 7.2mm and 8.2mm, then go ahead and use the STL files available on [printables](https://www.printables.com/model/1659997-case-for-hector36). Otherwise, you can copy and edit the [onshape file](https://cad.onshape.com/documents/dab7ead69061981322a5fa82/w/eeec2b07408bf6c3576b55db/e/49101eb28d1b1828dfaa91ca?renderMode=0&uiState=69db021f7ce9695c3c22be27). Simply modify the `bottom_pcb_to_usbc` variable at the top of the variable table.


1. Print the top half face down, and enable supports:
![top_case_orca](images/top_case_orca.png)
1. disable support for the bottom part.
2. remove the support for the top half:
![](images/20260411_211316.jpg)
![](images/20260411_212211.jpg)
1. put in the M3 heat set inserts:
![](images/20260411_212926.jpg)
1. put in the switch extender in the orientation shown below
![](images/20260411_213357.jpg)
1. put everything together and we're done!
![](images/20260411_213432.jpg)
![](images/20260411_183440.jpg)


## Firmware
see [zmk module](https://github.com/ezxzeng/zmk-keyboards-hector36)
