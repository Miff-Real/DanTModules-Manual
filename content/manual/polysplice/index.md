---
title: 'PolySplice'
date: 2023-06-22T12:00:00
weight: 11
---

- [Overview](#overview)
  - [Controls](#controls)
  - [Basic operation](#basic-operation)

## Overview

**`7hp`**

PolySplice is a polyphonic version of the original [5Splice](/manual/5splice/) module, a
"window mixer" with up to 16 inputs, 6 different modes, an internal slew, a window signal output and
polyphonic output modes.

![NuMetal-PolySplice](/images/polysplice.png)

### Controls

From top-left to bottom-right:

* Polyphonic input
* Trigger button
* Trigger input
* Mode knob
* Mode CV input
* Slew knob
* Reset button
* Slew CV input
* Reset trigger input
* Slew CV attenuvertor
* Channel LEDs
* Window output
* Polyphonic mode switch
* Signal output
* Output attenuvertor

### Basic operation

* You need at minimum two channels to get useful outputs.
* Each channel with a signal is represented by one of the LEDs, the LEDs for channels without a
  signal will be off. The selected channel LED will be lit brightly.
* On each trigger a new channel will be selected to be the output based upon the current mode:
  * **Forwards**
  * **Forwards by 2**
  * **Backwards**
  * **Backwards by 2**
  * **Ping-Pong**
  * **Random**
* When in Ping-Pong mode, the mode title will include an arrow to indicate the current direction,
  and there will be a small button to manually change the direction.
  ![Ping-pong direction manual button](/images/polysplice-pingpongbutton.png)
* When the selected channel is changed, the slew will be applied between the previous and next
  channel values. There is a light which will be lit when the slew is active.
  ![Slew active light](/images/polysplice-slewlight.png)
* On any reset trigger, channel `1` will be selected and any current slew will be interrupted.
* The window output will be `0.5 volts` per channel, e.g. if channel `3` is selected, the window
  output will be `1.5 volts`, if channel `16` is selected, the window output will be `8 volts`.
* The output will be the selected channels value affected by the output attenuvertor.
* There are two extra polyphonic modes:
  * `Inputs incremental` the number of channels output will match the number of input channels.
    Channel `1` will be the selected channel, subsequent channels will have the value of the next
    channel, and wrap back to channel `1`.
  * `All normalled` all 16 channels will output the currently selected channel value affected by the
    output attenuvertor.
