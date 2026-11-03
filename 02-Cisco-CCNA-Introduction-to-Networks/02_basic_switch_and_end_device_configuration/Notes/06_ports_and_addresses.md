# 🌐 2.6 Ports and Addresses

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 02 - Basic Switch and End Device Configuration    
**Focus Area:** IP Addresses, Network Interfaces & Physical Ports  

## 🎯 Objective 

- Understand the purpose of IP addresses in network communication.
- Identify the differences between IPv4 and IPv6 addresses.
- Understand the purpose of network interfaces and physical ports.
- Recognise common network connection types.


## 🧠 2.6.1 IP Addresses

An **IP (Internet Protocol) address** is a logical address used to identify a device's network interface and allow communication across IP networks.

There are two versions of IP addresses:

### IPv4 (Internet Protocol Version 4)

- Uses a 32-bit address.
- Written as four decimal numbers separated by dots.
- Each number ranges from 0 to 255.

Example:
```text
192.168.1.10
```

### IPv6 (Internet Protocol Version 6)

- Uses a 128-bit address.
- Written as hexadecimal numbers separated by colons.
- Provides a much larger address space than IPv4.

Example:
```text
2001:db8:abcd:1::10
```

> NOTE: IP addresses are assigned to network interfaces, rather than permanently identifying the physical device itself.

## 🧠 2.6.2 Interfaces and Ports

Network devices use **interfaces and ports** to connect to other devices and exchange data.

A **physical port** is a connection point on a networking device where a cable can be connected.

> NOTE: Each physical interface has specifications or standards that define it. A cable connecting to the interface must meet the physical standards of that interface.

An **interface** is the network connection through which a device sends and receives data. Interfaces can be physical or virtual.

### Common Network Connections

- Ethernet: Used for wired network connections.
- Wireless: Used for network communication without cables.
- Console: Used for local device management and configuration.

Cisco Interface Examples:
```text
FastEthernet0/1
GigabitEthernet0/1
```

These names identify specific network interfaces on Cisco devices.

> NOTE: Physical switch ports typically forward Ethernet frames, while a switch virtual interface (SVI) can be assigned an IP address for remote management.

## 📌 Key Concepts to Remember

- IP Address: A logical address used for communication across IP networks.
- IPv4: Uses 32-bit addresses written in dotted-decimal notation.
- IPv6: Uses 128-bit addresses written in hexadecimal notation.
- Physical Port: A connection point for a network cable.
- Network Interface: A physical or virtual connection used for network communication.
- Console Port: Provides local management access without requiring an IP address.


## 🔐 Security Relevance

- IP addresses help administrators identify and manage devices on a network.
- Network interfaces can be configured to control connectivity and access.
- Unused switch ports should be disabled to reduce unauthorised physical network access.
- Management interfaces should be protected to prevent unauthorised device configuration.
