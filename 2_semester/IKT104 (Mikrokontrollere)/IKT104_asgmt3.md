---
alias: "IKT104 Assignment 3 - I2C: Temperature and humidity"
---

# Assignment 3 - I2C: Temperature and humidity


## Preparations

This assignment assumes you have completed all steps of the previous assignments. The resources and general instructions from previous assignments are still useful here, this assignment will only list new relevant resources.

1.  Create a new program for target DISCO-L475VG-IOT01A (B-L475E-IOT01A) under git folder (_<course folder>/assignments/_) called _assignment_3_. You can choose to create a new program based on example _mbed-os-example-blinky-baremetal_ or simply take a copy of a previous assignment. In any cases make sure to link _mbed-os_ library to the shared instance you previously created and make a clean build.  
      
    
2.  Install the STM32 HTS221 library to your project from URL [https://os.mbed.com/teams/ST/code/HTS221/Lenker til en ekstern side.](https://os.mbed.com/teams/ST/code/HTS221/)  

![[Pasted image 20230109154638.png]]

      
    
3.  Add Mbed version of [the DFRobot LCD library Lenker til en ekstern side.](https://drive.google.com/file/d/1_pAloGqN2qxBgUnQEKW5XsiAl8n0NUxe/view). Extract the files next to your main.cpp file in Mbed Studio. The constructor takes LCD number of columns, rows, which pins to use for SDA and SCL, print to LCD with printf syntax:
    ```
    DFRobot_RGBLCD lcd(16, 2, D14, D15); lcd.init(); lcd.printf("Number: %i", 42);
    ```
4.  You will probably use float in printout, e.g. printf("Temp: %.1f C", temp). Open file mbed_app.json and set:  
    ```
    "platform.minimal-printf-enable-floating-point": true,  
    "platform.stdio-minimal-console-only": false
    ```

## Resources

-   [LCD examples Lenker til en ekstern side.](https://github.com/DFRobot/DFRobot_RGBLCD/tree/master/examples)(Note: Arduino examples, but you will see examples of to use the DFRobot LCD Library)
-   [HTS221 API description Lenker til en ekstern side.](https://os.mbed.com/teams/ST/code/HTS221/docs/tip/classHTS221Sensor.html) 
-   [Board pinoutsLenker til en ekstern side.](https://os.mbed.com/platforms/ST-Discovery-L475E-IOT01A/)
-   [InterruptInLenker til en ekstern side.](https://os.mbed.com/docs/mbed-os/v6.15/apis/interruptin.html)
-   [Board documentation Lenker til en ekstern side.](https://www.st.com/resource/en/user_manual/dm00347848-discovery-kit-for-iot-node-multichannel-communication-with-stm32l4-stmicroelectronics.pdf)(see page 10 for sensor location)

## Requirements

In this assignment you will create a temperature / humidity device. Measured values comes from the HTS221 sensor that is mounted on the board connected to I2C2. These values are then displayed on the LCD which you must connect over I2C1. To test temperature put a finger on the temperature / humidity sensor to heat it up. Breathe on it to test humidity.

1.  5% Connect a button to a digital input
2.  10% Connect the RGB LCD to I2C1 and VCC/GND. (see underside of the LCD)
3.  10% Read the temperature and humidity values from the sensor and print them (use serial monitor to see them)
4.  20% Show the current temperature on the LCD. The value should update regularly. (e.g. once per second)
5.  25% Toggle which value is shown with the button. Default is temperature. Press once and it changes to humidity. Press and it changes back.
6.  15% Set the backlight color of the LCD based on the temperature when showing temperature. < 20 C: blue. >= 20 <= 24: orange. > 24: red.
7.  15% Set the backlight color of the LCD based on the humidity when showing humidity. 0% humidity: white. Then gradually fade to blue (how blue = humidity). 100%: Fully blue.

## Delivery

Deliverer the following as text in Canvas:

-   Link to Bitbucket where to code has been delivered.  
    Directly to the file if there is only 1, or the directory if more than 1.
-   Link to YouTube (or other video service) with video showing each of the requirements.  
    Make sure that each requirement you have completed is clearly shown.  
    You don't need to show the actual code, just which of the requirements are met.