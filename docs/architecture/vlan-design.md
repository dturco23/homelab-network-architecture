# VLAN Design

## Overview

This document outlines the VLAN segmentation strategy used throughout the homelab environment.

The primary goals of segmentation are:
- establish clear trust boundaries
- reduce unnecessary lateral traffic
- improve operational organization
- isolate infrastructure services
- support scalable future growth
- simulate production-style infrastructure practices

The environment is intentionally designed around operational separation rather than flat-network convenience.

---

## Segmentation Philosophy

The network is divided into functional trust zones based on:
- device trust level
- operational role
- administrative requirements
- exposure risk
- service communication needs

Segmentation is used to:
- limit unnecessary device communication
- improve troubleshooting clarity
- simplify policy management
- support future firewall refinement
- prepare for more advanced infrastructure services

---

## VLAN Overview

| VLAN | Name | Purpose | Trust Level |
|---|---|---|---|
| 10 | Management | Infrastructure administration and management interfaces | High Trust |
| 50 | Trusted Clients | Primary personal and administrative devices | High Trust |
| 60 | Media | Streaming and casting devices | Medium Trust |
| 70 | IoT | Smart home and embedded devices | Low Trust |
| 99 | Guest | Internet-only guest access | Untrusted |

---

## VLAN Details

### VLAN 10 — Management

The management network is reserved for:
- infrastructure administration
- management interfaces
- hypervisors
- networking equipment
- future monitoring and management systems

This VLAN is intended to remain highly restricted and isolated from general client traffic.

Planned systems include:
- gateway management
- switch management
- hypervisor management
- infrastructure dashboards
- monitoring platforms

---

### VLAN 50 — Trusted Clients

This VLAN contains primary trusted devices used for:
- administration
- engineering work
- infrastructure management
- daily operational tasks

Devices on this network maintain broader internal access due to their trusted status.

This VLAN serves as the primary operational network for infrastructure interaction.

---

### VLAN 60 — Media

The media VLAN exists to support:
- streaming devices
- casting endpoints
- smart entertainment hardware

This network is intentionally separated from trusted client systems while still allowing controlled service interoperability where required.

Special consideration is given to:
- mDNS behavior
- casting compatibility
- service discovery requirements

---

### VLAN 70 — IoT

The IoT VLAN contains:
- smart home devices
- embedded systems
- lower-trust network appliances

This segment is designed to minimize unnecessary access into trusted infrastructure while still permitting required outbound communication.

The long-term goal is to heavily restrict east-west traffic originating from IoT devices.

---

### VLAN 99 — Guest

The guest network is designed for:
- temporary devices
- visitor access
- isolated internet connectivity

Guest devices should not have access to:
- infrastructure systems
- trusted clients
- management interfaces
- internal services

This VLAN represents the lowest-trust segment within the environment.

---

## SSID Mapping Strategy

Wireless networks are mapped directly to VLAN trust zones to maintain operational consistency.

| SSID | VLAN | Purpose |
|---|---|---|
| HOME | 50 | Trusted client access |
| MEDIA | 60 | Streaming and entertainment devices |
| IOT | 70 | Smart home devices |
| GUEST | 99 | Guest internet access |

SSID naming and mapping may evolve over time as infrastructure standards mature.

---

## Operational Considerations

Key operational priorities include:
- minimizing accidental cross-network exposure
- maintaining predictable traffic flows
- simplifying troubleshooting workflows
- preserving management network stability
- supporting future firewall policy refinement

Segmentation changes are approached cautiously due to the operational impact of:
- trunk configuration errors
- management VLAN migration
- wireless adoption dependencies
- service discovery complications

---

## Lessons Learned

Early VLAN deployment efforts highlighted several important operational realities:
- management VLAN planning should occur before large-scale profile deployment
- trunk configuration consistency is critical
- wireless adoption dependencies can create recovery complexity
- service discovery protocols require additional planning across segmented networks

Operational troubleshooting experience became a major driver for improving documentation and deployment discipline.

---

## Future Improvements

Planned future improvements include:
- dedicated management VLAN enforcement
- refined firewall policies
- infrastructure monitoring segmentation
- centralized logging
- enhanced service observability
- infrastructure automation
- expanded documentation and topology visualization

---

## Security & Sanitization

All published documentation has been sanitized to remove:
- public IP information
- infrastructure identifiers
- credentials
- internal DNS records
- VPN configuration details
- sensitive operational data
