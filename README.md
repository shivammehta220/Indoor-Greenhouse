# Indoor Greenhouse Project

![Greenhouse](/assets/greenhouse_image2.jpg)

This repository contains information and code for an Indoor Greenhouse project I undertook during my high school years. The project aimed to create a self-contained greenhouse with automated watering and monitoring systems using Arduino and Raspberry Pi. This was one of my first major projects involving micro-controllers and electronics so there are aspects that I would do differently now.

## Project Overview

The goal of this project was to construct a table equipped with grow lights and an automatic watering system to facilitate indoor plant growth. The entire system was controlled by an Arduino, and a Raspberry Pi was utilized to display and log various data from the plants, including moisture and humidity levels.

## Electronics and Sensors

Before constructing the complete greenhouse, I first gathered all the necessary electronic components and prototyped the setup to ensure everything was functional. The key components used in the project were:

- Soil Moisture Sensor
- Time/Clock Sensor
- Temperature Sensor
- Humidity Sensor
- Relays for controlling lights and water pump
- Arduino board for data collection and control

The Arduino was programmed to respond to sensor inputs and control the lighting and watering systems accordingly. When the soil moisture level was low, indicating dry conditions, the Arduino would activate the water pump to water the plants. The lighting system was controlled by the Arduino based on the time of day.

![Greenhouse2](/assets/prototype1.jpg)

Moreover, the Arduino sent serial data (soil moisture and humidity readings) to the Raspberry Pi via USB. The Raspberry Pi was responsible for displaying and storing this data over time.

![Greenhouse3](/assets/pi.jpg)

## Construction

For the physical construction of the greenhouse, I primarily used wood as the main construction material. The table was designed in a way that allowed the grow lights to be positioned directly above the plants, providing optimal light exposure.
The grow lights were attached to the table using junction boxes and wired down to the relays and power sources.

![Greenhouse4](/assets/table.jpg)

### Watering System

The watering system was simple yet effective. It consisted of a water reservoir and a pump. The pump was submerged in the reservoir and activated by the Arduino through a relay. When the pump was activated, water was pumped through pipes to irrigate the plants.

![Greenhouse5](/assets/water.jpg)

### Enclosure

After the successful prototyping phase, all the electronics were placed inside an enclosure to protect them and ensure a tidy and organized setup.

![Greenhouse6](/assets/enclosure.jpg)

# Results and Improvements

![Greenhouse7](/assets/greenhouse_image3.png)

After running the greenhouse for a few weeks, I obtained positive results but also identified some areas for improvement. The following issues need to be addressed:

1. **Relay Failsafe**: The code needs to be reworked to implement a failsafe mechanism so that the relays are not continuously activated, potentially causing overflow or overwatering.

2. **Data Logging Stability**: In case of an Arduino reset, the Raspberry Pi is unable to log data accurately for the corresponding time period. The data logging code on the Raspberry Pi needs to be reworked to handle such situations effectively.

## Conclusion

Overall, this Indoor Greenhouse project had been a valuable learning experience, combining electronics, programming, and construction skills.

I hope that the information and code provided in this repository will be helpful to anyone interested in exploring indoor gardening and automation using Arduino and Raspberry Pi. Happy gardening!
