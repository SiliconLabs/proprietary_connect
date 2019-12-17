<table border="0">
  <tr>
    <td align="left" valign="middle">
    <h1>EFR32 Connect Application Examples</h1>
  </td>
  <td align="left" valign="middle">
    <a href="https://www.silabs.com/wireless/proprietary">
      <img src="http://pages.silabs.com/rs/634-SLU-379/images/WGX-transparent.png"  title="Silicon Labs Gecko and Wireless Gecko MCUs" alt="EFM32 32-bit Microcontrollers" width="250"/>
    </a>
  </td>
  </tr>
</table>

## Silicon Labs Connect ##

Silicon Labs Connect functionality for the EFR32 is implemented on top of the RAIL library. Silicon Labs Connect supports many combinations of radio modulation, frequency and data rates. The stack includes MAC layer functionality such as scanning and joining, setting up a point-to-point, star, or extended-star networks, frequency hopping and LBT (Listen Before Talk) protocols required for regulatory compliance in each geographical region, and PHY configurations for each of these regions. The stack also supports other features such as mbedTLS security, sleepy end devices, channel-based multi-PHY, and firmware upgrades through the Gecko Bootloader. With all this functionality already implemented in the stack, developers can focus on their application development and not worry about the lower-level radio and network details. 

## Examples ##

- Multi-Region Sensor
  - An example that demonstrates how to use Connect's channel-based multi-PHY capabilities to build a single application that is compatible across multiple regions.