# DanTModules Changelog

## 1.1.0

* **TMNT**
  * **NEW MODULE:** Timed Mutating Non-Linear Triggers
  * A sequencer of sorts, outputs 19 different sets of triggers & 3 `0-10 volt` CV values
  * Has 64 steps, with CV control of X&Y BPM, X&Y Reset, run Direction, step Activation, Mutation type & direction and Shift direction
* **Visual Updates**
  * Minor changes to WAVULIKE panel to match with TMNT
  * Updated screws to look like Befaco Knurlies, because they are awesome

## 1.0.4

* **WAVULIKE**
  * **NEW: Adds LEDs for Amp & Clip**
  * Re-Scale Amplitude CV input from +10 volts to +-5 volts

## 1.0.3

* **WAVULIKE**
  * Bug Fix: https://github.com/Miff-Real/DanTModules-Manual/issues/2
  * Updates to the [Manual](https://github.com/Miff-Real/DanTModules-Manual)

## 1.0.2

* **WAVULIKE**
  * **NEW: Adds param control behaviors**, knobs and sliders can either follow the CV inputs as before, or can act as an offset for the CV input
  * **NEW: Adds CV Input Slew options**, the speed of the slew can now be set to `None`, `1ms`, `5ms`, `10ms`, `25ms`, `50ms` or `100ms`
  * **NEW: Adds option to disable DC Offset filter**
  * **NEW: Adds antialias option**, implemented as `8x` oversampling
  * Correct position of Clip Output switch
  * Various internal code refactors & standards implemented to aid future maintenance, potentially also minor performance gains

## 1.0.1

* **WAVULIKE**
  * **NEW: Adds an LFO Mode**, now you can create low frequency waveforms that shift over time, to modulate other modules in interesting ways
  * Corrects a display bug in the visualization screen where the right most part of the waveform was not wrapping to the first point correctly
  * Uses Rack defined Maths & DSP functions in place of C++ `std` functions to improve performance
  * Adds internal slew limiters to the Point control and Q control inputs to prevent clicks in the output audio when the input CV jumps (eg, Sample & Hold, or Square LFO)
  * Adds internal high pass filter at 15Hz to compensate for DC offset in the output

## 1.0.0

* Initial release, includes **WAVULIKE** module
