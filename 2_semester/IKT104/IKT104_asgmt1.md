---
alias: "IKT104 Assignment 1 - Getting started"
---

# Assignment 1 - Getting started
- [ ] Finish Assignement 1 📅 2023-01-22

## Introduction

This first assignment exists mostly to verify that the tools work as they should and for you to get familiar with the kit. You will also learn how to communicate between the microcontroller to the PC using serial communication, and to control an LED with a digital output.

**NOTE:** If Mbed Studio fails to upload your program to the board you might be using a charging cable, not a data cable. You can try a different cable before you ask for help.

## Preparation

1.  Complete [Course preparations](https://uia.instructure.com/courses/12507/pages/course-preparations "Course preparations") if you haven't already. Every member of the group should do this.  

2.  Go to your _<course folder>_ and create new folder _assignments_. You should avoid comitting and pushing large folders. Open Git Bash (Windows) or Terminal (OSX/Linux), go to _<course folder>/assignments_ and enter the following command: 

```
echo -e "BUILD\nmbed-os\n.mbed\n.github\n*.md" > .gitignore
```

3.  Open Mbed Studio and select your _<course folder>/assignments_ as workspace. Connect the development board to the PC or select target DISCO-L475VG-IOT01A (B-L475E-IOT01A). Create a new program based on example _mbed-os-example-blinky-baremetal_ and name the program _assignment_1_. Now instead of storing the Mbed OS in the program folder, select link to the existing shared Mbed OS git repository you created during [Course preparations](https://uia.instructure.com/courses/12507/pages/course-preparations "Course preparations") and add program. You should now have the first assignment located at _<course folder>/assignments/assignment_1_.  
      
	If you rather select _mbed-os-example-blinky_ in stead of the bare metal example, you will include lots of libraries for connectivity (BLE, Cellular, LoRaWAN, WiFi, NFC) and Internet protocols which we will not use at this stage, but the compile time will be huge (depending on of how powerfull your PC is). This can be avoided if you download file  [mbedignore_no_network_connectivity.zip](https://uia.instructure.com/courses/12507/files/2028962?wrap=1 "mbedignore_no_network_connectivity.zip") [Last ned mbedignore_no_network_connectivity.zip](https://uia.instructure.com/courses/12507/files/2028962/download?download_frd=1), unzip and add _.mbedignore_ file next to your _main.cpp_ file in the project.  
      
    
4.  Make sure _assignment_1_ is selected as the active program. Build the program (press _the-blue-hammer-button_) and check the console output for errors. If everything is fine, upload the program (press _the-blue-play-button_) to the microcontroller and verify it is running OK (there should be one LED blinking on the development board).

## Resources

-   [LED resistor calculatorLinks to an external site.](https://ledcalculator.net/)
-   [DigitalOutLinks to an external site.](https://os.mbed.com/docs/mbed-os/v6.15/apis/digitalout.html)
-   [BufferedSerialLinks to an external site.](https://os.mbed.com/docs/mbed-os/v6.15/apis/serial-uart-apis.html)

## Requirements

In this assignment you will create a program that lets you control an LED from the PC by pressing the 0 or 1 keys.

1.  25% Connect an LED (not blue) to an output with an appropriate resistor
2.  10% Configure the IO as output
3.  10% Configure the serial port with baud rate 115200
4.  10% Read 1 byte from the serial port:
    -   15% If the byte is '0' turn the led off
    -   15% If the byte is '1' turn the led on
    -   15% Do this forever

## Testing

To test the program you must first upload it to the microcontroller. When the development board is connected to your PC, a _Serial Monitor_ tab should be seen in the IDE. If not press _View_ and select the _Serial Monitor_, then press a key to send that key to the microcontroller. If the printout is corrupt, make sure that the baud rate is set to 115200. 

## Delivery

Deliverer the following as text in Canvas:

-   Link to Bitbucket where to code has been delivered.  
    Directly to the file if there is only 1, or the directory if more than 1.  
    Navigate to the delivery at [https://tools.uia.no/bitbucket Links to an external site.](https://tools.uia.no/bitbucket)and copy the URL from the browser.
-   Link to YouTube (or other video service) with video showing each of the requirements.  
    You don't need to show the actual code, just which of the requirements are met.



ch ikt104/mbed-os    # Change directory to your Mbed OS directory  
git checkout mbed-os-6.16.0   # Check out tag for Mbed OS release 6.16.0


# Svar

## Link to project:
https://tools.uia.no/bitbucket/projects/IKT104G23V/repos/sondrr07/browse/assignments/assignment_1/main.cpp


