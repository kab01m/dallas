## DV-87-12 is a replacement module for Dallas DS1287

This project is a complete replacement of widely used RTC modules DS1287, DS12887, DS12887+ originally made by Dallas and their derivatives.

### Options

#### R1/R2/R3

Only one of R1, R2 and R3 should be installed. DS1287 pin 1 is a mode select, some motherboards do not have it working, so you can pull pin 1 up with R2 for Motorola mode or down with R3 for Intel mode. Put zero resistor in R1 if you do not know.

#### R4/R5

Original DS1287 have 21 and 22 as not-connected, so by default you do not install R4 and R5. Some motherboards are known to use RCLR signal on pin 21, so you have to put zero resitor into R4 if it does not work right. DS13* or DS14* are using both 21 and 22 pins, so you put both R4 and R5 in place.

#### U1

You can use DS12885, bq3285 or bq4285 depending on what you can find and what original chip you want to replace.

* DS1287 series:
    * Dallas DS1287 / DS12887 / DS12B887 : bq3285 or DS12885S, use R1.
    * Dallas DS12C887, DS12887+ : bq3285 or DS12885S+, use R1 and R4.
    * ST M48T86PC1 : bq3285 or DS12885S+, use R1 and R4.
    * Benchmarq BQ3287 : bq3285, use R1, R4.
    * ODIN OEC12C887 : bq3285 or DS12885S, use R1.
    * VIA VT82887 : bq3285 or DS12885S, use R1.
* DS1387 series
    * Dallas DS1387 : DS1385, use R1, R4, R5.
* DS1487 series
    * Dallas DS14287 : bq4285, use R1, R4, R5.
    * Benchmarq BQ4287 : bq4285, use R1, R4, R5.
* Motorola MC146818A can be supported. Tell me if you need it.

#### B1

* DV-87-12 uses BS-1220-2 battery holder (found on Aliexpress).
* DV-87-12R uses Renata SMTU-1225-LF battery holder.

### Bill of Materials

* DV-87-12 PCB board, use supplied Gerbers.
* U1 - DS12885, bq3285, bq4285 or DS1385.
* B1 - BS-1220-2 or SMTU-1225-LF.
* B1 - CR1225 3V lithium cell
* Y1 - 32.768 kHz crystal, 3215 metric SMD.
* R1 - Zero 0805 inch SMD to enable selector mode (default).
* R2 - 10 K 0805 inch SMD to enable Motorola mode (optional).
* R3 - 10 K 0805 inch SMD to enable Intel mode (optional).
* R4 - Zero 0805 inch SMD for 21 pin (optional).
* R5 - Zero 0805 inch SMD for 22 pin (optional).

### Useful links

* [Necrowave project](https://github.com/necroware/nwX287) for replacing Dallas RTC.
* [Glitchworks](https://github.com/glitchwrks) have GW-1287-1 module, but did not publish sources.
