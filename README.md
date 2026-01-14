# garage-platformio

This repository is for firmware and updates for [garage-car-positioning](https://github.com/jwilleke/garage-car-positioning) project.

## Hardware

[garage-platformio hardware](https://github.com/jwilleke/garage-car-positioning/blob/master/hardware/wiring-diagram.md) shows the hardware used and the diagram shows the wiring for a single ESP32-C6 controlling all car positioning and garage door components.

See [platformio.ini](./platformio.ini) for pin assgnements.

## J1 USB

| Pin | Name | Type | Function |
| ---- | ---- | ---- | ---- |
| 1 | 3V3 | P | 3.3 V power supply |
| 2 | RST | I | High: enables the chip; Low: disables the chip. |
| 3 | 4 | I/O/T | MTMS 3, GPIO4, LP_GPIO4, LP_UART_RXD, ADC1_CH4, FSPIHD |
| 4 | 5 | I/O/T | MTDI 3, GPIO5, LP_GPIO5, LP_UART_TXD, ADC1_CH5, FSPIWP |
| 5 | 6 | I/O/T | MTCK, GPIO6, LP_GPIO6, LP_I2C_SDA, ADC1_CH6, FSPICLK |
| 6 | 7 | I/O/T | MTDO, GPIO7, LP_GPIO7, LP_I2C_SCL, FSPID |
| 7 | 0 | I/O/T | GPIO0, XTAL_32K_P, LP_GPIO0, LP_UART_DTRN, ADC1_CH0 |
| 8 | 1 | I/O/T | GPIO1, XTAL_32K_N, LP_GPIO1, LP_UART_DSRN, ADC1_CH1 |
| 9 | 8 | I/O/T | GPIO8 2 3 |
| 10 | 10 | I/O/T | GPIO10 |
| 11 | 11 | I/O/T | GPIO11 |
| 12 | 2 | I/O/T | GPIO2, LP_GPIO2, LP_UART_RTSN, ADC1_CH2, FSPIQ |
| 13 | 3 | I/O/T | GPIO3, LP_GPIO3, LP_UART_CTSN, ADC1_CH3 |
| 14 | 5V | P | 5 V power supply |
| 15 | G | G | Ground |
| 16 | NC | – | No connection |

## J3 USB

## Pins from Top Down

| CONNECTION | LEFT | RIGHT | CONNECTOION |
| ---- | ---- | ---- | ---- |
| - | 3V3 | G | - |
| - | RST | TX | DLD2450_FRONT_RX |
| DOOR_CLOSED_SWITCH | 4 | RX | DLD2450_FRONT_TX |
| HALL_EFFECT_SENSRO_A | 5 | 15 | - |
| HALL_EFFECT_SENSRO_B | 6 | 23 | - |
| - | 7 | 22 | - |
| - | 0 | 21 | - |
| - | 1 | 20 | - |
| DLED_PIN | 8 | 19 | DLD2450_REAR_TX |
| - | 10 | 18 | -DLD2450_REAR_RX |
| - | 11 | 9 | - |
| - | 2 | G | - |
| - | 3 | 13 | - |
| - | G | 12 | RELAY_MODULE_IN |
| - | NC | NC | - |
