# Wiring

After [crafting](./crafting.md) the tableau is physically constructed, painted and has LED chains in place. These chains will be left with trailing wires where they have been cut. The next job is connecting a voltage to these trailing wires.

The components used are common to audio or 12V automotive wiring. They are very well-suited for non-specialists to use, requiring just fingers, a screwdriver, pliers or a crimping tool rather than a soldering iron.

# Circuit Designs

We have used two types of chains in our constructions...

- Colour-controllable LEDs
- Straw-hat single-color LEDs

The straw-hat LEDs are cheapest. They are found in battery-powered christmas lights. In our 'static' pieces the straw-hat chains are permanently lit. In our 'animated' pieces, different areas of straw-hat LEDs power on and off according to programmed sequences to give the illusion of movement.

This has led to three distinct circuit designs in our catalog.

- A **static** circuit - single-colour bulbs lit permanently
- An **animated** circuit - single-colour bulbs lit in a sequence
- An **addressable** circuit - any colours sent to controllable LEDs

Every build begins by configuring a safety wire as described below. Different instructions are then provided to build each style.

## Safety Wire

All our pieces are provided with an unregulated DC voltage of around 5V. A safety wire with spade connectors and a 1A safety fuse is constructed for each piece to connect to power and to isolate it from other pieces.

Parts:

- 1M 22AWG Red/Black Copper speaker wire
- 2 Male 6.3mm Spade connector crimps
- Automotive fuse holder (self-stripping)
- 1A Automotive fuse

First peel apart about 10cm of red and black speaker wire at each end of the 1m length. Strip the insulation from all four separated ends of the speaker wire, leaving the strands showing. Crimp insulated male 6.3mm spade connectors to the strands at one end. At the other end, snip through the red wire about 5cm from the end, and join the two pieces back together using a self-stripping automotive fuse holder. Finally add a 1A fuse which will reconnect the red wire and act as a safety cutout.

The end of the 'safety wire' with male spades will connect to female spades constructed during the later [powering stage](./powering.md). The end with loose strands will be screwed into a terminal block in the next ([voltage regulator stage](#voltage-regulator)).

# Animated Circuit

- NodeMCU V2 flashed with Micropython
- TPIC6B595N Shift Register
-
