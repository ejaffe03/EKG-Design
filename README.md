# EKG-Design
This EKG design contains 2 electrodes, 2 differential amplifiers and 3 low pass Butterworth filters. The output is the correct voltage to go straight into an arduino although the code for that has not been written. 
Disclaimer: This is not designed to be a diagnostic tool and should not be used to diagnose soemone with a heart condition. If you are getting strange results or believe you have a heart condition go see a doctor for a more advanced and accurate EKG.
The block diagram is located in the same branch as a .png file.
The differential amplifier we used was the INA129-EP Precision Low Power Instrumentation Amplifiers, although a schematic is also given as a .png
For the first differential amplifier we used a resistor value of 15ohms, with a rail of -6V to 6V, so it could be attached to batteries. With a Ref value of 0V this gave us a gain of 1000.
We then went from the first differential amplifier into 3 identical Butterworth low pass filters, a diagram including the values of resistors and capacitors is given in the main branch, although the diagrams do NOT contain the -6V to 6V rails that all of them used. With a cut off of 10Hz this eliminated most of the noise. 
Then we went into the AC coupling to remove drift from much smaller frequency background noise (noise on the level of .5Hz), the diagram of this filter is also in the main branch and has outputs of Vin+ and Vin- that align with the inputs to the second differential amplifier.
For the second differential amplifier we used a resistor value of 610kohms, with a rail of -6V to 6V, and a ref value of 3V. This output gave us a clear signal between 0 to 5V, which is ideal for an analog input to an arduino.

Other Notes: Although we did not test multiple electrodes we found the electrodes we did use were highly impacted by level of contact with skin. They were also impacted by surrounding noise so be sure to try inital tests in low noise surroundings. The butterworth filter we used was 2nd order, although you may replace all 3 with one 6th order butterworth filter for similar results, although we found the multiple, simpler lower order low pass filters easier to adjust. 
For more information, check out the final presentation on this project at this link: https://docs.google.com/presentation/d/1ieznO6HPBW98dYtP-OkzMkAfX3Gt_auT-4N10zN17pA/edit?usp=sharing
