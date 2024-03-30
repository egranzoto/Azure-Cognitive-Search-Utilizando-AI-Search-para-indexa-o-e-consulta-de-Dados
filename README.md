# Azure Cognitive Search Utilizando AI Search para indexa o e consulta de Dados

# Explore an Azure AI Search index (UI)

Let’s imagine you work for Fourth Coffee, a national coffee chain. You’re asked to help build a knowledge mining solution that makes it easy to search for insights about customer experiences. You decide to build an Azure AI Search index using data extracted from customer reviews.

In this lab you’ll:

- Create Azure resources
- Extract data from a data source
- Enrich data with AI skills
- Use Azure’s indexer in the Azure portal
- Query your search index
- Review results saved to a Knowledge Store

# Azure resources needed

The solution you’ll create for Fourth Coffee requires the following resources in your Azure subscription:

- An Azure AI Search resource, which will manage indexing and querying.
- An Azure AI services resource, which provides AI services for skills that your search solution can use to enrich the data in the data source with AI-generated insights.

>Note Your Azure AI Search and Azure AI services resources must be in the same location!

- A Storage account with blob containers, which will store raw documents and other collections of tables, objects, or files.

# Create an Azure AI Search resource

1.Sign into the Azure portal.

2.Click the + Create a resource button, search for Azure AI Search, and create a Azure AI Search resource with the following settings:

- Subscription: Your Azure subscription.
- Resource group: Select or create a resource group with a unique name.
- Service name: A unique name.
- Location: Choose any available region.
- Pricing tier: Basic

3.Select Review + create, and after you see the response Validation Success, select Create.

4.After deployment completes, select Go to resource. On the Azure AI Search overview page, you can add indexes, import data, and search created indexes.

# Create an Azure AI services resource

You’ll need to provision an Azure AI services resource that’s in the same location as your Azure AI Search resource. Your search solution will use this resource to enrich the data in the datastore with AI-generated insights.

1.Return to the home page of the Azure portal. Click the ＋Create a resource button and search for Azure AI services. Select create an Azure AI services plan. You will be taken to a page to create an Azure AI services resource. Configure it with the following settings:
- Subscription: Your Azure subscription.
- Resource group: The same resource group as your Azure AI Search resource.
- Region: The same location as your Azure AI Search resource.
- Name: A unique name.
- Pricing tier: Standard S0
- By checking this box I acknowledge that I have read and understood all the terms below: Selected

2.Select Review + create. After you see the response Validation Passed, select Create.

3.Wait for deployment to complete, then view the deployment details.

# Create a storage account

1.Return to the home page of the Azure portal, and then select the + Create a resource button.

2.Search for storage account, and create a Storage account resource with the following settings:
- Subscription: Your Azure subscription.
- Resource group: The same resource group as your Azure AI Search and Azure AI services resources.
- Storage account name: A unique name.
- Location: Choose any available location.
- Performance: Standard
- Redundancy: Locally redundant storage (LRS)

3.Click Review and then click Create. Wait for deployment to complete, and then go to the deployed resource.

4.In the Azure Storage account you created, in the left-hand menu pane, select Configuration (under Settings).

5.Change the setting for Allow Blob anonymous access to Enabled and then select Save.
