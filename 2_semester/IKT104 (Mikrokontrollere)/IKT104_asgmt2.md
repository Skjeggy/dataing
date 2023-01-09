---
alias: "IKT104 Assignment 2 - Light dimmer"
---

# Assignment 2 - Light dimmer
- [ ] Finish Assignment 2 📅 2023-01-29

## Preparation

This assignment assumes you have completed all steps of the previous assignments. The resources and general instructions from previous assignments are still useful here, this assignment will only list new relevant resources.

1.  Create a new program for target DISCO-L475VG-IOT01A (B-L475E-IOT01A) under git folder (_<course folder>/assignments/_) called _assignment_2_. You can choose to create a new program based on example _mbed-os-example-blinky-baremetal_ or simply take a copy of your _assignment_1_. In any cases make sure to link _mbed-os_ library to the shared instance you previously created and make a clean build.

## Resources

-   [DigitalInLinks to an external site.](https://os.mbed.com/docs/mbed-os/v6.15/apis/digitalin.html)
-   [AnalogInLinks to an external site.](https://os.mbed.com/docs/mbed-os/v6.15/apis/i-o-apis.html)
-   [PwmOutLinks to an external site.](https://os.mbed.com/docs/mbed-os/v6.15/apis/pwmout.html)

## Requirements

In this assignment you will create a program that allows you to control the brightness of three LEDs using a potentiometer (turnable knob) and a button.

1.  10% Connect a button to a digital input
2.  20% Connect a potentiometer to an analog input
3.  20% Connect 3 LEDs of your choice to PWM outputs (place them in a row on the breadboard).  
    See the [pin overview Links to an external site.](https://os.mbed.com/platforms/ST-Discovery-L475E-IOT01A/)for which pins support PWM
4.  10% Read the value of the potentiometer ten times per second
5.  30% Use the read value to set the brightness of the LEDs.  
    The lowest 1/3 sets the brightness of the first LED, the middle 1/3 sets the brightness of the second LED and the last 1/3 sets the brightness of the last LED.  
    Meaning: Knob fully turned off = no LEDs are on. Turn it slowly and the first LED fades in as you turn, then the second LED fades in and finally the last LED fades in.
6.  10% Holding in the button sets all LEDs to full brightness. Releasing sets them back to the potentiometer value.

## Delivery

Deliverer the following as text in Canvas:

-   Link to Bitbucket where to code has been delivered.  
    Directly to the file if there is only 1, or the directory if more than 1.
-   Link to YouTube (or other video service) with video showing each of the requirements.  
    Make sure that each requirement you have completed is clearly shown.  
    You don't need to show the actual code, just which of the requirements are met.
