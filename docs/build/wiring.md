# Wiring

After [crafting](./crafting.md) the tableau is physically constructed, painted and has LED chains in place. These chains will be left with trailing wires where they have been cut. The next job is connecting a voltage to these trailing wires.

# Safety Wire

All our pieces are provided with an unregulated DC voltage of around 5V. A safety wire with spade connectors and a 1A safety fuse is constructed for each piece to connect to power and to isolate it from other pieces.

- 1M 22AWG Red/Black Copper speaker wire
- 2 Male 6.3mm crimped spades
- Automotive fuse holder (self-stripping)
- 1A Automotive fuse

First peel apart about 10cm of red and black speaker wire at each end of the 1m length. Strip the insulation from all four separated ends of the speaker wire, leaving the strands showing. Crimp insulated male 6.3mm spade connectors to the strands at one end. At the other end, snip through the red wire about 5cm from the end, and join the two pieces back together using a self-stripping automotive fuse holder. Finally add a 1A fuse which will reconnect the red wire and act as a safety cutout.

The end with male spades will connect to female spades constructed during the later [powering stage](./powering.md). The end with loose strands will be screwed into a terminal block in the next ([voltage regulator stage](#voltage-regulator)).

# Voltage Regulator

Next, a circuit is added to static pieces to light its LEDs with a constant 2.7V DC. A 3A Polyethylene screw terminal block in the place of a printed circuit board can be used compose this simple circuit by inserting the components then screwing the terminals shut. The terminals are also convenient to attach the voltage wires. Makers can therefore construct the power system with just a screwdriver rather than a soldering iron.

Break off 4 pairs of screw terminals. Leave a terminal pair empty for the 0V ground connection to pass through (from the unregulated DC supply to the regulated supply). The other three terminals will house the regulator's 3 pins, placing the its high-voltage pin furthest from ground.

Place the block with 4 holes uppermost which we will call holes 1-4. Unscrew every terminal on the uppermost side. Place the regulator with the numbered side towards you in the rightmost uppermost holes 2-4. You may need to bend the Regulator's legs to insert them cleanly. Insert a 1kOhm resistor between hole 3 and 2. Insert a 1.2kOhm resistor between hole 2 and 1. Screw holes 2 and 3 closed, holding the regulator and its two resistors firmly in place. Attach the red and black strands from a [safety wire](#safety-wire) to hole 1 (Ground, Black) and hole 4 (5V, Red) beside the regulator and resistor legs and screw the remaining uppermost terminals closed. Finally stripped red and black wires for the outbound 2.7V DC regulated voltage can be screwed to the lowermost terminals 1 and 3. Tighten all screws to finish the circuit.

# Testing Rig

To power each chain of LEDs you need to connect black and red wires the correct way round which will then be attached to 0V (Black) and 2.7V (Red) to light the piece.

To help with this, we often attach red and black crocodile clips to the 2.7V regulated wires coming out of a [voltage regulator](#voltage-regulator). You can attach this testing rig to a 5V supply, then use the crocodile clips to light up each chain. This checks the chain is working and proves which way round the red and black wires should be connected.

# Connecting LED Wires

Parts for the regulator

- 3A polyethylene terminal block
- LM317T Voltage regulator
- 1KOhm 0.5W Resistor
- 1.2KOhm 0.5W Resistor

The components used are more usually employed for other wiring jobs, such as audio or 12V automotive wiring. They are very well-suited for non-specialists to use, requiring just fingers, a screwdriver, pliers or a crimp-crushing tool. They are as follows...

- 0.5mm heatshrink butt crimp connectors
- Red/Black 22AWG copper speaker wire
- PCT-218 spring lever common terminal blocks
- Male 6.3mm blade insulated crimp connector

# Test rig

- USB
- LM317T Voltage regulator
- Crocodile clips
- Female 6.3mm blade t-tap sockets

We have used two types of chains in our constructions...

- Battery-operated straw-hat LED chains
- Colour-controlled addressable LED chains

### Battery-operated chains

In the case of battery operated chains, a regulated voltage can be provided across the two wires at the end, no matter how many LEDs in the chain. The LEDs we were using were regulated at around 2.7V

To create this regulated voltage, we use an

- A **static** circuit- a fixed regulated voltage lighting all the bulbs
- An **animated** circuit - a microcontroller switches the regulated voltage in a programmed sequence
- An **addressable** circuit - a microcontroller sends messages to a chain of addressable LEDs.

...and the circuit boards are hot-glued in place from behind.

## Animated Circuits

- NodeMCU V2 flashed with Micropython
- TPIC6B595N Shift Register
-
