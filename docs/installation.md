# Installation & Configuration

## Base OS Installation

- Debian 12 minimal install
- No desktop environment
- SSH server installed

- Disk partitioning scheme
```
NAME        FSTYPE FSVER LABEL UUID                                 FSAVAIL FSUSE% MOUNTPOINTS
sda         ext4   1.0         ee9bfe55-7ba4-4437-9bc8-fc79cbae7138  857.7G     1% /mnt/nextcloud-data
sr0                                                                                
nvme0n1                                                                            
├─nvme0n1p1 vfat   FAT32       2317-6604                               499M     2% /boot/efi
├─nvme0n1p2 ext4   1.0         ead996c4-78f4-4e77-bbcb-16e1c6e7050c  190.5G    13% /
└─nvme0n1p3 swap   1           8a5ebc04-870c-440c-b387-b9f18f18b3eb                [SWAP]
```

---

## Web Stack Setup

- Apache installed and configured
- HTTPS enforced
- Local CA created and trusted on client devices
- Cert locationed in `/etc/ssl/localca`
- No expiration policy

---

## Nextcloud Installation

- Nextcloud installed manually
  - Downloaded and installed a tarball?
- Data directory located on HDD
- Single-user configuration
- Path to `config.php`
  - `/var/www/nextcloud/config/`

---
