# Backups & Recovery

## Backup Tool

- restic
- Encrypted repositories
- Daily snapshots

### Backup Targets

- Local backup on NVME
- Remote backup to Remote Backup Host

- Local backup repo: `/mnt/backup/restic`
- Remote backup repo: `/home/<user>/restic`

- Retention policy
  - KEEP_DAILY=7 
  - KEEP_WEEKLY=2
  - KEEP_MONTHLY=3

---

## Backup Schedule

- Local backup: daily @ 03:00
- Inbox processing: daily @ 04:00
- Remote backup: daily @ 05:00
- Restore test: monthly

---

## Restore Verification

Monthly job restores a sample snapshot and verifies integrity.
- Restores latest snapshot to a temp directory
- Choses a single random file to restore
- Anything fails an email is sent
- Everything if removed at the end of the script
