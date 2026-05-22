# Service Inventory

## Overview

This document tracks infrastructure services deployed throughout the homelab environment.

The purpose of this inventory is to:
- maintain operational visibility
- document service purpose
- track deployment locations
- simplify troubleshooting
- support future migration planning
- improve infrastructure organization

The environment prioritizes lightweight, self-hosted infrastructure services designed to simulate production-style operational practices.

---

## Infrastructure Service Inventory

| Service | Platform | Purpose | Status |
|---|---|---|---|
| Pi-hole | Proxmox LXC | DNS filtering and network-wide ad blocking | Active |
| Home Assistant | Planned/Active | Smart home automation platform | Migration Planned/Active |
| Uptime Kuma | Proxmox LXC | Infrastructure and service monitoring | Active |
| Homer Dashboard | Proxmox LXC | Internal infrastructure dashboard | Active |
| TrueNAS SCALE | Dedicated NAS Platform | Centralized storage and backup platform | Planned/In Progress |

---

## Service Details

---

## Pi-hole

### Purpose
Pi-hole provides:
- DNS filtering
- network-wide advertisement blocking
- improved DNS visibility
- centralized DNS management

### Deployment Type
- Linux Container (LXC)
- Hosted on Proxmox VE

### Operational Notes
Pi-hole became one of the first core infrastructure services migrated into the virtualization platform.

The service highlighted the importance of:
- static addressing
- DNS planning
- infrastructure dependency awareness

---

## Home Assistant

### Purpose
Home Assistant is intended to centralize:
- smart home management
- automation workflows
- IoT orchestration
- infrastructure integration

### Deployment Goals
- improve IoT organization
- centralize automation logic
- separate smart devices from trusted systems

### Operational Considerations
Home Assistant deployment planning influenced broader VLAN and trust-zone design decisions throughout the environment.

---

## Uptime Kuma

### Purpose
Uptime Kuma provides:
- infrastructure monitoring
- service availability tracking
- operational visibility
- health validation

### Deployment Goals
The platform supports:
- infrastructure awareness
- outage visibility
- service uptime tracking

Monitoring became increasingly important as service count and segmentation complexity expanded.

---

## Homer Dashboard

### Purpose
Homer provides a centralized dashboard for:
- infrastructure services
- self-hosted applications
- operational navigation
- internal service organization

### Operational Benefits
The dashboard improved:
- infrastructure visibility
- service organization
- operational accessibility

---

## TrueNAS SCALE

### Purpose
The NAS platform is intended to provide:
- centralized storage
- backup infrastructure
- scalable storage management
- ZFS-based redundancy

### Platform Goals
The storage platform prioritizes:
- redundancy
- recoverability
- scalability
- operational consistency

### Planned Features
- RAIDZ2 storage pools
- centralized backups
- virtualization storage integration
- future service backup orchestration

---

## Operational Lessons

Maintaining a formal service inventory improves:
- troubleshooting clarity
- dependency awareness
- migration planning
- operational organization
- recovery workflows

As infrastructure complexity increases, service tracking becomes increasingly valuable.

---

## Future Improvements

Planned future additions include:
- reverse proxy infrastructure
- centralized logging
- observability tooling
- automation platforms
- configuration management systems
- infrastructure-as-code experimentation

---

## Security & Sanitization

All infrastructure documentation has been sanitized to remove:
- internal IP information
- credentials
- sensitive infrastructure details
- exposed service endpoints
- authentication configuration
