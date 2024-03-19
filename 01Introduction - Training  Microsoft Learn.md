---
created: 2024-02-28T16:52:46 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/create-azure-resource-manager-template-vs-code/1-introduction
author: tfitzmac
---

# Introduction - Training | Microsoft Learn

> ## Excerpt
> Introduction.

---
-   2 minutes

JSON Azure Resource Manager templates (ARM templates) allow you to specify your project's infrastructure in a declarative and reusable way. You can version and save the templates in the same source control as your development project.

Suppose you're managing a software team that's developing an inventory system for your partner companies. You plan to deploy this product to Azure, and let each partner company have its own solution. You plan to implement different policies for each deployment through different Azure storage accounts. You decide to use the practice of _infrastructure as code_ by using ARM templates. This approach lets you track the different versions and ensure that your infrastructure deployments for each environment are consistent and flexible.

In this module, we introduce you to ARM template structure and let you practice creating and deploying an ARM template to Azure.

Note

Bicep is a language for defining your Azure resources. It has a simpler authoring experience than JSON, along with other features that help improve the quality of your infrastructure as code. We recommend that anyone new to infrastructure as code on Azure use Bicep instead of JSON. To learn about Bicep, see the [Fundamentals of Bicep](https://learn.microsoft.com/en-us/training/paths/fundamentals-bicep/) learning path.

## Learning objectives

In this module, you will:

-   Implement a JSON ARM template by using Visual Studio Code.
-   Declare resources and add flexibility to your template by adding parameters and outputs.

## Prerequisites

-   Familiarity with Azure, including the Azure portal, subscriptions, resource groups, and resource definitions.
-   An Azure account. You can get a free account [here](https://azure.microsoft.com/free).
-   [Visual Studio Code](https://code.visualstudio.com/) installed locally.
-   The [Azure Resource Manager Tools for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=msazurermtools.azurerm-vscode-tools) extension installed locally.
-   Either:
    -   The latest [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) tools installed locally.
    -   The latest [Azure PowerShell](https://learn.microsoft.com/en-us/powershell/azure/install-az-ps) installed locally.

___

## Next unit: Explore Azure Resource Manager template structure

[Continue](https://learn.microsoft.com/en-us/training/modules/create-azure-resource-manager-template-vs-code/2-explore-template-structure/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
