# 🚀 AIRA Private 4G/5G Cellular Core & Telecom Router

![Country: India](https://img.shields.io/badge/Made_In-India_🇮🇳-orange.svg?style=for-the-badge)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)
![Platform: Ubuntu Linux](https://img.shields.io/badge/Platform-Ubuntu_Linux-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Language: Python](https://img.shields.io/badge/Language-Python_3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Core: Open5GS](https://img.shields.io/badge/Core-Open5GS_Framework-005A9C?style=for-the-badge)
![Database: MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

An advanced, low-latency private cellular core network manager and automated packet router. This infrastructure automates **Open5GS** and **srsRAN** topologies, allowing a local machine to act as an independent Mobile Network Operator (MNO) Core using Software Defined Radio (SDR) hardware.

> **💡 OFFLINE HUMANITARIAN DEPLOYMENT PROFILE:**
> This repository is customized specifically as an offline digital educational node for children in South Sudan. It enables zero-cost local VoIP calling, offline YouTube/Hugging Face caching, and an independent local AI knowledge base without requiring an active global internet backhaul.

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details. Contributions, forks, and redistribution are welcome under the terms of that license.

---

## 🏗️ Architectural Topology (Offline Loopback Mode)

```text
  +---------------------------------------+
  |        User Equipment (UE)            |  <-- Client Devices (Smartphones/IoT)
  |   (Wi-Fi & Cellular Enabled Hardware) |      Subnet Address: 10.45.0.X Pool
  +---------------------------------------+      QoS Priority Level 1 (Conversational Voice)
                      │
                      ▼ [Local Wi-Fi / Radio Link Access Connection]
  +---------------------------------------+
  |    ESP32 Access Point & NAT Router    |  <-- Hardware Interface (esp32_router.ino)
  |   (Local Gateway Instance: 10.45.0.1) |      lwIP Stack & Captive Portal Active
  +---------------------------------------+
                      │
                      ▼ [GTP Tunnel / Embedded Pipeline Stream]
  +---------------------------------------+
  |       Open5GS Core Framework          |  <-- Session, Routing & Voice Orchestration
  |  (SMF on 127.0.0.5 | UPF on 127.0.0.7)|      Local Gateway DNS Resolution (10.45.0.1)
  +---------------------------------------+
                      │
                      ▼ [ogstun Virtual Tunnel Interface Layer]
  +---------------------------------------+
  |    Automated NAT Routing Engine       |  <-- Managed via app.py (SIP/VoIP Enabled)
  |   (Linux Kernel IP Forwarding Matrix) |      Unlimited Local Bandwidth Matrix (1 Gbps)
  +---------------------------------------+
                      │
                      ▼ [Internal Loopback Matrix]
  +---------------------------------------+
  |       AIRA Central Local Server       |  <-- Offline Content Delivery Network (CDN)
  |      (Offline Flask Micro-Core)       |      Serves Cached YouTube & Hugging Face AI Data
  +---------------------------------------+
```

## 🌍 Motivation

Reliable connectivity is often unavailable in remote or under-resourced regions. AIRA packages standard open-source telecom components (Open5GS, srsRAN) with a lightweight local content-delivery layer, so a single machine and SDR/ESP32 hardware set can provide offline cellular connectivity, local VoIP, and a cached educational knowledge base — with zero dependency on a live internet backhaul.

## ⚙️ Core Components

- **Open5GS** — 4G/5G core network functions (SMF, UPF, AMF, etc.)
- **srsRAN** — software-defined radio access network stack
- **ESP32 Access Point** — local Wi-Fi/NAT gateway hardware interface
- **MongoDB** — subscriber database backend
- **Flask Micro-Core** — offline content delivery (cached educational/AI resources)

## 🚀 Getting Started

See `docs/` for setup instructions covering Open5GS configuration, SDR/ESP32 hardware setup, and the offline content server.

## 🤝 Contributing

Contributions are welcome under the MIT License. Please open an issue or pull request on the repository.
