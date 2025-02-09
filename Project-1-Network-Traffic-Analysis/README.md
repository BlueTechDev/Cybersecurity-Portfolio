# Project 1: Network Traffic Analysis and Threat Detection

## 🎯 **Objective**
Capture and analyze network traffic to identify and document potential security incidents, such as a brute-force SSH attack. This project demonstrates how network monitoring can detect early signs of malicious activity.

---

## 🛠 **Tools**
- **Wireshark**: For analyzing captured network traffic
- **tcpdump**: For capturing traffic in real-time on a target system
- **Linux (Ubuntu Server, Kali Linux)**: Virtual machines for attack and defense setup

---

## 🖥 **Setup and Environment**
1. **VM 1:** Ubuntu Server (Target machine)
   - Install and configure an SSH server (`sudo apt install openssh-server`).
   - Ensure it is reachable over the network.
   
2. **VM 2:** Kali Linux (Attacker machine)
   - Use tools like `Hydra` to simulate a brute-force SSH attack:
     ```bash
     hydra -l admin -P /usr/share/wordlists/rockyou.txt ssh://<target-ip>
     ```

3. **Capture traffic:**  
   On the Ubuntu server, run `tcpdump` to capture traffic:
   ```bash
   sudo tcpdump -i eth0 -w traffic_capture.pcap
