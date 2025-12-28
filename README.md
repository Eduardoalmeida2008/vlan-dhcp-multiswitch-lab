
# VLAN and DHCP Multi-Switch Lab

## 📌 Overview
This lab demonstrates the implementation of multiple VLANs with DHCP in a small enterprise network using **one router (Router-on-a-Stick)** and **four access switches**.  
The environment simulates a junior-level corporate network with proper segmentation, trunking, inter-VLAN routing, and centralized DHCP.

---

## 🖧 Network Topology
- 1 Router (Router-on-a-Stick)
- 4 Access Switches
- 5 VLANs (10, 20, 30, 40, 50)
- Multiple end devices per VLAN

---

## 🧰 Technologies Used
- VLAN segmentation
- IEEE 802.1Q trunking
- Inter-VLAN routing (Router-on-a-Stick)
- DHCP per VLAN
- Cisco IOS commands

---

## 🗂 VLAN Design

| VLAN | Purpose | Subnet |
|-----|--------|--------|
| 10 | Users | 192.168.10.0/24 |
| 20 | Users | 192.168.20.0/24 |
| 30 | Users | 192.168.30.0/24 |
| 40 | Users | 192.168.40.0/24 |
| 50 | Users | 192.168.50.0/24 |

Each VLAN has its own DHCP pool and default gateway configured on the router subinterfaces.

---

## ✅ Validation & Tests
- VLANs verified using `show vlan brief`
- Trunk links verified using `show interfaces trunk`
- Inter-VLAN routing validated via ICMP (ping)
- DHCP pools verified using `show ip dhcp pool`
- End devices successfully receiving IP addresses automatically

---

## 📌 Status
✔️ Fully functional  
✔️ Tested across all VLANs  
✔️ DHCP operational on all segments  

---

## 📸 Lab Evidence

### 1️⃣ Network Topology
![Topology](screenshots/01_topology.png)

---

### 2️⃣ VLAN Configuration (Switches)
![VLAN SW1](screenshots/02_vlan_brief_sw1.png)
![VLAN SW2](screenshots/03_vlan_brief_sw2.png)
![VLAN SW3](screenshots/04_vlan_brief_sw3.png)
![VLAN SW4](screenshots/05_vlan_brief_sw4.png)

---

### 3️⃣ Trunk Status
![Trunk Status](screenshots/06_trunk_status.png)

---

### 4️⃣ Router Configuration (Inter-VLAN Routing)
![Router Subinterfaces](screenshots/07_router_subinterfaces.png)

---

### 5️⃣ DHCP Configuration
![DHCP Pools](screenshots/08_dhcp_pool.png)

---

### 6️⃣ End Devices – IP Assignment per VLAN
![PC VLAN10](screenshots/09_pc_vlan10_ip.png)
![PC VLAN20](screenshots/10_pc_vlan20_ip.png)
![PC VLAN30](screenshots/11_pc_vlan30_ip.png)
![PC VLAN40](screenshots/12_pc_vlan40_ip.png)
![PC VLAN50](screenshots/13_pc_vlan50_ip.png)

---

### 7️⃣ Inter-VLAN Connectivity Tests
![Ping VLAN10](screenshots/14_ping_vlan10_to_others.png)
![Ping VLAN20](screenshots/15_ping_vlan20_to_others.png)
![Ping VLAN30](screenshots/16_ping_vlan30_to_others.png)
![Ping VLAN40](screenshots/17_ping_vlan40_to_others.png)
![Ping VLAN50](screenshots/18_ping_vlan50_to_others.png)
