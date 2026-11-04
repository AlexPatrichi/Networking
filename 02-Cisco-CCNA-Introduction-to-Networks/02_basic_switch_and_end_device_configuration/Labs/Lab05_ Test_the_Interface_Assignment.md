# Lab 05: Packet Tracer - Test the Interface Assignment

**Cisco Networking Academy | Solent University**

Course: CCNA: Introduction to Networks  
Platform: Cisco Packet Tracer  
Focus Area: Console Connectivity, Interface Verification, Switch Management Interfaces & Troubleshooting

## 🎯 Objective

- Establish console access to Cisco switches.
- Examine the IP address and operational status of switch interfaces.
- Identify and enable an administratively disabled management interface.
- Configure an IPv4 address on a second switch management interface.
- Verify interface assignments and operational status using Cisco IOS commands.

## 🧪 Lab Implementation

### Part 1: Establish Console Access to the Switches

Connected to the switches through their console ports to access the Cisco IOS Command-Line Interface (CLI).

**1. Establish a Console Connection**

Connected the PC's RS-232 port to the switch's Console port using a rollover console cable.

Opened **Desktop → Terminal** on the PC and used the default connection settings.

**2. Access the Cisco IOS CLI**

Pressed Enter to access the switch CLI and entered Privileged EXEC mode.

```text
Switch> enable
Switch#
```

- `enable` — Enters Privileged EXEC mode.
- `Switch#` — Confirms that Privileged EXEC mode is active.

Repeated the console access process on the second switch.

> **Note:** Console connections allow administrators to access and troubleshoot Cisco devices without requiring an IP address or an active network connection.

---

### Part 2: Verify the Existing Interface Configuration

Examined the existing configuration on the first switch to identify its assigned IP address and interface status.

```text
Switch# show ip interface brief
```

- `show ip interface brief` — Displays the IP addresses and operational status of the switch interfaces.

The VLAN 1 management interface already had an IP address assigned, but it was not operational.

**Understanding Interface Status**

| Status | Protocol | Meaning |
|---|---|---|
| administratively down | down | The interface is disabled by configuration. |
| up | down | The interface is enabled, but its line protocol is down. |
| up | up | The interface and line protocol are operational. |

> **Note:** Assigning an IP address does not automatically make an interface operational. Its administrative state and line protocol must also be operational for connectivity to work.

---

### Part 3: Enable the Switch Management Interface

Entered interface configuration mode and used `no shutdown` to enable the VLAN 1 management interface.

```text
Switch# configure terminal
Switch(config)# interface vlan 1
Switch(config-if)# no shutdown
Switch(config-if)# end
```

- `configure terminal` — Enters Global Configuration mode.
- `interface vlan 1` — Selects the VLAN 1 Switch Virtual Interface (SVI).
- `no shutdown` — Enables an administratively disabled interface.
- `end` — Returns directly to Privileged EXEC mode.

**Verify the Interface Status**

```text
Switch# show ip interface brief
```

Checked the VLAN 1 interface again to verify whether its status changed after enabling it.

> **Note:** The `no shutdown` command removes the administrative shutdown. For a VLAN 1 SVI to become `up/up`, VLAN 1 must also be active and have an operational switch port associated with it.

---

### Part 4: Configure the Second Switch Management Interface

On the second switch, configured the VLAN 1 management interface by assigning an IPv4 address and subnet mask, then enabling the interface.

```text
Switch> enable
Switch# configure terminal
Switch(config)# interface vlan 1
Switch(config-if)# ip address <IPv4-address> <subnet-mask>
Switch(config-if)# no shutdown
Switch(config-if)# end
```

- `interface vlan 1` — Enters VLAN 1 interface configuration mode.
- `ip address` — Assigns an IPv4 address and subnet mask to the management interface.
- `no shutdown` — Administratively enables the interface.

**Verify the Configuration**

```text
Switch# show ip interface brief
Switch# show running-config
```

- `show ip interface brief` — Verifies the assigned IP address and interface status.
- `show running-config` — Displays the active configuration, including the VLAN 1 interface settings.

> **Note:** A Layer 2 switch does not require an IP address to forward Ethernet frames. The management IP address allows the switch itself to communicate over IP for management and troubleshooting.

---

### Part 5: Verify Interface Assignment and Status

Compared the management interface configuration and status on both switches.

```text
Switch# show ip interface brief
```

**Verification Summary**

| Switch | Initial Condition | Configuration Action | Verification |
|---|---|---|---|
| Switch 1 | IP address already assigned; interface down | `no shutdown` | Check interface status |
| Switch 2 | Management interface required configuration | `ip address` and `no shutdown` | Check IP address and interface status |

The verification demonstrates the difference between assigning an IP address and enabling an interface.

An interface must be correctly configured and operational before it can provide IP connectivity.

## 🧰 Tools Used

- Cisco Packet Tracer
- Cisco IOS Command-Line Interface (CLI)
- Cisco Switches
- PC
- Rollover Console Cable
- Packet Tracer Terminal Application

## 📌 Lessons Learned

- Established console access to Cisco switches using a terminal application.
- Examined switch interface assignments and operational status.
- Learned that an interface can have an IP address configured but still be down.
- Used `no shutdown` to enable an administratively disabled interface.
- Configured a VLAN 1 management interface with an IPv4 address and subnet mask.
- Verified interface configuration using `show ip interface brief` and `show running-config`.
- Understood the difference between administrative interface status and line protocol status.

## 🔐 Security Relevance

- Console access allows administrators to troubleshoot devices even when network connectivity is unavailable.
- Physical access to console ports should be restricted to authorized personnel.
- Administratively disabling unused interfaces can reduce unnecessary network access.
- Switch management interfaces should be protected against unauthorized access.
- Interface verification helps identify configuration problems that affect network availability.