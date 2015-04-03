#MC-USB Development Board

*BIG IMPORTANT NOTE: The first run of PCBs has come back from the fab, and
yep, they don't work as designed. Until further notice, please don't make
any PCBs from these files. I'll update everything once I figure out how to
fix all of the issues. There aren't many, but the ones that exist are show
stoppers as far as I'm concerned.*

A board that should have all the hardware that you need to experiment with
V-USB or any other software-based USB stack on an ATTINY-85 MCU (current
configuration, other MCUs may be implemented in future editions). 

The design of this board originated with the AVR/V-USB schematics found in
Code and Life's AVR ATTINY USB Tutorial (linked below). I combined their schematics for
ATTINY-2313 and ATTINY-85 circuits and added an ISP header. 

*Note: the ISP header does not utilize VCC or GND. All power to this board
comes from the USB connection. Please keep this in mind if you decide to
program the MCU on this board.*

The ISP header doubles as a pinout for the ATTINY-85 chip. The "useful"
pins are labeled along with their ISP usages (MISO, MOSI, etc).

There is a spot on the board for a 12MHz external crystal. I would suggest
adding a 3-pin female header here instead, reason being the ATTINY-85's
internal 16.5MHz oscillator can be utilized in place of a crystal, and
that frees up the crystal pins (PB3 and PB4) for other uses. A crystal
will fit in a 3-pin female header just fine if one is used, otherwise the
header will give you much easier access to the freed pins. It's your call.

##Parts

* ATTINY-85 PDIP-8 AVR MCU
* 8 pin DIP socket
* 2-68k ohm 1/4 watt resistors (R1, R2)
* 2.2k ohm 1/4 watt resistor (R4)
* 4.7k ohm 1/4 watt resistor (R3)
* 10uF polarized capacitor (C1)
* 0.1uF ceramic capacitor (C2)
* 2-22pF ceramic capacitors (C3, C4)
* 2-3.6V 1/2 watt Zener diodes (D1, D2)
* 2x6 male header pins (ISP)
* 12MHz external crystal (optional)
* 3-pin female header for crystal (optional)
* Mini-B 5-pin SMT female USB connector (there are many, but they are similar. The version I used has two plastic pins that keep it from sliding horizontally on the board.)

##Resources

I'm not going to document V-USB usage, sorry. There are tutorials linked
to the V-USB page and numerous websites Out There™ that cover this in
detail. 

* [V-USB Website](http://www.obdev.at/products/vusb/index.html "V-USB Website") 
* [Code and Life's AVR ATTINY USB Tutorial](http://codeandlife.com/2012/01/22/avr-attiny-usb-tutorial-part-1/ "Code and Life's V-USB ATTINY Tutorial")

##Limitations

* I'm not 100% sure I got the ISP implemented correctly. Buyer beware.
* I'm not 100% sure I got the crystal set up correctly to allow PB3 and PB4 pin access if no crystal is used. Buyer beware again.

##Motivation

After successfully working up a breadboard with an ATTINY-85/V-USB
circuit, I realized there was no way in hell I was going through that
every time I wanted to work with AVR/USB stacks. A board that could take a
fresh (or flashed) ATTINY-85 would exponentially speed up the development
process. So, here we are.

##Miscellaneous Notes

Don't use these files yet. Moose out front should have told you.
