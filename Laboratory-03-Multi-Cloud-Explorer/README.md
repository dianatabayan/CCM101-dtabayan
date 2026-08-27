## Linux Server Investigation
Operating System: Ubuntu 24.04.4 LTS (checked using lsb_release -a) CPU Information: Intel Xeon E312xx (Sandy Bridge, IBRS update), 1 core (checked using lscpu) Memory: 1.9 GiB total RAM (checked using free -h) Disk Space: 19 GB total disk space on the main partition (checked using df -h)
Cloud Migration

Your Linux investigation is good. Here is a cleaner version you can use:

## Cloud Migration

Since this Linux server has only **1 CPU core, 1.9 GiB of RAM, and 19 GB of storage**, it is suitable for a small virtual machine on any of the three major cloud platforms.

* **AWS – Amazon EC2:** A small instance such as **t3.micro** can be used for lightweight workloads.
* **Azure – Azure Virtual Machines:** A small VM such as **B1s** can be used for low-traffic applications.
* **GCP – Compute Engine:** A small machine type such as **e2-micro** can be used for lightweight workloads.

### Recommended Choice

**Amazon EC2** would be a good choice because it supports Ubuntu and offers small, flexible virtual machine options for low-resource applications.

## Terminal Output

<img width="957" height="730" alt="Screenshot 2026-08-27 7 35 38 PM" src="https://github.com/user-attachments/assets/bc4d022f-520f-41de-b10d-c6e08fa767c9" />
<img width="957" height="556" alt="Screenshot 2026-08-27 7 35 58 PM" src="https://github.com/user-attachments/assets/e782e9b9-ea24-4351-bc8b-9b1560aef328" />
