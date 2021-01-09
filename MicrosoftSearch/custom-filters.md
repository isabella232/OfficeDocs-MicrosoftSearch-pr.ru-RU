---
title: Управление пользовательскими фильтрами
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
description: Управление пользовательскими фильтрами
ms.openlocfilehash: a050921058eac50d7588f1e71f5b0f56cc8e5752
ms.sourcegitcommit: a86265684871da86562a76c4961d0a6c1869f517
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/09/2021
ms.locfileid: "49790337"
---
# <a name="manage-custom-filters"></a><span data-ttu-id="202ef-103">Управление пользовательскими фильтрами</span><span class="sxs-lookup"><span data-stu-id="202ef-103">Manage custom filters</span></span>

<span data-ttu-id="202ef-104">Фильтры можно использовать для настройки поиска (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="202ef-104">You can use filters to customize the Microsoft Search experience.</span></span> <span data-ttu-id="202ef-105">Фильтры позволяет пользователям быстро уточнить набор результатов из поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="202ef-105">Filters let users quickly refine the set of results from their search query.</span></span>

<span data-ttu-id="202ef-106">Настраиваемый фильтр можно создать внутри вертикали на основе свойства подключения.</span><span class="sxs-lookup"><span data-stu-id="202ef-106">A custom filter can be created inside a vertical based on a connection property.</span></span> <span data-ttu-id="202ef-107">Например, можно создать фильтр **Published On** для подключения ServiceNow внутри вертикали.</span><span class="sxs-lookup"><span data-stu-id="202ef-107">For example, you can create a **Published On** filter for ServiceNow connection inside a vertical.</span></span>

## <a name="create-a-filter-in-an-organizational-level-vertical"></a><span data-ttu-id="202ef-108">Создание фильтра в вертикали организационного уровня</span><span class="sxs-lookup"><span data-stu-id="202ef-108">Create a filter in an organizational level vertical</span></span>

<span data-ttu-id="202ef-109">Чтобы создать фильтр поиска (Майкрософт), выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="202ef-109">To create a filter on Microsoft search follow these steps:</span></span>

1. <span data-ttu-id="202ef-110">В Центре администрирования Microsoft 365 перейдите в ["Вертикали".](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)</span><span class="sxs-lookup"><span data-stu-id="202ef-110">In the Microsoft 365 admin center, go to [Verticals](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
1. <span data-ttu-id="202ef-111">Создание и изменение вертикали, в которой нужно создать фильтр</span><span class="sxs-lookup"><span data-stu-id="202ef-111">Create/Edit the vertical in which you want to create the filter</span></span>
1. <span data-ttu-id="202ef-112">Перейдите к шагу "Фильтры" в мастере</span><span class="sxs-lookup"><span data-stu-id="202ef-112">Navigate to the 'Filters' step in the wizard</span></span>
1. <span data-ttu-id="202ef-113">Нажмите кнопку "Добавить фильтр" и йдите к работе</span><span class="sxs-lookup"><span data-stu-id="202ef-113">Click on 'Add Filter' and get started</span></span>
1. <span data-ttu-id="202ef-114">После добавления фильтров можно просмотреть и сохранить вертикаль.</span><span class="sxs-lookup"><span data-stu-id="202ef-114">After adding filters, you can review and save the vertical.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="202ef-115">Важные факторы</span><span class="sxs-lookup"><span data-stu-id="202ef-115">Things to consider</span></span>

1. <span data-ttu-id="202ef-116">Существуют дополнительные возможности фильтрации для содержимого подключений.</span><span class="sxs-lookup"><span data-stu-id="202ef-116">Additional filter capabilities exist on connection content.</span></span>

    - <span data-ttu-id="202ef-117">Можно также создать фильтр по псевдониму для свойств источника соединителей</span><span class="sxs-lookup"><span data-stu-id="202ef-117">You can also create filter on an alias to connector source properties</span></span>
    - <span data-ttu-id="202ef-118">Если у вертикали несколько подключений, можно создать общий фильтр для этих подключений.</span><span class="sxs-lookup"><span data-stu-id="202ef-118">If a vertical has multiple connections, you can create a common filter across these connections.</span></span> <span data-ttu-id="202ef-119">Это можно сделать, создав фильтр для общего псевдонима, который псевдонимует свойства источника в разных подключениях.</span><span class="sxs-lookup"><span data-stu-id="202ef-119">This can be done by creating the filter on an common alias which aliases source properties across across the different connections.</span></span> <span data-ttu-id="202ef-120">Например, вы можете создать фильтр **Author** в serviceNow и подмыве Jira, создав псевдонимы следующим образом:</span><span class="sxs-lookup"><span data-stu-id="202ef-120">For example you can create an **Author** filter across a ServiceNow and a Jira connection by creating aliases as follows:</span></span>

    | <span data-ttu-id="202ef-121">Connection</span><span class="sxs-lookup"><span data-stu-id="202ef-121">Connection</span></span> | <span data-ttu-id="202ef-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="202ef-122">Property</span></span> | <span data-ttu-id="202ef-123">Alias</span><span class="sxs-lookup"><span data-stu-id="202ef-123">Alias</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="202ef-124">Service Now</span><span class="sxs-lookup"><span data-stu-id="202ef-124">Service Now</span></span> | <span data-ttu-id="202ef-125">Владелец</span><span class="sxs-lookup"><span data-stu-id="202ef-125">Owner</span></span> | <span data-ttu-id="202ef-126">Автор</span><span class="sxs-lookup"><span data-stu-id="202ef-126">Author</span></span> |
    | <span data-ttu-id="202ef-127">Jira</span><span class="sxs-lookup"><span data-stu-id="202ef-127">Jira</span></span> | <span data-ttu-id="202ef-128">Publisher</span><span class="sxs-lookup"><span data-stu-id="202ef-128">Publisher</span></span> | <span data-ttu-id="202ef-129">Автор</span><span class="sxs-lookup"><span data-stu-id="202ef-129">Author</span></span> |

1. <span data-ttu-id="202ef-130">Фильтры существуют в области вертикали.</span><span class="sxs-lookup"><span data-stu-id="202ef-130">Filters exist within the scope of a vertical.</span></span>

    - <span data-ttu-id="202ef-131">Если фильтр создается в вертикали, которая находится на уровне организации, то фильтр будет виден только на уровне организации</span><span class="sxs-lookup"><span data-stu-id="202ef-131">If a filter is created in a vertical which is at organizational level, then the filter would only be visible at the organizational level</span></span>
    - <span data-ttu-id="202ef-132">Если фильтр создается в вертикали, которая находится на уровне сайта, то фильтр будет виден только на уровне сайта.</span><span class="sxs-lookup"><span data-stu-id="202ef-132">If a filter is created in a vertical which is at site level, then the filter would only be visible at the site level.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="202ef-133">Известные ограничения</span><span class="sxs-lookup"><span data-stu-id="202ef-133">Known Limitations</span></span>

1. <span data-ttu-id="202ef-134">В настоящее время фильтры можно создавать только & управляемых свойств типа даты.</span><span class="sxs-lookup"><span data-stu-id="202ef-134">You can currently create filters only on string & date type managed properties.</span></span>
1. <span data-ttu-id="202ef-135">Невозможно создать иерархические фильтры.</span><span class="sxs-lookup"><span data-stu-id="202ef-135">You cannot create hierarchical filters.</span></span>

## <a name="resources"></a><span data-ttu-id="202ef-136">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="202ef-136">Resources</span></span>

[<span data-ttu-id="202ef-137">Управление вертикалями и типами результатов</span><span class="sxs-lookup"><span data-stu-id="202ef-137">Manage verticals and result types</span></span>](customize-search-page.md)
