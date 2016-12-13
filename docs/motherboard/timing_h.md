---
layout: page
title: timing
description: MemSat API Reference
theme: green
---


### Dependencies:

* stdint.h
  * system.h
  
timing Timing module


This module provides some very basic functions to make timing easier. Several

other modules rely on the services provided by this module.


The module uses the HAL layer to provide the hardware specific functionality for the

timing module.  In this module, the hal\_timing.c file is included to allow the ISR

to access the time variable without externing the variable or making a function call.

This allows the ISR to be very efficient.




type for timer, change override this to uint16\_t for better efficiency on a 8 or 16

bit system.


Note: a define is used instead of a typedef so that the define can be overriden.


Max time that can be held with the tint\_t type.



Initialize the timing module


Call the HAL layer to initialize a timer to interrupt every 1ms.

Clears the timing count


Returns the current system time in milliseconds


* Returns: the current system time in milliseconds

TimeSince



Get the elapsed time


Calculate and return the time elapsed since a given time. Typically used

with TimeNow(). See the example usage.



uint32\_t t;

t = TimeNow();

while(TimeSince(t) < 5000){

//Insert code here

}


TimeNow


* Parameter: `t `- The time in milliseconds to calculate the elapsed time since

* Returns: - The time elapsed since the time given in milliseconds


Delay a specific number of milliseconds


DelayMs uses TimeNow() and TimeSince() to implement the delay


* Parameter: `delay specifies` the number of milliseconds to delay


Reset the system time



Reset system time (e.g. TimeNow() will return 0) and set appropriate

rollover times so TimeSince will work properly.


Timing discrepancies will occur if TimerRoll is called and not called

again for the next timer rollover. TimeSince() will result in a shorter time

than expected if the timer is allowed to naturally roll over after calling

TimerRoll. The difference will be MAX\_TIME - the time when TimerRoll was last

called. This could be fixed by adding a check for the timer rolling over naturally

and setting rollover\_time to TIME\_MAX in timing.c. Note: This is handled by the

task management system which typically will be the only user of Timing\_Roll()



*/
