---
alias: "IKT104 Assignment 5 - Timers"
---

# Assignment 5 - Timers


## Preparations

This assignment assumes you have completed all steps of the previous assignments. The resources and general instructions from previous assignments are still useful here, this assignment will only list new relevant resources.

1.  Create a new program for target DISCO-L475VG-IOT01A (B-L475E-IOT01A) under your git folder (_<course folder>/assignments/__)_ called _assignment_5_.  
    

## Resources

-   [Mbed OS documentationLenker til en ekstern side.](https://os.mbed.com/docs/mbed-os/v6.15/apis/index.html)
-   Lecture notes

## Requirements

In this assignment you will create an egg timer. Buttons are used for input, the [piezo buzzer Lenker til en ekstern side.](https://www.adafruit.com/product/160)(from the parts kit) is used to sound the alarm and the LCD will show the remaining time.

The default timer is 1 minute. The timer should start paused.

1.  10% Connect four buttons to digital inputs. You can use these with [interrupts Lenker til en ekstern side.](https://os.mbed.com/docs/mbed-os/v6.15/apis/interruptin.html)or with regular DigitalIn, that's up to you
2.  10% Connect the piezo buzzer to a [PWM output Lenker til en ekstern side.](https://os.mbed.com/docs/mbed-os/v6.15/apis/pwmout.html)(this way you can control the tone it plays)
3.  10% Connect the RGB LCD to I2C1 and VCC/GND. (see underside of the LCD)
4.  10% Show the remaining time on the LCD
5.  10% Button 1 should start/pause the timer
6.  10% Button 2 should reset the timer back to 1 minute and pause it
7.  10% Button 3 should add 5 seconds to the timer
8.  10% Button 4 should subtract 5 seconds from the timer
9.  20% Stop the countdown when the timer reaches 0 and sound the buzzer.  
    The countdown must be done with a _Timer_ or _Timeout_ from Mbed OS

## Delivery

Deliverer the following as text in Canvas:

-   Link to Bitbucket where to code has been delivered.  
    Directly to the file if there is only 1, or the directory if more than 1.
-   Link to YouTube (or other video service) with video showing each of the requirements.  
    Make sure that each requirement you have completed is clearly shown.  
    You don't need to show the actual code, just which of the requirements are met.