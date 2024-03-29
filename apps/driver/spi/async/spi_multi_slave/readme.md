---
parent: Harmony 3 driver and system service application examples for PIC32MK family
title: SPI Driver asynchronous - multi slave 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# SPI Driver asynchronous - multi slave

This example demonstrates how to use single instance of the SPI driver in asynchronous mode to communicate with multiple EEPROMs.

## Description

This example write and read data to and from two separate EEPROM connected over the same SPI bus by using the multi client feature of the driver.The example also demonstrates how to setup two different EEPROM transfers at different baud rates.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mk) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/spi/async/spi_multi_slave/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mk_mcj_curiosity_pro.X | MPLABX project for [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113) |
| pic32mk_mca_curiosity_pro.X | MPLABX project for [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mk_mcj_curiosity_pro.X | [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113) |
| pic32mk_mca_curiosity_pro.X | [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A) |
|||

- To run the demo, the following additional hardware are required:
    - Two [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) boards
    - Two [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) boards

### Setting up [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113)

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer
- Install [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) boards on to the [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) boards
- Connect [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) boards on to the "EXT1" (J501) and "EXT2" (J502) headers of the PIC32MK MCJ Curiosity Pro Development Board

### Setting up [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A)

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer
- Install one [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) board on to the mikroBUS socket of PIC32MK MCA Curiosity Pro Development Board
- Install another [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) board on to the [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board
- Connect [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board on to the "EXT1" (J501) header of the PIC32MK MCA Curiosity Pro Development Board


## Running the Application

1. Build and program the application using its IDE
2. The LED turns ON when the data read from the EEPROMs matches with the data written to the EEPROMs

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113) | LED2 |
|  [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A) | LED1 |
|||
