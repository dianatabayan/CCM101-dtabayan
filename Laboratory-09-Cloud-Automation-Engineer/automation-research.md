# Automation Research

## Bash Script
A Bash script is a plain text file containing a list of Linux commands that run one after another, so you don't have to type them by hand each time. The first line, `#!/bin/bash` (called the shebang), tells the system which program should run the file. In this case, it says to use the Bash shell to interpret the commands.

## Variables
A variable stores a value under a name, like `BACKUP_DIR="backups"`, so the script can reuse it by writing `$BACKUP_DIR`. Programmers use variables instead of typing the exact folder path every time because it saves effort and prevents typos. If the path ever changes, you update it in one place instead of editing every line of the script.

## Cron Job
A cron job is a task that the Linux cron scheduler runs automatically at a set time or interval, such as every night at 2:00 AM. It is essential for cloud operations because routine work like backups, log cleanup, and updates must happen reliably without a person remembering to do them. This keeps servers maintained and data protected around the clock.
