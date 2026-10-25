# Network Fundamentals – TryHackMe and Solent University Cybersecurity Coursework

Platform: TryHackMe    
Level:  Beginner / Foundation  
Focus Area: Networking Addressing 

## 🎯 Objective
- Understand how devices are identified on a network  
- Learn the difference between IP and MAC addresses  
- Understand how devices communicate within a local network 

## 🧠 Core Concepts Learned  

### IP Address (Internet Protocol Address)
- Every device gets an IP Address so data knows where to go.
- Can be used to identify a host on a network for a period of time.  

**Example:** 
 - Device (PC): 192.168.1.10
 - Router:      192.168.1.1

<p align="center">
<strong>IP Address</strong><br>

<table align="center">
  <tr>
    <td align="center"><strong>192</strong></td>
    <td align="center"><strong>168</strong></td>
    <td align="center"><strong>1</strong></td>
    <td align="center"><strong>1</strong></td>
  </tr>
  <tr>
    <td align="center">Octet 1</td>
    <td align="center">Octet 2</td>
    <td align="center">Octet 3</td>
    <td align="center">Octet 4</td>
  </tr>
  <tr>
    <td align="center">0–255</td>
    <td align="center">0–255</td>
    <td align="center">0–255</td>
    <td align="center">0–255</td>
  </tr>
</table>

</p>

- The value of each octet (0 - 255) is calculated through a techinque known as IP addressing & subnetting. 
- IP addresses can change over time (dynamic allocation)
- IP Addresses can change from device to device, but cannot be active simulaneously more than once within same network. 
- IP addresses follow a set of standards known as protocols, allowing all devices to communicate using the same rules. 

--- 

### **Public vs Private IP Addresses**
- Devices can be on both private and public networks
- They can have both public and private IP Address  

**Public IP Address**
 - Assigned by your Internet Service Provider (ISP)
 - The router has the Public IP Address of the network
 - Used to identify your network on the internet
 - Must be unique globally

**Private IP Address**
 - Used inside local networks to identify devices
 - Not directly accessible from the internet
 - Can be reused across different networks

---

### **NAT (Network Address Translation)**
- It is a mechanism that allows multiple devices to share one public IP Addresses.
- It made modern home internet possible as we know it; without it, the IPv4 internet would have collapsed long time ago.
- Works very well with IPv4 because allows multiple private devices to share one single public IP by translating internal addresses to external ones. 
- It hides devices, creating a false sense of security, but is not real protection.

#### **Types of NAT** 
1. SNAT (Source NAT) 
 - Internal → External  
 - Changes the **source IP** of outgoing traffic 
 - Your private IP Address becomes the router's public IP Address. 

2. DNAT (Destination NAT) 
 - External → Internal  
 - Changes the **destination IP** of incoming traffic   
 - Used for **port forwarding** (e.g. accessing CCTV remotely)  

3. PAT (Port Address Translation)
 - Used by most home routers  
 - Allows multiple devices to share one public IP Address using **different ports**  

#### **How they work together?**  
Your home router typically uses:

- **SNAT** → when traffic goes out to the internet  
- **PAT** → to keep track of multiple devices using one public IP  
- **DNAT** → when port forwarding is configured  

Example:
1. Your PC (192.168.1.10) sends a request to a website  
2. Router applies **SNAT + PAT** → replaces your IP with public IP + assigns a port  
3. Response comes back to router  
4. Router uses the port to send data back to the correct device 

#### **How PAT works?**
- Each device is assigned a **unique port number** when sending traffic  
- Router keeps a **translation table**:

<div align="center">

<table>
  <tr>
    <th>Private IP</th>
    <th>Private Port</th>
    <th>Public IP</th>
    <th>Public Port</th>
  </tr>
  <tr>
    <td>192.168.1.10</td>
    <td>1234</td>
    <td>203.0.113.1</td>
    <td>50001</td>
  </tr>
  <tr>
    <td>192.168.1.11</td>
    <td>5678</td>
    <td>203.0.113.1</td>
    <td>50002</td>
  </tr>
</table>

</div>

This allows:
- Many devices → one public IP  
- Router to know exactly where to send responses  

#### Important Notes
⚠️ Most home and small-business routers use **PAT + SNAT by default**.    
⚠️ **DNAT** is used to allow external users to access internal network services. 
(Example: CCTV system when you are on vacation)

---

### **IPv4 and Ipv6** 

<div align="center">
<table>
  <tr>
    <th>Feature</th>
    <th>IPv4</th>
    <th>IPv6</th>
  </tr>
  <tr>
    <td>Address Size</td>
    <td>32-bit</td>
    <td>128-bit</td>
  </tr>
  <tr>
    <td>Format</td>
    <td>Decimal (e.g. 192.168.1.1)</td>
    <td>Hexadecimal (e.g. 2001:0db8::1)</td>
  </tr>
  <tr>
    <td>Total Addresses</td>
    <td>~4.3 billion</td>
    <td>~340 undecillion</td>
  </tr>
  <tr>
    <td>Structure</td>
    <td>4 octets</td>
    <td>8 groups</td>
  </tr>
  <tr>
    <td>Usage</td>
    <td>Most common today</td>
    <td>Growing adoption</td>
  </tr>
  <tr>
    <td>Security</td>
    <td>Optional</td>
    <td>Built-in (IPSec support)</td>
  </tr>
  <tr>
    <td>Limitation</td>
    <td>Limited address space</td>
    <td>Designed for scalability</td>
  </tr>
  <tr>
    <td>Routing</td>
    <td>Less efficient</td>
    <td>More efficient</td>
  </tr>
  <tr>
    <td>NAT</td>
    <td>Yes</td>
    <td>No</td>
  </tr>
</table>

</div>

---

### MAC Address (Media Access Control Address)
- A MAC address is assigned to a network interface card (NIC), which is typically built into the device motherboard. 
- It is a 12-character hexadecimal value (48 bits), written as 6 pairs separated by colons.
   - **Part A (first 3 bytes)** → Organizationally Unique Identifier (OUI), identifies the manufacturer (Intel).
   - **Part B (last 3 bytes)** → Unique identifier assigned to the specific device.
- MAC Addresses are used for LAN communication and do not travel across the internet.
   - They only exist inside the local network. 
   - Once traffic hits the router, MAC Adreesses are replaced.
- Operates at **Layer 2 (Data Link layer)** of the OSI model

<div align="center">

<strong>MAC Address</strong><br>

<table align="center">
  <tr>
    <td colspan="3" align="center"><strong>Part A (OUI)</strong></td>
    <td colspan="3" align="center"><strong>Part B (Device ID)</strong></td>
  </tr>
  <tr>
    <td align="center"><strong>a4</strong></td>
    <td align="center"><strong>c3</strong></td>
    <td align="center"><strong>f0</strong></td>
    <td align="center"><strong>85</strong></td>
    <td align="center"><strong>ac</strong></td>
    <td align="center"><strong>2d</strong></td>
  </tr>
</table>

</div>

⚠️ MAC Addresses can be facked or "spoofed" in a proccess known as **SPOOFING**.
It occurs when a network device pretends to identify as another using its MAC Address.

--- 

### ARP (Address Resolution Protocol)
- ARP associate **IP addresses to MAC addresses** within a local network (LAN)  

**How it works?**
1. Your PC wants to send data to `192.168.1.20`  
2. It checks the **ARP table** for already saved MAC addresses  
3. If unknown, it sends an **ARP Request (broadcast)** to all devices  
4. The target device replies with its MAC address (**ARP Reply**)  
5. The mapping is stored in the ARP cache for future use  

**ARP Messages**
- ARP Request → "Who has 192.168.1.20?" (broadcast)  
- ARP Reply → "192.168.1.20 is at a4:c3:f0:85:ac:2d" (unicast)  

⚠️ ARP table is stored in **cache memory** to improve performance  
⚠️ ARP only works inside a **local network (LAN)**  
- MAC addresses do not travel across networks  
⚠️ ARP can be **spoofed (ARP poisoning)**  
- Attackers can redirect traffic (Man-in-the-Middle attack)

---

## 🧪 TryHackMe Lab Example (MAC Spoofing)
- Simulated a hotel Wi-Fi network where access control was enforced based on MAC addresses  

### Tasks Performed:
- Observed how network traffic was filtered based on device identity (MAC address)  
- Identified that Bob’s device traffic was blocked, while Alice’s was allowed  
- Modified (spoofed) Bob’s MAC address to match Alice’s and bypass restrictions   

###  Key Insight:
- MAC address filtering is not a secure method of access control  
- Devices can impersonate others by spoofing MAC addresses  
- Weak network controls can be bypassed if they rely only on device identity  

## 🛠️ Practical Skills Developed  
- Understanding how devices are identified on a network  
- Differentiating between IP and MAC addressing  
- Reading IP address structures  
- Understanding how devices find each other (ARP) 
- Understanding how private networks communicate with the internet (NAT)     

## 🧰 Tools Used  
- Solent University Cybersecurity Coursework
- TryHackMe Platform  
- Basic system commands (arp, ipconfig)  

## 🔐 Security Relevance  
- IP addresses can be tracked and analysed in network logs  
- MAC addresses can be spoofed to impersonate devices  
- ARP can be exploited using **ARP spoofing (poisoning)**  
- Understanding how private networks communicate with the internet (NAT)
- Understanding addressing helps detect suspicious network activity   

## 📌 Lessons Learned  
⚠️ IP addresses can be tracked and analysed in network logs  
⚠️ MAC addresses can be spoofed to impersonate devices  
⚠️ ARP can be exploited using **ARP spoofing (poisoning)**  
⚠️ NAT allows multiple devices to share one public IP  
⚠️ Understanding addressing helps detect suspicious network activity  