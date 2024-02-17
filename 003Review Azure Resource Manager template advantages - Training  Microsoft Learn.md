---
created: 2024-02-17T17:13:17 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/configure-resources-arm-templates/2-review-template-advantages
author: wwlpublish
---

# Review Azure Resource Manager template advantages > 
## Excerpt
Review Azure Resource Manager template advantages

---
-   3 minutes

An **Azure Resource Manager template** precisely defines all the Resource Manager resources in a deployment. You can deploy a Resource Manager template into a resource group as a single operation.

==Using Resource Manager templates will make== your deployments faster and more repeatable. For example, you no longer have to create a VM in the portal, wait for it to finish, and then create the next VM. Resource Manager template takes care of the entire deployment for you.

## Template benefits

-   **Templates improve consistency**. Resource Manager templates provide a common language for you and others to describe your deployments. Regardless of the tool or SDK that you use to deploy the template, the structure, format, and expressions inside the template remain the same.
-   **Templates help express complex deployments**. Templates enable you to deploy multiple resources in the correct order. For example, you wouldn't want to deploy a virtual machine prior to creating an operating system (OS) disk or network interface. Resource Manager maps out each resource and its dependent resources, and creates dependent resources first. Dependency mapping helps ensure that the deployment is carried out in the correct order.
-   **Templates reduce manual, error-prone tasks**. Manually creating and connecting resources can be time consuming, and it's easy to make mistakes. Resource Manager ensures that the deployment happens the same way every time.
-   **Templates are code**. Templates express your requirements through code. Think of a template as a type of Infrastructure as Code that can be shared, tested, and versioned similar to any other piece of software. Also, because templates are code, you can create a "paper trail" that you can follow. The template code documents the deployment. Most users maintain their templates under some kind of revision control, such as GIT. When you change the template, its revision history also documents how the template (and your deployment) has evolved over time.
-   **Templates promote reuse**. Your template can contain parameters that are filled in when the template runs. A parameter can define a username or password, a domain name, and so on. Template parameters enable you to create multiple versions of your infrastructure, such as staging and production, while still using the exact same template.
-   **Templates are linkable**. You can link Resource Manager templates together to make the templates themselves modular. You can write small templates that each define a piece of a solution, and then combine them to create a complete system.
-   **Templates simplify orchestration**. You only need to deploy the template to deploy all of your resources. Normally this would take multiple operations.

___

## Next unit: Explore the Azure Resource Manager template schema

[Continue](https://learn.microsoft.com/en-us/training/modules/configure-resources-arm-templates/3-explore-template-schema/)

