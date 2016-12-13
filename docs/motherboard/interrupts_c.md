---
layout: page
title: interrupts
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

* stdint.h        /* Includes uint16_t definition */
  

Includes uint16\_t definition */
* stdbool.h       /* Includes true/false definition */
  

Includes true/false definition */




Interrupt Vector Options                                                   */




*/


Refer to the C30 (MPLAB C Compiler for PIC24F MCUs and dsPIC33F DSCs) User */


Guide for an up to date list of the available interrupt options.           */


Alternately these names can be pulled from the device linker scripts.      */


*/


PIC24F Primary Interrupt Vector Names:                                     */


*/


\_INT0Interrupt      \_IC4Interrupt                                          */


\_IC1Interrupt       \_IC5Interrupt                                          */


\_OC1Interrupt       \_IC6Interrupt                                          */


\_T1Interrupt        \_OC5Interrupt                                          */


\_Interrupt4         \_OC6Interrupt                                          */


\_IC2Interrupt       \_OC7Interrupt                                          */


\_OC2Interrupt       \_OC8Interrupt                                          */


\_T2Interrupt        \_PMPInterrupt                                          */


\_T3Interrupt        \_SI2C2Interrupt                                        */


\_SPI1ErrInterrupt   \_MI2C2Interrupt                                        */


\_SPI1Interrupt      \_INT3Interrupt                                         */


\_U1RXInterrupt      \_INT4Interrupt                                         */


\_U1TXInterrupt      \_RTCCInterrupt                                         */


\_ADC1Interrupt      \_U1ErrInterrupt                                        */


\_SI2C1Interrupt     \_U2ErrInterrupt                                        */


\_MI2C1Interrupt     \_CRCInterrupt                                          */


\_CompInterrupt      \_LVDInterrupt                                          */


\_CNInterrupt        \_CTMUInterrupt                                         */


\_INT1Interrupt      \_U3ErrInterrupt                                        */


\_IC7Interrupt       \_U3RXInterrupt                                         */


\_IC8Interrupt       \_U3TXInterrupt                                         */


\_OC3Interrupt       \_SI2C3Interrupt                                        */


\_OC4Interrupt       \_MI2C3Interrupt                                        */


\_T4Interrupt        \_U4ErrInterrupt                                        */


\_T5Interrupt        \_U4RXInterrupt                                         */


\_INT2Interrupt      \_U4TXInterrupt                                         */


\_U2RXInterrupt      \_SPI3ErrInterrupt                                      */


\_U2TXInterrupt      \_SPI3Interrupt                                         */


\_SPI2ErrInterrupt   \_OC9Interrupt                                          */


\_SPI2Interrupt      \_IC9Interrupt                                          */


\_IC3Interrupt                                                              */


*/


PIC24H Primary Interrupt Vector Names:                                     */


*/


\_INT0Interrupt      \_SPI2Interrupt                                         */


\_IC1Interrupt       \_C1RxRdyInterrupt                                      */


\_OC1Interrupt       \_C1Interrupt                                           */


\_T1Interrupt        \_DMA3Interrupt                                         */


\_DMA0Interrupt      \_IC3Interrupt                                          */


\_IC2Interrupt       \_IC4Interrupt                                          */


\_OC2Interrupt       \_IC5Interrupt                                          */


\_T2Interrupt        \_IC6Interrupt                                          */


\_T3Interrupt        \_OC5Interrupt                                          */


\_SPI1ErrInterrupt   \_OC6Interrupt                                          */


\_SPI1Interrupt      \_OC7Interrupt                                          */


\_U1RXInterrupt      \_OC8Interrupt                                          */


\_U1TXInterrupt      \_DMA4Interrupt                                         */


\_ADC1Interrupt      \_T6Interrupt                                           */


\_DMA1Interrupt      \_T7Interrupt                                           */


\_SI2C1Interrupt     \_SI2C2Interrupt                                        */


\_MI2C1Interrupt     \_MI2C2Interrupt                                        */


\_CNInterrupt        \_T8Interrupt                                           */


\_INT1Interrupt      \_T9Interrupt                                           */


\_ADC2Interrupt      \_INT3Interrupt                                         */


\_IC7Interrupt       \_INT4Interrupt                                         */


\_IC8Interrupt       \_C2RxRdyInterrupt                                      */


\_DMA2Interrupt      \_C2Interrupt                                           */


\_OC3Interrupt       \_DCIErrInterrupt                                       */


\_OC4Interrupt       \_DCIInterrupt                                          */


\_T4Interrupt        \_U1ErrInterrupt                                        */


\_T5Interrupt        \_U2ErrInterrupt                                        */


\_INT2Interrupt      \_DMA6Interrupt                                         */


\_U2RXInterrupt      \_DMA7Interrupt                                         */


\_U2TXInterrupt      \_C1TxReqInterrupt                                      */


\_SPI2ErrInterrupt   \_C2TxReqInterrupt                                      */


*/


PIC24E Primary Interrupt Vector Names:                                     */


*/


\_\_INT0Interrupt     \_\_C1RxRdyInterrupt      \_\_U3TXInterrupt                */


\_\_IC1Interrupt      \_\_C1Interrupt           \_\_USB1Interrupt                */


\_\_OC1Interrupt      \_\_DMA3Interrupt         \_\_U4ErrInterrupt               */


\_\_T1Interrupt       \_\_IC3Interrupt          \_\_U4RXInterrupt                */


\_\_DMA0Interrupt     \_\_IC4Interrupt          \_\_U4TXInterrupt                */


\_\_IC2Interrupt      \_\_IC5Interrupt          \_\_SPI3ErrInterrupt             */


\_\_OC2Interrupt      \_\_IC6Interrupt          \_\_SPI3Interrupt                */


\_\_T2Interrupt       \_\_OC5Interrupt          \_\_OC9Interrupt                 */


\_\_T3Interrupt       \_\_OC6Interrupt          \_\_IC9Interrupt                 */


\_\_SPI1ErrInterrupt  \_\_OC7Interrupt          \_\_DMA8Interrupt                */


\_\_SPI1Interrupt     \_\_OC8Interrupt          \_\_DMA9Interrupt                */


\_\_U1RXInterrupt     \_\_PMPInterrupt          \_\_DMA10Interrupt               */


\_\_U1TXInterrupt     \_\_DMA4Interrupt         \_\_DMA11Interrupt               */


\_\_AD1Interrupt      \_\_T6Interrupt           \_\_SPI4ErrInterrupt             */


\_\_DMA1Interrupt     \_\_T7Interrupt           \_\_SPI4Interrupt                */


\_\_NVMInterrupt      \_\_SI2C2Interrupt        \_\_OC10Interrupt                */


\_\_SI2C1Interrupt    \_\_MI2C2Interrupt        \_\_IC10Interrupt                */


\_\_MI2C1Interrupt    \_\_T8Interrupt           \_\_OC11Interrupt                */


\_\_CM1Interrupt      \_\_T9Interrupt           \_\_IC11Interrupt                */


\_\_CNInterrupt       \_\_INT3Interrupt         \_\_OC12Interrupt                */


\_\_INT1Interrupt     \_\_INT4Interrupt         \_\_IC12Interrupt                */


\_\_AD2Interrupt      \_\_C2RxRdyInterrupt      \_\_DMA12Interrupt               */


\_\_IC7Interrupt      \_\_C2Interrupt           \_\_DMA13Interrupt               */


\_\_IC8Interrupt      \_\_DMA5Interrupt         \_\_DMA14Interrupt               */


\_\_DMA2Interrupt     \_\_RTCCInterrupt         \_\_OC13Interrupt                */


\_\_OC3Interrupt      \_\_U1ErrInterrupt        \_\_IC13Interrupt                */


\_\_OC4Interrupt      \_\_U2ErrInterrupt        \_\_OC14Interrupt                */


\_\_T4Interrupt       \_\_CRCInterrupt          \_\_IC14Interrupt                */


\_\_T5Interrupt       \_\_DMA6Interrupt         \_\_OC15Interrupt                */


\_\_INT2Interrupt     \_\_DMA7Interrupt         \_\_IC15Interrupt                */


\_\_U2RXInterrupt     \_\_C1TxReqInterrupt      \_\_OC16Interrupt                */


\_\_U2TXInterrupt     \_\_C2TxReqInterrupt      \_\_IC16Interrupt                */


\_\_SPI2ErrInterrupt  \_\_U3ErrInterrupt        \_\_ICDInterrupt                 */


\_\_SPI2Interrupt     \_\_U3RXInterrupt                                        */


*/


*/


For alternate interrupt vector naming, simply add 'Alt' between the prim.  */


interrupt vector name '\_' and the first character of the primary interrupt */


vector name.  There are no Alternate or 'Alt' vectors for the 24E family.  */


*/


For example, the vector name \_ADC2Interrupt becomes \_AltADC2Interrupt in   */


the alternate vector table.                                                */


*/


Example Syntax:                                                            */


*/


void \_\_attribute\_\_((interrupt,auto\_psv)) <Vector Name>(void)               */


{                                                                          */


<Clear Interrupt Flag>                                                 */


}                                                                          */


*/


For more comprehensive interrupt examples refer to the C30 (MPLAB C        */


Compiler for PIC24 MCUs and dsPIC DSCs) User Guide in the                  */


<compiler installation directory>/doc directory for the latest compiler    */


release.                                                                   */


*/




Interrupt Routines                                                         */




TODO Add interrupt routine code here. */
