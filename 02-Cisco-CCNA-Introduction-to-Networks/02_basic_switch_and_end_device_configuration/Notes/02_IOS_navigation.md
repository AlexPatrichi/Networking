# 🌐 2.2 IOS Navigation

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 02 - Basic Switch and End Device Configuration    
**Focus Area:** Cisco IOS Command Modes, CLI Navigation, and Command Structure

## 🎯 Objective 

Understand how to navigate the Cisco IOS CLI, switch between command modes, and use basic commands to configure and manage network devices.

## 🧠 2.2.1 Primary Command Modes

As a **network administrator**, using the CLI may provide more precise control and flexibility than using a GUI.

As a security feature, **Cisco IOS** separates management access into two primary command modes:

### User EXEC Mode

**User EXEC mode** provides limited access to basic monitoring commands.

- Allows users to view some device information ("view-only" mode).
- Does not allow changes to the device's configuration.
- Identified by the '>' command prompt.

**Example:** Switch>

### Privileged EXEC Mode

**Privileged EXEC mode** provides access to more advanced monitoring and management commands.

- Allows users to view detailed device information.
- Provides access to configuration modes.
- Identified by the '#' command prompt.
- Access can be protected using a password.

**Example:** Switch#

## 🧠 2.2.2 Configuration Mode and Subconfiguration Modes

### Configuration Mode
After entering **Privileged EXEC mode**, a network administrator can take a further step into **Global Configuration mode** to make changes to the device's configuration.

- **Privileged EXEC Mode (Switch#)**: Provides access to advanced management commands and configuration modes.
- **Global Configuration Mode (Switch(config)#)**: Allows administrators to modify device-wide settings.

**Example:**
Switch> enable
Switch# configure terminal
Switch(config)# hostname ABC
ABC(config)#

### Subconfiguration Modes

Global Configuration mode also provides access to **subconfiguration modes**, which allow administrators to configure specific parts of a networking device.

- **Interface Configuration Mode (Switch(config-if)#):** Configures a specific network interface.
- **Line Configuration Mode (Switch(config-line)#):** Configures console or remote access lines.

**Example:**
Switch(config)# interface fastEthernet 0/1
Switch(config-if)# description Connected-to-PC
Switch(config-if)# exit
Switch(config)#

>NOTE: The command prompt changes depending on the configuration mode you are using.
>NOTE: Certain commands are only available in specific command modes. Make sure you are in the appropriate mode before using them.

## 🧠 2.2.4 Navigate Between IOS Modes

Cisco IOS provides commands that allow administrators to navigate between different command modes.

Moving between **User EXEC Mode** and **Privileged EXEC Mode**:
- Use 'enable' to enter Privileged EXEC mode.
- Use 'disable' to return to User EXEC mode.

Moving between **Privileged EXEC Mode** and **Global Configuration Mode**:
- Use 'configure terminal' to enter Global Configuration Mode
- Use 'exit' to return to Privileged EXEC Mode

In **Global Configuration Mode** there are many different **Subconfiguration Modes**: 
- Use commands such as 'interface' or 'line' to enter specific subconfiguration modes.
- Use 'end' command or key combination 'CTRL+Z' to return directly to Privileged EXEC mode from any configuration mode.

> NOTE: 'exit' command returns to the previous mode.

## 🧠 2.2.6 A Note About Syntax Checker Activities

**Syntax Checker activities** allow students to practise entering Cisco IOS commands in a simulated CLI environment.

- Help students become familiar with IOS commands and their syntax.
- Provide feedback when commands are entered incorrectly.
- Reinforce navigation between different IOS command modes.

> NOTE: This is a safe environment to practise configuration and troubleshooting skills without damaging real equipment. 
> These activities are designed for practice and may not support every command available in a real Cisco IOS CLI.

## 📌 Key Concepts to Remember

- **User EXEC (>)**: Limited access to basic monitoring commands.
- **Privileged EXEC (#)**: Advanced management commands and access to configuration modes.
- **Global Configuration ((config)#)**: Modify device settings and access subconfiguration modes.
- **Subconfiguration modes**: Configure specific interfaces, lines, or features.
- 'enable': Enter Privileged EXEC mode.
- 'configure terminal': Enter Global Configuration mode.
- 'exit': Return to the previous mode.
- 'end' / 'Ctrl + Z': Return directly to Privileged EXEC mode from configuration modes.

> NOTE: Cisco IOS commands are mode-specific, and the command prompt indicates your current mode.

## 🔐 Security Relevance

Cisco IOS uses different command modes to help control administrative access to networking devices.

- **User EXEC mode**: Limits access to basic monitoring commands.
- **Privileged EXEC mode**: Provides access to advanced management and configuration modes.
- **Password protection**: Helps prevent unauthorised users from accessing privileged commands.
- **Access control**: Restricting administrative privileges reduces the risk of accidental or unauthorised configuration changes.