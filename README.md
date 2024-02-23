MicroPython LCD Driver in Python
================================

This is a work-in-progress fork of russhughes' st7789py_mpy module from
https://github.com/russhughes/st7789py_mpy.

This fork has been modified to use the MicroPython FrameBuffer class for speed. 
The results are much faster than the original version of this driver, however the framebuffer does use a large chunk of ram, so it's not a straight upgrade.

I have tried to keep support for all the same displays as the original driver did, however, I have only tested this version on am M5 Cardputer *(240x135, rotation=1, GRB color)*, and so it's likely that further modifications will need to be made to fully support other display configurations. 

<br/>

-----

<br/>

This driver has support for:

- 320x240, 240x240, 135x240, and 128x128 pixel and other displays
- RGB and BGR Color Orders
- Display rotation
- Hardware based scrolling
- Software based scrolling
- Drawing text using converted PC BIOS bitmap fonts
- Drawing text using converted TrueType fonts.
- Drawing text using the built-in framebuf font.
- Drawing converted bitmaps
- Drawing ellipses
- Drawing and deforming polygons

This is a work in progress. Documentation can be found in the docs directory
and at https://russhughes.github.io/st7789py_mpy/


Examples
--------

See the examples directory for example programs that run on:

- ESP32
  - Generic ESP32 320x240
  - LilyGo T-DISPLAY 135x240
  - LilyGo T-Dongle-S3 80x160 (ST7735)
  - LilyGo T-embed 170x320
  - LILYGO T-QT Pro 128x128 (GC9107)
  - M5STACK AtomS3 128x128 (GC9107)
  - M5STACK CORE2 320x240 (ILI9342)
  - M5STACK CORE 320x240 (ILI9342)
  - M5STACK CoreS3 320x240 (ILI9342)

- RP2040
  - LilyGo T-DISPLAY RP2040 135x240
  - RP2040-Touch-LCD-1.28 240x240 (GC9A01)
  - Waveshare Pico LCD 1.14 135x240
  - Waveshare Pico LCD 1.3 240x240
  - Waveshare Pico LCD 2 240x320
