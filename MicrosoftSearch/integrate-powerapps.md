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
description: Включение приложений на основе браузера в результаты закладок поиска Microsoft Search
ms.openlocfilehash: d8d9d099848e719c86e0f3cadee330263566d243
ms.sourcegitcommit: a5fd9d4f46bbb7c539630735ac16e0c786939e5d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2019
ms.locfileid: "33508828"
---
# <a name="integrate-powerapps"></a><span data-ttu-id="5a33e-103">Интеграция PowerApps</span><span class="sxs-lookup"><span data-stu-id="5a33e-103">Integrate PowerApps</span></span>

<span data-ttu-id="5a33e-104">Помогите пользователям выполнить задачи, например ввести время отпуска или отчеты об ошибках, интегрируя существующую PowerApps в закладки.</span><span class="sxs-lookup"><span data-stu-id="5a33e-104">Help your users complete tasks, such as entering vacation time or reporting expenses by integrating existing PowerApps into your bookmarks.</span></span> <span data-ttu-id="5a33e-105">Интегрированный PowerApps отображается в виде Закладка, что позволяет избежать необходимости переходить на другой сайт или открыть отдельное средство, которое экономит время и усилия.</span><span class="sxs-lookup"><span data-stu-id="5a33e-105">Integrated PowerApps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-powerapps"></a><span data-ttu-id="5a33e-106">Что такое PowerApps?</span><span class="sxs-lookup"><span data-stu-id="5a33e-106">What are PowerApps?</span></span>

<span data-ttu-id="5a33e-107">PowerApps — это служба, которая позволяет создавать бизнес-приложения, которые запускаются в браузере или на телефоне или планшете без необходимости программирования.</span><span class="sxs-lookup"><span data-stu-id="5a33e-107">PowerApps is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="5a33e-108">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="5a33e-108">Learn more:</span></span>
  
- [<span data-ttu-id="5a33e-109">Интерактивное обучение</span><span class="sxs-lookup"><span data-stu-id="5a33e-109">Guided Learning</span></span>](https://docs.microsoft.com/en-us/learn/browse/?products=powerapps)
    
- [<span data-ttu-id="5a33e-110">Документы</span><span class="sxs-lookup"><span data-stu-id="5a33e-110">Documentation</span></span>](https://docs.microsoft.com/en-us/powerapps/)
    
## <a name="add-a-powerapp-to-a-bookmark"></a><span data-ttu-id="5a33e-111">Добавление Поверапп к закладке</span><span class="sxs-lookup"><span data-stu-id="5a33e-111">Add a PowerApp to a bookmark</span></span>

<span data-ttu-id="5a33e-112">PowerApps работает в любом браузере и на любом устройстве и занимает меньше минуты, чтобы добавить.</span><span class="sxs-lookup"><span data-stu-id="5a33e-112">PowerApps work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="5a33e-113">[Найдите идентификатор приложения для поверапп](https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) , который необходимо интегрировать.</span><span class="sxs-lookup"><span data-stu-id="5a33e-113">[Find the App ID for the PowerApp](https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) you want to integrate</span></span> 
    
2. <span data-ttu-id="5a33e-114">На портале Microsoft Сеарчадмин перейдите к разделу **закладки** .</span><span class="sxs-lookup"><span data-stu-id="5a33e-114">In the Microsoft SearchAdmin portal, go to **Bookmarks**</span></span>
    
3. <span data-ttu-id="5a33e-115">Добавьте закладку или найдите существующую закладку, к которой требуется добавить Поверапп</span><span class="sxs-lookup"><span data-stu-id="5a33e-115">Add a bookmark or find an existing bookmark that you want to add a PowerApp to</span></span>
    
4. <span data-ttu-id="5a33e-116">В разделе Параметры закладок выберите пункт **Power App**, а затем щелкните **Добавить приложение Power** .</span><span class="sxs-lookup"><span data-stu-id="5a33e-116">In the bookmark settings, click **Power App**, and then click **Add a Power App**</span></span>
    
5. <span data-ttu-id="5a33e-117">Ввод или вставка идентификатора приложения</span><span class="sxs-lookup"><span data-stu-id="5a33e-117">Enter or paste the App ID</span></span>
    
    <span data-ttu-id="5a33e-118">Высота и ширина добавляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="5a33e-118">The height and width are automatically added.</span></span> <span data-ttu-id="5a33e-119">Закладки могут поддерживать как книжную, так и альбомную ориентацию, но в настоящее время их размер невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="5a33e-119">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="5a33e-120">В предварительном просмотре закладка показано, как будет выглядеть Поверапп в результатах закладка</span><span class="sxs-lookup"><span data-stu-id="5a33e-120">The bookmark preview shows how the PowerApp will appear in the bookmark result</span></span>
    
    <span data-ttu-id="5a33e-121">Поверапп в предварительной версии является полностью функциональным средством для упрощения тестирования и использования.</span><span class="sxs-lookup"><span data-stu-id="5a33e-121">The PowerApp in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="5a33e-122">Нажмите кнопку **опубликовать**</span><span class="sxs-lookup"><span data-stu-id="5a33e-122">Click **Publish**</span></span>
    
<span data-ttu-id="5a33e-123">Когда авторизованный пользователь поиска Microsoft выполняет поиск в Bing для любых ключевых слов закладки или зарезервированных ключевых слов, Поверапп будет отображаться в результатах закладка.</span><span class="sxs-lookup"><span data-stu-id="5a33e-123">When an authorized Microsoft Search user searches on Bing for any of the bookmark's keywords or reserved keywords, the PowerApp will appear in the bookmark result.</span></span>

  

