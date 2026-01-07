# Maintenance

## Disk Health Monitoring

- SMART checks run hourly
- NVMe SSD and HDD monitored
- Email alerts on failure
- Scripts located in `/usr/local/bin/`

---

## Logs

Important logs to monitor:
- Apache
  - `/var/log/apache`
- MariaDB
  - `/var/log/mysql/error.log` (Disabled by default)
  - To enable run `nano /etc/mysql/mariadb.conf.d/50-server.cnf`
  - And uncomment `#general_log_file       = /var/log/mysql/mysql.log`
- Nextcloud
  - `/var/www/nextcloud/data/nextcloud.log`
- fail2ban
  - `/var/log/fail2ban.log`
- Backups
  - `/var/log/nextcloud-restic-backup.log`
- Phone Processing
  - `/var/log/process-phone-inbox.log`
