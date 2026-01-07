# Security Model

## Access Control

- Root SSH login disabled
- Single non-root user with sudo
- Key-based SSH authentication only

---

## Firewall

- ufw enabled
- Only required ports open (SSH, HTTPS)
- `ufw status verbose` to check on open ports


---

## Intrusion Prevention

- fail2ban enabled
- SSH protection active

---

## Updates

- Automatic security updates enabled
- Located log
  - `/var/log/unattended-upgrades/unattended-upgrades.log`
