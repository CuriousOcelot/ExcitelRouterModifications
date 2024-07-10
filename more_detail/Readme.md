# How I did it

## Overview

This guide outlines the steps I took to disable the broadcasting of the SSID "www.excitel.com" on my router due to security concerns. Initially, I attempted to follow instructions from various sources, including YouTube tutorials and community forums, but encountered challenges along the way.

## Steps Taken

1. **Initial Attempts:**
   - I searched online for methods to disable the SSID broadcast and found a YouTube tutorial ([link](https://www.youtube.com/watch?v=W2JMMc4Ifa0)).
   - Unfortunately, the recommended method involving accessing "http://192.168.1.1/cgi-bin/upgrade.asp" did not work as expected, as the option for "ROMFILE BACKUP" was missing for my router.

2. **Exploring Alternative Methods:**
   - Determined to find a solution, I decided to disassemble the router and discovered a UART interface, which allowed me to sniff the router's boot logs and gain shell access.

3. **Further Research:**
   - Instead of desoldering the flash and reading the firmware directly, I researched the router's logs and found a similar device on the OpenWrt forums ([link](https://forum.openwrt.org/t/adding-openwrt-support-for-ancatus-a6-wifi-6-ax1800-ax3/104649)).
   - I also found the bootloader password ("telecomadmin" with the password "nE7jA%5m"), although it did not directly solve my issue.

4. **Analyzing the Firmware:**
   - Through analysis of the firmware, I identified the presence of "upgrade.asp" and located the download link for the ROM file at "http://192.168.1.1/romfile.cfg".
   - After downloading, modifying, and re-uploading the ROM file, I successfully disabled the broadcast of the unwanted SSID "www.excitel.com".

## Conclusion

Through persistence and a methodical approach to troubleshooting, I was able to achieve my goal of disabling the SSID broadcast on my router. This README serves as documentation of the steps I took, which may help others facing similar challenges with the devices.
