Custom Touch Key Pad — MIDI Keypad PCB

A custom-designed MIDI keypad PCB created using KiCad. This project combines capacitive touch controls, physical input components, and an ESP32-S3 microcontroller to create a compact controller intended for use with MIDI-compatible music software.

Project status: PCB design completed.

Project Overview

The goal of this project was to design a custom MIDI keypad from its electrical schematic through its printed circuit board layout. The design brings multiple input controls together on one PCB, allowing the device to send musical control inputs to compatible software.

The PCB was designed in KiCad, including the schematic, component footprints, board outline, and routed connections. Special attention was given to component placement and trace routing to create a more organized layout.

<img width="751" height="592" alt="image" src="https://github.com/user-attachments/assets/82578f06-824a-4add-8db3-00fbbcd7261a" />


Features and Components

The design incorporates the following components and features:

- ESP32-S3 microcontroller: The controller intended to process inputs and communicate with compatible MIDI software.
- Capacitive touch pads: Touch-sensitive inputs intended to trigger musical notes.
- Rotary encoder: A rotary input for controlling a parameter.
- Slider potentiometers: Physical controls intended for continuous MIDI parameter adjustments.
- RGB LEDs: Visual feedback using addressable LEDs.
- Custom PCB layout: A board designed to accommodate the components and their electrical connections.

The intended MIDI workflow is for the keypad to send control messages to a compatible host device, such as a computer or Android phone or tablet. The host's MIDI-compatible software generates the sound; the PCB itself does not require a built-in speaker.

<img width="709" height="697" alt="image" src="https://github.com/user-attachments/assets/0f136408-302b-4842-af1f-2611cc9b60fe" />


Design Process

1. Schematic and Footprint Assignment

The project began with creating the electrical schematic in KiCad and assigning footprints to the components. This established the electrical connections and the physical component layouts needed for PCB design.

One of the main challenges was creating a custom footprint for the capacitive touch pads. My initial attempts did not transfer correctly into the PCB Editor, so I recreated the footprint several times and used online tutorials to troubleshoot the problem. I eventually resolved the issue and successfully incorporated the footprint into the PCB design.

2. PCB Outline and Layout

After completing the schematic and footprint assignments, I moved to the PCB Editor and drew the board outline using the "Edge.Cuts" layer.

I then began placing the components and routing the electrical connections. The first routing attempt produced multiple design-rule errors, so I reviewed the layout and adjusted the component positions.

3. Routing and Layout Improvements

Routing the PCB was one of the most time-consuming parts of the project. Some connections were difficult to route cleanly, and certain traces were too close together. Rather than making only small adjustments, I reorganized much of the component placement, moving components around the board to improve the routing paths and make the layout more organized.

After several hours of routing and rearranging components, I completed the board's trace routing and reduced the remaining design-rule issues. I also compared the remaining checks with the project guide to understand which reported issues were expected for this design.

<!-- ADD PICTURE 3 HERE: Add a screenshot of the final routed PCB, with the traces clearly visible. -->"Final routed PCB" (images/pcb-routed.png)

4. Three-Dimensional PCB View

The PCB design can also be inspected using KiCad's 3D Viewer. This view helps visualize the board and the placement of components in three dimensions, rather than only as a flat layout.

<img width="1092" height="727" alt="image" src="https://github.com/user-attachments/assets/230497d7-188a-4cbf-af96-7c784c396fb9" />

<img width="1278" height="739" alt="image" src="https://github.com/user-attachments/assets/9cce9e1f-d244-4a9a-b5cd-bc6240613871" />

<img width="1155" height="495" alt="image" src="https://github.com/user-attachments/assets/dc87d34e-6da7-4afe-bdd0-8505673a1f61" />



Software and Tools

- KiCad: Electrical schematic, footprint assignment, PCB layout, routing, and 3D visualization.
- ESP32-S3: Microcontroller selected for the keypad design.

Challenges and What I Learned

This project gave me practical experience with the PCB design process, from schematic creation to board layout and routing.

The most significant challenge was getting the custom capacitive touch-pad footprint working correctly. I learned that a footprint must be properly created and available to the PCB Editor before it can be used in the board layout.

I also learned how strongly component placement affects PCB routing. My first layout resulted in many design-rule errors, but rearranging the components created better routing paths and a cleaner board. This taught me to consider both electrical connections and physical layout when designing a PCB.

Working through these problems improved my understanding of KiCad, footprints, board outlines, copper traces, design-rule checks, and the relationship between a schematic and a physical PCB.

Final Result

The PCB design phase of the MIDI keypad project is complete. The schematic was created, component footprints were assigned, the board outline was drawn, and the electrical connections were routed. The layout was reorganized to improve trace routing and component placement, and the design was reviewed using KiCad's design-rule checks.

The completed design represents the PCB layout for a custom MIDI keypad with capacitive touch inputs, a rotary encoder, slider potentiometers, RGB LEDs, and an ESP32-S3 microcontroller.



This project was based on the MIDI-Keypad guide by KaiPereira.

- Original project guide: https://github.com/KaiPereira/MIDI-Keypad/blob/master/README.md

The original guide was used as a reference for the design process. The PCB layout and troubleshooting work documented here reflect my own progress through the project.


Check out my BOM and my project cost is coming along $37. I am willing to pay $7 from my pocket as long as I can get the funding of $30(or $33 with margin).
