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

**Concept → Practical Implementation → Internal Breakdown → Documentation**

Every topic is studied, executed, analyzed, and recorded with intent.

---

## Repository Learning Modules

### Foundations

**1.1** [Basics of Docker](./basicsdocker.pdf)
**1.2** [Continuation on My Progress on Docker](./Continuation%20on%20my%20progress%20on%20docker.pdf)
**1.3** [Docker Intermediates](./Docker%20intermediates.pdf)

### Advanced Practice & Deep Exploration

**1.4** [Docker Practice and Advanced Work – Part 1](./Docker%20Practice%20and%20Advanced%20work-part%201.pdf)
**1.5** [Advanced Docker and Complete Practice – Part 2](./Advanced%20Docker%20and%20complete%20practice%20Part-2.pdf)
**1.6** [Advanced Docker and Final Practice](./Advanced%20Docker%20and%20final%20practice.pdf)

### Reflection & Learning Evolution

**1.7** [Mistakes Done and Learnings Made](./Mistakes%20done%20and%20learnings%20made.pdf)

---

## Unit 2: Orchestration with Docker Compose

### Introduction

With a solid understanding of individual containers, the next step is orchestration — managing multiple interconnected services as a single system.

Docker Compose introduces a declarative approach to defining and running multi-container applications.

This unit focuses on:

* Eliminating manual container linking
* Defining entire systems in a single configuration file
* Understanding how Docker internally manages multi-service environments
* Bridging the gap between containerization and orchestration systems like Kubernetes

---

### Repository Learning Modules (Unit 2)

**2.1** [Complete Docker Compose Practice](./completeDockerComposePractice.pdf)

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

* Single-container execution → Distributed systems
* Manual setup → Declarative infrastructure
* Local development → Production-ready architecture

---

## Unit 3: Build Systems with Maven

### Introduction

After mastering containerization and orchestration, the next critical layer is build automation and dependency management.

Apache Maven plays a key role in:

* Structuring Java-based projects
* Managing dependencies efficiently
* Automating builds and packaging
* Integrating seamlessly with Docker-based workflows

---

### Repository Learning Modules (Unit 3)

**3.1** [Complete Maven Mastery](./Complete%20Maven%20Mastery.pdf)

---

### Core Technical Domains Covered (Maven)

#### Project Structure & Lifecycle

* Standard directory layout
* Build lifecycle phases (validate → compile → test → package → install → deploy)
* Maven conventions over configuration

#### Dependency Management

* Transitive dependencies
* Dependency scopes (compile, provided, runtime, test)
* Conflict resolution (nearest definition strategy)

#### Build & Packaging

* JAR vs WAR packaging
* Plugins and goals
* Custom build configurations

#### POM (Project Object Model)

* XML structure and hierarchy
* GroupId, ArtifactId, Version
* Dependency declarations
* Plugin configuration

#### Integration with Docker

* Building artifacts for containerization
* WAR deployment into Tomcat containers
* Clean separation of build and runtime environments

---

### Internal Understanding Developed

* How Maven resolves dependencies from repositories
* How lifecycle phases map to actual build steps
* How plugins extend Maven functionality
* How builds become reproducible and consistent
* How Maven integrates into CI/CD pipelines

---

### Practical Systems Built

* Java Web Application (WAR packaging)
* Deployment on Tomcat using Docker
* Maven-based automated build pipeline
* Clean separation of source → artifact → container

---

### Maven in the Bigger Picture

Maven acts as a bridge between:

* Source code → Deployable artifact
* Manual compilation → Automated builds
* Local development → CI/CD pipelines

---

## Unit 4: CI/CD Pipelines (Automation & Deployment)

### Introduction

After mastering containerization, orchestration, and build systems, the final layer is automation — CI/CD.

CI/CD (Continuous Integration & Continuous Deployment) enables:

* Automated building, testing, and deployment
* Elimination of manual errors
* Faster and consistent delivery pipelines
* Production-grade DevOps workflows

---

### Repository Learning Modules (Unit 4)

**4.1** [Complete CI/CD Mastery](./Complete-CI-CD-Mastery.pdf)
**4.2** [CI/CD Pipeline Implementation](./ci-cd-pipeline.pdf)

---

### Core Technical Domains Covered (CI/CD)

#### Continuous Integration (CI)

* Automated build triggers on code push
* Maven-based build automation
* Dependency resolution in pipelines
* Artifact generation (JAR/WAR)

#### Continuous Deployment (CD)

* Automated Docker image creation
* Image tagging & versioning
* Push to container registry (GHCR/Docker Hub)
* Deployment-ready artifacts

#### Pipeline Architecture

* Workflow definition (GitHub Actions YAML)
* Job → Step execution model
* Event-based triggers (push, pull_request)
* Environment isolation (runners)

#### Docker + CI/CD Integration

* Build Docker images inside pipelines
* Multi-stage builds for optimization
* Registry authentication (tokens)
* Image publishing and version control

#### Automation & Reliability

* Eliminating manual build steps
* Reproducible deployments
* Version-controlled infrastructure
* Failure handling in pipelines

---

### Internal Understanding Developed

* How CI/CD pipelines execute step-by-step on remote runners
* How GitHub Actions converts YAML into executable workflows
* How build → test → package → dockerize → deploy flows work
* How artifacts move across stages
* How authentication enables secure registry access
* How pipelines ensure consistency across environments

---

### Practical Systems Built

* Maven-based automated build pipeline
* Docker image creation inside CI pipeline
* Image push to GitHub Container Registry (GHCR)
* Fully automated CI → CD workflow
* Version-controlled deployment process

---

### CI/CD in the Bigger Picture

CI/CD acts as the bridge between:

* Code → Automated Build → Deployment
* Manual execution → Fully automated pipelines
* Development → Production systems

---

## Unit 5: Jenkins Mastery (CI/CD Orchestration Engine)

### Introduction

After building a strong foundation in CI/CD pipelines, the next step is mastering Jenkins — a powerful automation server used to orchestrate complete DevOps workflows.

This unit focuses on:

* Understanding Jenkins architecture (Controller → Agent model)
* Building and managing CI/CD pipelines
* Integrating Maven and Docker into Jenkins workflows
* Executing distributed builds using agent nodes
* Understanding real-world pipeline execution and debugging

---

### Repository Learning Modules (Unit 5)

**5.1** [Complete Jenkins Mastery (CI/CD)](./Complete%20Jenkins%20Mastery%28CI-CD%29.pdf)

---

### Core Technical Domains Covered (Jenkins)

#### Jenkins Architecture

* Controller (master) vs Agent (node) model
* Distributed build execution
* Label-based node selection
* Workspace allocation per node

#### Pipeline Development

* Declarative pipeline syntax
* Stages and steps
* Post actions (success, failure, always)
* Pipeline structuring and readability

#### Maven Integration

* Tool configuration in Jenkins
* Automated build lifecycle execution
* Artifact generation (JAR/WAR)
* Build reproducibility

#### Docker Integration

* Running Docker commands inside pipelines
* Image build and container execution
* Container lifecycle management via Jenkins
* Debugging containerized applications

#### Distributed Builds (Nodes)

* Creating and configuring Jenkins agents
* Connecting agents using `agent.jar`
* Running pipelines on remote nodes
* Understanding node workspaces and execution flow

---

### Internal Understanding Developed

* How Jenkins schedules and distributes jobs
* How pipelines are executed step-by-step
* How tools like Maven and Docker integrate into CI/CD workflows
* How agent nodes handle execution independently
* How workspace isolation works across nodes
* How failures propagate through pipeline stages

---

### Practical Systems Built

* Jenkins pipeline for Docker command execution
* Maven-based build pipeline
* Maven + Docker integrated pipeline
* Fully automated CI/CD workflow
* Distributed pipeline execution using agent node

---

### Jenkins in the Bigger Picture

Jenkins acts as the bridge between:

* Source Code → Build → Containerization → Deployment
* Individual tools → Unified automation system
* Manual processes → Fully automated DevOps pipelines

---

## Core Technical Domains Covered

### Image Engineering

* Layer architecture
* Copy-on-write mechanism
* Build cache invalidation
* Tag mutability vs digest immutability
* Multi-stage builds

### Networking

* Default vs user-defined bridge networks
* Docker embedded DNS
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
* How overlay filesystems manage layers
* How registries store image manifests
* Why volumes outlive containers
* How version tags affect deployment stability

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

**Sreevishnu07**

A disciplined journey toward mastering systems, infrastructure, and production-grade software engineering.
