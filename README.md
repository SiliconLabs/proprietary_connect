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

# Silicon Labs Connect #

Silicon Labs Connect functionality for the EFR32 is implemented on top of the RAIL library. Silicon Labs Connect supports many combinations of radio modulation, frequency and data rates. The stack includes MAC layer functionality such as scanning and joining, setting up a point-to-point, star, or extended-star networks, frequency hopping and LBT (Listen Before Talk) protocols required for regulatory compliance in each geographical region, and PHY configurations for each of these regions. The stack also supports other features such as mbedTLS security, sleepy end devices, channel-based multi-PHY, and firmware upgrades through the Gecko Bootloader. With all this functionality already implemented in the stack, developers can focus on their application development and not worry about the lower-level radio and network details.

## Examples ##

- Multi-Region Sensor
  - An example that demonstrates how to use Connect's channel-based multi-PHY capabilities to build a single application that is compatible across multiple regions.

## Documentation ##

Official documentation can be found at our [Developer Documentation](https://docs.silabs.com/connect-stack/latest/) page.

## Reporting Bugs/Issues and Posting Questions and Comments ##

To report bugs in the Application Examples projects, please create a new "Issue" in the "Issues" section of this repo. Please reference the board, project, and source files associated with the bug, and reference line numbers. If you are proposing a fix, also include information on the proposed fix. Since these examples are provided as-is, there is no guarantee that these examples will be updated to fix these issues.

Questions and comments related to these examples should be made by creating a new "Issue" in the "Issues" section of this repo.

## Disclaimer ##

The Gecko SDK suite supports development with Silicon Labs IoT SoC and module devices. Unless otherwise specified in the specific directory, all examples are considered to be EXPERIMENTAL QUALITY which implies that the code provided in the repos has not been formally tested and is provided as-is.  It is not suitable for production environments.  In addition, this code will not be maintained and there may be no bug maintenance planned for these resources. Silicon Labs may update projects from time to time.
