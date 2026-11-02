# 🌐 2.4 Basic Device Configuration

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 02 - Basic Switch and End Device Configuration    
**Focus Area:**  Device Hostnames, Password Security, Password Configuration, Encryption, and Login Banners

## 🎯 Objective 

Understand how to perform basic Cisco IOS device configuration, including assigning hostnames, securing administrative access with passwords, protecting stored passwords, and configuring security warning banners.


## 🧠 2.4.1 Device Names

Every networking device should have a unique and descriptive hostname to help administrators identify and manage it.

A hostname should:

- Be easy to recognise and identify.
- Start with a letter.
- Contain no spaces.
- Use letters, numbers, and hyphens.
- Be fewer than 64 characters.

An organisation should choose a consistent naming convention that makes network devices easy to identify.  
Network documentation should explain the naming convention so that additional devices can be named consistently.

**Example:** 
```Text
Sw-Floor-1
Sw-Floor-2
Sw-Floor-3
```

**Cli Command Example:**
```text
Switch> enable
Switch# configure terminal
Switch(config)# hostname Sw-Floor-1
Sw-Floor-1(config)#
```
> NOTE: Changing the hostname also changes the name displayed in the Cisco IOS command prompt.

## 🧠 2.4.2 Password Guidelines

**Strong passwords** help prevent unauthorised access to networking devices.

Networking devices, including home wireless routers, should always have passwords configured to limit administrative access.

Recommended password practices include:

- Use passwords with at least 8 characters (longer passwords are preferable).
- Combine uppercase and lowercase letters, numbers, and special characters.
- Avoid common words and easily guessed information.
- Use different passwords for different access methods.
- Protect passwords and avoid sharing them.

> NOTE: Passwords are case-sensitive in Cisco IOS.

## 🧠 2.4.3 Configure Passwords

Cisco IOS allows administrators to configure passwords to protect different levels of device access.

### Secure User EXEC Mode

To protect local access to User EXEC mode, administrators can configure a console password.

**Secure Console Access**
```text
Switch(config)# line console 0                    — Enters console line configuration mode.
Switch(config-line)# password xxxxxxxxxxxxxxx     — Sets the console password.
Switch(config-line)# login                        — Enables password authentication.
Switch(config-line)# exit                         — Returns to Global Configuration mode.
```

### Secure Privileged EXEC Mode

We can add another layer of security to restrict access to Privileged EXEC mode, which provides advanced management commands and access to device configuration.

The `enable` secret command sets a password that users must enter before accessing Privileged EXEC mode.

```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# enable secret xxxxxxxxx
Sw-Floor-1(config)# exit
Sw-Floor-1#
```

### Secure Remote Access (VTY Lines)

VTY (Virtual Teletype) lines are used for remote CLI access, such as SSH or Telnet.
Many Cisco switches support up to 16 VTY lines, numbered from 0 to 15.

```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line vty 0 15
Sw-Floor-1(config-line)# password xxxxxxxxx
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

> NOTE: The number of available VTY lines depends on the Cisco device and IOS version.
> SSH is preferred over Telnet because it encrypts network communication.

## 🧠 2.4.4 Encrypt Passwords

Cisco IOS can protect passwords stored in the device configuration.
The service password-encryption command provides weak encryption for all plaintext passwords.

**Example:**
```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# service password-encryption
Sw-Floor-1(config)#
```
**To verify encrypted passwords, use:**
```text
Sw-Floor-1(config-line)# end
Sw-Floor-1# show running-config
```
> NOTE: service password-encryption uses weak, reversible protection for traditional line passwords. It should not be considered a substitute for strong passwords and secure administrative access.

## 🧠 2.4.5 Banner Messages

Cisco IOS allows administrators to display a message when someone connects to a networking device.

A **Message of the Day (MOTD) banner** is commonly used to warn users that access is restricted to authorised personnel.

**Example:**
```text
Switch(config)# banner motd #Unauthorized access is prohibited!#
```

> NOTE: Login banners should avoid revealing sensitive information about the device or network.

## 📌 Key Concepts to Remember
- Device Names: Use unique and descriptive hostnames to identify network devices.
- Password Security: Strong passwords help prevent unauthorised access.
- User EXEC Access: Console and VTY passwords protect access to the device.
- Privileged EXEC Access: The enable secret command protects advanced administrative access.
- Password Encryption: The service password-encryption command provides weak encryption for supported plaintext passwords.
- Banner Messages: Display warnings to users attempting to access the device.

## 🔐 Security Relevance

- Basic device configuration is an important first step in securing Cisco networking equipment.
- Unique hostnames: Help administrators identify devices and avoid configuration mistakes.
- Strong passwords: Reduce the risk of unauthorised access.
- Privileged access protection: Restricts access to sensitive management and configuration commands.
- Password protection: Reduces accidental exposure of passwords stored in configuration files.
- Login banners: Warn users that access is restricted to authorised personnel.

> NOTE: Password protection alone is not enough to secure a networking device. Secure management protocols, access controls, and regular configuration reviews are also important.