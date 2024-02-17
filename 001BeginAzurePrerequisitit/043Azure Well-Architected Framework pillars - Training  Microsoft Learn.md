---
created: 2024-02-14T08:33:50 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/azure-well-architected-introduction/2-pillars
author: martinekuan
---

# Azure Well-Architected Framework pillars - Training | Microsoft Learn

> ## Excerpt
> Learn about the five pillars in the Azure Well-Architected Framework.

---
-   10 minutes

The cloud has changed the way organizations solve their business challenges, and how applications and systems are designed. The role of a solution architect isn't limited to delivering business value through the functional requirements of the application. They must also ensure that the solution is designed in ways that are scalable, resilient, efficient, and secure.

Solution architecture is concerned with the planning, design, implementation, and ongoing improvement of a technology system. The architecture of a system must balance and align the business requirements with the technical capabilities that are needed to execute those requirements. The finished architecture is a balance of risk, cost, and capability throughout the system and its components.

## Azure Well-Architected Framework

The Azure Well-Architected Framework is a set of guiding tenets to build high-quality solutions on Azure. There's no one-size-fits-all approach to designing an architecture, but there are some universal concepts that apply regardless of the architecture, technology, or cloud provider.

These concepts aren't all-inclusive, but focusing on them can help you build a reliable, secure, and flexible foundation for your application.

The Azure Well-Architected Framework consists of five pillars:

-   Cost optimization
-   Operational excellence
-   Performance efficiency
-   Reliability
-   Security

![An illustration that shows the pillars of the Azure Well-Architected Framework.](pillars.png)

### Cost optimization

You want to design your cloud environment so that it's cost-effective for operations and development. Identify inefficiency and waste in cloud spending to ensure you're spending money where you can make the greatest use of it.

![An illustration that shows increasing quality, speed, and efficiency while maintaining decreasing costs.](efficiency.png)

### Operational excellence

By taking advantage of modern development practices such as DevOps, you can enable faster development and deployment cycles. You need to have a good monitoring architecture in place so that you can detect failures and problems before they happen or, at a minimum, before your customers notice. Automation is a key aspect of this pillar to remove variance and error while increasing operational agility.

### Performance efficiency

For an architecture to perform well and be scalable, it should properly match resource capacity to demand. Traditionally, cloud architectures accomplish this balance by scaling applications dynamically based on activity in the application. Demand for services changes, so it's important for your architecture to be able to adjust to demand. By designing your architecture with performance and scalability in mind, you provide a great experience for your customers while being cost-effective.

![An illustration that shows how resources in the cloud scale dynamically based on demand, resulting in highly efficient usage. When resources are implemented at a fixed level, it results in inefficient usage during low demand and shortage during high demand.](performance-demand.png)

### Reliability

Every architect's worst fear is having an architecture fail with no way to recover it. A successful cloud environment is designed in a way that anticipates failure at all levels. Part of anticipating failures is designing a system that can recover from a failure within the time that your stakeholders and customers require.

![An illustration that shows two virtual machines in a virtual network. One of the machines is shown as failed, while the other is working to service customer requests.](system-failure.png)

### Security

Data is the most valuable piece of your organization's technical footprint. In this pillar, you focus on securing access to your architecture through authentication and protecting your application and data from network vulnerabilities. You should also protect the integrity of your data through tools like encryption.

You must think about security throughout the entire lifecycle of your application, from design and implementation to deployment and operations. The cloud provides protections against various threats, such as network intrusion and DDoS attacks. But you still need to build security into your application, processes, and organizational culture.

![An illustration that shows the types of security threats and attacks that might affect your data in the cloud.](security.png)

## General design principles

In addition to each of these pillars, there are some consistent design principles that you should consider throughout your architecture.

-   **Enable architectural evolution**: No architecture is static. Allow for the evolution of your architecture by taking advantage of new services, tools, and technologies when they're available.
    
-   **Use data to make decisions**: Collect data, analyze it, and use it to make decisions surrounding your architecture. From cost data, to performance, to user load, using data can guide you to make the right choices in your environment.
    
-   **Educate and enable**: Cloud technology evolves quickly. Educate your development, operations, and business teams to help them make the right decisions and build solutions to solve business problems. Document and share configurations, decisions, and best practices within your organization.
    
-   **Automate**: Automation of manual activities reduces operational costs, minimizes error introduced by manual steps, and provides consistency between environments.
    

Moving to the cloud introduces a model of shared responsibility. In this model, your cloud provider manages certain aspects of your application, leaving you with the remaining responsibility.

In an on-premises environment, you're responsible for everything. As you move to infrastructure as a service (IaaS), then to platform as a service (PaaS) and software as a service (SaaS), your cloud provider takes on more of this responsibility.

This shared responsibility plays a role in your architectural decisions, because these decisions can have implications on cost, security, and your application's technical and operational capabilities. By shifting these responsibilities to your provider, you can focus on bringing value to your business and move away from activities that aren't a core business function.

![An illustration that shows the level of shared responsibilities in each type of cloud-service model.](cloud-responsibility-model.png)

## Design choices

In an ideal architecture, you'd build the most secure, high-performance, highly available, and efficient environment possible. However, as with everything, there are tradeoffs.

To build an environment with the highest level of all these pillars, there's a cost. That cost might be in money, time to deliver, or operational agility. Every organization has different priorities that affect the design choices that are made in each pillar. As you design your architecture, you need to determine which trade-offs are acceptable and which aren't.

When you're building an Azure architecture, there are many considerations to keep in mind. You want your architecture to be secure, scalable, available, and recoverable. To make that possible, you have to make decisions based on cost, organizational priorities, and risk.
