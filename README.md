# Yocto sample layout

This is a demo setup for Yocto 

## Setup

On Ubuntu 22.04:

```
sudo apt-get install -y gawk wget git-core diffstat unzip gcc-multilib \
    build-essential chrpath socat zstd repo lz4
```

## Sources

```
mkdir ~/Projects/acme
cd ~/Projects/acme
repo init -u https://github.com:gonzoua/yocto-manifests.git
repo sync
```

## Build

```
cd ~/Projects/acme
export TEMPLATECONF=$(pwd)/src/meta-acme/conf
source src/poky/oe-init-build-env build
bitbake acme-image-r2d2
ls -la tmp-glibc/deploy/images/r2d2/
```
