# Task 5-Capture-and-Analyze-Network-Traffic-Using-Wireshark

#
---

## 🧰 TASK STEPS:

### ✅ Step-by-Step:

1. **Install Wireshark**
    - Download from [https://www.wireshark.org](https://www.wireshark.org/) or Use Kali Linux Default wireshark Tool
    - Install both **Wireshark** and **TShark** (comes with WinPcap/Npcap on Windows)
2. **Start Capturing Traffic**
    - Open Wireshark
    - Select your **active network interface** (e.g., Wi-Fi or Ethernet)
    - Click the **shark fin icon ▶️** to start capturing
3. **Generate Network Traffic**
    - Open a browser and visit any HTTP site (e.g., [http://example.com](http://example.com/))
    - Or open CMD/PowerShell and run:
        
        ```bash
        ping google.com
        
        ```
        
4. **Stop Capture**
    - After about 1 minute, click the **stop button ⏹️**
5. **Filter by Protocol**
    - Use display filters like:
        - `tcp`
        - `udp`
        - `http`
        - `dns`
        - `icmp`
6. **Identify at Least 3 Protocols**
    - Example: TCP, DNS, ICMP
7. **Export as .pcap File**
    - Go to **File > Save As**
    - Choose location and save as `.pcap` or `.pcapng`
8. **Summarize Findings**
    - Write a short report of what you observed

---

## 📄 Sample Summary Report

### 📌 Title: Network Traffic Analysis Using Wireshark

**Date:** [Insert Date]

**Analyst:** [Your Name]

### 🔍 Overview:

This report presents an analysis of captured network traffic using **Wireshark**, focusing on identifying common protocols in use during normal internet browsing and basic connectivity tests.

### 🛠️ Tools Used:

- **Wireshark v4.x.x**
- **Windows 10 / macOS / Linux** (based on your system)
- Active Internet Connection

### 📦 Protocols Identified:

| Protocol | Description | Observations |
| --- | --- | --- |
| **HTTP** | Unencrypted web traffic | Observed GET and HTTP/1.1 responses when visiting websites |
| **DNS** | Domain Name Resolution | Multiple queries to resolve domain names (e.g., [google.com](http://google.com/)) |
| **ICMP** | Ping requests/responses | Seen after running `ping google.com` |
| **TCP** | Reliable connection-oriented communication | Seen in all HTTP and DNS traffic |
| **UDP** | Fast, connectionless transport | Used for DNS lookups |

### 📁 Exported File:

- **capture.pcapng** – Contains all packets captured during this session

### 🧠 Key Takeaways:

- Different types of traffic (web, name resolution, ping) are distinguishable via protocol.
- Filtering helps isolate specific traffic for troubleshooting or security analysis.
- Wireshark provides visibility into how data moves across networks.

---

## ❓ Interview Questions & Answers

### 1. **What is Wireshark used for?**

> Wireshark is a network protocol analyzer that captures and displays live network traffic, allowing users to inspect packet details for troubleshooting, security analysis, and learning network behavior.
> 

---

### 2. **What is a packet?**

> A packet is a unit of data sent over a network. It includes headers (metadata like source, destination, protocol) and payload (actual data being transmitted).
> 

---

### 3. **How do you filter packets in Wireshark?**

> In Wireshark, use the display filter bar at the top to enter filters such as:
> 
> - `tcp`
> - `http`
> - `ip.addr == 8.8.8.8`
> - `dns`
> This hides non-matching packets and isolates desired traffic.

---

### 4. **What is the difference between TCP and UDP?**

| Feature | TCP | UDP |
| --- | --- | --- |
| Connection | Connection-oriented | Connectionless |
| Reliability | Guaranteed delivery | No guarantee |
| Speed | Slower | Faster |
| Use Cases | Web, Email | Streaming, Gaming, DNS |

---

### 5. **What is a DNS query packet?**

> A DNS query packet is used to request translation of a domain name (like www.google.com) into an IP address. These typically use UDP port 53, though TCP can also be used.
> 

---

### 6. **How can packet capture help in troubleshooting?**

> Packet capture allows you to:
> 
> - Identify failed connections
> - See retransmissions or timeouts
> - Confirm if servers are responding correctly
> - Detect unexpected traffic patterns or potential attacks

---

### 7. **What is a protocol?**

> A protocol is a set of rules that govern how data is formatted, transmitted, and received across a network. Examples include HTTP, TCP, DNS, UDP, ICMP.
> 

---

### 8. **Can Wireshark decrypt encrypted traffic (HTTPS)?**

> By default, Wireshark cannot decrypt HTTPS traffic because it’s encrypted. However, decryption is possible if:
> 
> - You have the **server's private key**
> - You configure **SSLKEYLOGFILE** in browsers
> - The traffic uses older versions of TLS without full encryption

---

## 🎯 Deliverables Checklist:

✅ Installed Wireshark

✅ Captured live traffic

✅ Filtered by protocol

✅ Identified 3+ protocols

✅ Exported .pcap file

✅ Wrote a short summary report

✅ Ready to answer interview questions

---
