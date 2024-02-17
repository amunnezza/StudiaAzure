---
created: 2024-02-17T09:59:51 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/7-remove-resources-groups
author: wwlpublish
---

# Remove resources and resource groups - Training | Microsoft Learn

> ## Excerpt
> Remove resources and resource groups

---
-   3 minutes

Use caution when deleting a resource group. Deleting a resource group deletes all the resources contained within it. That resource group might contain resources that resources in other resource groups depend on.

![Screenshot showing the Delete resource group button (highlighted) in the portal.](Remove%20resources%20and%20resource%20groups%20-%20Training%20%20Microsoft%20Learn/delete-resource-groups-53e65483.png)

## Using PowerShell to delete resource groups

To remove a resource group use, **Remove-AzResourceGroup**. In this example, we are removing the ContosoRG01 resource group from the subscription. The cmdlet prompts you for confirmation and returns no output.

```
Remove-AzResourceGroup -Name "ContosoRG01"

```

## Removing resources

You can also delete individual resources within a resource group. For example, here we are deleting a virtual network. Instead, of deleting you can **move** the resource to another resource group.

![Screenshot from the portal of the route table page, with the Delete button highlighted to show you can delete an individual resource within a resource group.](Remove%20resources%20and%20resource%20groups%20-%20Training%20%20Microsoft%20Learn/delete-resources-7ac5596a.png)

___

## Next unit: Determine resource limits

[Continue](https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/8-determine-resource-limits/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
