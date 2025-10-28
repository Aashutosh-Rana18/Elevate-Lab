# 🔥 Firewall Configuration (UFW)

## Objective
Configure and test basic firewall rules using UFW (Uncomplicated Firewall) in Linux.

## Overview
A firewall is a network security tool that filters incoming and outgoing traffic based on predefined rules.  
UFW provides a simplified interface to manage iptables rules on Linux systems.

## Steps

### 1️⃣ Check if UFW is installed and enabled
```bash
sudo ufw status
sudo ufw enable
```

### 2️⃣ List current firewall rules
```bash
sudo ufw status numbered
```
Shows existing rules with numbers for easy management.

### 3️⃣ Block inbound traffic on a specific port (Telnet - port 23)
```bash
sudo ufw deny 23
```
🛑 Blocks all incoming connections on port 23 (Telnet).

### 4️⃣ Test the rule
```bash
telnet localhost 23
```
Expected result: `Connection refused` → The rule is working.

### 5️⃣ Allow SSH (port 22)
```bash
sudo ufw allow 22
```
✅ Ensures SSH access remains available while testing firewall rules.

### 6️⃣ Remove the test block rule
```bash
sudo ufw delete deny 23
```
Removes the Telnet block rule after testing.

### 7️⃣ List rules again to confirm
```bash
sudo ufw status
```
Displays all active rules to verify configuration.

## Summary
A firewall filters network traffic based on predefined rules.

- **Inbound filtering:** Controls which external connections can access your system.  
- **Outbound filtering:** Controls what your system can connect to outside.  
- **UFW:** A user-friendly interface for iptables that simplifies rule management.

**Examples:**
- `allow 22` → allows SSH traffic  
- `deny 23` → blocks Telnet connections  

## 🧑‍💻 Author
**Aashutosh Rana**
