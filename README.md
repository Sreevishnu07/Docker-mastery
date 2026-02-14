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
# Mastering the Intricacies of Docker

> A deep dive into understanding Docker beyond surface-level commands — focusing on architecture, networking, storage, and real-world workflows.

---

## Vision

This repository is dedicated to mastering Docker from fundamentals to advanced concepts.  
The goal is not just to *use* Docker — but to understand:

- How containers actually work
- What happens under the hood
- How networking, volumes, and isolation are implemented
- How Docker fits into real-world DevOps workflows

---

## What This Repository Covers

### Core Concepts
- Containers vs Virtual Machines
- Images and Layers
- Docker Architecture (Client, Daemon, Registry)
- Namespaces and cgroups (Linux foundations)

### Practical Docker
- Writing Dockerfiles
- Building and tagging images
- Running and managing containers
- Environment variables
- Port mapping and networking

### Storage & Data Management
- Volumes
- Bind mounts
- Persistent storage
- Data lifecycle management

### Advanced Topics
- Multi-stage builds
- Container networking internals
- Image optimization strategies
- Debugging containers
- Production-ready practices

---

## Branch Structure

- `main` → Stable or general-purpose branch
- `basics` → Active learning and experimentation branch

Each branch may contain structured notes, experiments, and applied examples.

---

## Learning Approach

This project follows a:

- Concept → Experiment → Breakdown → Optimization approach

Every concept explored is:
1. Understood theoretically
2. Implemented practically
3. Analyzed for internal behavior
4. Documented clearly

---

## Tools & Environment

- Docker Engine
- Ubuntu-based containers
- Git & GitHub
- Windows + Git Bash workflow

---

## Why This Matters

Docker is not just a tool — it is foundational to:

- Modern DevOps
- CI/CD pipelines
- Microservices architecture
- Cloud-native systems

Mastering Docker deeply builds a strong foundation for scalable system design.

---

## Ongoing Improvements

This repository will continuously evolve as new concepts, optimizations, and real-world experiments are explored.

---

## Contributions

Currently maintained as a structured self-learning repository.  
Future enhancements may include advanced orchestration topics (Kubernetes, container scaling, etc.).

---

## Final Note

This is not just about running `docker run`.

This is about understanding what truly happens when you do.
