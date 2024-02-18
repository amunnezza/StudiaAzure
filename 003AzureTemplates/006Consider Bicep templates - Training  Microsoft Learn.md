---
created: 2024-02-18T15:15:21 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/configure-resources-arm-templates/5-consider-bicep-templates
author: wwlpublish
---

# Consider Bicep templates - Training | Microsoft Learn

> ## Excerpt
> Consider Bicep templates

---
-   3 minutes

[Azure Bicep](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview) is a domain-specific language (DSL) that uses declarative syntax to deploy Azure resources. It provides concise syntax, reliable type safety, and support for code reuse.

You can use Bicep instead of JSON to develop your Azure Resource Manager templates (ARM templates). The JSON syntax to create an ARM template can be verbose and require complicated expressions. Bicep syntax reduces that complexity and improves the development experience. Bicep is a transparent abstraction over ARM template JSON and doesn't lose any of the JSON template capabilities.

**How does Bicep work?**

When you deploy a resource or series of resources to Azure, the tooling that's built into Bicep converts your Bicep template into a JSON template. This process is known as transpilation. Transpilation is the process of converting source code written in one language into another language.

![Bicep templates are converted to JSON templates..](Consider%20Bicep%20templates%20-%20Training%20%20Microsoft%20Learn/bicep.png)

Bicep provides many improvements over JSON for template authoring, including:

-   **Simpler syntax**: Bicep provides a simpler syntax for writing templates. You can reference parameters and variables directly, without using complicated functions. String interpolation is used in place of concatenation to combine values for names and other items. You can reference the properties of a resource directly by using its symbolic name instead of complex reference statements. These syntax improvements help both with authoring and reading Bicep templates.
    
-   **Modules**: You can break down complex template deployments into smaller module files and reference them in a main template. These modules provide easier management and greater reusability.
    
-   **Automatic dependency management**: In most situations, Bicep automatically detects dependencies between your resources. This process removes some of the work involved in template authoring.
    
-   **Type validation and IntelliSense**: The Bicep extension for Visual Studio Code features rich validation and IntelliSense for all Azure resource type API definitions. This feature helps provide an easier authoring experience.
    

___

## Next unit: Review QuickStart templates

[Continue](https://learn.microsoft.com/en-us/training/modules/configure-resources-arm-templates/6-review-quickstart-templates/)

