# ESPHome YAML
This repository contains various YAML files for EspHome I use.

- **[dds666.yaml](https://github.com/gianfrdp/esphome_yaml/blob/main/dds666.yaml)**: ModBus smart meter CHINT DDSU666
- **[sdm220.yaml](https://github.com/gianfrdp/esphome_yaml/blob/main/sdm220.yaml)**: ModBus smartmeter Eastron SDM220
- **[voltronic-7200.yaml](https://github.com/gianfrdp/esphome_yaml/blob/main/voltronic-7200.yaml)**: Voltronic Axpert Max 7200 Hybrid inverter using my fork and customizations [gianfrdp/esphome-pipsolar#pip8048](https://github.com/gianfrdp/esphome-pipsolar#pip8048) of [syssi/esphome-pipsolar#pip8048](https://github.com/syssi/esphome-pipsolar#pip8048)
- **[jk-bms.yaml](https://github.com/gianfrdp/esphome_yaml/blob/main/jk-bms.yaml)**: JK BMS JK_02A20S20P ver 11 using Bluetotth BLE from [syssi/esphome-jk-bms](https://github.com/syssi/esphome-jk-bms)
- **[jk-bms-soltaro.yaml](https://github.com/gianfrdp/esphome_yaml/blob/main/jk-bms-soltaro.yaml)**: Connection for JK BMS and Voltronic inverter using SOLTARO CAN protocol starting from [syssi/esphome-jk-bms](https://github.com/syssi/esphome-jk-bms). Following schema was used:

```
                Bluetooth                       UART-TTL                      CAN
┌────────────┐              ┌──────────────┐                ┌───────────┐            ┌-───────────┐
│            │              │              │<-----3.3V----->│   CAN     │            │ Voltronic  │
│    JK      │              │       GPIO 18│<----- RX ----->│Transceiver│            │ Axpert Max │
│    BMS     │ <--------->  │       GPIO 19│<----- TX ----->│       CanH│<---------->│6    BMS    │
│            │              │              │<-----GND -┬--->│       CanL│<---------->│7    port   │
│            │              │              │           |    │           │     ┌----->│8           │
│            │              │   ESP32      │           |    │SN65HVD230 │     |      │            │
└────────────┘              └──────────────┘           |    └───────────┘     |      └────────────┘
                                                       └----------------------┘
```
[ALiExpress SN65HVD230](https://www.aliexpress.com/item/1005002843997801.html?spm=a2g0o.order_list.order_list_main.16.14021802kmFoou)
