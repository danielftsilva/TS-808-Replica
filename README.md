<h1>TS-808 Replica Project</h1>

<h2>Description</h2>

This repository details my research, design, assembly, and testing of a replica of the iconic TS-808 distortion pedal.

<h2>🎸 Project Summary:</h2>

<b>Research:</b> Studied the original TS-808 design and gathered all necessary information.

<b>Design:</b> Created PCB schematics and layout using KiCad.

<b>Assembly:</b> Purchased components and assembled the PCB.

<b>Testing:</b> Tested to ensure functionality (the most fun part).

<b>Documentation:</b> Photos and documents of every step of the process.


<h2>⚡ Implementation Details:</h2>

<b>From Reference Schematic to PCB:</b>

- The design is rooted in the [reference schematic](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/ts-808_original%20reference_circuit.jpg) for the Ibanez TS-808 circuit, capturing the preamp, diode clipping, and tone control sections. This schematic outlines the signal path - from the initial buffering of the input signal through the op-amp stages to the final output drive.

- The "heart" of this circuit is the [RC4558](https://www.ti.com/lit/ds/symlink/rc4558.pdf?ts=1740038954763&ref_url=https%253A%252F%252Fwww.google.com%252F), a dual OP-AMP. It handles both the input buffering and the overdrive stages. It's low-noise gives you a warm, smooth distortion (the main and sought-out characteristic of this pedal!). Also, the dual configuration allows one section to amplify the signal while the other handles its tone.

- Here you can see the [final circuit schematic](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/Main%20Circuit.png).

<!-- modifications -->
<!-- There were a few modifications done on the circuit, namely:

1. Asymmetric clipping: two diodes placed in series (D1 and D2) introduce asymmetric clipping and produce a more "tube-like" distortion with a more dynamic response;

2. Clipper change: a lever switch (SPST) allows selection between different clipping devices - in this case between silicon diodes (1N914) and regular red LEDs. This gives us two distortion textures in the same circuit, providing more flexibility in shaping the pedal's sound;

3. AMZ Fat Modification

Change: A switch is added to bypass capacitor C3.

Impact: Increases boost and enhances bass response, resulting in a fuller and richer tone.

4. Keeley 808 Reissue Modifications

Changes:

Replace R6 (4.7kΩ) with a 2.4kΩ resistor.

Replace R7 (51kΩ) with a 20kΩ resistor.

Replace C3 (0.047µF) with a 0.1µF capacitor.

Replace C9 (0.22µF) with a 0.18µF capacitor.

Impact: Improves bass response and increases distortion at higher drive settings, enhancing the pedal's versatility.

5. Diode Lift Modification

Change: Uses an on-off-on SPDT toggle switch for the diode clipper selector, allowing diode clippers to be lifted from the feedback loop.

Impact: Enables the pedal to function as a clean booster when the diodes are lifted. At high drive settings, this may introduce a more aggressive, raw distortion.

6. Expensive Boutique Modifications

Changes:

Implements diode switching with a diode lift option.

Applies asymmetric clipping modification.

Replaces the Drive potentiometer with a 1MΩ logarithmic pot.

Impact: Aims to replicate high-end boutique overdrive pedals, providing increased gain and a unique tonal character.

Build Information

The project is built on a PCB based on the original TS-808 schematic, with additional wiring for the modifications.

High-quality components were used to maintain signal integrity and reliability.

The modifications were inspired by well-known guitar pedal modders and adapted to suit a wide range of playing styles. -->
<!-- -->

- The [placement afterwards](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/Layout/Placement_2.png) was super simple and straighforward - just had to pay attention to the distance between the components (I used a [1mm track width](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/Layout/tracks_2.png) as it was more than enough for this project).

- This PCB is comprised of a simple 2-layer stackup ([main design rules here](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/production/JLCPCB_KiCad_board_setup_1.png)) - the components occupy the top layer (even though they are all THT). Therefore, in order to not this layer, all the tracks were routed on the bottom layer, which can be seen here in the [final layout](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/Layout/Layout.png).

<b>Component Selection and Soldering:</b>

- The components selected are listed in the [BOM file](https://github.com/danielftsilva/TS-808-Replica/blob/main/BOM/ts_808_generated_BOM.xlsx).

- The [PCB](https://github.com/danielftsilva/TS-808-Replica/blob/main/Assembly/PCB_unpopulated.jpg) was ordered from [JLC PCB](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/production/JLC_PCB_order.png) and it measures 75.00mm x 52.00mm. It was intended to fit inside a 127.00mm x 76.250mm [Hammond enclosure](https://eu.mouser.com/ProductDetail/Hammond-Manufacturing/1411NU?qs=k5YXvLLCsLFkprr1MgbOww%3D%3D).

- Here you can see the [final populated PCB](https://github.com/danielftsilva/TS-808-Replica/blob/main/Assembly/PCB_populated.jpg).


<b>Testing and Troubleshooting:</b>

- I started by assembling the populated PCB and external components with the help of a breadboard. Then, I powered up the pedal to check for proper voltage levels and continuity across the circuit using a multimeter.

- I used [this troubleshooting guide](https://github.com/danielftsilva/TS-808-Replica/blob/main/Tests/TROUBLESHOOTING%20CHART.jpg) for my [check](https://github.com/danielftsilva/TS-808-Replica/blob/main/Tests/schematic%20component%20test%20check.png). It is very useful to diagnose common issues like misoriented components or cold solder joints.

- *Note: if you encounter audible noise on this breadboard setup, do not worry too much - it is much likely due to the lack of proper grounding. Also, using somewhat long prototyping cables like I used can help pickup random noise! This should be solved once you assemble everything inside the metal enclosure.*

- Here is [video footage of me testing the complete circuit](https://github.com/danielftsilva/TS-808-Replica/blob/main/Tests/Test.mov), using a breadboard - troubleshooting phase.

- Here you can see the [final assembled pedal turned on](https://github.com/danielftsilva/TS-808-Replica/blob/main/Tests/Pedal_ON_2.jpeg), using a 9V, 1A AC/DC adapter.

- and video footage (Test.mov), ensures every aspect of the build is verified.


<b>Mechanical Integration:</b>

- Once populated, the PCB was mounted within the pedal's enclosure. Let the importance of proper mechanical support be stressed! This is to minimize vibration and potential interference.

- The external components - jacks, switches and potentiometers - [were then connected](https://github.com/danielftsilva/TS-808-Replica/blob/main/Assembly/Pedal_assembled_1.jpeg). Wire routing is crucial to prevent noise pickup.

- The enclosure was then prepared for final assembly, including optional steps: in my case, I drilled the [necessary holes](https://github.com/danielftsilva/TS-808-Replica/blob/main/Assembly/Pedal_assembled_2.jpeg) and sanded them with #220 grit sandpaper - this is recommended before painting to ensure more durability. [I painted it green](https://github.com/danielftsilva/TS-808-Replica/blob/main/Assembly/Pedal_assembled_3.jpeg).


<h2>🛠️ Tools Needed:</h2>

- Soldering iron and stand

- Solder

- Small side cutters and wire strippers

- Hookup wire (24 gauge stranded, insulated)

- Multimeter

- Magnifying glass (optional)

- Close-in bright light (desk lamp)

*Credits to [General Guitar Gadgets](https://generalguitargadgets.com/effects-projects/distortion/tube-screamer/).*
