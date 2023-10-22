---
title: 'Chromakey'
date: 2023-06-22T12:00:00
weight: 10
---

- [Overview](#overview)
  - [Basic Operation](#basic-operation)
  - [Colour \& RGB Lock](#colour--rgb-lock)

## Overview

**`variable-hp`**

Chromakey is a resizable & recolourable blank panel

![Chromakey](/DanTModules-Manual/images/chromakey.png)

### Basic Operation

Once added to a patch, Chromakey can be resized by dragging either side of the panel

The context menu has an option that allows you to save the current width as the default

By default, the panel colour will be set to the values of the
[Chromagica](/DanTModules-Manual/manual/chromagica/) module

There is a context menu option that will allow you to lock in the current colour of the panel, so
that further changes on the Chromagica module do not affect this instance of Chromakey

The `Preset Colours` option provides a number of default colours that you can set the panel to,
these also necessarily engage the colour lock

When the `Bypass Room Brightness` option is enabled, the module will not be dimmed with the room
brightness setting

This module is designed to enable you to create chroma-key effects (aka green-screen) in video
streaming or editing software

### Colour & RGB Lock

The context menu also includes the `Lock Colour` and `Lock RGB`options.

When `Lock Colour` is enabled, the ARGB values will no longer be controlled by the Chromagica
module.

`Lock RGB` works in the same way except the A value is still alterable, allowing you to dim the
colour of the module.
