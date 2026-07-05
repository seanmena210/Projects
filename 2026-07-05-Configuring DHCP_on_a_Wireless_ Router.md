# 🌐 Packet Tracer Lab: Configuring DHCP on a Wireless Router

This lab demonstrates how to build a small home network in Packet Tracer, configure DHCP on a wireless router, and verify connectivity between three PCs.

---

## 🖼️ Network Diagram (ASCII)

```
                +----------------------+
                |   Wireless Router    |
                |   IP: 192.168.5.1    |
                |   DHCP Enabled       |
                +----------+-----------+
                           | 
        ---------------------------------------------
        |                     |                     |
   +---------+           +---------+           +---------+
   |  PC0    |           |  PC1    |           |  PC2    |
   | DHCP    |           | DHCP    |           | DHCP    |
   +---------+           +---------+           +---------+
```

---

## 🧩 Part 1 — Build the Network Topology

1. Add **three Generic PCs** 🖥️🖥️🖥️  
2. Add a **Wireless Router** 📡  
3. Connect each PC to the router using **Copper Straight‑Through** cables  
4. Wait for link lights to turn **green** 🟢

---

## 🧩 Part 2 — View Default DHCP Settings

1. Open **PC0 → Desktop → IP Configuration**  
2. Select **DHCP**  
3. Record the **Default Gateway**  
4. Open **Web Browser**  
5. Enter the gateway IP  
6. Log in with:  
   - Username: **admin**  
   - Password: **admin**  
7. Scroll through **Basic Setup** to view:  
   - Router IP  
   - DHCP status  
   - Starting IP  
   - Max users  

---

## 🧩 Part 3 — Change the Router’s IP Address

1. In **Router IP Settings**, change IP to:  
   **192.168.5.1**  
2. Click **Save Settings**  
3. Browser will show an error (expected)  
4. On PC0 → IP Configuration:  
   - Click **Static**  
   - Click **DHCP** again to renew  
5. Open browser → go to **192.168.5.1**  
6. Log in again

---

## 🧩 Part 4 — Modify the DHCP Range

1. Notice DHCP pool updated to the new network  
2. Change **Starting IP** → **192.168.5.126**  
3. Change **Max Users** → **75**  
4. Save settings  
5. Renew PC0’s IP again  
6. Open **Command Prompt** → run:

```
ipconfig
```

7. Record PC0’s new IP

---

## 🧩 Part 5 — Enable DHCP on PC1 and PC2

Repeat for **PC1** and **PC2**:

1. Desktop → IP Configuration  
2. Select **DHCP**  
3. Record assigned IPs

---

## 🧩 Part 6 — Verify Connectivity

On **PC2 → Command Prompt**:

```
ipconfig
ping 192.168.5.1      // router
ping 192.168.5.126    // PC0
ping 192.168.5.127    // PC1
```

All pings should succeed ✔️

---

# 🎉 What I Learned

### ✅ **How DHCP works on a home router**  
I learned that DHCP automatically assigns IP addresses to devices so they can join the network without manual configuration.

### ✅ **How to change a router’s IP address**  
Changing the router IP forces all devices to renew their addresses and join the new subnet.

### ✅ **How DHCP pools work**  
I learned how to modify the starting IP and the number of available addresses.

### ✅ **How to verify network connectivity**  
Using `ping` and `ipconfig`, I confirmed that all devices were communicating correctly.

### ✅ **Basic network topology building**  
I practiced connecting devices, understanding link lights, and navigating Packet Tracer’s interface.

---

# 🚀 Final Result

I now have:
- A wireless router with a custom IP  
- A modified DHCP pool  
- Three PCs receiving DHCP addresses  
- Verified communication across the network  

This lab is a great foundation for CCNA studies and home networking skills.


.<img width="670" height="587" alt="Screenshot 2026-07-05 153458" src="https://github.com/user-attachments/assets/aa3dfab6-95bd-4585-9573-79165d899509" />
