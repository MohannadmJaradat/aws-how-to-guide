# Amazon ECS Mini Project

A hands-on mini project for learning Amazon Elastic Container Service (ECS) with AWS Fargate.

## Key Concepts

### Virtual Machines vs Containers

- **Hypervisor**: Enables running multiple virtual machines on the same hardware. Each VM includes a Guest OS, Service Runtime, and the application — making them heavier and slower to start.
- **Containers**: Share the host's hardware *and* OS. A container engine (e.g., Docker) sits on top, running isolated processes called containers. Each container packages only the application and its runtime, making containers lightweight and fast.
- **Dockerfile**: Each instruction in a Dockerfile creates a new layer in the image.

### ECS Core Components

| Component | Description |
|---|---|
| **Task Definition** | The blueprint for your application. Defines the base image, IAM roles, container definitions, networking mode, CPU/memory, storage volumes, and exposed ports. |
| **ECS Cluster** | A logical grouping of containers. Where you configure the VPC, subnets, and infrastructure parameters. |
| **ECS Service** | Manages the lifecycle and scalability of your running tasks (containers). |

### ECS Fargate Networking

In ECS Fargate, tasks run in a shared AWS-managed environment outside your VPC. AWS injects **Elastic Network Interfaces (ENIs)** directly into your VPC, which act as the bridge between your VPC and the running containers.

## Project Contents

- `ritual-roast-code.zip` — Application source code used in this project.
