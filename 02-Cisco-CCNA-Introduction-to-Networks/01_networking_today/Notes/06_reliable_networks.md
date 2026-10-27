# 🌐 1.6 Reliable Networks

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 01 - Networking Today     
**Focus Area:** Network Architecture, Fault Tolerance, Scalability, Quality of Service, and Network Security

## 🎯 Objective 
- Understand the four characteristics of a reliable network.

## 🧠 1.6.1 Network Architecture 

**Network architecture** refers to the technologies and infrastructure that support communication across a network. 

Refers to how a network is designed, including: 
- Devices: Routers, switches, servers, and computers.
- Connections: How devices are connected through cables or wireless networks.
- Technologies and protocols: How devices communicate and exchange data.
- Network design: How the network supports reliability, performance, growth, and security.

A reliable network is designed around four key characteristics:

## 🧠 1.6.2 Fault Tolerance 

**Fault tolerance** is the ability of a network to continue operating when a device or connection fails.

- Uses redundant (backup) connections and devices.
- Provides alternative paths for network traffic.
- Reduces disruption when failures occur.

Example: A company has two network connections between its offices. If one connection fails, traffic can use the other connection to maintain communication.  

Redundancy means having backup connections or devices to reduce the impact of failures.

### Packet-Switched Network:
A **packet-switched network** breaks data into smaller packets and sends them to their destination through available network paths.

Packets can take different routes to reach the same destination. If one path fails, they can use another available route.
    > The network must have **redundant paths** and be able to reroute traffic when a failure occurs. 

## 🧠 1.6.3 Scalability 

**Scalability** is the ability of a network to expand and support more users, devices, and applications without significantly reducing performance.

- Allows new devices and users to be added.
- Supports business growth.
- Uses networking standards and protocols to support expansion.

Example: A company expands from 50 to 100 employees. Its scalable network can support the additional computers, printers, and network traffic without requiring a complete redesign.

## 🧠 1.6.4 Quality of Services 

**Quality of Service (QoS)** is a network mechanism that prioritises certain types of traffic to maintain performance when network resources are limited.
    > When the volume of traffic is grater than what can be transported across the network, devices will hold the packets in memory until resources become available to transmit them.

- Prioritises time-sensitive traffic.
- Helps reduce delays for important applications.
- Supports voice and video communications.

Example: Employees are attending video conferences while others download large files. QoS, managed by the router, can prioritise video and voice traffic to help prevent interruptions during meetings.

NOTE: QoS does not increase the available bandwidth. It helps the network decide **which traffic should receive priority when congestion occurs.**

## 🧠 1.6.5 Network Security

**Network security** protects network infrastructure, devices, and data from unauthorised access, misuse, and attacks.

- Confidentiality: Ensures information is accessible only to authorised users.
- Integrity: Protects information from unauthorised modification.
- Availability: Ensures network services and information remain accessible when needed.

Example: A company uses firewalls to control network traffic, authentication to restrict access, and encryption to protect sensitive information.

Confidentiality, Integrity, and Availability are known as the CIA Triad.

## 📌 Key Concepts to Remember

- Fault Tolerance : Keep the network operating during failures
- Scalability: Support network growth
- Quality of Service: Prioritise important traffic
- Security: Protect devices, data, and communications


## 🔐 Security Relevance

- Reliable networks must remain both available and secure.
- Redundant connections help maintain availability during failures.
- Scalable designs allow security controls to expand as networks grow.
- QoS helps critical communications perform reliably.
- Firewalls, authentication, and encryption protect network resources.

Key Takeaway: A reliable network should continue operating during failures, support growth, prioritise important traffic, and protect information.

 