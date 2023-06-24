---
title: 'Nonaquant'
date: 2023-06-22T12:00:00
weight: 8
---

- [Overview](#overview)
  - [Basic Operation](#basic-operation)
  - [Memory Banks](#memory-banks)
  - [Note Readout](#note-readout)

## Overview

**`40hp`**

Nonaquant is a 16 channel polyphonic 9 octave quantizer

![Nonaquant](/images/nonaquant.png)

### Basic Operation

Send (1 to 16 channels) CV signals to the `IN` input and get `1volt/octave` quantized CV signals
back from the `QUANT` output

If the `TRIG` input is connected, the quantized note will only change on `> 0 volts` triggers

The number of channels connected is displayed by the dynamic text below the `IN` input

The All Seeing Eye knob at the top left controls which channel is visualized by the lights and knobs

Click the keys to activate the desired notes, the notes selected apply to all channels

When the `BEND` and `PORTO` inputs are NOT connected, the knob controls this parameter and applies
it to all channels, when the inputs are connected, each channel takes its value directly from the CV
signal overriding the knob value

`BEND` will add or subtract semitones to the quantized note, you can use an envelope, for example,
to create a bend effect

`PORTO` will introduce a slew to note changes up to `1 second` long

The `TRANSPOSE` inputs are all monophonic and activate on `> 0 volts` triggers

The global `TRANSPOSE` will move all notes up or down, notes can move from one octave to the next

The individual octave `TRANSPOSE` will move only the notes in that octave, notes that are moved past
the top or bottom of the octave, will be lost

### Memory Banks

Nonaquant has 16 module & 16 plugin memory banks

These banks store the set of active notes

Module memory banks are per instance of Nonaquant, and are saved in the patch

Plugin memory banks are shared between all instances of Nonaquant, and are saved in the
`Rack2\DanTModules.json` file

The right-click context menu has options that allow you to save the currently selected notes into a
memory bank

There are also options to manually load a memory bank, or clear all the currently selected notes

There are two separate polyphonic inputs that allow you to load a specific memory bank, a trigger on
a channel will immediately load the corresponding memory bank

### Note Readout

You can enable the note readout via the right-click context menu

When enabled there will be a display below the keys that show the quantized note selected for each
active channel in the format of `channelNumber[NoteName OctaveNumber]`

![Note Readout](/images/nonaquant-readout.png)
