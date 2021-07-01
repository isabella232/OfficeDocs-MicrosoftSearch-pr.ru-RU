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
ms.openlocfilehash: 4bcfb871fabae07270611762d2112a6e72d4762b
ms.sourcegitcommit: 93fc70f0073ab45b4dbd702441ac2fc07a7668bc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "53230892"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="4a551-103">Обзор соединителей Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="4a551-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="4a551-104">[Поиск (Майкрософт)](./overview-microsoft-search.md) индексирует все [Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их поиском для пользователей.</span><span class="sxs-lookup"><span data-stu-id="4a551-104">[Microsoft Search](./overview-microsoft-search.md) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="4a551-105">С помощью соедините Graph Microsoft организация может индексировать сторонние данные, чтобы они Поиск (Майкрософт) результатах.</span><span class="sxs-lookup"><span data-stu-id="4a551-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="4a551-106">Эта возможность расширяет типы источников содержимого, по которым можно выполнять поиск как в ориентированных на повышение производительности приложениях Microsoft 365, так и в более широком контексте экосистемы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="4a551-106">This feature expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="4a551-107">Сторонние данные могут быть организованы на локальной основе или в общедоступных или частных облаках.</span><span class="sxs-lookup"><span data-stu-id="4a551-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="4a551-108">Эта статья призвана помочь администраторам Microsoft 365 найти ресурсы, доступные для ответа на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="4a551-108">This article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="4a551-109">Какие источники данных можно подключать к Поиск (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="4a551-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="4a551-110">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="4a551-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="4a551-111">Каковы требования к лицензиям и условия использования для соединители Microsoft Graph?</span><span class="sxs-lookup"><span data-stu-id="4a551-111">What are the license requirements and terms of use for Microsoft Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-connectors)
* [<span data-ttu-id="4a551-112">Какие функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="4a551-112">What are the preview features?</span></span>](#what-are-the-preview-features)
* [<span data-ttu-id="4a551-113">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="4a551-113">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="4a551-114">Как искать данные соединитетеля в настраиваемом приложении?</span><span class="sxs-lookup"><span data-stu-id="4a551-114">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)
* [<span data-ttu-id="4a551-115">Как настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="4a551-115">How do I customize search results?</span></span>](#how-do-i-customize-search-results)
* [<span data-ttu-id="4a551-116">Каковы ограничения соединитетеля</span><span class="sxs-lookup"><span data-stu-id="4a551-116">What are the connector limitations</span></span>](#what-are-the-connector-limitations)

<!---Modify to another note that is more accurate after rollout completion--->
> [!IMPORTANT]
> <span data-ttu-id="4a551-117">Теперь Graph и Поиск (Майкрософт) API Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4a551-117">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="4a551-118">Первыми выкатами будут клиенты, настроенные для целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="4a551-118">The first rollouts will be to customers configured for  targeted release.</span></span> <span data-ttu-id="4a551-119">Если вы хотите использовать соединители Graph в клиенте, пользователи и администраторы должны выбрать [целевой выпуск](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="4a551-119">If you want to use a Graph connector in your tenant, users and administrators must opt into [Targeted release](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide).</span></span>

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

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="4a551-120">Какие источники данных можно подключать к Поиск (Майкрософт)?</span><span class="sxs-lookup"><span data-stu-id="4a551-120">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="4a551-121">Корпорация Майкрософт предоставляет 9 соединители, а наши партнеры по экосистеме создали более 100 соединители.</span><span class="sxs-lookup"><span data-stu-id="4a551-121">Microsoft provides 9 connectors and our ecosystem partners have created over 100 more connectors.</span></span> <span data-ttu-id="4a551-122">Вы также можете создать собственный соединитектор.</span><span class="sxs-lookup"><span data-stu-id="4a551-122">You can also build your own connector.</span></span>

### <a name="microsoft-graph-connectors-by-microsoft"></a><span data-ttu-id="4a551-123">Соединители Graph Майкрософт</span><span class="sxs-lookup"><span data-stu-id="4a551-123">Microsoft Graph connectors by Microsoft</span></span>

<span data-ttu-id="4a551-124">Вы можете подключиться к следующим источникам данных с помощью соединители, созданные Корпорацией Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="4a551-124">You can connect to the following data sources using connectors created by Microsoft:</span></span>

<!---Add links below when new docs are created--->
* [<span data-ttu-id="4a551-125">Azure Data Lake Storage 2-го поколения</span><span class="sxs-lookup"><span data-stu-id="4a551-125">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="4a551-126">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="4a551-126">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="4a551-127">Azure SQL и Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="4a551-127">Azure SQL and Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="4a551-128">Корпоративные веб-сайты</span><span class="sxs-lookup"><span data-stu-id="4a551-128">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="4a551-129">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="4a551-129">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="4a551-130">Файловый ресурс</span><span class="sxs-lookup"><span data-stu-id="4a551-130">File share</span></span>](fileshare-connector.md)
* [<span data-ttu-id="4a551-131">Oracle SQL</span><span class="sxs-lookup"><span data-stu-id="4a551-131">Oracle SQL</span></span>](OracleSQL-connector.md)
* [<span data-ttu-id="4a551-132">Salesforce (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4a551-132">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="4a551-133">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="4a551-133">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="4a551-134">В [галерее соедините](https://www.microsoft.com/microsoft-search/connectors) Graph Microsoft содержится краткое описание каждого из этих соединитетелей.</span><span class="sxs-lookup"><span data-stu-id="4a551-134">The [Microsoft Graph connectors gallery](https://www.microsoft.com/microsoft-search/connectors) contains a brief description of each of these connectors.</span></span> <span data-ttu-id="4a551-135">Если вы готовы подключить один из этих источников данных к вашему клиенту, обязательно ознакомьтесь с обзором установки и другими статьями в разделе Установки в разделе Microsoft, которые применяются к источнику данных. [](configure-connector.md)</span><span class="sxs-lookup"><span data-stu-id="4a551-135">If you're ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="microsoft-graph-connectors-by-our-partners"></a><span data-ttu-id="4a551-136">Соединители Graph Майкрософт нашими партнерами</span><span class="sxs-lookup"><span data-stu-id="4a551-136">Microsoft Graph connectors by our partners</span></span>

<span data-ttu-id="4a551-137">Галерея [соедините Graph](https://www.microsoft.com/microsoft-search/connectors) Майкрософт содержит краткое описание каждого из соединители, созданных нашими партнерами, и ссылку на веб-сайт каждого партнера.</span><span class="sxs-lookup"><span data-stu-id="4a551-137">The [Microsoft Graph connectors gallery](https://www.microsoft.com/microsoft-search/connectors) includes a brief description of each of the connectors created by our partners, and a link to each partner's website.</span></span> <span data-ttu-id="4a551-138">Чтобы узнать больше, свяжитесь с каждым партнером напрямую.</span><span class="sxs-lookup"><span data-stu-id="4a551-138">To learn more, contact each partner directly.</span></span>

### <a name="build-your-own-microsoft-graph-connector"></a><span data-ttu-id="4a551-139">Создание собственного соединитетеля Graph Майкрософт</span><span class="sxs-lookup"><span data-stu-id="4a551-139">Build your own Microsoft Graph connector</span></span>

<span data-ttu-id="4a551-140">При желании можно создать собственный соединититель.</span><span class="sxs-lookup"><span data-stu-id="4a551-140">You can build your own connector if you prefer.</span></span> <span data-ttu-id="4a551-141">Дополнительные сведения о создании соединители см. в записи Сборка первого [настраиваемой соединители Microsoft Graph.](/graph/connecting-external-content-build-quickstart)</span><span class="sxs-lookup"><span data-stu-id="4a551-141">For more information on building connectors, see  [Build your first custom Microsoft Graph connector](/graph/connecting-external-content-build-quickstart).</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="4a551-142">Как управлять подключениями?</span><span class="sxs-lookup"><span data-stu-id="4a551-142">How do I manage my connections?</span></span>

<span data-ttu-id="4a551-143">Вы можете управлять подключениями со вкладки [Соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в [Центр администрирования Microsoft 365.](https://admin.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="4a551-143">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="4a551-144">Дополнительные сведения об управлении подключениями см. в рублях: [Управление подключениями.](manage-connector.md)</span><span class="sxs-lookup"><span data-stu-id="4a551-144">For more information about managing connections, see: [Manage your connections](manage-connector.md).</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-connectors"></a><span data-ttu-id="4a551-145">Каковы требования к лицензиям и условия использования соединители?</span><span class="sxs-lookup"><span data-stu-id="4a551-145">What are the license requirements and terms of use for connectors?</span></span>

<span data-ttu-id="4a551-146">Для просмотра данных из соединители в результатах поиска Microsoft 365 или Office 365 лицензии и достаточной квоты соединителов для пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="4a551-146">You need a valid Microsoft 365 or Office 365 license and sufficient connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="4a551-147">Дополнительные новости см. в дополнительных подробной информации о требованиях к [лицензиям, ценах](licensing.md) и [сроках использования.](terms-of-use.md)</span><span class="sxs-lookup"><span data-stu-id="4a551-147">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="what-are-the-preview-features"></a><span data-ttu-id="4a551-148">Какие функции предварительного просмотра?</span><span class="sxs-lookup"><span data-stu-id="4a551-148">What are the preview features?</span></span>

<span data-ttu-id="4a551-149">Несмотря на Graph и Поиск (Майкрософт) API, в настоящее время доступны несколько функций, которые находятся в предварительном просмотре.</span><span class="sxs-lookup"><span data-stu-id="4a551-149">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that are in preview.</span></span>

<span data-ttu-id="4a551-150">Набор соединители и функции в предварительном просмотре включают в себя:</span><span class="sxs-lookup"><span data-stu-id="4a551-150">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="4a551-151">Azure DevOps соединители</span><span class="sxs-lookup"><span data-stu-id="4a551-151">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="4a551-152">Соединители salesforce</span><span class="sxs-lookup"><span data-stu-id="4a551-152">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="4a551-153">[Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска с использованием исходных acLs</span><span class="sxs-lookup"><span data-stu-id="4a551-153">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="4a551-154">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="4a551-154">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="4a551-155">Несколько подключений в вертикали</span><span class="sxs-lookup"><span data-stu-id="4a551-155">Multiple connections in a vertical</span></span>](customize-search-page.md#multiple-connections-in-a-vertical)

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="4a551-156">Как настроить и настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="4a551-156">How do I customize and configure search results?</span></span>

<span data-ttu-id="4a551-157">Существует множество способов настройки и настройки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="4a551-157">There are many ways to customize and configure search results.</span></span> <span data-ttu-id="4a551-158">Дополнительные статьи см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="4a551-158">See the following articles to learn more:</span></span>

* [<span data-ttu-id="4a551-159">Управление вертикалями и типами результатов</span><span class="sxs-lookup"><span data-stu-id="4a551-159">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="4a551-160">Управление макетами результатов поиска</span><span class="sxs-lookup"><span data-stu-id="4a551-160">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="4a551-161">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="4a551-161">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="4a551-162">Управление пользовательскими фильтрами</span><span class="sxs-lookup"><span data-stu-id="4a551-162">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="4a551-163">Как искать данные соединитетеля в настраиваемом приложении?</span><span class="sxs-lookup"><span data-stu-id="4a551-163">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="4a551-164">После индексации пользовательских данных разработчики могут [запрашивать эти данные.](/graph/search-concept-custom-types)</span><span class="sxs-lookup"><span data-stu-id="4a551-164">After custom data is indexed, developers can [query this data](/graph/search-concept-custom-types).</span></span> <span data-ttu-id="4a551-165">Вы можете просматривать данные в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="4a551-165">You can view your data in any application.</span></span> <span data-ttu-id="4a551-166">Дополнительные сведения см. в [обзоре API Поиск (Майкрософт) Microsoft Graph.](/graph/search-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="4a551-166">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](/graph/search-concept-overview).</span></span>

## <a name="how-do-i-customize-search-results"></a><span data-ttu-id="4a551-167">Как настроить результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="4a551-167">How do I customize search results?</span></span>

<span data-ttu-id="4a551-168">Следующим шагом является настройка результатов поиска, как рекомендуется в этой статье Как настроить и [настроить результаты поиска?](#how-do-i-customize-and-configure-search-results).</span><span class="sxs-lookup"><span data-stu-id="4a551-168">The next step is to customize the search results as recommended in this article [How do I customize and configure search results?](#how-do-i-customize-and-configure-search-results).</span></span> <span data-ttu-id="4a551-169">Дополнительные информацию о настройке результатов поиска см. в странице [Настройка страницы результатов поиска.](customize-search-page.md)</span><span class="sxs-lookup"><span data-stu-id="4a551-169">To learn more about customizing search results, see [Customize the search results page](customize-search-page.md).</span></span>

## <a name="what-are-the-connector-limitations"></a><span data-ttu-id="4a551-170">Какие ограничения имеют соединители?</span><span class="sxs-lookup"><span data-stu-id="4a551-170">What are the connector limitations?</span></span>

* <span data-ttu-id="4a551-171">При **публикации** соединитетеля, созданного Корпорацией Майкрософт, может занять несколько минут для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="4a551-171">When you **publish** a Microsoft-built connector, it can take a few minutes for the connection to be created.</span></span> <span data-ttu-id="4a551-172">В течение этого времени подключение будет показывать свое состояние как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="4a551-172">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="4a551-173">Пропускная способность ingestion отламеяна примерно по четырем пунктам в секунду.</span><span class="sxs-lookup"><span data-stu-id="4a551-173">Ingestion throughput is throttled at approximately four items per second.</span></span>

* <span data-ttu-id="4a551-174">Обновления схемы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="4a551-174">There is no support for schema updates.</span></span> <span data-ttu-id="4a551-175">После создания настройки подключения не будет возможности обновить схему.</span><span class="sxs-lookup"><span data-stu-id="4a551-175">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="4a551-176">Вы можете только удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="4a551-176">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="4a551-177">Существует ограничение подключения.</span><span class="sxs-lookup"><span data-stu-id="4a551-177">There is a connection limit.</span></span> <span data-ttu-id="4a551-178">Каждый клиент может создать до 10 подключений.</span><span class="sxs-lookup"><span data-stu-id="4a551-178">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="4a551-179">Вы не можете изменить или изменить подключение после его создания.</span><span class="sxs-lookup"><span data-stu-id="4a551-179">You cannot edit or change a connection after it has been created.</span></span> <span data-ttu-id="4a551-180">Если вам необходимо изменить какие-либо сведения, необходимо удалить и воссоздать подключение.</span><span class="sxs-lookup"><span data-stu-id="4a551-180">If you need to change any details, you must delete and recreate the connection.</span></span>
