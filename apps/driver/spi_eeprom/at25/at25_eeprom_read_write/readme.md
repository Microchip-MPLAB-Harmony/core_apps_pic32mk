[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# SPI EEPROM AT25 driver - EEPROM Read Write

This example application shows how to use the AT25 driver to perform read and write operations on AT25 series of EEPROM

## Description

This example uses the AT25 driver to communicate with the SPI based AT25 series of external EEPROMs to perform write and read operations in Bare-Metal environment.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mk) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/spi_eeprom/at25/at25_eeprom_read_write/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mk_gp_db.X | MPLABX project for [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) |
| pic32mk_mcj_curiosity_pro.X | MPLABX project for PIC32MK MCJ Curiosity Pro Board |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mk_mcj_curiosity_pro.X | PIC32MK MCJ Curiosity Pro Board |
| pic32mk_gp_db.X | [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) |
|||

- To run the demo, the following additional hardware are required:
    - One [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) board

### Setting up [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106)

- Connect micro USB cable to the 'Debug USB' connector(J12) on the board to the computer
- Install [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) board on to the J1 click board slot provided on [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106)

### Setting up PIC32MK MCJ Curiosity Pro Board

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer
- Install [EEPROM 4 Click](https://www.mikroe.com/eeprom-4-click) board on to the [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board
- Connect [mikroBUS Xplained Pro](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) board on to the "EXT1" header (J501) of the PIC32MK MCJ Curiosity Pro Development Board

## Running the Application

1. Build and program the application using its IDE
2. The LED is turned ON when the value read from EEPROM matches with the written data

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) | LED2 |
|  PIC32MK MCJ Curiosity Pro Board | LED2 |
|||
