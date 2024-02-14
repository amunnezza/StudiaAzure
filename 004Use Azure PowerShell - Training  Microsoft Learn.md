---
created: 2024-02-14T22:23:44 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/configure-azure-resources-tools/4-use-azure-powershell
author: wwlpublish
---

# Use Azure PowerShell - Training | Microsoft Learn

> ## Excerpt
> Use Azure PowerShell

---
-   3 minutes

Azure PowerShell is a module that you add to Windows PowerShell or PowerShell Core to enable you to connect to your Azure subscription and manage resources. Azure PowerShell requires PowerShell to function. PowerShell provides services such as the shell window and command parsing. Azure PowerShell adds the Azure-specific commands.

For example, Azure PowerShell provides the **New-AzVm** command that creates a virtual machine inside your Azure subscription. To use it, you would launch the PowerShell application and then issue a command such as the following command:

**New-AzVm `
   -ResourceGroupName "CrmTestingResourceGroup" `
   -Name "CrmUnitTests" `
   -Image "UbuntuLTS"
   ...
**

Azure PowerShell is also available two ways: inside a browser via the Azure Cloud Shell, or with a local installation on Linux, macOS, or the Windows operating system. In both cases, you have two modes from which to choose: you can use it in interactive mode in which you manually issue one command at a time, or in scripting mode where you execute a script that consists of multiple commands.

**What is the Az module?**

**Az** is the formal name for the Azure PowerShell module containing cmdlets to work with Azure features. It contains hundreds of cmdlets that let you control nearly every aspect of every Azure resource. You can work with the following features, and more:

-   Resource groups
-   Storage
-   VMs
-   Microsoft Entra ID
-   Containers
-   Machine learning

This module is an open-source component [available on GitHub](https://github.com/Azure/azure-powershell).

Note

You might have seen or used Azure PowerShell commands that used an **\-AzureRM** format. In December 2018 Microsoft released for general availability the AzureRM module replacement with the Az module. This new module has several features, notably a shortened cmdlet noun prefix of **\-Az**, which replaces **AzureRM**. The **Az** module ships with backwards compatibility for the AzureRM module, so the **\-AzureRM** cmdlet format will work.

Bookmark the [Azure PowerShell Reference](https://learn.microsoft.com/en-us/powershell/azure/?view=azps-6.5.0).

___

## Next unit: Interactive lab simulation (Azure PowerShell)

[Continue](https://learn.microsoft.com/en-us/training/modules/configure-azure-resources-tools/5-simulation-powershell/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
