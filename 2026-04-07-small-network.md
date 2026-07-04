
# 🖧 Configuring Wired & Wireless Devices in Cisco Packet Tracer  
*A beginner‑friendly walkthrough for DHCP, IP verification, Wi‑Fi setup, and connectivity testing.*

In this lab, I configured both a **PC (wired)** and a **Laptop (wireless)** inside Cisco Packet Tracer to verify DHCP addressing and test connectivity to a local server (`cisco.srv`). This post breaks down each step in simple, beginner‑friendly instructions.

---

## 📌 Step 1 — Configure the PC (Wired)

### **1. Open the PC**
- Click the **PC** device.
- Go to the **Desktop** tab.
- Open **IP Configuration**.

### **2. Verify DHCP**
- Make sure **DHCP** is selected.
- If no IPv4 address appears, click **DHCP** again.
- Watch the PC request an IP address from the router’s DHCP server.

### **3. Check IP Details**
- Close IP Configuration.
- Open **Command Prompt**.
- Type:

```
ipconfig /all
```

You should see:
- IPv4 address in the **192.168.0.x** range  
- Subnet mask **255.255.255.0**  
- Default gateway **192.168.0.1**

### **4. Test Connectivity**
Ping the server:

```
ping cisco.srv
```

You should receive **four replies**, confirming network connectivity.

---

## 📌 Step 2 — Configure the Laptop (Wireless)

### **1. Swap the Network Module**
- Click the **Laptop** → go to **Physical** tab.
- **Power off** the laptop.
- Remove the **Ethernet copper module** (drag it to the left).
- Install the **Wireless WPC300N module** (drag it into the slot).
- **Power on** the laptop.

### **2. Connect to Wi‑Fi**
- Go to **Desktop** → **PC Wireless**.
- Open the **Connect** tab.
- Click **Refresh** if needed.
- Select **HomeNetwork**.
- Click **Connect**.

### **3. Test Web Connectivity**
- Open **Web Browser**.
- Navigate to:

```
cisco.srv
```

If the page loads, the laptop is successfully connected.

---

## 📊 Reflection — IP Addressing Table

After running `ipconfig` on both devices, fill out your table:

| Device | IPv4 Address | Subnet Mask | Default Gateway |
|--------|--------------|-------------|-----------------|
| **PC** | 192.168.0.x | 255.255.255.0 | 192.168.0.1 |
| **Laptop** | 192.168.0.x | 255.255.255.0 | 192.168.0.1 |

> DHCP assigns each device a **unique** IP between **192.168.0.2 – 192.168.0.254**.  
> The router acts as the **default gateway**, forwarding traffic out of the local network.

---

## 🧠 Understanding the Network (Simple Analogy)

- **Network (192.168.0.x)** = your street  
- **Host number (.2, .3, etc.)** = your house number  
- **Subnet mask** = defines where the street name ends  
- **Default gateway** = the intersection that leads to other streets (networks)

---

## ✔️ Summary

In this lab, I successfully:
- Enabled DHCP on the PC  
- Verified IP addressing  
- Pinged the local server  
- Installed a wireless NIC on the laptop  
- Connected to the HomeNetwork Wi‑Fi  
- Confirmed web access to `cisco.srv`  
- Documented IP addressing for both devices  

<img width="912" height="578" alt="Screenshot 2026-07-04 172054" src="https://github.com/user-attachments/assets/2924bcc9-7dac-4e5b-a52c-352e16450328" />
