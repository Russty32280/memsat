# MemSat API
## Power
### Motherboard Inputs

| Pin  | Type | Description |
| :--- | :--- | :---        |
|      |      |             |
|      |      |             |

### Motherboard Outputs

| Pin  | Type | Description |
| :--- | :--- | :---        |
|      |      |             |
|      |      |             |

From the battery management system, we have a high and low we need from the Pic 

2 5V regulators that have two logic outputs that are needed
2 3.3V regulators that have two logic outputs that are needed
1 logic monitoring on the rail
Prefreably Finch would enjoy one analog on the logic rail

4 digital / logic output
3 analog monitoring rails

Upon future expansion, with MOSFETS, only two extra logic rails would be used.

### Function Signatures

* `void Power_`

## Payload

On the FlatSat, there's a separate processor for the payload. It communicates with the motherboard over SPI.

### Motherboard Inputs

| Pin  | Type | Description |
| :--- | :--- | :---        |
| MEM_ADDR  | MEM_ADDR SPI  | Sends us flipped memory addresses. MB needs to concatenate date/time and store in Flash. |


### MEM_ADDR OP Code
Send a 23-bit encoded signal depicting status:
`w xxxxx yyyyyyyy,yyyyyyyy z`

* 1-bit Dead / Alive chip identifier
* 5-bit chip identifier
* 16-bit memory address
* 1-bit Latch / Flipped

Technically, the decoding only needs to be done by the ground station. The MB just needs to concatenate data to the ending.

Using the system's [real-time clock (see Section 19)](http://ww1.microchip.com/downloads/en/DeviceDoc/39905e.pdf), 40-bits of data are concatenated. (Month, day, hour, minutes, seconds). This is a total of 63-bits per SEU that are saved into Flash.

### Function Signatures

Implement
* `void Payload_ReceiveData(char[] data)`
    * `data` - 3-byte String of values from payload, is a `MEM_ADDR` OP code
    
## Comms
### Motherboard Inputs

| Pin  | Type | Description |
| :--- | :--- | :---        |
|      |      |             |
|      |      |             |

### Motherboard Outputs

| Pin  | Type | Description |
| :--- | :--- | :---        |
|      |      |             |
|      |      |             |

### Function Signatures
