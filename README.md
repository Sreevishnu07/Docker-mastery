# Docker Basics

This branch documents a structured exploration of fundamental Docker concepts through hands-on experimentation and analysis.

The objective is to build operational clarity around how containers function, how services are exposed, and how host-container interaction is managed.

## Core Areas Covered

- Running and managing containers
- Image fundamentals and layering
- Port publishing
- Bind mounts
- Executing commands inside running containers

## Port Publishing

Port publishing enables external access to services running inside a container.

Using:

docker run -p <host_port>:<container_port> image_name

A container’s internal port is mapped to a port on the host machine. This allows applications (such as web servers) running inside containers to be accessed via `localhost:<host_port>`.

This mechanism is essential for development, testing, and service exposure.

## Bind Mounts

Bind mounts link a directory from the host system to a directory inside the container.

docker run -v /host/path:/container/path image_name

This creates a live synchronization between host and container filesystems. Changes made on either side are reflected immediately.

Bind mounts are commonly used for:
- Source code sharing during development
- Persisting data
- Avoiding repeated image rebuilds

## Executing Commands in Running Containers

To interact with a running container:

docker exec -it <container_name> bash

This allows inspection, debugging, and real-time interaction with the container’s environment without restarting it.

It is a critical tool for understanding container state and behavior.

## Purpose

This branch is maintained as a focused study of Docker fundamentals, forming the foundation for more advanced containerization and DevOps workflows.
