# Network Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: VPN   

## 🎯 Objective
- Understand what a VPN is and how it secures communication  
- Learn how VPNs protect privacy and data  
- Identify common VPN technologies and their differences  

## 🧠 Core Concepts Learned 
## Virtual Private Network (VPN)
- A VPN is a service that creates a secure, encrypted tunnel between a device and another network over the Internet  
- The VPN encrypts traffic before it leaves the device
- It allows data to be transmitted privately, as if the device were directly connected to that network  

### How It Works
**Normal Connection**
- Device → ISP → Internet → Website  

**VPN Connection**
- Device → Encrypted Tunnel → VPN Server → Internet → Website  

⚠️ The VPN server acts as an intermediary, hiding the user’s real IP address 

### Benefits
- **Privacy:** Hides your real IP address  
- **Encryption:** Protects data from interception  
- **Location masking:** Allows access from different geographic regions  

### VPN Technologies
**PPP (Point-to-Point Protocol)**
- A protocol used to establish direct connections between two nodes  
- Provides basic authentication and data encapsulation  
- Does not provide strong encryption by itself  

**PPTP (Point-to-Point Tunneling Protocol)**
- One of the earliest VPN protocols  
- Uses PPP to create a tunnel over the Internet  
- Fast but uses weak encryption → **not recommended for secure use**  

**IPSec (Internet Protocol Security)**
- Is using protocols that encrypts and authenticates IP traffic  
- More complex to configure but provides strong security
- Is widely used in modern VPNs  
- Can operate in:
  - Transport mode  
  - Tunnel mode  

### VPN vs Proxy
- VPN encrypts all traffic from the device  
- Proxy only forwards specific application traffic  
- VPN provides stronger security and privacy  

### Trust in VPN Providers
- While VPNs encrypt traffic, the VPN provider can still see user activity  
- Users must trust the provider not to log or misuse data  

## 🛠️ Practical Skills Developed
- Understanding how VPNs protect network communication  
- Recognising different VPN protocols and their strengths  
- Identifying when and why VPNs are used  

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  

## 🔐 Security Relevance
- Protects data on unsecured networks (public Wi-Fi)  
- Prevents eavesdropping and man-in-the-middle attacks  
- Weak protocols (PPTP) can expose sensitive data  
- VPNs do not provide full anonymity — trust in the provider is required 

## 📌 Lessons Learned  
⚠️ VPNs encrypt traffic but do not make users completely anonymous  
⚠️ Not all VPN protocols are secure — some are outdated  
⚠️ VPNs are essential for secure remote access and privacy      