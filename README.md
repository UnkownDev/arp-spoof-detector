# arp-spoof-detector
Python tool to detect ARP spoofing using Scapy and real-time packet sniffing.
# 🛡️ ARP Spoofing Detection System

This project is a Python-based **ARP spoofing detection tool** built using [Scapy](https://scapy.readthedocs.io/).  
It monitors ARP traffic on a local network and detects suspicious activity (such as ARP spoofing / MITM attacks).  

## 🚀 Features
- Sniffs **outgoing ARP requests** made by the host.
- Sniffs **incoming ARP replies** from the network.
- Detects **inconsistent ARP headers**.
- Maintains an **IP-MAC mapping table** for known devices.
- Identifies suspicious ARP packets (IP-MAC mismatch).
- Performs **spoof detection** using:
  - **Full Cycle check** → Validates ARP replies by sending a TCP SYN to the claimed IP.
  - **Half Cycle check** → Sends ARP requests to validate unsolicited ARP replies.
- Raises alarms on detecting spoof attempts.

## 🏗️ Requirements
- Python **3.7+**
- [Scapy](https://scapy.readthedocs.io/en/latest/)

Install dependencies:
```bash
pip install scapy
