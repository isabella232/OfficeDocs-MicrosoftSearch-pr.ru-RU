---
title: Обзор соединители Microsoft Graph
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Обзор соединители Microsoft Graph для Поиска (Майкрософт)
ms.openlocfilehash: 13127d092fe4e624ed448037d83f16f83ddc560a
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084878"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="8c08b-103">Обзор соединители Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8c08b-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="8c08b-104">[Поиск (Майкрософт)](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) индексирует [все ваши данные Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их поиском пользователей.</span><span class="sxs-lookup"><span data-stu-id="8c08b-104">[Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="8c08b-105">С помощью соединители Microsoft Graph ваша организация может индексировать сторонние данные, чтобы они появляются в результатах Поиска (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="8c08b-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="8c08b-106">Эта функция расширяет типы источников контента, доступных для поиска в приложениях Для повышения производительности Microsoft 365 и в экосистеме Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8c08b-106">This feature expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="8c08b-107">Сторонние данные могут быть локально или в общедоступных или закрытых облаках.</span><span class="sxs-lookup"><span data-stu-id="8c08b-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="8c08b-108">Эта статья предназначена для помощи администраторам Microsoft 365 в поиске ресурсов, доступных для ответа на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="8c08b-108">This article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="8c08b-109">Какие источники данных можно подключать к Поиску (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="8c08b-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="8c08b-110">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="8c08b-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="8c08b-111">Каковы требования к лицензиям и условия использования соединители Graph?</span><span class="sxs-lookup"><span data-stu-id="8c08b-111">What are the license requirements and terms of use for Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [<span data-ttu-id="8c08b-112">Что такое функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="8c08b-112">What are the preview features?</span></span>](#what-are-the-preview-features)
* [<span data-ttu-id="8c08b-113">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="8c08b-113">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="8c08b-114">Как искать данные соединители из пользовательского приложения?</span><span class="sxs-lookup"><span data-stu-id="8c08b-114">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)

<!---Modify to another note that is more accurate after rollout completion--->
> [!IMPORTANT]
> <span data-ttu-id="8c08b-115">Теперь соединители Microsoft Graph и API Поиска (Майкрософт) доступны в целом.</span><span class="sxs-lookup"><span data-stu-id="8c08b-115">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="8c08b-116">Первый выпуск будет для клиентов, настроенных для целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="8c08b-116">The first rollouts will be to customers configured for  targeted release.</span></span> <span data-ttu-id="8c08b-117">Если вы хотите использовать соединители Graph в клиенте, пользователи и администраторы должны выбрать выпуск [Targeted.](https://docs.microsoft.com/microsoft-365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="8c08b-117">If you want to use a Graph connector in your tenant, users and administrators must opt into [Targeted release](https://docs.microsoft.com/microsoft-365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true).</span></span>

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below***
To create a **connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="8c08b-118">Какие источники данных можно подключать к Поиску (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="8c08b-118">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="8c08b-119">Корпорация Майкрософт предоставляет 9 соединители Graph, и наши партнеры по экосистеме создали более 100 дополнительных соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="8c08b-119">Microsoft provides 9 Graph connectors and our ecosystem partners have created over 100 more Graph connectors.</span></span> <span data-ttu-id="8c08b-120">Вы также можете создать собственный соединител Graph.</span><span class="sxs-lookup"><span data-stu-id="8c08b-120">You can also build your own Graph connector.</span></span>

### <a name="graph-connectors-by-microsoft"></a><span data-ttu-id="8c08b-121">Соединители Graph от Майкрософт</span><span class="sxs-lookup"><span data-stu-id="8c08b-121">Graph connectors by Microsoft</span></span>

<span data-ttu-id="8c08b-122">Вы можете подключаться к следующим источникам данных, используя соединители Graph, созданные корпорацией Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="8c08b-122">You can connect to the following data sources using Graph connectors created by Microsoft:</span></span>

<!---Add links below when new docs are created--->
* [<span data-ttu-id="8c08b-123">Azure Data Lake Storage 2-го поколения</span><span class="sxs-lookup"><span data-stu-id="8c08b-123">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="8c08b-124">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="8c08b-124">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="8c08b-125">Azure SQL и Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="8c08b-125">Azure SQL and Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="8c08b-126">Корпоративные веб-сайты</span><span class="sxs-lookup"><span data-stu-id="8c08b-126">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="8c08b-127">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="8c08b-127">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="8c08b-128">Файловый ресурс</span><span class="sxs-lookup"><span data-stu-id="8c08b-128">File share</span></span>](fileshare-connector.md)
* [<span data-ttu-id="8c08b-129">Oracle SQL (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="8c08b-129">Oracle SQL (preview)</span></span>](OracleSQL-connector.md)
* [<span data-ttu-id="8c08b-130">Salesforce (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="8c08b-130">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="8c08b-131">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="8c08b-131">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="8c08b-132">В [коллекции соединители Graph](connectors-gallery.md) содержится краткое описание каждого из этих соединитеителей Graph.</span><span class="sxs-lookup"><span data-stu-id="8c08b-132">The [Graph connectors gallery](connectors-gallery.md) contains a brief description of each of these Graph connectors.</span></span> <span data-ttu-id="8c08b-133">Если вы готовы подключить один из этих источников данных к вашему арендатору, ознакомьтесь с обзором программы установки и другими статьями в разделе "Соединители установки" корпорации Майкрософт, которые относятся к вашему источнику данных. [](configure-connector.md)</span><span class="sxs-lookup"><span data-stu-id="8c08b-133">If you're ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="graph-connectors-by-our-partners"></a><span data-ttu-id="8c08b-134">Соединители Graph от наших партнеров</span><span class="sxs-lookup"><span data-stu-id="8c08b-134">Graph connectors by our partners</span></span>

<span data-ttu-id="8c08b-135">В [коллекции соединитеев Microsoft Graph](connectors-gallery.md) содержится краткое описание каждого соединители Graph, созданных нашими партнерами, и ссылка на веб-сайт каждого партнера.</span><span class="sxs-lookup"><span data-stu-id="8c08b-135">The [Microsoft Graph connectors gallery](connectors-gallery.md) includes a brief description of each of the Graph connectors created by our partners, and a link to each partner's website.</span></span> <span data-ttu-id="8c08b-136">Чтобы узнать больше, свяжитесь с каждым партнером напрямую.</span><span class="sxs-lookup"><span data-stu-id="8c08b-136">To learn more, contact each partner directly.</span></span>

### <a name="build-your-own-graph-connector"></a><span data-ttu-id="8c08b-137">Создание собственного соединитела Graph</span><span class="sxs-lookup"><span data-stu-id="8c08b-137">Build your own Graph connector</span></span>

<span data-ttu-id="8c08b-138">При желании вы можете создать собственный соединититель Graph.</span><span class="sxs-lookup"><span data-stu-id="8c08b-138">You can build your own Graph connector if you prefer.</span></span> <span data-ttu-id="8c08b-139">Дополнительные сведения о создании соединителов Graph см. в обзоре [API Поиска (Майкрософт) в Microsoft Graph.](https://docs.microsoft.com/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="8c08b-139">For more information on building Graph connectors, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="8c08b-140">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="8c08b-140">How do I manage my connections?</span></span>

<span data-ttu-id="8c08b-141">Вы можете управлять подключениями на вкладке ["Соединители"](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в Центре администрирования [Microsoft 365.](https://admin.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="8c08b-141">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="8c08b-142">Дополнительные сведения об управлении подключениями см. в под [управлении подключениями.](manage-connector.md)</span><span class="sxs-lookup"><span data-stu-id="8c08b-142">For more information about managing connections, see: [Manage your connections](manage-connector.md).</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a><span data-ttu-id="8c08b-143">Каковы требования к лицензиям и условия использования соединители Graph?</span><span class="sxs-lookup"><span data-stu-id="8c08b-143">What are the license requirements and terms of use for Graph connectors?</span></span>

<span data-ttu-id="8c08b-144">Для просмотра данных соединителов в результатах поиска пользователям в организации необходима действующая лицензия Microsoft 365 или Office 365 и достаточная квота соединителов Graph.</span><span class="sxs-lookup"><span data-stu-id="8c08b-144">You need a valid Microsoft 365 or Office 365 license and sufficient Graph Connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="8c08b-145">Дополнительные узнать [см. в требованиях к лицензиям, ценах](licensing.md) [и условиях использования.](terms-of-use.md)</span><span class="sxs-lookup"><span data-stu-id="8c08b-145">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="what-are-the-preview-features"></a><span data-ttu-id="8c08b-146">Что такое функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="8c08b-146">What are the preview features?</span></span>

<span data-ttu-id="8c08b-147">Хотя соединители Microsoft Graph и API Поиска (Майкрософт) теперь доступны в целом, существует несколько функций, доступных в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="8c08b-147">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that are in preview.</span></span>

<span data-ttu-id="8c08b-148">Набор соединители и функции в предварительной версии включают:</span><span class="sxs-lookup"><span data-stu-id="8c08b-148">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="8c08b-149">Соединителю Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="8c08b-149">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="8c08b-150">Соединители Salesforce</span><span class="sxs-lookup"><span data-stu-id="8c08b-150">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="8c08b-151">[Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска, использующем исходные ALS</span><span class="sxs-lookup"><span data-stu-id="8c08b-151">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="8c08b-152">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="8c08b-152">Manage result cluster</span></span>](result-cluster.md)

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="8c08b-153">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="8c08b-153">How do I customize and configure search results?</span></span>

<span data-ttu-id="8c08b-154">Существует множество способов настройки и настройки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="8c08b-154">There are many ways to customize and configure search results.</span></span> <span data-ttu-id="8c08b-155">Подробнее см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="8c08b-155">See the following articles to learn more:</span></span>

* [<span data-ttu-id="8c08b-156">Управление вертикалями и типами результатов</span><span class="sxs-lookup"><span data-stu-id="8c08b-156">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="8c08b-157">Управление макетами результатов поиска</span><span class="sxs-lookup"><span data-stu-id="8c08b-157">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="8c08b-158">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="8c08b-158">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="8c08b-159">Управление пользовательскими фильтрами</span><span class="sxs-lookup"><span data-stu-id="8c08b-159">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="8c08b-160">Как искать данные соединители из пользовательского приложения?</span><span class="sxs-lookup"><span data-stu-id="8c08b-160">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="8c08b-161">После индексации пользовательских данных разработчики могут [запросить эти данные.](https://docs.microsoft.com/graph/search-concept-custom-types)</span><span class="sxs-lookup"><span data-stu-id="8c08b-161">After custom data is indexed, developers can [query this data](https://docs.microsoft.com/graph/search-concept-custom-types).</span></span> <span data-ttu-id="8c08b-162">Вы можете просматривать данные в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="8c08b-162">You can view your data in any application.</span></span> <span data-ttu-id="8c08b-163">Дополнительные сведения см. в [обзоре API Поиска (Майкрософт) в Microsoft Graph.](https://docs.microsoft.com/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="8c08b-163">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).</span></span>

## <a name="next-steps"></a><span data-ttu-id="8c08b-164">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="8c08b-164">Next steps</span></span>

<span data-ttu-id="8c08b-165">Убедитесь, что вы настроили результаты поиска согласно рекомендациям в этой статье Как настроить и настроить [результаты поиска?](#how-do-i-customize-and-configure-search-results).</span><span class="sxs-lookup"><span data-stu-id="8c08b-165">Make sure you customize the search results as recommended in this article [How do I customize and configure search results?](#how-do-i-customize-and-configure-search-results).</span></span> <span data-ttu-id="8c08b-166">Дополнительные узнать о настройке результатов поиска см. на странице "Настройка [результатов поиска".](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page)</span><span class="sxs-lookup"><span data-stu-id="8c08b-166">To learn more about customizing search results, see [Customize the search results page](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page).</span></span>

## <a name="limitations"></a><span data-ttu-id="8c08b-167">Ограничения</span><span class="sxs-lookup"><span data-stu-id="8c08b-167">Limitations</span></span>

* <span data-ttu-id="8c08b-168">При **публикации** соединители, созданного корпорацией Майкрософт, может потребоваться несколько минут для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="8c08b-168">When you **publish** a Microsoft-built connector, it might take a few minutes for the connection to be created.</span></span> <span data-ttu-id="8c08b-169">В течение этого времени подключение будет отложено.</span><span class="sxs-lookup"><span data-stu-id="8c08b-169">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="8c08b-170">Центр [администрирования Microsoft 365](https://admin.microsoft.com) не поддерживает  редактирование схемы поиска после публикации подключения.</span><span class="sxs-lookup"><span data-stu-id="8c08b-170">The [Microsoft 365 admin center](https://admin.microsoft.com) doesn't support editing the **search schema** after a connection is published.</span></span> <span data-ttu-id="8c08b-171">Чтобы изменить схему поиска, удалите подключение и создайте новое.</span><span class="sxs-lookup"><span data-stu-id="8c08b-171">To edit the search schema, delete your connection and then create a new one.</span></span>

* <span data-ttu-id="8c08b-172">Пропускная способность при входеть в нее отлажается примерно при четырех пунктах в секунду.</span><span class="sxs-lookup"><span data-stu-id="8c08b-172">Ingestion throughput is throttled at about four items per second.</span></span>

* <span data-ttu-id="8c08b-173">Обновления схемы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8c08b-173">There is no support for schema updates.</span></span> <span data-ttu-id="8c08b-174">После создания настройки подключения обновить схему нельзя.</span><span class="sxs-lookup"><span data-stu-id="8c08b-174">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="8c08b-175">Можно только удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="8c08b-175">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="8c08b-176">Существует ограничение подключений.</span><span class="sxs-lookup"><span data-stu-id="8c08b-176">There is a connections limit.</span></span> <span data-ttu-id="8c08b-177">Каждый клиент может создать до 10 подключений.</span><span class="sxs-lookup"><span data-stu-id="8c08b-177">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="8c08b-178">Поддержка редактирования подключения недоступна.</span><span class="sxs-lookup"><span data-stu-id="8c08b-178">Edit support for connection is not available.</span></span> <span data-ttu-id="8c08b-179">После создания подключения изменить или изменить его нельзя.</span><span class="sxs-lookup"><span data-stu-id="8c08b-179">Once the connection has been created, you cannot edit or change it.</span></span> <span data-ttu-id="8c08b-180">Если необходимо изменить какие-либо сведения, необходимо удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="8c08b-180">If you need to change any details, you must delete and recreate the connection.</span></span>
