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
ms.openlocfilehash: f68b3c2b74f0a5c1712f0e86e86826e1f2c94b58
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639850"
---
# <a name="integrate-powerapps"></a><span data-ttu-id="af110-103">Интеграция PowerApps</span><span class="sxs-lookup"><span data-stu-id="af110-103">Integrate PowerApps</span></span>
   
<span data-ttu-id="af110-104">Помогите пользователям выполнять задачи, например ввести время отпуска или сообщить о расходах, интегрировав существующую службу PowerApps в закладки.</span><span class="sxs-lookup"><span data-stu-id="af110-104">Help your users complete tasks, such as entering vacation time or reporting expenses, by adding existing PowerApps to your bookmarks.</span></span> <span data-ttu-id="af110-105">Интегрированная служба PowerApps отображается в результатах для закладок, не требуя перехода на другой сайт или открытия отдельного инструмента, что экономит время и усилия.</span><span class="sxs-lookup"><span data-stu-id="af110-105">Integrated PowerApps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-powerapps"></a><span data-ttu-id="af110-106">Что такое PowerApps?</span><span class="sxs-lookup"><span data-stu-id="af110-106">What are PowerApps?</span></span>

<span data-ttu-id="af110-107">PowerApps — это служба, которая позволяет создавать бизнес-приложения, работающие в браузере, на телефоне или планшете, при этом не требуется опыт кодирования.</span><span class="sxs-lookup"><span data-stu-id="af110-107">PowerApps is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="af110-108">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="af110-108">Learn more:</span></span>
  
- [<span data-ttu-id="af110-109">Интерактивное обучение</span><span class="sxs-lookup"><span data-stu-id="af110-109">Guided Learning</span></span>](https://docs.microsoft.com/learn/browse/?products=powerapps)
    
- [<span data-ttu-id="af110-110">Документация</span><span class="sxs-lookup"><span data-stu-id="af110-110">Documentation</span></span>](https://docs.microsoft.com/powerapps/)
    
## <a name="add-a-powerapp-to-a-bookmark"></a><span data-ttu-id="af110-111">Добавление PowerApp в закладку</span><span class="sxs-lookup"><span data-stu-id="af110-111">Add a PowerApp to a bookmark</span></span>

<span data-ttu-id="af110-112">Служба PowerApps работает в любом браузере и на любом устройстве, и ее добавление занимает меньше минуты.</span><span class="sxs-lookup"><span data-stu-id="af110-112">PowerApps work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="af110-113">[Найдите идентификатор приложения PowerApp](https://docs.microsoft.com/ru-RU/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id), которое нужно интегрировать.</span><span class="sxs-lookup"><span data-stu-id="af110-113">Find the [App ID for the PowerApp](https://docs.microsoft.com/ru-RU/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) that you want to add.</span></span> 
    
2. <span data-ttu-id="af110-114">На портале администрирования Поиска (Майкрософт) откройте вкладку **Закладки**.</span><span class="sxs-lookup"><span data-stu-id="af110-114">In the Microsoft Search Admin portal, go to **Bookmarks**</span></span>
    
3. <span data-ttu-id="af110-115">Добавьте или найдите существующую закладку, в которую вы хотите добавить PowerApp.</span><span class="sxs-lookup"><span data-stu-id="af110-115">Add a bookmark or find an existing bookmark that you want to add a PowerApp to.</span></span>
    
4. <span data-ttu-id="af110-116">В параметрах закладки выберите пункт **Приложение Power Apps** и щелкните **Добавить приложение Power Apps**</span><span class="sxs-lookup"><span data-stu-id="af110-116">In Bookmark settings, select Power App, and then Add a Power App.</span></span>
    
5. <span data-ttu-id="af110-117">Введите или вставьте идентификатор приложения</span><span class="sxs-lookup"><span data-stu-id="af110-117">Enter or paste the App ID.</span></span>
    
    <span data-ttu-id="af110-118">Высота и ширина добавляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="af110-118">The height and width are automatically adjusted.</span></span> <span data-ttu-id="af110-119">Закладки могут поддерживать альбомную и книжную ориентацию, но в настоящее время нельзя изменить размер.</span><span class="sxs-lookup"><span data-stu-id="af110-119">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="af110-120">В области предварительного просмотра закладки показано, как PowerApp будет отображаться в результатах для закладок</span><span class="sxs-lookup"><span data-stu-id="af110-120">The bookmark preview shows how the PowerApp will appear in the bookmark result</span></span>
    
    <span data-ttu-id="af110-121">Служба PowerApp в области предварительного просмотра поддерживает все функции, чтобы упростить ее тестирование и использование.</span><span class="sxs-lookup"><span data-stu-id="af110-121">The PowerApp in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="af110-122">Нажмите кнопку **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="af110-122">Click **Publish**.</span></span>
    
<span data-ttu-id="af110-123">Когда авторизованный пользователь Поиска (Майкрософт) выполняет в Bing поиск любого из ключевых или зарезервированных слов закладки, приложение PowerApp будет отображаться в результатах для закладок.</span><span class="sxs-lookup"><span data-stu-id="af110-123">When an authorized Microsoft Search user searches on Bing for any of the bookmark's keywords or reserved keywords, the PowerApp will appear in the bookmark result.</span></span>
