---
created: 2024-02-14T09:59:19 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/azure-well-architected-introduction/6-reliability
author: martinekuan
---

# Reliability - Training | Microsoft Learn

> ## Excerpt
> Reliability

---
-   10 minutes

Imagine that you run a clinical system for a healthcare organization. Clinicians and caregivers have little tolerance for downtime. They need to have access to clinical IT systems around the clock to ensure that they're always providing the highest-quality care.

To meet the around-the-clock demands of clinicians, applications must be able to handle failures with minimal impact to their users. How do they keep their applications operational, both for localized incidents and for large-scale disasters?

In this unit, you learn how to include elements from the reliability pillar in your architecture design.

## What is reliability?

In a complex application, any number of things can go wrong at any scale. Individual servers and hard drives can fail. A deployment issue might unintentionally drop all tables in a database. Whole datacenters might become unreachable. A ransomware incident might maliciously encrypt all your data. It's critical that your application stays reliable and can handle both localized and broad-impact incidents.

Designing for reliability includes maintaining uptime through small-scale incidents and temporary conditions like partial network outages. You can ensure that your application handles localized failures by integrating high availability into each component. This application design eliminates single points of failure. Such a design also minimizes the impact of infrastructure maintenance. High-availability designs typically aim to eliminate the impact of incidents quickly and automatically, and to ensure that the system can continue to process requests with little to no effect.

Designing for reliability also focuses on recovery from data loss and from larger-scale disasters. Recovery from these types of incidents often involves active intervention, though automated recovery steps can reduce the time needed to recover. These types of incidents might result in some amount of downtime or permanently lost data. Disaster recovery is as much about careful planning as it is about execution.

Including high availability and recoverability in your architecture design protects your business from financial losses that result from downtime and lost data. They also protect your business from a loss of reputation caused by a loss of trust from your customers.

Architecting for reliability ensures that your application can meet the commitments you make to your customers. You want to ensure that your systems are _available_ to end users and can _recover_ from any failures.

### Build a highly available architecture

For availability, identify the service-level agreement (SLA) to which you're committing. Examine the potential high-availability capabilities of your application relative to your SLA, and identify where you have proper coverage and where you need to make improvements. Your goal is to add redundancy to components of the architecture so that you're less likely to experience an outage.

Examples of high-availability design components include clustering and load balancing:

-   Clustering replaces a single VM with a set of coordinated VMs. When one VM fails or becomes unreachable, services can fail over to another one that can service the requests.
    
-   Load balancing spreads requests across many instances of a service, detecting failed instances and preventing requests from being routed to them.
    

### Build an architecture that can recover from failure

For recoverability, you should perform an analysis that examines your possible data loss and major downtime scenarios. Your analysis should include an exploration of recovery strategies and the cost/benefit tradeoff for each. This exercise gives you important insight into your organization's priorities, and helps clarify the role of your application. The results of your analysis should include these duration values for your application:

-   **Recovery point objective (RPO)**: The maximum duration of acceptable data loss. RPO is measured in units of time, not volume. Examples are "30 minutes of data," "four hours of data," and so on. RPO is about limiting and recovering from data _loss_, not data _theft_.
    
-   **Recovery time objective (RTO)**: The maximum duration of acceptable downtime, where your specification defines "downtime". For example, if the acceptable downtime duration is eight hours if there's a disaster, then your RTO is eight hours.
    

With RPO and RTO defined, you can design backup, restore, replication, and recovery capabilities into your architecture to meet these objectives.

Every cloud provider offers a suite of services and features that you can use to improve your application's availability and recoverability. When possible, use existing services and best practices, and try to resist creating your own.

Hard drives can fail, datacenters can become unreachable, and hackers can attack. It's important that you maintain a good reputation with your customers by using availability and recoverability. Availability focuses on maintaining uptime through conditions like network outages, and recoverability focuses on retrieving data after a disaster.

## Check your knowledge

1.

Suppose you want to increase the availability of your system to provide a better service-level agreement (SLA) to your customers. Which of the following is a guiding principle you can use?

Reduce your target for maximum duration of acceptable data loss.

This action can increase recoverability, but not availability.

Encrypt all data at rest.

**Eliminate single point of failure.**

_Reliability focuses on maintaining service despite temporary conditions and localized failures. Adding redundancy to eliminate single points of failure is a core strategy for improving availability._

2.

Which of the following is affected by your defined recovery point objective (RPO)?

**The frequency of database backups.**

_The recovery point objective (RPO) defines the amount of tolerable data loss. So, the frequency of backups needs to be within this time window, and your defined RPO directly affects it._

The number of regions that data is replicated to.

The number of instances in a database cluster.

The type of load-balancing technology used in your application.

_The type of load-balancing technology used in your application can be an important decision, but your defined RPO doesn't affect it._

Need help? See our [troubleshooting guide](https://learn.microsoft.com/en-us/training/support/troubleshooting?uid=learn.azure-well-architected-introduction.6-reliability&documentId=a4befbd4-97d0-7493-9c8a-ed665687ed45&versionIndependentDocumentId=33dedf42-7fce-c67c-85ae-9569dab53244&contentPath=%2FMicrosoftDocs%2Flearn-pr%2Fblob%2Flive%2Flearn-pr%2Fazure%2Fazure-well-architected-introduction%2F6-reliability.yml&url=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Ftraining%2Fmodules%2Fazure-well-architected-introduction%2F6-reliability&author=martinek) or provide specific feedback by [reporting an issue](https://learn.microsoft.com/en-us/training/support/troubleshooting?uid=learn.azure-well-architected-introduction.6-reliability&documentId=a4befbd4-97d0-7493-9c8a-ed665687ed45&versionIndependentDocumentId=33dedf42-7fce-c67c-85ae-9569dab53244&contentPath=%2FMicrosoftDocs%2Flearn-pr%2Fblob%2Flive%2Flearn-pr%2Fazure%2Fazure-well-architected-introduction%2F6-reliability.yml&url=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Ftraining%2Fmodules%2Fazure-well-architected-introduction%2F6-reliability&author=martinek#report-feedback).
