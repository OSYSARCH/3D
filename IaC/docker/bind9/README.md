<!--
SPDX-FileCopyrightText: Huawei Inc.

SPDX-License-Identifier: CC-BY-4.0
-->

# Hardware Lab as a Service Blueprint space

### DNS server

DNS server needs to run for lab to function properly. [dispatcher-config](https://git.ostc-eu.org/OSTC/infrastructure/lava/lava-config/-/tree/master/lava.ostc-eu.org/master-configs/lava-server/dispatcher-config/devices) contains controlling scripts that during testing phases and they heavily rely on ```localnet``` domain for lab environment.

[db.localnet](db.localnet) zone file defines lab services related entries and should be updated according to controlling scripts content and ip addresses of deployed services. In order to that, we propose to use static DHCP addresses of lab devices. The mac addresses of devices can be obtained from dhcp server leases file and changed to static entries in dhcp server configuration.