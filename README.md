# Custom Firmware for the Wanhao Duplicator i3 v2.1, by Bot-In-a-Box

![The custom bootscreen featuring Chippy from Bot-In-a-Box](https://botinabox.ca/wp-content/uploads/2018/12/chippy_bootscreen.jpg  "The custom bootscreen featuring Chippy from Bot-In-a-Box")

## Based on Marlin Firmware v2.0

A big thank-you is in order to everyone who's contributed to the Marlin Firmware over the years; because of their support and continued development Marlin has become a state-of-the-art, highly-extensible universal firmware for 3D Printers everywhere. 

For more information about the Marlin firmware head to the [Marlin Homepage - marlinfw.org](http://marlinfw.org/).
Check out Marlin's [Github repo](https://github.com/MarlinFirmware/Marlin/tree/bugfix-2.0.x) as well.

## About this Firmware

I realized the default firmware that came with my Wanhao Duplicator i3 was, frankly, not great. It was slow, unstable, clunky, and all-around unideal. However, once I realized that it was based on Marlin, I knew I could do better. Besides, OctoPrint warned me that the firmware didn't even have built-in thermal protection! But by reading pages upon pages of documentation, example code, and forum posts, I was able to piece together exactly how I needed to alter the Marlin 2.0 source code to get it to work with my printer. I'd especially like to point out the posts I found most useful:

[https://www.reddit.com/r/3Dprinting/comments/8o3wg8/installing_marlin_on_maker_select_v2/](https://www.reddit.com/r/3Dprinting/comments/8o3wg8/installing_marlin_on_maker_select_v2/)
[https://www.thingiverse.com/thing:2450111](https://www.thingiverse.com/thing:2450111)


## Some Features

+ Custom "Chippy" Bootscreen by [Bot-In-a-Box](https://botinabox.ca)
+ Built-in Thermal Runway Protection
+ Change Settings and Save/Load them from EEPROM
+ Printing over SD Micro/USB Mini Support
* Custom Thermistor Table (99) made using ```buildroot/share/scripts/createTemperatureLookupMarlin.py``` for 10k pull-up resistor with the out-of-the-box thermistor
+ Print Time Elapsed and Progress Bar 
+ Minor Stability/Connection/Performance Improvements
	
## How to Install

1. Flash the Optiboot Bootloader on your Melzi board after taking it out of the box (I used my Raspberry Pi to do it): [https://www.fission3d.com/guides/flash-bootloader-and-install-firmware-with-raspberry-pi](https://www.fission3d.com/guides/flash-bootloader-and-install-firmware-with-raspberry-pi)
2. Auto Build the Firmware with Platform.io in Atom or VS Code [http://marlinfw.org/docs/basics/install_platformio.html](http://marlinfw.org/docs/basics/install_platformio.html)
3. Auto Upload the Firmware with Platform.io in Atom (After connecting the Melzi to your computer via USB Mini and ensuring the PWR jumper on the Melzi is set to the USB Setting)
4. (You can also use the Arduino IDE with ```/Marlin/Marlin.ino``` to compile/upload the firmware)

## Scrapbook

![The Marlin Bootscreen](https://botinabox.ca/wp-content/uploads/2018/12/marlin_bootscreen.jpg "The Marlin Bootscreen")
![A simple trick to change to VREG or USB power is to use Dupont Jumper cables and stick them out the 110V/220V hole](https://botinabox.ca/wp-content/uploads/2018/12/simple_trick.jpg "A simple trick to change to VREG or USB power")
![My 3D Printer](https://botinabox.ca/wp-content/uploads/2018/12/bbwanhao.jpg "My 3D Printer")



## License

Marlin is published under the GPL License, and a copy of that license is included in the source code. It's worth noting that the license explicitly states that any software licensed under it is offered with "NO WARRANTY... OF ANY KIND, EITHER EXPRESSED OR IMPLIED." I'm offering this firmware open-source in the hopes that it might prove helpful to someone else, but I'm not responsible if anything goes wrong with your printer or anything else because of it; it's AS-IS.

At any rate, I hope this firmware solves some problems for you; think of it like a 2019 update for the Wanhao i3.

- [Sincerely, Matthew Piercey](https://matthewpiercey.ml)