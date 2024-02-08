---
created: 2024-02-08T10:19:23 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/3-exercise-create-azure-virtual-machine
author: wwlpublish
---

# Exercise - Create an Azure virtual machine - Training | Microsoft Learn

> ## Excerpt
> Exercise - Create an Azure virtual machine

---
-   10 minutes

In this exercise, you create an Azure virtual machine (VM) and install Nginx, a popular web server.

You could use the Azure portal, the Azure CLI, Azure PowerShell, or an Azure Resource Manager (ARM) template.

In this instance, you're going to use the Azure CLI.

## Task 1: Create a Linux virtual machine and install Nginx

Use the following Azure CLI commands to create a Linux VM and install Nginx. After your VM is created, you'll use the Custom Script Extension to install Nginx. The Custom Script Extension is an easy way to download and run scripts on your Azure VMs. It's just one of the many ways you can configure the system after your VM is up and running.

1.  From Cloud Shell, run the following `az vm create` command to create a Linux VM:
    
    ```
    <span><span>az vm create </span>\
      <span>--resource-group</span> <span>"[sandbox resource group name]"</span> \
      <span>--name</span> my<span>-vm</span> \
      <span>--public-ip-sku</span> Standard \
      <span>--image</span> Ubuntu2204 \
      <span>--admin-username</span> azureuser \
      <span>--generate-ssh-keys</span>    
    </span>
    ```
    
    Your VM will take a few moments to come up. You named the VM **my-vm**. You use this name to refer to the VM in later steps.
    
2.  Run the following `az vm extension set` command to configure Nginx on your VM:
    
    ```
    <span><span>az vm extension set </span>\
      <span>--resource-group</span> <span>"[sandbox resource group name]"</span> \
      <span>--vm-name</span> my<span>-vm</span> \
      <span>--name</span> customScript \
      <span>--publisher</span> Microsoft.Azure.Extensions \
      <span>--version</span> <span>2.1</span> \
      <span>--settings</span> <span>'{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}'</span> \
      <span>--protected-settings</span> <span>'{"commandToExecute": "./configure-nginx.sh"}'</span>    
    </span>
    ```
    
    This command uses the Custom Script Extension to run a Bash script on your VM. The script is stored on GitHub. While the command runs, you can choose to [examine the Bash script](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh) from a separate browser tab. To summarize, the script:
    
    1.  Runs `apt-get update` to download the latest package information from the internet. This step helps ensure that the next command can locate the latest version of the Nginx package.
    2.  Installs Nginx.
    3.  Sets the home page, _/var/www/html/index.html_, to print a welcome message that includes your VM's host name.

## Continue

That's all for this exercise. The sandbox will keep running, and you'll come back to this point in a few units to update the network configuration so you can get to the website.

___

## Next unit: Describe Azure virtual desktop

[Continue](https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/4-virtual-desktop/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
