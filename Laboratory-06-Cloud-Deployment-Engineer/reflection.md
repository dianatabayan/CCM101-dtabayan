
# Mission Reflection

## 1. How does writing a docker-compose.yml file make a cloud engineer's job easier?
Writing a docker-compose.yml file lets a cloud engineer describe an entire application stack in one file instead of typing long docker run commands for every container. It is repeatable, easy to share with teammates, and can be stored in GitHub as version-controlled documentation. One command starts or stops everything, which saves time and reduces mistakes.

## 2. What happens if you make an indentation error (like using a Tab instead of Spaces) in a YAML file?
YAML uses spaces to show structure, and Tabs are not allowed. If a Tab is used, Docker Compose fails with a parsing error, or services may end up nested in the wrong place, so the deployment will not start until the indentation is fixed. That is why the lab warned that YAML is strictly space-sensitive.

## 3. Why did we use environment variables (like MYSQL_PASSWORD) in the Compose file?
Environment variables pass configuration such as the database name, user, and password into the containers without changing the images. The Nextcloud container and the MariaDB container need matching values so they can connect. The downside is that hardcoding passwords in a file is not safe for real production, where secrets should be handled more securely.

## 4. How did it feel to deploy a fully functional enterprise cloud storage system (Nextcloud) in just a few minutes?
It felt surprising and empowering. A full enterprise-grade storage system was running after one file and one command, which would normally take a lot of manual installation and setup. Fixing the Git token error along the way also showed me that real deployments involve troubleshooting, not just running commands.

## 5. How has your understanding of Cloud Computing evolved since Mission 1?
At the start, I thought cloud computing mostly meant storing files online. Now I understand it is about infrastructure defined as code, containers, multi-tier design, and automation. I can see how services are deployed, tested, and removed quickly, and how documentation and version control are part of an engineer's work.

