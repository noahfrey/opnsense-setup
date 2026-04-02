## Network Diagram (Base Topology)

```mermaid
flowchart LR
    ONT[ISP ONT / Fiber Box]
    ISP_Router[ISP Router\n(Router Mode)]
    OPNsenseWAN[OPNsense Firewall\nWAN Interface]
    OPNsenseLAN[OPNsense Firewall\nLAN Interface]
    AP[ASUS AX3000\nAccess Point Mode]
    Wired[Wired LAN Devices]
    Wireless[Wireless Devices]

    ONT --> ISP_Router
    ISP_Router --> OPNsenseWAN
    OPNsenseWAN --> OPNsenseLAN
    OPNsenseLAN --> AP
    AP --> Wired
    AP --> Wireless
```
