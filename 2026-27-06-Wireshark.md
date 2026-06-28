# Wireshark — Packet Analysis Practice

Today I spent time using Wireshark to deepen my understanding of how network traffic works and to strengthen my skills in packet analysis. I focused on capturing local traffic, dissecting packets layer by layer, and learning how each part of a TCP conversation behaves. Throughout the session, I was able to identify key fields, interpret protocol behavior, and see how devices communicate behind the scenes.

This hands‑on practice helped me visualize how data moves across my system, how protocols interact, and how Wireshark reveals each step of the communication process. It was a great way to build a stronger foundation in cybersecurity and become more confident analyzing real network activity.

---

## Packet Dissection Steps

### 01 — Identify the Packet Type
Understanding the protocol sets the stage for analysis.

- Check the **Protocol** column (TCP, UDP, ICMP, DNS, HTTP, ARP, etc.)
- Review the **Info** column for clues (SYN, ACK, GET, POST, Query, Reply)

This tells you the packet’s role in the conversation.

---

### 02 — Check Source and Destination
This shows who is communicating.

- Look at **Source** and **Destination IPs**
- `127.0.0.1` or `::1` = loopback (your own machine)
- External IPs = internet communication
- Ports reveal the service (e.g., 80 = HTTP, 5985 = WinRM)

---

### 03 — Expand the Packet Details
This is where the real dissection happens.

- Click the packet
- Expand **Frame**, **Ethernet**, **IP**, **TCP/UDP**, and **Application Layer**

Each layer reveals different information about the packet.

---

### 04 — Analyze the TCP/UDP Layer
This layer shows connection behavior.

- Look for flags: **SYN**, **ACK**, **FIN**, **RST**
- Check **Sequence** and **Acknowledgment numbers**
- Review **Window Size**, **MSS**, **SACK**, and other options

These explain how the connection is functioning.

---

### 05 — Inspect the Application Layer
This is where readable content appears (if unencrypted).

- **HTTP:** GET, POST, headers, payload  
- **DNS:** Queries and responses  
- **FTP:** USER, PASS, directory listings  

Encrypted traffic (HTTPS) will not show readable content.

---

### 06 — Follow the Stream
This reconstructs the entire conversation.

- Right‑click the packet → **Follow → TCP Stream**
- View the full request/response flow

This gives context beyond a single packet.

---

### 07 — Check Related Packets
Packets rarely act alone.

- Use **Packet → Show Packet in Conversation**
- Look at previous and next packets

This helps you understand what the ACK or SYN is responding to.

---

### 08 — Interpret the Packet’s Purpose
Combine all layers to understand what the packet is doing.

- Starting a connection? (**SYN**)  
- Confirming data? (**ACK**)  
- Sending content? (**HTTP GET/POST**)  
- Closing the connection? (**FIN**)  
- Performing a DNS lookup? (**Query/Response**)

---

