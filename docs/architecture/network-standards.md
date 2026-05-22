# Network Standards

## Overview

This document defines operational standards used throughout the homelab network environment.

The purpose of these standards is to:
- improve infrastructure consistency
- simplify troubleshooting
- reduce configuration drift
- support scalable deployment practices
- maintain operational clarity

Standardization became increasingly important as infrastructure complexity expanded.

---

## VLAN Standards

| VLAN | Purpose | Trust Level |
|---|---|---|
| 10 | Management | High Trust |
| 50 | Trusted Clients | High Trust |
| 60 | Media | Medium Trust |
| 70 | IoT | Low Trust |
| 99 | Guest | Untrusted |

VLAN purposes should remain consistent across:
- wired infrastructure
- wireless SSIDs
- firewall policy design
- future automation workflows

---

## SSID Standards

| SSID | VLAN | Purpose |
|---|---|---|
| HOME | 50 | Trusted devices |
| MEDIA | 60 | Streaming and entertainment |
| IOT | 70 | Smart home devices |
| GUEST | 99 | Guest access |

SSID naming prioritizes:
- readability
- operational clarity
- predictable segmentation

---

## Infrastructure Standards

Infrastructure systems should prioritize:
- predictable naming
- stable management access
- segmented trust boundaries
- centralized documentation

Operational consistency is prioritized over unnecessary complexity.

---

## Trunk Standards

Trunk configuration should remain:
- standardized
- documented
- minimally modified without validation

Operational lessons reinforced the importance of:
- native VLAN consistency
- predictable propagation behavior
- staged deployment testing

---

## Documentation Standards

Infrastructure changes should include:
- deployment documentation
- rollback planning
- topology updates
- changelog tracking

Documentation-first operational practices reduce troubleshooting overhead and improve recovery confidence.

---

## Future Improvements

Future standardization goals include:
- infrastructure naming standards
- automation deployment standards
- configuration management workflows
- centralized monitoring conventions
- infrastructure-as-code practices
