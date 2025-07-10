# GeoIP-Update-for-OPNsense

Update GeoIP data on OPNsense without using Maxmind's account.

## Linking Script

This repository includes a helper script: [`link.sh`](./link.sh). This script can be used to create symbolic links or assist with deployment steps. Check the script for details on its usage and adapt it as needed for your environment.

## Configuration

The configuration file for this tool is [`actions_updategeoip.conf`](./actions_updategeoip.conf). Edit this file to customize update behavior or integration with OPNsense.

## Source of GeoIP

https://github.com/herrbischoff/country-ip-blocks

Many thanks for providing GeoIP data.

## Usage

Run the following commands in FreeBSD or OPNsense

```shell
# make
# make install
```

will generate a binary application `updategeoip` to /usr/local/bin (root account required)

you may also just

```shell
# make
```

and copy `updategeoip` to any directory you want.

and run it

```shell
# updategeoip
```

it will update GeoIP data of OPNsense.

A better way is write a cron entry to update it automatically.
