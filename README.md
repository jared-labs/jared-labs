# Homelab & Projects — Jared Shaw

> **What is this?**  
> My living lab notebook + portfolio. It documents how I run my homelab Proxmox cluster and adjacent personal projects. Expect a mix of **runbooks I actually use**, architecture/decisions, inventories, and the occasional one-off build. Not everything here is pure IT/SysAdmin/SecOps.

## What you’ll find
- **Runbooks:** spinning up VMs/services, adding a Proxmox node, rolling upgrades, backup/restore tests.
- **Docs:** topology, decisions, inventories, storage/backups, gotchas.
- **Troubleshooting:** real-world quirks and fixes I’ve hit.
- **One-offs:** Home Assistant automations, 3D/DIY, etc.

## What this is not
- A step-by-step vendor tutorial.
- A place for secrets (keys/creds are redacted or omitted).

## Who it’s for
- **Me** — operational notes I can repeat.
- **You** — see how I work or borrow what helps.

## Repo layout
- `README.md` — high-level overview and current state (this page)  
- `docs/homelab/runbooks/` — task-oriented runbooks (coming online)  
- `assets/` — screenshots/diagrams

_This is a living document; sections reflect current reality and evolve over time._

---

## Homelab
- Network Overview
- [Proxmox Cluster](https://github.com/jared-labs/Proxmox-Cluster)
- NAS

## Self-Hosted Services
- Proxmox (Hypervisor)
  - [Add a Proxmox node runbook](docs/homelab/runbooks/add-node.md)
- Home Assistant
- Cribl
  - [Cribl VM Spinup Runbook](https://github.com/jared-labs/Cribl-Runbook)
- Graylog
  - [Graylog VM Spinup Runbook](https://github.com/jared-labs/Graylog-Runbook)
- OpenVAS
  - [OpenVAS VM Spinup Runbook](https://github.com/jared-labs/OpenVAS-Runbook)
- OctoPrint
- SmokePing
- WireGuard
- Omada SDN

## Automation
- Home Assistant Dashboard Overview
- Chicken Coop
- Lighting

## Maker / Tools
*(projects to be added)*

## Comms & Field Tech
*(projects to be added)*

---

## Related runbooks (separate repos)
- **Cribl Stream:** https://github.com/jared-labs/Cribl-Runbook  
- **Graylog:** https://github.com/jared-labs/Graylog-Runbook  
- **New Proxmox Node:** https://github.com/jared-labs/New-Proxmox-Node-Runbook  
- **OpenVAS / Greenbone:** https://github.com/jared-labs/OpenVAS-Runbook  
- **Open-AudIT:** https://github.com/jared-labs/Open-AudIT-Runbook  
- **Proxmox Cluster (this repo):** https://github.com/jared-labs/Proxmox-Cluster
