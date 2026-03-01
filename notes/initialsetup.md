# Initial Setup

## Hardware
- G48S Alder Lake N100 mini‑PC (8GB DDR5, 256GB SSD)
- 32GB thumb drive
- ASUS AX3000 router

## Installation
- Created a bootable USB installer and successfully installed OPNsense using Balena Etcher.
- Completed the initial setup wizard and accessed the web GUI without any issues.
- Original install later became unusable after a long period of no use; successfully reinstalled OPNsense again using a new USB.

## Base Configuration
- Configured LAN and WAN interfaces.
- Verified connectivity and basic routing.
- Confirmed DHCP and interface behavior using default OPNsense settings.

## Access Point Integration
- Added an ASUS AX3000 WiFi 6 router to serve as the access point.
- Enabled bridge mode on the AP.
- Assigned a static IP within the LAN subnet.
- Verified that the AP appeared in OPNsense and passed traffic correctly.

## Current Working State
- OPNsense is installed and stable.
- LAN/WAN routing is functional.
- Access point is fully integrated.
- Devices can connect through the AP both wired and wirelessly.
