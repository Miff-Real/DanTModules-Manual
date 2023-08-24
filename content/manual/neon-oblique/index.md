---
title: 'Neon-Oblique'
date: 2023-08-21T12:00:00
weight: 13
---

- [Overview](#overview)
  - [MOAR COWBELL!](#moar-cowbell)

## Overview

Neon-Oblique modules are intended to be experimental releases of in-progress work that could benefit
from public feedback. A kind of beta release set.

Neon-Oblique modules are subject to change, but patch breaking changes will be documented.

Bug reports & feedback can be submitted on the [DanTModules discussion board](https://github.com/Miff-Real/DanTModules-Manual/discussions).

### MOAR COWBELL!

This module produces bell-like sounds using a combination of waveforms, frequencies, filters,
envelopes and effects.

![MOAR COWBELL!](/DanTModules-Manual/images/moarcowbell.png)

The way in which these frequencies interact is not linear and can be a bit temperamental, extreme
modulation is not recommended.

It is also possible to create a feedback loop with certain settings, so there is a `Panic` button at
the bottom of the module which should reset the audio buffer if required.

All the CV inputs are calibrated to +-5volts and are added to the knob value, the result is clamped
to the knob extents.
