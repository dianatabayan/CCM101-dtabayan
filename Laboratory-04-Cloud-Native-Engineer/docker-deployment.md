# Docker Deployment

## Container Lifecycle Commands

| Command | What It Did |
|---|---|
| `docker ps` | Listed all currently running containers, showing that `nginx-web` was up and mapped to port 8080. |
| `docker stop nginx-web` | Gracefully stopped the `nginx-web` container, shutting down the Nginx process inside it without deleting the container itself. |
| `docker ps -a` | Listed all containers including stopped ones, confirming `nginx-web` now showed a status of "Exited" instead of "Up". |
| `docker rm nginx-web` | Permanently deleted the stopped `nginx-web` container, freeing its resources; running `docker ps -a` again afterward confirmed it no longer appeared in the list at all. |
