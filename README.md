#GL.iNet and OPNsense Network

This diagram documents the physical and logical connection between a GL.iNet router, an OPNsense firewall, and downstream DHCP clients.

## Network flow

`Internet → GL.iNet router → OPNsense firewall → DHCP clients`

- The GL.iNet router uses `192.168.8.1` as its LAN gateway.
- OPNsense connects through its WAN interface at `192.168.8.2`.
- The OPNsense LAN interface uses `192.168.2.69`.
- OPNsense provides DHCP addresses from `192.168.2.70` through `192.168.2.80`.
- Three GL.iNet LAN interfaces are unused.
- Two additional OPNsense interfaces are disabled.

## Diagram

[Open the editable Draw.io diagram](https://github.com/Kin3o/Network-Diagram/blob/main/OPNsense%20GL-iNet%20Network%20Diagram.drawio.pdf)
