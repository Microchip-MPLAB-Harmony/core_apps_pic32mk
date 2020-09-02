---
parent: Harmony 3 driver and system service application examples for PIC32MK family
title: SPI Driver synchronous - Self loopback multi client 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# SPI Driver synchronous - Self loopback multi client

This example demonstrates how to use the SPI driver in synchronous mode to achieve self-loop back between multiple clients in RTOS environment

## Description

- This example writes and reads back the same data (self loop back) for two different clients connected over the same SPI bus by using the multi client feature of a synchronous SPI driver

- The example also demonstrates how to setup two different client transfers at two different baud rates

- The example has three RTOS threads for the purpose:
    - **APP_CLIENT1_Tasks:**
        - This thread opens the SPI driver instance and performs a continuous loop back transfer
        - If the loop back is successful, the loop back is repeated every 100 ms
        - In case of an error, the thread closes the driver and suspends itself
    - **APP_CLIENT2_Tasks:**
        - This thread opens the SPI driver instance and performs a continuous loop back transfer
        - If the loop back is successful, the loop back is repeated every 100 ms
        - In case of an error, the thread closes the driver and suspends itself
    - **APP_MONITOR_Tasks:**
        - This thread checks the status of loop back done by the two client tasks and turns on the LED if the loop back transfer status reported by both the clients is successful

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mk) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/spi/sync/spi_self_loopback_multi_client/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mk_gp_db_freertos.X | MPLABX project for [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) |
| pic32mk_mcj_curiosity_pro_freertos.X | MPLABX project for PIC32MK MCJ Curiosity Pro Board |
| pic32mk_mcm_curiosity_pro_freertos.X | MPLABX project for PIC32MK MCM Curiosity Pro Board |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mk_mcm_curiosity_pro_freertos.X | PIC32MK MCM Curiosity Pro Board |
| pic32mk_mcj_curiosity_pro_freertos.X | PIC32MK MCJ Curiosity Pro Board |
| pic32mk_gp_db_freertos.X | [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) |
|||

### Setting up [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106)

- Connect micro USB cable to the 'Debug USB' connector(J12) on the board to the computer
- Use jumper wire to Connect MOSI and MISO lines of J1 connector
    - SPI6 MOSI signal is mapped to RB0
    - SPI6 MISO signal is mapped to RG9

### Setting up PIC32MK MCJ Curiosity Pro Board

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer
- Use jumper wire to connect "Pin 16 of J501 header" to "Pin 17 of J501 header"
    - SDI2 is mapped to RD6 that is routed to "Pin 17 of J501 header"
    - SDO2 is mapped to RC7 that is routed to "Pin 16 of J501 header"

### Setting up PIC32MK MCM Curiosity Pro Board

- Connect a micro USB cable to the USB DEBUG port J500
- Use jumper wire to connect Pin 5 to Pin 6 of mikroBUS header (J300)
    - SDI6 is mapped to RG9 that is routed to Pin 5 of mikroBUS header
    - SDO6 is mapped to RB0 that is routed to Pin 6 of mikroBUS header

## Running the Application

1. Build and program the application using its IDE
2. The LED is turned ON on Success

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) | LED2 |
|  PIC32MK MCJ Curiosity Pro Board | LED2 |
|  PIC32MK MCM Curiosity Pro Board | LED1 |
|||
