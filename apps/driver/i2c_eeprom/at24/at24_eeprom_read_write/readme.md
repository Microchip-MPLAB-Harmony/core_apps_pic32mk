---
parent: Harmony 3 driver and system service application examples for PIC32MK family
title: I2C EEPROM AT24 driver - EEPROM Read Write 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# I2C EEPROM AT24 driver - EEPROM Read Write

This example application shows how to use the AT24 driver to perform read and write operations on AT24 series of EEPROM

## Description

- This example uses the AT24 driver to communicate with I2C based External AT24CM0 series EEPROMs to perform write and read operations in Bare-Metal environment.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mk) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/i2c_eeprom/at24/at24_eeprom_read_write/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mk_mcj_curiosity_pro.X | MPLABX project for PIC32MK MCJ Curiosity Pro Board |
| pic32mk_mca_curiosity_pro.X | MPLABX project for PIC32MK MCA Curiosity Pro Board |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mk_mcj_curiosity_pro.X | PIC32MK MCJ Curiosity Pro Board |
| pic32mk_mca_curiosity_pro.X | PIC32MK MCA Curiosity Pro Board |
|||

- To run the demo, the following additional hardware are required:
    - One [EEPROM 3 Click](https://www.mikroe.com/eeprom-3-click) board

### Setting up PIC32MK MCJ Curiosity Pro Board

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer
- Install the [EEPROM 3 Click](https://www.mikroe.com/eeprom-3-click) board on to the [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board
- Connect the [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board to the EXT1 header (J501) of the PIC32MK MCJ Curiosity Pro Development Board

### Setting up PIC32MK MCA Curiosity Pro Board

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer
- Install the [EEPROM 3 Click](https://www.mikroe.com/eeprom-3-click) board on to the mikroBUS connector of the PIC32MK MCA Curiosity Pro Development Board


## Running the Application

1. Build and program the application using its IDE
2. The LED is turned ON when the data read from EEPROM matches with the written data

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  PIC32MK MCJ Curiosity Pro Board | LED2 |
|  PIC32MK MCA Curiosity Pro Board | LED1 |
|||
