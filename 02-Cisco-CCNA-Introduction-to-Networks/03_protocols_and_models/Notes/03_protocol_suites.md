# 🌐 3.3 Protocol Suites

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 03 - Protocols and Models  
**Focus Area:** Network Protocol Suites and TCP/IP Communication

## 🎯 Objective

Understand how network protocols are organised into protocol suites, how these suites have evolved, and how the TCP/IP protocol suite enables communication between devices across networks.

## 🧠 3.3.1 Network Protocol Suites

A **protocol suite** is a group of related network protocols that work together to provide network communication services.

Each protocol performs a specific function, and the protocols interact to allow information to travel between devices.

**Important Characteristics:**

- **Individual Protocols:** Each protocol has a specific responsibility.
- **Protocol Interaction:** Protocols work together to support communication.
- **Layered Structure:** Protocols are organised into layers according to their functions.

**Example:**

When opening a website, several protocols work together:

- **HTTP/HTTPS:** Handles communication between the web browser and web server.
- **TCP:** Provides reliable, ordered delivery of data.
- **IP:** Provides logical addressing and packet routing.
- **Ethernet:** Handles communication over the local wired network.

These protocols belong to the TCP/IP protocol suite or operate alongside it.

## 🧠 3.3.2 Evolution of Protocol Suites

Different protocol suites were developed as computer networks evolved.

Initially, many organisations used their own proprietary network protocols, which made communication between equipment from different manufacturers difficult.

Over time, TCP/IP became the dominant protocol suite because its open standards allowed devices from different manufacturers to communicate.

**Examples of Protocol Suites:**

- **TCP/IP:** An open-standard protocol suite used by the internet and modern networks.
- **OSI Protocol Suite:** Developed as an alternative to TCP/IP but never widely adopted.
- **AppleTalk:** A proprietary protocol suite developed by Apple, now obsolete.
- **Novell NetWare (IPX/SPX):** A protocol suite historically used in Novell networks, now largely obsolete.

**Why did TCP/IP become dominant?**

- **Open Standards:** Devices from different manufacturers can communicate.
- **Compatibility:** Works across different network technologies.
- **Scalability:** Supports small networks and large interconnected networks.
- **Widespread Adoption:** Became the foundation of the modern internet.

## 🧠 3.3.3 TCP/IP Protocol Example

The **TCP/IP protocol suite** contains multiple protocols that perform different functions during communication.

For example, when accessing a website:

1. **HTTP:** Defines how the browser requests web content and how the server responds.
2. **TCP:** Establishes a connection and provides reliable, ordered delivery.
3. **IP:** Adds logical addressing information so packets can travel between networks.
4. **Ethernet:** Encapsulates IP packets into frames for transmission across a local wired network.

**Human Communication Analogy:**

Imagine sending a document through the postal service:

- You write the document using an agreed language.
- You divide it into numbered pages if necessary.
- You place the document inside an addressed envelope.
- The postal service transports it towards its destination.

Similarly, each networking protocol performs a different task to support successful communication.

> **NOTE:** This example uses HTTP over TCP and Ethernet. Other combinations are possible, including HTTPS and Wi-Fi.

## 🧠 3.3.4 TCP/IP Protocol Suite

The TCP/IP model organises network communication into **four layers**.

| Layer | Main Function | Protocol Examples |
|---|---|---|
| **Application** | Provides network services to applications. | HTTP, HTTPS, DNS, DHCP |
| **Transport** | Manages communication between applications. | TCP, UDP |
| **Internet** | Provides logical addressing and routing between networks. | IPv4, IPv6, ICMP |
| **Network Access** | Handles communication over the physical network medium. | Ethernet, Wi-Fi |

Each layer relies on the services provided by the layer below it.

**Two Important Characteristics of TCP/IP:**

1. **Open Standard Protocol Suite**
   - Publicly available and can be implemented by any manufacturer in their hardware or software.

2. **Standards-Based Protocol Suite**
   - Developed and maintained through recognised standards organisations, helping ensure compatibility between devices from different manufacturers.

### Common Protocols at Each Layer
#### 1. Application Layer 

Provides network services used by applications.   

**Name System**
- **DNS (Domain Name System):** 
Translates domain names into IP addresses.

**Host Configuration**
- **DHCPv4 / DHCPv6 (Dynamic Host Configuration Protocol):** 
Automatically provides IPv4 or IPv6 configuration information to devices.
- **SLAAC (Stateless Address Autoconfiguration):** 
Allows IPv6 devices to configure their own addresses without a DHCPv6 server.

**Email**
- **SMTP (Simple Mail Transfer Protocol):** 
Sends emails between clients and mail servers (or between mail servers).
- **POP3 (Post Office Protocol version 3):** 
Downloads emails from a mail server.
- **IMAP (Internet Message Access Protocol):** 
Allows users to access and manage emails stored on a mail server.

**File Transfer**
- **FTP (File Transfer Protocol):** 
Transfers files between devices over a network.
- **SFTP (SSH File Transfer Protocol):** 
Securely transfers files using SSH encryption.
- **TFTP (Trivial File Transfer Protocol):** 
A simple file transfer protocol with minimal overhead and no built-in authentication or encryption.

**Web and Web Services**
- **HTTP (Hypertext Transfer Protocol):** 
Exchanges web content between clients and servers.
- **HTTPS (Hypertext Transfer Protocol Secure):** 
Protects HTTP communication using encryption.
- **REST (Representational State Transfer):** 
An architectural style commonly used with HTTP to build web services and APIs.

#### 2. Transport Layer

Manages communication between applications running on different devices.

**Connection-Oriented**
- **TCP (Transmission Control Protocol):** 
Provides reliable, ordered communication using acknowledgements and retransmissions.

**Connectionless**
- **UDP (User Datagram Protocol):** 
Sends data without establishing a connection or guaranteeing successful delivery.

#### 3. Internet Layer

Provides logical addressing, packet delivery and routing between networks.

**Internet Protocol**
- **IPv4 (Internet Protocol version 4):** 
Uses 32-bit addresses to identify devices and deliver packets across networks.
- **IPv6 (Internet Protocol version 6):** 
Uses 128-bit addresses and provides similar packet delivery functions.
- **NAT (Network Address Translation):** 
Translates IPv4 addresses, commonly allowing private networks to communicate using public IPv4 addresses.

**Messaging**
- **ICMPv4 (Internet Control Message Protocol for IPv4):** 
Reports errors and provides diagnostic information for IPv4 communication.
- **ICMPv6 (Internet Control Message Protocol for IPv6):** 
Provides error reporting and diagnostic functions for IPv6.
- **ICMPv6 ND (Neighbour Discovery):** 
Helps IPv6 devices discover neighbours, resolve link-layer addresses and detect duplicate addresses.

**Routing Protocols**
- **OSPF (Open Shortest Path First):** 
A link-state routing protocol that uses areas to organise routing information.
- **EIGRP (Enhanced Interior Gateway Routing Protocol):** 
A routing protocol developed by Cisco that uses metrics to determine suitable paths.
- **BGP (Border Gateway Protocol):** 
Exchanges routing information between autonomous systems, including internet service providers.

#### 4. Network Access Layer

Handles communication over the local network medium.

**Address Resolution**
- **ARP (Address Resolution Protocol):** 
Resolves IPv4 addresses to MAC addresses on a local network.

> **NOTE:** Cisco places ARP in the Network Access layer because its primary purpose is to discover MAC addresses, although some references classify it differently.

**Data Link Protocols**
- **Ethernet:** 
Defines standards for wired local network communication, including framing and media access.
- **WLAN (Wireless Local Area Network):** 
Uses wireless networking standards, such as Wi-Fi, to communicate over radio signals.

## 🧠 3.3.5 TCP/IP Communication Process

When two devices communicate, data moves through the TCP/IP layers.

At the sender, information moves **down the layers**, with each layer adding the information needed for transmission.

Sender: 
Application (User Data) → Transport (TCP) → Internet (IP) → Network Access (Ethernet)

This process is called **encapsulation** (✈️ Boarding the plane).

**Example: Sending a Web Request**

1. **Application:** The browser creates an HTTP request.
2. **Transport:** TCP adds a header containing port numbers and other control information.
3. **Internet:** IP adds a header containing source and destination IP addresses.
4. **Network Access:** Ethernet adds frame information, including source and destination MAC addresses, and the frame is transmitted as signals.

At the receiving device, information moves **up the layers** as the protocol information is processed and removed.

This process is called **de-encapsulation** (🛬 Leaving the plane).

Receiver:
Network Access (Ethernet) → Internet (IP) → Transport (TCP) → Application (User Data) 

> **NOTE:** When packets travel through routers, the network access frame is replaced as necessary for each outgoing link, while the IP packet continues towards its destination.

## 📌 Key Concepts to Remember

- **Protocol Suite:** A group of related protocols that work together to support network communication.
- **TCP/IP:** The main protocol suite used on the internet and modern networks.
- **Open Standards:** Allow devices and software from different manufacturers to communicate.
- **Four TCP/IP Layers:** Application, Transport, Internet and Network Access.
- **Encapsulation:** Adds protocol information as data moves down the layers.
- **De-encapsulation:** Processes and removes protocol information as data moves up the layers.
- **Protocol Interaction:** Different protocols cooperate to deliver information between devices.

## 🔐 Security Relevance

- Understanding protocol suites helps administrators identify how network traffic is generated, transmitted and received.
- Firewalls can inspect IP addresses, transport protocols and port numbers to control network communication.
- Packet analysis tools such as Wireshark allow administrators to examine protocol headers and investigate suspicious traffic.
- Secure protocols such as HTTPS, SSH and IPsec help protect communication through encryption and authentication.
- Understanding encapsulation and de-encapsulation helps security professionals analyse packets and troubleshoot network problems.