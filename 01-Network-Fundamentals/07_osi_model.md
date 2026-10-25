# Network Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: The OSI Model  

## 🎯 Objective
- Understand how the OSI Model structures network communication  
- Learn the role of each layer in data transmission  
- Identify how different layers relate to real-world security threats  

## 🧠 Core Concepts Learned 
### The OSI Model (OPEN SYSTEMS INTERCONNECTION MODEL)
- A conceptual framework that defines how all networked devices send, receive and interpret data
- Consists of 7 layers, each with a specific role in data transmission

⚠️ **Key Concepts: Encapsulation** and **Decapsulation**
- **(Encapsulation)**
    - As data moves through OSI layers, specific processes take place, and additional information (headers) is added to the data 
- **Decapsulation**
    - At the receiving end, the data is unpacked 

---

### Layers: 
#### 7. Application Layer 
- The layer where users interact with network services
- At this level protocols and rules are in place to determine how the user should interact with data sent or received
- Here most of applications provide a friendly Graphical User Interface (GUI) for users to interact with data

**Examples:** HTTP/S, FTP, SMTP, DNS  

**Security relevance:**  
- Phishing attacks  
- Malicious websites  
- Fake services  
- Data exfiltration  

⚠️ Application Layer is the most exposed (phishing, malicious payloads)


#### 6. Presentation Layer 
- Responsible for formatting, encrypting, and compressing data  
- Ensures data is converted into a **standard format** that can be understood by different systems  
- Handles translation between different data representations (e.g., character encoding)

**Examples:** 
- Encryption: SSL / TLS 
- Data encoding formats: ASCII, Unicode
- Compression

⚠️ Presentation Layer provides data confidentiality through encryption

#### 5. Session Layer
- Establishes, manages, and terminates sessions between devices  
- Maintains the connection while data is being exchanged  
- Can close inactive or interrupted sessions  
- Supports session checkpoints, allowing data to resume from the last known point instead of retransmitting everything  

⚠️ Vulnerable to session hijacking

#### 4. Transport Layer  
- Responsible for end-to-end communication between devices  
- Breaks data into segments and reassembles it at the destination  
- Manages reliability, flow control, and error detection  

**It follows two different protocols:**

- **TCP (Transmission Control Protocol)**  
  - Reliable, connection-oriented  
  - Guarantees delivery using acknowledgements and retransmissions  
  - Ensures correct order of data  
  - Examples: HTTP, HTTPS, FTP  

- **UDP (User Datagram Protocol)**  
  - Fast, connectionless  
  - No guarantee of delivery or order  
  - Used where speed is more important than reliability  
  - Examples: DNS, VoIP, Streaming
  
⚠️ TCP can be targeted by SYN flood attacks   
⚠️ UDP can be abused in amplification attacks (e.g., DDoS)   
⚠️ Port scanning can be used to identify open services  

#### 3. Network Layer 
- Responsible for logical addressing and routing of data between networks
- Uses IP addresses to identify source and destination devices
- Breaks data into packets and adds IP headers for delivery
- Enables communication across multiple interconnected networks (the Internet)
- Determines the best logical path for data to travel across networks 

**Routing Protocols:** 
    - OSPF: Open Shortest Path First
    - RIP: Routing Information Protocol

**Devices:** Routers

⚠️ Vulnerable to IP spoofing, Routing attacks, Network scanning and mapping 

#### 2. Data Link Layer  
- Responsible for local communication within the same network  
- Uses MAC addresses to identify devices on the local network  
- Packages data into frames for transmission  
- Performs error detection using frame checks (e.g., CRC)
- Works closely with the Network Layer to deliver packets on the local link 

**Protocols:** 
- ARP: maps IP addresses to MAC addresses  

**Devices:** Switches  

⚠️ Vulnerable to ARP spoofing, MAC flooding attacks and VLAN hopping

#### 1. Physical Layer 
- Devices use electrical signals to transfer data between them which are in binary system, this layer is responsible for transmitting raw bits (0s and 1s) over a physical medium 
- Defines the hardware components and transmission methods used in communication  

**Examples:**  
- Ethernet cables  
- Fiber optic cables  
- Wireless signals (radio waves) 

⚠️ Vulnerable to physical tampering, cable tapping (data interception), hardware damage or disruption

---

### How it works
**Example: Accessing a Website**

1. **Application Layer (7)**  
    - User enters: `www.google.com`
    - HTTP/HTTPS request is created  

2. **Presentation Layer (6)**  
   - Data is encrypted (HTTPS)
   - Data is formatted for transmission 

3. **Session Layer (5)**  
   - A session is established and maintained between client and server

4. **Transport Layer (4)**  
   - TCP breaks data into segments  
   - Ensures reliable delivery (error checking, retransmission, sequencing) 

5. **Network Layer (3)**  
   - IP addresses are added  
   - Routing determines the best path to the destination 

6. **Data Link Layer (2)**  
   - Frames are created  
   - MAC addresses are added for local delivery  


7. **Physical Layer (1)**  
   - Data is transmitted as electrical signals or radio waves (Wi-Fi)

⚠️ **On the Receiving Side (Decapsulation)**
- The data travels back up from Layer 1 → Layer 7  
- Each layer removes its header and processes the data  
- The application (e.g., browser) finally displays the website

## 🛠️ Practical Skills Developed
- Understanding how data flows through network layers  
- Identifying protocols and their functions  
- Mapping network attacks to OSI layers  
- Improving ability to troubleshoot network communication issues 

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  

## 🔐 Security Relevance
- Each OSI layer presents different attack surfaces  
- Understanding layers helps identify where attacks occur  
- Essential for roles such as SOC Analyst and Network Security Engineer  

## 📌 Lessons Learned  
⚠️ The OSI Model simplifies complex network communication into manageable layers    
⚠️ Each layer has distinct responsibilities but works together as a system   
⚠️ It provides a structured way to understand how data flows across networks     
⚠️ Security vulnerabilities can occur at each stage   