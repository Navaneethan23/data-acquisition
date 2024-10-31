# data-acquisition
#Communication protocols
#Embedded C
#LPC2129
Features :
Data Acquisition:
RTC Data: Retrieves date and time from the RTC module using I2C.
Temperature Sensor Data: Collects temperature data from a sensor using I2C or SPI, based on the sensor type.
Communication Interfaces:
I2C: Used for communication with the RTC and some temperature sensors.
SPI: Used for communication with SPI-compatible temperature sensors.
UART: Transfers data from the microcontroller to a PC for display or logging.
Requirements
Microcontroller with UART, I2C, and SPI support (e.g., STM32, Arduino, LPC2129, ARM Board)
PC with serial communication support and compatible data visualization software (e.g., Tera Term, CoolTerm, or custom software)
RTC Module (e.g., DS3231 for I2C)
Temperature Sensor (e.g., LM75 for I2C or MAX6675 for SPI)
Embedded C Libraries for I2C, SPI, and UART as per your microcontroller
Usage
Initial Setup
Initialize Communication Protocols:

Configure I2C for RTC communication.
Set up SPI (if using an SPI temperature sensor).
Initialize UART for data transmission to the PC.

Read Data:
Use I2C to retrieve date and time from the RTC.
Use I2C or SPI to read temperature data, depending on the sensor type.

Transmit Data to PC:
Send formatted data (e.g., YYYY-MM-DD HH:MM:SS, Temperature: XX.XX °C) via UART to be displayed or logged by the PC.
Code Structure
rtc.c / rtc.h: Functions for reading date and time from the RTC using I2C.
temp_sensor.c / temp_sensor.h: Functions for reading temperature from the sensor using I2C or SPI.
uart.c / uart.h: UART communication functions to transfer data to the PC.
main.c: Initializes protocols and runs the main data acquisition and transmission loop.

SAMPLE OUTPUT:
Time: 2024-10-31 14:25:10, Temperature: 23.45°C
Time: 2024-10-31 14:25:11, Temperature: 23.47°C

