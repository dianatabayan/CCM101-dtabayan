# Cloud Infrastructure Components

## Compute Resources
**Purpose:** Compute resources are the processing power (CPU) and memory (RAM) that execute tasks, run applications, and process data.

**Importance in Cloud Computing:** Compute is the resource cloud providers let users scale up or down on demand — a level of flexibility fixed physical hardware can't match.

**Relation to the KillerCoda Linux Environment:** `lscpu` and `free -h` show the server running on an Intel Xeon E312xx CPU with 1.9 GiB of RAM. This mirrors how a provider like AWS provisions a virtual instance with a defined amount of vCPU and memory for a user.

## Storage Resources
**Purpose:** Storage resources hold data, files, and system information, either temporarily (in RAM) or persistently (on disk).

**Importance in Cloud Computing:** Reliable, scalable storage lets applications save and retrieve data on demand, and ensures that data survives even when compute instances are stopped or restarted.

**Relation to the KillerCoda Linux Environment:** `df -h` shows the server's disk partitions — `/dev/vda1` (19G), mounted at `/` as the root filesystem, alongside `/boot` and `/boot/efi` for system boot files. These function as the persistent storage layer of the virtual server, comparable to block storage volumes (e.g., AWS EBS) attached to a cloud VM.

## Networking Resources
**Purpose:** Networking resources let servers communicate with each other, with users, and with the internet, through IP addressing, interfaces, and routing.

**Importance in Cloud Computing:** Networking ties compute and storage together and exposes services to the outside world — without it, cloud resources would be isolated and unreachable.

**Relation to the KillerCoda Linux Environment:** `ip a` reveals three interfaces: `enp1s0`, assigned a private IP (172.30.1.2/24) for external communication; `lo`, the loopback interface (127.0.0.1) for internal traffic; and `docker0` (172.17.0.1) for container networking. This setup parallels how cloud VMs receive private/public IPs and virtual network interfaces.

## Operating System
**Purpose:** The operating system manages hardware resources, runs processes, and provides the environment in which applications and services operate.

**Importance in Cloud Computing:** The OS is the foundation that lets compute, storage, and networking resources be accessed and managed consistently across virtual machines and cloud instances.

**Relation to the KillerCoda Linux Environment:** `cat /etc/os-release` confirms the server runs Ubuntu 24.04.4 LTS — a lightweight, stable, long-term-support distribution supported by all major cloud providers.
