# Service Dependency Mapping

## Overview

This document outlines major service dependencies throughout the homelab infrastructure environment.

The purpose of dependency tracking is to:
- improve operational visibility
- simplify troubleshooting
- support recovery planning
- identify critical infrastructure relationships
- improve deployment awareness

As infrastructure complexity increased, understanding service relationships became increasingly important.

---

## Core Infrastructure Dependencies

The environment is built around several foundational infrastructure layers:

```text
Internet Connectivity
    ↓
Gateway / Firewall
    ↓
Switching & Wireless Infrastructure
    ↓
Virtualization Platform
    ↓
Infrastructure Services
    ↓
Client & Application Access
```

---

## Core Dependency Relationships

| Service | Depends On |
|---|---|
| Pi-hole | Gateway, Proxmox, Network Connectivity |
| Home Assistant | Proxmox, IoT Connectivity |
| Uptime Kuma | Network Connectivity, Service Availability |
| Homer Dashboard | Proxmox, Hosted Services |
| NAS Platform | Network Infrastructure, Storage Hardware |

---

## Infrastructure Dependency Priorities

### Critical Infrastructure
Critical systems include:
- gateway/firewall
- switching infrastructure
- DNS services
- virtualization hosts

Failure within these systems may impact large portions of the environment.

---

### Core Operational Services

Operational services include:
- monitoring systems
- dashboards
- storage systems
- automation platforms

These systems improve operational visibility and infrastructure usability.

---

### Secondary & Experimental Services

Experimental systems should remain operationally isolated where possible to reduce:
- infrastructure instability
- troubleshooting complexity
- unintended dependency expansion

---

## DNS Dependency Awareness

DNS became one of the most operationally important services throughout the environment.

Several infrastructure components rely heavily on:
- internal DNS resolution
- reliable network connectivity
- stable infrastructure routing

This significantly increased awareness around DNS reliability and recovery planning.

---

## Virtualization Dependency Awareness

As services consolidated into the Proxmox platform:
- virtualization reliability became increasingly important
- centralized infrastructure dependencies expanded
- recovery planning became more critical

Platform stability directly influences service availability.

---

## Operational Lessons

Several operational lessons reinforced the importance of dependency mapping:

### Hidden Dependencies Increase Complexity

Infrastructure systems frequently rely on:
- DNS
- routing
- virtualization
- service discovery

without those relationships being immediately obvious.

---

### Centralized Services Increase Recovery Importance

As more services consolidated into shared infrastructure:
- recovery sequencing became more important
- backup planning became more critical
- infrastructure visibility became increasingly valuable

---

### Monitoring Supports Dependency Awareness

Monitoring platforms improve visibility into:
- service availability
- infrastructure reachability
- cascading failures
- operational health

---

## Future Improvements

Planned future improvements include:
- dependency visualization diagrams
- service mapping refinement
- monitoring integration
- automated infrastructure documentation
- infrastructure dependency tracking

---

## Long-Term Goals

Long-term goals include:
- improved operational awareness
- predictable recovery workflows
- scalable service architecture
- platform-oriented infrastructure management
- improved infrastructure resilience

---

## Security & Sanitization

All published dependency documentation has been sanitized to remove:
- internal endpoints
- infrastructure identifiers
- sensitive configuration details
- exposed service relationships
