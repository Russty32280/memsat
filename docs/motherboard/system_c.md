---
layout: page
title: system
description: MemSat API Reference
theme: green
---





Files to Include                                                           */




Device header file */

### Dependencies:

* xc.h
  
### Dependencies:

* p24Exxxx.h
  
### Dependencies:

* p24Fxxxx.h
  
### Dependencies:

* p24Hxxxx.h
  
### Dependencies:

* stdint.h          /* For uint32_t definition */
  

For uint32\_t definition */
* stdbool.h         /* For true/false definition */
  

For true/false definition */

### Dependencies:

* system.h          /* variables/params used by system.c */
  

variables/params used by system.c */




System Level Functions                                                     */


*/


Custom oscillator configuration funtions, reset source evaluation          */


functions, and other non-peripheral microcontroller initialization         */


functions get placed in system.c                                           */


*/



Refer to the device Family Reference Manual Oscillator section for




TODO Add clock switching code if appropriate.  An example stub is below.   */


Disable Watch Dog Timer */


When clock switch occurs switch to Prim Osc (HS, XT, EC)with PLL */


Set OSCCONH for clock switch */


Start clock switching */


Wait for Clock switch to occur */


Wait for PLL to lock, if PLL is used */


while(OSCCONbits.LOCK != 1); */
