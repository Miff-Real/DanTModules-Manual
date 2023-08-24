---
title: 'DanTModules - Manual'
date: 2018-11-28T15:14:39+10:00
weight: 1
---

- [Neon-Oblique Modules](#neon-oblique-modules)
- [Nu-Metal Modules](#nu-metal-modules)
  - [Nu-Metal settings](#nu-metal-settings)
  - [Nu-Metal Controls \& Concepts](#nu-metal-controls--concepts)
- [Common Controls \& Concepts](#common-controls--concepts)
  - [Global Plugin Settings](#global-plugin-settings)
  - [Themes](#themes)
    - [Objectively Blue](#objectively-blue)
    - [Superficially Deep](#superficially-deep)
    - [Magical CV](#magical-cv)
  - [CV Param Mode](#cv-param-mode)
    - [Offset](#offset)
    - [Follow](#follow)
    - [Attenuate](#attenuate)
  - [CV Input Slew](#cv-input-slew)
  - [Clamp CV Values](#clamp-cv-values)

## Neon-Oblique Modules

* Neon-Oblique modules were introduced as of plugin version `2.4.30`
* Neon-Oblique modules are *EXPERIMENTAL*, as such there is little to no documentation and module
  features & functions are subject to change

## Nu-Metal Modules

* Nu-Metal modules were introduced as of plugin version `2.4.1`

### Nu-Metal settings

![Common NuMetal menu](/DanTModules-Manual/images/numetal-menu.png)

Nu Metal modules have their own plugin settings, which are saved to the file `DanTNuMetal.json`.

### Nu-Metal Controls & Concepts

* `Port Type Colours` will toggle the port type colours
  * inputs are slightly brighter than outputs
  * multi purpose ports match the panel colour
    ![General ports](/DanTModules-Manual/images/nm-p-any.png)
  * red = audio ![Audio ports](/DanTModules-Manual/images/nm-p-aud.png)
  * yellow = volt per octave ![Volt per Octave ports](/DanTModules-Manual/images/nm-p-vpo.png)
  * magenta = reset ![Reset ports](/DanTModules-Manual/images/nm-p-rst.png)
  * aqua = clock ![Clock ports](/DanTModules-Manual/images/nm-p-clk.png)
  * blue = trigger ![Trigger ports](/DanTModules-Manual/images/nm-p-trg.png)
  * dark blue = gate ![Gate ports](/DanTModules-Manual/images/nm-p-gat.png)
  * green = modulation ![Modulation ports](/DanTModules-Manual/images/nm-p-mod.png)
  * rainbow = polyphonic

* `Coloured Knobs` will toggle knob type colours
  * DanT blue = general knobs ![General knobs](/DanTModules-Manual/images/nm-k-any.png)
  * green = uni or bi polar knobs ![Uni/Bi-polar knobs](/DanTModules-Manual/images/nm-k-pol.png)
  * grey = attenuvertor knobs ![Attenuvertor knobs](/DanTModules-Manual/images/nm-k-att.png)

* `Knob Displays` will toggle the knob value and CV display
  * unipolar knobs have a green value arc and a yellow CV arc (if CV control is offered)
    ![Unipolar knob display with CV](/DanTModules-Manual/images/dant-nm-uni-kd.gif)
  * bipolar knobs have a positive green and negative red arc, with a yellow CV arc (if CV control is
    offered)
  * attenuvertor knobs have a dark arc with notches for values of `-2`, `-1`, `0`, `1`, `2` (where
    offered)

* `Displays Lit` will toggle the knob display being full brightness

* `Light Panel Text` will toggle between dark and light panel elements

* `Panel Colour` allows you to set a custom colour for the panels

* `Reset Appearance` resets all the above settings to their default values

## Common Controls & Concepts

### Global Plugin Settings

Some modules in the plugin have the ability to save a setting as default, this will determine its
value when adding the module to a patch in future

Settings like this will be saved to a `Rack2\DanTModules.json` file

You can edit this file directly to change the default settings, though do ensure the edits are valid
JSON

You can also delete the file to reset the plugin defaults

### Themes

All modules in the plugin (except Chromakey) have a right-click context menu option where the module
and plugin default theme can be selected

The plugin default theme is saved to `DanTModules.json` under the key of `defaultTheme` with a value
of `0` to `2`

#### Objectively Blue

This is the original and default yellow on blue theme of the plugin

This themes settings value is `0`

#### Superficially Deep

This is an alternative darker theme of orange on navy

This themes settings value is `1`

![Superficially Deep Theme](/DanTModules-Manual/images/dantmodules-deep.png)

#### Magical CV

This is a special theme of black on custom colour panels, where the panel colour is controlled by
the [Chromagica](DanTModules-Manual/chromagica/) module

This themes settings value is `2`

![Magical CV Theme](/DanTModules-Manual/images/dantmodules-magic.png)

### CV Param Mode

The CV Param Mode controls how a CV signal input interacts with the related Parameter

It has 3 different modes:

#### Offset

The CV signal is simply added to the current parameter value

#### Follow

The parameter value will be directly set to the CV signal value, causing the control to move
autonomously, also meaning that the control cannot be changed by the user while the CV input is
connected

#### Attenuate

The CV signal input will be attenuated by the current parameter value

If the parameter is bi-polar then the value can be attenuverted

### CV Input Slew

This option allows a module to apply a slew to all of its CV inputs and can be used to prevent audio
artifacts caused by abrupt changes in parameter values

A slew value of `None` will disable this option, otherwise the slew length is set in milliseconds,
from `1` to `100`

### Clamp CV Values

Depending on the [CV Param Mode](#cv-param-mode), the resulting value may fall outside the range of
the parameter

When this option is enabled, this value will be clamped to the parameter range

Disabling this option will allow values to exceed their parameter ranges
