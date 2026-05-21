# Network Overview

## Purpose

This document provides a high-level overview of the homelab network architecture, segmentation model, and infrastructure goals.

The environment is designed to simulate production-style operational practices while supporting:
- virtualization
- self-hosted services
- infrastructure experimentation
- network segmentation
- operational troubleshooting
- long-term technical learning

---

## Core Infrastructure Goals

- Separate trusted and untrusted devices
- Reduce unnecessary east-west traffic
- Establish clear trust boundaries
- Support infrastructure service hosting
- Improve operational visibility
- Create scalable deployment standards

---

## Core Components

| Component | Purpose |
|---|---|
| Gateway / Firewall | Routing, segmentation, security policies |
| Managed Switching | VLAN distribution and device connectivity |
| Wireless Access Points | SSID-to-VLAN mapping |
| Proxmox Hosts | Virtualization platform |
| NAS Platform | Centralized storage |
| Infrastructure Services | DNS, monitoring, dashboards, automation |

---

## Current Focus Areas

- VLAN standardization
- Infrastructure service migration
- Documentation maturity
- Monitoring improvements
- Management network deployment planning

---

## Design Philosophy

The environment prioritizes:
- maintainability
- operational clarity
- segmented trust zones
- iterative improvement
- documentation-first infrastructure practices
