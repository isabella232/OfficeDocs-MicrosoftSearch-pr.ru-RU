---
title: Обзор соединителей
ms.author: monaray
author: monaray97
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Общие сведения о Microsoft Graph Connectors for Microsoft Search
ms.openlocfilehash: 7388653927ca6a7af0ba64c3c592f2689780c181
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367526"
---
# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="2acf4-103">Обзор соединителей Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="2acf4-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="2acf4-104">[Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) индексирует все данные [Microsoft 365](https://www.microsoft.com/microsoft-365) , чтобы обеспечить возможность поиска для пользователей.</span><span class="sxs-lookup"><span data-stu-id="2acf4-104">[Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="2acf4-105">С помощью соединителей Microsoft Graph организация может индексировать сторонние данные, чтобы они отображались в результатах поиска Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2acf4-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="2acf4-106">Это расширяет типы источников контента, которые доступны для поиска в приложениях Microsoft 365 для продуктивной работы, а также в обширной экосистеме корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2acf4-106">This expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="2acf4-107">Сторонние данные могут размещаться в локальной среде или в общедоступных или частных облаках.</span><span class="sxs-lookup"><span data-stu-id="2acf4-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="2acf4-108">Оставшаяся часть этой статьи предназначена для того, чтобы помочь администраторам Microsoft 365 найти ресурсы, которые аваиабле, чтобы ответить на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="2acf4-108">The rest of this article is intended to help Microsoft 365 administrators locate the resources that are avaiable to answer the following questions:</span></span>

* [<span data-ttu-id="2acf4-109">Какие источники данных могут быть подключены к поиску Майкрософт?</span><span class="sxs-lookup"><span data-stu-id="2acf4-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="2acf4-110">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="2acf4-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="2acf4-111">Каковы требования к лицензии и условия использования для соединителей Graph?</span><span class="sxs-lookup"><span data-stu-id="2acf4-111">What are the license requirements and terms of use for Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [<span data-ttu-id="2acf4-112">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="2acf4-112">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="2acf4-113">Поиск данных о соединителе из настраиваемого приложения</span><span class="sxs-lookup"><span data-stu-id="2acf4-113">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)

<!---Modify to another note that is more accurate--->
> [!IMPORTANT]
> <span data-ttu-id="2acf4-114">Microsoft Graph Connectors и API службы поиска, как правило, доступны в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="2acf4-114">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="2acf4-115">Первые развертывания будут выполняться для клиентов, настроенных для целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="2acf4-115">The first rollouts will be to customers configured for  targeted release.</span></span> <span data-ttu-id="2acf4-116">Если вы хотите использовать графический соединитель в клиенте, пользователи и администраторы должны принять участие в [целевой версии](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="2acf4-116">If you want to use a Graph connector in your tenant, users and administrators must opt into [Targeted release](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span></span>

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below**_
To create a _*connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="2acf4-117">Какие источники данных могут быть подключены к поиску Майкрософт?</span><span class="sxs-lookup"><span data-stu-id="2acf4-117">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="2acf4-118">Корпорация Майкрософт предоставляет десять графических соединителей, а наши партнеры по экосистеме создали более 100 дополнительных графических соединителей.</span><span class="sxs-lookup"><span data-stu-id="2acf4-118">Microsoft provides ten Graph connectors and our ecosystem partners have created over 100 additional Graph connectors.</span></span> <span data-ttu-id="2acf4-119">Вы также можете создать собственный соединительный соединитель.</span><span class="sxs-lookup"><span data-stu-id="2acf4-119">You can also build your own Graph connector.</span></span> 

### <a name="graph-connectors-by-microsoft"></a><span data-ttu-id="2acf4-120">Графические соединители корпорации Майкрософт</span><span class="sxs-lookup"><span data-stu-id="2acf4-120">Graph connectors by Microsoft</span></span>

<span data-ttu-id="2acf4-121">С помощью соединителей Graph, созданных корпорацией Майкрософт, можно подключаться к следующим источникам данных:</span><span class="sxs-lookup"><span data-stu-id="2acf4-121">You can connect to the following data sources using Graph connectors created by Microsoft:</span></span>

<!---Need to add a few links below when docs exist--->
* [<span data-ttu-id="2acf4-122">Azure Data Lake Storage 2-го поколения</span><span class="sxs-lookup"><span data-stu-id="2acf4-122">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="2acf4-123">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="2acf4-123">Azure DevOps</span></span>](azure-devops-connector.md)
* <span data-ttu-id="2acf4-124">Azure SQL</span><span class="sxs-lookup"><span data-stu-id="2acf4-124">Azure SQL</span></span>
* [<span data-ttu-id="2acf4-125">Корпоративные веб-сайты</span><span class="sxs-lookup"><span data-stu-id="2acf4-125">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="2acf4-126">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="2acf4-126">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="2acf4-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="2acf4-127">Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="2acf4-128">Файловый ресурс</span><span class="sxs-lookup"><span data-stu-id="2acf4-128">File share</span></span>](fileshare-connector.md)
* <span data-ttu-id="2acf4-129">Oracle (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="2acf4-129">Oracle (preview)</span></span>
* [<span data-ttu-id="2acf4-130">SalesForce (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="2acf4-130">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="2acf4-131">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="2acf4-131">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="2acf4-132">В [галерее Graph Connectors](connectors-gallery.md) содержится краткое описание каждого из этих соединителей Graph.</span><span class="sxs-lookup"><span data-stu-id="2acf4-132">The [Graph connectors gallery](connectors-gallery.md) contains a brief description of each of these Graph connectors.</span></span> <span data-ttu-id="2acf4-133">Если вы готовы подключить один из этих источников данных к клиенту, ознакомьтесь с [обзором программы установки](configure-connector.md) и другими статьями раздела Настройка соединителей Майкрософт, которые применимы к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="2acf4-133">If you are ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="graph-connectors-by-our-partners"></a><span data-ttu-id="2acf4-134">Graph Connectors by наших партнеров</span><span class="sxs-lookup"><span data-stu-id="2acf4-134">Graph connectors by our partners</span></span>

<span data-ttu-id="2acf4-135">В [коллекции соединителей Microsoft Graph](connectors-gallery.md) содержатся краткие описания всех соединителей графов, созданных нашими партнерами, а также ссылки на веб-сайт каждого партнера.</span><span class="sxs-lookup"><span data-stu-id="2acf4-135">The [Microsoft Graph connectors gallery](connectors-gallery.md) includes a brief descriptions of each of the Graph connectors created by our partners and a link to each partner's website.</span></span> <span data-ttu-id="2acf4-136">Свяжитесь с каждым партнером напрямую, чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="2acf4-136">Contact each partner directly to learn more.</span></span>

### <a name="build-your-own-graph-connector"></a><span data-ttu-id="2acf4-137">Создание собственного соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="2acf4-137">Build your own Graph connector</span></span>

<span data-ttu-id="2acf4-138">Если вы планируете создать собственный соединительный соединитель, ознакомьтесь со статьей [Обзор API Microsoft Search API в Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="2acf4-138">If you plan to build your own Graph connector, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview) for more information.</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="2acf4-139">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="2acf4-139">How do I manage my connections?</span></span>

<span data-ttu-id="2acf4-140">Вы можете управлять подключениями на [вкладке соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) [центра администрирования Microsoft 365](https://admin.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2acf4-140">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="2acf4-141">Дополнительные сведения можно найти [в разделе Manage Your Connections](manage-connector.md) .</span><span class="sxs-lookup"><span data-stu-id="2acf4-141">See [Manage your connections](manage-connector.md) for more information.</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a><span data-ttu-id="2acf4-142">Каковы требования к лицензии и условия использования для соединителей Graph?</span><span class="sxs-lookup"><span data-stu-id="2acf4-142">What are the license requirements and terms of use for Graph connectors?</span></span>

<span data-ttu-id="2acf4-143">Вам необходима действительная лицензия Microsoft 365 или Office 365 и достаточная квота Graph Connectors для пользователей в вашей организации, чтобы просматривать данные из соединителей в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="2acf4-143">You need a valid Microsoft 365 or Office 365 license and sufficient Graph Connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="2acf4-144">Чтобы узнать больше, ознакомьтесь со статьей [требования к лицензии и цены](licensing.md) и [условия использования](terms-of-use.md).</span><span class="sxs-lookup"><span data-stu-id="2acf4-144">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="2acf4-145">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="2acf4-145">How do I customize and configure search results?</span></span>

<span data-ttu-id="2acf4-146">Существует несколько способов настройки и настройки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="2acf4-146">There are a number of ways to customize and configure search results.</span></span> <span data-ttu-id="2acf4-147">Чтобы узнать больше, ознакомьтесь со следующими статьями:</span><span class="sxs-lookup"><span data-stu-id="2acf4-147">See the following articles to learn more:</span></span>

* [<span data-ttu-id="2acf4-148">Управление вертикалями и типами результатов</span><span class="sxs-lookup"><span data-stu-id="2acf4-148">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="2acf4-149">Управление макетами результатов поиска</span><span class="sxs-lookup"><span data-stu-id="2acf4-149">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="2acf4-150">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="2acf4-150">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="2acf4-151">Управление настраиваемыми фильтрами</span><span class="sxs-lookup"><span data-stu-id="2acf4-151">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="2acf4-152">Поиск данных о соединителе из настраиваемого приложения</span><span class="sxs-lookup"><span data-stu-id="2acf4-152">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="2acf4-153">После индексирования пользовательских данных разработчики могут [запрашивать эти данные](https://docs.microsoft.com/graph/search-concept-custom-types).</span><span class="sxs-lookup"><span data-stu-id="2acf4-153">After custom data is indexed, developers can [query this data](https://docs.microsoft.com/graph/search-concept-custom-types).</span></span> <span data-ttu-id="2acf4-154">Вы можете просматривать данные в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="2acf4-154">You can view your data in any application.</span></span> <span data-ttu-id="2acf4-155">Дополнительные сведения можно найти в [обзоре API службы поиска Microsoft Graph в Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).</span><span class="sxs-lookup"><span data-stu-id="2acf4-155">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).</span></span>
