# Orange Pi 4A Kernel with WireGuard

Custom Linux kernel for Orange Pi 4A with enabled WireGuard support. Based on the default one with an upgraded Wireguard module.


## Features

- WireGuard enabled
- Tested on Orange Pi 4A
- Kernel: 5.15.147-sun55iw3
- Based: Debian


```bash
# zcat /proc/config.gz | grep WIREGUARD
CONFIG_WIREGUARD=m
# CONFIG_WIREGUARD_DEBUG is not set
```

## Installation

```bash
sudo dpkg -i linux-image-*.deb
sudo dpkg -i linux-dtb-*.deb
sudo reboot
modprobe wireguard
