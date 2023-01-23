# USB2CAN

USB2CAN is a compact and low cost open source USB to CAN bus adaptor. 

Based on candleLight firmware and STM32F072 crystal-less MCU, usb2can provides linux native socketcan support.

USB2CAN是一款紧凑且低成本的开源USB到CAN总线转化器.

基于candleLight固件和STM32F072无外置晶振MCU, usb2can提供了Linux原生SocketCAN支持.

## Quick Start | 快速开始

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

1. 使用GERBER文件 `usb2can_pcb/gerber/` 打样PCB
2. SMT或使用 [ibom](usb2can_pcb/bom/ibom.html)手工焊接
3. 编译candleLight固件
4. 使用 `dfu-utils` 烧录固件
5. 测试
```bash
sudo ip link set can0 up type can bitrate 1000000
# CAN receive
candump can0
# CAN send
cansend can0 200#5A5A5A5A5A5A5A5A
```

## Toolchains | 工具链

* PCB Design: KiCad 6.0.9
* Complier: arm-none-eabi-gcc 12.2.0
* Firmware Programmer: dfu-utils 0.11

* PCB设计: KiCad 6.0.9
* 编译器: arm-none-eabi-gcc 12.2.0
* 固件烧录: dfu-utils 0.11

## License | 许可证

* The USB2CAN project is released under GPLv3 license.

* candleLight Firmware Sources is distributed under the MIT License (MIT) Copyright (c) 2016 Hubert Denkmair

* The STM32 HAL is distributed under a non-restrictive BSD (Berkeley Software Distribution) license.

* Code from the STM32 USB library is licensed under ST STMicroelectronics [Ultimate Liberty license SLA0044](www.st.com/SLA0044)

* USB2CAN项目基于GPLv3协议发布

* candleLight固件源码根据MIT分发, 版权所有2016 Hubert Denkmair

* STM32 HAL 在非限制性BSD许可下分发.

* STM32 USB 库中的代码根据 [Ultimate Liberty license SLA0044](www.st.com/SLA0044) 获得许可


## Related Projects | 相关项目

[candleLight_fw](https://github.com/candle-usb/candleLight_fw)