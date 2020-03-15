For More Project Documentation (parts, prices, licenses, and hookup), view the following link: https://docs.google.com/document/d/1IHjDpGhEGYvSrTsLehtoSzCsxU5Pvv6ZDAVGaKjEqGU/edit#

Our Group name is Newton's Busties. We are comprised of four members: Christopher, Harrison, David, and Elizabeth. This was our ENGR114 Project in Prof. Kazarinoff's class at PCC. 

![0311201600d](https://user-images.githubusercontent.com/59817284/76693640-dd3ff200-6625-11ea-91cb-a7ed8ea43dd8.jpg)

# Follow-the-Light
Sets up an apparatus that keeps your plant in maximum sunlight by moving your plant via a gondola to the spot in your windowsill with the most sunlight. Also generates a graph with python code to show where the plant moved.


## In the *NewtonsBust.zip* file is the needed .ino arduino code files for running the stepper motor, and the multiple .py files for running the python code, generating the graphs, and controlling the arduino:

## Basic Design
This was the first sketch of our set up for our idea:
![bsaic_carl](https://user-images.githubusercontent.com/59817284/76691707-099a4500-660b-11ea-95ea-d6d4f9a05dc5.png)

## How it works:
1)  The light sensors attached to the gondola are photo-resisters. They read how much light is striking the gondola at the time, then send the data as a anologue value to the attached arduino.
2)  The arduino then sends the anologue value (how much light is striking the gondola) to the attached computer. While the arduino does this, the arduino also tells the motor controller to continue to move the gondolla across its path. This allows the arduino to have light readings from multiple places. The Arduino sends both light on gondola, and position of gondola for the system to the attached computer.
3)  The computer then records a light versus position graph. The computer finds the positional value for the highest amount of light, and then sends a command to the arduino.
4)  The arduino then tells the motor controller to move the gondola to the position where the most light was recorded.
5)  At a set amount of time later, the process repeats so that maximum sunlight for the plant in the gondola is ensured.

### Things to note: 
* The system reads position based on the amount of turns the stepper motor has done, so the system does not actually read where the gondola is. The code has to be modified so that the gondola has a certain max range of motion (length of the gondola wire). 
* The photoresisters send a lower anologue value for more light. This is because they add voltage resistance to the system, which decreases the anologue value when more light is present.


# This is a Fritzing Schematic of the Hardware Hookup. 
![_untitledimage](https://user-images.githubusercontent.com/59817284/76695519-bee5f080-663d-11ea-8ce2-75ae3b9318ef.png)
Notice above that the AC wall outlet power to DC power for the stepper motor is not included in the Fritzing design. Neither is the computer usb to micro-usb for the arduino included in the Fritzing build. We also used a RedBoard instead of an Arduino Uno. The only difference in set-up between the Arduino Uno and the Redboard is the usb type C used for the computer to arduino connection instead of a micro-usb.


## Building the Gondola Stand:
Materials:
* 1 48" 2X4 
* 4 18" 2X4
* Screws

![gondola](https://user-images.githubusercontent.com/62195067/76709708-23489480-66be-11ea-8cb3-5612e4e13648.jpg)

This was assembled to hold up the gondola as if it were hung over a window. The top bar of the stand would represent the top of the window if someone were to use this for their house plant. The pulleys were fastened to the two upper corners. These were designed in OnShape and printed along with the mounting pieces. The string was then pulled across and wrapped around the pulleys, holding up the gondola. The gondola was designed in Tinkercad to hold the pot and dangle from the string. 
