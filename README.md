# GL.iNet and OPNsense Network

This diagram documents the physical and logical connection between a GL.iNet router, an OPNsense firewall, and downstream DHCP clients.

## Network flow

`Internet → GL.iNet router → OPNsense router/firewall → DHCP clients`

1. **Internet to GL.iNet router**  
   The internet connection enters through the GL.iNet router’s WAN interface.

2. **GL.iNet upstream network**  
   The GL.iNet router provides the `192.168.8.0/24` upstream network and uses `192.168.8.1` as its LAN gateway.

3. **GL.iNet to OPNsense**  
   An Ethernet cable connects GL.iNet LAN 1 to the OPNsense WAN interface. OPNsense receives the reserved address `192.168.8.2`.

4. **OPNsense to DHCP clients**  
   The OPNsense LAN interface uses `192.168.2.69` and provides DHCP addresses from `192.168.2.70` through `192.168.2.80` to connected clients.
### Noteable things
- Three GL.iNet LAN interfaces are unused.
- Two additional OPNsense interfaces are disabled.
- The OPNsense clients use double NAT to route packets

## Diagram

[Open the editable Draw.io diagram](https://github.com/Kin3o/Network-Diagram/blob/main/OPNsense%20GL-iNet%20Network%20Diagram.drawio.pdf)
