---
created: 2024-02-13T10:52:55 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/microsoft-cloud-adoption-framework-for-azure/6-adopt
author: Zimmergren
---

# Adopt - Training | Microsoft Learn

> ## Excerpt
> Adopt

---
-   7 minutes

At this point, you've established your business justification and defined your business outcomes. You've prepared your organization. Your people and your Azure environment are ready to deploy your prioritized applications. You're ready to adopt cloud technologies following the selected digital estate rationalization path.

As discussed, your organization has unique motivations to adopt the cloud. They all converge into _migration_ or _innovation_ to the cloud.

![Icon indicating play video](Adopt%20-%20Training%20%20Microsoft%20Learn/video-icon.png)

![[ADOPT.mp4]]Watch this video to learn more.
transcript
<span style="background:cyan">
Adopt is divided into two different optionsâ€”migrate and

innovate. If you would like to migrate your workload, a lift

and shift is probably the easiest way to get your assets

into the cloud. Although the lift and shift may be a great

starting point, it may provide the least value for your cloud

adoption in the long run. That is where innovate can

provide real value.

When migrating your assets, make sure you evaluate

your assets and establish a migration plan. Prerequisites

such as a landing zone and quantitative factors like

networking and compatibility are things to include. Also,

you want to assess any process dependencies or business

events for your workload.

Rehost is also known as lift and shift, and this relatively

simple effort moves the current state to Azure. You can

also utilize the Azure migration guide to help you choose

the migration method and features that you can use to

govern and secure the environment.

While your initial migration might use the rehost model,

you will still want to optimize and transform your services.

Make sure you balance performance and price, delivering

the right experience within budget.

Once you have migrated your environment to Azure,

you will need to address the security and methods

required to manage your environment for ongoing

operations.

Innovate is the second option around adopt. If you are

interested in taking full advantage of the cloud, innovate

may be the best way to achieve your goals. If you want to

achieve a global scale, agility, security, or autoscaling,

innovate can help you maximize the value of your cloud

adoption. We mentioned the 5Rs earlierâ€”rehost, refactor,

rearchitect, rebuild, and replaceâ€”and this is where you will

determine the best option for your migration.

Refactor may be one of your best options if you are able to

do a simple move from IaaS to PaaS. It may reduce the

operational costs associated with your application.

You may be able to maximize benefits by moving some of

your workloads into containers with rearchitect.

The rebuild approach can provide a new born-in-the cloud

application that can really provide value in your cloud adoption.

These two journeys represent two extremes of experience

for customers who invest in cloud migration. Most

companies reflect a combination of the two scenarios

above. After reviewing the journeys, use the cloud adoption

framework migration model to start the migration conversation

and modify the baseline journeys to more closely meet

your needs.
</SPAN>

  

## Cloud migration

Cloud migration is the process of moving existing digital assets to a cloud platform. Existing assets are replicated to the cloud with minimal modifications. After an application or workload becomes operational in the cloud, users are transitioned from the existing solution to the cloud solution.

![Icon of lightbulb](Adopt%20-%20Training%20%20Microsoft%20Learn/lightbulb.png)

_Cloud migration is one way to effectively balance a cloud portfolio. This is often the fastest and most agile approach in the short term. Conversely, some benefits of the cloud might not be realized without additional future modification. Enterprises and mid-market customers use this approach to accelerate the pace of change, avoid planned capital expenditures, and reduce ongoing operational costs._

The strategy and tools you use to migrate an application to Azure largely depend on your business motivations, technology strategies, and timelines. Your decisions are also based on a deep understanding of the application and the assets to be migrated. These assets include infrastructure, apps, and data. This decision tree serves as high-level guidance to help you select the best tools to use based on migration decisions.

**Migration preparation:** Establish a rough migration backlog, based largely on the current state and desired outcomes.

-   **Business outcomes:** The key business objectives that drive this migration. They're defined in the Plan phase.
-   **Digital estate estimate:** A rough estimate of the number and condition of workloads to be migrated. It's defined in the Plan phase.
-   **Roles and responsibilities:** A clear definition of the team structure, separation of responsibilities, and access requirements. They're defined in the Ready phase.
-   **Change management requirements:** The cadence, processes, and documentation required to review and approve changes. They're defined in the Ready phase.

## Cloud innovation

Cloud-native applications and data accelerate development and experimentation cycles. Older applications can take advantage of many of the same cloud-native benefits by modernizing the solution or components of the solution. Modern DevOps and software development lifecycle (SDLC) approaches that use cloud technology shorten the time from idea to product transformation. Combined, these tools invite the customer into the process to create shorter feedback loops and better customer experiences.

Modern approaches to infrastructure deployment, operations, and governance are rapidly bridging the gaps between development and operations. Modernization and innovation in the IT portfolio create tighter alignment with DevOps and accelerate innovations across the digital estate and application portfolio.

![Icon of key](Adopt%20-%20Training%20%20Microsoft%20Learn/key-takeaway.png)

Here are the key points from this unit:

-   Cloud migration is the process of moving existing digital assets to a cloud platform. Adopt is divided into two different options, migrate and innovate.
-   Each cloud migration activity is contained during one of the following processes, as it relates to the migration backlog: assess, migrate, optimize, and secure. Then, you manage each backlog asset.
-   Modernization and innovation in the IT portfolio create tighter alignment with DevOps and accelerate innovations across the digital estate and application portfolio.

You've learned how to plan, get ready, and start to deploy your first applications to the cloud. Now let's talk about governance and management in the cloud.

Need help? See our [troubleshooting guide](https://learn.microsoft.com/en-us/training/support/troubleshooting?uid=learn-wwl.microsoft-cloud-adoption-framework-for-azure-v1-1.6-ready&documentId=9518d89b-2635-454d-15ab-3b4f3ec743be&versionIndependentDocumentId=39cf84c7-1040-f0e6-c3a9-9fe7ca369dcf&contentPath=%2FMicrosoftDocs%2Flearn-pr%2Fblob%2Flive%2Flearn-pr%2Fwwl-mba%2Fmicrosoft-cloud-adoption-framework-for-azure%2F6-adopt.yml&url=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Ftraining%2Fmodules%2Fmicrosoft-cloud-adoption-framework-for-azure%2F6-adopt&author=tozimmergren) or provide specific feedback by [reporting an issue](https://learn.microsoft.com/en-us/training/support/troubleshooting?uid=learn-wwl.microsoft-cloud-adoption-framework-for-azure-v1-1.6-ready&documentId=9518d89b-2635-454d-15ab-3b4f3ec743be&versionIndependentDocumentId=39cf84c7-1040-f0e6-c3a9-9fe7ca369dcf&contentPath=%2FMicrosoftDocs%2Flearn-pr%2Fblob%2Flive%2Flearn-pr%2Fwwl-mba%2Fmicrosoft-cloud-adoption-framework-for-azure%2F6-adopt.yml&url=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Ftraining%2Fmodules%2Fmicrosoft-cloud-adoption-framework-for-azure%2F6-adopt&author=tozimmergren#report-feedback).


