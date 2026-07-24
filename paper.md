---
title: 'AIRA: An Open-Source Private 4G/5G Cellular Core and Offline Content Delivery Router for Humanitarian Deployment'
tags:
  - Python
  - telecommunications
  - 5G
  - Open5GS
  - srsRAN
  - offline networking
  - humanitarian technology
authors:
  - name: Adam Eehan
    affiliation: 1
affiliations:
  - name: Independent Researcher, India
    index: 1
date: 24 July 2026
bibliography: paper.bib
---

# Summary

AIRA is an open-source orchestration framework that automates the deployment of a private 4G/5G cellular core network using the `Open5GS` and `srsRAN` software stacks, combined with low-cost Software Defined Radio (SDR) and ESP32-based access-point hardware. Rather than relying on a live internet backhaul, AIRA allows a single local machine to operate as an independent Mobile Network Operator (MNO) core, providing offline cellular connectivity, local VoIP calling, and a cached educational content-delivery layer (including cached web and AI knowledge resources) to end-user devices over standard cellular and Wi-Fi radio links. The project's initial deployment profile targets offline digital-education nodes for underserved regions, including a pilot use case supporting children's access to educational content in South Sudan.

# Statement of need

Reliable internet connectivity is frequently unavailable in remote, conflict-affected, or under-resourced regions, limiting access to digital education and communication tools. While core telecom software such as `Open5GS` and `srsRAN` provides the building blocks for private cellular networks, assembling them into a complete, self-contained offline system — including subscriber management, NAT/IP routing, VoIP signalling, and local content caching — requires substantial integration effort spanning networking, radio configuration, and application-layer services. AIRA addresses this gap by providing a single automated orchestration layer over these components, packaging session/routing management, subscriber databases, and an offline content-delivery server into one deployable system. This lowers the barrier for humanitarian, educational, and research deployments of private cellular infrastructure in areas without dependable internet access.

# Functionality

AIRA automates the following:

- **Core network orchestration**: configuration and lifecycle management of Open5GS core functions (SMF, UPF, and related components).
- **Radio access integration**: coordination with `srsRAN`-based radio access network topologies over SDR hardware.
- **Hardware gateway management**: an ESP32-based access point acting as a local Wi-Fi/NAT gateway for client devices.
- **Subscriber and routing management**: automated NAT routing and subscriber database handling for connected User Equipment (UE).
- **Offline content delivery**: a local Flask-based content server that caches educational and AI knowledge resources for access without an external network connection.

# Acknowledgements

The author acknowledges the maintainers of the Open5GS and srsRAN open-source projects, upon which this framework builds.

# References
