## Assignment 1 -- Programming and Project Development
This assignment is worth 8% of your module result.

The deadline for submission is Thursday March 11, midnight.

Write a complete Keil MDK project comprising a main program and a subroutine.

The subroutine must be called “fact” and should calculate the factorial of the number passed to it in R0. The subroutine must be recursive. Zero marks will be awarded for a non-recursive solution.

The purpose of the main program is to demonstrate and test the subroutine.

Calculations  must be done in 64-bit unsigned arithmetic and the result must be returned in R0 & R1, with the most significant 32 bits in R0 and the least significant 32 bits in R1.

If any error occurs, the C bit of the CPSR must be set and a result of 0 returned in R0 & R1. If there are no errors, the C bit must be clear.

The main program should use the subroutine four times:

1. Calculate the factorial of 5.
2. Calculate the factorial of 14.
3. Calculate the factorial of 20.
4. Calculate the factorial of 30.

Each result should be stored, by the main program, as a 64-bit result in RAM, starting at 0x40000000. Do this by reserving four 8-byte spaces at the start of the read-write area.

Note that the ARM7 does not do 64-bit arithmetic — you’ll have to somehow make use of 32-bit calculations to do 64-bit arithmetic.

Do not use repeated addition to implement multiplication. Zero marks will be awarded for a solution that uses repeated addition.

Please create a plain text file called “qanda.txt” ( for Questions AND Answers) and include it in your project folder. In it, please answer the following questions very briefly (one or two sentences each, max):

1. What does “well behaved” mean in the context of subroutines?
2. Explain how/why your subroutine is “well behaved”.
3. How would you test that your subroutine is well behaved?
4. Why is using repeated addition to implement multiplication such a bad idea?
5. What would happen to the program if a very large number of recursive calls were made, i.e. if there was very "deep" recursion?

Marks will be awarded as follows:

1. Has a Keil project, including the quanda.txt file, been submitted? (2)
2. Does the project assemble with no errors or warnings? (2)
3. Is the progam well organised and structured? (3)
4. Are the correct answers produced and stored correctly? (8)
5. Are the follow-on questions answered correctly? (5)
6. Please submit the entire project folder as a zip archive (a "Compressed (zipped) folder" in Windows) to Blackboard by the deadline.

