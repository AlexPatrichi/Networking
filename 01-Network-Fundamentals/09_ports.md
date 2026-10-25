# Network Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: Ports 

## 🎯 Objective
- Understand what ports are and how they are used in network communication  
- Learn how services are identified using port numbers  
- Identify the security implications of open and exposed ports  

## 🧠 Core Concepts Learned 
### Ports 
- Networking devices use ports to enforce strict rules when communicating with one another
- Applications, software and behaviours are associate with a standard set of rules

**Example:**
   - All web browser data is sent over port 80
   - All web browser data share one common rule 

- When a connection has been established succesfully, any data sent or received by a device will go through these ports 

- Ports are numerical values ranging from **0 to 65,535** 
- Used by transport layer protocols such as TCP and UDP  

**Why only 65,535 ports?**
- Source ports and destination port are stored in TCP/UDP headers
- Each port number is **16 bits** in size  
- 16 bits = 2¹⁶ = 65,536 possible values (0 to 65,535)

⚠️ There are 65,536 TCP ports and 65,536 UDP ports available

#### Port Number Use
**// 0 to 1023**
- Reserved for knwon services 
- Assigned by **IANA (Internet Assigned Numbers Authority)** 
- These ports are **public**, any application can use them  

Examples:
- HTTP → 80  
- HTTPS → 443  
- FTP → 21  
- SSH → 22  

**// 1024 to 49,151**
- Reserved for specific applications or services that need a consistent port (businesses or government)
- They need to be registered officialy   

Examples: 
- 3306 for MySQL
- 25565 for Minecraft

**// 49,152 to 65,535**
- Temporary ports used by clients
- When session ends, the port is released for future use

#### How Ports Work (Client–Server Model)
- A server listens on a specific port (443 for HTTPS)  
- A client connects using a temporary port  
- Communication happens between:
  - Source IP + Source Port  
  - Destination IP + Destination Port  

- This combination is called a **socket**

#### TCP vs UDP Ports

**TCP Ports:**
- Reliable, connection-oriented  
- Used for services requiring accuracy  
- Examples: HTTP, HTTPS, FTP  

**UDP Ports:**
- Fast, connectionless  
- Used where speed is more important than reliability  
- Examples: DNS, VoIP, streaming  

## 🧪 TryHackMe Lab Example
- Connected to a remote service using a non-standard port  

### Tasks Performed:
- Accessed an external IP address (8.8.8.8) using a custom port (1234)   

### Key Insight:
- Services can run on non-standard ports  
- Accessing them requires specifying the port number manually  
- Network communication depends on both IP address and port number  

## 🛠️ Practical Skills Developed
- Understanding how services communicate using ports  
- Identifying common ports and their associated protocols  
- Recognising how attackers discover open services 

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  
- Command Line Interface (CLI)
  - Windows Command Prompt (cmd)
  - Linux Terminal (bash)

## 🔐 Security Relevance
- Open ports can expose services to attackers  
- Port scanning is used to discover running services  
- Misconfigured services can lead to exploitation  
- Common tools: Nmap (port scanning)  

## 📌 Lessons Learned  
⚠️ Ports allow multiple services to run on a single device  
⚠️ Each service is identified by a unique port number  
⚠️ Open ports can represent potential security risks  