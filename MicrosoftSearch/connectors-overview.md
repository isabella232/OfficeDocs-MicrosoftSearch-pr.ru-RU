---
title: Обзор Graph соединители Майкрософт
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
description: Обзор соединители microsoft Graph для Поиск (Майкрософт)
ms.openlocfilehash: 87645e32e274eb166d6ba008c4ac720667105a1f
ms.sourcegitcommit: 52129e0129a201ec056903b2461d012fda6d3636
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "53383486"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="bd8b1-103">Обзор соединителей Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="bd8b1-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="bd8b1-104">[Поиск (Майкрософт)](./overview-microsoft-search.md) индексирует все [Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их поиском для пользователей.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-104">[Microsoft Search](./overview-microsoft-search.md) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="bd8b1-105">С помощью соедините Graph Microsoft организация может индексировать сторонние данные, чтобы они Поиск (Майкрософт) результатах.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="bd8b1-106">Эта возможность расширяет типы источников содержимого, по которым можно выполнять поиск как в ориентированных на повышение производительности приложениях Microsoft 365, так и в более широком контексте экосистемы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-106">This feature expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="bd8b1-107">Сторонние данные могут быть организованы на локальной основе или в общедоступных или частных облаках.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="bd8b1-108">Эта статья призвана помочь администраторам Microsoft 365 найти ресурсы, доступные для ответа на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="bd8b1-108">This article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="bd8b1-109">Какие источники данных можно подключать к Поиск (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="bd8b1-110">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="bd8b1-111">Каковы требования к лицензиям и условия использования для соединители Microsoft Graph?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-111">What are the license requirements and terms of use for Microsoft Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-connectors)
* [<span data-ttu-id="bd8b1-112">Какие функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-112">What are the preview features?</span></span>](#what-are-the-preview-features)
* [<span data-ttu-id="bd8b1-113">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-113">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="bd8b1-114">Как искать данные соединитетеля в настраиваемом приложении?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-114">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)
* [<span data-ttu-id="bd8b1-115">Как настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-115">How do I customize search results?</span></span>](#how-do-i-customize-search-results)
* [<span data-ttu-id="bd8b1-116">Каковы ограничения соединитетеля</span><span class="sxs-lookup"><span data-stu-id="bd8b1-116">What are the connector limitations</span></span>](#what-are-the-connector-limitations)

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

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="bd8b1-117">Какие источники данных можно подключать к Поиск (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-117">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="bd8b1-118">Корпорация Майкрософт предоставляет 9 соединители, а наши партнеры по экосистеме создали более 100 соединители.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-118">Microsoft provides 9 connectors and our ecosystem partners have created over 100 more connectors.</span></span> <span data-ttu-id="bd8b1-119">Вы также можете создать собственный соединитектор.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-119">You can also build your own connector.</span></span>

### <a name="microsoft-graph-connectors-by-microsoft"></a><span data-ttu-id="bd8b1-120">Соединители Graph Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bd8b1-120">Microsoft Graph connectors by Microsoft</span></span>

<span data-ttu-id="bd8b1-121">Вы можете подключиться к следующим источникам данных с помощью соединители, созданные Корпорацией Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="bd8b1-121">You can connect to the following data sources using connectors created by Microsoft:</span></span>

<!---Add links below when new docs are created--->
* [<span data-ttu-id="bd8b1-122">Azure Data Lake Storage 2-го поколения</span><span class="sxs-lookup"><span data-stu-id="bd8b1-122">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="bd8b1-123">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="bd8b1-123">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="bd8b1-124">Azure SQL и Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="bd8b1-124">Azure SQL and Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="bd8b1-125">Корпоративные веб-сайты</span><span class="sxs-lookup"><span data-stu-id="bd8b1-125">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="bd8b1-126">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="bd8b1-126">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="bd8b1-127">Файловый ресурс</span><span class="sxs-lookup"><span data-stu-id="bd8b1-127">File share</span></span>](fileshare-connector.md)
* [<span data-ttu-id="bd8b1-128">Oracle SQL</span><span class="sxs-lookup"><span data-stu-id="bd8b1-128">Oracle SQL</span></span>](OracleSQL-connector.md)
* [<span data-ttu-id="bd8b1-129">Salesforce (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-129">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="bd8b1-130">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="bd8b1-130">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="bd8b1-131">В [галерее соедините](https://www.microsoft.com/microsoft-search/connectors) Graph Microsoft содержится краткое описание каждого из этих соединитетелей.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-131">The [Microsoft Graph connectors gallery](https://www.microsoft.com/microsoft-search/connectors) contains a brief description of each of these connectors.</span></span> <span data-ttu-id="bd8b1-132">Если вы готовы подключить один из этих источников данных к вашему клиенту, обязательно ознакомьтесь с обзором установки и другими статьями в разделе Установки в разделе Microsoft, которые применяются к источнику данных. [](configure-connector.md)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-132">If you're ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="microsoft-graph-connectors-by-our-partners"></a><span data-ttu-id="bd8b1-133">Соединители Graph Майкрософт нашими партнерами</span><span class="sxs-lookup"><span data-stu-id="bd8b1-133">Microsoft Graph connectors by our partners</span></span>

<span data-ttu-id="bd8b1-134">Галерея [соедините Graph](https://www.microsoft.com/microsoft-search/connectors) Майкрософт содержит краткое описание каждого из соединители, созданных нашими партнерами, и ссылку на веб-сайт каждого партнера.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-134">The [Microsoft Graph connectors gallery](https://www.microsoft.com/microsoft-search/connectors) includes a brief description of each of the connectors created by our partners, and a link to each partner's website.</span></span> <span data-ttu-id="bd8b1-135">Чтобы узнать больше, свяжитесь с каждым партнером напрямую.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-135">To learn more, contact each partner directly.</span></span>

### <a name="build-your-own-microsoft-graph-connector"></a><span data-ttu-id="bd8b1-136">Создание собственного соединитетеля Graph Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bd8b1-136">Build your own Microsoft Graph connector</span></span>

<span data-ttu-id="bd8b1-137">При желании можно создать собственный соединититель.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-137">You can build your own connector if you prefer.</span></span> <span data-ttu-id="bd8b1-138">Дополнительные сведения о создании соединители см. в записи Сборка первого [настраиваемой соединители Microsoft Graph.](/graph/connecting-external-content-build-quickstart)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-138">For more information on building connectors, see  [Build your first custom Microsoft Graph connector](/graph/connecting-external-content-build-quickstart).</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="bd8b1-139">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-139">How do I manage my connections?</span></span>

<span data-ttu-id="bd8b1-140">Вы можете управлять подключениями со вкладки [Соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в [Центр администрирования Microsoft 365.](https://admin.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-140">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="bd8b1-141">Дополнительные сведения об управлении подключениями см. в рублях: [Управление подключениями.](manage-connector.md)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-141">For more information about managing connections, see: [Manage your connections](manage-connector.md).</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-connectors"></a><span data-ttu-id="bd8b1-142">Каковы требования к лицензиям и условия использования соединители?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-142">What are the license requirements and terms of use for connectors?</span></span>

<span data-ttu-id="bd8b1-143">Для просмотра данных из соединители в результатах поиска Microsoft 365 или Office 365 лицензии и достаточной квоты соединителов для пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-143">You need a valid Microsoft 365 or Office 365 license and sufficient connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="bd8b1-144">Дополнительные новости см. в дополнительных подробной информации о требованиях к [лицензиям, ценах](licensing.md) и [сроках использования.](terms-of-use.md)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-144">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="what-are-the-preview-features"></a><span data-ttu-id="bd8b1-145">Какие функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-145">What are the preview features?</span></span>

<span data-ttu-id="bd8b1-146">Несмотря на Graph и Поиск (Майкрософт) API, в настоящее время доступны несколько функций, которые находятся в предварительном просмотре.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-146">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that are in preview.</span></span>

<span data-ttu-id="bd8b1-147">Набор соединители и функции в предварительном просмотре включают в себя:</span><span class="sxs-lookup"><span data-stu-id="bd8b1-147">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="bd8b1-148">Azure DevOps соединители</span><span class="sxs-lookup"><span data-stu-id="bd8b1-148">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="bd8b1-149">Соединители salesforce</span><span class="sxs-lookup"><span data-stu-id="bd8b1-149">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="bd8b1-150">[Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска с использованием исходных acLs</span><span class="sxs-lookup"><span data-stu-id="bd8b1-150">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="bd8b1-151">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="bd8b1-151">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="bd8b1-152">Несколько подключений в вертикали</span><span class="sxs-lookup"><span data-stu-id="bd8b1-152">Multiple connections in a vertical</span></span>](customize-search-page.md#multiple-connections-in-a-vertical)

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="bd8b1-153">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-153">How do I customize and configure search results?</span></span>

<span data-ttu-id="bd8b1-154">Существует множество способов настройки и настройки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-154">There are many ways to customize and configure search results.</span></span> <span data-ttu-id="bd8b1-155">Дополнительные статьи см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="bd8b1-155">See the following articles to learn more:</span></span>

* [<span data-ttu-id="bd8b1-156">Управление вертикалями и типами результатов</span><span class="sxs-lookup"><span data-stu-id="bd8b1-156">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="bd8b1-157">Управление макетами результатов поиска</span><span class="sxs-lookup"><span data-stu-id="bd8b1-157">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="bd8b1-158">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="bd8b1-158">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="bd8b1-159">Управление пользовательскими фильтрами</span><span class="sxs-lookup"><span data-stu-id="bd8b1-159">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="bd8b1-160">Как искать данные соединитетеля в настраиваемом приложении?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-160">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="bd8b1-161">После индексации пользовательских данных разработчики могут [запрашивать эти данные.](/graph/search-concept-custom-types)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-161">After custom data is indexed, developers can [query this data](/graph/search-concept-custom-types).</span></span> <span data-ttu-id="bd8b1-162">Вы можете просматривать данные в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-162">You can view your data in any application.</span></span> <span data-ttu-id="bd8b1-163">Дополнительные сведения см. в [обзоре API Поиск (Майкрософт) Microsoft Graph.](/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-163">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](/graph/search-concept-overview).</span></span>

## <a name="how-do-i-customize-search-results"></a><span data-ttu-id="bd8b1-164">Как настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-164">How do I customize search results?</span></span>

<span data-ttu-id="bd8b1-165">Следующим шагом является настройка результатов поиска, как рекомендуется в этой статье Как настроить и [настроить результаты поиска?](#how-do-i-customize-and-configure-search-results).</span><span class="sxs-lookup"><span data-stu-id="bd8b1-165">The next step is to customize the search results as recommended in this article [How do I customize and configure search results?](#how-do-i-customize-and-configure-search-results).</span></span> <span data-ttu-id="bd8b1-166">Дополнительные информацию о настройке результатов поиска см. в странице [Настройка страницы результатов поиска.](customize-search-page.md)</span><span class="sxs-lookup"><span data-stu-id="bd8b1-166">To learn more about customizing search results, see [Customize the search results page](customize-search-page.md).</span></span>

## <a name="what-are-the-connector-limitations"></a><span data-ttu-id="bd8b1-167">Какие ограничения имеют соединители?</span><span class="sxs-lookup"><span data-stu-id="bd8b1-167">What are the connector limitations?</span></span>

* <span data-ttu-id="bd8b1-168">При **публикации** соединитетеля, созданного Корпорацией Майкрософт, может занять несколько минут для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-168">When you **publish** a Microsoft-built connector, it can take a few minutes for the connection to be created.</span></span> <span data-ttu-id="bd8b1-169">В течение этого времени подключение будет показывать свое состояние как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-169">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="bd8b1-170">Пропускная способность ingestion отламеяна примерно по четырем пунктам в секунду.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-170">Ingestion throughput is throttled at approximately four items per second.</span></span>

* <span data-ttu-id="bd8b1-171">Обновления схемы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-171">There is no support for schema updates.</span></span> <span data-ttu-id="bd8b1-172">После создания настройки подключения не будет возможности обновить схему.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-172">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="bd8b1-173">Вы можете только удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-173">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="bd8b1-174">Существует ограничение подключения.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-174">There is a connection limit.</span></span> <span data-ttu-id="bd8b1-175">Каждый клиент может создать до 10 подключений.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-175">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="bd8b1-176">Вы не можете изменить или изменить подключение после его создания.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-176">You cannot edit or change a connection after it has been created.</span></span> <span data-ttu-id="bd8b1-177">Если вам необходимо изменить какие-либо сведения, необходимо удалить и воссоздать подключение.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-177">If you need to change any details, you must delete and recreate the connection.</span></span>
