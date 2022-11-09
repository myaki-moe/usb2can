# USB2CAN

USB2CAN is a compact and low cost open source USB to CAN bus adaptor. 

Based on candleLight firmware and STM32F072 crystal-less MCU, can2usb provides linux native socketcan support.

## Quick Start

1. PCB proofing using GERBER file `usb2can_pcb/gerber/`
2. SMD or hand soldering using [ibom](usb2can_pcb/bom/ibom.html)
3. Build candleLight firmware
4. Flash the firmware using `dfu-utils`
5. Testing
```bash
sudo ip link set can0 up type can bitrate 1000000
# CAN receive
candump can0
# CAN send
cansend can0 200#5A5A5A5A5A5A5A5A
```

## Toolchains

* PCB Design: KiCad 6.0.9
* Complier: arm-none-eabi-gcc 12.2.0
* Firmware Programmer: dfu-utils 0.11

## License

* The USB2CAN project is released under GPLv3 license.

* candleLight Firmware Sources is distributed under the MIT License (MIT) Copyright (c) 2016 Hubert Denkmair

* The STM32 HAL is distributed under a non-restrictive BSD (Berkeley Software Distribution) license.

* Code from the STM32 USB library is licensed under ST STMicroelectronics [Ultimate Liberty license SLA0044](www.st.com/SLA0044)

## Related Projects

[candleLight_fw](https://github.com/candle-usb/candleLight_fw)