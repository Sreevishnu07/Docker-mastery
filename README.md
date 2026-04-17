# Mastering the Intricacies of DevOps

A structured, hands-on journey into DevOps — focused on internal mechanics, operational clarity, and production-grade workflows.

---

## Introduction

This repository documents a deep exploration of Docker — not just at the command level, but at the architectural level.

The goal is to understand:

* How containers actually work under the hood
* How image layers are constructed and reused
* How networking and storage are implemented
* How Docker integrates into real-world DevOps pipelines

This project follows a disciplined learning loop:

Concept → Practical Implementation → Internal Breakdown → Documentation

Every topic is studied, executed, analyzed, and recorded with intent.

---

## Repository Learning Modules

### Foundations

**1.1**
[Basics of Docker](./basicsdocker.pdf)

**1.2**
[Continuation on My Progress on Docker](./Continuation%20on%20my%20progress%20on%20docker.pdf)

**1.3**
[Docker Intermediates](./Docker%20intermediates.pdf)

---

### Advanced Practice & Deep Exploration

**1.4**
[Docker Practice and Advanced Work – Part 1](./Docker%20Practice%20and%20Advanced%20work-part%201.pdf)

**1.5**
[Advanced Docker and Complete Practice – Part 2](./Advanced%20Docker%20and%20complete%20practice%20Part-2.pdf)

**1.6**
[Advanced Docker and Final Practice](./Advanced%20Docker%20and%20final%20practice.pdf)

---

### Networking and Swarm Practicals

**1.7**
[Docker Networking + Swarm Practicals](./Docker%20Networking%2BSwarm%20practicals.pdf)

---

### Reflection & Learning Evolution

**1.8**
[Mistakes Done and Learnings Made](./Mistakes%20done%20and%20learnings%20made.pdf)

---

## Unit 2: Docker Networking and Swarm

### Introduction

With a strong understanding of standalone containers, the next step is to explore how containers communicate and scale across systems.

This unit focuses on networking fundamentals and extends into distributed orchestration using Docker Swarm. It bridges the gap between single-container execution and multi-node distributed systems.

---

### Core Technical Domains Covered

#### Networking

* Default vs user-defined bridge networks
* Docker embedded DNS
* Container ↔ Container communication
* Host ↔ Container communication
* Port publishing internals

#### Overlay Networking

* Multi-node virtual networking
* Cross-node container communication
* VXLAN-based encapsulation
* Foundation for distributed systems

#### Docker Swarm

* Swarm initialization and cluster formation
* Manager vs Worker node architecture
* Service and task abstraction
* Desired state management

#### Routing Mesh and Ingress

* Routing mesh enabling any node to accept traffic
* Ingress network as the entry point for external requests
* Traffic forwarding to active containers
* Port exposure across all nodes

#### Service Deployment and Discovery

* Service creation using docker service create
* Port publishing using --publish
* DNS-based service discovery
* Communication using service names

#### Scaling and Load Balancing

* Service scaling using replicas
* Automatic load balancing using IPVS
* Traffic distribution across containers
* Fault tolerance and container rescheduling

---

### Internal Understanding Developed

* Difference between containers and services
* How routing mesh forwards requests across nodes
* Why port publishing behaves differently in Swarm
* How overlay networks enable distributed communication
* How Swarm abstracts infrastructure complexity
* How load balancing is implemented at kernel level

---

### Practical Systems Built

* Custom bridge network communication
* Container-to-container DNS resolution
* Backend and database connectivity using service names
* Overlay network creation and usage
* Multi-replica web service deployment
* Load balancing verification using container-specific responses

---

### Swarm in the Bigger Picture

Docker Swarm acts as a bridge between:

* Single-container execution → Distributed systems
* Manual deployment → Automated orchestration
* Static infrastructure → Scalable services

---

## Unit 3: Orchestration with Docker Compose

### Introduction

With a solid understanding of networking and distributed orchestration, the next step is managing structured multi-container applications.

Docker Compose introduces a declarative approach to defining and running multi-container systems.

---

### Repository Learning Modules (Unit 3)

**3.1**
[Complete Docker Compose Practice](./completeDockerComposePractice.pdf)

---

### Core Technical Domains Covered (Compose)

#### Multi-Container Architecture

* Service abstraction
* Container dependency management
* Application-level structuring

#### Networking

* Default Compose network
* Embedded DNS-based service discovery
* Container ↔ Container communication
* Host ↔ Service exposure

#### Storage

* Named volumes in Compose
* Data persistence across services
* Volume lifecycle independence

#### Configuration Management

* Environment variables
* YAML-based infrastructure definition
* Build vs Image strategies

---

### Internal Understanding Developed

* How Compose translates YAML into container runtime instructions
* How Docker automatically provisions networks for services
* How DNS resolution replaces manual linking
* How volumes decouple storage from containers
* How multi-service systems behave during startup and shutdown

---

### Practical Systems Built

* Node.js + MongoDB multi-container setup
* Service communication via internal DNS
* Persistent database using volumes
* Port exposure and request routing

---

### Compose in the Bigger Picture

Docker Compose acts as a bridge between:

* Single-container execution → Structured multi-service systems
* Manual setup → Declarative infrastructure
* Local development → Production-ready architecture

---

## Unit 4: Build Systems with Maven

### Repository Learning Modules (Unit 4)

**4.1**
[Complete Maven Mastery](./Complete%20Maven%20Mastery.pdf)

---

(remaining Maven content unchanged)

---

## Unit 5: CI/CD Pipelines (Automation & Deployment)

### Repository Learning Modules (Unit 5)

**5.1**
[Complete CI/CD Mastery](./Complete-CI-CD-Mastery.pdf)

**5.2**
[CI/CD Pipeline Implementation](./ci-cd-pipeline.pdf)

---

(remaining CI/CD content unchanged)

---

## Unit 6: Jenkins Mastery (CI/CD Orchestration Engine)

### Repository Learning Modules (Unit 6)

**6.1**
[Complete Jenkins Mastery (CI/CD)](./Complete%20Jenkins%20Mastery%28CI-CD%29.pdf)

---

(remaining Jenkins content unchanged)

---

## Core Technical Domains Covered

### Image Engineering

* Layer architecture
* Copy-on-write mechanism
* Build cache invalidation
* Tag mutability vs digest immutability
* Multi-stage builds

### Networking

* Bridge vs overlay networks
* Routing mesh and ingress
* Port publishing internals
* Host ↔ Container communication
* Container ↔ Container communication

### Storage

* Named volumes
* Bind mounts
* Mount masking behavior
* Persistent data lifecycle
* Separation of image, container layer, and volume

### Registry & Distribution

* Docker Hub vs GHCR
* Registry namespaces
* Token-based authentication
* Versioned image publishing
* Semantic versioning strategy

---

## Final Armageddon Deployment

A full production-style integration combining:

* Custom Dockerfile
* ENV configuration
* VOLUME declaration
* EXPOSE instruction
* Semantic tagging (1.0.0, latest)
* Publishing to GHCR
* Persistent storage
* Versioned deployment flow

Demonstrates:

* Image immutability
* Volume persistence across rebuilds
* Registry boundary control
* Deployment reproducibility

---

## Tools & Environment

* Docker Engine
* Alpine & Ubuntu images
* MySQL container deployments
* Git & GitHub
* GitHub Container Registry (GHCR)
* Windows + Git Bash workflow

---

## Philosophy

This repository is not about memorizing commands.

It is about understanding:

* What happens inside the kernel
* How namespaces isolate processes
* How overlay networking routes traffic across nodes
* How registries store image manifests
* Why volumes outlive containers
* How orchestration abstracts infrastructure

Understanding Docker deeply is not about running containers.

It is about understanding what truly happens when you do.

---

## Long-Term Direction

This foundation directly supports:

* CI/CD automation
* Microservices architecture
* Image optimization
* Secure software supply chains
* Kubernetes orchestration

---

## Maintained by

Sreevishnu07

A disciplined journey toward mastering systems, infrastructure, and production-grade software engineering.
