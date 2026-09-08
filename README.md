# Interfacing a 16×2 LCD with Arduino using an I2C Module for Sensor Data Display

## Aim

To interface a **16×2 LCD display with Arduino using an I2C module** and display sensor data on the LCD.

## Objectives

- To understand the operation of a 16×2 LCD.
- To interface the LCD with Arduino using an I2C module.
- To reduce the number of GPIO pins required for LCD communication.
- To read sensor data using Arduino.
- To display the sensor readings on the LCD.

## Hardware / Software Tools Required

### Hardware

- Arduino UNO
- 16×2 LCD Display
- I2C LCD Module (PCF8574-based)
- DHT11 Temperature and Humidity Sensor
- Breadboard
- Jumper wires
- USB cable

### Software

- Arduino IDE
- Arduino C/C++ programming language
- LiquidCrystal_I2C library
- DHT sensor library

## Components

### 16×2 LCD
### I2C Module
### Circuit Connections
### I2C Communication
### Working Principle

1. The DHT11 sensor measures temperature and humidity.
2. Arduino reads the sensor values through the digital data pin.
3. The Arduino processes the received sensor data.
4. The processed values are sent to the LCD through the I2C interface.
5. The LCD displays the temperature on one line.
6. The humidity is displayed on the second line.
7. The readings are periodically updated.
 
# DIAGRAM:

<img width="923" height="443" alt="image" src="https://github.com/user-attachments/assets/c0045e52-162c-44b8-9d86-a119cc8b754d" />

 
 
# PROGRAM:
```
#include <Wire.h>
#include <LiquidCrystal_I2C.h>

LiquidCrystal_I2C lcd(0x27, 16, 2);

void setup() {
  lcd.init();
  lcd.backlight();

  lcd.setCursor(0, 0);
  lcd.print("HELLO");

  lcd.setCursor(0, 1);
  lcd.print("JANI, DIVYA");
}

void loop() {
}
```

 
# OUTPUT

<img width="1254" height="974" alt="image" src="https://github.com/user-attachments/assets/9d633986-6ea7-4329-92b1-13747ff0c872" />



# RESULT
Thus, the ADC is interfaced with ARM LPC 1768 microprocessor.




