# Lab 04: Packet Tracer - Implement Basic Connectivity

**Cisco Networking Academy | Solent University**

Course: CCNA: Introduction to Networks
Platform: Cisco Packet Tracer    
Focus Area: IPv4 Addressing, Switch Management Interfaces, Network Connectivity & Verification 

## 🎯 Objective 

- Apply basic configurations to two Cisco switches.
- Configure IPv4 addresses on PCs and switch management interfaces.
- Verify interface configurations using Cisco IOS commands.
- Test network connectivity using 'ping'.

## 🧪 Lab Implementation

### Part 1: Perform a Basic Configuration on S1 and S2

Configured both switches with hostnames, console authentication, Privileged EXEC passwords, and MOTD security banners.

```text
=== Step 1: Configure S1 and S2 with a hostname: ===
Switch> enable
Switch# configure terminal
Switch(config)# hostname S1

=== Step 2: Configure the console: ===
S1(config)# line console 0
S1(config-line)# password cisco
S1(config-line)# login
S1(config-line)# exit

=== Step 3: Encrypt privileged EXEC mode passwords: ===
S1(config)# enable secret class

=== Step 4: Use an appropriate banner text to warn unauthorized access: ===
S1(config)# banner motd "Authorized access only. Violators will be prosecuted to the full extent of the law."
S1(config)# end

=== Step 5: Save the configuration file to NVRAM: ===
S1# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
```

> Repeated the same configuration on S2.

### Part 2: Configure the PCs

Configured static IPv4 addresses on PC1 and PC2 using the IP Configuration tool in Cisco Packet Tracer.

**1. Configure IPv4 Addressing**

Opened **Desktop → IP Configuration** on each PC and entered the following settings:

| Device | Interface | IPv4 Address | Subnet Mask |
|---|---|---|---|
| PC1 | NIC | `192.168.1.1` | `255.255.255.0` |
| PC2 | NIC | `192.168.1.2` | `255.255.255.0` |

Both PCs belong to the same network, `192.168.1.0/24`, allowing them to communicate directly without a router.

**2. Test Initial Connectivity**

Opened **Desktop → Command Prompt** on PC1 and attempted to ping the management IP address assigned to S1 in the addressing table.

```text
PC> ping 192.168.1.253
```

**Expected Result:** The ping fails because S1's VLAN 1 management interface has not yet been configured with its IP address.

### Part 3: Configure the Switch Management Interface

Configured VLAN 1 management interfaces on S1 and S2 to allow IP communication with the switches.

**1. Configure the VLAN 1 Management Interface on S1 and S2**

```text
=== Switch S1 ===
S1# configure terminal
S1(config)# interface vlan 1
S1(config-if)# ip address 192.168.1.253 255.255.255.0
S1(config-if)# no shutdown
S1(config-if)# end

=== Switch S2 ===
S2# configure terminal
S2(config)# interface vlan 1
S2(config-if)# ip address 192.168.1.254 255.255.255.0
S2(config-if)# no shutdown
S2(config-if)# end
```

- `interface vlan 1` — Enters configuration mode for the VLAN 1 Switch Virtual Interface (SVI).
- `ip address 192.168.1.253 255.255.255.0` — Assigns an IPv4 address and subnet mask to the management interface.
- `no shutdown` — Administratively enables the interface.

> NOTE: Both switches now have management IP addresses in the `192.168.1.0/24` network.

> **Note:** A Layer 2 switch forwards Ethernet frames using MAC addresses and does not need an IP address for basic switching. The management SVI allows administrators to communicate with the switch over IP.

**2. Verify the Management Interface Configuration**

Used Cisco IOS commands to check the configured IP addresses and interface status.

```text
S1# show ip interface brief
S1# show running-config
```

- `show ip interface brief` — Displays the IP addresses and operational status of the switch interfaces.
- `show running-config` — Displays the active configuration, including the VLAN 1 IP address.

**3. Save the Switch Configurations**

Saved the updated configurations on both switches to NVRAM.

```text
S1# copy running-config startup-config
S2# copy running-config startup-config
```

**4. Verify Network Connectivity**

Opened **Desktop → Command Prompt** on PC1 and tested connectivity to PC2 and both switches.

```text
PC> ping 192.168.1.2
PC> ping 192.168.1.253
PC> ping 192.168.1.254
```

| Destination | IP Address | Expected Result |
|---|---|---|
| PC2 | `192.168.1.2` | Successful |
| S1 | `192.168.1.253` | Successful |
| S2 | `192.168.1.254` | Successful |

> **Note:** The first ping may lose a packet while ARP (Address Resolution Protocol) discovers the destination MAC address. Repeating the ping should succeed if the network is configured correctly.

## 🧰 Tools Used

- Cisco Packet Tracer
- Cisco IOS Command-Line Interface (CLI)
- Cisco 2960 Switches (S1 and S2)
- PCs (PC1 and PC2)
- Ethernet Connections
- Packet Tracer IP Configuration Tool
- Packet Tracer Command Prompt

## 📌 Lessons Learned

- Applied basic switch configurations to two Cisco switches.
- Configured static IPv4 addresses on PCs.
- Learned how to configure VLAN 1 Switch Virtual Interfaces (SVIs) for switch management.
- Understood why Layer 2 switches do not require IP addresses for basic frame forwarding.
- Verified switch IP addresses and interface status using `show ip interface brief`.
- Tested connectivity between devices using `ping`.
- Learned that ARP resolution can cause the first ping attempt to fail.

## 🔐 Security Relevance

- Console authentication restricts access to switch configuration.
- `enable secret` protects Privileged EXEC mode using a hashed password.
- MOTD banners warn users that access is restricted to authorized personnel.
- Switch management IP addresses allow remote management and should be protected against unauthorized access.
- Verifying network connectivity helps identify configuration errors and connectivity problems.

