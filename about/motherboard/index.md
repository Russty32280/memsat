---
layout: page
title: Motherboard
description: Information about Motherboard
theme: green
---

<img src='/assets/images/chip.svg' style='height:140px; margin-left:auto; margin-right:auto; display:block;' />

***"*** *Since the dawn of time, man has wished to ascend to the heavens. Today, we have achieved this dream beyond our wildest expectations. We have truly entered a new age of humanity.*

---

The motherboard is the heart of MemSat, using a Pic24 microcontroller and interfacing with the various subsystems through [our api](/docs/api/). It is powered in part by [Mulhbaier's Embedded Libary](https://gitlab.com/memsat/Embedded-Library) along with custom APIs and interfaces developed by students as part of the C&DH (Command and data handling) subsystem.

## Peripherals
There is currently a Hardware Abstraction Layer (HAL) on this board to use: 

* UART Tx
* SPI Tx/Rx
* Timers
* Real-Time Clock (RTC)
* Analog-Digital Converter (ADC)

More peripheral support is in development.

### Bootloader
A bootloader is in development, to re-program the PIC over-the-air as well as recover the program if there are any corruption issue with in flight.