# WiFi Jiggle

Much like a VCR that needs a smacking or a toilette handle which needs to be jiggled, the WiFi card in your laptop also needs a hand every now and then. This repo will provide an executable named `wifi-jiggle` which can help convince a stuck card to scan for networks again.

Linux only.

## Installation

* First you need to install some `iw*` library (TODO: name)

```sh
gcc list-wireless-networks.c -o list-wireless-networks
cp list-wireless-networks /usr/sbin
cp wifi-jiggle /usr/bin
```

## Running

Once you're ready you can run the command

```sh
wifi-jiggle
```

It will prompt for your password (uses `sudo`). It'll list some networks (maybe none, maybe old cached ones), then brings the interface down and back up, then list them again (hopefully all networks).

## Configuring

Modify the `wifi-jiggle` bash script if you need to change the interface name from `wlan0`.
