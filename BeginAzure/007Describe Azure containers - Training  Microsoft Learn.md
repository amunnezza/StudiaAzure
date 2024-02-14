---
created: 2024-02-08T16:30:49 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/5-containers
author: wwlpublish
---

# Describe Azure containers - Training | Microsoft Learn

> ## Excerpt
> Describe Azure containers

---
-   6 minutes

While virtual machines are an excellent way to reduce costs versus the investments that are necessary for physical hardware, they're still limited to a single operating system per virtual machine. If you want to run multiple instances of an application on a single host machine, containers are an excellent choice.

## What are containers?

Containers are a virtualization environment. Much like running multiple virtual machines on a single physical host, you can run multiple containers on a single physical or virtual host. Unlike virtual machines, you don't manage the operating system for a container. Virtual machines appear to be an instance of an operating system that you can connect to and manage. Containers are lightweight and designed to be created, scaled out, and stopped dynamically. It's possible to create and deploy virtual machines as application demand increases, but containers are a lighter weight, more agile method. Containers are designed to allow you to respond to changes on demand. With containers, you can quickly restart if there's a crash or hardware interruption. One of the most popular container engines is Docker, and Azure supports Docker.

## Compare virtual machines to containers

The following video highlights several of the important differences between virtual machines and containers:
![[video001.mp4]]
Transcript.
>>In this video, we'll discuss the difference between virtual machines and containers.
So let's begin. Deploying server applications has always been complicated.
That complexity drove system admins to start looking
at virtualization techniques, like virtual machines and containers.

Virtual machines, or VMs, provide an abstraction layer for CPU, memory, and storage

that can be changed without having to invest in new hardware,
while still allowing the environment to be flexible and secure.

With VMs, you're in control.
You decide the operating system, install tools and packages.
And your app runs either in isolation or with the other apps you install into the VM.
But there are downsides. VMs can only run one operating system at a time.
So if you have multiple server apps that all require different runtime environments,
they may also require multiple virtual machines to execute properly.
And because the VM is emulating a full computer,
tasks like starting one up or taking a snapshot are pretty slow, often taking several minutes.
But there's a lighter-weight solution that solves some of these issues. Containers.
A container bundles a single app and its dependencies,
referred to as containerizing the app, then deploys it as a unit to a container host.
The container host provides a standardized runtime environment,
which abstracts away the operating system and infrastructure requirements,
allowing the containerized application to run side-by-side with other containerized apps.

An easy way to differentiate between VMs and containers is
virtual machines virtualize the hardware,
while containers virtualize the operating system.

The operating system level virtualization of containers is one reason
why the container approach is more efficient than a full virtual machine.
It allows you to run multiple lightweight containers on a single host
without sacrificing the isolation that the virtual machine originally offered.
Azure supports several container variations, the most popular being Docker.
Unlike VMs, you can spin up containers quickly.
You're just waiting for the app to launch instead of both the operating system and the app.
Also, containerized apps tend to be much smaller in size.
And the development process is simplified, because your
development runtime environment can look exactly like the production environment.
Another advantage to containers is that they
can be orchestrated with container cluster orchestration.
You can easily deploy and manage multiple containerized applications
without worrying about which server will host each container.
The decision of whether to use a VM or a container depends on how much flexibility you need.
If you need to completely control the environment, then you might choose a VM.
If not then the portability, performance characteristics, and management capabilities of containers might be the better choice.

Il video si trova in Azure/video1.mp4 fuori dal repository perche occupa troppo spazio

### Azure Container Instances

Azure Container Instances offer the fastest and simplest way to run a container in Azure; without having to manage any virtual machines or adopt any additional services. Azure Container Instances are a platform as a service (PaaS) offering. Azure Container Instances allow you to upload your containers and then the service will run the containers for you.

### Azure Container Apps

Azure Container Apps are similar in many ways to a container instance. They allow you to get up and running right away, they remove the container management piece, and they're a PaaS offering. Container Apps have extra benefits such as the ability to incorporate load balancing and scaling. These other functions allow you to be more elastic in your design.

### Azure Kubernetes Service

Azure Kubernetes Service (AKS) is a container orchestration service. An orchestration service manages the lifecycle of containers. When you're deploying a fleet of containers, AKS can make fleet management simpler and more efficient.

### Use containers in your solutions

Containers are often used to create solutions by using a microservice architecture. This architecture is where you break solutions into smaller, independent pieces. For example, you might split a website into a container hosting your front end, another hosting your back end, and a third for storage. This split allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently.

Imagine your website back-end has reached capacity but the front end and storage aren't being stressed. With containers, you could scale the back end separately to improve performance. If something necessitated such a change, you could also choose to change the storage service or modify the front end without impacting any of the other components.

___

## Next unit: Describe Azure functions

[Continue](https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/6-functions/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
