For Project Documentation, view the following link: https://docs.google.com/document/d/1IHjDpGhEGYvSrTsLehtoSzCsxU5Pvv6ZDAVGaKjEqGU/edit#

Our Group name is Newton's Busties. We comprise of four members: Christopher, Harrison, David, and Elizabeth. This was our ENGR114 Project in Prof. Kazarinoff's class at PCC.


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


