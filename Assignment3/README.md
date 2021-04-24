# Assignment 3 -- Interrupt Handling
This assignment is worth 10% of your module result.

The deadline for submission is Wednesday April 21, midnight.

Write a complete program for the Keil Development System that can run and be demonstrated in the Emulator.

The main program should "display" the elapsed time, in hours, minutes and seconds, since the program started running, on the 32 bits of GPIO 1 using Binary Code Decimal (BCD) format. As the time goes by, the "display" should update appropriately. It must be exact.


For example, say the time to display is "12:34:56". Each character occupies four bits (a "nybble") and  use "1111" as a spacer instead of of the ":". This means that the above time would appear as:

00010010111100110100111101010110

in the GPIO (that is: "1 2 1111 3 4 1111 5 6" or, in hexadecimal: 0x12F34F56).

The time should be absolutely exact -- that is, it should be as accurate as the hardware of the computer will allow.

The program should consist of a main program (and subroutines, if necessary) an an interrupt handler. Once initialised, your program should run in the user mode.

You interrupt handler should somehow make use of one of the timers in the LPC2138. It should be extremely simple and very fast. It should do the absolute minimum necessary at interrupt level. Everything else should run in the main program. In particular, the interrupt handler must not have anything to do with the displaying of the elapsed time on the GPIO -- that is the responsibility of the main program.

The main program will consist basically of two parts:

The "initialisation" part of the main program sets everything up for subsequent operation. So, it must set up any data necessary, configure the timer and the Vectored Interrupt Controller and finally enable interrupts.
Note: It is really important to ensure everything is absolutely ready before you enable interrupts, because as soon as interrupts are enabled, it is possible that an interrupt will immediately occur. If all your initialisation is incomplete, then it may cause the interrupt handler to misbehave.
The "application" part that actually implements the display. As you know, the system starts up in a privileged mode. When the initialisation part of your main program is finished, make the rest of the program run in the User Mode. (Obviously, the interrupt handler will run in Interrupt Mode.)

## Grading criteria

1. Project Submitted (2).
2. Program assembles without errors or warnings (2).
3. Program works (4).
4. Main program runs in User Mode (1).
5. Interrupt handler is simple (2).
6. Structure of program (2).
7. Good comments (2).
8. Review questions (5).

## Review Questions

Please answer each question very briefly, preferably in one sentence.

1. What is the difference between "system" mode and "supervisor" mode on the ARM 7?
2. When the term "preemptive" is used in respect of a thread or process scheduler, what does it mean? 
3. Based on what we have discussed in class, why it is inadvisable to use a general-purpose operating system in a situation where real-time operation must be guaranteed?
4. What basic hardware facilities are provided to enable system builders to enforce privilege outside the CPU ("off-chip")? 
5. Overall, which is more efficient: interrupt-driven I/O or polled I/O? In your answer, explain why and roughly estimate the difference in efficiency.

Marks will be awarded for a well structured program. You should consider the separate components of the program, and write individual subroutines for them.

## Marks will be awarded as follows:

1. Has a Keil project been submitted? (2)
2. Does the project assemble with no errors or warnings? (2)
3. Is the progam well organised and structured? (3)
4. Does the program behave correctly? (8)
5. Are the follow-on questions answered correctly? (5)

Please submit the entire project folder as a zip archive (a "Compressed (zipped) folder" in Windows) to Blackboard by the deadline.
