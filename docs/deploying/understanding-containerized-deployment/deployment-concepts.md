---
id: deployment-concepts
title: Deployment Concepts
sidebar_label: Deployment Concepts
---

Alfresco Content Services deployment introduces a number of concepts.

The way you deploy and run Alfresco Content Services has changed significantly since version 6.0. Traditionally, you'd download an installer that installed Java, Tomcat, Database, WARs, tools, etc. and everything was configured to work together out-of-the-box. Then you'd use a script to start things off. That's no longer the case and there are no installers available. We'll be working with Docker containers instead.

You can start Alfresco Content Services from a number of Docker images. These images are available in the Docker Hub and Quay repositories. However, starting individual Docker containers based on these images, and configuring them to work together might not be the most productive way to get up and running. To make things easier, and achieve a single-step deploy and run solution, a Docker Compose file is available to quickly start Alfresco Content Services when you need to test something or work on a proof-of-concept (PoC).

There are also Helm charts available to deploy Alfresco Content Services in a Kubernetes cluster, for example, on Amazon Web Services (AWS). These charts are a deployment template which can be used as the basis for your specific deployment needs. The Helm charts are undergoing continual development and improvement and should not be used "as-is" for a production deployment, but should help you save time and effort deploying Alfresco Content Services for your organisation.

The following is a list of concepts and technologies that you'll need to understand as part of deploying and using Alfresco Content Services. If you know all about Docker, then you can skip this part.

**Virtual Machine Monitor (Hypervisor)**

A Hypervisor is used to run other OS instances on your local host machine. Typically it's used to run a different OS on your machine, such as Windows on a Mac. When you run another OS on your host it is called a guest OS, and it runs in a Virtual Machine (VM).

**Image**

An image is a number of layers that can be used to instantiate a container. This could be, for example, Java and Apache Tomcat. You can find all kinds of Docker images on the public repository Docker Hub. There are also private image repositories (for things like commercial enterprise images), such as the one Alfresco uses called Quay.

**Container**

An instance of an image is called a container. If you start this image, you have a running container of this image. You can have many running containers of the same image.

**Docker**

Docker is one of the most popular container platforms. Docker provides functionality for deploying and running applications in containers based on images.

**Docker Compose**

When you have many containers making up your solution, such as with Alfresco Content Services, and you need to configure each individual container so that they all work well together, then you need a tool for this. Docker Compose is such a tool for defining and running multi-container Docker applications locally. With Compose, you use a YAML file to configure your application's services. Then, with a single command, you create and start all the services from your configuration.

**Dockerfile**

A Dockerfile is a script containing a successive series of instructions, directions, and commands which are run to form a new Docker image. Each command translates to a new layer in the image, forming the end product. The Dockerfile replaces the process of doing everything manually and repeatedly. When a Dockerfile finishes building, the end result is a new image, which you can use to start a new Docker container.