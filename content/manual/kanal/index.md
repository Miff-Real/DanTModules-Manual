---
title: 'Kanal'
date: 2023-06-22T12:00:00
weight: 5
---

- [Overview](#overview)
  - [Basic Operation](#basic-operation)

## Overview

**`6hp`**

Kanal is a waveshaper that works by sculpting a *canal* out of the middle of a waveform.

![Kanal](https://library.vcvrack.com/screenshots/200/DanTModules/Kanal.png)

### Basic Operation

Send a signal to the input. The **ATT Parameter** applies gain to the signal (`-2x` to `2x`).

The **P Parameter** controls the position of the center of the canal (`-2.5 volts` to `2.5 volts`).

The **W Parameter** controls the width of the canal (`0` no effect, to `5 volts` from the bottom to
the top of the canal).

The **TB Parameter** controls the amount of *Top Boost*, this is a multiplier applied to the
waveform above the canal. Negative values will invert the waveform back into the canal.

The **BB Parameter** controls the amount of *Bottom Boost*, this is a multiplier applied to the
waveform below the canal. Negative values will invert the waveform back into the canal.

The shaped waveform is sent to the OUT output.

The X-0 output will fire a trigger when the input signal crosses `0 volts`.
