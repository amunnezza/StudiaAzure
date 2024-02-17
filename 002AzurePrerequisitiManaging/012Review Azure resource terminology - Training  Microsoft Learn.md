---
created: 2024-02-15T09:44:44 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/3-review-terminology
author: wwlpublish
---

# Review Azure resource terminology - Training | Microsoft Learn

> ## Excerpt
> Review Azure resource terminology

---
-   3 minutes

If you're new to Azure Resource Manager, there are some terms you might not be familiar with.

-   **resource** - A manageable item that is available through Azure. Some common resources are a virtual machine, storage account, web app, database, and virtual network, but there are many more.
-   **resource group** - A container that holds related resources for an Azure solution. The resource group can include all the resources for the solution, or only those resources that you want to manage as a group. You decide how you want to allocate resources to resource groups based on what makes the most sense for your organization.
-   **resource provider** - A service that supplies the resources you can deploy and manage through Resource Manager. Each resource provider offers operations for working with the resources that are deployed. Some common resource providers are Microsoft.Compute, which supplies the virtual machine resource, Microsoft.Storage, which supplies the storage account resource, and Microsoft.Web, which supplies resources related to web apps.
-   **template** - A JavaScript Object Notation (JSON) file that defines one or more resources to deploy to a resource group. It also defines the dependencies between the deployed resources. The template can be used to deploy the resources consistently and repeatedly.
-   **declarative syntax** - Syntax that lets you state "Here is what I intend to create" without having to write the sequence of programming commands to create it. The Resource Manager template is an example of declarative syntax. In the file, you define the properties for the infrastructure to deploy to Azure.

## Resource providers

Each resource provider offers a set of resources and operations for working with an Azure service. For example, if you want to store keys and secrets, you work with the **Microsoft.KeyVault** resource provider. This resource provider offers a resource type called vaults for creating the key vault.

The name of a resource type is in the format: **{resource-provider}/{resource-type}**. For example, the key vault type is **Microsoft.KeyVault/vaults**.

**Note**

<SPAN STYLE="BACKGROUND:AZURE">Before deploying your resources, you should gain an understanding of the available resource providers. Knowing the names of resource providers and resources helps you define resources you want to deploy to Azure. Also, you need to know the valid locations and API versions for each resource type. </SPAN>


___

## Next unit: Create resource groups

[Continue](https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/4-create-resource-groups/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
