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
ROBOTS: NOINDEX
description: Создание результатов, связанных с работой, для Поиска (Майкрософт) с помощью поисковых запросов из SharePoint
ms.openlocfilehash: 1538c57a7b4138b36fe62e3076feb58d746b2b3e
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591605"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a><span data-ttu-id="295fc-103">Импорт популярных запросов и повышенных результатов SharePoint</span><span class="sxs-lookup"><span data-stu-id="295fc-103">Import SharePoint promoted results and top queries</span></span>

> [!IMPORTANT]
> <span data-ttu-id="295fc-104">Эта статья относится к Поиску (Майкрософт) на портале администрирования Bing.</span><span class="sxs-lookup"><span data-stu-id="295fc-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="295fc-105">Мы переносим портал в Центр администрирования Microsoft 365 с последующим его удалением.</span><span class="sxs-lookup"><span data-stu-id="295fc-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="295fc-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="295fc-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="295fc-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="295fc-107">[Overview of Microsoft Search](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="295fc-108">Чтобы использовать запросы пользователей и наиболее подходящие элементы, созданные в SharePoint, Поиск (Майкрософт) содержит два средства для импорта этих сведений в виде рекомендуемых закладок:</span><span class="sxs-lookup"><span data-stu-id="295fc-108">To leverage users' queries and Best Bets you've created in SharePoint, Microsoft Search includes two tools to import this information as suggested bookmarks:</span></span> 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a><span data-ttu-id="295fc-109">Импорт правил запросов повышенных результатов SharePoint</span><span class="sxs-lookup"><span data-stu-id="295fc-109">Import SharePoint promoted result query rules</span></span>

<span data-ttu-id="295fc-110">Импортируйте эти правила (прежнее название — наиболее подходящие элементы) в виде рекомендуемых закладок.</span><span class="sxs-lookup"><span data-stu-id="295fc-110">Import these rules, previously called Best Bets, as suggested bookmarks.</span></span> <span data-ttu-id="295fc-111">Чтобы сделать их доступными для пользователей, опубликуйте их.</span><span class="sxs-lookup"><span data-stu-id="295fc-111">To make them available to your users, publish them.</span></span> <span data-ttu-id="295fc-112">Время публикации зависит от количества выбранных закладок.</span><span class="sxs-lookup"><span data-stu-id="295fc-112">Publishing time varies based on the number of bookmarks you select.</span></span>
  
## <a name="import-top-sharepoint-queries-using-powershell"></a><span data-ttu-id="295fc-113">Импорт популярных запросов SharePoint с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="295fc-113">Import top SharePoint queries using PowerShell</span></span>

- <span data-ttu-id="295fc-114">Скачайте самые популярные запросы из SharePoint.</span><span class="sxs-lookup"><span data-stu-id="295fc-114">Download the top queries from your SharePoint.</span></span> <span data-ttu-id="295fc-115">Сценарий PowerShell запросит ваши учетные данные администратора SharePoint.</span><span class="sxs-lookup"><span data-stu-id="295fc-115">The PowerShell script will prompt you for your SharePoint administrator credentials.</span></span>
    
- <span data-ttu-id="295fc-116">Выполните поиск SharePoint для каждого из самых популярных запросов, чтобы получить самый популярный результат поиска.</span><span class="sxs-lookup"><span data-stu-id="295fc-116">Run a SharePoint search for each of the top queries to get the top search result.</span></span>
    
- <span data-ttu-id="295fc-117">Добавление рекомендуемых закладок на портал администрирования.</span><span class="sxs-lookup"><span data-stu-id="295fc-117">Add suggested bookmarks to the Admin portal.</span></span>
    
- <span data-ttu-id="295fc-118">Самые популярные запросы SharePoint отлично подходят для закладок.</span><span class="sxs-lookup"><span data-stu-id="295fc-118">Your top SharePoint queries are excellent candidates for bookmarks.</span></span> <span data-ttu-id="295fc-119">Используйте сценарий PowerShell, чтобы импортировать их в виде рекомендуемых закладок.</span><span class="sxs-lookup"><span data-stu-id="295fc-119">Use the PowerShell script to import them as suggested bookmarks.</span></span> <span data-ttu-id="295fc-120">Действия сценария:</span><span class="sxs-lookup"><span data-stu-id="295fc-120">This script will:</span></span>
    
<span data-ttu-id="295fc-121">Чтобы ознакомиться со сведениями о требованиях, примерах и доступных параметрах, скачайте сценарий и просмотрите файл сведений.</span><span class="sxs-lookup"><span data-stu-id="295fc-121">For information about requirements, examples, and available parameters, download the script and review the README file.</span></span> <span data-ttu-id="295fc-122">После выполнения сценария PowerShell администратор или редактор должен проверить рекомендуемые закладки и внести необходимые изменения перед их публикацией.</span><span class="sxs-lookup"><span data-stu-id="295fc-122">After the PowerShell script runs, an admin or editor should review the suggested bookmarks and make any necessary edits before they're published.</span></span>

  

