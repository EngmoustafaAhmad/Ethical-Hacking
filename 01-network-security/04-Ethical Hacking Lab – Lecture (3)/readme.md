# 🛡️ Ethical Hacking Lab – Lecture (3)
## 📘 Network Scanning (2025–2026)

---

# 📌 Table of Contents
- Network Scanning Concepts
- Networking Protocols Revision
- Host Discovery Techniques
- Network Scanning Tools
- Practical Commands (Nmap, hping3, Metasploit)

---

# 1. 🔍 Network Scanning Concepts

Network scanning refers to probing a network to gather information such as:
- IP addresses
- Active devices (live hosts)
- Open ports
- Running services

## 🎯 Objectives:
- Discover live hosts
- Identify IP addresses in a network
- Detect open ports & services
- Find possible vulnerabilities

---

# 2. 🌐 Overview of Networking Protocols

## 🔗 TCP (Transmission Control Protocol)
TCP ensures reliable communication between devices.

### TCP Flags:
- **URG** → urgent data
- **PSH** → push data immediately
- **ACK** → acknowledgment
- **SYN** → start connection
- **FIN** → close connection
- **RST** → reset connection

---

## 🤝 3-Way Handshake (TCP Connection)

1. Client → SYN  
2. Server → SYN + ACK  
3. Client → ACK → connection established  

---

## 🔚 Connection Termination
- Uses FIN + ACK sequence to close connections safely

---

# 3. 🌍 Networking Concepts

## 📡 Network Segment
A group of computers connected via switch or WiFi.

## 🌐 Subnet
A smaller network inside a larger network.

### Examples:
- `/24` → ~254 hosts
- `/16` → ~65,000 hosts

## 🔥 Firewall
Controls and filters network traffic based on security rules.

---

# 4. 📡 Networking Protocols Used in Scanning

## 🧭 ARP (Link Layer)
- Resolves IP → MAC address
- Works only in local networks (LAN)

## 📶 ICMP (Network Layer)
Used for ping operations:
- Echo Request (Type 8)
- Echo Reply (Type 0)

## 🚦 TCP / UDP (Transport Layer)
Used for port scanning and service detection.

---

# 5. 🕵️ Host Discovery Techniques

## 1. ARP Ping Scan
- Works in LAN only
- Very fast and accurate

---

## 2. ICMP Ping Scan
- Sends echo requests to detect live hosts
- May be blocked by firewalls

### Types:
- Echo Ping
- Timestamp Ping
- Address Mask Ping
- Ping Sweep (range scan)

---

## 3. UDP Ping Scan
- Sends UDP packets
- ICMP “port unreachable” indicates host is alive

---

## 4. TCP Ping Scan
### Types:
- SYN Ping → checks open ports
- ACK Ping → bypass firewall detection

---

## 5. IP Protocol Scan
- Uses multiple protocols (TCP/UDP/ICMP)
- Detects live systems

---

# 6. 🛠️ Network Scanning Tools

## 🔧 1. Nmap

Used for:
- Host discovery
- Port scanning
- OS detection
- Service detection

### Full Scan Example:
```bash
nmap -p 1-65535 -T4 -A -v 10.10.1.11
