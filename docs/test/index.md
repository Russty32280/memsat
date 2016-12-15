## Embedded Library Tests
Embedded Library Tests employ UART to verify functionality remotely.

These tests should be accompanied by `.c` files with a `main` function which runs. Follow the [UART](/docs/uart/) guide for how to run the Python tests.

`python {test name}.py {port #} {baud rate}`

### UART
* `uart_test.py` - Sends and receives incrementing characters and breaks if there is a misread
* `uart_echo.py` - Receives incrementing characters to verify UART works
* `uart_buffer.py` - Sends and receives large batches of characters to test errors in the UART buffer / reader

## Continuous Integration
For Memsat, we are using [MagnumCI](magnum-ci.com/) to automatically run tests or other actions whenever code is committed to a specific repository. It runs code in a blank Linux virtual machine. Bash commands can be run.