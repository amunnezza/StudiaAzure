---
created: 2024-02-15T13:08:11 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/6-reorganize-azure-resources
author: wwlpublish
---

# Reorganize Azure resources - Training | Microsoft Learn

> ## Excerpt
> Reorganize Azure resources

---
-   3 minutes

Sometimes you may need to move resources to either a new subscription or a new resource group in the same subscription.

![Diagram showing two subscriptions.](Reorganize%20Azure%20resources%20-%20Training%20%20Microsoft%20Learn/move-resources-1ce2912e.png)

When moving resources, both the source group and the target group are locked during the operation. Write and delete operations are blocked on the resource groups until the move completes. This lock means you can't add, update, or delete resources in the resource groups. Locks don't mean the resources aren't available. For example, if you move a virtual machine to a new resource group, an application can still access the virtual machine.

## Limitations

Before beginning this process be sure to read the [Move operation support for resources](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/move-support-resources) page. This page details what resources can be moved between resources group, subscriptions, and regions.

## Implementation

To move resources, select the resource group containing those resources, and then select the **Move** button. Select the resources to move and the destination resource group. Acknowledge that you need to update scripts.

![Screenshot of the Move a Resource page.](Reorganize%20Azure%20resources%20-%20Training%20%20Microsoft%20Learn/move-resource-groups-aae58bce.png)

Note

==Just because a service can be moved doesn’t mean there aren’t restrictions. For example, you can move a virtual network, but you must also move its dependent resources, like gateways.`==

___

## Next unit: Remove resources and resource groups

[Continue](https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/7-remove-resources-groups/)

