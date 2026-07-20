# Jared Shaw — Home Lab & Security Projects

Operational documentation from a multi-node home lab focused on security monitoring, vulnerability management, and infrastructure automation.

## Lab Infrastructure

7-node Proxmox cluster running 14+ VMs and containers across a segmented 10.0.0.0/24 network with dedicated ranges for IoT, servers, and DHCP.

**Core Stack:** Proxmox VE · TrueNAS · Graylog · Cribl · OpenVAS · MISP · Open-AudIT · Home Assistant · WireGuard · N8N · TAK Server

---

## Runbooks

Sanitized, repeatable procedures for standing up and configuring each service.

### Hypervisor & Infrastructure

| Runbook | Description |
|---------|-------------|
| [Proxmox Cluster](https://github.com/jared-labs/Proxmox-Cluster) | Cluster architecture, storage, and networking |
| [New Proxmox Node](https://github.com/jared-labs/New-Proxmox-Node-Runbook) | Adding a node to the existing cluster |
| [Proxmox PVE 9 Cluster Upgrade](https://github.com/jared-labs/Proxmox-PVE9-Cluster-Upgrade) | Rolling PVE 8→9 upgrade across 7 nodes — GRUB EFI recovery, canary strategy |

### Security & Monitoring

| Runbook | Description |
|---------|-------------|
| [Graylog](https://github.com/jared-labs/Graylog-Runbook) | SIEM deployment — inputs, streams, index sets |
| [Cribl](https://github.com/jared-labs/Cribl-Runbook) | Log routing — pipelines, sources, destinations |
| [OpenVAS](https://github.com/jared-labs/OpenVAS-Runbook) | Greenbone deployment, authenticated scanning, feed management, wave scheduling |
| [OpenVAS → Graylog Pipeline](https://github.com/jared-labs/OpenVAS-to-Graylog-Pipeline) | Security data pipeline — NDJSON export, field schema, SIEM integration, design decisions |
| [Open-AudIT](https://github.com/jared-labs/Open-AudIT-Runbook) | Asset inventory and network discovery |
| [Detection Engineering Runbook](https://github.com/jared-labs/Detection-Engineering-Runbook) | Sanitized home lab SIEM detection engineering runbook with Graylog event definitions, alert lifecycle guidance, and posture-based detection examples |

### Threat Intelligence

| Runbook | Description |
|---------|-------------|
| [MISP Deployment](https://github.com/jared-labs/MISP-Runbook) | Threat intel platform setup |
| [MISP Initial Config](https://github.com/jared-labs/MISP-Initial-Configuration) | Feeds, taxonomies, and sharing groups |
| [MISP → Cribl IOC Export](https://github.com/jared-labs/MISP-to-Cribl-IOC-Export-Enrichment-Runbook) | Enriching log streams with threat intel IOCs |

### Automation & Fleet Management

| Runbook | Description |
|---------|-------------|
| [Ansible Fleet Management](https://github.com/jared-labs/Ansible-Fleet-Management) | Control node design, inventory modeling, patch orchestration |

### Situational Awareness

| Runbook | Description |
|---------|-------------|
| [TAK Server](https://github.com/jared-labs/TAK-Server-Runbook) | mTLS coordination platform, service architecture, upgrade strategy |

### Identity & Access

| Runbook | Description |
|---------|-------------|
| [Vaultwarden](https://github.com/jared-labs/Vaultwarden-Runbook) | Self-hosted password manager deployment |

---

## Log Pipeline

```
Sources                    Routing              SIEM
──────────────────────    ─────────────        ──────────────
Proxmox hosts        ──►                  ──►
Omada SDN Controller ──►  Cribl Stream    ──►  Graylog
OpenVAS scan results ──►                  ──►
rsyslog (Linux VMs)  ──►                  ──►
```

## Threat Intel Flow

```
MISP (IOC feeds) ──► Cribl (enrichment) ──► Graylog (correlation/alerting)
```

---

## 3D Prints & DIY

| Project | Link |
|---------|------|
| ANYSECU T68 4G Radio Button Cover | [Thingiverse](https://www.thingiverse.com/thing:7222981) |
| Suzuki KingQuad Headlight Mount | [Thingiverse](https://www.thingiverse.com/thing:6703471) |
| KLR250 LED Headlight Bracket | [Thingiverse](https://www.thingiverse.com/thing:6740377) |
| U94 PTT Vertical Molle Retaining Plate | [Thingiverse](https://www.thingiverse.com/thing:6424578) |

---

*This is a living document. Runbooks reflect real operational procedures from an active lab environment.*
