---
alias: "IKT104 Assignment 4 - Interrupts: external and watchdog"
---

# Assignment 4 - Interrupts: external and watchdog

## Preparations

This assignment assumes you have completed all steps of the previous assignments. The resources and general instructions from previous assignments are still useful here, this assignment will only list new relevant resources.

1.  Create a new program for target DISCO-L475VG-IOT01A (B-L475E-IOT01A) under your git folder (_<course folder>/assignments/_) called _assignment_4_.  
      
    
2.  Enable the watchdog functionality in your project. See the lecture for how to do this.

## Resources

-   [WatchdogLenker til en ekstern side.](https://os.mbed.com/docs/mbed-os/v6.15/apis/watchdog.html)
-   [Timer Lenker til en ekstern side.](https://os.mbed.com/docs/mbed-os/v6.15/apis/timer.html)

## Requirements

In this assignment you will create a stop watch with a somewhat peculiar behavior. The stop watch will count upwards as long as the user periodically pushes a button. If the button isn't pushed for a certain amount of time the stop watch resets. The reset will happen with the watchdog.

Since the functionality of this odd device is a bit more complicated than before try to focus on understanding and solving one problem at a time.

1.  10% Connect two buttons to digital inputs. Configure them with external interrupts, you are not allowed to read these buttons with _digitalRead()_.  
    To prevent button bounce (unstable signal) use falling edge interrupts and set a variable in the interrupt that is later checked in the loop.
2.  10% Connect the RGB LCD to I2C1 and VCC/GND. (see underside of the LCD)
3.  20% Print the current stop watch time on the LCD, with two decimal points. You can use 
    
    _timer.elapsed_time__()_ since started and cast to milliseconds. See example at the Mbed OS API reference and tutorials.  
    
4.  20% Configure the watchdog to trigger after 10 seconds
5.  20% Refresh the watchdog when the first button is pressed. Thus the button must be pressed at least every 10 seconds, otherwise the stopwatch resets.
6.  20% Pause / unpause the timer when the second button is pressed. While the timer is paused the first button does not have to pressed to prevent resets.

## Delivery

Deliverer the following as text in Canvas:

-   Link to Bitbucket where to code has been delivered.  
    Directly to the file if there is only 1, or the directory if more than 1.
-   Link to YouTube (or other video service) with video showing each of the requirements.  
    Make sure that each requirement you have completed is clearly shown.  
    You don't need to show the actual code, just which of the requirements are met.