# EKG-Design
This EKG design contains 2 electrodes, 2 differential amplifiers and 3 low pass Butterworth filters. The output is the correct voltage to go straight into an arduino although the code for that has not been written. 
The block diagram is located in the same branch as a .png file.
The differential amplifier we used was the INA129-EP Precision Low Power Instrumentation Amplifiers, although a schematic is also given as a .png
For the first differential amplifier we used a resistor value of 15ohms, with a rail of -6V to 6V, so it could be attached to batteries. With a Ref value of 0V this gave us a gain of 1000.
