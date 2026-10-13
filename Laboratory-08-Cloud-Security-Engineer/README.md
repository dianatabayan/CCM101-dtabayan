# Laboratory 08 - Cloud Security Engineer

## Mission Overview
In this lab, I acted as a cloud security engineer. I deployed an Nginx web server in a container on a Killercoda Ubuntu playground, then secured it with UFW (Uncomplicated Firewall) using a Default Deny policy and opened only the ports that were needed.

## Objectives
- Set up the lab folder structure in my GitHub portfolio
- Research and define key security concepts (Least Privilege, Attack Surface, Default Deny)
- Deploy a containerized Nginx web application on port 8080
- Configure UFW to block all incoming traffic by default
- Allow only SSH (port 22) and web traffic (port 8080)
- Document the configuration and reflect on what I learned

## Commands Executed
```bash
# Deploy the application
docker run -d --name secure-web-app -p 8080:80 nginx
curl http://localhost:8080

# Build the firewall
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose

# Open the web port
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
```

## Skills Learned
- Applying the Principle of Least Privilege and reducing the attack surface
- Using UFW to create a Default Deny firewall
- Allowing specific ports without exposing the whole server
- Verifying firewall rules with `ufw status` and `curl`
- Documenting technical work in Markdown and organizing it on GitHub
