#  Inverse RIAA filter

Inverse RIAA filter for testing phono preamps. If we want to test phono preamps with
a soundcard interface, we need a lot of attenuation of the soundcard output - and we
would also like to invert the RIAA filtering that is part of an ordinary phono 
preamp such that the soundcard input receives a signal which, under ideal operation,
has a constant amplitude as the frequency varies.

![Picture of assembled filter in a box](./graphics/iriaa-box.jpg)

This is a passive filter. I have built one into a Hammond 1455N1201BK extruded box,
with isolated (stereo) BNCs in and out. There is an option to add 20 dB of attenuation
for testing MC phono preamps.

First build with the faceplate from jlcpcb had some issues:

1. The switch and the BNC connectors should have been more forward on the board, accounting for the plastic bezel.
2. The mounting holes were off by a bit and quite tight. I drilled them out to make the front panel sit flat, not pretty.
3. The grounding should of the case needs a bit more work; since the box is anodized there is not good contact throughout.
