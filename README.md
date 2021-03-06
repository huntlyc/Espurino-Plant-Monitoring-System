Espruino Plant Monitoring System
================================
Simple soil moisture and ambient temperature monitoring system.

To _"IoT"_ this project checkout my [raspbery pi project](https://www.github.com/huntlyc/pi-espruino-plant-monitor)

## Required components/Shopping list:

- [Espruino](https://www.espruino.com/EspruinoBoard) 
- [One Wire Digital Temperature Sensor - DS18B20](https://www.sparkfun.com/products/245)
- [Soil Moisture Sensor](https://www.bitsbox.co.uk/index.php?main_page=product_info&cPath=302_306&products_id=2816)
- 4.7K resistor - If you don't have one, get a [resistor pack](https://coolcomponents.co.uk/products/resistor-kit-1-4w-500-total)

## Basic Setup
There are only 2 sensors in this project, both can be run off a shared 3.3v rail and shared ground rail if breadboarding it.

Check out the fritzing diagram for more clarification. ***Please note:*** the soil moisture sensor in the fritzing diagram isn't the same, but they all work on the same principle.

![Circuit Diagram](https://github.com/huntlyc/Espruino-Plant-Monitoring-System/raw/master/circuit-diagram.png)

### Soil Sensor

* VCC - 3.3v rail
* GND - Ground rail
* DO - _not used_
* AO - straight to pin C5

### Temperature Sensor
With the rounded side facing ***away*** from left to right:

* 0 - Ground rail
* 1 - pin A1
* 2 - 3.3v rail

***Note:*** You need to put the 4.7K resistor between pins 1 & 2 (data and power)

## Use

This is just a super basic system:

* LED1 - Green - Signals temp OK
* LED2 - Red -  Outside ideal range (20 - 35 degrees Celsius)
* LED3 - Blue - Signals low moisture
