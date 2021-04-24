# Assignment 2 -- Polling
This assignment is worth 10% of your module result.

The deadline for submission is Monday April 5, midnight.

Write a complete program for the Keil Development System that can run and be demonstrated in the Emulator.

The program should allow you to do simulated input and output on the simulated GPIO Port 1.

The program should monitor inputs on Pins 24 to 27 and should provide a response on Pins 23 to 16 as follows:

Pins 23 -- 16 should be treated as a 8-bit number "D" whose value is initially 0. Pin 23 is the MSB, Pin 16 the LSB.

Pins 27 -- 24 should be treated as individual inputs, where a pin's value going from 1 to 0 is to be interpreted as a corresponding [imaginary] push-button being pressed and the transition from 0 to 1 is is to be interpreted as the release of the button. For example, if Button 23 is pressed and released, Pin 23's value will go from 1 to 0; then, when Button 23 is released, the value of Pin 23 will return from 0 to 1. You can click theses values in the emulator.

## The program should do the following:

1. Pressing Button 24 should add 1 to the value of D.
2. Pressing Button 25 should subtract 1 from the value of D.
3. Pressing Button 26 should shift the bits in D to the left by one bit position.
4. Pressing Button 27 should shift the bits in D to the right by one bit position.
5. Marks will be awarded for a well structured program. You should consider the separate components of the program, and write individual subroutines for them.

## Please create a plain text file called “qanda.txt” ( for Questions AND Answers) and include it in your project folder. In it, please answer the following questions very briefly (one or two sentences each, max):

1. What does the term "Memory Mapped" in "Memory Mapped I/O" mean?
2. What is the difference between a byte-sized memory-mapped interface register and a regular byte of RAM?
3. Why is polling considered to be inefficient?
4. How could you organise polling of two or more interfaces?
5. Why would polling be bad for a computer's energy consumption?


## Marks will be awarded as follows:

1. Has a Keil project been submitted? (2)
2. Does the project assemble with no errors or warnings? (2)
3. Is the progam well organised and structured? (3)
4. Does the program behave correctly? (8)
5. Are the follow-on questions answered correctly? (5)

Please submit the entire project folder as a zip archive (a "Compressed (zipped) folder" in Windows) to Blackboard by the deadline.

