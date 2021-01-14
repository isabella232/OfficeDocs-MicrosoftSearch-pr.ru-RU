---
title: Общие сведения о соединители
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
description: Обзор соединители Microsoft Graph для Поиска (Майкрософт)
ms.openlocfilehash: 677c91f121185faa6dc96f80c517917f429a3ab0
ms.sourcegitcommit: 469be70ad295a5837978d75babf5243115257f77
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/13/2021
ms.locfileid: "49847522"
---
# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="ff2ed-103">Обзор соединители Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="ff2ed-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="ff2ed-104">[Поиск (Майкрософт)](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) индексирует [все ваши данные Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их поиском пользователей.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-104">[Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="ff2ed-105">С помощью соединители Microsoft Graph ваша организация может индексировать сторонние данные, чтобы они появляются в результатах Поиска (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="ff2ed-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="ff2ed-106">Это расширяет типы источников контента, доступных для поиска в приложениях Для повышения производительности Microsoft 365 и в более широкой экосистеме Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-106">This expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="ff2ed-107">Сторонние данные могут быть локально или в общедоступных или закрытых облаках.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="ff2ed-108">Остальная часть этой статьи предназначена для помощи администраторам Microsoft 365 в поиске ресурсов, доступных для ответа на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="ff2ed-108">The rest of this article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="ff2ed-109">Какие источники данных можно подключать к Поиску (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="ff2ed-110">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="ff2ed-111">Каковы требования к лицензиям и условия использования соединители Graph?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-111">What are the license requirements and terms of use for Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [<span data-ttu-id="ff2ed-112">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-112">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="ff2ed-113">Как искать данные соединители из пользовательского приложения?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-113">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)

<!---Modify to another note that is more accurate--->
> [!IMPORTANT]
> <span data-ttu-id="ff2ed-114">Теперь соединители Microsoft Graph и API Поиска (Майкрософт) доступны в целом.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-114">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="ff2ed-115">Первый выпуск будет для клиентов, настроенных для целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-115">The first rollouts will be to customers configured for  targeted release.</span></span> <span data-ttu-id="ff2ed-116">Если вы хотите использовать соединители Graph в клиенте, пользователи и администраторы должны выбрать выпуск [Targeted.](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-116">If you want to use a Graph connector in your tenant, users and administrators must opt into [Targeted release](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true).</span></span>

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

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="ff2ed-117">Какие источники данных можно подключать к Поиску (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-117">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="ff2ed-118">Корпорация Майкрософт предоставляет десять соединитеев Graph, а наши партнеры по экосистеме создали более 100 дополнительных соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-118">Microsoft provides ten Graph connectors and our ecosystem partners have created over 100 additional Graph connectors.</span></span> <span data-ttu-id="ff2ed-119">Вы также можете создать собственный соединител Graph.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-119">You can also build your own Graph connector.</span></span> 

### <a name="graph-connectors-by-microsoft"></a><span data-ttu-id="ff2ed-120">Соединители Graph от Майкрософт</span><span class="sxs-lookup"><span data-stu-id="ff2ed-120">Graph connectors by Microsoft</span></span>

<span data-ttu-id="ff2ed-121">Вы можете подключаться к следующим источникам данных, используя соединители Graph, созданные корпорацией Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="ff2ed-121">You can connect to the following data sources using Graph connectors created by Microsoft:</span></span>

<!---Need to add a few links below when docs exist--->
* [<span data-ttu-id="ff2ed-122">Azure Data Lake Storage 2-го поколения</span><span class="sxs-lookup"><span data-stu-id="ff2ed-122">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="ff2ed-123">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="ff2ed-123">Azure DevOps</span></span>](azure-devops-connector.md)
* <span data-ttu-id="ff2ed-124">Azure SQL</span><span class="sxs-lookup"><span data-stu-id="ff2ed-124">Azure SQL</span></span>
* [<span data-ttu-id="ff2ed-125">Корпоративные веб-сайты</span><span class="sxs-lookup"><span data-stu-id="ff2ed-125">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="ff2ed-126">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="ff2ed-126">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="ff2ed-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ff2ed-127">Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="ff2ed-128">Файловый ресурс</span><span class="sxs-lookup"><span data-stu-id="ff2ed-128">File share</span></span>](fileshare-connector.md)
* <span data-ttu-id="ff2ed-129">Oracle (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-129">Oracle (preview)</span></span>
* [<span data-ttu-id="ff2ed-130">Salesforce (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-130">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="ff2ed-131">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="ff2ed-131">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="ff2ed-132">В [коллекции соединители Graph](connectors-gallery.md) содержится краткое описание каждого из этих соединитеителей Graph.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-132">The [Graph connectors gallery](connectors-gallery.md) contains a brief description of each of these Graph connectors.</span></span> <span data-ttu-id="ff2ed-133">Если вы готовы подключить один из этих источников данных к [](configure-connector.md) вашему арендатору, ознакомьтесь с обзором программы установки и другими статьями в разделе "Соединители установки" корпорации Майкрософт, которые относятся к вашему источнику данных.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-133">If you are ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="graph-connectors-by-our-partners"></a><span data-ttu-id="ff2ed-134">Соединители Graph от наших партнеров</span><span class="sxs-lookup"><span data-stu-id="ff2ed-134">Graph connectors by our partners</span></span>

<span data-ttu-id="ff2ed-135">В [коллекции соединитеев Microsoft Graph](connectors-gallery.md) содержится краткое описание каждого соединители Graph, созданных нашими партнерами, и ссылка на веб-сайт каждого партнера.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-135">The [Microsoft Graph connectors gallery](connectors-gallery.md) includes a brief descriptions of each of the Graph connectors created by our partners and a link to each partner's website.</span></span> <span data-ttu-id="ff2ed-136">Свяжитесь с каждым партнером напрямую, чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-136">Contact each partner directly to learn more.</span></span>

### <a name="build-your-own-graph-connector"></a><span data-ttu-id="ff2ed-137">Создание собственного соединитела Graph</span><span class="sxs-lookup"><span data-stu-id="ff2ed-137">Build your own Graph connector</span></span>

<span data-ttu-id="ff2ed-138">Если вы планируете создать собственный соединитатель Graph, дополнительные сведения см. в обзоре [API Поиска (Майкрософт) в Microsoft Graph.](https://docs.microsoft.com/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-138">If you plan to build your own Graph connector, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview) for more information.</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="ff2ed-139">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-139">How do I manage my connections?</span></span>

<span data-ttu-id="ff2ed-140">Вы можете управлять подключениями на вкладке ["Соединители"](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в Центре администрирования [Microsoft 365.](https://admin.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-140">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="ff2ed-141">Дополнительные [сведения см. в](manage-connector.md) под управлением подключений.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-141">See [Manage your connections](manage-connector.md) for more information.</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a><span data-ttu-id="ff2ed-142">Каковы требования к лицензиям и условия использования соединители Graph?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-142">What are the license requirements and terms of use for Graph connectors?</span></span>

<span data-ttu-id="ff2ed-143">Для просмотра данных соединителов в результатах поиска пользователям в организации необходима действующая лицензия Microsoft 365 или Office 365 и достаточная квота соединителов Graph.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-143">You need a valid Microsoft 365 or Office 365 license and sufficient Graph Connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="ff2ed-144">Дополнительные [см. в требованиях к лицензиям, ценах](licensing.md) [и условиях использования.](terms-of-use.md)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-144">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="ff2ed-145">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-145">How do I customize and configure search results?</span></span>

<span data-ttu-id="ff2ed-146">Существует несколько способов настройки и настройки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-146">There are a number of ways to customize and configure search results.</span></span> <span data-ttu-id="ff2ed-147">Подробнее см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="ff2ed-147">See the following articles to learn more:</span></span>

* [<span data-ttu-id="ff2ed-148">Управление вертикалями и типами результатов</span><span class="sxs-lookup"><span data-stu-id="ff2ed-148">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="ff2ed-149">Управление макетами результатов поиска</span><span class="sxs-lookup"><span data-stu-id="ff2ed-149">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="ff2ed-150">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="ff2ed-150">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="ff2ed-151">Управление пользовательскими фильтрами</span><span class="sxs-lookup"><span data-stu-id="ff2ed-151">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="ff2ed-152">Как искать данные соединители из пользовательского приложения?</span><span class="sxs-lookup"><span data-stu-id="ff2ed-152">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="ff2ed-153">После индексации пользовательских данных разработчики могут [запросить эти данные.](https://docs.microsoft.com/graph/search-concept-custom-types)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-153">After custom data is indexed, developers can [query this data](https://docs.microsoft.com/graph/search-concept-custom-types).</span></span> <span data-ttu-id="ff2ed-154">Вы можете просматривать данные в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-154">You can view your data in any application.</span></span> <span data-ttu-id="ff2ed-155">Дополнительные сведения см. в [обзоре API Поиска (Майкрософт) в Microsoft Graph.](https://docs.microsoft.com/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="ff2ed-155">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).</span></span>

## <a name="limitations"></a><span data-ttu-id="ff2ed-156">Ограничения</span><span class="sxs-lookup"><span data-stu-id="ff2ed-156">Limitations</span></span>

* <span data-ttu-id="ff2ed-157">При **публикации** соединители, созданного корпорацией Майкрософт, может потребоваться несколько минут для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-157">When you **publish** a Microsoft-built connector, it might take a few minutes for the connection to be created.</span></span> <span data-ttu-id="ff2ed-158">В течение этого времени подключение будет отложено.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-158">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="ff2ed-159">Центр [администрирования Microsoft 365](https://admin.microsoft.com) не поддерживает  редактирование схемы поиска после публикации подключения.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-159">The [Microsoft 365 admin center](https://admin.microsoft.com) doesn't support editing the **search schema** after a connection is published.</span></span> <span data-ttu-id="ff2ed-160">Чтобы изменить схему поиска, удалите подключение и создайте новое.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-160">To edit the search schema, delete your connection and then create a new one.</span></span>

* <span data-ttu-id="ff2ed-161">Пропускная способность при входеть в нее отлажается примерно при четырех пунктах в секунду.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-161">Ingestion throughput is throttled at about four items per second.</span></span>

* <span data-ttu-id="ff2ed-162">Обновления схемы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-162">There is no support for schema updates.</span></span> <span data-ttu-id="ff2ed-163">После создания настройки подключения обновить схему нельзя.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-163">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="ff2ed-164">Можно только удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-164">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="ff2ed-165">Существует ограничение подключений.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-165">There is a connections limit.</span></span> <span data-ttu-id="ff2ed-166">Каждый клиент может создать до 10 подключений.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-166">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="ff2ed-167">Поддержка редактирования подключения недоступна.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-167">Edit support for connection is not available.</span></span> <span data-ttu-id="ff2ed-168">После создания подключения изменить или изменить его нельзя.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-168">Once the connection has been created, you cannot edit or change it.</span></span> <span data-ttu-id="ff2ed-169">Если необходимо изменить какие-либо сведения, необходимо удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="ff2ed-169">If you need to change any details, you must delete and recreate the connection.</span></span>
