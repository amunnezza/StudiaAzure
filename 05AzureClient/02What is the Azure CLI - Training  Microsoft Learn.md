---
created: 2024-02-23T08:37:06 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/control-azure-services-with-cli/2-what-is-the-azure-cli
author: dbradish-microsoft
---

# What is the Azure CLI? - Training | Microsoft Learn

> ## Excerpt
> Learn about the Azure CLI and the basics of installing it on each platform.

---
-   3 minutes

The Azure CLI is a command-line program to connect to Azure and execute administrative commands on Azure resources. It runs on Linux, macOS, and Windows, and allows administrators and developers to execute their commands through a terminal or command-line prompt (or script) instead of a web browser. For example, to restart a virtual machine (VM), you'd use the following command:

```PowerShell
az vm restart -g MyResourceGroup -n MyVm

```

The Azure CLI provides cross-platform command-line tools for managing Azure resources, and you can easily install it locally on Linux, Mac, or Windows computers. You can also use the Azure CLI from a browser through the Azure Cloud Shell. In both cases, you can use it interactively or scripted. For interactive use, you'll first launch a shell (such as cmd.exe on Windows or Bash on Linux or macOS), then issue the command at the shell prompt. To automate repetitive tasks, you'll assemble the CLI commands into a shell script using the script syntax of your chosen shell, then execute the script.

## How to install the Azure CLI

On both Linux and macOS, you'll use a package manager to install the Azure CLI. The recommended package manager differs by OS and distribution:

-   Linux: **apt-get** on Ubuntu, **yum** on Red Hat, and **zypper** on OpenSUSE
-   Mac: **Homebrew**

The Azure CLI is available in the Microsoft repository, so you'll first need to add that repository to your package manager.

On Windows, you can install the Azure CLI by downloading and running an MSI file.

## Using the Azure CLI in scripts

If you want to use the Azure CLI commands in scripts, you need to be aware of any issues around the "shell" (or environment) used for running the script. For example, in a Bash shell, you'll use this syntax when setting variables:

```bash
variable="value"
variable=integer

```

If you use a PowerShell environment for running Azure CLI scripts, you'll use this syntax for variables:

```PowerShell
$variable="value"
$variable=integer

```

You must install the Azure CLI before you can use it to manage Azure resources from a local computer. The installation steps vary for Windows, Linux, and macOS, but once installed, the commands are common across platforms.

___

## Next unit: Exercise - Install and run the Azure CLI

[Continue](https://learn.microsoft.com/en-us/training/modules/control-azure-services-with-cli/3-exercise-install-and-run-the-azure-cli/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
