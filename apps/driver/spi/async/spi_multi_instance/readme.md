---
parent: Harmony 3 driver and system service application examples for PIC32MK family
title: SPI Driver asynchronous - multi instance 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# SPI Driver asynchronous - multi instance

This example demonstrates how to use multiple instances of the SPI driver in asynchronous mode to communicate with multiple EEPROMs

## Description

This example writes and reads data to and from two separate EEPROM connected over two different SPI bus by using multi instance feature of the driver. The example also demonstrates how to setup two different EEPROM transfers at different baud rates.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mk) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/spi/async/spi_multi_instance/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mk_mcm_curiosity_pro.X | MPLABX project for [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mk_mcm_curiosity_pro.X | [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A) |
|||

- To run the demo, the following additional hardware are required:
    - Two [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) boards

### Setting up [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A)

- Connect a micro USB cable to the USB DEBUG port J500
- Install two [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) boards on to the two mikroBUS sockets (J300 and J301) of [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A)

## Running the Application

1. Build and program the application using its IDE
2. The LED is turned ON when the data read from the EEPROMs matches with the data written to the EEPROMs

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A) | LED1 |
|||
