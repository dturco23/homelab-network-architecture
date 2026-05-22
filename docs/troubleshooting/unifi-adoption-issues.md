# UniFi Adoption & VLAN Troubleshooting

## Overview

This document outlines several operational issues encountered during VLAN deployment and UniFi infrastructure migration within the homelab environment.

The issues primarily involved:
- switch adoption instability
- VLAN trunk configuration errors
- management reachability problems
- wireless dependency complications
- infrastructure recovery workflows

These incidents significantly influenced later documentation standards and deployment practices.

---

## Environment Context

### Core Infrastructure
- UniFi Gateway
- Managed UniFi Switching
- UniFi Wireless Access Points
- VLAN-segmented environment
- Proxmox-hosted infrastructure services

### Deployment Goals
- introduce segmented VLAN architecture
- migrate clients into trust zones
- standardize switch port profiles
- prepare for management network separation

---

## Incident Summary

Several deployment attempts resulted in:
- switch adoption failures
- controller reachability loss
- wired network interruption
- inconsistent management connectivity
- partial wireless functionality during outages

In some cases:
- wireless clients remained operational
- wired routing failed
- infrastructure management access became unstable

---

## Primary Contributing Factors

### Trunk Configuration Inconsistency

Trunk configuration mismatches between:
- gateway uplinks
- switch uplinks
- access point ports

created inconsistent VLAN propagation behavior across the environment.

Improper native VLAN handling contributed to intermittent management reachability issues.

---

### Management Network Dependency

At the time of deployment:
- management VLAN strategy was still evolving
- infrastructure management traffic was not fully standardized
- adoption traffic relied heavily on existing flat-network assumptions

This created situations where:
- infrastructure devices lost controller connectivity
- adoption behavior became inconsistent
- recovery required rollback of port profiles

---

### Wireless Dependency Complexity

Wireless access points continued partially functioning during some outages because:
- APs retained partial configuration state
- wireless clients maintained temporary connectivity
- wired infrastructure paths failed independently

This complicated troubleshooting because:
- some services appeared healthy
- actual routing stability was degraded

---

## Troubleshooting Process

### Initial Response
- verified physical connectivity
- reviewed switch uplink configuration
- checked VLAN assignments
- validated trunk behavior
- confirmed gateway reachability

### Recovery Actions
- reverted problematic port profiles
- restored known-good trunk configurations
- simplified VLAN propagation paths
- re-established management connectivity
- validated controller communication

### Validation Steps
- tested wired connectivity
- verified wireless operation
- confirmed DHCP behavior
- checked inter-VLAN routing expectations
- monitored switch adoption stability

---

## Operational Lessons Learned

### Standardize Trunks Early

Infrastructure trunk standards should be established before:
- broad VLAN deployment
- port-profile migration
- management network segmentation

---

### Preserve Stable Management Access

Infrastructure management access should remain:
- predictable
- isolated
- minimally dependent on experimental configuration changes

---

### Document Recovery Paths

Rollback procedures became critical during troubleshooting.

Future deployments should include:
- rollback checkpoints
- configuration snapshots
- staged migration plans

---

### Avoid Large-Scale Simultaneous Changes

Attempting:
- VLAN restructuring
- profile migration
- management redesign

simultaneously increased troubleshooting complexity significantly.

Incremental deployment strategies provide more stable operational outcomes.

---

## Long-Term Improvements

Future improvements include:
- formalized trunk standards
- dedicated management VLAN enforcement
- infrastructure configuration baselines
- improved monitoring visibility
- change-tracking discipline
- topology documentation refinement

---

## Conclusion

These troubleshooting events became a major turning point in improving:
- operational discipline
- infrastructure documentation
- deployment planning
- rollback preparation
- segmentation strategy maturity

The experience reinforced the importance of:
- staged deployments
- management network stability
- infrastructure standardization
- documentation-first operational practices
