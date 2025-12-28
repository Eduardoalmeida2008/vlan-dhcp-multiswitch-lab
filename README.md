# vlan-dhcp-multiswitch-lab
Network lab implementing multiple VLANs with DHCP using one router and four access switches. Includes inter-VLAN routing, trunk links, and full documentation.

````
 VLAN and DHCP Multi-Switch Lab

Overview
This lab demonstrates the implementation of multiple VLANs with DHCP in a small enterprise network using one router and four access switches.
````
```
Topology
- 1 Router (Router-on-a-Stick)
- 4 Access Switches
- 5 VLANs (10, 20, 30, 40, 50)
- Multiple end devices per VLAN
```
````
Technologies Used
- VLAN segmentation
- 802.1Q trunking
- Inter-VLAN routing
- DHCP per VLAN
- Cisco IOS commands
````
```
 VLAN Design
| VLAN | Purpose | Subnet |
|-----|--------|--------|
| 10 | Users | 192.168.10.0/24 |
| 20 | Users | 192.168.20.0/24 |
| 30 | Users | 192.168.30.0/24 |
| 40 | Users | 192.168.40.0/24 |
| 50 | Users | 192.168.50.0/24 |

```
````
Validation
- VLANs verified with `show vlan brief`
- Trunks verified with `show interfaces trunk`
- Inter-VLAN routing verified via ping
- DHCP verified with `show ip dhcp pool`
- End devices receiving IP addresses automatically
````
````
 Status
✔️ Fully functional and tested
````
