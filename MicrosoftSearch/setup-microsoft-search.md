---
title: Настройка Поиска (Майкрософт)
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка Microsoft поиска в первый раз.
ms.openlocfilehash: 94ee7ece8a56d599778b151d5b836240d8832762
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626912"
---
# <a name="set-up-microsoft-search"></a><span data-ttu-id="bb060-103">Настройка Поиска (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="bb060-103">Set up Microsoft Search</span></span>

<span data-ttu-id="bb060-104">Поиск (Майкрософт) предоставляет пользователям понятный интерфейс для поиска сведений, например файлов и документов, внутренних сайтов и бизнес-средств, людей и групп, расположений и маршрутов, бесед и ответов. Он использует безопасный доступ ко всем источникам данных в организации пользователя, включая сообщения электронной почты, файлы, файлы SharePoint, содержимое OneDrive и другие общие ресурсы, а также Интернет.</span><span class="sxs-lookup"><span data-stu-id="bb060-104">Microsoft Search provides a user-friendly interface to help users find information, like files and documents, internal sites and business tools, people and groups, locations and directions, conversations and answers by securely accessing all data sources, including emails, files, SharePoint files, OneDrive content, and other shared resources as well as the internet in the user’s organization.</span></span>

<span data-ttu-id="bb060-105">Дополнительные сведения о возможностях Поиска (Майкрософт) см.в статье [Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="bb060-105">To learn more about Microsoft Search features, see [Microsoft Search Overview](overview-microsoft-search.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="bb060-106">Начало работы</span><span class="sxs-lookup"><span data-stu-id="bb060-106">Get Started</span></span>

<span data-ttu-id="bb060-107">Поиск (Майкрософт) включен по умолчанию для всех приложений Майкрософт, поддерживающих его, в составе Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bb060-107">Microsoft Search is turned on by default for all Microsoft apps that supports it, as a part of Microsoft 365.</span></span> <span data-ttu-id="bb060-108">Настройка не требуется, но вы можете увеличить общие возможности поиска в Microsoft с помощью некоторых базовых задач администрирования.</span><span class="sxs-lookup"><span data-stu-id="bb060-108">There is no setup required,but you can improve the overall Microsoft Search experience through some basic administrative tasks.</span></span>

<span data-ttu-id="bb060-109">Управление Поиском (Майкрософт) выполняется из Центра администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bb060-109">You manage Microsoft Search from Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="bb060-110">В Центре администрирования Microsoft 365 откройте раздел **Параметры** > **Поиск (Майкрософт)**.</span><span class="sxs-lookup"><span data-stu-id="bb060-110">In Microsoft 365 admin center, go to **Settings** > **Microsoft Search**.</span></span>

<span data-ttu-id="bb060-111">**Примечание.** Если Поиск (Майкрософт) НЕ отображается в разделе **Параметры**, включите переключатель **Попробовать предварительную версию** в правом верхнем углу Центра администрирования.</span><span class="sxs-lookup"><span data-stu-id="bb060-111">**Note:** If you are NOT seeing Microsoft Search under **Settings**, turn on the **Try the preview** switch in the right top corner of any admin center page.</span></span>

<span data-ttu-id="bb060-112">Администратору следует учитывать некоторые моменты, обеспечивающие эффективность и удобство Поиска (Майкрософт) в организации.</span><span class="sxs-lookup"><span data-stu-id="bb060-112">As an admin you should consider a few things that can make the Microsoft Search experience efficient and user friendly in your organization.</span></span>

## <a name="step-1-assign-search-admin-and-search-editor"></a><span data-ttu-id="bb060-113">Шаг 1: назначение поискового администратора и редактора поиска</span><span class="sxs-lookup"><span data-stu-id="bb060-113">Step 1: Assign Search admin and Search editor</span></span>

<span data-ttu-id="bb060-114">В Поиске (Майкрософт) можно управлять контентом и параметрами поиска организации, назначая пользователям следующие роли:</span><span class="sxs-lookup"><span data-stu-id="bb060-114">In Microsoft Search, you can manage your organization’s search settings and content by assigning these roles to users:</span></span>

1. <span data-ttu-id="bb060-115">**Администратор Поиска.** Эта роль может создавать и контролировать содержимое результатов поиска, а также определять параметры запросов для улучшенных результатов поиска в организации.</span><span class="sxs-lookup"><span data-stu-id="bb060-115">**Search admin:** This role can create and manage search result content and define query settings for improved search results within the organization.</span></span> <span data-ttu-id="bb060-116">Администратор Поиска управляет конфигурацией Поиска (Майкрософт) и может выполнять все те же задачи по управлению контентом, что и редактор Поиска.</span><span class="sxs-lookup"><span data-stu-id="bb060-116">Search admin manages the Microsoft Search configuration and can perform all of the content-management tasks a Search editor can.</span></span>
2. <span data-ttu-id="bb060-117">**Редактор Поиска.** Создает, контролирует и удаляет контент для Поиска (Майкрософт) в Центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bb060-117">**Search editor:** Creates, manages, and deletes content for Microsoft Search in the Microsoft 365 admin center.</span></span> <span data-ttu-id="bb060-118">Эта роль может создавать и контролировать редакторский контент, например вопросы и ответы, важные места и расположения, а также популярные сайты и приложения.</span><span class="sxs-lookup"><span data-stu-id="bb060-118">This role can create and manage editorial content, such as frequently asked questions and answers, important places and locations, frequently searched and used sites and apps.</span></span>

<span data-ttu-id="bb060-119">В настоящее время роли "Администратор Поиска" и "Редактор Поиска" должен назначать глобальный администратор. Дополнительные сведения см. в статье [Назначение ролей администратора](https://docs.microsoft.com/office365/admin/add-users/assign-admin-roles?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="bb060-119">Currently, the Search admin and Search editor roles must be assigned by a global admin. For more information, see [Assign admin roles](https://docs.microsoft.com/office365/admin/add-users/assign-admin-roles?view=o365-worldwide).</span></span>

<span data-ttu-id="bb060-120">Администраторы поиска непосредственно влияют на возможности поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="bb060-120">Search administrators directly influence the search experience for end users.</span></span> <span data-ttu-id="bb060-121">Сюда относится выбор типов результатов, которые должны отображаться для пользователей.</span><span class="sxs-lookup"><span data-stu-id="bb060-121">This includes choosing the types of results you want to surface to your users.</span></span> <span data-ttu-id="bb060-122">Одному человеку может быть сложно выбрать и создать достоверное содержимое по множеству разных тем, которые пользователи ищут в организации.</span><span class="sxs-lookup"><span data-stu-id="bb060-122">It may be difficult for one person to choose and create authoritative content on many different topics that users search for in an organization.</span></span> <span data-ttu-id="bb060-123">Рекомендуем использовать опыт и знания профильных специалистов, а также других пользователей, добавляя их в качестве редакторов Поиска.</span><span class="sxs-lookup"><span data-stu-id="bb060-123">We recommend that you leverage the expertise and knowledge of subject matter experts (SME) and other users by adding them as Search editors.</span></span>

## <a name="step-2-create-answers"></a><span data-ttu-id="bb060-124">Шаг 2: создание ответов</span><span class="sxs-lookup"><span data-stu-id="bb060-124">Step 2: Create answers</span></span>

<span data-ttu-id="bb060-125">Поиск (Майкрософт) предоставляет администраторам средства, которые можно использовать при создании функционального интерфейса поиска для пользователей.</span><span class="sxs-lookup"><span data-stu-id="bb060-125">Microsoft Search provides administrators with tools that they can use to build a robust search experience for their users.</span></span> <span data-ttu-id="bb060-126">В Microsoft Search администраторы имеют три различных содержимого для поиска, которые могут быть созданы для улучшения качества поиска, а также для улучшения поиска контента:</span><span class="sxs-lookup"><span data-stu-id="bb060-126">In Microsoft Search, administrators have three different search contents that they can create for a better search experience and to improve the "findability" of content:</span></span>

<span data-ttu-id="bb060-127">Закладки — это наиболее часто используемый тип ответа.</span><span class="sxs-lookup"><span data-stu-id="bb060-127">Bookmarks are the most commonly used answer type.</span></span> <span data-ttu-id="bb060-128">Они позволяют пользователям быстро находить нужные результаты для запросов пользователей к началу результатов поиска и легко находить нужные результаты.</span><span class="sxs-lookup"><span data-stu-id="bb060-128">They promote the best possible results for your users’ queries to the top of the search results and make it easy for your users to find what they are looking for.</span></span>
<span data-ttu-id="bb060-129">Информационный контент, доступный всем пользователям; Например, сведения о компании, Справка по Windows и приложениям Office и т. д. Контент, который пользователи в организации обычно ищет в повседневной работе.</span><span class="sxs-lookup"><span data-stu-id="bb060-129">Informational content that is available for everyone; for example, information about the company, help for Windows and Office apps, etc. Content that people in the organization generally search for in their day-to-day work.</span></span> <span data-ttu-id="bb060-130">К обычным поисковым запросам, связанным с работой, относятся льготы сотрудников, отчеты о времени и расходах, отправка заказов на покупку и обращение за помощью к ИТ-службам.</span><span class="sxs-lookup"><span data-stu-id="bb060-130">Common work-related searches include employee benefits, time and expense reporting, submitting purchase orders, and getting help from IT services.</span></span>

<span data-ttu-id="bb060-131">Чтобы создавать ответы и управлять ими, ознакомьтесь со статьей [Планирование контента](plan-your-content.md).</span><span class="sxs-lookup"><span data-stu-id="bb060-131">For creating and managing answers, see [Plan your content](plan-your-content.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="bb060-132">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="bb060-132">Next steps</span></span>

<span data-ttu-id="bb060-133">Если вы хотите узнать больше о том, как пользователи будут использовать Microsoft Search, ознакомьтесь со следующими статьями:</span><span class="sxs-lookup"><span data-stu-id="bb060-133">If you'd like to learn more about how your users will use Microsoft Search, see the following articles:</span></span>

- [<span data-ttu-id="bb060-134">Находите нужные элементы с помощью Поиска (Майкрософт) в Office</span><span class="sxs-lookup"><span data-stu-id="bb060-134">Find what you need with Microsoft Search in Office</span></span>](https://support.office.com/article/find-what-you-need-with-microsoft-search-in-office-2457d4d8-48a8-4ad4-ab89-5a0657aa8446)
- [<span data-ttu-id="bb060-135">Обучение работе с Office 365</span><span class="sxs-lookup"><span data-stu-id="bb060-135">Office 365 Training Center</span></span>](https://support.office.com/office-training-center)
- [<span data-ttu-id="bb060-136">Центр Поиска (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="bb060-136">Microsoft Search Center</span></span>](https://support.office.com/article/-working-title-microsoft-search-center-b8bf5a2c-7515-40a9-9a6a-b8ed382c86bc)
