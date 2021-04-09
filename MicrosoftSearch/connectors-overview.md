---
title: Обзор соединители Microsoft Graph
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Обзор соединители Microsoft Graph для microsoft Search
ms.openlocfilehash: ccf1e746c2a8bf97429bf5b13c8340db015e3eb1
ms.sourcegitcommit: a07c957dfa1d31542f0362379251bc9679dfae41
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2021
ms.locfileid: "51639865"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="6d510-103">Обзор соединители Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6d510-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="6d510-104">[Microsoft Search](./overview-microsoft-search.md) индексирует все данные [Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их более понятными для пользователей.</span><span class="sxs-lookup"><span data-stu-id="6d510-104">[Microsoft Search](./overview-microsoft-search.md) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="6d510-105">С помощью соединители Microsoft Graph ваша организация может индексировать сторонние данные, чтобы они фигурали в результатах поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6d510-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="6d510-106">Эта функция расширяет типы источников контента, доступных для поиска в приложениях производительности Microsoft 365, и более широкую экосистему Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6d510-106">This feature expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="6d510-107">Сторонние данные могут быть организованы на локальной основе или в общедоступных или частных облаках.</span><span class="sxs-lookup"><span data-stu-id="6d510-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="6d510-108">Эта статья предназначена для того, чтобы помочь администраторам Microsoft 365 найти ресурсы, доступные для ответа на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="6d510-108">This article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="6d510-109">Какие источники данных можно подключать к Microsoft Search?</span><span class="sxs-lookup"><span data-stu-id="6d510-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="6d510-110">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="6d510-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="6d510-111">Каковы требования к лицензиям и условия использования для соединители Graph?</span><span class="sxs-lookup"><span data-stu-id="6d510-111">What are the license requirements and terms of use for Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [<span data-ttu-id="6d510-112">Какие функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="6d510-112">What are the preview features?</span></span>](#what-are-the-preview-features)
* [<span data-ttu-id="6d510-113">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="6d510-113">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="6d510-114">Как искать данные соединитетеля в настраиваемом приложении?</span><span class="sxs-lookup"><span data-stu-id="6d510-114">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)
* [<span data-ttu-id="6d510-115">Как настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="6d510-115">How do I customize search results?</span></span>](#how-do-i-customize-search-results)
* [<span data-ttu-id="6d510-116">Каковы ограничения соединитетеля</span><span class="sxs-lookup"><span data-stu-id="6d510-116">What are the connector limitations</span></span>](#what-are-the-connector-limitations)

<!---Modify to another note that is more accurate after rollout completion--->
> [!IMPORTANT]
> <span data-ttu-id="6d510-117">Теперь в общем доступе доступны соединители Microsoft Graph и API поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6d510-117">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="6d510-118">Первыми выкатами будут клиенты, настроенные для целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="6d510-118">The first rollouts will be to customers configured for  targeted release.</span></span> <span data-ttu-id="6d510-119">Если вы хотите использовать соединители Graph в клиенте, пользователи и администраторы должны выбрать [целевой выпуск.](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="6d510-119">If you want to use a Graph connector in your tenant, users and administrators must opt into [Targeted release](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide).</span></span>

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](./overview-microsoft-search.md) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below***
To create a **connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="6d510-120">Какие источники данных можно подключать к Microsoft Search?</span><span class="sxs-lookup"><span data-stu-id="6d510-120">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="6d510-121">Корпорация Майкрософт предоставляет 9 соединители Graph, а наши партнеры по экосистеме создали более 100 соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="6d510-121">Microsoft provides 9 Graph connectors and our ecosystem partners have created over 100 more Graph connectors.</span></span> <span data-ttu-id="6d510-122">Вы также можете создать собственный соединитатель Graph.</span><span class="sxs-lookup"><span data-stu-id="6d510-122">You can also build your own Graph connector.</span></span>

### <a name="graph-connectors-by-microsoft"></a><span data-ttu-id="6d510-123">Соединители Graph от Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6d510-123">Graph connectors by Microsoft</span></span>

<span data-ttu-id="6d510-124">Вы можете подключиться к следующим источникам данных с помощью соединители Graph, созданные Корпорацией Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="6d510-124">You can connect to the following data sources using Graph connectors created by Microsoft:</span></span>

<!---Add links below when new docs are created--->
* [<span data-ttu-id="6d510-125">Azure Data Lake Storage 2-го поколения</span><span class="sxs-lookup"><span data-stu-id="6d510-125">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="6d510-126">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="6d510-126">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="6d510-127">Azure SQL и Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="6d510-127">Azure SQL and Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="6d510-128">Корпоративные веб-сайты</span><span class="sxs-lookup"><span data-stu-id="6d510-128">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="6d510-129">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="6d510-129">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="6d510-130">Файловый ресурс</span><span class="sxs-lookup"><span data-stu-id="6d510-130">File share</span></span>](fileshare-connector.md)
* [<span data-ttu-id="6d510-131">Oracle SQL (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="6d510-131">Oracle SQL (preview)</span></span>](OracleSQL-connector.md)
* [<span data-ttu-id="6d510-132">Salesforce (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="6d510-132">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="6d510-133">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="6d510-133">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="6d510-134">Галерея [соединители Graph](connectors-gallery.md) содержит краткое описание каждого из этих соединителеров Graph.</span><span class="sxs-lookup"><span data-stu-id="6d510-134">The [Graph connectors gallery](connectors-gallery.md) contains a brief description of each of these Graph connectors.</span></span> <span data-ttu-id="6d510-135">Если вы готовы подключить один из этих источников данных к вашему клиенту, обязательно ознакомьтесь с обзором установки и другими статьями в разделе Установки в разделе Microsoft, которые применяются к источнику данных. [](configure-connector.md)</span><span class="sxs-lookup"><span data-stu-id="6d510-135">If you're ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="graph-connectors-by-our-partners"></a><span data-ttu-id="6d510-136">Соединители графов нашими партнерами</span><span class="sxs-lookup"><span data-stu-id="6d510-136">Graph connectors by our partners</span></span>

<span data-ttu-id="6d510-137">В [галерее](connectors-gallery.md) соединители Microsoft Graph содержится краткое описание каждого из соединители Graph, созданных нашими партнерами, и ссылка на веб-сайт каждого партнера.</span><span class="sxs-lookup"><span data-stu-id="6d510-137">The [Microsoft Graph connectors gallery](connectors-gallery.md) includes a brief description of each of the Graph connectors created by our partners, and a link to each partner's website.</span></span> <span data-ttu-id="6d510-138">Чтобы узнать больше, свяжитесь с каждым партнером напрямую.</span><span class="sxs-lookup"><span data-stu-id="6d510-138">To learn more, contact each partner directly.</span></span>

### <a name="build-your-own-graph-connector"></a><span data-ttu-id="6d510-139">Создание собственного соединитетеля Graph</span><span class="sxs-lookup"><span data-stu-id="6d510-139">Build your own Graph connector</span></span>

<span data-ttu-id="6d510-140">При желании можно создать собственный соединититель Graph.</span><span class="sxs-lookup"><span data-stu-id="6d510-140">You can build your own Graph connector if you prefer.</span></span> <span data-ttu-id="6d510-141">Дополнительные сведения о создании соединителов Graph см. в обзоре [API поиска Майкрософт в Microsoft Graph.](/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="6d510-141">For more information on building Graph connectors, see the [Overview of the Microsoft Search API in Microsoft Graph](/graph/search-concept-overview).</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="6d510-142">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="6d510-142">How do I manage my connections?</span></span>

<span data-ttu-id="6d510-143">Вы можете управлять подключениями со вкладки [Соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в центре администрирования [Microsoft 365.](https://admin.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="6d510-143">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="6d510-144">Дополнительные сведения об управлении подключениями см. в рублях: [Управление подключениями.](manage-connector.md)</span><span class="sxs-lookup"><span data-stu-id="6d510-144">For more information about managing connections, see: [Manage your connections](manage-connector.md).</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a><span data-ttu-id="6d510-145">Каковы требования к лицензиям и условия использования для соединители Graph?</span><span class="sxs-lookup"><span data-stu-id="6d510-145">What are the license requirements and terms of use for Graph connectors?</span></span>

<span data-ttu-id="6d510-146">Вам нужна действительная лицензия Microsoft 365 или Office 365 и достаточную квоту соединителов графа для пользователей в организации для просмотра данных соединителов в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="6d510-146">You need a valid Microsoft 365 or Office 365 license and sufficient Graph Connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="6d510-147">Дополнительные новости см. в дополнительных подробной информации о требованиях к [лицензиям, ценах](licensing.md) и [сроках использования.](terms-of-use.md)</span><span class="sxs-lookup"><span data-stu-id="6d510-147">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="what-are-the-preview-features"></a><span data-ttu-id="6d510-148">Какие функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="6d510-148">What are the preview features?</span></span>

<span data-ttu-id="6d510-149">Несмотря на то что соединители Microsoft Graph и API поиска в Microsoft Search теперь доступны, существует несколько функций, которые находятся в предварительном просмотре.</span><span class="sxs-lookup"><span data-stu-id="6d510-149">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that are in preview.</span></span>

<span data-ttu-id="6d510-150">Набор соединители и функции в предварительном просмотре включают в себя:</span><span class="sxs-lookup"><span data-stu-id="6d510-150">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="6d510-151">Соединителю Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="6d510-151">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="6d510-152">Соединители salesforce</span><span class="sxs-lookup"><span data-stu-id="6d510-152">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="6d510-153">[Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска с использованием исходных acLs</span><span class="sxs-lookup"><span data-stu-id="6d510-153">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="6d510-154">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="6d510-154">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="6d510-155">Несколько подключений в вертикали</span><span class="sxs-lookup"><span data-stu-id="6d510-155">Multiple connections in a vertical</span></span>](customize-search-page.md#multiple-connections-in-a-vertical)

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="6d510-156">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="6d510-156">How do I customize and configure search results?</span></span>

<span data-ttu-id="6d510-157">Существует множество способов настройки и настройки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="6d510-157">There are many ways to customize and configure search results.</span></span> <span data-ttu-id="6d510-158">Дополнительные статьи см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="6d510-158">See the following articles to learn more:</span></span>

* [<span data-ttu-id="6d510-159">Управление вертикалями и типами результатов</span><span class="sxs-lookup"><span data-stu-id="6d510-159">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="6d510-160">Управление макетами результатов поиска</span><span class="sxs-lookup"><span data-stu-id="6d510-160">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="6d510-161">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="6d510-161">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="6d510-162">Управление пользовательскими фильтрами</span><span class="sxs-lookup"><span data-stu-id="6d510-162">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="6d510-163">Как искать данные соединитетеля в настраиваемом приложении?</span><span class="sxs-lookup"><span data-stu-id="6d510-163">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="6d510-164">После индексации пользовательских данных разработчики могут [запрашивать эти данные.](/graph/search-concept-custom-types)</span><span class="sxs-lookup"><span data-stu-id="6d510-164">After custom data is indexed, developers can [query this data](/graph/search-concept-custom-types).</span></span> <span data-ttu-id="6d510-165">Вы можете просматривать данные в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="6d510-165">You can view your data in any application.</span></span> <span data-ttu-id="6d510-166">Дополнительные сведения см. в [обзоре API поиска Майкрософт в Microsoft Graph.](/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="6d510-166">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](/graph/search-concept-overview).</span></span>

## <a name="how-do-i-customize-search-results"></a><span data-ttu-id="6d510-167">Как настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="6d510-167">How do I customize search results?</span></span>

<span data-ttu-id="6d510-168">Следующим шагом является настройка результатов поиска, как рекомендуется в этой статье Как настроить и [настроить результаты поиска?](#how-do-i-customize-and-configure-search-results).</span><span class="sxs-lookup"><span data-stu-id="6d510-168">The next step is to customize the search results as recommended in this article [How do I customize and configure search results?](#how-do-i-customize-and-configure-search-results).</span></span> <span data-ttu-id="6d510-169">Дополнительные информацию о настройке результатов поиска см. в странице [Настройка страницы результатов поиска.](customize-search-page.md)</span><span class="sxs-lookup"><span data-stu-id="6d510-169">To learn more about customizing search results, see [Customize the search results page](customize-search-page.md).</span></span>

## <a name="what-are-the-connector-limitations"></a><span data-ttu-id="6d510-170">Какие ограничения имеют соединители?</span><span class="sxs-lookup"><span data-stu-id="6d510-170">What are the connector limitations?</span></span>

* <span data-ttu-id="6d510-171">При **публикации** соединитетеля, созданного Корпорацией Майкрософт, может занять несколько минут для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="6d510-171">When you **publish** a Microsoft-built connector, it can take a few minutes for the connection to be created.</span></span> <span data-ttu-id="6d510-172">В течение этого времени подключение будет показывать свое состояние как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="6d510-172">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="6d510-173">Пропускная способность ingestion отламеяна при приближении четырех элементов в секунду.</span><span class="sxs-lookup"><span data-stu-id="6d510-173">Ingestion throughput is throttled at approimately four items per second.</span></span>

* <span data-ttu-id="6d510-174">Обновления схемы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="6d510-174">There is no support for schema updates.</span></span> <span data-ttu-id="6d510-175">После создания настройки подключения не будет возможности обновить схему.</span><span class="sxs-lookup"><span data-stu-id="6d510-175">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="6d510-176">Вы можете только удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="6d510-176">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="6d510-177">Существует ограничение подключения.</span><span class="sxs-lookup"><span data-stu-id="6d510-177">There is a connection limit.</span></span> <span data-ttu-id="6d510-178">Каждый клиент может создать до 10 подключений.</span><span class="sxs-lookup"><span data-stu-id="6d510-178">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="6d510-179">Вы не можете изменить или изменить подключение после его создания.</span><span class="sxs-lookup"><span data-stu-id="6d510-179">You cannot edit or change a connection after it has been created.</span></span> <span data-ttu-id="6d510-180">Если вам необходимо изменить какие-либо сведения, необходимо удалить и воссоздать подключение.</span><span class="sxs-lookup"><span data-stu-id="6d510-180">If you need to change any details, you must delete and recreate the connection.</span></span>
