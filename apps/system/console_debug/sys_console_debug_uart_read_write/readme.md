---
parent: Harmony 3 driver and system service application examples for PIC32MK family
title: Console Debug System Service using UART 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# Console Debug System Service using UART

This example application demonstrates the UART based console and debug system service.

## Description

- The application example first demonstrates the various debug system service macros
- It then demonstrates the console related APIs
- The application asks the user to enter a character on the console which is echoed back using the console system service read/write APIs

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mk) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/system/console_debug/sys_console_debug_uart_read_write/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mk_gp_db.X | MPLABX project for [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) |
| pic32mk_mcj_curiosity_pro.X | MPLABX project for [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113) |
| pic32mk_mcm_curiosity_pro.X | MPLABX project for [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A) |
| pic32mk_mca_curiosity_pro.X | MPLABX project for [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mk_mcm_curiosity_pro.X | [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A) |
| pic32mk_mcj_curiosity_pro.X | [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113) |
| pic32mk_mca_curiosity_pro.X | [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A) |
| pic32mk_gp_db.X | [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) |
|||

### Setting up [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106)

- Connect micro USB cable to the 'Debug USB' connector(J12) on the board to the computer
- Connect a micro USB cable to the USART-USB port J25. This will enumerate as a COM port on the PC

### Setting up [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113)

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer. This will enumerate as a COM port on the PC

### Setting up [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A)

- Connect a micro USB cable to the USB DEBUG port J500
- Connect a micro USB cable to the USB to UART port J400. This will enumerate as a COM port on the PC

### Setting up [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A)

- Connect micro USB cable to the 'Debug USB' connector(J1) on the board to the computer. This will enumerate as a COM port on the PC

## Running the Application

1. Open the Terminal application (Ex.:Tera term) on the computer
2. Connect to the EDBG Virtual COM port and configure the serial settings as follows:
    - Baud : 115200
    - Data : 8 Bits
    - Parity : None
    - Stop : 1 Bit
    - Flow Control : None
3. Build and Program the application using its IDE
4. Observe the following output on the terminal

    ![output_1](images/output_sys_console_debug_uart_read_write_1.png)

    - First few prints demonstrate the output from the debug system service APIs
    - It then prints the free space available in the receive buffer
    - It then asks the user to enter 10 characters

5. After entering 10 characters, observe the following output on the terminal

    ![output_2](images/output_sys_console_debug_uart_read_write_2.png)

    - The output first prints the free space available in the receive buffer
    - Since 10 characters are pending to be read out from the receive buffer, the free space in the receive buffer is reduced by 10
    - After this, it prints the received characters on the terminal
    - Application then waits for the transmit buffer to become empty
    - Once empty, the application prints the free space available in the transmit buffer, which should be same as the size of the transmit buffer configured in MHC minus 1

6. After this, the demonstration asks the user to enter a character, and echoes it back on the terminal.

    ![output_3](images/output_sys_console_debug_uart_read_write_3.png)

    - LED toggles every-time the character is printed on the terminal

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  [PIC32MK GP Development Kit](https://www.microchip.com/developmenttools/ProductDetails/dm320106) | LED1 |
|  [PIC32MK MCJ Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/DT100113) | LED2 |
|  [PIC32MK MCM Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV31E34A) | LED2 |
|  [PIC32MK MCA Curiosity Pro Board](https://www.microchip.com/en-us/development-tool/EV15D86A) | LED1 |


