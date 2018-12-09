# Raspberry Pi B Digital Dashboard

## Main Idea : To create a a portable speedometer that can give reading for velocity,speed & acceleration using a Raspberry Pi 3 B 
I am going to attach some good-to-have links for pinouts,schematic diagrams and manuals

[product page](https://www.adafruit.com/product/2298)

[Github page for Fritzing parts](https://github.com/adafruit/Fritzing-Library)

## Nov 20th- Hardware / Enclosure
### Update on enclosure
I have now recieved my case and finished cleaning it up from the plastic debris. The top of the case whcih should show the screen and the 4 buttons is there but isn't aligned correctly with the screen itself. I have attached pictures of the enclosure below.

![withouttop](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/20181201_141259.jpg)
![bottomsdcard](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/20181201_141351.jpg)
![ports](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/20181201_141714.jpg)
![withscreen](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/20181201_141722.jpg)
![otherports](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/20181201_141240.jpg)

### Current Progress

All the internals are working and only piece of hardware required is the case.Case is now aquired and acrylic drawing of stand is on the way.

[Pi Stand STL File](DigitalDashboard/pistand.stl)

[Pi Bottom STL File](DigitalDashboard/Bottom4.stl)

[Pi Top STL File](DigitalDashboard/pitft35-top.stl)

### Problems and Opportunities
I just recieved a email from the prototype lab and they said I should recreate the pi stand in acrylic using Corel Idraw which I will and upload the design to Github.

### Financial Status
As I discussed in my last week blog about buying a keyboard, I have now recieved the invoice from Amazon.

![KeyboardInvoice](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/keyboardinvoice.png)

## Nov 13th- Hardware Demonstrating

### Current Progress
Everything is going as planned, now I have sent the prototype lab the 3d printed designs for the Raspberry pi case! Once I receive the 3d printed case I can recreate the case according to my button layout on the display. :white_check_mark:

This is what happens when you run the event demonstration

![demonstration](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/20181113_205534.jpg)

This is the outcome when the screen is touched and a output is given 

![touched screen](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/20181113_205612.jpg) 

### Problems and Opportunities
Now that my touchscreen works fine I had to demonstrate that its picking up accurate touches. To do that I installed the "event test" and "touchscreen library" packages.

### This is the required code for the packages and command

```C
'For the event test and touchscreen library packages'
sudo apt-get install evtest tslib libts-bin

'Event test tool'
sudo evtest /dev/input/touchscreen
```

### Financial Status
Since my raspberry pi uses a touchscreen display I am required to bring a keyboard and mouse into class. I will invest in a wireless keyboard and mouse for portability. 

## Nov 6th- Hardware Testing

### Current Progress
Everything is going as planned, now I am trying to get the X and y coordinates to pop up in terminal to showcase the capacitive screen working! :white_check_mark:

### Problems and Opportunities
I could not create a PCB as discussed with Professor Medri, so I dont have any PCB to showcase.

### Financial Status
No extra money was spent on this project

## Oct 30th - Progress Report
### Activities versus the schedule
Everything is on schedule as I have the Raspberry Pi and screen working    :white_check_mark:

### Current Progress 
As of now I have the Adafruit Capactive Touchscreen working on top of my Raspberry pi B. Got both the screen and the touch working well! To get the screen to work I ran a script that Adafruit provided.

### This is the script file

```C
 cd ~
 wget https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/adafruit-pitft.sh
 chmod +x adafruit-pitft.sh
 sudo ./adafruit-pitft.sh
```
### This is the i2c Detect for my device

This is the ![i2c](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/ic2.png)
### Problems and Opportunities

The most frequent problem that I ran into was choosing the incorrect display driver when running the script on my raspberry pi. Installing the incorrect driver can casue issues for the display. Also I chose to use gui mode as terminal mode doesnt allow for any gui. My device wont allow me to create a PCB as it requires all 40 GPIO pins to be used by the touchscreen.Professor Medri allowed me to continue with no PCB design.

### Financial Status

No extra money was spent on this project

## Oct 23rd - Fritzing Diagram And completed Breadboarding 

### Completed Breadboarding for the Raspberry Pi,Screen and Breadboard

### Working Display
![Working Display](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/2.8%20inch%20Capacitive%20touchscreen.jpg)

This is the [Fritzing Diagram](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/pifritzing.fzz)

This requires the Fritzing Software to see. See below for a PNG of the Diagram

This is the image ![Fritzing Diagram PNG](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/BreadboardDiagram.png)

## Oct 16th - UML Diagram

This is the ![UML diagram](https://raw.githubusercontent.com/KaranRajKanwar/DigitalDashboard/master/Digital%20Dashboard%20UML%20Diagram.png)

## Oct 2nd - Proof of Purchase

This is the [proof of pruchase](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/Proof%20of%20purchase.pdf)

## Sept 25th - Project Budget

This is the [project budget](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/DigitalDashboardBudget.xlsx)

## Sept 18th - Project Schedule

This is the [project schedule](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/schedule.mpp)

## Sept 11th - Project Proposal

This is the [project proposal](https://github.com/KaranRajKanwar/DigitalDashboard/blob/master/DigitalDashboard%20Proposal.xlsx)
