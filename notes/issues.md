# Issues and Troubleshooting
This file documents real issues encountered during the OPNsense and ASUS AP setup, along with root‑cause analysis and resolutions. It serves as a reference for reproducibility and demonstrates systematic troubleshooting in a home network environment.


## Format
Each issue is documented with:
- **Issue** — what went wrong  
- **Symptoms** — what was observed  
- **Cause** — root cause or likely cause  
- **Resolution** — what fixed it  
- **Notes** — anything useful for future reference  

---


## OPNsense install becoming unusable after long inactivity
**Issue** — The original OPNsense installation became unstable after sitting unused.

**Symptoms** — Web GUI inaccessible, no DHCP leases, device unresponsive to pings.

**Cause** — Likely corrupted install or degraded USB media.

**Resolution** — Reinstalled OPNsense using a new USB drive created with Balena Etcher.

**Notes** — Fresh installation media resolved the issue immediately.

---

## ASUS AP not saving configuration changes
**Issue** — The ASUS AX3000 did not retain configuration changes during initial setup.

**Symptoms** — AP appeared to accept settings but rebooted into a partially configured state. Mode selection and network settings were not applied.

**Cause** — The AP was reset or power‑cycled before completing its full configuration write cycle, leaving it in an incomplete “almost AP mode” state.

**Resolution** — Performed a full factory reset, allowed the AP to complete its entire boot and initialization process, then re‑applied AP mode settings from a clean state.

**Notes** — Interrupting the AP during configuration can leave it in a half‑applied state that looks valid but does not function correctly.

---

## ASUS AP stuck in rescue mode loop
**Issue** — The ASUS AX3000 repeatedly entered rescue/firmware recovery mode during setup.

**Symptoms** — Blinking blue power light, emergency mini web server available, normal UI inaccessible.

**Cause** — The AP was being reset while still partially configured, causing it to boot into recovery repeatedly.

**Resolution** — Fully erased settings, waited for the AP to complete its boot cycle, then configured AP mode from a clean state.

**Notes** — The AP must complete its full boot before applying mode changes or resets.

---

## ASUS AP not appearing in OPNsense
**Issue** — The ASUS AX3000 access point was not showing up in OPNsense after initial setup.

**Symptoms** — AP missing from DHCP leases, devices had no internet, and the router UI occasionally entered rescue mode.

**Cause** — Incorrect mode selection and inconsistent resets during configuration.

**Resolution** — Performed a full factory reset, set AP mode explicitly, assigned a static IP, and rebooted both devices.

**Notes** — Rescue mode resets can leave the AP in a half-configured state.


