---
layout: page
title: Motherboard API
description: What is the motherboard?
theme: green
---

## About the Motherboard
Learn more about the [Motherboard](/motherboard/) and the C&DH subsystem.

## Interface Control Document (ICD)

This ICD serves as a series of interfaces that connect or interact with other subsystems.

### Power

From the battery management system, we have a high and low we need from the Pic 

2 5V regulators that have two logic outputs that are needed
2 3.3V regulators that have two logic outputs that are needed
1 logic monitoring on the rail
Prefreably Finch would enjoy one analog on the logic rail

4 digital / logic output
3 analog monitoring rails

Upon future expansion, with MOSFETS, only two extra logic rails would be used.

### Payload

On the FlatSat, there's a separate processor for the payload. It communicates with the motherboard over SPI. Payload is the SPI slave.

#### Motherboard Inputs

| Pin  | Type | Description |
| :--- | :--- | :---        |
| MEM_ADDR  | MEM_ADDR SPI  | Sends us flipped memory addresses. MB needs to concatenate date/time and store in Flash. |

#### MEM_ADDR OP Code
Send a 46-bit encoded signal depicting status:
`xxxxx yyyyyyyy,yyyyyyyy z aaaaaaaaaaaa bbbbbbbbbbbb`

* 5-bit chip identifier
* 16-bit memory address
* 1-bit Latch / Flipped
* 12-bit temperature sensor data
* 12-bit radiation sensor data

Technically, the decoding only needs to be done by the ground station. C&DH just needs to concatenate data to the ending.

Using the system's [real-time clock (see Section 19)](http://ww1.microchip.com/downloads/en/DeviceDoc/39905e.pdf), 40-bits of data are concatenated. (Month, day, hour, minutes, seconds). This is a total of 86 (88)-bits per SEU that are saved into Flash.

#### Sensor Data

* Temperature Sensor is 12 bits
* Radiation Sensor is 12 bits

Each datum will be appended at the end of the last and the data processor will have to handle parsing.

This data will be timestamped and logged. We will also be doing some data pre-processing with the P21451-1-1-4 standard as part of a secondary experiment.

#### Interfaces
C&DH will send a 2-bit request. `0b01`. Then it will read from Payload the number of data points to collect. Then C&DH will send a read request `0b10` and then read all of the data points `3 * data_size` amount of data. This data will be timestamped and logged.

#### Function Signatures

Implement
* `void Payload_ReceiveData(char[] data)`
    * `data` - 3-byte String of values from payload, is a `MEM_ADDR` OP code
    
### Comms
Currently there are no defined API interfaces with the Comms subsystem.

#### Beacon
We talk to the beacon over UART.

#### Comms Module
The comms module is the slave and present an SPI interface to the PIC. And from there, we don't know how to do control words. They may pull a pin high to indicate there is a message. The comms module has very low memory, so we'll continually read things into our memory but not deal with it immediately if there are higher priority functions.

### Ground Control
C&DH handles communications from a ground station and does a variety of things.