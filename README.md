# SentinelX  
A Modern Security Monitoring & Analysis Platform

## 📌 Overview
SentinelX is a customizable security monitoring and analysis platform designed for real-time threat detection, network analysis, file integrity monitoring, log analytics, and endpoint visibility.  
It centralizes multiple cybersecurity tools into a unified interface to support SOC analysts, researchers, and students.

SentinelX enhances traditional monitoring by integrating with widely used open-source security tools, including:

- **Wireshark** – network packet capture & analysis  
- **Nmap** – network scanning & reconnaissance  
- **Suricata** – intrusion detection & deep packet inspection  
- **Zeek** – advanced network security monitoring  
- **OSQuery** – live endpoint analytics and SQL-based queries  
- **ClamAV** – malware detection & file scanning  
- **OpenSearch Dashboards** – visualization, dashboards & analytics  

Together, these tools provide a powerful environment for threat detection, forensic analysis, and security monitoring.

---

## 🚀 Key Features

### 🔍 Real-Time Monitoring
- Endpoint activity logging  
- Log ingestion & correlation  
- Network event inspection  
- Alert generation & analysis  

### 🛡 Threat Detection Capabilities
- Behavioral alerts  
- IDS/IPS detection (Suricata/Zeek)  
- Malware scanning (ClamAV)  
- Vulnerability & configuration assessments  

### 🧰 Tool Integrations
SentinelX consolidates multiple tools into one platform:
- Packet analysis (Wireshark, Zeek)  
- Host inspection (OSQuery)  
- Port scanning & discovery (Nmap)  
- Threat intel feeds  
- Dashboard visualization (OpenSearch)  

### 🎨 Custom Interface & Branding
- Custom SentinelX dark theme  
- New dashboard background  
- Custom login UI  
- Updated icons, favicon, and tab title  
- SentinelX-branded dashboard visuals  

---

## 📦 Installation

### 1. Install Security Manager Components
```bash
curl -s https://packages.wazuh.com/4.x/install.sh | sudo bash
```

### 2. Install Agents on Endpoints
```
wget https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_*.deb
sudo WAZUH_MANAGER="<your-ip>" WAZUH_AGENT_GROUP="default" dpkg -i wazuh-agent_*.deb
```

### 3. Apply SentinelX Frontend Branding
```
Copy your UI assets into the dashboard folders:

/usr/share/wazuh-dashboard/src/core/server/core_app/assets/
/usr/share/wazuh-dashboard/src/core/public/
/usr/share/wazuh-dashboard/plugins/wazuh/public/
```
```
Rebuild UI assets:

sudo rm -rf /usr/share/wazuh-dashboard/optimize/*
sudo systemctl restart wazuh-dashboard
```
## 📂 Project Structure
```
SentinelX/
│
├── assets/
│   ├── sentinelx_logo.svg
│   ├── sentinelx_favicon.ico
│   └── sentinelx_bg.svg
│
├── integrations/
│   ├── wireshark/
│   ├── nmap/
│   ├── suricata/
│   ├── zeek/
│   ├── osquery/
│   └── clamav/
│
└── README.md
```
## ⚖️ Disclaimer

SentinelX integrates multiple open-source cybersecurity tools and monitoring engines.
Some backend components utilize open-source technologies such as Wazuh, OpenSearch, and other community security tools.
SentinelX applies custom branding, UI modifications, and workflow enhancements and does not claim ownership over the core technologies it interfaces with.

## ⭐ Acknowledgements

Thanks to the open-source cybersecurity community whose tools and innovations make SentinelX possible.
