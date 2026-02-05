# MyPortfolio-MULTI-SWITCH-VLAN-NETWORK-WITH-DHCP-AND-STATIC-ROUTING--PROJECT-03
Project-03
# Multi-Switch VLAN Network with DHCP & Static IPs

This project demonstrates a multi-switch VLAN network using **Router-on-a-Stick** for inter-VLAN routing. It includes both **static IP** and **DHCP** addressing, reflecting real enterprise network practices.

## 🔹 Network Topology

- 2 × Cisco Switches (2960)
- 1 × Cisco Router (2911)
- 8 × PCs across 4 VLANs
- Router-on-a-Stick for inter-VLAN routing
- Trunk links between switches and router

### VLANs & IP Addressing

| VLAN ID | Department | Method  | Subnet              | Default Gateway   |
|---------|------------|--------|-------------------|-----------------|
| 10      | HR         | DHCP   | 192.168.20.96/28  | 192.168.20.97   |
| 20      | IT         | DHCP   | 192.168.20.32/27  | 192.168.20.33   |
| 30      | Finance    | Static | 192.168.20.0/27   | 192.168.20.1    |
| 40      | Sales      | DHCP   | 192.168.20.64/27  | 192.168.20.65   |

### DHCP Pools

- HR: 192.168.20.98 – 192.168.20.110
- IT: 192.168.20.34 – 192.168.20.62
- Sales: 192.168.20.66 – 192.168.20.94
- Finance: **No DHCP** (static IPs only)

### PC Assignment

| PC   | VLAN | IP Method |
|------|------|-----------|
| PC0  | 10   | DHCP      |
| PC1  | 20   | DHCP      |
| PC2  | 30   | Static    |
| PC3  | 40   | DHCP      |
| PC4  | 10   | DHCP      |
| PC5  | 20   | DHCP      |
| PC6  | 30   | Static    |
| PC7  | 40   | DHCP      |

### ✅ Key Features

- VLANs allow devices to communicate within the same department.
- DHCP automatically assigns IPs to HR, IT, and Sales PCs.
- Finance PCs have static IPs for stability and security.
- Inter-VLAN communication works via Router-on-a-Stick.
- Trunk ports allow VLAN traffic across switches.

### 🔧 Tools Used

- Cisco Packet Tracer
- Cisco 2960 Switch
- Cisco 2911 Router

### 📸 Screenshots (optional)

- VLAN creation
- Trunk configuration
- Router subinterfaces
- DHCP configuration
- Successful pings
