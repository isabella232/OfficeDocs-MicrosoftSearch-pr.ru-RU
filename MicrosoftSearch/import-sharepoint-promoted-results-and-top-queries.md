---
title: Импорт популярных запросов и рекомендуемых результатов SharePoint
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
description: Использование поисковых запросов из SharePoint для создания результатов работы Microsoft Search
ms.openlocfilehash: f4fa4354fed667800c1cdcf63c86f59d736c342a
ms.sourcegitcommit: a5fd9d4f46bbb7c539630735ac16e0c786939e5d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2019
ms.locfileid: "33508756"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a><span data-ttu-id="69e7e-103">Импорт популярных запросов и рекомендуемых результатов SharePoint</span><span class="sxs-lookup"><span data-stu-id="69e7e-103">Import SharePoint promoted results and top queries</span></span>

<span data-ttu-id="69e7e-104">Чтобы использовать запросы пользователей и наиболее подХодящие элементы, созданные в SharePoint, Microsoft Search включает два средства для импорта этих сведений в виде предложенных закладок:</span><span class="sxs-lookup"><span data-stu-id="69e7e-104">To leverage users' queries and Best Bets you've created in SharePoint, Microsoft Search includes two tools to import this information as suggested bookmarks:</span></span> 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a><span data-ttu-id="69e7e-105">Импорт правил запроса результатов, продвигаемых SharePoint</span><span class="sxs-lookup"><span data-stu-id="69e7e-105">Import SharePoint promoted result query rules</span></span>

<span data-ttu-id="69e7e-106">Импортируйте эти правила, ранее называемые наиболее подХодящими элементами, в качестве предлагаемых закладок.</span><span class="sxs-lookup"><span data-stu-id="69e7e-106">Import these rules, previously called Best Bets, as suggested bookmarks.</span></span> <span data-ttu-id="69e7e-107">Чтобы сделать их доступными для пользователей, опубликуйте их.</span><span class="sxs-lookup"><span data-stu-id="69e7e-107">To make them available to your users, publish them.</span></span> <span data-ttu-id="69e7e-108">Время публикации зависит от количества выбранных закладок.</span><span class="sxs-lookup"><span data-stu-id="69e7e-108">Publishing time varies based on the number of bookmarks you select.</span></span>
  
## <a name="import-top-sharepoint-queries-using-powershell"></a><span data-ttu-id="69e7e-109">Импорт лучших запросов SharePoint с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="69e7e-109">Import top SharePoint queries using PowerShell</span></span>

- <span data-ttu-id="69e7e-110">Скачайте самые популярные запросы из SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69e7e-110">Download the top queries from your SharePoint.</span></span> <span data-ttu-id="69e7e-111">Сценарий PowerShell предложит вам ввести учетные данные администратора SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69e7e-111">The PowerShell script will prompt you for your SharePoint administrator credentials.</span></span>
    
- <span data-ttu-id="69e7e-112">Выполните поиск SharePoint для каждого из самых популярных запросов, чтобы получить высший результат поиска.</span><span class="sxs-lookup"><span data-stu-id="69e7e-112">Run a SharePoint search for each of the top queries to get the top search result.</span></span>
    
- <span data-ttu-id="69e7e-113">Добавьте предложенные закладки на портал администрирования.</span><span class="sxs-lookup"><span data-stu-id="69e7e-113">Add suggested bookmarks to the Admin portal.</span></span>
    
- <span data-ttu-id="69e7e-114">Ваши самые распространенные запросы SharePoint являются отличными кандидатами для закладок.</span><span class="sxs-lookup"><span data-stu-id="69e7e-114">Your top SharePoint queries are excellent candidates for bookmarks.</span></span> <span data-ttu-id="69e7e-115">С помощью скрипта PowerShell импортируйте их как предложенные закладки.</span><span class="sxs-lookup"><span data-stu-id="69e7e-115">Use the PowerShell script to import them as suggested bookmarks.</span></span> <span data-ttu-id="69e7e-116">Этот сценарий позволяет:</span><span class="sxs-lookup"><span data-stu-id="69e7e-116">This script will:</span></span>
    
<span data-ttu-id="69e7e-117">Для получения сведений о требованиях, примерах и доступных параметрах Скачайте сценарий и просмотрите файл README.</span><span class="sxs-lookup"><span data-stu-id="69e7e-117">For information about requirements, examples, and available parameters, download the script and review the README file.</span></span> <span data-ttu-id="69e7e-118">После запуска скрипта PowerShell администратор или редактор должен проверить предложенные закладки и внести необходимые изменения перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="69e7e-118">After the PowerShell script runs, an admin or editor should review the suggested bookmarks and make any necessary edits before they're published.</span></span>

  

