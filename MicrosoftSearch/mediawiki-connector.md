---
title: Соединитель Медиавики для службы поиска Майкрософт
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединителя Медиавики для поиска Майкрософт
ms.openlocfilehash: b9c8d80ae5cb8e86b0f6341bfe9231b709569e7a
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "47423021"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="812ce-103">Соединитель Медиавики</span><span class="sxs-lookup"><span data-stu-id="812ce-103">MediaWiki connector</span></span>

<span data-ttu-id="812ce-104">С помощью соединителя Медиавики организация может обнаруживать и индексировать данные из вики-сайта, созданного с помощью программного обеспечения Медиавики.</span><span class="sxs-lookup"><span data-stu-id="812ce-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="812ce-105">Этот соединитель индексирует указанное содержимое в Microsoft Search и поддерживает периодические обходы контента для поддержания индекса в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="812ce-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="812ce-106">Эта статья предназначена для администраторов Microsoft 365 или пользователей, которые настраивают, запускают и осуществляют мониторинг соединителя Медиавики.</span><span class="sxs-lookup"><span data-stu-id="812ce-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki connector.</span></span> <span data-ttu-id="812ce-107">В этой статье объясняется, как настроить возможности соединителя и соединителя, ограничения и способы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="812ce-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="812ce-108">Подключение к источнику данных</span><span class="sxs-lookup"><span data-stu-id="812ce-108">Connect to a data source</span></span>

<span data-ttu-id="812ce-109">Введите URL-адрес и учетные данные Медиавики для проверки подлинности подключения.</span><span class="sxs-lookup"><span data-stu-id="812ce-109">Enter your MediaWiki URL and credentials for authenticating the connection.</span></span> <span data-ttu-id="812ce-110">Вам потребуются следующие сведения: **идентификатор клиента**, **идентификатор ресурса**, **идентификатор клиента**и **секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="812ce-110">You'll need the following information: **Tenant ID**, **Resource ID**, **Client ID**, and the **Client Secret**.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="812ce-111">Управление схемой поиска</span><span class="sxs-lookup"><span data-stu-id="812ce-111">Manage the search schema</span></span>

<span data-ttu-id="812ce-112">После успешного подключения настройте сопоставление схемы поиска.</span><span class="sxs-lookup"><span data-stu-id="812ce-112">After successful connection, configure the search schema mapping.</span></span> <span data-ttu-id="812ce-113">Вы можете выбрать свойства, которые будут доступны для **запроса**, **поиска**и **извлечения**.</span><span class="sxs-lookup"><span data-stu-id="812ce-113">You can choose which properties to make **queryable**, **searchable**, and **retrievable**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="812ce-114">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="812ce-114">Manage search permissions</span></span>

<span data-ttu-id="812ce-115">Соединитель Медиавики поддерживает только разрешения поиска, видимые **всем пользователям**.</span><span class="sxs-lookup"><span data-stu-id="812ce-115">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="812ce-116">Индексированные данные отображаются в результатах поиска и видимы всем пользователям в Организации.</span><span class="sxs-lookup"><span data-stu-id="812ce-116">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="812ce-117">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="812ce-117">Set the refresh schedule</span></span>

<span data-ttu-id="812ce-118">Это расписание обновляет индексированные данные, поэтому изменения в вики-сайте отражаются в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="812ce-118">This schedule refreshes indexed data, so changes to the wiki are reflected in Microsoft Search.</span></span> <span data-ttu-id="812ce-119">Все новые страницы, удаленные страницы, содержимое страниц или изменения метаданных отображаются в результатах поиска по истечении указанного интервала обновления.</span><span class="sxs-lookup"><span data-stu-id="812ce-119">All new pages, deleted pages, page content, or metadata changes appear in search results after the specified refresh interval.</span></span> <span data-ttu-id="812ce-120">Время обхода зависит от размера вики-сайта.</span><span class="sxs-lookup"><span data-stu-id="812ce-120">The crawl time is dependent on the size of the wiki.</span></span> <span data-ttu-id="812ce-121">В настоящее время выполняется обход для соединителя 50 страниц в минуту.</span><span class="sxs-lookup"><span data-stu-id="812ce-121">Currently the connector crawls at around 50 pages per minute.</span></span>

## <a name="limitations"></a><span data-ttu-id="812ce-122">Ограничения</span><span class="sxs-lookup"><span data-stu-id="812ce-122">Limitations</span></span>

<span data-ttu-id="812ce-123">Медиавики Connector имеет следующие ограничения в предварительной версии:</span><span class="sxs-lookup"><span data-stu-id="812ce-123">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="812ce-124">Поддержка только облачных вики-сайтов.</span><span class="sxs-lookup"><span data-stu-id="812ce-124">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="812ce-125">Поддерживает только базовые или OAuth 2,0 с проверкой подлинности Azure Active Directory или Azure.</span><span class="sxs-lookup"><span data-stu-id="812ce-125">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="812ce-126">Не поддерживает выбор пространства имен для индексирования.</span><span class="sxs-lookup"><span data-stu-id="812ce-126">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="812ce-127">Индексирует только пространства имен **Main**, **Category**и **File** .</span><span class="sxs-lookup"><span data-stu-id="812ce-127">Indexes only **Main**, **Category**, and **File** namespaces.</span></span>
* <span data-ttu-id="812ce-128">Не поддерживает списки управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="812ce-128">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="812ce-129">Таким образом, индексированные страницы видны всем пользователям в Организации.</span><span class="sxs-lookup"><span data-stu-id="812ce-129">Thus, indexed pages are visible to all users in the organization.</span></span>
