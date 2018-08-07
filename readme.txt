Yamaha SFG 05/01-B Clone Board v1.1
Copyright (c) 2017 RBSC

The Setup
---------

After assembling, the board needs to be programmed in order to function properly. The following steps are necessary:

 1. Upload the Altera's firmware
 2. Program the BIOS with the provided ROM file


How to upload the firmware
--------------------------

The below instructions are for programming the Altera chip.

 1. Solder jumper pins to the "+5v" and "GND" soldering points on the board
 2. Prepare the ByteBlaster 2 programmer, open the Quartus II software, keep default JTAG selection
 3. Supply 5v power to the board via jumper pins (mind the correct polarity!)
 4. Connect the ByteBlaster's cable to the AS socket of the board (make sure you connect the cable correctly!)
 5. Click "Autodetect" in Quartus II software, the Altera chip should be found and ready for programming
 6. Use "Change file" option and select the .POF file from the "Firmware" directory
 7. Enable the checkboxes: "Program/Configure", "Verify" and "Blank Check"
 8. Click "Start" and monitor the programming and verification process

If the programming completed successfully, disconnect the ByteBlaster's cable and 5v power from the board.

You must also write the provided ROM file from BIOS directory into the 27C512 EPROM/EEPROM chip (DIP28) using any EEPROM
programmer. The ROM file contains 2 different BIOS versions that can be selected by the special jumper on the board. It is
also possible to use 27C256 EPROM/EEPROM chip to only have one of the BIOS versions instead of two.


Installing the audio wire
-------------------------

In order to connect the audio from the SFG board to MSX's internal amplifier a shielded wire must be installed between soldering
points named "X8A" and "X8B". The easiest way is to solder two 2-pin jumper pins onto those soldering points and attach a shielded
wire with Dupont connectors on both ends. The 74HCT04_fix.jpg shows such connection on the right side of the image. In order to
keep the connectors within the SFG casing, it's recommended to remove the plastic from the 2-pin jumper connectors and to cut the
pins a bit to allow the Dupont conenctor to settle down as close to the board as possible.

Alternatively a shielded wire can be soldered directly to the "X8A" and "X8B" soldering points. It is strongly recommended to use
a shielded wire for the above described connection to avoid interference from the digital components on the board. When installing
the wire please make sure that the shield is connected to the "GND" pin and the audio wire is connected to the other pin. Incorrect
connection may damage the board!


Installing into a case
----------------------

The SFG module can be installed into a network module case that was available in YIS503II, YIS503III and YIS805/128 MSX computers
that were available in Russia (USSR) in the 90-s. The holes for the MIDI connectors fit perfectly. However to be able to use
the RCA and external music keyboard, the front part of the case needs to be modified. See the sfg_case.jpg file for an example
of such installation.


Starting SFG BIOS
-----------------

To start the built-in SFG BIOS make sure that Basic is loaded and type "_musica" or "call musica" without quotes and press Enter.
The BIOS should start immediately. Depending on whether the jumper is installed or not, either the SFG-01 BIOS or SFG-05 BIOS will
be launched. To exit from BIOS software just reboot your MSX.


Notes
-----

If you are using 74HCT04 chip instead of 74LS04 please make sure you add one additional 47pf capacitor. See the 74HCT04_fix.jpg
image for capacitor mounting instructions. This picture shows how to install the capacitor on board version 1.0. Later boards
have the special placeholder for the capacitor.


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!


Contact information
-------------------

The members of RBSC group Wierzbowsky, Ptero and DJS3000 can be contacted via the MSX.ORG or ZX-PK.RU forums. Just send a personal
message and state your business.

The RBSC repository can be found here:

https://github.com/rbsc


-= ! MSX FOREVER ! =-
