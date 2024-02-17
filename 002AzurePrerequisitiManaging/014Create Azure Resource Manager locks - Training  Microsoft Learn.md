---
created: 2024-02-15T12:40:18 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/5-create-locks
author: wwlpublish
---

# Create Azure Resource Manager locks - Training | Microsoft Learn

> ## Excerpt
> Create Azure Resource Manager locks

---
-   3 minutes

A common concern with resources provisioned in Azure is the ease with which they can be deleted. An over-zealous or careless administrator can accidentally erase months of work with a few steps. Resource Manager locks allow organizations to put a structure in place that prevents the accidental deletion of resources in Azure.

-   You can associate the lock with a subscription, resource group, or resource.
-   Locks are inherited by child resources.

![Screenshot of the Management locks page. In the Settings options, Locks are highlighted and in the Add Lock page, the Lock type, Ready-only, and Delete option are displayed and highlighted.](Create%20Azure%20Resource%20Manager%20locks%20-%20Training%20%20Microsoft%20Learn/resource-manager-locks-853635fd.png)

## Lock types

There are two types of resource locks.

-   **Read-Only locks**, which prevent any changes to the resource.
-   **Delete locks**, which prevent deletion.

Note

Only the Owner and User Access Administrator roles can create or delete management locks.

___

## Next unit: Reorganize Azure resources

[Continue](https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/6-reorganize-azure-resources/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
