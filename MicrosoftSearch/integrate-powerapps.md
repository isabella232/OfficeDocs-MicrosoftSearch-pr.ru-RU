---
title: Интеграция PowerApps
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/18/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 1fadcba3-4a7f-4a55-8476-d4e64d49a15f
ROBOTS: NOINDEX
description: Добавляйте браузерные приложения в результаты для закладок в Поиске (Майкрософт)
ms.openlocfilehash: d818ab8149032b4664adb90098700d4432a6fbb7
ms.sourcegitcommit: a7ca4c38d37fbdec58e002e42d865188939d0483
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2019
ms.locfileid: "35003122"
---
# <a name="integrate-powerapps"></a><span data-ttu-id="14175-103">Интеграция PowerApps</span><span class="sxs-lookup"><span data-stu-id="14175-103">Integrate PowerApps</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14175-104">Эта статья относится к Поиску (Майкрософт) на портале администрирования Bing.</span><span class="sxs-lookup"><span data-stu-id="14175-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="14175-105">Мы переносим портал в Центр администрирования Microsoft 365 с последующим его удалением.</span><span class="sxs-lookup"><span data-stu-id="14175-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="14175-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="14175-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="14175-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="14175-107">[Overview of Microsoft Search](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="14175-108">Помогите пользователям выполнять задачи, например ввести время отпуска или сообщить о расходах, интегрировав существующую службу PowerApps в закладки.</span><span class="sxs-lookup"><span data-stu-id="14175-108">Help your users complete tasks, such as entering vacation time or reporting expenses, by adding existing PowerApps to your bookmarks.</span></span> <span data-ttu-id="14175-109">Интегрированная служба PowerApps отображается в результатах для закладок, не требуя перехода на другой сайт или открытия отдельного инструмента, что экономит время и усилия.</span><span class="sxs-lookup"><span data-stu-id="14175-109">Integrated PowerApps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-powerapps"></a><span data-ttu-id="14175-110">Что такое PowerApps?</span><span class="sxs-lookup"><span data-stu-id="14175-110">What are PowerApps?</span></span>

<span data-ttu-id="14175-111">PowerApps — это служба, которая позволяет создавать бизнес-приложения, работающие в браузере, на телефоне или планшете, при этом не требуется опыт кодирования.</span><span class="sxs-lookup"><span data-stu-id="14175-111">PowerApps is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="14175-112">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="14175-112">Learn more:</span></span>
  
- <span data-ttu-id="14175-113">
  [Интерактивное обучение](https://docs.microsoft.com/ru-RU/learn/browse/?products=powerapps)</span><span class="sxs-lookup"><span data-stu-id="14175-113">[Guided Learning](https://docs.microsoft.com/en-us/learn/browse/?products=powerapps)</span></span>
    
- <span data-ttu-id="14175-114">
  [Документация](https://docs.microsoft.com/ru-RU/powerapps/)</span><span class="sxs-lookup"><span data-stu-id="14175-114">[Documentation](https://docs.microsoft.com/en-us/powerapps/)</span></span>
    
## <a name="add-a-powerapp-to-a-bookmark"></a><span data-ttu-id="14175-115">Добавление PowerApp в закладку</span><span class="sxs-lookup"><span data-stu-id="14175-115">Add a PowerApp to a bookmark</span></span>

<span data-ttu-id="14175-116">Служба PowerApps работает в любом браузере и на любом устройстве, и ее добавление занимает меньше минуты.</span><span class="sxs-lookup"><span data-stu-id="14175-116">PowerApps work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="14175-117">
  [Найдите идентификатор приложения PowerApp](https://docs.microsoft.com/ru-RU/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id), которое нужно интегрировать.</span><span class="sxs-lookup"><span data-stu-id="14175-117">Find the [App ID for the PowerApp](https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) that you want to add.</span></span> 
    
2. <span data-ttu-id="14175-118">На портале администрирования Поиска (Майкрософт) откройте вкладку **Закладки**.</span><span class="sxs-lookup"><span data-stu-id="14175-118">In the Microsoft Search Admin portal, go to **Bookmarks**</span></span>
    
3. <span data-ttu-id="14175-119">Добавьте или найдите существующую закладку, в которую вы хотите добавить PowerApp.</span><span class="sxs-lookup"><span data-stu-id="14175-119">Add a bookmark or find an existing bookmark that you want to add a PowerApp to.</span></span>
    
4. <span data-ttu-id="14175-120">В параметрах закладки выберите пункт **Приложение Power Apps** и щелкните **Добавить приложение Power Apps**</span><span class="sxs-lookup"><span data-stu-id="14175-120">In Bookmark settings, select Power App, and then Add a Power App.</span></span>
    
5. <span data-ttu-id="14175-121">Введите или вставьте идентификатор приложения</span><span class="sxs-lookup"><span data-stu-id="14175-121">Enter or paste the App ID.</span></span>
    
    <span data-ttu-id="14175-122">Высота и ширина добавляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="14175-122">The height and width are automatically adjusted.</span></span> <span data-ttu-id="14175-123">Закладки могут поддерживать альбомную и книжную ориентацию, но в настоящее время нельзя изменить размер.</span><span class="sxs-lookup"><span data-stu-id="14175-123">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="14175-124">В области предварительного просмотра закладки показано, как PowerApp будет отображаться в результатах для закладок</span><span class="sxs-lookup"><span data-stu-id="14175-124">The bookmark preview shows how the PowerApp will appear in the bookmark result</span></span>
    
    <span data-ttu-id="14175-125">Служба PowerApp в области предварительного просмотра поддерживает все функции, чтобы упростить ее тестирование и использование.</span><span class="sxs-lookup"><span data-stu-id="14175-125">The PowerApp in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="14175-126">Нажмите кнопку **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="14175-126">Click **Publish**.</span></span>
    
<span data-ttu-id="14175-127">Когда авторизованный пользователь Поиска (Майкрософт) выполняет в Bing поиск любого из ключевых или зарезервированных слов закладки, приложение PowerApp будет отображаться в результатах для закладок.</span><span class="sxs-lookup"><span data-stu-id="14175-127">When an authorized Microsoft Search user searches on Bing for any of the bookmark's keywords or reserved keywords, the PowerApp will appear in the bookmark result.</span></span>
