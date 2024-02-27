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

PolySplice is a polyphonic version of the original [5Splice](/DanTModules-Manual/manual/5splice/)
module, a "window mixer" with up to 16 inputs, 6 different modes, an internal slew, a window signal
output and polyphonic output modes.

![NuMetal-PolySplice](https://library.vcvrack.com/screenshots/200/DanTModules/PolySplice.png)

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
* Channels knob
* Channels CV input
* Channel LEDs
* Start channel knob
* Start channel CV input
* Window output
* Polyphonic mode switch
* Signal output
* Output attenuvertor

### Basic operation

* You need at minimum two channels to get useful outputs.
* Each channel with a signal is represented by one of the LEDs.
  * Channels with an input signal will be lit green.
  * Channels without an input will not be lit.
  * The currently selected channel will be brightly lit.
  * Channels that are inactive due to the Channels parameter & the Start Channel parameter will be
    red.
* On each trigger a new channel will be selected to be the output based upon the current mode:
  * **Forwards**
  * **Forwards by 2**
  * **Backwards**
  * **Backwards by 2**
  * **Ping-Pong**
  * **Random**
* The Channels parameter can be used to reduce the number of channels which are switched between.
  If the Channels parameter value is greater than the number of inputs, it will have no effect.
* The Start Channel parameter value can be used in conjunction with the Channels parameter to
  create a sub-group of channels to switch between. If the sub-group extends beyond the number of
  inputs, the selections will wrap around to channel 1.
* When in Ping-Pong mode, the mode title will include an arrow to indicate the current direction,
  and there will be a small button to manually change the direction.
  ![Ping-pong direction manual button](/DanTModules-Manual/images/polysplice-pingpongbutton.png)
* When the selected channel is changed, the slew will be applied between the previous and next
  channel values. There is a light which will be lit when the slew is active.
  ![Slew active light](/DanTModules-Manual/images/polysplice-slewlight.png)
* On any reset trigger, the Start Channel parameter value will determine which channel becomes
  active, and any current slew will be interrupted.
* The window output will be `0.5 volts` per channel, e.g. if channel `3` is selected, the window
  output will be `1.5 volts`, if channel `16` is selected, the window output will be `8 volts`.
* The output will be the selected channels value affected by the output attenuvertor.
* There are two extra polyphonic modes:
  * `Inputs incremental` the number of channels output will match the number of input channels.
    Channel `1` will be the selected channel, subsequent channels will have the value of the next
    channel, and wrap back to channel `1`.
  * `All normalled` all 16 channels will output the currently selected channel value affected by the
    output attenuvertor.
