---
created: 2024-02-09T23:04:32 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/5-exercise-create-storage-blob
author: wwlpublish
---

# Exercise - Create a storage blob - Training | Microsoft Learn

> ## Excerpt
> Exercise - Create a storage blob

---
-   10 minutes

## Create a storage account

In this task, you'll create a new storage account.

1.  Sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com/learn.docs.microsoft.com)
    
2.  Select **Create a resource**.
    
3.  Under Categories, select **Storage**.
    
4.  Under Storage account, select **Create**.
    
5.  On the **Basics** tab of the Create a storage account blade, fill in the following information. Leave the defaults for everything else.
   
   | **Setting** | **Value** |
   | --- | --- |
   | Subscription | Concierge Subscription |
   | Resource group | Select the resource group that starts with **learn** |
   | Storage account name | Create a unique storage account name |
   | Region | Leave default |
   | Performance | Standard |
   | Redundancy | Locally redundant storage (LRS) |

6.  On the **Advanced** tab of the Create a storage account blade, fill in the following information. Leave the defaults for everything else.

  
   |**Setting** | **Value** |
    | --- | --- |
    | Allow enabling anonymous access on individual containers | Checked |
![[010storage-account-anonymous-containers-5e5f584a.png]]

    
7.  Select **Review** to review your storage account settings and allow Azure to validate the configuration.
    
8.  Once validated, select **Create**. Wait for the notification that the account was successfully created.
    
9.  Select **Go to resource**.
    

## Work with blob storage

In this section, you'll create a Blob container and upload a picture.



1.  Under **Data storage**, select **Containers**.
    ![[011storage-account-menu-9472480e.png]]
    
    
2.  Select **\+ Container** and complete the information.
     
| **Setting** | **Value** |
    | --- | --- |
    | Name | Enter a name for the container |
    | Anonymous access level | Private (no anonymous access) |
    
3.  Select Create.
    
    Note
    
    <span style="background:gold" >Step 4 will need an image. If you want to upload an image you already have on your computer, continue to Step 4. Otherwise, open a new browser window and search Bing for an image of a flower. Save the image to your computer.
    </span>
    
4.  Back in the Azure portal, select the container you created, then select Upload.
    
5.  Browse for the image file you want to upload. Select it and then select upload.
    
    <span style= "background:gold">
    Note
    
    You can upload as many blobs as you like in this way. New blobs will be listed within the container.
    </span>
    
6.  Select the Blob (file) you just uploaded. You should be on the properties tab.
    
7.  Copy the URL from the URL field and paste it into a new tab.
    
    You should receive an error message similar to the following.
    
    ```
    <Error>
      <Code>ResourceNotFound</Code>
      &lt;Message&gt;The specified resource does not exist. RequestId:4a4bd3d9-101e-005a-1a3e-84bd42000000&lt;/Message&gt;
    &lt;/Error&gt;
    
    ```
    

## Change the access level of your blob

1.  Go back to the Azure portal.
    
2.  Select Change access level.
    
3.  Set the Anonymous access level to Blob (anonymous read access for blobs only).
![[012blob-access-level-213a74e6.png]]
 
4.  Select OK.
    
5.  Refresh the tab where you attempted to access the file earlier.
    

Congratulations - you've completed this exercise. You created a storage account, added a container to the storage account, and then uploaded blobs (files) to your container. Then you changed the access level so you could access your file from the internet.

## Clean up

The sandbox automatically cleans up your resources when you're finished with this module.

When you're working in your own subscription, it's a good idea at the end of a project to identify whether you still need the resources you created. Resources that you leave running can cost you money. You can delete resources individually or delete the resource group to delete the entire set of resources.

___

## Next unit: Identify Azure data migration options

[Continue](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/6-identify-azure-data-migration-options/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
