# Mission Reflection

## 1. How does a host-based firewall protect a server even if the physical network perimeter is breached?
A host-based firewall runs on the server itself, so it checks every connection no matter where it comes from. If an attacker gets past the network perimeter, such as the office router or the cloud network firewall, they still have to get through the rules on the server. With a Default Deny policy, any traffic I did not explicitly allow is dropped. This gives me a second layer of defense instead of relying on one wall.

## 2. Why is managing open network ports critical to reducing a server's attack surface?
Every open port is a door into the server, and each one is tied to a service that could have bugs or weak passwords. The more ports are open, the more places an attacker can probe. By opening only port 22 for SSH and port 8080 for the web app, I kept the attack surface small. Closing unused ports means there is nothing there to attack.

## 3. Why is it dangerous to leave a database port like 3306 open to the public internet?
Attackers constantly scan the internet for open database ports. If MySQL is exposed, they can try password guessing, exploit known vulnerabilities, or steal and delete data directly. A database should only be reachable by the application servers that need it, usually through a private network or a firewall rule limited to specific IP addresses.

## 4. How did completing this mission change your perspective on how easily a server can be compromised?
Before this lab, I assumed a server was safe as long as it was running properly. I learned that a server with default settings can be wide open, and that a small mistake, like enabling the firewall before allowing SSH, can lock out even the owner. Security needs deliberate setup and careful ordering of steps.

## 5. How does your GitHub portfolio currently look with eight completed missions?
My portfolio now has eight organized lab folders, each with a README, documentation, and screenshots as proof of my work. It shows my progress from basic cloud concepts to security, and it feels like a real record of skills I could show to an employer.
