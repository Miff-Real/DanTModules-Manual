---
title: 'Kalkatron'
date: 2023-08-04T12:00:00
weight: 13
---

- [Overview](#overview)
  - [Controls](#controls)
  - [Basic operation](#basic-operation)
  - [Legacy docs from the VCV community](#legacy-docs-from-the-vcv-community)

## Overview

**`26hp`**

Kalkatron, documentation TBD.

![NuMetal-Kalkatron](/DanTModules-Manual/images/kalkatron.png)

### Controls

TODO

### Basic operation

TODO

### Legacy docs from the VCV community

![Annotated beta Kalkatron module](/DanTModules-Manual/images/kalkatron-legacy.png)

A: Input section - This is where the signal is tracked or generated.
There is a signal input with attenuvertor & offset param, and there is a signal sample trigger input
and button. When signal sample is triggered, the value at the input will be added to the offset and
displayed in the xInput box. Since the value inputs have an offset, you can set this offset to a
specific value and leave the input disconnected if you want a static value.

B: Maths section - This is where the maths operations can be performed. You can add, subtract,
multiply or divide the input signal by a specific value. Each operation has its own controls and
they all work in the same way. There is an operation trigger input and button. A value input with
attenuvertor and offset. And a sample value trigger input and button. When sample value is
triggered, the value at the input will be added to the offset and displayed in the operation box at
the bottom. When the operation is triggered, the value in the operation box will be used to perform
the operation upon the current xInput value. Note that divide by 0 is a no-op.

C: Calculation section - This is where the current calculation result = Equals is displayed. Note
that this display is affected by the output mode, output slew, output attenuvertor and output clip.

D: Mode & Output section - This is where you control the module output. The lights indicate the
currently selected output mode. There is an output mode selector knob, and input with attenvertor.
The main module output is bottom right, and it has an attenuvertor and Clip output switch. When clip
is active the output will be limited between -10.0 and 10.0. There are 6 output modes:

Floating Point - The standard calculation result
Rounded .1 - The calculation will be rounded to the nearest .1
Rounded .2 - The calculation will be rounded to the nearest .2
Rounded .5 - The calculation will be rounded to the nearest .5
Integer - The calculation will be rounded to the nearest whole number
Quantized - The calculation will be quantized to the nearest note frequency and a note display will
be shown next to the Calculation box

E: Slew section - This allows you to slew between the previous calculation result and the current
calculation result. There is a slew length knob, with an input and attenuvertor. The slew length is
in milliseconds, and has a light to show when its actively slewing the output.

F: Auto-reset & Bounds section - This area allows you to set an upper and lower bound for the output
signal. When the calculation result is out of bounds there are gates output and you can also
automatically reset the module. The switch activates auto-reset. The top row is for the upper bound
and the bottom row is for the lower bound. The gate outputs for out of bounds signals are to the
right. The other controls are the same as the operations, a value input with attenuvertor and
offset, and a sample trigger and button.

G: Reset section - This is simply a trigger input and button to reset the module, however, the reset
behaviour can be customised:

Initialize Parameters - On a reset, all the parameters will be set to their default values, the same
as if you select Initialize from the context menu

Zero Signal Value - On a reset, the xInput value will be set to 0
Zero Plus Value - On a reset, the + Plus value will be set to 0
Zero Subtract Value - On a reset, the - Subtract value will be set to 0
Zero Multiply Value - On a reset, the × Multiply value will be set to 0
Zero Divide Value - On a reset, the ÷ Divide value will be set to 0
Zero Calculation - On a reset, the = Equals calculation result will be set to 0
Reset Upper-bound - On a reset, the upper bound value will be set to the default of 10
Reset Lower-bound - On a reset, the lower bound value will be set to the default of -10
Sample Signal Value - On a reset, the xInput value sample will be triggered
Sample Plus Value - On a reset, the + Plus value sample will be triggered
Sample Subtract Value - On a reset, the - Subtract value sample will be triggered
Sample Multiply Value - On a reset, the × Multiply value sample will be triggered
Sample Divide Value - On a reset, the ÷ Divide value sample will be triggered
Sample Upper-bound - On a reset, the upper bound value sample will be triggered
Sample Lower-bound - On a reset, the lower bound value sample will be triggered
Reset Slew - On a reset, any currently active slew will be ended and the slew value will be set to
0. If the slew length is > 0 this will instigate a new slew, this is great for creating boing noises
