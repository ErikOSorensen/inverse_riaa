#  Inverse RIAA filter

Inverse RIAA filter for testing phono preamps. If we want to test phono preamps with
a soundcard interface, we need a lot of attenuation of the soundcard output - and we
would also like to invert the RIAA filtering that is part of an ordinary phono 
preamp such that the soundcard input receives a signal which, under ideal operation,
has a constant amplitude as the frequency varies.

## The schematic

The design is a simple and direct implementation of the suggestion of Lipshitz and Jung (1980),
in their paper "A High Accuracy Inverse RIAA Network" (Figure 3). I have adapted it by paralleling
some parts for greater accuracy.

![One channel of the filter](./graphics/schematics_page1.png)

## First physical build

![Picture of assembled filter in a box](./graphics/iriaa-box.jpg)

This is a passive filter. I have built one into a Hammond 1455N1201BK extruded box,
with isolated (stereo) BNCs in and out. There is an option to add 20 dB of attenuation
for testing MC phono preamps.

For this first build I have used Susumu 0.5% resistors and Murata 1% capacitors.


## Characterization

Measurement of the attenuation and comparison to what we should expect (calculated
in LT spice) indicates that the filter is within 0.2 dB of the correct curve over
most of the frequency range.

![Measurements with Analog Discovery 2](./graphics/deviations.png)

Note that the measurements (in the MM path) were taken with an Analog Discovery
2, which only has a 14 bit ADC, so there is a lot of noise and quantization
error at the lower frequencies where attenuation is greatest. With the AD2, the
dynamic range is not sufficient to test the MC path, but since that only
involves a single extra resistor (which can be verified with a DMM), that
shouldn't involve any additional concerns.