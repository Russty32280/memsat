---
layout: page
title: hal_timing
description: MemSat API Reference
theme: green
---




hal\_timing.h



Created on: 6/29/2015

Author: Muhlbaier





hal\_timing (HAL) Timing module
timing



This module provides the hardware abstraction needed for the timing module



This module needs to do the following:

- Define hal\_Timing\_Init() as detailed below hal\_Timing\_Init()

- Call TimingISR() macro from within the timer ISR and clear the interrupt

flag if required





Initialize hardware timer peripheral





*/


HAL\_TIMING\_H\_ */
