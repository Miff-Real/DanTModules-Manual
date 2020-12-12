# DanTModules Changelog

## 1.0.1

* **WAVULIKE**
  * **NEW: Adds an LFO Mode**, now you can create low frequency waveforms that shift over time, to modulate other modules in interesting ways
  * Corrects a display bug in the visualization screen where the right most part of the waveform was not wrapping to the first point correctly
  * Uses Rack defined Maths & DSP functions in place of C++ std functions to improve performance
  * Adds internal slew limiters to the Point control and Q control inputs to prevent clicks in the output audio when the input CV jumps (eg, Sample & Hold, or Square LFO)
  * Adds internal high pass filter at 15Hz to compensate for DC offset in the output

## 1.0.0

* Initial release, includes **WAVULIKE** module
