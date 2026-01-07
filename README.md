# Nextcloud Debian 12 Server

## Overview

This project documents a personal, self-hosted Nextcloud instance running on
a headless Debian 12 server. The primary goal is to migrate and maintain the
majority of personal data off third-party cloud services (notably Google Drive)
while maintaining reliability, security, and simplicity.

The system is designed to be:
- LAN-only by default
- Secure by design
- Boring, maintainable, and scriptable
- Independent of all external cloud services

This server is intended for **single-user use only**.

---

## High-Level Goals

- Replace Google Drive with a self-hosted Nextcloud instance
- Maintain full control over data storage and access
- Ensure strong backups and recoverability
- Keep the system understandable and rebuildable from documentation alone

> **NOTE TO FUTURE ME:**  
> If this server ever fails catastrophically, this repository should contain
> everything needed to rebuild it from bare metal.

---

## Hardware Summary

- **Machine:** Dell OptiPlex 7050 (repurposed desktop)
- **RAM:** 8 GB
- **CPU Model** Intel(R) Core(TM) i5-7500 CPU @ 3.40GHz
- **OS Disk:** 256 GB NVMe SSD
- **Data Disk:** 1 TB SATA HDD
- **Total Data Stored (current):** ~10 GB

---

## Documentation Index

- [Architecture](docs/architecture.md)
- [Installation & Configuration](docs/installation.md)
- [Security Model](docs/security.md)
- [Backups & Recovery](docs/backups.md)
- [Maintenance](docs/maintenance.md)
- [Future Plans](docs/future-plans.md)
