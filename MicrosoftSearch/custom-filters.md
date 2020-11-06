---
title: Управление настраиваемыми фильтрами
ms.author: rodhb
author: rodhb
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Управление настраиваемыми фильтрами
ms.openlocfilehash: 75273035a7825683f626464df7bbc8e294b41b6f
ms.sourcegitcommit: 59435698bece013ae64ca2a68c43455ca10e3fdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "48927389"
---
# <a name="create-custom-filters"></a><span data-ttu-id="2cee1-103">Создание настраиваемых фильтров</span><span class="sxs-lookup"><span data-stu-id="2cee1-103">Create custom Filters</span></span>

<span data-ttu-id="2cee1-104">Вы можете создать фильтры, чтобы настроить поисковый интерфейс, который пользователи видят при поиске в Microsoft [SharePoint](https://sharepoint.com/), Microsoft [Office](https://office.com)и Microsoft Search в [Bing](https://bing.com).</span><span class="sxs-lookup"><span data-stu-id="2cee1-104">You can create filters to customize the search experience that users see when they search in Microsoft [SharePoint](https://sharepoint.com/), Microsoft [Office](https://office.com), and Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="2cee1-105">Фильтры позволяют пользователям быстро уточнять набор результатов из запроса поиска.</span><span class="sxs-lookup"><span data-stu-id="2cee1-105">Filters lets users quickly refine the set of results from their search query.</span></span>

<span data-ttu-id="2cee1-106">Настраиваемый фильтр можно создать в вертикальном направлении на основе свойства Connection.</span><span class="sxs-lookup"><span data-stu-id="2cee1-106">A custom filter can be created inside a vertical based on a connection property.</span></span> <span data-ttu-id="2cee1-107">Например, вы можете создать **опубликованный** фильтр для подключения ServiceNow в настраиваемом вертикальном расположении.</span><span class="sxs-lookup"><span data-stu-id="2cee1-107">For example, you can create a **Published On** filter for ServiceNow connection inside a custom vertical.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="2cee1-108">Важные факторы</span><span class="sxs-lookup"><span data-stu-id="2cee1-108">Things to consider</span></span>

1. <span data-ttu-id="2cee1-109">Для создания настраиваемого фильтра для источника контента подключения предоставляются некоторые дополнительные возможности:</span><span class="sxs-lookup"><span data-stu-id="2cee1-109">For creating custom filter on connection content source, some additional capabilities are provided:</span></span>
- <span data-ttu-id="2cee1-110">Вы также можете создать фильтр для свойств источника для соединителя.</span><span class="sxs-lookup"><span data-stu-id="2cee1-110">You can also create filter on an alias to connector source properties</span></span>
- <span data-ttu-id="2cee1-111">Если вертикальная линия имеет несколько подключений, вы можете создать общий фильтр для этих подключений.</span><span class="sxs-lookup"><span data-stu-id="2cee1-111">In case your vertical has multiple connections then you can create a common filter across these connections.</span></span> <span data-ttu-id="2cee1-112">Это можно сделать, создав фильтр на общем псевдониме, который будет псевдонимом свойств источника для разных подключений.</span><span class="sxs-lookup"><span data-stu-id="2cee1-112">This can be done by creating the filter on an common alias which aliases source properties across across different connections.</span></span> <span data-ttu-id="2cee1-113">Например, вы можете создать фильтр **авторов** в ServiceNow & подключения жира, создав псевдонимы следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2cee1-113">For example you can create an **Author** filter across a ServiceNow & a Jira connection by creating aliases as follows:</span></span>

| <span data-ttu-id="2cee1-114">Connection</span><span class="sxs-lookup"><span data-stu-id="2cee1-114">Connection</span></span> | <span data-ttu-id="2cee1-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="2cee1-115">Property</span></span> | <span data-ttu-id="2cee1-116">Alias</span><span class="sxs-lookup"><span data-stu-id="2cee1-116">Alias</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2cee1-117">Служба сейчас</span><span class="sxs-lookup"><span data-stu-id="2cee1-117">Service Now</span></span> | <span data-ttu-id="2cee1-118">Владелец</span><span class="sxs-lookup"><span data-stu-id="2cee1-118">Owner</span></span> | <span data-ttu-id="2cee1-119">Автор</span><span class="sxs-lookup"><span data-stu-id="2cee1-119">Author</span></span> |
| <span data-ttu-id="2cee1-120">жира</span><span class="sxs-lookup"><span data-stu-id="2cee1-120">Jira</span></span> | <span data-ttu-id="2cee1-121">Publisher</span><span class="sxs-lookup"><span data-stu-id="2cee1-121">Publisher</span></span> | <span data-ttu-id="2cee1-122">Автор</span><span class="sxs-lookup"><span data-stu-id="2cee1-122">Author</span></span> |

2. <span data-ttu-id="2cee1-123">Существуют фильтры в пределах области действия по вертикали.</span><span class="sxs-lookup"><span data-stu-id="2cee1-123">Filters exist within the scope of the vertical.</span></span> <span data-ttu-id="2cee1-124">Силу</span><span class="sxs-lookup"><span data-stu-id="2cee1-124">Hence,</span></span>  
- <span data-ttu-id="2cee1-125">Если фильтр создается вертикально на уровне Организации, то фильтр будет виден только на уровне Организации.</span><span class="sxs-lookup"><span data-stu-id="2cee1-125">If a filter is created in a vertical which is at organizational level, then the filter would only be visible at the organizational level</span></span>
- <span data-ttu-id="2cee1-126">Если фильтр создается по вертикали на уровне сайта, то фильтр будет виден только на уровне сайта.</span><span class="sxs-lookup"><span data-stu-id="2cee1-126">If a filter is created in a vertical which is at site level, then the filter would only be visible at the site level.</span></span>

## <a name="steps-to-create-custom-filter"></a><span data-ttu-id="2cee1-127">Действия для создания настраиваемого фильтра</span><span class="sxs-lookup"><span data-stu-id="2cee1-127">Steps to Create custom filter</span></span>

### <a name="create-filter-in-organizational-level-vertical"></a><span data-ttu-id="2cee1-128">Создать фильтр на вертикальном уровне Организации:</span><span class="sxs-lookup"><span data-stu-id="2cee1-128">Create filter in organizational level vertical:</span></span>

<span data-ttu-id="2cee1-129">Чтобы создать фильтр для поиска Microsoft Search, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2cee1-129">To create a filter on Microsoft search follow these steps:</span></span>

1. <span data-ttu-id="2cee1-130">В центре администрирования Microsoft 365 откройте страницу [вертикальные черты](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals) .</span><span class="sxs-lookup"><span data-stu-id="2cee1-130">In the Microsoft 365 admin center, go to the [Verticals](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals) page.</span></span>
2. <span data-ttu-id="2cee1-131">Создайте или измените вертикальный фильтр, на котором нужно создать фильтр.</span><span class="sxs-lookup"><span data-stu-id="2cee1-131">Create/Edit the vertical in which you want to create the filter</span></span>
3. <span data-ttu-id="2cee1-132">Перейдите к шагу "фильтры" мастера.</span><span class="sxs-lookup"><span data-stu-id="2cee1-132">Navigate to the 'Filters' step in the wizard</span></span>
4. <span data-ttu-id="2cee1-133">Нажмите кнопку "добавить фильтр" и приступайте к работе после добавления фильтров вы можете просмотреть и сохранить вертикальную.</span><span class="sxs-lookup"><span data-stu-id="2cee1-133">Click on 'Add Filter' and get started After adding filters, you can review and save the vertical.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="2cee1-134">Известные ограничения</span><span class="sxs-lookup"><span data-stu-id="2cee1-134">Known Limitations</span></span>

1. <span data-ttu-id="2cee1-135">В настоящее время фильтры можно создавать только для строкового & тип данных управляемых свойств.</span><span class="sxs-lookup"><span data-stu-id="2cee1-135">You can currently create filters only on String & Date type managed properties.</span></span>
2. <span data-ttu-id="2cee1-136">Невозможно создать иерархические фильтры</span><span class="sxs-lookup"><span data-stu-id="2cee1-136">You cannot create hierarchical filters</span></span>

## <a name="resources"></a><span data-ttu-id="2cee1-137">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="2cee1-137">Resources</span></span>

[<span data-ttu-id="2cee1-138">Настройка страницы результатов поиска</span><span class="sxs-lookup"><span data-stu-id="2cee1-138">Customize search result page</span></span>](customize-search-page.md)