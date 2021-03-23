---
title: Настройка Поиска (Майкрософт)
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка Microsoft поиска в первый раз.
ms.openlocfilehash: 98499c2df1d8d732cdc1961116cafaaffeb4c5d6
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031668"
---
# <a name="set-up-microsoft-search"></a><span data-ttu-id="af634-103">Настройка Поиска (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="af634-103">Set up Microsoft Search</span></span>

<span data-ttu-id="af634-104">Microsoft Search предоставляет пользовательский интерфейс, который поможет пользователям находить сведения, такие как файлы и документы, внутренние сайты и бизнес-инструменты, людей и групп, расположения и направления, беседы и ответы.</span><span class="sxs-lookup"><span data-stu-id="af634-104">Microsoft Search provides a user-friendly interface to help users find information like files and documents, internal sites and business tools, people and groups, locations and directions, conversations and answers.</span></span> <span data-ttu-id="af634-105">Он обеспечивает безопасный доступ ко всем источникам данных, включая электронную почту, файлы, файлы SharePoint, контент OneDrive и другие общие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="af634-105">It does this by securely accessing all data sources, including emails, files, SharePoint files, OneDrive content, and other shared resources as well.</span></span> <span data-ttu-id="af634-106">С помощью Microsoft Search в Bing вы также можете получать результаты поиска из Интернета.</span><span class="sxs-lookup"><span data-stu-id="af634-106">With Microsoft Search in Bing you can get search results from the internet as well.</span></span>

<span data-ttu-id="af634-107">Дополнительные сведения о возможностях Поиска (Майкрософт) см.в статье [Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="af634-107">To learn more about Microsoft Search features, see [Microsoft Search Overview](overview-microsoft-search.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="af634-108">Начало работы</span><span class="sxs-lookup"><span data-stu-id="af634-108">Get Started</span></span>

<span data-ttu-id="af634-109">Поиск (Майкрософт) включен по умолчанию для всех приложений Майкрософт, поддерживающих его, в составе Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="af634-109">Microsoft Search is turned on by default for all Microsoft apps that supports it, as a part of Microsoft 365.</span></span> <span data-ttu-id="af634-110">Настройка не требуется, но вы можете улучшить общий опыт поиска в Microsoft с помощью некоторых основных административных задач.</span><span class="sxs-lookup"><span data-stu-id="af634-110">There is no setup required, but you can improve the overall Microsoft Search experience through some basic administrative tasks.</span></span>

<span data-ttu-id="af634-111">Управление Поиском (Майкрософт) выполняется из Центра администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="af634-111">You manage Microsoft Search from Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="af634-112">В центре администрирования Microsoft 365 перейдите в **службу поиска**  >  [**& параметры.**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)</span><span class="sxs-lookup"><span data-stu-id="af634-112">In Microsoft 365 admin center, go to **Settings** > [**Search & intelligence**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span>

<span data-ttu-id="af634-113">Администратору следует учитывать некоторые моменты, обеспечивающие эффективность и удобство Поиска (Майкрософт) в организации.</span><span class="sxs-lookup"><span data-stu-id="af634-113">As an admin you should consider a few things that can make the Microsoft Search experience efficient and user friendly in your organization.</span></span>

## <a name="step-1-assign-search-admin-and-search-editor"></a><span data-ttu-id="af634-114">Шаг 1. Назначение администратора поиска и редактора поиска</span><span class="sxs-lookup"><span data-stu-id="af634-114">Step 1: Assign Search admin and Search editor</span></span>

<span data-ttu-id="af634-115">В Поиске (Майкрософт) можно управлять контентом и параметрами поиска организации, назначая пользователям следующие роли:</span><span class="sxs-lookup"><span data-stu-id="af634-115">In Microsoft Search, you can manage your organization’s search settings and content by assigning these roles to users:</span></span>

1. <span data-ttu-id="af634-116">**Администратор Поиска.** Эта роль может создавать и контролировать содержимое результатов поиска, а также определять параметры запросов для улучшенных результатов поиска в организации.</span><span class="sxs-lookup"><span data-stu-id="af634-116">**Search admin:** This role can create and manage search result content and define query settings for improved search results within the organization.</span></span> <span data-ttu-id="af634-117">Администратор Поиска управляет конфигурацией Поиска (Майкрософт) и может выполнять все те же задачи по управлению контентом, что и редактор Поиска.</span><span class="sxs-lookup"><span data-stu-id="af634-117">Search admin manages the Microsoft Search configuration and can perform all of the content-management tasks a Search editor can.</span></span>
2. <span data-ttu-id="af634-118">**Редактор Поиска.** Создает, контролирует и удаляет контент для Поиска (Майкрософт) в Центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="af634-118">**Search editor:** Creates, manages, and deletes content for Microsoft Search in the Microsoft 365 admin center.</span></span> <span data-ttu-id="af634-119">Эта роль может создавать и контролировать редакторский контент, например вопросы и ответы, важные места и расположения, а также популярные сайты и приложения.</span><span class="sxs-lookup"><span data-stu-id="af634-119">This role can create and manage editorial content, such as frequently asked questions and answers, important places and locations, frequently searched and used sites and apps.</span></span>

<span data-ttu-id="af634-120">В настоящее время роли "Администратор Поиска" и "Редактор Поиска" должен назначать глобальный администратор. Дополнительные сведения см. в статье [Назначение ролей администратора](/office365/admin/add-users/assign-admin-roles?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="af634-120">Currently, the Search admin and Search editor roles must be assigned by a global admin. For more information, see [Assign admin roles](/office365/admin/add-users/assign-admin-roles?view=o365-worldwide).</span></span>

<span data-ttu-id="af634-121">Администраторы поиска непосредственно влияют на возможности поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="af634-121">Search administrators directly influence the search experience for end users.</span></span> <span data-ttu-id="af634-122">Сюда относится выбор типов результатов, которые должны отображаться для пользователей.</span><span class="sxs-lookup"><span data-stu-id="af634-122">This includes choosing the types of results you want to surface to your users.</span></span> <span data-ttu-id="af634-123">Одному человеку может быть сложно выбрать и создать достоверное содержимое по множеству разных тем, которые пользователи ищут в организации.</span><span class="sxs-lookup"><span data-stu-id="af634-123">It may be difficult for one person to choose and create authoritative content on many different topics that users search for in an organization.</span></span> <span data-ttu-id="af634-124">Рекомендуем использовать опыт и знания профильных специалистов, а также других пользователей, добавляя их в качестве редакторов Поиска.</span><span class="sxs-lookup"><span data-stu-id="af634-124">We recommend that you leverage the expertise and knowledge of subject matter experts (SME) and other users by adding them as Search editors.</span></span>

## <a name="step-2-create-answers"></a><span data-ttu-id="af634-125">Шаг 2. Создание ответов</span><span class="sxs-lookup"><span data-stu-id="af634-125">Step 2: Create answers</span></span>

<span data-ttu-id="af634-126">Поиск (Майкрософт) предоставляет администраторам средства, которые можно использовать при создании функционального интерфейса поиска для пользователей.</span><span class="sxs-lookup"><span data-stu-id="af634-126">Microsoft Search provides administrators with tools that they can use to build a robust search experience for their users.</span></span> <span data-ttu-id="af634-127">В Microsoft Search администраторы имеют три различных содержимого поиска, которые они могут создать для улучшения поиска и улучшения "найдите" контента:</span><span class="sxs-lookup"><span data-stu-id="af634-127">In Microsoft Search, administrators have three different search contents that they can create for a better search experience and to improve the "findability" of content:</span></span>

<span data-ttu-id="af634-128">Закладки являются наиболее часто используемым типом ответа.</span><span class="sxs-lookup"><span data-stu-id="af634-128">Bookmarks are the most commonly used answer type.</span></span> <span data-ttu-id="af634-129">Они продвигают наилучшие результаты для запросов пользователей в верхней части результатов поиска и упрощют пользователям поиск того, что они ищут.</span><span class="sxs-lookup"><span data-stu-id="af634-129">They promote the best possible results for your users’ queries to the top of the search results and make it easy for your users to find what they are looking for.</span></span>
<span data-ttu-id="af634-130">Информационное содержимое, доступное для всех; например, сведения о компании, справки для приложений Windows и Office и т. д. Контент, который люди в организации обычно ищут в своей ежедневной работе.</span><span class="sxs-lookup"><span data-stu-id="af634-130">Informational content that is available for everyone; for example, information about the company, help for Windows and Office apps, etc. Content that people in the organization generally search for in their day-to-day work.</span></span> <span data-ttu-id="af634-131">К обычным поисковым запросам, связанным с работой, относятся льготы сотрудников, отчеты о времени и расходах, отправка заказов на покупку и обращение за помощью к ИТ-службам.</span><span class="sxs-lookup"><span data-stu-id="af634-131">Common work-related searches include employee benefits, time and expense reporting, submitting purchase orders, and getting help from IT services.</span></span>

<span data-ttu-id="af634-132">Для создания и управления ответами см. [в перенаправляемом контенте.](plan-your-content.md)</span><span class="sxs-lookup"><span data-stu-id="af634-132">For creating and managing answers, see [Plan your content](plan-your-content.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="af634-133">Следующие шаги</span><span class="sxs-lookup"><span data-stu-id="af634-133">Next steps</span></span>

<span data-ttu-id="af634-134">Если вы хотите узнать больше о том, как пользователи будут использовать Microsoft Search, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="af634-134">If you'd like to learn more about how your users will use Microsoft Search, see the following articles:</span></span>

- [<span data-ttu-id="af634-135">Находите нужные элементы с помощью Поиска (Майкрософт) в Office</span><span class="sxs-lookup"><span data-stu-id="af634-135">Find what you need with Microsoft Search in Office</span></span>](https://support.office.com/article/find-what-you-need-with-microsoft-search-in-office-2457d4d8-48a8-4ad4-ab89-5a0657aa8446)
- [<span data-ttu-id="af634-136">Обучение работе с Office 365</span><span class="sxs-lookup"><span data-stu-id="af634-136">Office 365 Training Center</span></span>](https://support.office.com/office-training-center)
- [<span data-ttu-id="af634-137">Центр Поиска (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="af634-137">Microsoft Search Center</span></span>](https://support.office.com/article/-working-title-microsoft-search-center-b8bf5a2c-7515-40a9-9a6a-b8ed382c86bc)