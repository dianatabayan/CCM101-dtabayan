# Laboratory 02 – Build the Cloud Infrastructure Blueprint

## Mission Overview
This laboratory simulates the planning phase of a cloud deployment for a fictional company, CloudNova Technologies. Using a Linux server provisioned through the KillerCoda Playground, I investigated the underlying infrastructure, identified its major components, compared how top cloud providers offer equivalent services, and sketched a simple cloud architecture diagram — all documented as a Cloud Infrastructure Assessment Report.

## Objectives
- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationships between cloud infrastructure components.
- Produce professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components
- **Compute** – The processing power (CPU/RAM) that runs applications and workloads. Investigated using `lscpu` and `free -h` on the KillerCoda server.
- **Storage** – Where data is stored persistently or temporarily. Investigated using `df -h`, which revealed partitions such as `/dev/vda1` mounted at `/`.
- **Networking** – Enables communication between systems and the internet. Investigated using `ip a`, which revealed the server's private IP and network interfaces.
- **Identity and Access Management** – Manages access to resources through users, groups, and permissions.
- **Operating System** – Manages hardware and provides the runtime environment. The server runs Ubuntu 24.04.4 LTS, confirmed via `cat /etc/os-release`.

Full details are documented in `cloud-components.md` and `infrastructure-report.md`.

## Tools Used
- KillerCoda Playground (Linux terminal sandbox)
- Git and GitHub (version control and portfolio hosting)
- Markdown (documentation formatting)
- Draw.io (cloud architecture diagram)

## Linux Commands Executed

| Command | Purpose |
|---|---|
| `cat /etc/os-release` | Identify the operating system |
| `uname -r` | Check the kernel version |
| `lscpu` | Examine CPU model and core count |
| `free -h` | Check total, used, and available RAM |
| `df -h` | Examine disk partitions and storage capacity |
| `ip a` | Identify network interfaces and IP addresses |

## Repository Structure
- `README.md` – Laboratory overview (this file)
- `cloud-components.md` – Checkpoint 3: Cloud infrastructure components explained
- `cloud-provider-comparison.md` – Checkpoint 4: AWS vs Azure vs GCP comparison
- `infrastructure-report.md` – Checkpoint 2: Server investigation findings
- `reflection.md` – Checkpoint 6/7: Mission reflection
- `screenshots/` – Supporting screenshots
