# Wiring

After [crafting](./crafting.md) the tableau is physically constructed, painted and has LED chains in place. These chains will be left with trailing wires where they have been cut. The next job is connecting a voltage to these trailing wires.

The components used are more usually employed for other wiring jobs, such as audio or 12V automotive wiring. They are very well-suited for non-specialists to use, requiring just fingers, a screwdriver, pliers or a crimping tool rather than a soldering iron.

# Safety Wire

Parts:

- 1M 22AWG Red/Black Copper speaker wire
- 2 Male 6.3mm Spade connector crimps
- Automotive fuse holder (self-stripping)
- 1A Automotive fuse

All our pieces are provided with an unregulated DC voltage of around 5V. A safety wire with spade connectors and a 1A safety fuse is constructed for each piece to connect to power and to isolate it from other pieces.

First peel apart about 10cm of red and black speaker wire at each end of the 1m length. Strip the insulation from all four separated ends of the speaker wire, leaving the strands showing. Crimp insulated male 6.3mm spade connectors to the strands at one end. At the other end, snip through the red wire about 5cm from the end, and join the two pieces back together using a self-stripping automotive fuse holder. Finally add a 1A fuse which will reconnect the red wire and act as a safety cutout.

The end of the 'safety wire' with male spades will connect to female spades constructed during the later [powering stage](./powering.md). The end with loose strands will be screwed into a terminal block in the next ([voltage regulator stage](#voltage-regulator)).

# Voltage Regulator

Parts:

- 3A polyethylene terminal block
- LM317T Voltage regulator
- 1KOhm 0.5W Resistor
- 1.2KOhm 0.5W Resistor
- 1 [Safety wire](#safety-wire)

Static pieces require a circuit to light their LEDs with a constant 2.7V DC. A 3A Polyethylene screw terminal block can be used in the place of a printed circuit board to compose a simple voltage regulator circuit. Makers will simply insert the components then screw the terminals shut. The terminals are also convenient to attach the voltage wires. This regulator can be constructed with just a screwdriver.

Break off 4 double-sided screw terminals. One terminal pair is for the 0V ground connection to pass through (from the unregulated DC supply to the regulated supply). The other three terminals will house the regulator's 3 pins, placing the its high-voltage pin furthest from the 0V pin.

Place the block with 4 holes uppermost which we will call holes 1-4. Unscrew every terminal on the uppermost side. Place the regulator with the numbered side towards you in the rightmost uppermost holes 2-4. You may need to bend the Regulator's legs to insert them cleanly. Insert a 1kOhm resistor between hole 3 and 2. Insert a 1.2kOhm resistor between hole 2 and 1. Screw holes 2 and 3 closed, holding the regulator and its two resistors firmly in place. Attach the red and black strands of a [safety wire](#safety-wire) into hole 1 (Ground, Black) and hole 4 (5V, Red). The strands go in beside the regulator and resistor legs and are held in place by screwing the remaining uppermost terminals closed. Finally stripped red and black wires for the outbound 2.7V DC regulated voltage can be screwed to the lowermost terminals 1 and 3. Tighten all screws to finish the circuit.

# Testing Rig

Parts:

- A red wire with crocodile clip
- A black wire with crocodile clip
- A [voltage regulator](#voltage-regulator)
- Optionally - 5V USB adaptor and USB power cable

To power a chain of LEDs in an illumination you need to connect black (0V) and red (2.7V) wires the correct way round to light the piece.

To help with this, we often attach red and black crocodile clips as the 2.7V regulated wires coming out of a [voltage regulator](#voltage-regulator). After attaching the other end of this testing rig to a 5V supply, (e.g. a Mobile phone charger) you can use the crocodile clips to light up the chains one by one by clipping onto the wires trailing from the illumination. This checks the chain is working and proves which way round the red and black wires should be connected.

# Fixing Regulator and Blocks

Parts:

- 0.5mm Heatshrink butt crimp connectors
- Red/Black 22AWG Copper speaker wire
- 2pcs PCT-218 Spring lever 'common terminal' blocks

Decide on the location of the voltage regulator on the backboard of each piece. Screw terminals should be easy to reach for maintenance. The wire between the regulator and the LED chains should be minimised. Squeeze a large blob of hot-glue on the board, and push the back of the terminal block into it, with the screw holes upwards. Hold until cooled.

Pieces have multiple differently coloured chains with two wires each to power them. We will use a PCT-218 common terminal spring level block to join multiple LED chains to 2.7V without soldering and a separate block to join the other end of the chains to the 0V ground.

Open a lever terminal at one end of a PCT-218. Insert the 0V black wire from the regulator. Close the lever and gently tug to check. The other holes of this block will be used later to connect black wires to LED ground.

Open the lever from a separate PCT-218, insert the regulator's 2.7V red wire, close the lever and tug. The other holes of this block will be used later to connect red wires to 2.7V.

# Connecting LED Chains

Christmas LED chains normally have clear cables for both supply and ground wires. We need to identify which is which, and connect red (2.7V) to one end, and black (0V) to the other.

Choose a single LED chain at a time. Find the nearest end of the chain and strip about 0.5mm of insulation from the two wires. Crimp one-half of a heatshrink butt connector onto the strands, ensuring metal to metal contact.

Measure and cut enough 22AWG red and black speaker wire to reach comfortably between the butt connectors and the spring lever blocks on the backboard. Strip 0.5mm of insulation from all four ends of the speaker wire. Peel apart the red and black for a minimum of 25mm at each end. Check the stripped ends are not touching each other.

Take the red and black wires from one end and insert them into the corresponding lever blocks on the board, powering the cable. At the other end, slide the red wire into one butt connector, and the black wire into its neigbour. If the chain lights, then the polarity is correct. Otherwise, reverse the polarity. Once the chain is lit, fully-crimp the butt connectors to make the connection to red and black permanent.

# Test rig

- USB pigtail cable
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
