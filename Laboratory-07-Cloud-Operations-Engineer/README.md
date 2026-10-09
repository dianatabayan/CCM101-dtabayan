# Laboratory 07: Cloud Operations Engineer

## Mission Overview
In this laboratory, I acted as a Cloud Operations Engineer responsible for keeping a client's web service healthy. I established a baseline for the host server's health, deployed an Nginx web server in a Docker container, generated traffic to it, and then monitored the container using its application logs and real-time resource metrics.

## Objectives
- Organize the lab deliverables in a structured folder in my GitHub repository.
- Establish a baseline of the host server's RAM, disk storage, and CPU load.
- Deploy a containerized Nginx web server and simulate user traffic, including a failed request.
- Retrieve and interpret application logs to trace what happened.
- Monitor the container's CPU and memory usage in real time.
- Reflect on why monitoring matters for reliable cloud operations.

## Monitoring Commands Executed
- `free -h`: checked the server's current memory (RAM) usage.
- `df -h`: checked the server's available disk storage.
- `top`: viewed active processes and CPU load in the task manager.
- `docker run`: deployed the Nginx container named client-website on port 8080.
- `curl http://localhost:8080`: simulated user visits to the website.
- `curl http://localhost:8080/hidden-admin-page`: triggered a 404 Not Found error.
- `docker logs client-website`: retrieved the container's application logs.
- `docker stats`: viewed the container's live CPU, memory, and network usage.

## Skills Learned
- Reading host-level metrics (RAM, disk, CPU) to judge server health.
- Deploying and running a containerized web server with Docker.
- Generating test traffic with curl and reading HTTP status codes (200 and 404).
- Using container logs to troubleshoot errors.
- Using docker stats to monitor resource consumption.
- Documenting work clearly and committing it to GitHub.
