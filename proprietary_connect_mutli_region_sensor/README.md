# Connect Multi-Region Sensor #
![Type badge](https://img.shields.io/badge/Type-Application%20Examples-green)
![Technology badge](https://img.shields.io/badge/Technology-Connect-green)
![License badge](https://img.shields.io/badge/License-Zlib-green)
![SDK badge](https://img.shields.io/badge/SDK-v2.7.0-green)
![GCC badge](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/SiliconLabs/application_examples_ci/master/proprietary_connect/proprietary_connect_mutli_region_sensor_gcc.json)

## Summary ##

This example project uses the channel based multiPHY capabilites of the Connect stack to create a sensor that is able to work across multiple regions.

## Gecko SDK version ##

v2.7

## Hardware Required ##

- One BRD4253A radio board
- One additional sub-GHz radio board that can run Connect examples
- Two BRD4001A WSTK boards

## Setup ##

Import the included .sls file to Studio then build and flash the project to the BRD4253A radio board. This project is based on the default Connect (SoC): Sensor example, but I've added two additional commands. These commands are "get-region" and "set-region", which can be used to see the current region of the device and change it to the other region. As is, the device is configured with 2 regions, with region 0 being the US and region 1 being the EU.

Create a new Connect (SoC): Sink example for the other radio board, and set the radio configuration to the "Connect 902 MHz 2GFSK 200kbps" profile. Generate, build, and flash the sink project onto the radio board. Open a terminal window to both devices, and form a network on the sink. If you set the sensor's region to EU using the command `set-region 1`, the sensor will be unable to join the sink's network. Use the command `set-region 0` to set the region back to the US. The sensor should now be able to join the sink's network.

## How It Works ##

The sensor is configured with two PHYs. Both phys are based on the "Connect 902 MHz 2GFSK 200kbps" PHY. Channels 0-20 are configured to have the base channel frequency as 902 MHz and channels 21-41 have a base channel frequency of 863 MHz. Within flex-callbacks.c I have defined a struct that will hold the channel number offset and name of the region. The example has an array that populated with the information for the two configured phys. Using the "set-region" command, the region can be set on the device. The project has been modified so that the region channel number offset of the current region will be applied whenever the channel is changed. The connect stack will recognize that the channel change requires a change in PHY and automatically apply the changes. For example, if the current region is EU, then changing the channel to 5 results in the internal channel number changing to 26, as the channel number offset for that region is 21. Please note that the "info" command has been modified to show the region and channel number within that region.

## .sls Projects Used ##

proprietary_connect_mutli_region_sensor_fg12.sls

## How to Port to Another Part ##

Open the .isc file in studio and go to the general tab. Once in the general tab, click the edit architecture button and select the options for the part you would like to use. Once you finish editing the architecture, then generate the project. Then replace the generated flex-callbacks.c file with the one from the src folder.
