<!--
SPDX-FileCopyrightText: Huawei Inc.

SPDX-License-Identifier: CC-BY-4.0
-->

# QUICKSTART for Hardware Lab as a Service Blueprint space

## Prerequisites
Basic [infrastructure services](https://gitlab.eclipse.org/pastanki/HLaaS/-/blob/main/README.md#internal-infrastructure-services) should exist or be deployed in your lab.

This section describes setting lab for building and testing hardware lab environment for Oniroproject and utilizing Raspberry Pi4 as (D)evice (U)nder (T)est.

We encourage you to start building 19" rack based lab from the very beginining as this will reduce connections related issues. Depending on how much DUTs and additional hardware you are going to have, choose rack cabinet of appropriate height.

Other DUTs can be found in [hardware](hardware/) directory.

1. Acquire needed hardware as described in [RaspberryPi4 README](hardware/RaspberryPi4/README.md)
1. 3D print one [shelf](https://www.printables.com/model/69176-1u-raspberry-pi-rack-with-moduler-trays/files) and at least [Rack - Left Side.stl](https://media.printables.com/media/prints/69176/stls/755130_4ad3b9ff-03a3-49e8-bfba-66af717b4bf1/rack-left-side.stl#_ga=2.182943142.1252397465.1652961384-59019936.1652961384), [Rack - Middle.stl](https://media.printables.com/media/prints/69176/stls/755131_8a87622c-3bbc-4c19-b789-956ce662223e/rack-middle.stl#_ga=2.182943142.1252397465.1652961384-59019936.1652961384), [Rack - Right Side.stl](https://media.printables.com/media/prints/69176/stls/755136_0156aba9-224c-4a07-8bb3-e1416042c88e/rack-right-side.stl#_ga=2.182943142.1252397465.1652961384-59019936.1652961384). Yes, you need to convert stl files to gcode files appropriate for your printer. Yuo can use [Full_Rack_0.2mm_PETG_MK3S_14h29m.gcode](https://media.printables.com/media/prints/69176/gcodes/802169_97798cfb-cff9-4a2d-9555-cd4a65f4133a/full_rack_02mm_petg_mk3s_14h29m.gcode#_ga=2.143423541.1252397465.1652961384-59019936.1652961384) for Prusa MK3S.
1. 3D print RPi4 [tray](3D_shelves/trpi4-1-rpi4-tray-all.stl)
1. The trays empty spaces can be utilized later, for additional DUTs or accompanying hardware.
1. Install shelf, trays and hardware inside rack cabinet.  Connections diagrams are [here](dut_diagrams/KiCAD/Raspberry%20DUT/Raspberry%20DUT.pdf)
1. Make sure you have needed infrastructure services, as described at [IaC](./README.md#internal-infrastructure-services)
1. Next step - configure [lava worker](https://git.ostc-eu.org/OSTC/infrastructure/lava/lava-playbooks#deploy-docker-worker)

## Contributing

See the `CONTRIBUTING.md` file.

## License

The license of this repository is as follows:

* Documentation text is under `CC-BY-4.0` license
* 3D printed designs of shelves and trays under `CC-BY-NC-SA-4.0` license
* Scripts, tools, and so on, are under `Apache-2.0` license

See the `LICENSES` directory in project main directory for full license texts.
