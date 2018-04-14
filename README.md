# Automatic-Digital-Multimeter
Low-cost multi-channel digital multimeter using PSoC 4/5.
This project is intended to constantly monitor/ plot one or more voltage, capcacitance , resistance, current.  
Currently only supports DC voltage upto 5V and Capacitance in pF. 

## Operating Requirements ##
* Windows XP/7/10 and everything in between
* PSoC Programmer http://www.cypress.com/file/410636/download
* Python 2.7
* PSoC creator(if you want to edit the source, which is recomended)
## Hardware ##
CY8CKIT-043 is used here as it cheap and readily available, but it can be modified for any Cypress Kit. 

## Description ##
PSoC programmer provides COM that can be used with win32com API in python. 
This also gives python the ability to directly talk to the MCU over I2C/SPI/UART. 
I2C is more structured and pretty scalable and is hence used here. 
PSoC 4 is configured as an I2C slave with a register map.

Register Address | Type of data | Channel name 
------------- | ------------- | ---------------
0x00  | float32 | V0
0x04  | float32 | V1
0x08  | float32 | V2
0x0C  | float32 | V3
0x10  | uint16  | C0
0x12  | uint16  | C1
0x14  | uint16  | C2
0x16  | uint16  | C3

## Future Enhancements ##
AC Voltage
DC Current 
AC Current
Inductance
Cross platform (linux and MAC)
