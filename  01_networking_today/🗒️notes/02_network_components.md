# 1.2 Network Components

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 01 - Networking Today     
**Focus Area:** Network Components & Communication

## 🎯 Objective 
- Understand the roles of hosts, clients, and servers in a network.
- Explain how peer-to-peer networks operate.
- Identify different types of end devices.
- Understand the purpose of intermediary network devices.
- Recognise the different types of network media used to transmit data.

## 🧠 1.2.1 Host Roles

A **host** is an end device connected to a network that can send or receive information.

Hosts are identified on IP networks using IP addresses, which allow devices to communicate with one another.

Hosts can operate as clients, servers, or both, depending on the services they provide or request.

### Clients

A **client** is a device or application that requests services or resources from another device.

Examples include:
- A laptop requesting a webpage from a web server.
- A smartphone accessing an email service.
- A computer accessing files stored on a network server.

### Servers

A **server** is a device or application that provides services or resources to clients over a network.

Common types of servers include:

- Web Server: Hosts websites and delivers web content.
- Email Server: Sends, receives, or stores email messages.
- File Server: Stores and shares files across a network.

**Real-World Example**

When a student accesses a university learning platform, their web browser acts as a client and communicates with a server that provides the requested content.

**Key Concept:** Clients request services, while servers provide them.

## 🧠 1.2.2 Peer-to-Peer

The word **peer** means someone or something of equal standing.

A **peer-to-peer (P2P) network** allows devices to share resources directly with one another without requiring a dedicated server.

In this type of network, **a device can act as both a client and a server**.

**Advantages**
- Simple to configure for small networks.
- Lower cost because a dedicated server is not required.
- Devices can share files and resources directly.

**Disadvantages**
- Difficult to manage as networks grow
- No centralised administration.
- Each computer is responsible for managing its own security.
- Performance may be affected when devices share multiple resources.
- Data availability depends on the devices providing the resources.

**Real-World Example**
Two computers connected to the same local network can share files directly.   

- Computer A: Shares access to a printer.
- Computer B: Shares files stored on its computer.

Scenario 1: Printer Sharing
Computer B (Client) **→** Requests to print a document **→** Computer A (Server)

Scenario 2: File Sharing
Computer A (Client) **→** Requests access to shared files **→** Computer B (Server)

## 🧠 1.2.3 End Devices

**End devices** are devices that send or receive data over a network.

Each end device has an address that helps identify it on the network. When one device sends a message, it uses the destination device's address to specify where the message should go.

### Examples of End Devices

- Desktop computers and laptops.
- Smartphones and tablets.
- Servers.
- Network printers.

**Real-World Example**
When a laptop accesses a website:
- Source: The laptop sends a request.
- Destination: The web server receives the request.

The server then sends a response back to the laptop, reversing their roles as the source and destination.

## 🧠 1.2.4 Intermediary Devices 

**Intermediary devices** connect end devices and networks, allowing data to travel between the source and destination.

They help manage network traffic and ensure that messages are forwarded towards the correct destination.

### Examples of Intermediary Devices

- Switch: Connects devices within a local network (LAN) and forwards data based on MAC addresses.
- Router: Connects different networks and forwards data packets based on IP addresses.
- Wireless Access Point (AP): Allows wireless devices to connect to a network.
- Firewall: Monitors and controls network traffic based on security rules.

### Main Functions

- Connect devices and different networks.
- Forward messages towards their destinations.
- Determine the best available path for data when routing.
- Regenerate or retransmit signals when necessary.
- Apply security rules to permit or block network traffic.

**Real-World Example**

In a university network:

- Switches connect computers and other wired devices within a building.
- Wireless Access Points allow students to connect laptops and smartphones using Wi-Fi.
- Routers connect different networks and provide paths towards external networks, including the internet.
- Firewalls help protect network resources by controlling permitted traffic.

## 🧠 1.2.5 Network Media

**Network media** refers to the physical or wireless methods used to transmit data between devices on a network.

There are three main types of network media:

### 1. Copper Cabling

Copper cables transmit data using **electrical signals**.

- Commonly used in Ethernet networks.
- Used to connect computers, switches, and routers.
- Relatively inexpensive and easy to install.
- Can be affected by electromagnetic interference (EMI).

**Example:** Connecting a computer to a network switch using an Ethernet cable.

### 2. Fibre-Optic Cabling

Fibre-optic cables transmit data using **pulses of light** through glass or plastic fibres.

- Supports high-speed data transmission.
- Suitable for long-distance connections.
- Resistant to electromagnetic interference.
- Commonly used in data centres and network backbones.

**Example:** Connecting network switches between university buildings using fibre-optic cables.

### 3. Wireless Media

Wireless networks transmit data using **electromagnetic waves**, typically radio waves.

- Allows devices to connect without physical cables, which supports mobility.
- Commonly used for Wi-Fi connections.
- Can be affected by interference, obstacles, and distance.

**Example:** A student connecting a laptop to the university Wi-Fi network.

### Choosing Network Media

When selecting network media, network engineers consider:
- **Distance:** How far the signal needs to travel.
- **Bandwidth:** How much data the connection needs to support per second.
- **Cost:** The price of equipment and installation.
- **Environment:** Whether interference or physical obstacles could affect communication.

 ## 🛠️ Key Concepts to Remember

| Component | Main Function |
|---|---|
| Host | Sends or receives data over a network |
| Client | Requests services or resources |
| Server | Provides services or resources |
| Peer-to-Peer | Allows devices to share resources without a dedicated server |
| End Device | Acts as the source or destination of network communication |
| Intermediary Device | Connects devices and forwards network traffic |
| Network Media | Carries data between devices using electrical signals, light, or radio waves |

## 🔐 Security Relevance

Understanding network components helps identify how data travels across a network and where security risks may occur.

- **End Device Security:** Protecting computers, servers, and smartphones from malware and unauthorised access.
- **Network Device Security:** Securing routers, switches, and wireless access points against unauthorised configuration changes.
- **Access Control:** Restricting access to shared files, printers, and other network resources.
- **Network Traffic Security:** Using encryption to protect sensitive information during transmission.
- **Wireless Security:** Securing Wi-Fi connections through authentication and encryption.

## 📌 Key Takeaways

- Hosts communicate over networks and can act as clients, servers, or both.
- Peer-to-peer networks allow devices to share resources directly without dedicated servers.
- End devices are the source or destination of network communication.
- Intermediary devices connect networks and forward data towards their destinations.
- Copper cables use electrical signals, fibre-optic cables use light, and wireless connections use radio waves.
- Understanding network components is essential for network configuration, troubleshooting, and cybersecurity.