---
created: 2024-02-18T15:35:57 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/configure-resources-arm-templates/8-knowledge-check
author: wwlpublish
---

# Knowledge check - Training | Microsoft Learn

> ## Excerpt
> Knowledge check

---
Choose the best response for each question. Then select Check your answers.

1. 

What is an Azure Resource Manager template?

 

A series of Azure CLI commands to deploy infrastructure to Azure.

==A JavaScript Object Notation (JSON) file that defines the infrastructure and configuration for the deployment.==

Correct. An Azure Resource Manager template is a JSON file that defines the infrastructure and configuration for the deployment.

A script used by the Azure Resource Manager to manage the Azure storage account.

2. 

Which of the following parameters is an element in the template schema?

 

Includes

Scripts

==Outputs==

Correct. Outputs are part of the template schema. Outputs are used to return values from the deployed resources.

3. 

What happens if the same template is run a second time?

 

Azure Resource Manager deploys the new resources as copies of the previously deployed resources.

==Azure Resource Manager doesn't change the deployed resources.==

Correct. If the resource already exists and no change is detected in the properties, no action is taken. If the resource already exists and a property has changed, the resource is updated. If the resource doesn't exist, it's created.

~~Azure Resource Manager deletes the previously deployed resources and redeploys them.~~

Incorrect. If the resource already exists and no change is detected in the properties, no action is taken. If the resource already exists and a property has changed, the resource is updated. If the resource doesn't exist, it's created.


A