# Firewall Configuration

## Commands Used

**Allow SSH:**
```bash
sudo ufw allow ssh
```

**Set the Default Deny policy:**
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

**Allow Port 8080:**
```bash
sudo ufw allow 8080/tcp
```

## What would happen if `sudo ufw enable` ran before `sudo ufw allow ssh`?
The firewall would start with a default deny policy and no rule allowing port 22, so it would block my SSH connection and lock me out of my own server.
