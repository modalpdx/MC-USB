#TINY85-USB Development Board

A board that should have all the hardware that you need to experiment with
V-USB or any other software-based AVR USB stack on an ATTINY-85 MCU. 

The design of this board originated with the AVR/V-USB schematics found in
[**Code and Life's AVR ATTINY USB
Tutorial**](http://codeandlife.com/2012/01/22/avr-attiny-usb-tutorial-part-1/,
"Code and Life's V-USB ATTINY Tutorial").  I combined their schematics for
ATTINY-2313 and ATTINY-85 circuits and added an ISP header. Note: the ISP
header does not utilize VCC or GND. All power to this board comes from the
USB connection. Please keep this in mind if you decide to program the MCU
on this board.

The ISP header doubles as a pinout for the ATTINY085 chip. The "useful"
pins are labeled along with their ISP usages (MISO, MOSI, etc).

There is a spot for a 12MHz external crystal. I would suggest adding a
3-pin female header here instead of soldering a crystal to the board,
reason being the ATTINY-85's internal 16.5MHz oscillator can be utilized
in place of a crystal, and that frees up the crystal pins (PB3 and PB4)
for other uses. A crystal will fit in a 3-pin female header just fine if
one is used, otherwise the header will give you much easier access to
the freed pins. It's your call.

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

* V-USB home site
  
* [V-USB Website](http://www.obdev.at/products/vusb/index.html, "V-USB Website") 
* [Code and Life's AVR ATTINY USB Tutorial](http://codeandlife.com/2012/01/22/avr-attiny-usb-tutorial-part-1/, "Code and Life's V-USB ATTINY Tutorial")

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

A similar circuit on a breadboard was identified on my MacBook Pro as an
HID device. I used the ATTINY-85's internal 16.5MHz oscillator instead of
an external crystal. The circuit was based on the Code and Life tutorial
circuit mentioned a few times above. Basically, this *should* work.

The first run of PCBs from OSHPark has been submitted but not received
yet. If you decide to make boards from these files in the meantime,
well...you're on your own.

