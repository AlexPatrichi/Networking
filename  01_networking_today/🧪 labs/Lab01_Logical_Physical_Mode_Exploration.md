# Lab 01: Packet Tracer - Logical and Physical Mode Exploration

**Cisco Networking Academy | Solent University**

Course: CCNA: Introduction to Networks
Platform: Cisco Packet Tracer    
Focus Area: Network Topology, Device Connectivity & Basic Router Configuration

## 🎯 Objective 

- Explore the Logical and Physical workspaces in Cisco Packet Tracer.
- Identify networking devices and connections. 
- Practise basic network installation and configuration tasks within a simulated business environment. 

## 🧠 Core Concepts Learned

- Logical Mode: Displays network devices and their connections in a logical topology.
- Physical Mode: Represents the physical location of networking equipment, including buildings, wiring closets, racks, and cables.
- Network Devices: Routers connect different networks, while switches connect devices within a local network.
- Network Cabling: Different cables serve different purposes, including network connectivity and device management.
- Console Access: Allows administrators to access and configure network devices through a direct management connection.
- Cisco IOS: Provides a command-line interface for configuring and managing Cisco networking devices.

## 🧪 Lab Implementation

### Part 1: Investigate the Bottom Toolbar

Investigated the bottom toolbar and identified the available categories of networking devices, end devices, components, and connections.

![Investigate the Bottom Toolbar](../📷%20images/Lab01-Bottom-Toolbar.png)

**Question:** What are the subcategories for Network Devices?  
**Answer:**
- Routers
- Switches
- Hubs
- Wireles Devices
- Security
- WAN Emulation

---

### Part 2: Investigate Devices in a Wiring Closet

Navigated through the Physical Workspace to examine the branch office wiring closet.

Identified networking equipment, including routers, switches, a wireless access point, equipment racks, and network cabling.

Compared the representation of devices and connections in Logical and Physical modes.

**Question:** What devices use a wired connection to connect to switch ALS2?  
**Answer:** Switch ALS1 and the Packet Tracer access point.

![Investigate Devices in a Wiring Closet Physical](../📷%20images/Lab01-Physical.png)

**Question:** Which device is connected to Access_Point?  
**Answer:** Laptop_01

![Investigate Devices in a Wiring Closet Logical](../📷%20images/Lab01-Logical.png)

**Question:** Where is the device connected to Access_Point physically located?  
**Answer:** On the table

---

### Part 3: Connect End Devices to Networking Devices

Practised connecting devices using different network cables.
- Connected a PC to a switch using a copper straight-through cable.
- Connected a PC to a router using a console cable.
- Identified the difference between network connectivity and management connectivity.

![Connect End Devices to Networking Devices](../📷%20images/Lab01-Physical.png)

---

### Part 4: Install a Backup Router

Installed a backup router in the equipment rack, powered it on, and established a USB console connection between the router and a laptop.

![Install a Backup Router](../📷%20images/Lab01-Backup-Router.png)

---

### Part 5: Configure a Router Hostname

Accessed the backup router through the laptop's terminal and used Cisco IOS commands to configure its hostname.

```text
Router> enable
Router# configure terminal
Router(config)# hostname Edge_Router_Backup
Edge_Router_Backup(config)# end
```

The command changed the router's hostname to `Edge_Router_Backup`.

![Configure a Router Hostname](../📷%20images/Lab01-Configure-Hostname.png)

![Backup Router Configuration](../📷%20images/Lab01-Backup-Router-Config.png)

---

### Part 6: Explore the Rest of the Network 

Explored additional areas of the simulated network to become familiar with different network environments and their physical and logical representations.

![Warrenton Data Center](../📷%20images/Lab01-Warrenton-Data-Center.png)

![Teleworker Home](../📷%20images/Lab01-Teleworker-Home.png)

## 🧰 Tools Used
- Cisco Packet Tracer
- Cisco IOS Command-Line Interface (CLI)
- Virtual routers, switches, PCs, and laptops

## 🔐 Security Relevance
Understanding network infrastructure and device management is essential for network security.

Console connections provide a method of accessing network devices for administration, while familiarity with network topologies helps identify critical infrastructure and understand how devices communicate.

## 📌 Lessons Learned
This exercise helped me understand the differences between Logical and Physical modes in Cisco Packet Tracer, as well as how networking devices are connected in business and home environments.

I also gained introductory experience with Cisco IOS commands and learned how to access a router through a console connection to configure its hostname.

 