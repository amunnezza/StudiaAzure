---
created: 2024-02-23T08:34:09 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/control-azure-services-with-cli/3-exercise-install-and-run-the-azure-cli?pivots=windows
author: dbradish-microsoft
---

# Exercise - Install and run the Azure CLI - Training | Microsoft Learn

> ## Excerpt
> Install the Azure CLI on various platforms

---
-   10 minutes

Let's install the Azure CLI on your local machine, then run a command to verify your installation. The method you use for installing the Azure CLI depends on your computer's operating system. Choose the steps for your operating system.

==Note==

==This exercise guides you through installing the Azure CLI tool locally. The remainder of the module will use the Azure Cloud Shell so you can leverage the free subscription support in Microsoft Learn. You can consider this exercise as an optional activity and just review the instructions if you prefer.==

## Windows

Here, you'll install the Azure CLI on Windows using the MSI installer.

1.  Go to [https://aka.ms/installazurecliwindows](https://aka.ms/installazurecliwindows) and select **Run** or **Open file** in the browser security dialog box.
2.  In the installer, accept the license terms, then select **Install**.
3.  In the **User Account Control** dialog, select **Yes**.

## Running the Azure CLI

You can run the Azure CLI by opening a bash shell (Linux and macOS), or from the command prompt or PowerShell (Windows).

1.  Start the Azure CLI and verify your installation by running the version check.
  
		 ```PowerShell
	    az --version
        ```

Tip

Running the Azure CLI from PowerShell has some advantages over running the Azure CLI from the Windows command prompt. PowerShell provides more tab-completion features than those available from the command prompt.

You've set up your local machines to administer Azure resources with the Azure CLI. You can now use the Azure CLI locally to enter commands or execute scripts. The Azure CLI will forward your commands to the Azure datacenters, where they'll run inside your Azure subscription.

___

## Next unit: Work with the Azure CLI

[Continue](https://learn.microsoft.com/en-us/training/modules/control-azure-services-with-cli/4-work-with-the-cli/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
