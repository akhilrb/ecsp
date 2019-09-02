# ECSP

ECSP, *Elliptically Compensated Spectro-Photometer*, more lovingly called *El Cheapo Spectro-Photometer* is an intelligent colorimeter able to back-estimate the dominant absorption spectra of a solution with characteristic wavelengths in the visible light range. It is born out of [BITS Pilani's (Hyderabad) MEMS research group](https://www.bits-pilani.ac.in/Hyderabad/sgoel/Group) headed by [Dr. Sanket Goel](https://www.bits-pilani.ac.in/Hyderabad/sgoel/Profile).  
ECSP is a heavily self-contained device which has grown to involve the following features:

* Completely self-sufficient in terms of mathematics and processing involved
* **Portable**, with a battery backup of about 750+ tests on a single charge
* Built-in one touch **self calibration**, calibrates with varying colour-temperature of light and/or variable optical path
* Built-in one touch **self test**, which checks for and ensures quality-behaviour of internal acquisition eletronics
* Access to acquisition settings that can change the behaviour of device and give tailored results
* Available trade-off between acquisition time and precision, with satisfactory results of **1 nm precision in under 10 seconds**
* Clean GUI with self-explanatory touch buttons to guide through the screens

ECSP ~~expects different solutions with increasing gradient input in an incremental order~~ now expects simply loading the original solution directly. This requires a few more microlitres (as compared to the previously required volume) to be drained into a specifically designed PDMS channel, which is calibrated along with the light's colour-temperature. 

---

## Hardware

The device employs:

* ATMega2560
* Standard 2.4 inch TFT resistive touchscreen
* TCS3200 sensor
* White LED
* 3D printed enclosure

These parts are easily available off the shelf at a reasonably cheap price.

---

## Software

The software for ECSP has been decided to be provided as a free-download, with the intention of making it openly accessible to everyone.  
Schematics and models will soon be uploaded.

The software has been written keeping in mind that everything must be intuitive, as well as highly descriptive as possible, without clobbering the user's experience with extreme data.<br>
The user is exposed only to the output data, yet some functions related to changing the underlying algorithms are given so that outputs can be tailored according to usage.<br>
The GUI is clean and simple with clickable buttons to determine what to do next.<br>
A "help" section will soon be included.

The code (v3.2) uses 68754 bytes of program storage space and global variables use 3043 bytes of dynamic memory.
This is a huge improvement from v2.3, which used 72584 bytes of program storage space and 6643 bytes of dynamic memory.

## Uploading the program

*ECSP is currently supported only on ATMega2560. Please submit a request if you want support for other boards as well.*

Two hex files have been provided. If you need to use the hexfile containing *with_bootloader* in the name, you probably already know what to do.  
Otherwise, the hexfile named `ecsp.ino.mega.hex` can be uploaded to a Mega board using:  

`<PATH/TO/AVRDUDE/TOOLCHAIN> -C <PATH/TO/AVRDUDE/CONF> -v -V -patmega2560 -cwiring -P/dev/ttyACM0 -b115200 -D -Uflash:w:ecsp.ino.mega.hex:i`

If you have the `avrdude` toolchain installed, the paths for the first two parameters would depend on the installation.  
However, if you have the Arduino IDE installed, you can make use of the inbuilt avrdude toolchain. The paths will be something along these lines:  

Path to avrdude toolchain : `<ArduinoInstallDirectory>/hardware/tools/avr/bin/avrdude`  
Path to avrdude conf file : `<ArduinoInstallDirectory>/hardware/tools/avr/etc/avrdude.conf`


