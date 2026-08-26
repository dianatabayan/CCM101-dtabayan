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

Operating System:

CPU Information:

Memory:

Disk Space:
