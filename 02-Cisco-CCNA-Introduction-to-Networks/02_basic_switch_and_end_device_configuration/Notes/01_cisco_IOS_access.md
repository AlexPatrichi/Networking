# 🌐 2.1 Cisco IOS Access

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 02 - Basic Switch and End Device Configuration    
**Focus Area:** Operating Systems, GUI, CLI, Cisco IOS Access Methods, and Terminal Emulation

## 🎯 Objective 

Understand how operating systems work on networking devices and how to access Cisco IOS using different connection methods.


## 🧠 2.0 Introduction

Out of the box, **switches and end devices** come with default configuration, but they need additional settings to operate correctly within a particular network.  

> Network administrators configure devices according to the network's requirements.

## 🧠 2.1.1 Operating Systems

An **Operating System (OS)** is software that manages a device's hardware and allows users to interact with it.

An operating system has two important components:
- **Kernel:** The part of the OS that interacts directly with the computer's hardware.
- **Shell:** The part of the OS that allows users and applications to interact with the system.

Users can interact with the operating system shell through two types of interfaces:
- **Command-Line Interface (CLI):** Allows users to interact with the system by typing commands.
- **Graphical User Interface (GUI):** Allows users to interact with the system using windows, icons, and menus.

## 🧠 2.1.2 GUI

A **Graphical User Interface (GUI)** allows users to interact with an operating system using visual elements such as windows, icons, and menus.

- Easier to use for many everyday tasks.
- Requires less knowledge of the underlying command structure that controls the system.
- Common on computers and smartphones.
- Some networking devices also provide web-based graphical interfaces.

**Example:** A user opens Windows Settings to configure their computer's network connection.

> NOTE: GUIs may not provide all the features available through the CLI. For this reason, network devices are often configured and managed using a CLI.

### Cisco IOS 

Cisco networking devices use operating systems such as **Cisco IOS (Internetwork Operating System)**.

Cisco IOS allows network administrators to configure, monitor, and troubleshoot supported Cisco devices.

Different Cisco routers and switches may use different versions of Cisco IOS, depending on the device model and supported features.

> NOTE: The operating system on a home router is commonly referred to as **firmware**. Home routers are typically configured using a web browser-based GUI.

> **Firmware** is a broader term for software embedded in a device, which can include its operating system.

## 🧠 2.1.3 Purpose of an OS

An **operating system** allows users to interact with a device, run programs, and manage its hardware resources.

A CLI-based network operating system, such as Cisco IOS on a router or switch, allows a network technician to:

- Use a keyboard to enter text-based commands.
- Run commands to configure, monitor, and troubleshoot network devices.
- View command output on a screen.

**Example:** A network administrator enters commands in the Cisco IOS CLI to configure a switch's hostname and network settings.

> The **shell** handles user interaction, while the **kernel** manages hardware resources.

## 🧠 2.1.4 Access Methods

### NOTE: In-band vs Out-of-band Management
- **In-band:** Management access through the normal network connection.
Example: A laptop connects to a Cisco switch over the network using its IP address.
- **Out-of-band:** Management access through a separate connection, independent of the normal network.
Example: A laptop connects directly to a Cisco switch using a console cable.

Cisco networking devices can be accessed and configured using different methods:

### Console

A **console connection** provides direct local access to a networking device.

Provides **out-of-band access** via a dedicated management channel that is used for device maintenance purposes only. 

- Uses a console cable and terminal emulation software.
- Does not require an IP address or an active network connection.
- Commonly used for initial configuration and troubleshooting.

**Example:** A network administrator connects a laptop directly to a Cisco switch using a console cable to perform its initial configuration.

### SSH (Secure Shell)

**SSH** is an **in-band** method that provides secure remote access to a networking device over a network.

- Encrypts communication between the administrator and the device.
- Requires network connectivity and appropriate device configuration.
- Recommended for remote CLI management.

**Example:** An administrator uses SSH to securely configure a switch located in another building.

### Telnet

**Telnet** provides remote CLI access over a network but does not encrypt communication.

- Requires network connectivity.
- Sends data, including credentials, in plaintext.
- Not recommended for managing devices on untrusted networks.

**Example:** An administrator accesses an older network device using Telnet in a controlled lab environment.

NOTE: Some Cisco routers support a legacy Auxiliary (AUX) port, which allows remote CLI access through a telephone connection using a modem.  
Like the console port, the AUX port provides out-of-band management and does not require an active IP network connection.

## 🧠 2.1.5 Terminal Emulation Programs

A **terminal emulation program** allows a computer to interact with a networking device's CLI.

Common examples include:

- **PuTTY:** Supports SSH, Telnet, and serial console connections.
- **Tera Term:** Supports serial and remote terminal connections.
- **SecureCRT:** Supports secure remote access and terminal sessions.

**Example:** A network administrator uses PuTTY on a laptop to connect to a Cisco switch through its console port and configure the device.

> Cisco Packet Tracer also provides a terminal interface for practising Cisco IOS commands.

## 📌 Key Concepts to Remember

- **Cisco IOS:** Operating system used to configure and manage supported Cisco networking devices.
- **GUI:** Allows users to interact with devices using graphical elements.
- **CLI:** Allows users to interact with devices by entering commands.
- **Shell:** Provides the interface between the user and the operating system.
- **Kernel:** Manages hardware and system resources.
- **Console:** Direct local access without requiring an IP address.
- **SSH:** Secure, encrypted remote CLI access.
- **Telnet:** Unencrypted remote CLI access.
- **Terminal Emulator:** Software used to establish CLI sessions with networking devices.

## 🔐 Security Relevance

- Protect console access because it provides direct device management.
- Use **SSH instead of Telnet** for secure remote administration.
- Restrict administrative access to authorised users.
- Use strong authentication credentials.
- Disable unnecessary remote management services.

**Key Takeaway:** Cisco IOS allows administrators to configure, monitor, and troubleshoot networking devices. Understanding GUI, CLI, console, SSH, and Telnet access is essential for managing Cisco networks securely.