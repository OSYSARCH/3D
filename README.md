<!--
SPDX-FileCopyrightText: Huawei Inc.

SPDX-License-Identifier: CC-BY-4.0
-->

# Hardware Lab as a Service Blueprint space

## Overview

This is **Hardware Lab as a Service Blueprint** space for building Oniroproject test bench. The lab consists of several parts:

* DUTs [setups](hardware) along with alternative setups
* Linaro Automation and Validation Architecture [LAVA](https://lava.ostc-eu.org/static/docs/v2/index.html) configurations
* Wiring and connections diagrams
* Lab accompanying infrastructure services
* Integration with gitlab and CI/CD pipelines
* [Monitoring](Observability) of state of the lab
* Rack space organisation [example](3D_shelves/DUT_rack.png)

## Devices Under Tests (DUTs)
Information about tested hardware along with wiring diagrams can be found in [hardware directory](hardware)

Supported DUTs
* [Raspberry Pi4](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/)
* [Arduino Nano 33BLE](https://docs.arduino.cc/hardware/nano-33-ble)
* [SECO SBC B68 ALVIN](https://edge.seco.com/en_eu/alvin.html)
* [SECO SBC C61 ASTRID](https://edge.seco.com/en_eu/astrid.html)
* [Nitrogen by 96boards](https://www.96boards.org/product/nitrogen/)

### Connections diagrams
Infrastructure related diagrams are located in [network directory](network)

## Integration with external services
### Internal infrastructure services
A minimal set of infrastructure services is needed for environment to function. Those are:
* [DHCP server](IaC/docker/isc-dhcp-server)
* [DNS server](IaC/docker/bind9)
* [NTP server](IaC/docker/chrony)
* [lava worker](https://git.ostc-eu.org/OSTC/infrastructure/lava/lava-playbooks)

* [KISS cache](IaC/docker/KissCache)
* [lava artifacts cache](IaC/docker/artifacts-cache)

We recommend putting http/https services behing traefik
* [traefik load balancer](IaC/docker/traefik)

Additional external dependencies
* [Lava server](https://docs.lavasoftware.org/lava/pipeline-server.html)
* [SQUAD - Software Quality Dashboard](https://github.com/Linaro/squad)
* [hawkbit with s3](https://github.com/eclipse/hawkbit)
* [gitlab-runner environment](https://docs.gitlab.com/runner/)


Directory [IaC](IaC) is where code for setting up the services is located.

## Rack space organisation
### Shelves and trays
Directory [3D_shelves](3D_shelves) contains rack shelves and trays 3D designs for DUTs and additional controlling hardware

## Howto start

[QUICKSTART](QUICKSTART.md) file contains instructions on howto start quickly with Oniro on Raspberry Pi 4 DUT

---
## Contributing

See the `CONTRIBUTING.md` file.

## License

The license of this repository is as follows:

* Documentation text is under `CC-BY-4.0` license
* 3D printed designs of shelves and trays under `CC-BY-NC-SA-4.0` license
* Scripts, tools, and so on, are under `Apache-2.0` license

See the `LICENSES` subdirectory for full license texts.
