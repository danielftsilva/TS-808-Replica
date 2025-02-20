<h1>TS-808 Replica Project</h1>

<h2>Description</h2>

This repo details my research, design, assembly, and testing of a replica of the iconic TS-808 distortion pedal.

<h2>🎸 Project Summary:</h2>

<b>Research:</b> Studied the original TS-808 design and gathered all necessary information.

<b>Design:</b> Created PCB schematics and layout using KiCad.

<b>Assembly:</b> Purchased components and assembled the PCB.

<b>Testing:</b> Tested to ensure functionality (the most fun part).

<b>Documentation:</b> Photos and documents of every step of the process.








<h2>⚡ Implementation Details:</h2>

<b>From Reference Schematic to PCB:</b>

The design is rooted in the [reference schematic](https://github.com/danielftsilva/TS-808-Replica/blob/main/KiCad%20Project/ts-808_original%20reference_circuit.jpg) for the Ibanez TS-808 circuit, capturing the preamp, diode clipping, and tone control sections. This schematic outlines the signal path - from the initial buffering of the input signal through the op-amp stages to the final output drive.

The "heart" of this circuit is the [RC4558](https://www.ti.com/lit/ds/symlink/rc4558.pdf?ts=1740038954763&ref_url=https%253A%252F%252Fwww.google.com%252F), a dual OP-AMP. It handles both the input buffering and the overdrive stages. It's low-noise gives you a warm, smooth distortion (the main and sought-out characteristic of this pedal!). Also, the dual configuration allows one section to amplify the signal while the other handles its tone.


<!-- modifications -->
Features and Modifications

1. Asymmetric Clipping Modification

Change: Replacing diode D2 with two diodes in series introduces asymmetric clipping.

Impact: Produces a more "tube-like" distortion with a different harmonic character, offering a more dynamic response.

2. Clipper Modifications

Change: A toggle switch allows selection between different clipping devices, such as silicon diodes (1N914) and red LEDs.

Impact: Enables multiple distortion textures, providing more flexibility in shaping the pedal’s sound.

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

The modifications were inspired by well-known guitar pedal modders and adapted to suit a wide range of playing styles.
<!-- -->




Using KiCad, the PCB layout was meticulously planned to ensure optimal trace routing and minimal interference. Every component placement was verified against the schematic to maintain fidelity to the original design.
Component Selection and Soldering:

Component Sourcing:
High-quality components are selected as per the guide’s recommendations. This includes precision resistors, low-noise capacitors, high-current diodes, and robust transistors and op-amps.
Soldering Order:
Start with soldering sockets (if used) to avoid potential heat damage later.
Next, solder resistors and capacitors—paying close attention to the correct polarity on polarized components.
Follow with diodes and transistors before finally soldering the integrated circuits (ICs).
Best Practices:
Double-check each component’s orientation before soldering.
Inspect solder joints for any bridges or cold joints to ensure strong, reliable connections.
Assembly and Integration:

PCB Population:
The PCB is carefully populated component by component, ensuring that the layout mirrors the schematic exactly.
Visual documentation (e.g., PCB_populated.jpg and PCB_unpopulated.jpg) is used throughout the process to verify correct assembly.
Mechanical Integration:
Once populated, the PCB is securely mounted within the pedal’s enclosure. The guide stresses the importance of proper mechanical support to minimize vibration and potential interference.
Wiring and Enclosure Preparation:

Wiring Off-Board Components:
External components such as jacks, switches, and potentiometers are connected following the detailed wiring diagram provided in the guide.
Wire routing is carefully planned to prevent noise pickup and ensure a tidy internal layout.
Enclosure Finishing:
The enclosure is prepared for final assembly, including optional steps like painting or applying a powder coat finish.
Surface preparation, such as sanding with #220 grit sandpaper, is recommended before painting to ensure durability and a professional look.
Testing and Troubleshooting:

Initial Testing:
Upon assembly, the pedal is powered up to check for proper voltage levels and continuity across the circuit using a multimeter.
The guide recommends comparing these readings with expected values to quickly identify any discrepancies.
Functional Verification:
Audio tests are performed to confirm the pedal’s distortion characteristics, tone control functionality, and overall signal integrity.
Detailed test documentation, including images (Pedal_ON_1.jpeg, Pedal_ON_2.jpeg) and video footage (Test.mov), ensures every aspect of the build is verified.
Troubleshooting Procedures:
A comprehensive troubleshooting chart (TROUBLESHOOTING CHART.jpg) is provided to diagnose common issues like misoriented components or cold solder joints.
Additional schematic component tests help verify that each section of the circuit performs as expected.
Documentation and Quality Assurance:

Throughout the build, every step is thoroughly documented with photos, videos, and checklists as recommended by the GGG guide.
This extensive documentation not only aids in the initial build process but also serves as a valuable reference for future repairs or modifications, ensuring the project remains replicable and maintainable.




<h2>🛠️ Tools Needed:</h2>

Soldering iron and stand

Solder

Small side cutters and wire strippers

Hookup wire (24 gauge stranded, insulated)

Multimeter

Magnifying glass (optional)

Close-in bright light (desk lamp)

<h2>🔧 Assembly Steps:</h2>

<b>Sockets (if used):</b> Solder any IC sockets first.

<b>Resistors:</b> Solder all resistors in place.

<b>Capacitors:</b> Solder all capacitors.

<b>Diodes and Transistors:</b> Solder diodes and transistors.

<b>Integrated Circuits (ICs):</b> Solder ICs last.

<h2>🛡️ Enclosure Preparation (Optional):</h2>

<b>Painting the Enclosure:</b>

Optionally paint and label the enclosure.

A powder coat finish is recommended for durability.

Smooth the surface with #220 grit sandpaper before painting.

<h2>🔌 Mounting and Wiring:</h2>

<b>Mount the PCB:</b> Secure the PCB inside the enclosure.

<b>Wire Off-Board Components:</b> Connect jacks, switches, and pots following the provided wiring diagram.

<h2>✅ Testing:</h2>

Conduct tests to ensure the pedal functions correctly:

Refer to test images: Pedal_ON_1.jpeg and Pedal_ON_2.jpeg.

Watch the test video: Test.mov.

Use the troubleshooting chart (TROUBLESHOOTING CHART.jpg) and schematic component test check (schematic component test check.png) for reference.

<h2>📸 Results:</h2>

<b>Photos of the Assembled PCB and Pedal:</b>

PCB: PCB_populated.jpg, PCB_unpopulated.jpg

Pedal: Pedal_assembled_1.jpeg, Pedal_assembled_2.jpeg, Pedal_assembled_3.jpeg

<b>Test Results:</b>

Images: Pedal_ON_1.jpeg, Pedal_ON_2.jpeg

Video: Test.mov
