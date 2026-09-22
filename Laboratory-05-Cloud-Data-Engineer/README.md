### Laboratory 05: Cloud Data Engineer

# Mission Overview

In this mission, I worked as a **cloud data engineer** for a client who needed a reliable solution for storing user-uploaded images. I researched the three main types of cloud storage—**block, file, and object storage**—and evaluated their common use cases. I then deployed a **MinIO object storage server** using Docker and accessed its web console to create a bucket and upload a sample file.

## Objectives

* Compare **block, file, and object storage** and explain why object storage is suitable for user-uploaded images.
* Deploy a **MinIO server** using Docker in a KillerCoda Ubuntu Playground.
* Access the **MinIO web console**, create a storage bucket, and upload a sample file.
* Document the deployment process, troubleshooting steps, and key learnings from the mission.

## Tools and Technologies Used

* **Docker** — Used to deploy and run the MinIO container.
* **MinIO** — Used as an S3-compatible object storage server.
* **KillerCoda Ubuntu Playground** — Used as the Linux environment for the deployment.
* **Linux Command Line** — Used to execute Docker commands and manage the container.
* **Git and GitHub** — Used to organize and store the project documentation.
* **Markdown** — Used to create the technical documentation.

## Skills Learned

Through this mission, I developed the following skills:

* Understanding the differences between **block, file, and object storage** and their appropriate use cases.
* Deploying a containerized application using `docker run`, including **port mapping and environment variables**.
* Troubleshooting common Docker issues, including **image pull errors and container name conflicts**.
* Managing **buckets and objects** using the MinIO web console.
* Creating clear and structured **technical documentation using Markdown**.
* Organizing deployment evidence and project files in a GitHub repository.

## Repository Contents

The repository contains the following files and folders:

* **`storage-types-research.md`** — Comparison of block, file, and object storage, including the recommended use case for user-uploaded images.
* **`minio-deployment.md`** — MinIO deployment process, configuration, troubleshooting steps, and verification.
* **`reflection.md`** — Personal reflection on the mission and the skills gained.
* **`screenshots/`** — Screenshots showing the successful MinIO deployment, bucket creation, and file upload.
