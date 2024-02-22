---
created: 2024-02-20T09:18:41 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/automate-azure-tasks-with-powershell/4-exercise-install-azure-powershell?pivots=windows
author: mikefrobbins
---

# Exercise - Install PowerShell - Training | Microsoft Learn

> ## Excerpt
> Exercise - Install PowerShell

---
-   10 minutes

In this unit, you'll learn how to check the version of **PowerShell** installed on your local machine and install the latest version.

Note

This exercise guides you through creating a local installation of PowerShell tools. The remainder of this module uses the Azure Cloud Shell, so you can leverage the free subscription support in Microsoft Learn. If you prefer, consider this exercise as an optional activity and just review the instructions.

## Windows

Windows PowerShell is included with the Windows operating system; however, we recommend installing PowerShell 7.0.6 LTS, PowerShell 7.1.3, or higher for use with Azure Az PowerShell module PowerShell. You can check which version is installed using the following steps:

1.  In the **System tray search box**, type **PowerShell**. You may have multiple shortcut links:
    
    -   PowerShell 7 (x64) - The 64-bit version. Generally, you should choose this shortcut.
    -   Windows PowerShell - The 64-bit version included with Windows.
    -   Windows PowerShell (x86) - A 32-bit version installed on 64-bit Windows.
    -   Windows PowerShell ISE - The Integrated Scripting Environment (ISE) is used for writing scripts in Windows PowerShell.
    -   Windows PowerShell ISE (x86) - A 32-bit version of the ISE on Windows.
2.  Select the best-match PowerShell icon.
    
3.  Type the following command to determine the version of PowerShell installed.
    
    ```
    <span><span>$PSVersionTable</span>.PSVersion
    </span>
    ```
    
    _or_
    
    ```
    <span>pwsh<span> -ver</span>
    </span>
    ```
    
    If the major version number is lower than 7, follow the instructions to [upgrade existing Windows PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows#upgrading-an-existing-installation). It's important to install the SDK to support .NET tools, as well.
    
    You need the [.NET SDK installed](https://learn.microsoft.com/en-us/dotnet/core/sdk) to run this command.
    
    ```
    <span>dotnet tool install<span> --global</span> PowerShell
    </span>
    ```
    
    After the .NET tool is installed, run the PowerShell version command again to verify your installation.
    

You'll also need to set up your local machine(s) to support PowerShell. In the next unit, we'll review commands you can add, including the Azure Az PowerShell module.

___

## Next unit: Create an Azure Resource using scripts in Azure PowerShell

[Continue](https://learn.microsoft.com/en-us/training/modules/automate-azure-tasks-with-powershell/5-create-resource-interactively/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
