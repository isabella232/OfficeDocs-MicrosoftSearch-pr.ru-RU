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
description: Добавляйте браузерные приложения в результаты для закладок в Поиске (Майкрософт)
ms.openlocfilehash: 96b409274e3fa06cef7dcc6f1c43360a3e6b9d34
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2019
ms.locfileid: "33968387"
---
# <a name="integrate-powerapps"></a><span data-ttu-id="a9490-103">Интеграция PowerApps</span><span class="sxs-lookup"><span data-stu-id="a9490-103">Integrate PowerApps</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9490-104">Параметры Поиска (Майкрософт) в Bing теперь доступны в Центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a9490-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="a9490-105">Начните с [назначения администраторов поиска](https://docs.microsoft.com/ru-RU/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) в Центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="a9490-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="a9490-106">Помогите пользователям выполнять задачи, например ввести время отпуска или сообщить о расходах, интегрировав существующую службу PowerApps в закладки.</span><span class="sxs-lookup"><span data-stu-id="a9490-106">Help your users complete tasks, such as entering vacation time or reporting expenses, by adding existing PowerApps to your bookmarks.</span></span> <span data-ttu-id="a9490-107">Интегрированная служба PowerApps отображается в результатах для закладок, не требуя перехода на другой сайт или открытия отдельного инструмента, что экономит время и усилия.</span><span class="sxs-lookup"><span data-stu-id="a9490-107">Integrated PowerApps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-powerapps"></a><span data-ttu-id="a9490-108">Что такое PowerApps?</span><span class="sxs-lookup"><span data-stu-id="a9490-108">What are PowerApps?</span></span>

<span data-ttu-id="a9490-109">PowerApps — это служба, которая позволяет создавать бизнес-приложения, работающие в браузере, на телефоне или планшете, при этом не требуется опыт кодирования.</span><span class="sxs-lookup"><span data-stu-id="a9490-109">PowerApps is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="a9490-110">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="a9490-110">Learn more:</span></span>
  
- <span data-ttu-id="a9490-111">
  [Интерактивное обучение](https://docs.microsoft.com/ru-RU/learn/browse/?products=powerapps)</span><span class="sxs-lookup"><span data-stu-id="a9490-111">[Guided Learning](https://docs.microsoft.com/en-us/learn/browse/?products=powerapps)</span></span>
    
- <span data-ttu-id="a9490-112">
  [Документация](https://docs.microsoft.com/ru-RU/powerapps/)</span><span class="sxs-lookup"><span data-stu-id="a9490-112">[Documentation](https://docs.microsoft.com/en-us/powerapps/)</span></span>
    
## <a name="add-a-powerapp-to-a-bookmark"></a><span data-ttu-id="a9490-113">Добавление PowerApp в закладку</span><span class="sxs-lookup"><span data-stu-id="a9490-113">Add a PowerApp to a bookmark</span></span>

<span data-ttu-id="a9490-114">Служба PowerApps работает в любом браузере и на любом устройстве, и ее добавление занимает меньше минуты.</span><span class="sxs-lookup"><span data-stu-id="a9490-114">PowerApps work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="a9490-115">
  [Найдите идентификатор приложения PowerApp](https://docs.microsoft.com/ru-RU/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id), которое нужно интегрировать</span><span class="sxs-lookup"><span data-stu-id="a9490-115">Find the [App ID for the PowerApp](https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) that you want to add.</span></span> 
    
2. <span data-ttu-id="a9490-116">На портале администрирования Поиска (Майкрософт) откройте вкладку **Закладки**</span><span class="sxs-lookup"><span data-stu-id="a9490-116">In the Microsoft SearchAdmin portal, go to **Bookmarks**</span></span>
    
3. <span data-ttu-id="a9490-117">Добавьте или найдите существующую закладку, в которую вы хотите добавить PowerApp</span><span class="sxs-lookup"><span data-stu-id="a9490-117">Add a bookmark or find an existing bookmark that you want to add a PowerApp to.</span></span>
    
4. <span data-ttu-id="a9490-118">В параметрах закладки выберите пункт **Приложение Power Apps** и щелкните **Добавить приложение Power Apps**</span><span class="sxs-lookup"><span data-stu-id="a9490-118">In Bookmark settings, select Power App, and then Add a Power App.</span></span>
    
5. <span data-ttu-id="a9490-119">Введите или вставьте идентификатор приложения</span><span class="sxs-lookup"><span data-stu-id="a9490-119">Enter or paste the App ID.</span></span>
    
    <span data-ttu-id="a9490-120">Высота и ширина добавляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="a9490-120">The height and width are automatically adjusted.</span></span> <span data-ttu-id="a9490-121">Закладки могут поддерживать альбомную и книжную ориентацию, но в настоящее время нельзя изменить размер.</span><span class="sxs-lookup"><span data-stu-id="a9490-121">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="a9490-122">В области предварительного просмотра закладки показано, как PowerApp будет отображаться в результатах для закладок</span><span class="sxs-lookup"><span data-stu-id="a9490-122">The bookmark preview shows how the PowerApp will appear in the bookmark result</span></span>
    
    <span data-ttu-id="a9490-123">Служба PowerApp в области предварительного просмотра поддерживает все функции, чтобы упростить ее тестирование и использование.</span><span class="sxs-lookup"><span data-stu-id="a9490-123">The PowerApp in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="a9490-124">Нажмите кнопку **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="a9490-124">Click **Publish**.</span></span>
    
<span data-ttu-id="a9490-125">Когда авторизованный пользователь Поиска (Майкрософт) выполняет в Bing поиск любого из ключевых или зарезервированных слов закладки, приложение PowerApp будет отображаться в результатах для закладок.</span><span class="sxs-lookup"><span data-stu-id="a9490-125">When an authorized Microsoft Search user searches on Bing for any of the bookmark's keywords or reserved keywords, the PowerApp will appear in the bookmark result.</span></span>

  

