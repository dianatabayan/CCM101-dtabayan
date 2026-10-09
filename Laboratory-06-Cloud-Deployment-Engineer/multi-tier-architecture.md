# Multi-Tier Architecture

## What is a Two-Tier Architecture?
A two-tier architecture splits an application into two separate layers,
each with its own responsibility. One layer handles the application and
user-facing logic, and the other layer handles data storage. The two tiers
communicate over a network connection.

## The Web/Application Tier
This tier serves the user interface and handles HTTP requests from users.
It runs the application logic, such as logging in, uploading files, and
sharing them. In this mission, the Nextcloud container is the
web/application tier.

## The Database Tier
This tier stores persistent data, such as user accounts, passwords, and
file metadata, so the information is kept even when the application
restarts. In this mission, the MariaDB container is the database tier.

## Why Separate Them?
Separating the web server and the database makes each part easier to
manage and secure. If Nextcloud needs updating or crashes, the MariaDB
container and its data are not affected. The database can also be hidden
from the public and reachable only by the application container, which
reduces security risks. Finally, each tier can be scaled or replaced
independently as CloudNova's needs grow.
