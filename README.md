# For More Project Documentation (parts, prices, licenses, and hookup), view the following link:
https://docs.google.com/document/d/1IHjDpGhEGYvSrTsLehtoSzCsxU5Pvv6ZDAVGaKjEqGU/edit# 

Our Group name is Newton's Busties. We are comprised of four members: Christopher, Harrison, David, and Elizabeth. This was our ENGR114 Project in Prof. Kazarinoff's class at PCC. 

![0311201604](https://user-images.githubusercontent.com/59817284/76715404-7f74de00-66e9-11ea-9abf-178ec6afeca6.jpg)

# Follow-the-Light
Sets up an apparatus that keeps your plant in maximum sunlight by moving your plant via a gondola to the spot in your windowsill with the most sunlight. Also generates a graph with python code to show where the plant moved.


## In the *[NewtonsBust.zip](https://github.com/CrazedCrusade/Follow-the-Light/files/4335050/NewtonsBust.zip)* file is the needed .ino arduino code files for running the stepper motor, and the multiple .py files for running the python code, generating the graphs, and controlling the arduino. In this file are the details for set-up:

## Basic Design
This was the first sketch of our set up for our idea:
![bsaic_carl](https://user-images.githubusercontent.com/59817284/76691707-099a4500-660b-11ea-95ea-d6d4f9a05dc5.png)

## How it works:
1)  The light sensors attached to the gondola are photo-resistors. They read how much light is striking the gondola at the time, then send the data as a anologue value to the attached arduino.
2)  The arduino then sends the anologue value (how much light is striking the gondola) to the attached computer. While the arduino does this, the arduino also tells the motor controller to continue to move the gondolla across its path. This allows the arduino to have light readings from multiple places. The Arduino sends both light on gondola, and position of gondola for the system to the attached computer.
3)  The computer then records a light versus position graph. The computer finds the positional value for the highest amount of light, and then sends a command to the arduino.
4)  The arduino then tells the motor controller to move the gondola to the position where the most light was recorded.
5)  At a set amount of time later, the process repeats so that maximum sunlight for the plant in the gondola is ensured.

### Things to note: 
* The system reads position based on the amount of turns the stepper motor has done, so the system does not actually read where the gondola is. The code has to be modified so that the gondola has a certain max range of motion (length of the gondola wire). 
* The photoresistors send a lower anologue value for more light. This is because they add voltage resistance to the system, which decreases the anologue value when more light is present.


# This is a Fritzing Schematic of the Hardware Hookup.
  (The .fzz file is located in the file cabinet of the repository (above))
![_untitledimage](https://user-images.githubusercontent.com/59817284/76695519-bee5f080-663d-11ea-8ce2-75ae3b9318ef.png)
Notice above that the AC wall outlet power to DC power for the stepper motor is not included in the Fritzing design. Neither is the computer usb to micro-usb for the arduino included in the Fritzing build. We also used a RedBoard instead of an Arduino Uno. The only difference in set-up between the Arduino Uno and the Redboard is the usb type C used for the computer to arduino connection instead of a micro-usb.


## Building the Gondola Stand:
Materials:
* 1 48" 2X4 
* 4 18" 2X4
* Screws

![gondola](https://user-images.githubusercontent.com/62195067/76709708-23489480-66be-11ea-8cb3-5612e4e13648.jpg)

This was assembled to hold up the gondola as if it were hung over a window. The top bar of the stand would represent the top of the window if someone were to use this for their house plant. The pulleys were fastened to the two upper corners. These were designed in OnShape and printed along with the mounting pieces. The string was then pulled across and wrapped around the pulleys, holding up the gondola. The gondola was designed in Tinkercad to hold the pot and dangle from the string. 

## Pulleys and Gondola:
![0311201612](https://user-images.githubusercontent.com/59817284/76710844-f6997a80-66c7-11ea-94f6-b31370b46397.jpg)

* Our pulleys and gondola were designed using the Onshape 3d modeling software. The only requirement for the pulleys is that they need to put the gondola line under tension, and one pulley must be turned by the stepper motor. The 3d printable STL pulley models are in located in the CARL STL folder at the top. 
![0311201600d](https://user-images.githubusercontent.com/59817284/76710860-15980c80-66c8-11ea-8fd3-880cbb22020c.jpg)

* Also note that the gondola should be designed to carry the photo-resistors so that the amount of light can be read where the gondola is.
## Running the Code:
We already created the code, so all you have to do is run it. 
1) Download the *[NewtonsBust.zip](https://github.com/CrazedCrusade/Follow-the-Light/files/4335050/NewtonsBust.zip)*
2) Find the downloaded file, right click, and then click "extract all." Extract it to the default location your PC chooses.
3) Open the Arduino IDE (You can get it online for free).
4) Go to File.
5) Click Open.
6) Open the extracted *NewtonsBust* folder. Open Arduino_Firmata_Stepper.
7) Follow the instructions in the code opened in the Arduino IDE.

## Results:
Youtube link to our first test:https://www.youtube.com/watch?v=yzFK8nZ47Xs
As can be seen from the video, Aragorn (representing the plant gondola) would have the Light Sensing Apparatus attached to him (What the lighter was lit over). Where-ever the Light Sensing Apparatus detects the most light, the gondola will return to that spot before re-starting its sweep. The code ideally will continuously perform sweeps every few minutes to place the plant (represented by Aragorn) where the most light is present. In this video, we set the code to perform an immediate sweep after it finds the position with the most light.

## License
MIT License

Copyright (c) 2020 Newton's Busties

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
