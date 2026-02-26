# Mastering the Intricacies of Docker

A structured, hands-on journey into Docker — focused on internal mechanics, operational clarity, and production-grade workflows.

---

## Introduction

This repository documents a deep exploration of Docker — not just at the command level, but at the architectural level.

The goal is to understand:

- How containers actually work under the hood  
- How image layers are constructed and reused  
- How networking and storage are implemented  
- How Docker integrates into real-world DevOps pipelines  

This project follows a disciplined learning loop:

> **Concept → Practical Implementation → Internal Breakdown → Documentation**

Every topic is studied, executed, analyzed, and recorded with intent.

---

# Repository Learning Modules

## Foundations

-  [Basics of Docker](./basicsdocker.pdf)
-  [Continuation on My Progress on Docker](./Continuation%20on%20my%20progress%20on%20docker.pdf)
-  [Docker Intermediates](./Docker%20intermediates.pdf)

---

## Advanced Practice & Deep Exploration

-  [Docker Practice and Advanced Work – Part 1](./Docker%20Practice%20and%20Advanced%20work-part%201.pdf)
-  [Advanced Docker and Complete Practice – Part 2](./Advanced%20Docker%20and%20complete%20practice%20Part-2.pdf)
-  [Advanced Docker and Final Practice](./Advanced%20Docker%20and%20final%20practice.pdf)

---

##  Reflection & Learning Evolution

-  [Mistakes Done and Learnings Made](./Mistakes%20done%20and%20learnings%20made.pdf)

This document highlights:
- Conceptual misunderstandings corrected
- Internal behavior clarifications
- Architectural refinements in understanding

---

#  Core Technical Domains Covered

##  Image Engineering
- Layer architecture
- Copy-on-write mechanism
- Build cache invalidation
- Tag mutability vs digest immutability
- Multi-stage builds

##  Networking
- Default vs user-defined bridge networks
- Docker embedded DNS
- Port publishing internals
- Host ↔ Container communication
- Container ↔ Container communication

##  Storage
- Named volumes
- Bind mounts
- Mount masking behavior
- Persistent data lifecycle
- Separation of image, container layer, and volume

##  Registry & Distribution
- Docker Hub vs GHCR
- Registry namespaces
- Token-based authentication
- Versioned image publishing
- Semantic versioning strategy

---

#  Final Armageddon Deployment

A full production-style integration combining:

- Custom Dockerfile
- ENV configuration
- VOLUME declaration
- EXPOSE instruction
- Semantic tagging (1.0.0, latest)
- Publishing to GHCR
- Persistent storage
- Versioned deployment flow

Demonstrates:
- Image immutability
- Volume persistence across rebuilds
- Registry boundary control
- Deployment reproducibility

---

#  Tools & Environment

- Docker Engine
- Alpine & Ubuntu images
- MySQL container deployments
- Git & GitHub
- GitHub Container Registry (GHCR)
- Windows + Git Bash workflow

---

#  Philosophy

This repository is not about memorizing commands.

It is about understanding:

- What happens inside the kernel
- How namespaces isolate processes
- How overlay filesystems manage layers
- How registries store image manifests
- Why volumes outlive containers
- How version tags affect deployment stability

Understanding Docker deeply is not about running containers.

It is about understanding what truly happens when you do.

---

#  Long-Term Direction

This foundation directly supports:

- CI/CD automation
- Microservices architecture
- Image optimization
- Secure software supply chains
- Kubernetes orchestration

---

##  Maintained by
**Sreevishnu07**

A disciplined journey toward mastering systems, infrastructure, and production-grade software engineering.
