---
title: Импорт популярных запросов и повышенных результатов SharePoint
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 9/8/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 3d2a1498-174e-4214-9cf1-8b58cce5a872
description: Создание результатов, связанных с работой, для Поиска (Майкрософт) с помощью поисковых запросов из SharePoint
ms.openlocfilehash: 6e55e2000792bdb576a18a0efeb353dc3ea13605
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2019
ms.locfileid: "33968454"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a><span data-ttu-id="6bc5b-103">Импорт популярных запросов и повышенных результатов SharePoint</span><span class="sxs-lookup"><span data-stu-id="6bc5b-103">Import SharePoint promoted results and top queries</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bc5b-104">Параметры Поиска (Майкрософт) в Bing теперь доступны в Центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="6bc5b-105">Начните с [назначения администраторов поиска](https://docs.microsoft.com/ru-RU/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) в Центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="6bc5b-106">Чтобы использовать запросы пользователей и наиболее подходящие элементы, созданные в SharePoint, Поиск (Майкрософт) содержит два средства для импорта этих сведений в виде рекомендуемых закладок:</span><span class="sxs-lookup"><span data-stu-id="6bc5b-106">To leverage users' queries and Best Bets you've created in SharePoint, Microsoft Search includes two tools to import this information as suggested bookmarks:</span></span> 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a><span data-ttu-id="6bc5b-107">Импорт правил запросов повышенных результатов SharePoint</span><span class="sxs-lookup"><span data-stu-id="6bc5b-107">Import SharePoint promoted result query rules</span></span>

<span data-ttu-id="6bc5b-108">Импортируйте эти правила (прежнее название — наиболее подходящие элементы) в виде рекомендуемых закладок.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-108">Import these rules, previously called Best Bets, as suggested bookmarks.</span></span> <span data-ttu-id="6bc5b-109">Чтобы сделать их доступными для пользователей, опубликуйте их.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-109">To make them available to your users, publish them.</span></span> <span data-ttu-id="6bc5b-110">Время публикации зависит от количества выбранных закладок.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-110">Publishing time varies based on the number of bookmarks you select.</span></span>
  
## <a name="import-top-sharepoint-queries-using-powershell"></a><span data-ttu-id="6bc5b-111">Импорт популярных запросов SharePoint с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="6bc5b-111">Import top SharePoint queries using PowerShell</span></span>

- <span data-ttu-id="6bc5b-112">Скачайте самые популярные запросы из SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-112">Download the top queries from your SharePoint.</span></span> <span data-ttu-id="6bc5b-113">Сценарий PowerShell запросит ваши учетные данные администратора SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-113">The PowerShell script will prompt you for your SharePoint administrator credentials.</span></span>
    
- <span data-ttu-id="6bc5b-114">Выполните поиск SharePoint для каждого из самых популярных запросов, чтобы получить самый популярный результат поиска.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-114">Run a SharePoint search for each of the top queries to get the top search result.</span></span>
    
- <span data-ttu-id="6bc5b-115">Добавление рекомендуемых закладок на портал администрирования.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-115">Add suggested bookmarks to the Admin portal.</span></span>
    
- <span data-ttu-id="6bc5b-116">Самые популярные запросы SharePoint отлично подходят для закладок.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-116">Your top SharePoint queries are excellent candidates for bookmarks.</span></span> <span data-ttu-id="6bc5b-117">Используйте сценарий PowerShell, чтобы импортировать их в виде рекомендуемых закладок.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-117">Use the PowerShell script to import them as suggested bookmarks.</span></span> <span data-ttu-id="6bc5b-118">Действия сценария:</span><span class="sxs-lookup"><span data-stu-id="6bc5b-118">This script will:</span></span>
    
<span data-ttu-id="6bc5b-119">Чтобы ознакомиться со сведениями о требованиях, примерах и доступных параметрах, скачайте сценарий и просмотрите файл сведений.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-119">For information about requirements, examples, and available parameters, download the script and review the README file.</span></span> <span data-ttu-id="6bc5b-120">После выполнения сценария PowerShell администратор или редактор должен проверить рекомендуемые закладки и внести необходимые изменения перед их публикацией.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-120">After the PowerShell script runs, an admin or editor should review the suggested bookmarks and make any necessary edits before they're published.</span></span>

  

