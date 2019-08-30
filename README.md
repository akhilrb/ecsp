# ECSP

ECSP, *Elliptically Compensated Spectro-Photometer*, more lovingly called *El Cheapo Spectro-Photometer* is an intelligent colorimeter able to back-estimate the dominant absorption spectra of a solution with characteristic wavelengths in the visible light range. It is born out of BITS Pilani's (Hyderabad) MEMS [research group](https://www.bits-pilani.ac.in/Hyderabad/sgoel/Group).  
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

The software for ECSP is provided as a free-download, with the intention of making it openly accessible to everyone.  
Schematics and models will soon be uploaded.

The software has been written keeping in mind that everything must be intuitive, as well as highly descriptive as possible, without clobbering the user's experience with extreme data.<br>
The user is exposed only to the output data, yet some functions related to changing the underlying algorithms are given so that outputs can be tailored according to usage.<br>
The GUI is clean and simple with clickable buttons to determine what to do next.<br>
A "help" section will soon be included.


