# Raspberry Pi 4 Model B Setup

The following instructions will show you how to set up a Raspberry Pi 4 Model B for the correct communications box configuration that will be used during development and field testing.

## Materials
- Raspberry Pi
- Raspberry Pi power cable
- Computer with SD card slot and internet access
- FTDI cable
- USB C to Outlet Brick
- Ethernet cable
- Micro SD Card (blank 256 GB)
- Micro SD to SD card adapter
- Extra connectors with one male/one female ends

## Software
- [Raspberry Pi Imager](https://www.raspberrypi.com/software/)
- [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) -- putty-64bit-0.76-installer.msi was used in this example

## Procedure
1. Install the software listed above to your computer.
2. Insert the blank micro SD card into the micro SD to SD card adapter and then into your computer.
3. Create a Raspberry Pi OS/Raspian image using the Raspberry Pi Imager.\
   a. Open the Raspberry Pi Imager on your computer and select "Raspberry Pi OS (64-Bit)" as the Operating System.\
   ![Raspberry Pi Imager](https://www.raspberrypi.org/app/uploads/2020/12/image-1-500x331.png)
4. Remove the micro SD from your computer and insert it into the Pi.
5. Connect the power cable to the Pi.
6. Connect one end of the Ethernet cable to either of the two Ethernet ports on the Pi
7. Connect the other end to your computer or another device port that has internet access. This will allow your Pi internet access.
8. Connect the USB end of the FTDI cable to your computer.
9. Connect the other end to the breakout pins on the Raspberry Pi such that the following pins are connected to their corresponding cable slots as listed in the table below.
   
| Raspberry Pi Pin Number | Raspberry Pi Pin Name | FTDI Cable Color | FTDI Cable Name |
| :---------------------: | :-------------------: | :--------------: | :-------------: |
| 6                       | GND                   | Black            | GND             |
| 8                       | GPIO 14 (TXD)         | Yellow           | RXD             |
| 10                      | GPIO 14 (RXD)         | Orange           | TXD             |\

Note: If the FTDI cable is harnessed together, you may need to use the extra connector wires to reach the Pi pins.\
![Raspberry Pi Pinout](https://www.raspberrypi.com/documentation/computers/images/GPIO-Pinout-Diagram-2.png)
![FTDI Cable](https://archive.fabacademy.org/2016/fablabesan2016/students/328/images/pasted%20image%20879x348.jpg)

10. Check that the FTDI cable connection is showing up on your computer by checking the Device Manager. There should be a COMx listed under "Ports (COM & LPT)".
11. Once you have found the connection, open PuTTY on your computer and select a Serial connection type. Change the "Speed" to 115200 and the "Serial line" to the COM port the FTDI cable was detected on. Click "Open".\
![PuTTY Window](https://i.stack.imgur.com/6cT0p.jpg)
12. After opening the PuTTY connection and connecting the power to the Pi, the login prompt for the Pi should come up. Enter the default login information.
    
| Login | Password  |
| :---: | :-------: |
| pi    | raspberry |

13. Change the password from the default in the command line console.\
`passwd`\
`[Enter new password]`
-----------
## You are done and ready to use the Pi for development!
   
   
