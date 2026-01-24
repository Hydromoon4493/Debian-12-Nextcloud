# System Architecture

## Physical Architecture

- Single physical host
- Headless operation
- Local storage only (no object storage, no external APIs)

### Storage Layout

- NVMe SSD (256 GB)
  - Debian 12 OS
  - Installed packages
  - Configuration files
  - Scripts
  - Backup metadata
- SATA HDD (1 TB)
  - Nextcloud data directory
  - Local restic backups
  - Raw data storage

- Exact mount points: 
  - `sda           8:0    0 931.5G  0 disk /mnt/nextcloud-data`
  - `nvme0n1p1 259:1    0   512M  0 part /boot/efi`

---

## Software Stack

- OS: Debian 12
- Web server: Apache
- Database: MariaDB
- PHP with required Nextcloud modules
- Application: Nextcloud (single-user instance)

- Exact Nextcloud version - Nextcloud 32.0.5
  - Found via `sudo -u www-data php /var/www/nextcloud/occ version`
- PHP version - PHP 8.2.29
  - Found via `php -v`
- MariaDB version - Ver 15.1 Distrib 10.11.14-MariaDB
  - Found via `mariadb --version`

---

## Network Model

- LAN-only access
- HTTPS enabled using **local Certificate Authority**
- No public DNS records
- No inbound internet exposure
- SSH restricted to a single non-root user

> **IMPORTANT DESIGN NOTE:**  
> This server is intentionally not exposed to the public internet.  
> Any future remote access must preserve this constraint.

---

## Data Flow

1. User devices sync files to Nextcloud
2. Files stored on HDD-mounted Nextcloud data directory
3. Nightly backups via restic:
   - Local backup on NVME
   - Remote backup to Remote Backup Host
4. Monthly restore verification job ensures backups are 