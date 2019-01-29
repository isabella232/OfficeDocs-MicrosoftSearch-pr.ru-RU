---
title: Добавление поля поиска на сайте интрасети
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 10/31/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: f980b90f-95e2-4b66-8b21-69f601ff4b50
description: Получайте предложения поиска и поиск результатов рабочих быстрее, добавив поле поиска Microsoft Search в интрасети или страницы.
ms.openlocfilehash: 699cfd9c411c9b86f3a2f8742c425aaedef1ebc5
ms.sourcegitcommit: 1c038d87efab4840d97b1f367b39e2b9ecdfee4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29612420"
---
# <a name="add-a-search-box-to-your-intranet-site"></a><span data-ttu-id="3c1fd-103">Добавление поля поиска на сайте интрасети</span><span class="sxs-lookup"><span data-stu-id="3c1fd-103">Add a search box to your intranet site</span></span>

<span data-ttu-id="3c1fd-104">Для быстрого доступа к предложений поиска и результатов рабочих добавьте поле поиска Microsoft Search для любого сайта интрасети или страницы.</span><span class="sxs-lookup"><span data-stu-id="3c1fd-104">For fast access to relevant search suggestions and work results, add a Microsoft Search search box to any intranet site or page.</span></span>
  
## <a name="add-a-search-box-to-an-intranet-page"></a><span data-ttu-id="3c1fd-105">Добавить поле поиска на страницу интрасети</span><span class="sxs-lookup"><span data-stu-id="3c1fd-105">Add a search box to an intranet page</span></span>

<span data-ttu-id="3c1fd-106">Необходимо добавить два элемента на страницу: контейнер для поля поиска и скрипт, который включает его.</span><span class="sxs-lookup"><span data-stu-id="3c1fd-106">You need to add two elements to the page: a container for the search box and the script that powers it.</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

<span data-ttu-id="3c1fd-107">Классический сайта SharePoint добавьте веб-часть редактора сценариев и поместите сценарий в нем.</span><span class="sxs-lookup"><span data-stu-id="3c1fd-107">On a SharePoint classic site, add a Script Editor Web Part and drop the script in it.</span></span>
  
## <a name="enable-the-search-box-for-mobile"></a><span data-ttu-id="3c1fd-108">Включить поле «Поиск» для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="3c1fd-108">Enable the search box for mobile</span></span>

<span data-ttu-id="3c1fd-109">Для сайтов интрасети или страницы, доступные для пользователей мобильных устройств, добавьте isMobile: ИСТИНА объект параметров:</span><span class="sxs-lookup"><span data-stu-id="3c1fd-109">For intranet sites or pages available to mobile users, add isMobile: true to the settings object:</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox", 
        isMobile: true
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="put-focus-on-the-search-box-by-default"></a><span data-ttu-id="3c1fd-110">Переход на поле поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3c1fd-110">Put focus on the search box by default</span></span>

<span data-ttu-id="3c1fd-111">Чтобы помочь пользователям поиск быстрее, если загружает страницу или сайта поместите курсор в поле «Поиск», добавив фокус: ИСТИНА объект параметров:</span><span class="sxs-lookup"><span data-stu-id="3c1fd-111">To help users search faster, when the page or site loads place the cursor in the search box by adding focus: true to the settings object:</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox",
        focus: true
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="use-an-iframe-to-embed-a-search-box"></a><span data-ttu-id="3c1fd-112">Используйте элемент iFrame для внедрения поля поиска</span><span class="sxs-lookup"><span data-stu-id="3c1fd-112">Use an iFrame to embed a search box</span></span>

<span data-ttu-id="3c1fd-113">Если внедрение сценария не вариант для сайта, используйте элемент iFrame для добавления поля поиска:</span><span class="sxs-lookup"><span data-stu-id="3c1fd-113">If embedding a script isn't an option for the site, use an iFrame to add the search box:</span></span>
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```
