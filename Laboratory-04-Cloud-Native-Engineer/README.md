# Laboratory 04 - Cloud Native Engineer

## Mission Overview
This lab covers the fundamentals of containerization with Docker, moving from
theory (how containers differ from virtual machines) into hands-on practice:
verifying a Docker environment, pulling and deploying a real web server image,
and managing the full lifecycle of a running container. The goal is to build a
working understanding of why cloud-native teams use containers to deploy web
applications faster and more efficiently than traditional VM-based setups.

## Objectives
- Understand the architectural differences between Virtual Machines and Containers
- Verify a Docker installation and check the status of the Docker environment
- Pull an official image from Docker Hub and deploy it as a running container
- Manage a container through its full lifecycle: list, stop, verify, and remove
- Document commands, outcomes, and lessons learned throughout the process

## Docker Commands Executed

**Checkpoint 3 — Verify Docker**
```
docker --version
docker info
```

**Checkpoint 4 — Deploy the Nginx Container**
```
docker pull nginx
docker run -d -p 8080:80 --name nginx-web nginx
curl http://localhost:8080
```

**Checkpoint 5 — Container Lifecycle**
```
docker ps
docker stop nginx-web
docker ps -a
docker rm nginx-web
docker ps -a
```

## Skills Learned
- How to verify that Docker is installed and running correctly on a host
- How to pull a pre-built image from Docker Hub instead of building one from scratch
- How port mapping (`-p host:container`) connects traffic from the host machine into an isolated container
- How to manage a container's full lifecycle — listing, stopping, verifying, and removing it — using core Docker CLI commands
- How to document infrastructure work clearly for a client-facing audience

## Challenges Encountered
Getting Git authenticated correctly took a few tries — GitHub no longer accepts
account passwords for Git operations, so a personal access token was needed
instead. There was also a mix-up early on where a file was created outside the
cloned repository (because a `cd` into a not-yet-created folder failed silently
in the background), which meant the folder structure and file had to be rebuilt
before committing. Beyond the Git setup, the Docker commands themselves worked
as expected once the environment was verified.
