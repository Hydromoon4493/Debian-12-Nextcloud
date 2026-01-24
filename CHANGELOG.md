# Changelog

## 2026-01-07
- Changed `monthly-restic-check.sh`
    - Sanitized email address by creating `/etc/nextcloud/health-check.conf`
- Change health-check-mail.sh
    - Added email address to environment file
- Uploaded and pushed this documentation to GitHub

## 2026-01-03
- Initial documentation created

# 2026-01-08
- Change backups scripts
    - Change DB_DUMP tp `/tmp/nextcloud-db.sql`
    - This was to fix the restic snapshots
- Manually pruned both local and remote 

# 2026-01-23
- Campus IT added NC Server to VLAN 1026 allowing my laptop and phone access to the server
- Updated /etc/hosts to add IPs for Dad's network
- Updated Nextcloud config file to add new IP to trusted_domains
- Change health report email to use swaks for easier mailing

# 2026-01-24
- Changed backup scripts to have 31 "=" as opposed to ~50
- Edited `away-restic-backup.sh` to fail if WireGuard tunnel is not up
- Added two different commands to `process-phone-inbox.sh`
    - `sudo -u www-data php /var/www/nextcloud/occ files:scan --path="sam/files"` to update Nextcloud Files tab
    - `sudo -u www-data php /var/www/nextcloud/occ background-job:worker` to update the Nextcloud Photos tab
