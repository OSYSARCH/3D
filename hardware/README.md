<!--
SPDX-FileCopyrightText: Huawei Inc.

SPDX-License-Identifier: CC-BY-4.0
-->

# Hardware Lab as a Service Blueprint
The aim of the project is to help Contributors get up to speed with setup similar to what OSTC Developers are using in their LAB.
The set of hardware is based on what has been tested and interfaced with WRC services. Any hardware with similar functionality can be used but we've found that it takes time and seasoning and refinement to make setups stable.

# Hardware inventory

We're adding new DUTs and new set of accessories, according to Oniroproject blueprints inventory.

Devices come in different sizes; different set of connectors; power supplies requirements, network interfaces, etc.
Unification of environment where they can be put becomes evident with the number of growing amount of DUTs, cabling mesh and collection of power supplies and accessiories.
We've been there. A large desk with meticulously arranged configuration is unmanagable and becomes pile
of wires very quickly and it's very easy for electrical shortcut to occur and makes environment not stable.

We want to make the setups reliable, compact and clean. Although at some point it becomes a matter of aestetics and cool gadgets, the most important is to have it reliable and manageable.

## List of hardware needed to build Oniroproject based laboratory
- DUT - Device Under Test
- PoE - Power Over Ethernet, 802.3af (PoE, 15.4W max), 802.3at (PoE+, 30W max), 802.3bt (PoE++, 60W max), 802.3bt (PoE++, 100W max)
- PDU - Power Distribution Unit - controlled AC line

## Base hardware

### Power supplies
prerequisities:
* appropriate parameters - voltage, max current, physical dimentions
* controllable via cli/web UI/code

The list of PSUs being used in Oniroproject
* [RPi4 power supply usb-c 3.1 A](https://botland.store/socket-power-supply/7819-power-supply-extreme-usb-31-typ-c-usb-5v31a-for-raspberry-pi-4b-5901445617400.html)
* [Power supply for RPi4 ](https://botland.store/raspberry-pi-4b-power-supply/14488-power-supply-for-raspberry-pi-4-usb-c-51v-3a-original-white-765756931243.html)


### PoE
- [PoE+ HAT](https://www.amazon.de/gp/product/B0928ZD7QQ)
- [PoE splitter for 12V](https://www.aliexpress.com/item/33018258800.html)
- [PoE splitter fpr 12V](https://www.aliexpress.com/item/4001038785964.html)
- [PoE splitter for 12V/19V/24V](https://planetechusa.com/product/poe-172s-single-port-10-100-1000mbps-ultra-poe-splitter-12v-19v-24v/)
- PoE switch/router (Huawei S5700, Cisco POE switches/routers, etc.)

### Power Distribution units
In our configuration we use mixed PDU/PoE/USB power control of devices, but we are aiming at having uniform solution.
The list of PDUs being used in Oniroproject
- [Intelinet PDU](https://www.komputronik.pl/product/592881/intellinet-listwa-zasilajaca-pdu-1u-zarzadzalna-po-ip-z-wyswietlaczem-do-szaf-rack-19-.html)
- [Rack PDU, Switched, 1U, 16A, 208/230V](https://www.apc.com/shop/us/en/products/Rack-PDU-Switched-1U-16A-208-230V-8-C13/P-AP7921B)

#### DUTs setups
* Raspberry Pi4
* SECO SBC B68
* SECO SBC C61
* Arduino nano 33BLE
* 96Boards BLE Nitrogen

### USB switches for switching SSD disks between devices
- [ATEN US3344I 4x4 USB 3.1, USB switch](https://www.amazon.pl/gp/product/B07N2ZXCHF)
- [Yepkit USB Switchable Hub](https://www.yepkit.com/products/ykush)
- [YKUSH 3 Yepkit USB 3.1 Switchable Hub](https://www.yepkit.com/product/300110/YKUSH3)

### USB hubs for connecting multiple devices
- [HUB USB Icy Box 13x USB-A 3.0 (IB-AC6113)](https://www.morele.net/hub-usb-icy-box-13x-usb-3-0-z-portem-ladujacym-usb-czarny-ib-ac6113-713603/)
- [PowerPad15S 15 ports | USB 2.0 | 2.1A (10W) | 480Mbps | Desktop | Charge & Sync | Control](https://www.cambrionix.com/products/powerpad15s-pp15s-industrial-usb-hub)

### RS232 (TTL) -> USB interfaces
- [Converter USB - TTL](https://www.amazon.pl/dp/B07WX2DSVB)

### RS485 interfaces
- [RS485 for Aten](https://elty.pl/pl/p/Konwerter-USB-na-RS232RS485TTL-z-izolacja./2468?utm_source=ceneo&utm_medium=referral)

### relay switches
- [RPi relay HAT](https://botland.store/raspberry-pi-gpio-extensions/6804-rpi-relay-board-3-relays-cap-for-raspberry-pi-5904422371753.html)
- [Devantech ETH008-B-8-Channel-16A-Relay-Board](https://www.rapidonline.com/Devantech-ETH008-B-8-Channel-16A-Relay-Board-Controlled-Via-Ethernet-60-5055)

## Contributing

See the `CONTRIBUTING.md` file.

## License

The license of this repository is as follows:

* Documentation text is under `CC-BY-4.0` license
* 3D printed designs of shelves and trays under `CC-BY-NC-SA-4.0` license
* Scripts, tools, and so on, are under `Apache-2.0` license

See the `LICENSES` subdirectory for full license texts.
