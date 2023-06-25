# EuroPi LC
### A Low-Cost Hardware Version of the [EuroPi](https://github.com/Allen-Synthesis/EuroPi)

Hardware specifications:
- 4x Outputs (0-10V, smoothed PWM, each with indicator LED)
- 2x Inputs (Both capable of 0-10V analogue input, 12 bit, input 1 also capable of digital input with hardware interrupt)
- 2 Knobs (12 bit)
- 2 Push buttons
- 4HP wide (20.32mm)

### What actully *is* a "EuroPi LC"?
The EuroPi LC (Low-Cost) can be essentially seen as a '[HAT](https://www.raspberrypi.com/news/introducing-raspberry-pi-hats/)', but using a XIAO RP2040 instead of a full sized Raspberry Pi. Without going into too much depth, the circuit converts the 3.3V signals that the XIAO RP2040 deals with (both for inputs and outputs) into 0-10V signals which are more useful in a Eurorack context. The knobs and buttons are just extra components added for the user to work with in their code. If you plan on just using code other people have written, then ignore all the 'HAT' stuff, and just think of the EuroPi LC as any other Eurorack module.  
  
So what does "work with" actually mean? Well, the EuroPi LC (as with the standard hardware EuroPi, lots of this information is interchangeable) is a platform that can be used to bring your ideas for new modules to life using [MicroPython](https://micropython.org/). In the same way that a Raspberry Pi HAT with some LEDs on it allows your Raspberry Pi code to interact with some LEDs, the EuroPi LC allows your XIAO RP2040 code to interact with all the other modules in your Eurorack system.  
  
For example, you can write very simple scripts using commands as simple as `cv3.voltage(2)` to set CV (Control Voltage) output 4 to 2 volts, which you can then plug into another module and voila - your MicroPython script is now directly controlling another module in your rack, and you have *complete* control over what it does. Of course it can get a lot *lot* more complex than setting a single CV output to a voltage, and eventually you end up with scripts like quantizers, polyrhythmic sequencers, and complex synced LFOs.
