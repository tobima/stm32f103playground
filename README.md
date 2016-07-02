# stm32f103playground

## Development setup

In order to flash the STM32F103 Development Kit, only the following cabels must be connected:

On the ARM-JTAG of the 

| Pin | Connector | Description |
| --- | --- | --- |
| 1 | VCC | This is the traget board Vcc. It is used by the STLINK/V2
| 7 | TMS/SWDIO | The SWD Data signal
| 8 | GND | Be sure there is a common ground
| 9 | TCK/SWCLK | The SWD Clock Signal
| 15 | nSRST/RESET | System reset – probably optional 

[http://www.micromouseonline.com/2011/11/05/stlink-swd-for-stm32/ Source]

## PIN Background

## STM103 JTAG

 JTAG Signals

| Signal | Connects to... |
| --- | --- | 
| TMS (SWDIO) | Test Mode State pin — Use 100K Ohm pull-up resistor to VCC. |
| TDO (SWO) | Test Data Out pin. |
| RTCK | JTAG Return Test ClocK. (see Note below) |
| TDI |	Test Data In pin — Use 100K Ohm pull-up resistor to VCC. |
| TRST | Test ReSeT/ pin — Use 100K Ohm pull-up resistor to VCC. TRST is optional and not available on some devices. You may leave it unconnected. |
| TCLK (SWCLK) | Test CLocK pin — Use 100K Ohm pull-down resistor to GND. |
| VCC |	Positive Supply Voltage — Power supply for JTAG interface drivers. |
| GND |	Digital ground. |
| RESET | RSTIN/ pin — Connect this pin to the (active low) reset input of the target CPU. |

[http://www.keil.com/support/man/docs/ulinkpro/ulinkpro_hw_if_jtag20.htm Source]

## ST-Link V2

Debug connector CN2 (SWD)

| Pin | CN2 | Designation
| --- | --- | --- |
| 1 | VDD_TARGET | VDD from application |
| 2 | SWCLK | SWD clock |
| 3 | GND | Ground |
| 4 | SWDIO | SWD data input/output |
| 5 | NRST | RESET of target MCU |
| 6 | SWO | Reserved |

Found in chapter 4.2.2 of the STM32F4DISCOVERY hardware and layout document
