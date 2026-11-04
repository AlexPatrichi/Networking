# Lab 06: Packet Tracer - Test End-to-End Connectivity

**Cisco Networking Academy | Solent University**

Course: CCNA: Introduction to Networks  
Platform: Cisco Packet Tracer  
Focus Area: End-to-End Connectivity, ICMP, Ping Testing & Network Troubleshooting

## 🎯 Objective

- Use the `ping` command to test connectivity between network devices.
- Verify connectivity between a PC and a switch.
- Test communication between two PCs.
- Understand the importance of testing connectivity in both directions.
- Identify possible connectivity problems using ping results.

## 🧪 Lab Implementation

### Part 1: Test Connectivity Between a PC and a Switch

Opened **Desktop → Command Prompt** on the PC to test connectivity to the switch's management IP address.

```text
PC> ping <switch-ip-address>
```

- `ping` — Sends ICMP Echo Request messages to test whether a destination can respond over the IP network.
- `<switch-ip-address>` — The management IP address assigned to the switch.

**Verify the Ping Result**

A successful ping indicates that the destination responded to the ICMP Echo Request.

> **Note:** The switch must have a working management IP interface to respond to a ping directed at that address.

---

### Part 2: Test End-to-End Connectivity Between PCs

Used the `ping` command to test communication between two PCs.

**1. Test Connectivity from PC1 to PC2**

Opened Command Prompt on PC1 and pinged PC2.

```text
PC1> ping <PC2-ip-address>
```

**2. Test Connectivity from PC2 to PC1**

Repeated the test in the opposite direction.

```text
PC2> ping <PC1-ip-address>
```

**Why Test Both Directions?**

Testing connectivity in both directions helps identify problems that may affect communication differently depending on where the traffic originates.

A successful ping from PC1 to PC2 confirms that the ICMP request reached PC2 and its reply returned to PC1. However, it does not guarantee that a new ping initiated from PC2 to PC1 will also succeed.

> **Note:** In real networks, security rules, routing configurations, or host firewalls may cause communication to behave differently depending on the direction of the connection.

---

### Part 3: Verify and Troubleshoot Connectivity

Compared the ping results to determine whether communication was successful.

**Connectivity Verification**

| Test | Source | Destination | Expected Result |
|---|---|---|---|
| 1 | PC1 | Switch | Successful |
| 2 | PC1 | PC2 | Successful |
| 3 | PC2 | PC1 | Successful |

**Understanding Ping Results**

- **Reply from** — The destination responded to the ICMP Echo Request.
- **Request timed out** — No ICMP Echo Reply was received within the allowed time.
- **Destination host unreachable** — A device reports that the destination cannot be reached.

If a ping fails, check the IP addresses, subnet masks, network connections, interface status, and any relevant routing or firewall settings.

> **Note:** A failed ping does not always mean the destination is offline. ICMP traffic may be blocked by a firewall or security policy.

## 🧰 Tools Used

- Cisco Packet Tracer
- Cisco Switch
- PCs
- Packet Tracer Command Prompt
- ICMP (Internet Control Message Protocol)
- `ping` Command

## 📌 Lessons Learned

- Used `ping` to verify connectivity between a PC and a switch.
- Tested end-to-end communication between two PCs.
- Learned why connectivity should be checked in both directions.
- Understood how ICMP Echo Requests and Echo Replies are used by `ping`.
- Identified common ping results and their meaning.
- Learned that network troubleshooting should verify communication rather than assume connectivity is working.

## 🔐 Security Relevance

- Ping testing helps administrators identify connectivity problems that affect network availability.
- Firewalls and access control lists (ACLs) may restrict ICMP traffic.
- Bidirectional testing can help identify differences in network security policies.
- ICMP testing should be performed only on networks and devices where testing is authorized.