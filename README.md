# INTERFACING-OF-ADC-WITH-ARM-PROCESSOR

# AIM: 
   To interface and toggle the led with ARM LPC 1768 microprocessor           
           
# COMPONENTS REQUIRED:

## Hardware:
ARM LPC1343 / LPC1768
LCD module
## Software:
Coocox IDE

# PROCEDURE:
Step 1: Go to start All programs  COIDE.
Step 2: Give a suitable file name for your project and give the destination folder and then next. Step 3: Go to chip NXP LPC 13XX  LPC1343  Next.
Step 4: Select the required library file (SYSCON and GPIO) from the repository. Step 5: A new project will be created.
Step 6: Double click on main.c and type the program.
Step 7: Add the required library source file to the project (Right click on include Add file to group and
add the source file).
Step 8: Build the program using build option.
Step 9: Flash the program by clicking on download code to flash. Step 10: Interface the required component and note down the output. ADD FILES:
Repository:
CMSIS core, CMSIS boot, common header files, SYSCON, GPIO.

# Source files:
simple example.c, Uart Receiver interrupt.c, lcd.c, lcd.h
 
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




