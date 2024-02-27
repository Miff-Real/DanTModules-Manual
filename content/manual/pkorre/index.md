---
title: 'pKorre'
date: 2023-06-22T12:00:00
weight: 4
---

- [Overview](#overview)
  - [Basic Operation](#basic-operation)

## Overview

**`6hp`**

pKorre is a phase correlation meter and CV generator.

![pKorre](https://library.vcvrack.com/screenshots/200/DanTModules/PKorre.png)

### Basic Operation

This module will compare two signals and generate a CV signal based on the correlation between them.

The correlation is basically a measure of how similar the two signals are over a specific window of
time.

Send the two signals that you want to compare to the **A** and **B** inputs.

The **WIN Parameter** controls the length of time during which the signals are compared, in samples.
Smaller sample windows will work better for audio rate signals, but longer windows may give
interesting results or work better for LFO type signals.

The LED meter will show a visual representation of the calculated correlation and a CV signal
representing the correlation will be output at **COR**.

A positive correlation will occur when the two waveforms trend in the same direction on average
during the window, whereas a negative signal will occur when the two waveforms trend opposite on
average during the window.

The **INV** output will have the inverted correlation signal.

Both the **COR** and **INV** outputs can be attenuated by the **\* Parameter** and offset by the
**± Parameter**.

The EOW output will fire a trigger at the end of each comparison window.
