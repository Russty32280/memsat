---
layout: page
title: Automated Tests
description: What is the motherboard?
theme: green
---

## Embedded Library Tests
Embedded Library Tests employ UART to verify functionality remotely.

These tests should be accompanied by `.c` files with a `main` function which runs. Follow the [UART](/docs/uart/) guide for how to run the Python tests.

`python {test name}.py {port #} {baud rate}`

### UART Unit Tests
* `test_beacon_setup.py` - Mocks the beacon and makes appropriate responses from PIC
* `test_encryption.py` - Tests encryption and decryption on the PIC 
* `test_ota_update.py` - Tests a variety of OTA functions and potential behaviors
* `test_uart.py` - Sends and receives incrementing characters and breaks if there is a misread
* `test_uart_echo.py` - Receives incrementing characters to verify UART works

### UART Timing Tests
Using the same structure as above, we can also measure the length of time for particular functions for a better idea of how the microcontroller will behave in space.

* `timing_encryption.py` - Encrypts and decrypts data 10 times and reports the length of time for each

## Continuous Integration
For Memsat, we are using [MagnumCI](magnum-ci.com/) to automatically run tests or other actions whenever code is committed to a specific repository. It runs code in a blank Linux virtual machine. Bash commands can be run.