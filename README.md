# CubieKid 

<img src="photos/CubieKid.jpg" width="600">

## A cute MP3 player project - made-to-measure (small) children's needs.

When I learned about [Thorsten's TonUINO project](https://www.voss.earth/tonuino/) I decided to create a compatible housing which fits the needs of (small)kids and parents. The result is CubieKid. It is still an ongoing process as I get improvement suggestions and comments to make it even better.

There are no sharp corners, no external screws or loose parts. The speaker is scoop-proof covered. For serviceing (audio-files and battery-change) the access panel can be removed with a designated tool only. 

The whole player is powered by batteries, accu pack or USB-power-bank. So there is no need for external cables and power supplies. This all makes CubieKid the ideal all-day companion.

### Housing

This housing can be made from medium density fibreboard with a thickness of 3mm (sorry folks this is a german design - so everything is in metric dimensions).

I'm using a homemade CNC-mill ([Make: MaXYposi](https://www.heise.de/make/artikel/MaXYposi-Projektseite-zum-universellen-XY-Portalroboter-von-Make-3676050.html)) which works well. But you can use a Laser Cutting Device as well.

<img src="photos/CubieKid_1.jpg" width="500">



### Electronics

<img src="photos/PCB_2.jpg">

The newest upgrade is an optimized circuit and the associated single-sided pcb. So the reproduction is easy and inexpensive.



Highlights:

- Intended to be used with batteries, accu packs and USB-powerbanks

- Power-On with one of the three buttons

- Auto-standby-function saves battery live by reducing current down to just a few micro-amperes

- Battery voltage monitoring function with audio alert and shut-down


## Construction Manual

Please follow the instructions step by step to build a good looking and stable box.

<img src="photos/Wooden_parts.jpg">



#### Wooden parts

Cut out all parts. You need medium density fibreboard with a thickness of 3mm. Here's a survey with all wooden parts you need:



<img src="photos/Parts-Survey-V1-0.jpg">



#### Additional material

You will need some more things to build CubieKid:

- PVA glue (fast-drying type recommended)
- 1 x 32mm foldback clip
- 4 x Small socket screws for wood, length: 5-6mm
- 2 x Metric screw M4 x 20mm
- 2 x M4 nut

#### Front-, Top-, Bottom and Side panels

Glue the both front panels together. Do the same likewise with the top- and bottom panels. Make sure that the engraving of the card area on upper top panel is visible.

Take two different side panels and glue them together. Continue with the remaining side panels but make sure they’re glued together mirror-inverted. So you’ll get a right and a left side for the box.

The speaker will be glued (hot-glue) on a second speaker grid which makes the speaker scoop-proof.

<img src="photos/Speaker_Grid_1.jpg">

<img src="photos/Speaker_Grid_2.jpg">

 I am using a recycled speaker (out of an old amateur radio) with 7 cm diameter and 1 Watt power. The speaker grid has two adjusting-notches which should fit the corresponding notches on the inner front panel.

<img src="photos/Speaker_Installation_1.jpg">

#### Back panel (Service Access)

Now you can start to assemble the back-cover with the locking function. Take the panel (that’s the one without any drill holes.) and put it into its later position at the box. 

Glue the two long rectangular parts to the inner side of the back panel. They will keep the back panel in place, so they should be quite close to the upper / lower corner. Do NOT apply glue to the side facing the upper/lower panel – the back panel must be removable. Every box is a little bit different so it is the best to fix thr rear panel at the half-finished box (like at the photo) then glue in the rectangular parts and push them in the direction of the yellow arrows.

<img src="photos/Panel_assembly_1a.jpg">

Now we need the two D-shaped sliders and the two smaller rectangular pieces. To make sure the slider’s function they probably need to be sandpapered to somewhat less than 3mm thickness.

<img src="photos/Panel_assembly_1.jpg">

Put the siders on the inner side of the back panel – the rounded corners must face outside. Do NOT glue them. Put a small rectangular piece into each D-hole. Find a position where the slider is able to slide out about 4-5mm, then glue the rectangular piece to the back panel. The small rectangular pieces act as stoppers protecting the sliders from being pushed out too far.

Now we have a nice little two-sided sliding mechanism. To apply the mechanical force to keep the sliders in the outer position we will need a 32mm foldback-clip. 

Remove the handles of the foldback-clip and discard the black metal part. We’ll only need the handles. Insert the handles between the sliders -the open sides must face the center.

<img src="photos/Panel_assembly_2.jpg">

Now attach the inner panel (that one with four small holes) with small screws.

Your back panel is now ready to be snapped into position. But be aware: You’ll need to build a removal tool first to be able to remove the back panel again.

#### Opening Tool

<img src="photos/Opening_tool.jpg">

To open the rear panel you will need an opening tool. Take a piece of wood or aluminium (length: about 9cm) and drill two 4mm holes (space center/center: 60mm). Insert a M4 screw* into each hole and fix it with a M4 nut. 

*:The screws need to be long enough to pust the slider out of the adjacent side panel.

Use: Push the opening tool into the holes on one side of the box. Now pull the rear panel away from the box at that side you attached the tool. It will work on both sides (some kind of redundancy thanks to the use of the same part on both sides).

<img src="photos/Insert_Opening-Tool.jpg">



### Electronic Assembly

<img src="photos/Platine1-3.jpg">

You will need (for Rev.1.3):

- 1x 	pcb "CubieKid"
- 1x	Arduino Nano (clone)
- 1x	DFPlayer Mini Module
- 1x	RFID-RC522 Shield and compatible RFID-cards
- 1x	IC CD 4011 (DIL)
- 1x	SD Card (up to 32GB)
- 1x	Diode 1N4001
- 6x	Diode 1N4148
- 1x	FET IRF 4905
- 2x	Resistor 10k
- 2x	Resistor 100R
- 1x	Resistor 100k
- 1x	Resistor 1k
- 1x	Capacitor 0,1uF (100nF), e.g. WIMA MKS2
- 1x	Speaker (about 7cm diameter, 8 Ohms, 1...3 Watts)
- 3x	24mm arcade pushbuttons

and:

Connecting cables, pinheaders, battery holder(s), 5 cm silver wire (0,8mm diameter).



The finished pcb looks like this (Rev.1.3):

<img src="photos/Platine1-3_1.jpg">

It is small enough to be fitted on the upper half of the rear panel. So the access to the Micro-SD Card and USB-Port are easy. Make sure the connecting wires are long enough to open the panel.

<img src="photos/PCB_assembly.jpg">



Update Rev. 1.3:

In Revision 1.3 the power needed on standby was reduced down to less than 0.02mA (20 microamperes).

R3 stays empty (no Bridge, no resistor)

R6 most be a wire bridge or zero ohms resistor.

As battery you can use either 4x 1,2V AA accu cells or 3x 1,5V batteries. Diode D1 (1N4001) acts as reverse battery protection and as overvoltage protection (if you use 4 accu cells and you put in 4 batteries by error).  In the case that you use 4 battery cells (each 1.5V) you'll need diode D1 in place. For 3 cell configurations or 4 accu cells you install a wire bridge instead of D1.



A 5V USB power bank should work too (not tested yet). But you will need an extra cable to connect the power bank to the power in pins. Be aware that most of the powerbanks have their own voltage monitoring. So they might switch off before any warning from CubieKid.



...to be continued.
