# Network Security: Suricata IDS/IPS Deployment & Rule Configuration

## 📌 Project Overview
This project demonstrates the deployment of **Suricata** as an Intrusion Prevention System (IPS) on Kali Linux. It focuses on signature-based detection, 
custom rule creation, and troubleshooting YAML configuration issues in high-performance network security tools.

## 🛠️ Key Features
- **IPS Mode Configuration:** Successfully configured Suricata to monitor the `eth0` interface.
- **Custom Rule Engine:** Developed local rules to detect YouTube access and drop/block Facebook traffic.
- **YAML Troubleshooting:** Resolved critical indentation and path errors in `suricata.yaml` to ensure successful system loading.
- **Live Threat Monitoring:** Analyzed real-time security alerts via `fast.log`.

## 🚦 Security Rules Implemented
- **YouTube Detection:** `alert tcp any any -> any any (msg:"YouTube Access Detected"; content:"youtube.com"; sid:1000002;)`
- **Facebook Prevention:** `drop tcp any any -> any any (msg:"Facebook Blocked"; content:"facebook.com"; sid:1000010;)`

## 📸 Project Milestones
- **Configuration Success:** Verified with `sudo suricata -T`.
- **Traffic Logging:** Monitored live DHCP and privacy violation alerts.

## ⚠️ Technical Challenges: Zeek Deployment
During the lab, a manual installation of **Zeek** was attempted using a `.deb` package. 
However, a version mismatch between the Kali system library (`libc6 2.42`) and the Zeek package requirements (`libc6 < 2.38`) was identified. The package is staged for deployment in a compatible containerized environment.
