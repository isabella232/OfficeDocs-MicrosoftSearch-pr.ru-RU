---
title: Добавление поля поиска на сайте интрасети
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 10/31/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: f980b90f-95e2-4b66-8b21-69f601ff4b50
ROBOTS: NoIndex
description: Быстрее получайте релевантные варианты поиска и находите результаты, связанные с работой, добавив поле Поиска (Майкрософт) на сайт или страницу интрасети.
ms.openlocfilehash: af12ce4d17c2695e196f8e4d79ccd515f002f238
ms.sourcegitcommit: 92206ea179ec00b22496f6fd2866b5406449cf40
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "44798228"
---
# <a name="add-a-search-box-to-your-intranet-site"></a><span data-ttu-id="c6a63-103">Добавление поля поиска на сайте интрасети</span><span class="sxs-lookup"><span data-stu-id="c6a63-103">Add a search box to your intranet site</span></span>

<span data-ttu-id="c6a63-104">Чтобы предоставить пользователям доступ к результатам из вашей организации, добавьте Microsoft Search в поле поиска Bing на любой сайт или страницу интрасети.</span><span class="sxs-lookup"><span data-stu-id="c6a63-104">To provide your users with easy access to results from your organization, add a Microsoft Search in Bing search box to any intranet site or page.</span></span> <span data-ttu-id="c6a63-105">Ниже приведены некоторые преимущества.</span><span class="sxs-lookup"><span data-stu-id="c6a63-105">These are some of the benefits:</span></span>

- <span data-ttu-id="c6a63-106">Поле поиска на портале SharePoint или интрасети предоставляет известную надежную точку входа для начала поиска</span><span class="sxs-lookup"><span data-stu-id="c6a63-106">A search box on your SharePoint or intranet portal provides a familiar, trusted entry point to start searching</span></span>
- <span data-ttu-id="c6a63-107">Поддержка всех основных веб-браузеров, в том числе Google Chrome и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6a63-107">Supports all major web browsers, including Google Chrome and Microsoft Edge</span></span>
- <span data-ttu-id="c6a63-108">Отображаются только предложения поиска из вашей организации, веб-предложения никогда не включаются</span><span class="sxs-lookup"><span data-stu-id="c6a63-108">Only search suggestions from your organization appear, web suggestions are never included</span></span>
- <span data-ttu-id="c6a63-109">Переводит пользователей на страницу результатов тестирования Microsoft Search, которая исключает рекламу и веб-результаты.</span><span class="sxs-lookup"><span data-stu-id="c6a63-109">Takes users to a Microsoft Search in Bing work results page, which excludes ads and web results</span></span>
- <span data-ttu-id="c6a63-110">Управление внешним видом и поведением поля поиска</span><span class="sxs-lookup"><span data-stu-id="c6a63-110">You control the appearance and behavior of the search box</span></span>
  
## <a name="add-a-search-box-to-an-intranet-page"></a><span data-ttu-id="c6a63-111">Добавление поля поиска на странице интрасети</span><span class="sxs-lookup"><span data-stu-id="c6a63-111">Add a search box to an intranet page</span></span>

<span data-ttu-id="c6a63-112">Нужно добавить на страницу два элемента: контейнер для поля поиска и скрипт, который его запустит.</span><span class="sxs-lookup"><span data-stu-id="c6a63-112">You need to add two elements to the page: a container for the search box and the script that powers it.</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

<span data-ttu-id="c6a63-113">На классическом сайте SharePoint добавьте веб-часть редактора скриптов и вставьте в нее этот скрипт.</span><span class="sxs-lookup"><span data-stu-id="c6a63-113">On a SharePoint classic site, add a Script Editor Web Part and drop the script in it.</span></span>
  
## <a name="enable-the-search-box-for-mobile"></a><span data-ttu-id="c6a63-114">Включение поля поиска для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="c6a63-114">Enable the search box for mobile</span></span>

<span data-ttu-id="c6a63-115">Для сайтов и страниц интрасети, которые доступны пользователям мобильных устройств, добавьте в объект параметров строку "isMobile: true":</span><span class="sxs-lookup"><span data-stu-id="c6a63-115">For intranet sites or pages available to mobile users, add isMobile: true to the settings object:</span></span>
  
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

## <a name="put-focus-on-the-search-box-by-default"></a><span data-ttu-id="c6a63-116">Установка фокуса в поле поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a63-116">Put focus on the search box by default</span></span>

<span data-ttu-id="c6a63-117">Чтобы пользователи быстрее находили нужную информацию, установите курсор в поле поиска, когда страница или сайт загружается. Для этого добавьте в объект параметров строку "focus: true":</span><span class="sxs-lookup"><span data-stu-id="c6a63-117">To help users search faster, when the page or site loads place the cursor in the search box by adding focus: true to the settings object:</span></span>
  
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

## <a name="customize-the-appearance-of-the-search-box"></a><span data-ttu-id="c6a63-118">Настройка внешнего вида поля поиска</span><span class="sxs-lookup"><span data-stu-id="c6a63-118">Customize the appearance of the search box</span></span> 

<span data-ttu-id="c6a63-119">Чтобы поле поиска лучше подходило стилю вашей интрасети, можно использовать различные параметры настройки.</span><span class="sxs-lookup"><span data-stu-id="c6a63-119">To help the search box better fit with the style of your intranet, there are a variety of configuration options you can use.</span></span> <span data-ttu-id="c6a63-120">Комбинируйте параметры в соответствии со своими потребностями.</span><span class="sxs-lookup"><span data-stu-id="c6a63-120">Mix and match options to suit your needs.</span></span>

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
                                                // when absent, ghost text will be "Search work"
                                                // when specified, text will be "Search <companyNameInGhostText>"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="use-an-iframe-to-embed-a-search-box"></a><span data-ttu-id="c6a63-121">Внедрение поля поиска с помощью iFrame</span><span class="sxs-lookup"><span data-stu-id="c6a63-121">Use an iFrame to embed a search box</span></span>

<span data-ttu-id="c6a63-122">Если внедрить скрипт на сайт невозможно, добавьте поле поиска с помощью iFrame.</span><span class="sxs-lookup"><span data-stu-id="c6a63-122">If embedding a script isn't an option for the site, use an iFrame to add the search box.</span></span> <span data-ttu-id="c6a63-123">Вы не сможете настроить внешний вид поля поиска.</span><span class="sxs-lookup"><span data-stu-id="c6a63-123">You won't be able to customize the appearance of the search box.</span></span>
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```
