# Honda NX650 Monitoring System

![NX650 MS](images/docs/01.jpg)

<br>

***This is a short summary of my Honda NX650 Monitoring System project.***

<br>

The source code is available [**here**](code/MMS-source/MMS-source.ino).

<br>

## Overview



The device displays the following:

- Engine Head Temperature;
- Engine Sump Temperature;
- Battery Voltage;
- Threshold warnings;
- Time;
- Air Temperature;
- Air Relative Humidity.

<br>

[![Watch video](images/docs/video_thumbnail.jpg)](https://www.youtube.com/watch?v=qPbqtzeUloo)

<br>

## Main Components
- [Main Box Assembly](#main-box-assembly)
- [Display Box Assembly](#display-box-assembly)
- [Air Monitoring Box Assembly](#air-monitoring-box-assembly)

<br>

## Main Box Assembly

The main box houses most of the electronics, including:

- Microcontroller (Raspberry Pi Pico);
- Precision Clock Module (DS3231);
- ADC Custom Board: mainly voltage dividers for the thermistors and voltage monitoring, along with signal filtering;
- Power Supply Unit: mainly a buck converter module, extra filtering, and a MOSFET to power the device only when the ignition is turned on;
- Button for time adjustment.

<br>

![Main Box Assembly](images/docs/main_box_assembly.jpg "Main Box Assembly")

<p align="center">
    <a href="images/docs/main_box.jpg">
        <img src="images/docs/main_box.jpg" alt="Main Box" width="80%">
    </a>
</p>

This assembly bolts to the motorcycle's fuse box mounting bracket. 

I designed a pad to be placed between the bracket and the assembly to reduce vibration. There's also a sleeve around the mounting bolts for the same purpose. 

The motorcycle's fuse box is then bolted on top of the assembly.

<p align="center">
    <a href="images/docs/main_box_installation.jpg">
        <img src="images/docs/main_box_installation.jpg" alt="Main Box Installation" width="80%">
    </a>
</p>

The Power Supply Unit (PSU) ensures the motorcycle's battery voltage is converted to a stable, filtered 5V. It also has a MOSFET used to power the device only when the ignition is turned on.

<p align="center">
    <a href="images/docs/psu_circuit_diagram.jpg">
        <img src="images/docs/psu_circuit_diagram.jpg" alt="PSU Circuit Diagram" width="80%">
    </a>
</p>

<br>

## Display Box Assembly

This enclosure houses the OLED display module.

![Display Box Assembly](images/docs/display_box_assembly.jpg "Display Box Assembly")

<p align="center">
    <a href="images/docs/display_box.jpg">
        <img src="images/docs/display_box.jpg" alt="Display Box" width="80%">
    </a>
</p>

<br>

## Air Monitoring Box Assembly

This enclosure houses the DHT22 air temperature and humidity module, as well as a small blower fan. The fan creates negative pressure inside the enclosure to promote air circulation. This, in addition to the snorkel, was designed in an effort to reduce the influence of hot air from the engine.

![Air Monitoring Box Assembly](images/docs/air_monitoring_box_assembly.jpg "Air Monitoring Box Assembly")


<p align="center">
    <a href="images/docs/air_monitoring_box.jpg">
        <img src="images/docs/air_monitoring_box.jpg" alt="Air Monitoring Box" width="80%">
    </a>
</p>
