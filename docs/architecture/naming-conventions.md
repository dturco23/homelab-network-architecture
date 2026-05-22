# Naming Conventions

## Overview

This document defines naming conventions used throughout the homelab infrastructure environment.

Consistent naming improves:
- operational clarity
- troubleshooting efficiency
- infrastructure organization
- service identification
- documentation readability

---

## Infrastructure Naming Philosophy

Naming conventions prioritize:
- readability
- predictability
- operational consistency
- scalability

Infrastructure names should remain:
- concise
- descriptive
- standardized

---

## VLAN Naming

| VLAN | Standard Name |
|---|---|
| 10 | Management |
| 50 | Trusted |
| 60 | Media |
| 70 | IoT |
| 99 | Guest |

---

## SSID Naming

| SSID | Purpose |
|---|---|
| HOME | Trusted client access |
| MEDIA | Streaming devices |
| IOT | Smart home devices |
| GUEST | Guest access |

SSID naming intentionally mirrors VLAN segmentation for operational clarity.

---

## Host Naming

Infrastructure systems should use:
- readable
- role-based
- standardized naming

Examples:
- proxmox-node-01
- nas-platform-01
- monitoring-service-01
- infrastructure-dns-01

Naming standards may evolve as infrastructure complexity expands.

---

## Documentation Naming

Documentation files should prioritize:
- descriptive names
- lowercase formatting
- hyphen-separated naming

Examples:
- vlan-design.md
- service-inventory.md
- operational-lessons.md

---

## Diagram Naming

Diagrams should use:
- version tracking
- descriptive naming
- consistent formatting

Examples:
- topology-v1.drawio
- topology-v1.png
- segmentation-v2.png

---

## Future Improvements

Future naming goals include:
- environment prefixes
- automation-friendly naming
- standardized inventory tracking
- infrastructure tagging standards
