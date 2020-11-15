# Morecambe Mini Illuminations

<p style="text-align:center">
<img src="../images/logo.png" style="height:250px"  />
</p>


Morecambe has a long history as a holiday-goers destination. In the winter months this used to mean _illuminations_. The old illuminations shown along the Morecambe Promenade can still be seen in antique postcards. 

<p style="text-align:center">
<img src="../images/postcard.jpg" style="height:250px"/>
</p>

---

We decided to restart this long-standing tradition, but with _Mini_ Illuminations, made by community members using modern low-voltage electronic lights and small microcontrollers for animation. 


This repository has a summary of the standard approach to constructing and deploying our mini-illuminations which we have developed over 3 years of shows and more than 60 different illuminations since November 2016.

# Build stages

We have separated instructions into sequential stages, 1) Crafting, 2) Wiring and 3) Powering. 

First, when [Crafting](build/crafting.md) the tableau is designed as vector art and sketched on a board, the baffles between coloured areas are cut and glued. Each area and its baffle-sides are painted, and holes are drilled for the insertion of bulbs.

Second, when [Wiring](build/wiring.md) separate chains of LEDs are laid within the holes of each baffled area, with trailing wires connecting back to one of three supporting circuits...
* A static circuit, providing a simple regulated voltage
* An animated circuit, with a programmable microcontroller connecting different chains to a regulated voltage according to an animated sequence
* A Microcontroller driving a chain of 5V addressable LEDs.
...and the LEDs and circuit boards are hot-glued in place from behind.

Finally, [Powering](build/powering.md) 

You can dive in to the detail of each stage by following the links in this list, or read on for more about our design philosophy.

* [Crafting](build/crafting.md): Shaping and painting the tableau
* [Wiring](build/wiring.md): Static or animated chains of LEDs
* [Powering](build/powering.md): Providing power to one or hundreds


# About the Approach

The build process is designed to be accessible. Materials and techniques are within the reach of community members in educational and informal settings. The table below contrasts the historical illuminations build with the 'Mini' process we have selected.

| Feature   | Original     | Mini                         | Explanation                                                     |
|-----------|--------------|------------------------------|-----------------------------------------------------------------|
| Bulbs     | Incandescent | LED                          | Bulbs available cheaply pre-wired on a reel, cool to the touch. |
| Material  | Metal        | Plywood, Card, Acrylic paint | Familiar craft materials, easy to work and repair               |
| Voltage   | 240V AC      | 5V DC                        | Low voltage circuit wiring without risk. 5V safe in the rain.   |
| Joints    | Soldering    | Crimping                     | Unskilled, low temperature crimping with hand tools.            |
| Structure | Welding      | Hot glue                     | Minimal hazard, easy to rework with a heat gun                  |
| Control   | PLController | Micropython                  | Learner programming language commonly used in schools           |
