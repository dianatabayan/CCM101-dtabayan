# Laboratory 09 - Cloud Automation Engineer

## Mission Overview
In this lab, I acted as a cloud automation engineer for CloudNova Technologies. I wrote a Bash script that automatically backs up client data into a compressed file, made it executable, and scheduled it with a cron job to run every night at 2:00 AM.

## Objectives
- Set up the lab folder structure in my GitHub portfolio
- Research Bash scripts, variables, and cron jobs
- Create a backup script using variables and the `tar` command
- Fix the "Permission denied" error using `chmod +x`
- Schedule the script to run automatically with cron
- Document the work for the client's IT team and reflect on what I learned

## Commands Executed
```bash
# Create the dummy client data
mkdir app-data
echo "This is critical client data." > app-data/data.txt

# Create the script
nano backup.sh

# Permissions and execution
./backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/

# Schedule the cron job
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

## Skills Learned
- Writing a Bash script with variables and a shebang line
- Compressing folders into timestamped backups with `tar`
- Managing file permissions with `chmod`
- Scheduling recurring tasks with cron
- Documenting technical work in Markdown for a client team
