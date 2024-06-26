---
page_type: sample
description: "Contains several projects to help you get started with Azure AI Search and the .NET SDK"
languages:
- csharp
products:
- azure
- azure-cognitive-search
---

# Getting Started with Azure AI Search using .NET

This repository includes several projects that show you how to use the [**Azure.Search.Documents**](https://docs.microsoft.com/dotnet/api/overview/azure/search.documents-readme) client library in Azure SDK for .NET to create C# applications that use Azure AI Search.

An earlier version of the samples that were built using the [**Microsoft.Azure.Search**](https://docs.microsoft.com/dotnet/api/overview/azure/search/client10) client libraries can be found in the **v10** branch of this repo. To download those versions, switch the branch from **master** to **v10**, and then select **Code** to download or open those samples.

## DotNetHowTo

This sample is a simple .NET Core console application that shows you how to:

* Create and delete a search index
* Upload documents
* Search and filter documents within an index

To run this sample, open the solution in Visual Studio and modify **appsettings.json** to use valid values for your search service.

<!-- For detailed instructions, see [How to develop in C# using Azure.Search.Documents](https://docs.microsoft.com/azure/search/search-howto-dotnet-sdk-v11).  -->

## DotNetHowToEncryptionUsingCMK

This sample demonstrates how to create a synonym-map and an index that are encrypted with a customer-managed key in Azure Key Vault. This sample uses several services that must be set up in advance: Azure Key Vault, Azure Active Directory, and modifications to your existing search service.

The **appsettings.json** file provides placeholders for service information.

For detailed instructions, see [How to configure customer-managed keys for data encryption in Azure AI Search](https://docs.microsoft.com/azure/search/search-security-manage-encryption-keys).

## DotNetHowToIndexers

This sample is a simple .NET Core console application that shows how create and run a search indexer that retrieves data from an Azure SQL database.

Before you can run this sample, you will need an Azure SQL database that contains sample data used by the indexer. You will also need to modify settings in **appsettings.json**.

1. Create a new database in Azure SQL named hotels.
1. Run the `data\hotels.sql` script provided in this sample against your Azure SQL database.
1. Open the DotNetHowToIndexers.sln in Visual Studio.
1. Update the appsettings.json with your service name, api key, and connection string to your Azure SQL database.
1. Compile and Run the project using Visual Studio.

## Retired samples

The following samples have been removed from the master branch.

### DotNetETagsExplainer

This sample is [now archived](https://github.com/Azure-Samples/azure-search-sample-archive). It's a .console application that shows how to use ETags to update Azure AI Search resources safely in the presence of concurrency. The code in this sample simulates concurrent write operations so that you can see how that condition is handled.

### DotNetHowToSecurityTrimming (Archived)

This sample is [now archived](https://github.com/Azure-Samples/azure-search-sample-archive). It's replaced by [instructions for setting up access control](https://github.com/Azure-Samples/azure-search-openai-demo/blob/main/LoginAndAclSetup.md) on the [azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo/tree/main).

### DotNetHowToSynonyms (Archived)

This C# sample was used to demonstrate the benefits of adding a synonym map using "before-and-after" queries. The Azure SDK team provides a more recent sample. See [Azure.Search.Documents Samples - Service Operations](https://github.com/Azure/azure-sdk-for-net/blob/main/sdk/search/Azure.Search.Documents/samples/Sample02_Service.md#create-a-synonym-map) for replacement code.

### DotNetHowToAutocomplete

This sample was not migrated to use the Azure.Search.Documents client library. It has been replaced by a project in the [create-first-app](https://github.com/Azure-Samples/azure-search-dotnet-samples/tree/master/create-first-app) sample in the [azure-search-dotnet-samples](https://github.com/Azure-Samples/azure-search-dotnet-samples) repository. Alternatively, you can look at the v10 version of the sample.

### DotNetHowToMultipleDataSources

This sample was not migrated to use the Azure.Search.Documents client library. It has been replaced by the [multiple-data-sources](https://github.com/Azure-Samples/azure-search-dotnet-samples/tree/master/multiple-data-sources) sample in the [azure-search-dotnet-samples](https://github.com/Azure-Samples/azure-search-dotnet-samples) repository. Alternatively, you can look at the v10 version of the sample.

### DotNetSample

This sample was not migrated to use the Azure.Search.Documents client library. We recommend that you refer to **DotNetHowToIndexers** to view code that calls the Azure SQL Indexer. Alternatively, you can look at the v10 version of the sample.

---

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.