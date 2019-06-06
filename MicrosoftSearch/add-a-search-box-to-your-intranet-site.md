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
ROBOTS: NoIndex
description: Быстрее получайте релевантные варианты поиска и находите результаты, связанные с работой, добавив поле Поиска (Майкрософт) на сайт или страницу интрасети.
ms.openlocfilehash: ea3efc224b69ffe894104068b055efe8b5882cc1
ms.sourcegitcommit: fe7f3dae4edba97071a4d127e8a27bdf4fa00d81
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2019
ms.locfileid: "34727927"
---
# <a name="add-a-search-box-to-your-intranet-site"></a><span data-ttu-id="b8411-103">Добавление поля поиска на сайте интрасети</span><span class="sxs-lookup"><span data-stu-id="b8411-103">Add a search box to your intranet site</span></span>

<span data-ttu-id="b8411-104">Чтобы обеспечить быстрый доступ к релевантным вариантам поиска и результатам, связанным с работой, добавьте поле Поиска (Майкрософт) на любой сайт или страницу интрасети.</span><span class="sxs-lookup"><span data-stu-id="b8411-104">For fast access to relevant search suggestions and work results, add a Microsoft Search search box to any intranet site or page.</span></span>
  
## <a name="add-a-search-box-to-an-intranet-page"></a><span data-ttu-id="b8411-105">Добавление поля поиска на странице интрасети</span><span class="sxs-lookup"><span data-stu-id="b8411-105">Add a search box to an intranet page</span></span>

<span data-ttu-id="b8411-106">Нужно добавить на страницу два элемента: контейнер для поля поиска и скрипт, который его запустит.</span><span class="sxs-lookup"><span data-stu-id="b8411-106">You need to add two elements to the page: a container for the search box and the script that powers it.</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

<span data-ttu-id="b8411-107">На классическом сайте SharePoint добавьте веб-часть редактора скриптов и вставьте в нее этот скрипт.</span><span class="sxs-lookup"><span data-stu-id="b8411-107">On a SharePoint classic site, add a Script Editor Web Part and drop the script in it.</span></span>
  
## <a name="enable-the-search-box-for-mobile"></a><span data-ttu-id="b8411-108">Включение поля поиска для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="b8411-108">Enable the search box for mobile</span></span>

<span data-ttu-id="b8411-109">Для сайтов и страниц интрасети, которые доступны пользователям мобильных устройств, добавьте в объект параметров строку "isMobile: true":</span><span class="sxs-lookup"><span data-stu-id="b8411-109">For intranet sites or pages available to mobile users, add isMobile: true to the settings object:</span></span>
  
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

## <a name="put-focus-on-the-search-box-by-default"></a><span data-ttu-id="b8411-110">Установка фокуса в поле поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b8411-110">Put focus on the search box by default</span></span>

<span data-ttu-id="b8411-111">Чтобы пользователи быстрее находили нужную информацию, установите курсор в поле поиска, когда страница или сайт загружается. Для этого добавьте в объект параметров строку "focus: true":</span><span class="sxs-lookup"><span data-stu-id="b8411-111">To help users search faster, when the page or site loads place the cursor in the search box by adding focus: true to the settings object:</span></span>
  
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

## <a name="customize-the-appearance-of-the-search-box"></a><span data-ttu-id="b8411-112">Настройка внешнего вида поля поиска</span><span class="sxs-lookup"><span data-stu-id="b8411-112">Customize the appearance of the search box</span></span> 

<span data-ttu-id="b8411-113">Чтобы поле поиска лучше подходило стилю вашей интрасети, можно использовать различные параметры настройки.</span><span class="sxs-lookup"><span data-stu-id="b8411-113">To help the search box better fit with the style of your intranet, there are a variety of configuration options you can use.</span></span> <span data-ttu-id="b8411-114">Комбинируйте параметры в соответствии со своими потребностями.</span><span class="sxs-lookup"><span data-stu-id="b8411-114">Mix and match options to suit your needs.</span></span>

```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox",
        width: 560,                             // default: 560, min: 360, max: 650
        height: 40,                             // default: 40, min: 40, max: 72
        cornerRadius: 6,                        // default: 6, min: 0, max: 25                                   
        strokeOutline: true,                    // default: true
        dropShadow: true,                       // default: true
        iconColor: "#067FA6",                   // default: #067FA6
        companyNameInGhostText: "Contoso"       // default: not specified
                                                // when absent, ghost text will be "Search work and the web"
                                                // when specified, text will be "Search the web and [Contoso]"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="use-an-iframe-to-embed-a-search-box"></a><span data-ttu-id="b8411-115">Внедрение поля поиска с помощью iFrame</span><span class="sxs-lookup"><span data-stu-id="b8411-115">Use an iFrame to embed a search box</span></span>

<span data-ttu-id="b8411-116">Если внедрить скрипт на сайт невозможно, добавьте поле поиска с помощью iFrame.</span><span class="sxs-lookup"><span data-stu-id="b8411-116">If embedding a script isn't an option for the site, use an iFrame to add the search box.</span></span> <span data-ttu-id="b8411-117">Вы не сможете настроить внешний вид поля поиска.</span><span class="sxs-lookup"><span data-stu-id="b8411-117">You won't be able to customize the appearance of the search box.</span></span>
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```