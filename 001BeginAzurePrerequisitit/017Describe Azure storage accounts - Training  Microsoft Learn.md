---
created: 2024-02-09T16:32:38 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/2-accounts
author: wwlpublish
---

# Describe Azure storage accounts - Training | Microsoft Learn

> ## Excerpt
> Describe Azure storage accounts

---
-   5 minutes

The following video introduces the different services that should be available with Azure Storage.
![[Video003AzureStorage.mp4]]

TRANSCRIPT
Azure Storage is Microsoft's cloud storage solution for modern data storage scenarios.
Core storage services offer a massively scalable object store for data objects, disk storage for Azure virtual machines, a file system service for the cloud, a messaging store for reliable messaging, and a NoSQL store.

Azure Blob Storage is an object storage solution that you can use to store massive amounts
of unstructured data, such as text or binary data.
Blob Storage is ideal for serving images or documents directly to a browser, storing data for archives or distributed access, streaming video and audio, and disaster recovery scenarios.

Azure File Storage offers fully managed file shares in the cloud, and shares are accessible using industry standard network protocols.
Mounting Azure file shares is just like connecting to shares on your local network.

Azure Disk Storage provides disks for virtual machines and applications to access and use as they need - similar to how they would access disks that were on premises.

Azure offers both solid state drives for higher performance workloads and conventional hard drives for your less critical business scenarios.

Azure Table Storage offers a NoSQL data store for key value pairs using large scale datasets.
You can use Azure Table Storage to store petabytes of semi-structured data, and keep your costs down.

Azure Queue Storage provides asynchronous message queuing for communication between
application components, whether they're running in the cloud, on the desktop, on premises, or on mobile devices.

There are three Azure storage tiers that you can use to balance your costs:
hot, cool, and archive.

The hot storage tier is optimized for storing data that is accessed frequently, such as images for your website.

The cold storage tier is optimized for data that is infrequently accessed, and stored for at least 30
days, such as customer invoices.
And the archive storage tier is appropriate for data that is rarely accessed, and stored for at least 180 days, such as long-term backups.

Regardless of your business scenario, Azure has a solution to help
you manage your storage needs.
fine transcript

A storage account provides a unique namespace for your Azure Storage data that's accessible from anywhere in the world over HTTP or HTTPS. Data in this account is secure, highly available, durable, and massively scalable.

When you create your storage account, you’ll start by picking the storage account type. The type of account determines the storage services and redundancy options and has an impact on the use cases. Below is a list of redundancy options that will be covered later in this module:

-   Locally redundant storage (LRS)
-   Geo-redundant storage (GRS)
-   Read-access geo-redundant storage (RA-GRS)
-   Zone-redundant storage (ZRS)
-   Geo-zone-redundant storage (GZRS)
-   Read-access geo-zone-redundant storage (RA-GZRS)

| **Type** | **Supported services** | **Redundancy Options** | **Usage** |
| --- | --- | --- | --- |
| Standard general-purpose v2 | Blob Storage (including Data Lake Storage), Queue Storage, Table Storage, and Azure Files | LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS | Standard storage account type for blobs, file shares, queues, and tables. Recommended for most scenarios using Azure Storage. If you want support for network file system (NFS) in Azure Files, use the premium file shares account type. |
| Premium block blobs | Blob Storage (including Data Lake Storage) | LRS, ZRS | Premium storage account type for block blobs and append blobs. Recommended for scenarios with high transaction rates or that use smaller objects or require consistently low storage latency. |
| Premium file shares | Azure Files | LRS, ZRS | Premium storage account type for file shares only. Recommended for enterprise or high-performance scale applications. Use this account type if you want a storage account that supports both Server Message Block (SMB) and NFS file shares. |
| Premium page blobs | Page blobs only | LRS | Premium storage account type for page blobs only. |

## Storage account endpoints

One of the benefits of using an Azure Storage Account is having a unique namespace in Azure for your data. In order to do this, every storage account in Azure must have a unique-in-Azure account name. The combination of the account name and the Azure Storage service endpoint forms the endpoints for your storage account.

When naming your storage account, keep these rules in mind:

-   Storage account names must be between 3 and 24 characters in length and may contain numbers and lowercase letters only.
-   Your storage account name must be unique within Azure. No two storage accounts can have the same name. This supports the ability to have a unique, accessible namespace in Azure.

The following table shows the endpoint format for Azure Storage services.

| **Storage service** | **Endpoint** |
| --- | --- |
| Blob Storage | https://<storage-account-name>.blob.core.windows.net |
| Data Lake Storage Gen2 | https://<storage-account-name>.dfs.core.windows.net |
| Azure Files | https://<storage-account-name>.file.core.windows.net |
| Queue Storage | https://<storage-account-name>.queue.core.windows.net |
| Table Storage | https://<storage-account-name>.table.core.windows.net |

___

## Next unit: Describe Azure storage redundancy

[Continue](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/3-redundancy/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
