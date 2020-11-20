---
title: Соединитель Медиавики для службы поиска Майкрософт
ms.author: monaray
author: monaray97
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединителя Медиавики для поиска Майкрософт
ms.openlocfilehash: 7f6b34dcafc4b82ab3778ec1d7a4921383e44a44
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367643"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="4f559-103">Соединитель Медиавики</span><span class="sxs-lookup"><span data-stu-id="4f559-103">MediaWiki connector</span></span>

<span data-ttu-id="4f559-104">С помощью соединителя Медиавики организация может обнаруживать и индексировать данные из вики-сайта, созданного с помощью программного обеспечения Медиавики.</span><span class="sxs-lookup"><span data-stu-id="4f559-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="4f559-105">Этот соединитель индексирует указанное содержимое в Microsoft Search и поддерживает периодические обходы контента для поддержания индекса в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4f559-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="4f559-106">Эта статья предназначена для администраторов Microsoft 365 или пользователей, которые настраивают, запускают и осуществляют мониторинг соединителя Медиавики.</span><span class="sxs-lookup"><span data-stu-id="4f559-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki connector.</span></span> <span data-ttu-id="4f559-107">В этой статье объясняется, как настроить возможности соединителя и соединителя, ограничения и способы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="4f559-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="4f559-108">Подключение к источнику данных</span><span class="sxs-lookup"><span data-stu-id="4f559-108">Connect to a data source</span></span>

<span data-ttu-id="4f559-109">Введите URL-адрес и учетные данные Медиавики для проверки подлинности подключения.</span><span class="sxs-lookup"><span data-stu-id="4f559-109">Enter your MediaWiki URL and credentials for authenticating the connection.</span></span> <span data-ttu-id="4f559-110">Вам потребуются следующие сведения: **идентификатор клиента**, **идентификатор ресурса**, **идентификатор клиента** и **секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="4f559-110">You'll need the following information: **Tenant ID**, **Resource ID**, **Client ID**, and the **Client Secret**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="4f559-111">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="4f559-111">Manage search permissions</span></span>

<span data-ttu-id="4f559-112">Соединитель Медиавики поддерживает только разрешения поиска, видимые **всем пользователям**.</span><span class="sxs-lookup"><span data-stu-id="4f559-112">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="4f559-113">Индексированные данные отображаются в результатах поиска и видимы всем пользователям в Организации.</span><span class="sxs-lookup"><span data-stu-id="4f559-113">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="4f559-114">Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="4f559-114">Assign property labels</span></span>

<span data-ttu-id="4f559-115">Можно назначить свойство источника каждой метке, выбрав в меню пункт Параметры.</span><span class="sxs-lookup"><span data-stu-id="4f559-115">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="4f559-116">Хотя это действие не является обязательным, наличие некоторых меток свойств повысит релевантность поиска и обеспечит более точные результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="4f559-116">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="4f559-117">Управление схемой</span><span class="sxs-lookup"><span data-stu-id="4f559-117">Manage schema</span></span>

<span data-ttu-id="4f559-118">На экране **Управление схемой** можно изменить атрибуты схемы (возможность **запроса**, возможность **поиска**, **Извлечение** и **уточнение**), связанные со свойствами, добавить необязательные псевдонимы и выбрать свойство **содержимого** .</span><span class="sxs-lookup"><span data-stu-id="4f559-118">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="4f559-119">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="4f559-119">Set the refresh schedule</span></span>

<span data-ttu-id="4f559-120">Это расписание обновляет индексированные данные, поэтому изменения в вики-сайте отражаются в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="4f559-120">This schedule refreshes indexed data, so changes to the wiki are reflected in Microsoft Search.</span></span> <span data-ttu-id="4f559-121">Все новые страницы, удаленные страницы, содержимое страниц или изменения метаданных отображаются в результатах поиска по истечении указанного интервала обновления.</span><span class="sxs-lookup"><span data-stu-id="4f559-121">All new pages, deleted pages, page content, or metadata changes appear in search results after the specified refresh interval.</span></span> <span data-ttu-id="4f559-122">Время обхода зависит от размера вики-сайта.</span><span class="sxs-lookup"><span data-stu-id="4f559-122">The crawl time is dependent on the size of the wiki.</span></span> <span data-ttu-id="4f559-123">В настоящее время выполняется обход для соединителя 50 страниц в минуту.</span><span class="sxs-lookup"><span data-stu-id="4f559-123">Currently the connector crawls at around 50 pages per minute.</span></span>

## <a name="limitations"></a><span data-ttu-id="4f559-124">Ограничения</span><span class="sxs-lookup"><span data-stu-id="4f559-124">Limitations</span></span>

<span data-ttu-id="4f559-125">Медиавики Connector имеет следующие ограничения в предварительной версии:</span><span class="sxs-lookup"><span data-stu-id="4f559-125">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="4f559-126">Поддержка только облачных вики-сайтов.</span><span class="sxs-lookup"><span data-stu-id="4f559-126">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="4f559-127">Поддерживает только базовые или OAuth 2,0 с проверкой подлинности Azure Active Directory или Azure.</span><span class="sxs-lookup"><span data-stu-id="4f559-127">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="4f559-128">Не поддерживает выбор пространства имен для индексирования.</span><span class="sxs-lookup"><span data-stu-id="4f559-128">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="4f559-129">Индексирует только пространства имен **Main**, **Category** и **File** .</span><span class="sxs-lookup"><span data-stu-id="4f559-129">Indexes only **Main**, **Category**, and **File** namespaces.</span></span>
* <span data-ttu-id="4f559-130">Не поддерживает списки управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="4f559-130">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="4f559-131">Таким образом, индексированные страницы видны всем пользователям в Организации.</span><span class="sxs-lookup"><span data-stu-id="4f559-131">Thus, indexed pages are visible to all users in the organization.</span></span>
