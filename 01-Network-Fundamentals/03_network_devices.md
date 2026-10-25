# Network Fundamentals – TryHackMe and Solent University Cybersecurity Coursework

Platform: TryHackMe     
Level:  Beginner / Foundation  
Focus Area: Network Devices and Infrastructure

## 🎯 Objective
- Understand the role of key network devices  
- Learn how devices communicate within and across networks  
- Build a foundation for analysing network traffic in cybersecurity

## 🧠 Core Concepts Learned

### Network Devices and Their Attributes
- Each device plays a specific role in how data is transmitted, controlled, and secured within a network  
- Understanding these devices is essential for analysing network behaviour and detecting threats

- **Devices (PC, Phone, Server)**  
  - Send and receive data

<br>

- **Switch**  
  - Connects devices (computers, printers, servers) within the same network  
  - Can support multiple devices depending on the number of ports (e.g. 4–64+)  
  - Keeps track of which device is connected to which port  
  - Uses **MAC addresses** to forward traffic  

- **Router**  
  - Routes traffic between different networks (e.g. home → internet)  
  - **Routing** is the process of data travelling across networks  
    - Determines the best path for data to reach its destination  
    - More efficient when multiple paths exist between networks 

<br>

⚠️ **Switches and Routers work efficiently together:**
- The **switch** handles communication inside the local network (LAN)  
- The **router** connects the network to other networks (e.g. the internet)  
- Switches operate at **Layer 2 (Data Link)**, routers operate at **Layer 3 (Network)**  
 
<br>

- **Modem**  
  - Connects the router to the Internet Service Provider (ISP)  
  - Converts digital signals into a format suitable for transmission over the internet  
  - Acts as the entry point to the internet for a home network   

<br>

- **Firewall**  
  - Filters incoming and outgoing traffic based on rules  
  - Often the first line of defense in network security  
  - Allows or blocks traffic depending on security policies   
  - Can be hardware (router/firewall device) or software-based   

<br>

- **IDS (Intrusion Detection System)**  
  - Monitors network traffic for suspicious activity  
  - Generates alerts but does not block traffic  

- **IPS (Intrusion Prevention System)**  
  - Monitors and actively blocks malicious traffic  
  - Can stop attacks in real time   

<br>

- **Access Point**  
  - Provides wireless (Wi-Fi) connectivity to devices  
  - Extends a wired network into a wireless network  
  - Common in homes, offices, and public networks  

## 🛠️ Practical Skills Developed
- Identifying different network devices and their roles  
- Understanding how traffic flows within a network (LAN)  
- Understanding how traffic moves between networks (LAN → Internet)  
- Recognising how devices interact (switch ↔ router)  
- Reading and interpreting basic network diagrams

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework  
- TryHackMe Platform  

## 🔐 Security Relevance
- Network devices control how traffic flows and where it goes  
- Firewalls help enforce security policies and filter malicious traffic  
- IDS/IPS systems detect and prevent attacks in real time  
- Misconfigured devices can create security vulnerabilities  
- Understanding device roles helps identify weak points in a network  

## 📌 Lessons Learned 
⚠️ Different devices have specific roles in a network  
⚠️ Switches operate inside networks, routers connect networks together  
⚠️ Network security depends on correct device configuration  
⚠️ Network infrastructure controls how traffic flows across networks