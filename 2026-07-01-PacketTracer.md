## Home Network Topology (Packet Tracer)

This is a simple home network simulation built in Cisco Packet Tracer.

<img width="636" height="561" alt="Screenshot 2026-07-01 201224" src="https://github.com/user-attachments/assets/5f0e4778-57f6-4c10-864c-8154a29a0f4e" />


## Overview
This Packet Tracer lab demonstrates a simple home network environment integrating traditional computing devices with an IoT component. The topology models how everyday home networks operate, showing how multiple wireless clients connect to a single access point for internet access, local communication, and device management.
This scenario is ideal for beginners learning networking fundamentals, cybersecurity students practicing home‑lab analysis, and OSINT learners exploring how IoT devices appear inside network diagrams.

## Device Roles
### HomeRouter‑PT (AC Wireless Router)  
Serves as the central wireless access point and DHCP server. It provides IP addressing, wireless connectivity, and basic routing for all connected devices.

### PC‑PT (PC0)  
A wired/wireless client device representing a standard desktop computer. Used for general network testing, pinging, configuration validation, and basic endpoint behavior.

### Laptop‑PT (Laptop0)  
A mobile wireless client connected via Wi‑Fi. Useful for demonstrating roaming behavior, wireless security settings, and endpoint diversity within a home network.

### Webcam IoT (IoT0)  
An IoT device connected wirelessly to the router. Represents smart‑home equipment such as security cameras. This device is important for understanding IoT vulnerabilities, unsecured traffic, and how IoT devices appear in network mapping.

## Wireless Link Explanation
All devices communicate with the HomeRouter‑PT using wireless connections:

### Solid green wireless links indicate active, stable Wi‑Fi associations.

### Dashed wireless links represent devices that are connected but may be using different wireless modes or lower signal strength.

The router acts as the central hub, broadcasting SSID information and managing all wireless associations.

This setup mirrors real‑world home networks where multiple devices share the same access point, each with different signal strengths, capabilities, and security requirements.

## Use‑Cases
### Home Lab Practice
This topology is perfect for beginners building a home networking lab. It allows you to practice:

DHCP behavior

Wireless configuration

Basic routing

Device connectivity testing

### IoT Security Training
The IoT webcam introduces realistic security considerations:

Weak default passwords

Unencrypted traffic

Device fingerprinting

Attack surface mapping

Students can simulate how attackers discover and exploit IoT devices inside home networks.

### OSINT (Open‑Source Intelligence) Practice
Network diagrams like this help OSINT learners understand:

How IoT devices appear in technical documentation

How home networks are structured

How to interpret network topology screenshots found online

How to identify device roles and potential vulnerabilities from visual evidence alone
