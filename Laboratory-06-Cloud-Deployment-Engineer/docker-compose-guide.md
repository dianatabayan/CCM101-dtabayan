# Docker Compose Guide

## The Compose File
```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?
The `services:` block lists every container that makes up the application.
Each entry underneath it (`database` and `app`) becomes its own container,
with its own image, ports, and settings. This lets one file describe the
whole infrastructure.

## How does the Nextcloud app container find the database?
Through the `MYSQL_HOST=database` environment variable. Docker Compose puts
all services on the same network and uses each service's name as its
hostname. Because the database service is named `database`, the app
container can reach MariaDB by using that name instead of an IP address.

## `docker run` vs `docker-compose up -d`
`docker run` starts a single container, and you must type out every option
(image, ports, environment variables) each time. `docker-compose up -d`
reads the YAML file and starts all the defined services together, creating
the shared network automatically. It is repeatable and easier to manage.
Both use `-d` to run in the background (detached mode).
