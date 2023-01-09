# DanTModules Changelog

## 2.3.6
* **Schmitt Triggers**
  * All triggers are now properly implemented as Schmitt Triggers.
  * As per the VCV SDK Docs:
  > Turns HIGH when value reaches a threshold (default 0.f), turns LOW when value reaches a threshold (default 1.f).
  * This should mean that all trigger CV inputs should be tolerant of "analogue" style triggers (a modeled pulse wave for example).
  * This might change behavior for previously saved patches in how manual trigger buttons work when their corresponding CV input is connected, if the CV does not fall back below the threshold, pressing the button will have no effect because the schmitt trigger will consider the previous trigger as still active.

## 2.3.4 **BrightIdea bug fix**
* **Bright-Idea**
  * Saving the default parameters via the context menu should now work correctly

## 2.3.3 **The Chroma Update**
* **NEW MODULES!**
  * **Chromagica** enables CV control over the **A**mount of **R**ed, **G**reen and **B**lue chroma used by the new Magical CV theme
  * **Chromakey** a resizable & recolourable blank panel that can be used for green-screen effects in your streaming or video editor
* **Themes**
  * **Superficially Deep** A new darker theme
  * **Magical CV** A theme with customizable panel colour
* **Plugin Settings**
  * The plugin will now create a `Rack2\DanTModules.json` to save plugin-wide settings
* **Bright-Idea**
  * New context menu options enable you to set default module behaviors and parameter values
* **Nonaquant**
  * Now has memory banks! 16 for the module, saved to the patch, and 16 for the plugin saved to the settings file (and shared between all instances of Nonaquant)
  * Polyphonic inputs allow you to load a memory bank with a trigger to the corresponding channel
  * Context menu option to clear all selected notes

## 2.3.2 **The Bright-Quant Update**
* **NEW MODULES!**
  * **Bright-Idea** CV control VCV Rack settings
  * **Nonaquant** Polyphonic 9 octave quantizer
* **Kanal**
  * The previous antialiasing implementation was total bologna, this has been updated, but is currently still fairly ineffective. The option is off by default for this reason and due it it being CPU intensive

## 2.3.0 **VCV Rack 2 Update**
* **NEW MODULES!**
  * **pKorre** CV source based on correlation between two signals
  * **Kanal** Waveshaper
  * **Bily G8s** Gates Generator
* **Visual Updates** New panels, knobs & port designs for V2
* **Right-click menus updated**
  * All modules now have a CV Param Mode menu option
    * `Offset` The CV value will be added to the param value
    * `Follow` The param will change automatically to the CV value
    * `Attenuate` The CV value will be attenuated by the param control, if the param is bi-polar then the value will be attenuverted
  * All modules except 5Splice now have a Clamp CV Values menu option
    * When active, this will ensure that CV values are restricted to within the params normal operating interval (ie. the minimum and maximum values of the param control)
    * Deactivating this option might reduce the modules CPU usage, but means that extraordinary CV values (typically < -5 volts & > 10 volts) can cause param values to exceed their normal operating interval, which can both be intended (for example making a BPM param on the TMNT module exceed 1000) and cause unintended effects, or worst case potentially cause other modules to function incorrectly
* **WAVULIKE**
  * Added factory presets
  * Frequency read-out in context menu fixed to 3 decimal places
  * **New Feature**: Auto-Duck. When active (on by default) will duck the internal VCA for a few milliseconds when the number of active points changes. This ensures there is no audible click when the waveform changes shape.
* **TMNT**
  * New switch graphics
  * Added CV inputs to trigger manual X & Y steps forwards & backwards
  * Added a button & CV input to just randomise the steps
  * Added factory presets
* **5Splice**
  * Added example slew presets
  * Increased maximum window slew time possible

## 1.2.3 **The Legibility Update**

* **Visual Updates**
  * New port graphic, rendered as a hexnut
  * Updated knob graphics, added definition
  * All panels updated to add text shadows
* **WAVULIKE**
  * Exact frequency added to right-click context menu. Note: this only updates when the menu is opened, it does not continuously update if the frequency is being modulated

## 1.2.2

* **5Splice**
  * **Bug:** Fixed potential run away code that would hang VCV when channel A or E were not connected in Ping-Pong mode

## 1.2.1

* **5Splice**
  * **NEW: Modes, change how the mixer window shifts between the signals**
  * Chose from Forward, ForwardX2, Backward, BackwardX2, PingPong, Random
  * Input to modulate the mode, CV value is added to the current parameter value

## 1.2.0

* **5Splice**
  * **NEW MODULE:** Window mixer for up to 5 channels with it's own slew
  * Connect up to 5 input signals and a trigger
  * Each trigger will cause the "window" to shift to the next input
  * Outputs both the mix signal and a 0-10 volt window signal
  * Has a built-in slew that interpolates between the previous and next signal passing through the window
  * Slew can be deactivated or set to a maximum of 44,100 samples (1 second at 44.1k sample rate)
  * Can mix both audio and CV signals, why not try audio rate triggers too?

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
