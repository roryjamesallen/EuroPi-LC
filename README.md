# EuroPi-LC
### A Low-Cost Hardware Version of the [EuroPi](https://github.com/Allen-Synthesis/EuroPi)

Hardware specifications:
- 4x Outputs (0-10V, smoothed PWM, each with indicator LED)
- 2x Inputs (Both capable of 0-10V analogue input, 12 bit, input 1 also capable of digital input with hardware interrupt)
- 2 Knobs (12 bit)
- 2 Push buttons

This hardware uses the [XIAO RP2040](https://www.seeedstudio.com/XIAO-RP2040-v1-0-p-5026.html) as opposed to the full sized [Raspberry Pi Pico](raspberrypi.com/products/raspberry-pi-pico/) used in the standard hardware to reduce the overall size of the module. It also has no display, so although it would be possible to load the menu system onto it, it's much more geared towards loading a single script which doesn't required the display.

The reductions in complexity allow the module to be not only cheaper, but also smaller, coming in at only 4HP - half the width of the standard EuroPi hardware.
