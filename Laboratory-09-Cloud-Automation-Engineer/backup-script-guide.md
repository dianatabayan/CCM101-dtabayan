# Backup Script Guide

This guide explains the automated backup script created for CloudNova Technologies, so the client's IT team can understand and maintain it.

## The Script (backup.sh)

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## What `chmod +x` Does
By default, Linux treats a new text file as data, not as a program. The `chmod +x backup.sh` command adds the **execute** permission to the file, so the system allows it to be run as a script with `./backup.sh`. Without it, you get a "Permission denied" error.

## The Cron Expression

```
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|-------|-------|---------|
| Minute | `0` | At minute 0 (the top of the hour) |
| Hour | `2` | At 2 AM |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

Together, this runs the backup script every night at exactly 2:00 AM.
