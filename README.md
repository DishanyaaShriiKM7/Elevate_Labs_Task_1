
# Elevate Labs Task 1 – Network Scanning & Packet Analysis

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Internship-blue)

## 📝 Overview
This repository contains my work for **Elevate Labs Task 1** as part of my **Cybersecurity Internship**.  
The main goal was to **perform network scanning using Nmap** and **analyze TCP traffic with Wireshark** to identify open ports, running services, and understand TCP handshakes.

---

## 🎯 Objectives
- Discover active hosts in the local network.  
- Identify open ports and running services.  
- Capture and analyze TCP handshake packets.  
- Understand potential security risks from open ports.  
- Document findings professionally.

---

## 🛠 Tools Used
- **Nmap** – Network scanning and port discovery.  
- **Wireshark** – Packet capture and TCP traffic analysis.  
- **Linux Terminal** – Command-line operations and file management.

---

## 🔍 Tasks Performed

### 1️⃣ Identifying Local Network
- Determined my machine’s local IP range (e.g., `192.168.1.0/24`) to scan the network.

### 2️⃣ Network Scanning
- Performed a **TCP SYN scan** using Nmap:
```bash
nmap -sS 192.168.1.0/24
```
- Collected responsive IP addresses and discovered open ports.

### 3️⃣ Packet Capture with Wireshark
- Captured packets while performing the Nmap scan.  
- Applied filters to inspect TCP handshake flags:
  - `tcp.flags.syn == 1 and tcp.flags.ack == 0` → Client SYN packets  
  - `tcp.flags.syn == 1 and tcp.flags.ack == 1` → Server SYN-ACK packets  
  - `tcp.flags.syn == 0 and tcp.flags.ack == 1` → Client ACK packets  
- Observed how Nmap performs a SYN scan without completing the full handshake.

### 4️⃣ Service Identification & Security Assessment
- Researched common services running on detected ports (e.g., HTTP, SSH).  
- Noted potential risks of leaving ports open in a network.

### 5️⃣ Documentation
- Saved Nmap scan results: `nmap_scan.txt`  
- Saved Wireshark packet capture: `wireshark_capture.pcap`  
- Wrote detailed observations: `notes.md`

---

## 📂 Repository Structure
```
Elevate_Labs_Task_1/
├── nmap_scan.txt          # Output of Nmap scan
├── wireshark_capture.pcap # Packet capture file
├── notes.md               # Observations and summary
└── README.md              # This file
```

---

## 🧠 Key Learnings
- Practical understanding of **TCP SYN scanning** and open port enumeration.  
- Ability to **analyze TCP handshake** and network traffic in Wireshark.  
- Awareness of **network services** and potential security vulnerabilities.  
- Developed **professional documentation skills** for cybersecurity tasks.

---

## 📌 References
- [Nmap Official Documentation](https://nmap.org/book/man.html)  
- [Wireshark Official Documentation](https://www.wireshark.org/docs/)  
- TCP/IP Networking Concepts

---
## 📌 contact
- [Mail](dishanyaaofficial@gmail.com)
