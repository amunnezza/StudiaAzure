---
created: 2024-02-15T09:42:13 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/2-review-benefits
author: wwlpublish
---

# Review Azure Resource Manager benefits - Training | Microsoft Learn

> ## Excerpt
> Review Azure Resource Manager benefits

---
-   3 minutes

The infrastructure for your application is typically made up of many components – maybe a virtual machine, storage account, and virtual network, or a web app, database, database server, and third-party services. These components are not separate entities, instead they are related and interdependent parts of a single entity. You want to deploy, manage, and monitor them as a group.

Azure Resource Manager enables you to work with the resources in your solution as a group. You can deploy, update, or delete all the resources for your solution in a single, coordinated operation. You use a template for deployment and that template can work for different environments such as testing, staging, and production. Azure Resource Manager provides security, auditing, and tagging features to help you manage your resources after deployment.

## Consistent management layer

Azure Resource Manager provides a consistent management layer to perform tasks through Azure PowerShell, Azure CLI, Azure portal, REST API, and client SDKs. Choose the tools and APIs that work best for you.

The following image shows how all the tools interact with the same Azure Resource Manager API. The API passes requests to the Azure Resource Manager service, which authenticates and authorizes the requests. Azure Resource Manager then routes the requests to the appropriate resource providers.

![Diagram of the Resource Manager request model.](Review%20Azure%20Resource%20Manager%20benefits%20-%20Training%20%20Microsoft%20Learn/resource-manager-016a1bac.png)

## Benefits

Azure Resource Manager provides several benefits:

-   You can deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.
-   You can repeatedly deploy your solution throughout the development lifecycle and have confidence your resources are deployed in a consistent state.
-   You can manage your infrastructure through declarative templates rather than scripts.
-   You can define the dependencies between resources so they're deployed in the correct order.
-   You can apply access control to all services in your resource group because Role-Based Access Control (RBAC) is natively integrated into the management platform.
-   You can apply tags to resources to logically organize all the resources in your subscription.
-   You can clarify your organization's billing by viewing costs for a group of resources sharing the same tag.

## Guidance

The following suggestions help you take full advantage of Azure Resource Manager when working with your solutions.

-   Define and deploy your infrastructure through the declarative syntax in Azure Resource Manager templates, rather than through imperative commands.
-   Define all deployment and configuration steps in the template. You should have no manual steps for setting up your solution.
-   Run imperative commands to manage your resources, such as to start or stop an app or machine.
-   Arrange resources with the same lifecycle in a resource group. Use tags for all other organizing of resources.

___

## Next unit: Review Azure resource terminology

[Continue](https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/3-review-terminology/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
