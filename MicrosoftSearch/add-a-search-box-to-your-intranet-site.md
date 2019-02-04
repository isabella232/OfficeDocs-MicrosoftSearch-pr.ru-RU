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
description: Быстрее получайте релевантные варианты поиска и находите результаты, связанные с работой, добавив поле Поиска (Майкрософт) на сайт или страницу интрасети.
ms.openlocfilehash: 699cfd9c411c9b86f3a2f8742c425aaedef1ebc5
ms.sourcegitcommit: 1c038d87efab4840d97b1f367b39e2b9ecdfee4a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29612420"
---
# <a name="add-a-search-box-to-your-intranet-site"></a><span data-ttu-id="c868f-103">Добавление поля поиска на сайте интрасети</span><span class="sxs-lookup"><span data-stu-id="c868f-103">Add a search box to your intranet site</span></span>

<span data-ttu-id="c868f-104">Чтобы обеспечить быстрый доступ к релевантным вариантам поиска и результатам, связанным с работой, добавьте поле Поиска (Майкрософт) на любой сайт или страницу интрасети.</span><span class="sxs-lookup"><span data-stu-id="c868f-104">For fast access to relevant search suggestions and work results, add a Microsoft Search search box to any intranet site or page.</span></span>
  
## <a name="add-a-search-box-to-an-intranet-page"></a><span data-ttu-id="c868f-105">Добавление поля поиска на странице интрасети</span><span class="sxs-lookup"><span data-stu-id="c868f-105">Add a search box to your intranet site</span></span>

<span data-ttu-id="c868f-106">Нужно добавить на страницу два элемента: контейнер для поля поиска и скрипт, который его запустит.</span><span class="sxs-lookup"><span data-stu-id="c868f-106">You need to add two elements to the page: a container for the search box and the script that powers it.</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

<span data-ttu-id="c868f-107">На классическом сайте SharePoint добавьте веб-часть редактора скриптов и вставьте в нее этот скрипт.</span><span class="sxs-lookup"><span data-stu-id="c868f-107">On a SharePoint classic site, add a Script Editor Web Part and drop the script in it.</span></span>
  
## <a name="enable-the-search-box-for-mobile"></a><span data-ttu-id="c868f-108">Включение поля поиска для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="c868f-108">Enable the search box for mobile</span></span>

<span data-ttu-id="c868f-109">Для сайтов и страниц интрасети, которые доступны пользователям мобильных устройств, добавьте в объект параметров строку "isMobile: true":</span><span class="sxs-lookup"><span data-stu-id="c868f-109">For intranet sites or pages available to mobile users, add isMobile: true to the settings object:</span></span>
  
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

## <a name="put-focus-on-the-search-box-by-default"></a><span data-ttu-id="c868f-110">Установка фокуса в поле поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c868f-110">Put focus on the search box by default</span></span>

<span data-ttu-id="c868f-111">Чтобы пользователи быстрее находили нужную информацию, установите курсор в поле поиска, когда страница или сайт загружается. Для этого добавьте в объект параметров строку "focus: true":</span><span class="sxs-lookup"><span data-stu-id="c868f-111">To help users search faster, when the page or site loads place the cursor in the search box by adding focus: true to the settings object:</span></span>
  
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

## <a name="use-an-iframe-to-embed-a-search-box"></a><span data-ttu-id="c868f-112">Внедрение поля поиска с помощью iFrame</span><span class="sxs-lookup"><span data-stu-id="c868f-112">Use an iFrame to embed a search box</span></span>

<span data-ttu-id="c868f-113">Если внедрить скрипт на сайт невозможно, добавьте поле поиска с помощью iFrame:</span><span class="sxs-lookup"><span data-stu-id="c868f-113">If embedding a script isn't an option for the site, use an iFrame to add the search box:</span></span>
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```
