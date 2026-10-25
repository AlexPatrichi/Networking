# Network Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: Port Forwarding

## 🎯 Objective
- Understand what port forwarding is and why it is used  
- Learn how external traffic reaches internal devices  
- Identify the security risks of exposing services to the internet  


## 🧠 Core Concepts Learned 
### What is Port Forwarding?
- Port forwarding is a router configuration that redirects incoming traffic to a specific device inside a local network  
- It allows external devices (Internet) to access services hosted on private networks  

### Why Port Forwarding is Needed
- Devices inside a local network use **private IP addresses**  
- These are not directly accessible from the Internet  
- A router uses **NAT (Network Address Translation)** to communicate with external networks  

⚠️ Port forwarding creates a rule that maps an external port to an internal device and service

- Without it, applications and services such as web servers are only available to devices within the same direct network

### How It Works (Example)
- Public IP (Router): `203.0.113.10`  
- Internal Device: `192.168.1.10`  
- Service: Web server running on port 80  

**Flow:**
1. External user connects to: `203.0.113.10:80`  
2. Router receives the request  
3. Port forwarding rule redirects traffic to:  
   → `192.168.1.10:80`  
4. Internal device responds  
5. Router sends the response back to the user  

---

### Analogy: Telephone Numbers and Extensions

- A **public IP address** is like a company’s main phone number  
- A **port** is like an extension number inside the company  
- A **device/service** is like a specific person or department  

### Without Port Forwarding
- Someone calls the main number  
- The receptionist (router) does not know which extension to connect them to  
- The call is blocked or ignored  

⚠️ External access is not allowed by default  

### With Port Forwarding
- A rule is set:
  - Calls to extension **80** → go to the **web server**  
  - Calls to extension **22** → go to the **SSH service**  

- Now when someone calls:
  - Main number + extension → they are routed correctly  

⚠️ This is exactly how port forwarding works  

---

### NAT vs Port Forwarding
- NAT allows multiple devices to share one public IP address  
- By default, incoming connections are blocked  
- Port forwarding creates an exception, allowing specific external traffic to reach an internal device  

### Key Components
- **Public IP** → visible on the Internet  
- **Private IP** → used inside local network  
- **Router (NAT device)** → translates and forwards traffic  
- **Port number** → identifies the service  

### Common Use Cases
- Hosting a web server from home  
- Online gaming servers  
- Remote desktop access  
- CCTV / IP cameras  

## 🛠️ Practical Skills Developed
- Understanding how routers manage incoming traffic  
- Configuring access to internal services  
- Recognising how external users connect to a private network

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  

## 🔐 Security Relevance
- Exposes internal services to the Internet  
- Misconfigured port forwarding can lead to unauthorised access  
- Attackers scan open ports to find vulnerable services  
- Should only expose necessary ports and use strong authentication  

## 📌 Lessons Learned  
⚠️ Devices in a private network are not directly accessible from the Internet  
⚠️ Port forwarding allows controlled external access to internal services  
⚠️ Exposing services increases security risk if not properly configured  