# Docker

- Containerization platform that allows developers to package applications and their dependencies into standardized, portable units called containers.

## Why use docker

1. Consistency Across Environments

   Ensures the app runs the same way in development, testing, staging, and production. Eliminates the `"It works on my machine!"` problem.

2. Portability

   Containers are platform-independent (Linux, Windows, macOS) and can run on any system with Docker installed.
   Easily shareable via Docker Hub or private registries.

3. Isolation

   Each container runs in its own isolated environment with its own file system, networking, and process space.
   Prevents dependency conflicts between applications.

4. Fast Startup & Lightweight

   Containers start in seconds (vs. minutes for VMs) because they share the host OS kernel.
   Lower resource overhead than full VMs.

5. Scalability & Orchestration

   Works seamlessly with orchestration tools like Kubernetes, Docker Swarm, or Nomad.
   Enables easy horizontal scaling and load balancing.

6. DevOps & CI/CD Integration

   Simplifies continuous integration/continuous deployment pipelines.
   Build once, deploy anywhere.

7. Large Ecosystem & Community

   Vast library of pre-built images on Docker Hub.
   Strong documentation, tutorials, and third-party tooling.

## Docker Execution With CLI

- <span style="font-weight: bold">docker images</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Check all images

- <span style="font-weight: bold">docker ps -a </span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Check all containers status

- <span style="font-weight: bold">docker pull [images]</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Pull a images from dockerhub

- <span style="font-weight: bold">docker volume ls</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Listing all containers internal storage

- <span style="font-weight: bold">docker volume rm [volume]</span>&nbsp;&nbsp;# Delete the storage by name

- <span style="font-weight: bold">docker run [parameters]</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Establish container and whole the entire terminal

- <span style="font-weight: bold">docker run [parameters] -d</span>&nbsp;&nbsp;# Establish container and run to background

- <span style="font-weight: bold">docker [contianer] start </span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Start the container by name or ID

- <span style="font-weight: bold">docker [container] stop</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Stop the container by name or ID

- <span style="font-weight: bold">docker stats [container]</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Show the docker containers resource usage

## Docker Execution With Docker Compose

- <span style="font-weight: bold">docker compose -f [yaml file] up -d </span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Create containers base on file setting and run to background

- <span style="font-weight: bold">docker compose -f [yaml file] down</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Destroy containers base on file setting

- <span style="font-weight: bold">docker compose -f [yaml file] start</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Start containers base on file setting

- <span style="font-weight: bold">docker compose -f [yaml file] stop</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Stop containers base on file setting

- <span style="font-weight: bold">docker compose -f [yaml file] ps</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Listing containers status base on file setting

# Reference

- [Docker cli](https://docs.docker.com/reference/cli/docker/)
- [Docker Compose](https://docs.docker.com/reference/compose-file/)
