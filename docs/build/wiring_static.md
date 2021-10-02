# Static Circuit

This circuit is for a simple tableau with permanently-lit coloured areas. Red-and-black speaker wire lengths are crimped to the LED chains in the board. These are inserted in spring lever blocks connecting to a 2.7V voltage regulator.

Follow the step-by-step build below.

## Make the Regulator

Parts:

- 3A polyethylene terminal block
- LM317T Voltage regulator
- 1KOhm 0.5W Resistor
- 1.2KOhm 0.5W Resistor
- 1 [Safety wire](./wiring.md#safety-wire)

The circuit will light its LEDs with a constant 2.7V DC. A 3A Polyethylene screw terminal block can be used in the place of a printed circuit board to make a voltage regulator circuit with just a screwdriver. The screw terminals also attach the power wires.

Cut a row of 4 double-sided screw terminals from the terminal block. One terminal pair is for the 0V ground connection to pass through (from the unregulated DC supply to the regulated 2.7V supply). The other three terminals will house the LM317T regulator's 3 pins, placing the high-voltage pin furthest from the 0V.

Place the block with 4 holes uppermost which we will call holes 1-4. Unscrew every terminal on the uppermost side. Place the regulator with the numbered side towards you in the rightmost uppermost holes 2-4. You may need to bend the Regulator's legs to insert them cleanly. Insert a 1kOhm resistor between hole 3 and 2. Insert a 1.2kOhm resistor between hole 2 and 1. Screw holes 2 and 3 closed, holding the regulator and its two resistors firmly in place. Attach the red and black strands of a [safety wire](#safety-wire) into hole 1 (Ground, Black) and hole 4 (5V, Red). The strands go in beside the regulator and resistor legs and are held in place by screwing the remaining uppermost terminals closed. Finally stripped red and black wires for the outbound 2.7V DC regulated voltage can be screwed to the lowermost terminals 1 and 3. Tighten all screws to finish the circuit.

# Install the Regulator

Parts:

- Red/Black 22AWG Copper speaker wire
- 2pcs PCT-218 Spring lever 'common terminal' blocks
- Hot glue gun

Decide on the location of the voltage regulator on the backboard of each piece. Screw terminals should be easy to reach for maintenance. The wire between the regulator and the LED chains should be minimised. Squeeze a large blob of hot-glue on the board, and push the back of the terminal block into it, with the screw holes upwards. Hold until cooled.

Pieces have multiple differently coloured chains with two wires each to power them. We will use a PCT-218 common terminal spring lever block to join multiple LED chains to 2.7V without soldering. A separate spring block connects them to 0V ground.

Open a lever terminal at one end of a PCT-218. Insert the 0V black wire from the regulator. Close the lever and gently tug to check. The other holes of this block will be used later to connect black wires to LED ground.

Open the lever from a separate PCT-218, insert the regulator's 2.7V red wire, close the lever and tug. The other holes of this block will be used later to connect red wires to 2.7V.

Hot-glue the blocks near each other, leaving the open holes clear for wires to be inserted.

# Connect the Chains

Parts:

- 0.5mm Heatshrink butt crimp connectors

Christmas LED chains have identical clear or green cables for both supply and ground wires. We need to identify which is which, and connect red (2.7V), and black (0V) wires back to the regulated voltage. Wiring LEDs backwards is safe, but no current will flow and they will not light.

Choose a single LED chain at a time. Find the nearest end of the chain to the spring blocks. Strip about 0.5mm of insulation from the two wires. Crimp one-half of a heatshrink butt connector onto the strands, ensuring metal to metal contact. Leave the empty half of the butt connector uncrimped.

Measure and cut enough 22AWG red and black speaker wire to extend comfortably from the butt connectors to the spring lever blocks on the backboard. Strip 0.5mm of insulation from all four ends of the speaker wire. Peel apart the red and black for a minimum of 25mm at each end. Check the stripped ends are not touching each other.

Take the red and black wires from one end and insert them into the corresponding lever blocks on the board, powering the cable. At the other end, slide the red wire into one butt connector, and the black wire into its neighbour. If the chain lights, then the polarity is correct. Otherwise, reverse the polarity. Once the chain is lit, fully-crimp the butt connectors to make the connection to red and black permanent.
