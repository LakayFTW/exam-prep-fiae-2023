# Table of Content
- [Table of Content](#table-of-content)
- [Docker vs VM](#docker-vs-vm)
  - [Docker](#docker)
  - [Virtual Machine](#virtual-machine)
  - [Brief Explanation](#brief-explanation)
- [Further on Docker](#further-on-docker)
  - [Basics](#basics)
  - [Terms](#terms)
    - [Image](#image)
    - [Container](#container)
    - [Layer](#layer)
    - [Dockerfile](#dockerfile)
    - [Repository](#repository)
    - [Registry](#registry)
  - [Setting Up Docker on Linux (Ubuntu)](#setting-up-docker-on-linux-ubuntu)
    - [Repository Setup](#repository-setup)
    - [Installing Docker Engine](#installing-docker-engine)
- [Hypervisor](#hypervisor)

# Docker vs VM

## Docker
A Docker container shares the kernel of the host system, allowing multiple isolated applications to run on a single operating system.

## Virtual Machine

A VM is a complete, independent operating system or guest operating system running on a host operating system. Resources such as processor, memory, and networks are distributed to the VM.

## Brief Explanation

VMs provide full virtualization, where a standalone operating system runs in an isolated environment.
Docker containers offer lightweight, application-based virtualization where applications run in isolated containers.
The choice between the two depends on specific requirements, resource consumption, and application portability.

# Further on Docker
[^6] [^9]<br>
Docker is a free software for isolating applications using containerization.
<br><br>

Docker simplifies the deployment of applications because containers containing all necessary packages can be easily transported and installed as files. Containers ensure the separation and management of resources used on a computer. According to the developers, this includes: code, runtime module, system tools, system libraries - everything that can be installed on a computer.
<br>

<img title="Docker Architecture" src="../img/Docker/architecture.svg"><br>
[^8]

## Basics
Docker is based on Linux techniques such as __Cgroups__ and __Namespaces__ to realize containers. While initially the LXC interface of the Linux kernel was used, the Docker developers have since developed their own programming interface called __libcontainer__, which is also available to other projects.
<br>

Normally, Docker is oriented towards virtualization with Linux, but it can also be used on Windows or macOS using __HyperV__, __Virtualbox__, __HyperKit__, or __VirtualBox__.

## Terms
### Image
A snapshot of a container. The image itself consists of several layers that are read-only and cannot be changed. An image is portable, can be stored in repositories, and shared with other users. Several containers can always be started from an image.

### Container
A container is the active instance of an image. The container is currently running and busy. Once the container stops running a program or completes its task, the container is automatically terminated.

### Layer
A layer is a part of an image and contains a command or file that was added to the image. The whole history of the image can be traced back using the layers.

### Dockerfile
A text file that describes an image with various commands. These are processed during execution, and a separate layer is created for each command.

### Repository
A repository is a set of identically named images with different tags, usually versions.

### Registry
A registry, such as __Docker Hub__ or __Artifactory__, is used to manage repositories.

## Setting Up Docker on Linux (Ubuntu)
[^7]

### Repository Setup
1. "Update the __apt__ package index and install packages to allow apt to use a repository over HTTPS:"

    ```sh
    $ sudo apt update
    ```

    ```sh
    $ sudo apt-get install \
     ca-certificates \
     curl \
     gnupg \
     lsb-release 
    ```

2. "Add Docker’s official GPG key:"

    ```sh
    $ sudo mkdir -m 0755 -p /etc/apt/keyrings
    $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
    ```

3. "Use the following command to set up the repository:"
    ```sh
    $ echo \
     "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
     $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```

### Installing Docker Engine
1. "Update the package index:"
    ```sh 
    $ sudo apt-get-update
    ```
2. "Install Docker Engine, containerd, and Docker Compose:"
    ```sh
    $ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    ```

3. "Verify that the Docker Engine is successful by running `hello-world` image:"
    ```sh
    $ sudo docker run hello-world
    ```

# Hypervisor
[^5]
A hypervisor or Virtual Machine Monitor (VMM) is the term for a class of systems in practical computer science that serves as an abstracting layer between actual hardware and additional operating systems to be installed.

A hypervisor allows the simultaneous operation of multiple guest systems on a host system. The hypervisor manages resource allocation for individual guest systems.

[^5]: https://en.wikipedia.org/wiki/Hypervisor
[^6]: https://en.wikipedia.org/wiki/Docker_(software)
[^7]: https://docs.docker.com/engine/install/ubuntu/
[^8]: https://docs.docker.com/assets/images/architecture.svg
[^9]: https://docs.docker.com/get-started/overview/
