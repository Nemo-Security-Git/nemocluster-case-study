# NemoCluster — Sanitized Capacity Snapshot

## Measurement Basis

The figures in this document are derived from a versioned internal inventory recorded on **1 September 2026 at 03:30 UTC**. They are not live telemetry and should be interpreted as an approximate dated snapshot. The analysis environment used to prepare this public case study had no route or administrative key to the private cluster.

## Aggregate Capacity

| Dimension | Recorded value |
|---|---:|
| Physical Proxmox nodes | **6** |
| Nodes marked online | **6** |
| CPU | **60 recorded cores**; at least **96 documented threads** |
| Aggregate memory | **271,268 MB**, approximately **264.9 GiB** |
| Active discrete compute GPUs | **7** |
| Approximate active VRAM | **54 GiB** |
| Recorded raw storage | Approximately **15.7 TB** |
| Principal capacity-oriented storage | Approximately **10 TB** |
| Distributed-storage devices | **6 Ceph OSDs** |
| Distributed-storage state | Documented as healthy in the dated inventory |

## Calculation Notes

The physical-node total excludes virtual machines and containers to prevent double-counting. GPU capacity excludes devices not used for compute and integrated display devices. CPU thread information was incomplete for one node, so the public figure is expressed as **at least 96 documented threads** rather than as a definitive cluster total.

Memory is rounded from the aggregate inventory value. Storage figures represent raw or configured capacity and must not be interpreted as guaranteed usable space after replication, filesystem overhead, reservations, or operational allocation.

## Disclosure Boundary

This public snapshot intentionally excludes node identities, processor models by host, GPU-to-workload mapping, device identifiers, network addresses, storage layout, cluster quorum details, management interfaces, failure domains, and capacity-allocation rules.

The purpose is to demonstrate the scale of the platform and the author’s capacity-planning responsibility without increasing the attack surface of the operational environment.
