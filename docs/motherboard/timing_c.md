---
layout: page
title: timing
description: MemSat API Reference
theme: green
---


### Dependencies:

* timing.h
  * hal_general.h
  

HAL Function Declarations



Including the hal\_timing.c file here allows the ISR defined in that module

to have access to the time variable without extern-ing it.  It allows the ISR


to not have to make a function call. */

### Dependencies:

* hal_timing.c
  
1000 + TimingUsNow();

1000 + TimingUsNow();
