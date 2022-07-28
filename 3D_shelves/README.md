<!--
SPDX-FileCopyrightText: Huawei Inc.

SPDX-License-Identifier: CC-BY-4.0
-->

# 3D prints and projects


This is our attempt to clean out the mess and cables matrix we have for different DUTs in WRC lab.

The projects are made created with open source [FreeCAD](https://www.freecadweb.org) tool.

The trays for DUTs are based on [Raspberry Pi rack](https://www.prusaprinters.org/prints/69176-1u-raspberry-pi-rack-with-moduler-trays/files)

List of Trays:

- SECO C61 + CS863 double DB9 connectors [board](SBCB68_tray.png) 
- SECO [B68](SBCB68_tray.png)
- [Arduino NANO 33 BLE ](Arduino_Nano_33_BLE_tray.png)
- [Nitrogen](3D_shelves/Nitrogen_tray.png)
- Raspberry PI4 + TTL-USB + Terminal block [RPI tray](3D_shelves/trpi4-1-rpi4-tray-all.png) (modified version of [Raspberry PI4](https://www.prusaprinters.org/prints/69176-1u-raspberry-pi-rack-with-moduler-trays/files))
- [3x Relay board ](3D_shelves/relay_tray-Relay_tray.png)
- [YKUSH USB kvm](3D_shelves/ykush_tray.png)
- [YKUSH3 USB kvm](3D_shelves/ykush3_tray.png)


# Special print and build notes

## Raspberry PI4 + TTL-USB + Terminal block

* The print requires block support enforcer in the area where TTL-USB interface is, as shown in [Tray in PrusaSlicer](trpi4-prusaslicer.png). Included [gcode for Prusa Mini](trpi4-1-rpi4-tray-all_0.2mm_PETG_MINI_7h22m.gcode) 
* Supports for TTL-USB interface pcb need to be [manually removed after print](remove_supports.png).
* The tray is suitted for RPi4, [PoE+ HAT](https://www.amazon.de/gp/product/B0928ZD7QQ), [slim SSD SATA disk](https://www.komputronik.pl/product/376298/kingston-ssd-a400-120gb.html), [SATA-USB interface](https://www.amazon.de/-/en/gp/product/B06XCV1W97), [ttl-usb interface](https://www.aliexpress.com/item/32786625237.html) and [wall mounted 6P terminal block connector](https://www.aliexpress.com/item/10000003892271.html)
* due to limitation of 1U rack space [replacing plastic covers with heat shrinked tubing and bending](bend_connectors.png) of terminal cables is needed and also [bending and removing plastic spacer of pins for TTL-USB interface is needed](bend_pins.png) to [fit in tray](rpi_assembly.png)

## Contributing

See the `CONTRIBUTING.md` file.

## License

The license of this repository is as follows:

* Documentation text is under `CC-BY-4.0` license
* 3D printed designs of shelves and trays under `CC-BY-NC-SA-4.0` license
* Scripts, tools, and so on, are under `Apache-2.0` license

See the `LICENSES` subdirectory for full license texts.
