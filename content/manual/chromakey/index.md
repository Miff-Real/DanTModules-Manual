---
title: 'Chromakey'
date: 2023-06-22T12:00:00
weight: 10
---

- [Overview](#overview)
- [Basic Operation](#basic-operation)
- [Colour](#colour)
- [Text Overlay](#text-overlay)
  - [Inputting Text](#inputting-text)
  - [Text Style](#text-style)

## Overview

Chromakey is a resizable & recolourable blank panel, which can also be used to display custom text.

![Chromakey](https://library.vcvrack.com/screenshots/200/DanTModules/Chromakey.png)

### Basic Operation

Once added to a patch, Chromakey can be resized by dragging either side of the panel.

The context menu has an option that allows you to save the current width as the default.

When the `Bypass Room Brightness` option is enabled, the module will not be dimmed with the room
brightness setting.

This module is designed to enable you to create chroma-key effects (aka green-screen) in video
streaming or editing software.

## Colour

The colour of the panel can be changed via the context menu.

There are three sliders (R, G, and B) that allow you to set the colour of the panel precisely.

The `Use plugin panel colour` option will set the panel's colour to the default theme colour for the plugin.

## Text Overlay

Chromakey can display text on top of the coloured panel.

The `Text Overlay` submenu in the context menu contains all the options for this feature.

First, you must enable the `Draw text` option.

### Inputting Text

There are two ways to input text:

-   **Direct Input**: Select `Input text` from the menu. This will open a text field where you can type or paste your desired text. Press Enter to confirm.
-   **Load from file**: Select `Load text file`. This will show a list of all `.txt` files located in your `<Rack user folder>/DanTModules/Chromakey/` directory. Selecting a file will load its content onto the panel. There is also a handy link to open this folder directly.

### Text Style

You can customize the appearance of the text:

-   **Text position**: Choose from nine alignment options (e.g., Top left, Middle centre, Bottom right).
-   **Font**: Select from six different fonts, including custom DanT fonts and standard VCV Rack fonts.
-   **Font size**: Adjust the size of the text using a slider.
-   **Colour**: Set the text colour using dedicated R, G, and B sliders.