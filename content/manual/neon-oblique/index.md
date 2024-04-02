---
title: 'Neon-Oblique'
date: 2023-08-21T12:00:00
weight: 14
---

- [Overview](#overview)
  - [MOAR COWBELL!](#moar-cowbell)
  - [Little Pig](#little-pig)

## Overview

Neon-Oblique modules are intended to be experimental releases of in-progress work that could benefit
from public feedback. A kind of beta release set.

Neon-Oblique modules are subject to change, but patch breaking changes will be documented.

Bug reports & feedback can be submitted on the [DanTModules discussion board](https://github.com/Miff-Real/DanTModules-Manual/discussions).

### MOAR COWBELL!

This module produces bell-like sounds using a combination of waveforms, frequencies, filters,
envelopes and effects.

![MOAR COWBELL!](https://library.vcvrack.com/screenshots/200/DanTModules/MoarCowbell.png)

The way in which these frequencies interact is not linear and can be a bit temperamental, extreme
modulation is not recommended.

It is also possible to create a feedback loop with certain settings, so there is a `Panic` button at
the bottom of the module which should reset the audio buffer if required.

All the CV inputs are calibrated to +-5volts and are added to the knob value, the result is clamped
to the knob extents.

### Little Pig

This module is an experimental feedback distortion.

![Little Pig](https://library.vcvrack.com/screenshots/200/DanTModules/LittlePig.png)

The controls are as follows (left to right, top to bottom):

* `Snuffle` - Input signals are amplified, this acts like a compressor/limiter for the input
* `Grunt` - This is the amount of distortion applied to the input signal
* `Snort` - This is basically a gain/volume for the distorted signal part of the output
* `Snout` - This is a mix/volume for the feedback, at minimum there won’t be much feedback, at
  maximum you will likely get a massive howl
* `Squeal` - This is the target feedback frequency, the input is volt/octave, it really depends on
  the input signal as to what effect this has, sometimes it can enhance the frequency, sometimes it
  can act like a filter
* `Pig Power!` - This is just an active switch to turn the distortion & feedback on and off
* `Clean Filth` - This button resets the internal buffers, this can be useful if you have pushed the
  feedback too far and have blown out the audio channels (ie. the module has stopped processing the
  input signal)
* `Audio input` yellow port - this is the signal input
* `Oink!` magenta port - this is the distorted signal + feedback output
* `Neat Trotters` switch & LED - This is basically a clip feature that will limit the output to
  10volts peak to peak, the LED will be red when clipping is happening, note that when on, this is
  still applied even when distortion and feedback are not active

All the CV inputs are calibrated to +-5volts and are added to the knob value, the result is clamped
to the knob extents.
