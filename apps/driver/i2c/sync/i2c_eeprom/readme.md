[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# I2C driver synchronous - I2C EEPROM

This example application shows how to use the I2C driver in synchronous mode to perform operations on the EEPROM.

## Description

This example uses the I2C driver in synchronous mode to communicate with the EEPROM to perform write and read operations in Bare-Metal environment. This application uses I2C driver to read and write data from an AT24CM02 EEPROM device.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mk) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/i2c/sync/i2c_eeprom/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mk_mcj_curiosity_pro_freertos.X | MPLABX project for PIC32MK MCJ Curiosity Pro Board |
| pic32mk_mcm_curiosity_pro_freertos.X | MPLABX project for PIC32MK MCM Curiosity Pro Board |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mk_mcm_curiosity_pro_freertos.X | PIC32MK MCM Curiosity Pro Board |
| pic32mk_mcj_curiosity_pro_freertos.X | PIC32MK MCJ Curiosity Pro Board |
|||

- To run the demo, the following additional hardware are required:
    - One [EEPROM 3 Click](https://www.mikroe.com/eeprom-3-click) board

### Setting up PIC32MK MCJ Curiosity Pro Board

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer
- Install the [EEPROM 3 Click](https://www.mikroe.com/eeprom-3-click) board on to the [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board
- Connect the [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board to the EXT1 header (J501) of the PIC32MK MCJ Curiosity Pro Development Board

### Setting up PIC32MK MCM Curiosity Pro Board

- Connect a micro USB cable to the USB DEBUG port J500
- Install the [EEPROM 3 Click](https://www.mikroe.com/eeprom-3-click) board on to the mikroBUS socket J300 of PIC32MK MCM Curiosity Pro Development Board

## Running the Application

1. Build and program the application using its IDE
2. The LED is turned ON when the value read from the EEPROM matched with the written value

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  PIC32MK MCJ Curiosity Pro Board | LED2 |
|  PIC32MK MCM Curiosity Pro Board | LED2 |
|||