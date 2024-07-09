# BudgetCAN G4

Hardware files for a simple CAN and LIN device built around an STM32 G4 MCU

![Alt text](budgetcan_g4_hw.png?raw=true "budgetcan_g4_hardware")

## Description

The BudgetCAN G4 Hardware is designed to implement the full CAN potential of the STM32G4 MCU.  The hardware has been designed with the following features:
* USB-C connector for robust connectivity to a host machine
* 3 CANFD channels each with SW selectable termination resistors
* 1 LIN channel with SW selectable master pull-up
* 12V power input provides power for LIN and a 3A 5V regulator
* Debug header pinout for STLINK v3 Mini 14-pin connector - the VCP pins are routed to a UART for debugging
* Onboard 8Mhz crystal provides high clock accuracy for CANFD
* 5V power MUX to ensure graceful handoff between USB and 12V power supplies
* 3x configurable LEDs for status indications
* Automotive grade Molex Mini50 connector
* 4 layer PCB
* BOM cost under $15USD

## File usage

* The HW was designed with KiCad8
* Part BOM included with the schematic is complete for JLCPCB parts

## Firmware
Firmware is available for this hardware in the budgetcan firmware repository.  This firmware is based on the gs_usb driver and currently is fully supported in Linux and will work in Windows using the same drivers that have been developed for gs_usb.
* https://github.com/ryedwards/budgetcan-fw


You can also use the included STM32CubeMX .ioc file to generate your own firmware.  

This hardware can also be used as a standalone device (gateway module, simulated ECU, etc) since it has a 12V input and can be used headless.

## Help

If you find any issues with the hardware please submit an issue into GitHub

## License

This project is licensed under the MIT License - see the LICENSE.md file for details


