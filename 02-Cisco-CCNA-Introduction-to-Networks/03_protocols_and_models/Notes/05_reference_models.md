# 🌐 3.5 Reference Models

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 03 - Protocols and Models  
**Focus Area:** OSI and TCP/IP Reference Models

## 🎯 Objective

Understand the benefits of layered networking models, the functions of the OSI and TCP/IP layers, and how these models describe communication between network devices.

## 🧠 3.5.1 The Benefits of Using a Layered Model

Network communication involves many different processes. A **layered model** divides these processes into smaller, more manageable layers, each responsible for specific functions.

Instead of understanding the entire communication process at once, we can focus on one layer at a time.

**Why do we use layered models?**

- **Simplifies Learning:** Makes complex network communication easier to understand.
- **Supports Troubleshooting:** Helps identify which part of the communication process is experiencing a problem.
- **Encourages Interoperability:** Allows devices from different manufacturers to communicate using common standards.
- **Supports Development:** Allows technologies and protocols within one layer to evolve without requiring changes to every other layer.
- **Provides a Common Language:** Helps networking professionals describe and discuss network communication.

**Human Communication Analogy:**

Think of travelling by plane.  
Your journey involves several stages, such as booking a ticket, checking in, passing through security, boarding and arriving at your destination.  
Each stage has a specific responsibility, but all stages work together to complete the journey.  

Similarly, networking layers perform different tasks that work together to deliver information.

## 🧠 3.5.2 The OSI Reference Model

The **OSI (Open Systems Interconnection) Reference Model** is a conceptual model developed by ISO to describe how network communication works.

It divides network communication into **seven layers**, each responsible for specific functions.

### Understanding Each OSI Layer

| Layer | Name | What It Actually Does | Real Examples |
|---|---|---|---|
| 7 | **Application** | Provides services for browsing websites, sending emails and transferring files. | HTTP, HTTPS, DNS, FTP, SMTP |
| 6 | **Presentation** | Converts data into a readable format, encrypts/decrypts it and compresses it. | UTF-8, JPEG, encryption, compression |
| 5 | **Session** | Opens, maintains and closes communication sessions between applications. | Session establishment, session management, checkpoints |
| 4 | **Transport** | Uses port numbers to deliver data to the correct application. TCP also checks delivery and retransmits lost data. | TCP, UDP, port numbers |
| 3 | **Network** | Uses IP addresses to identify destinations and routers to forward packets between networks. | IPv4, IPv6, routers, IP addresses |
| 2 | **Data Link** | Uses MAC addresses and frames to deliver data across a local network link. | Ethernet, switches, MAC addresses, frames |
| 1 | **Physical** | Sends bits through cables, fibre optics or wireless signals. | Ethernet cables, fibre-optic cables, radio waves, hubs |

**NOTE:** The OSI model is a reference model used to understand and describe network communication. Modern internet communication primarily uses the TCP/IP protocol suite.

## 🧠 3.5.3 The TCP/IP Protocol Model

The **TCP/IP (Transmission Control Protocol / Internet Protocol) model** describes how the TCP/IP protocol suite supports communication across networks.

It organises network communication into **four layers**.

| Layer | Main Function | Protocol Examples |
|---|---|---|
| **Application** | Provides network services to applications. | HTTP, HTTPS, DNS, DHCP |
| **Transport** | Manages communication between applications. | TCP, UDP |
| **Internet** | Provides logical addressing and packet routing. | IPv4, IPv6, ICMP |
| **Network Access** | Handles local network communication and physical transmission. | Ethernet, Wi-Fi, ARP |

The TCP/IP model is closely associated with the protocols used in real-world networks and the internet.

**Communication Process:**

- At the sender, data moves down through the layers, where protocol information is added through **encapsulation**.
- At the receiver, data moves up through the layers, where protocol information is processed and removed through **de-encapsulation**.

## 🧠 3.5.4 OSI and TCP/IP Model Comparison

Both models organise network communication into layers, but they group the functions differently.

The OSI model uses **seven layers**, while the TCP/IP model uses **four layers**.

| OSI Model | TCP/IP Model |
|---|---|
| 7. Application | Application |
| 6. Presentation | Application |
| 5. Session | Application |
| 4. Transport | Transport |
| 3. Network | Internet |
| 2. Data Link | Network Access |
| 1. Physical | Network Access |

**Main Differences:**

- The TCP/IP Application layer combines the functions of the OSI Application, Presentation and Session layers.
- The Transport layers perform similar functions in both models.
- The OSI Network layer corresponds to the TCP/IP Internet layer.
- The TCP/IP Network Access layer combines the functions of the OSI Data Link and Physical layers.

**Example: Opening a Website**

| Communication Task | OSI Layer | TCP/IP Layer |
|---|---|---|
| Requesting web content using HTTP | Application | Application |
| Delivering data using TCP | Transport | Transport |
| Addressing packets using IP | Network | Internet |
| Creating Ethernet frames | Data Link | Network Access |
| Transmitting signals through a cable | Physical | Network Access |

**Key Difference to Remember:**

The OSI model provides a detailed reference for understanding network communication, while the TCP/IP model describes the layered architecture associated with the protocols used by the internet.

## 📌 Key Concepts to Remember

- **Layered Models:** Divide complex network communication into smaller, manageable functions.
- **OSI Model:** A seven-layer reference model for understanding network communication.
- **TCP/IP Model:** A four-layer model associated with the internet protocol suite.
- **Transport Layer:** Manages end-to-end communication between applications.
- **Network / Internet Layer:** Handles logical addressing and packet routing.
- **Data Link Layer:** Handles frame delivery over a local network link.
- **Physical Layer:** Transmits bits as signals through a network medium.
- **Encapsulation:** Adds protocol information as data moves down the layers.
- **De-encapsulation:** Processes and removes protocol information as data moves up the layers.

## 🔐 Security Relevance

- Understanding networking layers helps security professionals identify where attacks or communication problems occur.
- Firewalls can filter traffic using IP addresses, transport protocols, port numbers and, in some cases, application information.
- Packet analysis tools such as Wireshark allow administrators to examine communication at different layers.
- Security mechanisms operate at different layers, such as IPsec at the Internet/Network layer and TLS above the Transport layer.
- Layered troubleshooting helps administrators isolate network failures and investigate suspicious activity.