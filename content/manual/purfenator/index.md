---
title: 'Purfenator'
date: 2023-12-20T12:00:00
weight: 12
---

- [Overview](#overview)
  - [Controls](#controls)
- [Seizure Trigger \[Purfenator Expander\]](#seizure-trigger-purfenator-expander)

## Overview

**`4hp`**

Purfenator is a module designed to make creating nice backdrops directly within VCV Rack as easy as
possible. It was inspired by this [video](https://youtu.be/5FeWTLwftUM?si=liYuLl64j3U93Gbo) from
[Urs Basteck](https://community.vcvrack.com/u/purf/summary).

![NuMetal-Purfenator](/DanTModules-Manual/images/purfenator.png)

### Controls

There is only one control on the module, which is the active button. When lit the module is active
and will draw the backdrop, when unlit the backdrop will not be drawn.

All the configuration and controls for customising the backdrop can be found in the right-click
context menu under the `Purf Stylee` heading:

* `Module & Patch Title`
  * `Draw button` - When active the active button will be visible on the module, when not active the
    active button will not be visible.
  * `Button position` - Controls the vertical position of the active button on the module panel.
  * `Draw title` - The patch title is the name of the current patch save file and is displayed on
    the module. When active the title will be displayed on the moduel panel, when not active the
    title will not be visible.
  * `Flip title` - When active the title will read from top to bottom, when not active the title
    will read from bottom to top.
  * `Bright title` - When active the title will bypass the room brightness and act like a light.
  * `Font size` - Controls the size of the text on the module panel.
  * `Colour rgba` - Controls the colour and transparency of the text on the module panel.
* `Colour Background` - Creates a layer below the modules and fill it with colour.
  * `Draw background` - Activate and deactivates this element.
  * `Gradient` - When active the the background will be a linear gradient from top to bottom.
  * `Colour rgba` - Controls the colour and transparency of the main background colour.
  * `Gradient rgba` - Controls the colour and transparency of the secondary gradient colour.
* `Image Background` - Creates a layer that can render an image.
  * ` - Load image` - Opens an OS file dialog where you can select an image file.
  * `Draw background` - Activate and deactivates this element.
  * `Image on top of colour` - When active the image will be drawn on top of the colour background
    layer, this means images with transparency can be rendered over different colour backgrounds.
    When not active the image will be drawn underneath the colour background layer, this means the
    image can be tinted or desaturated by reducing the colour background alpha value.
  * `Tiled` - When active the image will be tiled to fill the screen.
  * `Ignore zoom` - When active the image will ignore the Rack zoom setting and remain at a fixed
    size, when not active the image will change size when the zoom level is changed.
  * `Scale` - Controls the size of the image.
  * `Image position` - Controls the anchor point relative to the screen for the image.
  * `Width/Height offset` - Controls the amount to move the image relative to itself. This can be
    used to tweak where the repeat happens for a tiled image for example.
  * `X/Y offset` - Controls the amount to move the image relative to its screen anchor point.
  * ` - Clear image` - Remove the currently displayed image.
* `Skiff` - Creates virtual [skiffs](https://www.google.com/search?q=What+is+a+modular+skiff) around
  the modules added to the patch.
  * `Draw skiff` - When active the box of the skiff will be rendered.
  * `Draw bezel` - When active the lip of the skiff box will be rendered.
  * `Draw rails` - When active rails will be rendered inside the skiff box
  * `Draw shadow` - When active a shadow will be rendered under the skiff box.
  * `Multimode` - When not active only one skiff box will be drawn that encompasses all the modules
    added to the patch. Activating multimode allows that single skiff box to be split into multiple
    boxes, and is controlled by the following two parameters.
  * ` - Split vertically` - When enabled the skiff box will be split by any empty row.
  * `Horizontal threshold` - When not disabled, any gaps between modules larger than this value will
    split the skiff box.
  * `Skiff depth` - Controls the size of the skiff box sides.
  * `Bezel size` - Controls the width of the lip of the skiff box.
  * `Shadow size` - Controls how far the shadow extends from the skiff box.
  * `Shadow softness` - Controls how blurry the shadow is.
  * `Shadow intensity` - Controls how dark the shadow is.
  * `Skiff colour rgb` - Controls the colour of the skiff box sides and lip.
  * `Inside colour rgba` - Controls the colour of the inside of the skiff box.

## Seizure Trigger [Purfenator Expander]

This module is an expander to Purfenator that enables you to control the parameters via CV.

**Excessive modulation is highly discouraged.**
When all the features are active this module can use a fair amount of graphical resources,
especially if you are using high resolution images. Modulating many parameters at the same time will
increase the amount of resources required, and could create extreme visual stimulus, user discretion
is advised.

The module has 5 polyphonic inputs, with specific channels of each dedicated to a single parameter.

For any on/off parameter, the CV expects a trigger, although any signal greater than `0 volts` will
toggle it.

For number parameters, the CV expects a signal `0 - 10 volts` where `0` is the minimum and
`10` is the maximum.

Note: Because these parameters are in the context menu, the CV directly changes the parameter value,
there is no attenuvertor nor offset, and values that are altered by CV will not be undo-able.
However, a CV value of `0 volts` will not not affect the parameter.

The channel map for the polyphonic inputs is as follows:

 * **Module & Title parameters**
   * `01` - Module active
   * `02` - Draw button
   * `03` - Button position
   * `04` - Draw title
   * `05` - Flip title
   * `06` - Bright title
   * `07` - Font size
   * `08` - Colour Red
   * `09` - Colour Green
   * `10` - Colour Blue
   * `11` - Colour Alpha

 * **Colour Background parameters**
   * `01` - Draw background
   * `02` - Gradient
   * `03` - Colour Red
   * `04` - Colour Green
   * `05` - Colour Blue
   * `06` - Colour Alpha
   * `07` - Gradient Red
   * `08` - Gradient Green
   * `09` - Gradient Blue
   * `10` - Gradient Alpha

 * **Image Background parameters**
   * `01` - Draw background
   * `02` - Image on top of colour
   * `03` - Tiled
   * `04` - Ignore zoom
   * `05` - Scale
   * `06` - Image position
   * `07` - Width offset
   * `08` - Height offset
   * `09` - X offset
   * `10` - Y offset

 * **Skiff parameters**
   * `01` - Draw skiff
   * `02` - Draw bezel
   * `03` - Draw rails
   * `04` - Draw shadow
   * `05` - Skiff depth
   * `06` - Bezel size
   * `07` - Shadow size
   * `08` - Shadow softness
   * `09` - Shadow intensity
   * `10` - Skiff colour Red
   * `11` - Skiff colour Green
   * `12` - Skiff colour Blue
   * `13` - Inside colour Red
   * `14` - Inside colour Green
   * `15` - Inside colour Blue
   * `16` - Inside colour Alpha

 * **Multimode parameters**
   * `01` - Multimode
   * `02` - Split vertically
   * `03` - Horizontal threshold
