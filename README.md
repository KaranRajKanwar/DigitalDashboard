# DigitalDashboard Build Instructions
## Introduction

The digital dashboard is an interactive device that allows people to track their movements and actions. I am making this because it makes being able to keep statistics of your movement very easy, whether biking or in a car. All of this is easily understandable by its users as it works on a user-friendly customizable GUI on a 2.8-inch touch capacitive screen. This tracker will be storing data logs in its database when utilizing the DigitalDashboard, and to see your results you can view them on the screen on the fly. The data the DigitalDashboard will be holding is the average speed traveled, a source of transportation, average velocity, the date and where the screen was touched.

### System Diagram
![System Diagram](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/SystemDiagram.png)
    
## Bill of Materials/Budget
The budget for my project was $150 dollars, but after I bought everything and got it shipped to my house the total came out to be a bit over $400 as this includes the parts kits we are required to buy when we started this program.

|      Part Name               |         Part Number         |                Source                |Price with shipping & tax|
|------------------------------|-----------------------------|--------------------------------------|-------------------------|
| Raspberry Pi 3 Model B       |B01CD5VC92                   |[Amazon](https://tinyurl.com/yd8zt33y)|$55.99
|Raspberry Pi Case             |B01D8368RY                   |[Amazon](https://tinyurl.com/y7lkpouc)|$13.99
|Raspberry Pi 5V Power Supply  |B06Y431Y27                   |[Amazon](https://tinyurl.com/ya4kcvr3)|$19.13
|Sandisk 32gb microSDXC card   |B073JWXGNT                   |[Amazon](https://tinyurl.com/ydhm22or)|$19.65
|2 Mini Raspberry Pi Heatsinks |B014KKY19G                   |[Amazon](https://tinyurl.com/yawe5tvz)|$11.98
|HDMI Cable                    |B014I8SSD0                   |[Amazon](https://tinyurl.com/y6ups5wd)|$12.15
|Adafruit PiTFT Cap Touchscreen|B00XW2OI6A                   |[Amazon](https://tinyurl.com/ybco5so3)|$68.20
|Adafruit Faceplate & Buttons  |B019MGASTA                   |[Amazon](https://tinyurl.com/y8yd353a)|$29.98
|SMRaza Electronic Starter Kit |B01HRR7EBG                   |[Amazon](https://tinyurl.com/ycb737cn)|$58.08
|Wireless Keyboard             |B0173QNVT0                   |[Amazon](https://tinyurl.com/ydh8q29g)|$20.00
|Parts Kits                    |N/A                          |Humber Book Store                     |$120.00 
|Total price                   |                             |                                      |$430.00

* This project doesn't require a solder iron and solder, as there is no soldering required for the touchscreen to work with the raspberry pi.

* The SMRaza  Electronic Starter kit includes lots of accessories such as a breadboard, wires, LED's and much more but that stuff isn't required for the project. 

* [DigitalDashboard Budgeting](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/Blog%20Documentation/DigitalDashboard%20Budget.xlsx)

## Time Commitment
This project can be completed in 4 hours with ease considering you have the case printed and cleaned up from that protective residue.
* Settings up the raspberry pi with Raspbian OS (2 hours)
* Attaching the Capacitive touchscreen and getting it to work (1 hour)
* 3D printing the enclosure and cleaning it up(12+ hours)
* Getting everything put together(1 hour)
* Touchscreen Testing(30 mins)

**Total estimated time**: 4.5 hours to 5 hours not including the 3D-print time

## Mechanical Assembly
Installing the Touchscreen onto the raspberry doesn't require any custom PCB or soldering. Install the mini heatsinks by removing the adhesive from the bottom and place both heatsinks on the 2 chips on the Raspberry Pi motherboard. All you are required to do is place the touchscreen on top of the raspberry pi aligning with the pins.

Below are the 3D print .STL files attached for downloading.

![Top of 3D print](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/Blog%20Images/3D%20Print%20Top.stl)

![Bottom of 3D print](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/Blog%20Images/3D%20Print%20Bottom.stl)

Once mounted and powered up it gives us a white screen, nothing else. To fix this we are required to install the display drivers on the Raspberry Pi. To get the drivers type this in the terminal.
```C
 cd ~
 wget https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/adafruit-pitft.sh
 chmod +x adafruit-pitft.sh
 sudo ./adafruit-pitft.sh
```
When running these commands you will be asked if you want to use terminal only or GUI only, I chose GUI as you can use the terminal in that but in the terminal, you cant use the GUI. If you accidentally choose terminal you can revert to GUI by running the script again and choosing the right option. After doing this the screen will look like this.

![Working screen](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/2.8%20inch%20Capacitive%20touchscreen.jpg)

Now we are good to throw the Raspberry Pi with the attached touchscreen into the 3D-printed case. Make sure to wipe off any residue as it could get stuck near a contact point for the devices.

![Enclosure on](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/Top%20view%20with%20screen%20and%20case%20assembled.jpg)
![Usable ports](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/Side%20view%20without%20screen%20in%20case.jpg)
![Usable ports1](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/Side%20view%20of%20IO%20ports%20with%20case.jpg)
![Enclosure on without top](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/Top%20view%20without%20screen%20in%20case.jpg)

## PCB/Soldering
Not Required but I created a Fritzing design of how the connections look like for the 2 devices

![Fritzing](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/Breadboard%20Diagram.png)

## Power Up / Raspberry Pi setup
1. Download Raspbian disc image on a computer via ZIP download or torrent.
2. Unzip the downloaded file using any software of choice, I prefer WinRAR.
3. Write the disc image to the microSD card(must be a minimum of 8 GB), I prefer Win32 Disk Imager.
4. Plug in your choice of mouse, keyboard, display via HDMI, and power supply.
5. Install Raspbian on the Raspberry Pi by inserting the microSD card into the slot and giving it power.
6. On first boot you should be taken to a configuration screen, you don't have to do anything here, but I recommend changing your account password for security. If for some reason you were not able to see the configuration screen type the following command in terminal.
```C
sudo raspi-config
```
7. Update the repositories on the Raspberry Pi by running this command in the terminal.
```C
sudo apt-get update
sudo apt-get upgrade
```
## Unit Testing
If the touchscreen works and responds correctly with touches, it's confirmed that its been installed correctly but to make sure we can check our i2c address by running this command in the terminal.
```C
Sudo i2cdetect -y 1
```
![i2cdetect](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/i2c%20Test.png)

Running this command the value UU is placed on 30: and 8. That gives us 0x38 which is our devices correct i2c address. Now we confirm that we can demonstrate a program in which it states where the touchscreen was touched at and gives the x and y coordinates. In order to do this we must install the "event test" and "touchscreen libraries", this can be done by running these commands in the terminal.
```C
'For the event test and touchscreen library packages'
sudo apt-get install evtest tslib libts-bin

'Event test tool'
sudo evtest /dev/input/touchscreen
```

![Startup](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/teststart.png)
![testing](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Blog%20Images/testdemo.png)

## Production Testing
To make sure that the DigitalDashboard is good for production, we would test the sturdiness of the case and whether the software functions on all devices.
* Test the device and check if it's communicating with the Raspberry Pi by checking the i2c address. run this command in terminal to see if i2c is communicating
```c
Sudo i2cdetect -y 1
```
* Test the event handler for the touchscreen device to see if it's giving us accurate readings and to perform a nice first-time calibration.
