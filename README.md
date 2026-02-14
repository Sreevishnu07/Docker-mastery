# Mastering the Intricacies of Docker

> A structured, hands-on journey into Docker — focused on internal mechanics, operational clarity, and production-grade workflows.

---

## Introduction

This repository documents a deep exploration of Docker — not just at the command level, but at the architectural level.

The goal is to understand:

- How containers actually work under the hood  
- How image layers are constructed and reused  
- How networking and storage are implemented  
- How Docker integrates into real-world DevOps pipelines  

This project follows a disciplined learning loop:

**Concept → Practical Implementation → Internal Breakdown → Documentation**

Every topic is studied, executed, analyzed, and recorded with intent.

---

## Repository Structure

### `main`
Stable documentation, structured insights, and consolidated understanding.

### `basics`
Foundational Docker concepts explored through focused experimentation.

Core themes:
- Running and managing containers  
- Image fundamentals and layering  
- Port publishing (`-p`)  
- Bind mounts  
- Executing commands inside running containers  

This branch builds operational clarity around container lifecycle, host-container interaction, and basic exposure of services.

---

### `intermediates-of-docker-mastery`
Applied and scenario-driven Docker workflows integrating networking, storage, registries, and image management.

This branch focuses on realistic multi-component setups and deployment-oriented thinking.

---

## Intermediates: Activities & Experiments

### 1. Dockerizing MySQL with Custom Image and Port Publishing
- Built a custom MySQL container with environment configuration.
- Published container port to host and validated connectivity.
- Explored container isolation vs host exposure boundaries.

---

### 2. Container-to-Container Communication Using Custom Dockerfiles and Bridge Network
- Created multiple containers with custom images.
- Connected them via a user-defined bridge network.
- Verified internal DNS-based name resolution and isolated communication.

---

### 3. Implementing Persistent Storage in Docker Using Volumes (MySQL Example)
- Attached named volumes to database container.
- Demonstrated data persistence across container removal.
- Observed separation between image layers and persistent storage.

---

### 4. Demonstrating Bind Mounts in Docker and Comparing with Named Volumes
- Mounted host directories into containers.
- Compared lifecycle, control, and risks of bind mounts vs named volumes.
- Analyzed how mount masking overrides image filesystem content.

---

### 5. DNS Resolution Inside User-Defined Bridge
- Verified automatic service discovery via container names.
- Explored how Docker’s embedded DNS works.
- Compared default bridge vs user-defined bridge behavior.

---

### 6. Building, Tagging, and Publishing a Docker Image to GitHub Container Registry with Token-Based Authentication
- Built versioned images using semantic tagging.
- Authenticated using GitHub Personal Access Tokens.
- Pushed and pulled images from GHCR, enforcing access control.
- Understood registry boundaries and tag mutability.

---

### 7. FINAL ARMAGEDDON: Deploying a Versioned Web App with Persistent Storage and Publishing to GHCR (Content Registry)
- Wrote production-style Dockerfile using `ENV`, `VOLUME`, `EXPOSE`, `CMD`.
- Applied semantic versioning (`1.0.0`, `latest`) and analyzed tag behavior.
- Integrated networking, port mapping, volumes, and registry workflows in a single cohesive deployment.
- Demonstrated image immutability vs volume persistence across rebuilds and redeployments.

---

## Core Technical Domains Covered

### Image Engineering
- Layer architecture
- Copy-on-write mechanism
- Build cache invalidation strategy
- Tag mutability and digest immutability
- Multi-stage build principles

### Networking
- Bridge networks (default and user-defined)
- Container DNS resolution
- Port publishing mechanics
- Host-to-container and container-to-container flow

### Storage
- Named volumes
- Bind mounts
- Persistent data lifecycle
- Mount masking behavior
- Separation of image, container layer, and volume

### Registry & Distribution
- Docker Hub vs GHCR
- Registry namespaces
- Token-based authentication
- Private image access control
- Versioned deployment strategy

---

## Tools & Environment

- Docker Engine  
- Alpine and Ubuntu-based images  
- MySQL containers  
- Git & GitHub  
- Windows + Git Bash workflow  

---

## Philosophy

This repository is not about memorizing,

It is about understanding:
- What happens inside the kernel
- How namespaces isolate processes
- How overlay filesystems manage layers
- How registries store image manifests
- Why volumes outlive containers
- How version tags control deployment stability

---

## Long-Term Direction

This foundation directly supports:

- CI/CD automation  
- Microservices architecture  
- Image optimization  
- Secure software supply chains  
- Container orchestration (Kubernetes)  

---

## Final Note

This is not a collection of Docker commands.

This is a structured mastery of containerization principles.

Understanding Docker deeply is not about running containers.

It is about understanding what truly happens when you do.
