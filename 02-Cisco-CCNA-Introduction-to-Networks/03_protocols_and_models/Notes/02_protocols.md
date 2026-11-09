# 🌐 3.2 Protocols

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 03 - Protocols and Models  
**Focus Area:** Network Protocols

## 🎯 Objective

Understand the functions of network protocols and how different protocols interact to enable successful communication between network devices.

## 🧠 3.2.1 Network Protocol Overview

**Network protocols** are sets of agreed rules that allow devices to communicate and exchange information across a network.

Network protocols can be implemented in software, hardware or a combination of both on network devices.

Different protocols perform different tasks, but they work together to support network communication.

**Four Main Types of Network Protocols:**

1. **Network Communications Protocols:** Enable devices to exchange information across a network, defining how data is transmitted and received.
   - Examples: IP (Internet Protocol), TCP (Transmission Control Protocol), UDP (User Datagram Protocol) and HTTP (HyperText Transfer Protocol).

2. **Network Security Protocols:** Protect network communication by providing mechanisms such as encryption, authentication and data integrity.
   - Examples: TLS (Transport Layer Security), SSH (Secure Shell) and SSL (Secure Sockets Layer).

3. **Routing Protocols:** Allow routers to exchange routing information and determine suitable paths to reach destination networks.
   - Examples: OSPF (Open Shortest Path First) and BGP (Border Gateway Protocol).

4. **Service Discovery Protocols:** Help devices automatically discover other devices or available services on a network.
   - Examples: DHCP (Dynamic Host Configuration Protocol) and DNS (Domain Name System) which support network configuration and service location

## 🧠 3.2.2 Network Protocol Functions

Network protocols perform several important functions during communication.

| Function | Description |
|---|---|
| **Addressing** | Identifies the source and destination of a message. |
| **Reliability** | Provides mechanisms to detect and recover from lost data when supported by the protocol. |
| **Flow Control** | Regulates the transmission rate to prevent the receiver from being overwhelmed. |
| **Sequencing** | Uses sequence information to help organise data in the correct order. |
| **Error Detection** | Identifies errors that may occur during transmission. |
| **Application Interface** | Enables communication between network applications and network services. |

Not every protocol performs all these functions. Each protocol has specific responsibilities.

**Example:**

TCP provides sequencing, reliability and flow control, while IP provides logical addressing and packet delivery between networks.

## 🧠 3.2.3 Protocol Interaction

Network communication usually requires several protocols working together.

This combination of protocols is known as a **protocol suite**.

The **TCP/IP protocol suite** is used for communication across the internet and most modern networks.

**Example: Opening a Website**

When a user opens a website, several protocols may work together:

1. **DNS:** Resolves the website's domain name into an IP address.
2. **HTTPS:** Enables secure communication between the browser and web server.
3. **TCP:** Provides reliable communication between the applications.
4. **IP:** Provides logical addressing and routes packets towards their destination.
5. **Ethernet or Wi-Fi:** Transmits data across the local network.

**NOTE:** This example describes a common HTTPS connection using TCP. 

**Human Communication Analogy:**

When sending a letter through the postal service:

- The sender writes a message using a language the receiver understands.
- The sender places the letter inside an addressed envelope.
- The postal service uses the destination address to transport the letter.
- The receiver opens the envelope and reads the message.

Similarly, network protocols perform different tasks that work together to deliver information successfully.

## 📌 Key Concepts to Remember

- **Network Protocols:** Agreed rules that enable communication between network devices.
- **Protocol Functions:** Include addressing, reliability, flow control, sequencing, error detection and application interfaces.
- **Protocol Interaction:** Multiple protocols work together to support communication.
- **Protocol Suite:** A collection of related protocols designed to work together.
- **TCP/IP:** The main protocol suite used on modern networks.
- **TCP vs UDP:** TCP provides reliable, ordered delivery, while UDP does not guarantee delivery or ordering.
- **Encapsulation:** Protocols add their own control information as data moves through the networking layers.

## 🔐 Security Relevance

- Understanding network protocols helps administrators identify normal and suspicious communication.
- Analysing protocol headers can reveal source and destination addresses, ports and other communication details.
- Security tools such as firewalls use protocol information to inspect and filter network traffic.
- Secure protocols such as HTTPS protect communication through encryption and authentication.
- Understanding protocol interactions helps administrators troubleshoot connectivity problems and investigate network attacks.