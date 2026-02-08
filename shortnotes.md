# Docker Basics — Short Notes

## 1. What is Docker?

Docker is a **containerization platform** that packages an application along with its dependencies and runtime environment into **containers**, enabling consistent execution across different systems.

Docker provides **OS-level isolation** while sharing the host operating system kernel.

## 2. Problem Docker Solves

Traditional software deployment suffers from:
- Environment mismatches
- Dependency conflicts
- Inconsistent runtime behavior across systems

Docker solves this by shipping the **application + environment** together.

## 3. Docker Architecture (High Level)

- **Docker CLI**: User-facing command-line tool  
- **Docker Engine (dockerd)**: Background daemon that manages images, containers, networks, and volumes  
- **Docker Registry**: Remote storage for Docker images (e.g., Docker Hub)

## 4. Docker Image

### Definition
A **Docker image** is a **read-only, immutable, layered template** that contains:
- Application code
- Dependencies
- Runtime
- OS user-space files
- Metadata (CMD, ENTRYPOINT, ENV)

Images are used to create containers.

### Properties
- Immutable
- Layered
- Content-addressable
- Shared across containers

### Image vs Container

| Image | Container |
|------|----------|
| Static | Running |
| Blueprint | Instance |
| Read-only | Has writable layer |
| Stored on disk | Uses CPU & RAM |

## 5. Image Layers

- Images are composed of multiple **read-only layers**
- Each layer represents a filesystem change
- Layers are shared between images
- Only missing layers are downloaded during `docker pull`

This makes Docker storage-efficient and fast.

## 6. Writable Layer

Each container gets a **thin writable layer** on top of image layers.

### Purpose
Stores runtime changes such as:
- File creation
- File modification
- Logs
- Temporary files

### Important Notes
- Writable layer is **container-specific**
- Deleted when the container is removed
- Not suitable for persistent data (use volumes)

## 7. Docker Container

### Definition
A **Docker container** is a running instance of a Docker image with:
- Its own namespaces
- Its own writable layer
- Resource limits enforced by cgroups

A container exists as long as its **PID 1 process** exists.

## 8. `docker run` Lifecycle

Conceptually, `docker run` performs:
1. Pull image (if not present)
2. Create container
3. Start container

If the main process exits, the container stops.

Example:
```bash
docker run httpd echo "Hello"
