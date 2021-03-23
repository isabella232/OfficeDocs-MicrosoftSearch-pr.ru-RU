---
title: Интеграция power Apps
ms.author: dawholl
author: dawholl
manager: kellis
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 1fadcba3-4a7f-4a55-8476-d4e64d49a15f
description: Включаем приложения на основе браузера в результаты закладки для поиска в Microsoft Search
ms.openlocfilehash: 52fa78c54ab6db74ef1e3679d3d32151a3f5ac10
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031704"
---
# <a name="integrate-power-apps-in-microsoft-search-bookmarks"></a><span data-ttu-id="7fde6-103">Интеграция power Apps в закладки поиска Майкрософт</span><span class="sxs-lookup"><span data-stu-id="7fde6-103">Integrate Power Apps in Microsoft Search bookmarks</span></span>
   
<span data-ttu-id="7fde6-104">Помогите пользователям выполнять задачи, например вводить время отпуска или расходы на отчеты, интегрируя существующие [приложения Microsoft Power Apps](https://products.office.com/business/microsoft-powerapps) в закладки Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="7fde6-104">Help your users complete tasks, like entering vacation time or reporting expenses, by integrating existing [Microsoft Power Apps](https://products.office.com/business/microsoft-powerapps) into your Microsoft Search bookmarks.</span></span> <span data-ttu-id="7fde6-105">Интегрированные power Apps отображаются в результате закладки, устраняя необходимость перейти на другой сайт или открыть отдельный инструмент, который экономит время и усилия.</span><span class="sxs-lookup"><span data-stu-id="7fde6-105">Integrated Power Apps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-power-apps"></a><span data-ttu-id="7fde6-106">Что такое Power Apps?</span><span class="sxs-lookup"><span data-stu-id="7fde6-106">What are Power Apps?</span></span>

<span data-ttu-id="7fde6-107">[Power Apps](https://products.office.com/business/microsoft-powerapps) — это служба, которая позволяет создавать бизнес-приложения, которые работают в браузере или на телефоне или планшете без необходимости кодирования.</span><span class="sxs-lookup"><span data-stu-id="7fde6-107">[Power Apps](https://products.office.com/business/microsoft-powerapps) is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="7fde6-108">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="7fde6-108">Learn more:</span></span>
  
- [<span data-ttu-id="7fde6-109">Интерактивное обучение</span><span class="sxs-lookup"><span data-stu-id="7fde6-109">Guided Learning</span></span>](/learn/browse/?products=powerapps)
    
- [<span data-ttu-id="7fde6-110">Документация</span><span class="sxs-lookup"><span data-stu-id="7fde6-110">Documentation</span></span>](/powerapps/)
    
## <a name="add-a-power-app-to-a-bookmark"></a><span data-ttu-id="7fde6-111">Добавление power App в закладку</span><span class="sxs-lookup"><span data-stu-id="7fde6-111">Add a Power App to a bookmark</span></span>

<span data-ttu-id="7fde6-112">[Power Apps( работа в любом браузере и на любом устройстве и https://products.office.com/business/microsoft-powerapps) займет меньше минуты, чтобы добавить.</span><span class="sxs-lookup"><span data-stu-id="7fde6-112">[Power Apps(https://products.office.com/business/microsoft-powerapps) work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="7fde6-113">[Найдите ID приложения для приложения Power,](/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) которое необходимо интегрировать.</span><span class="sxs-lookup"><span data-stu-id="7fde6-113">[Find the App ID for the Power App](/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) you want to integrate.</span></span>
    
2. <span data-ttu-id="7fde6-114">В центре администрирования [](https://admin.microsoft.com)Microsoft 365 перейдите в **bookmarks**.</span><span class="sxs-lookup"><span data-stu-id="7fde6-114">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Bookmarks**.</span></span>
    
3. <span data-ttu-id="7fde6-115">Добавьте закладки или найдите существующую закладки, в которую необходимо добавить приложение Power.</span><span class="sxs-lookup"><span data-stu-id="7fde6-115">Add a bookmark or find an existing bookmark that you want to add a Power App to.</span></span>
    
4. <span data-ttu-id="7fde6-116">В параметрах закладок выберите **Power App** и выберите Добавить **power App**.</span><span class="sxs-lookup"><span data-stu-id="7fde6-116">In the bookmark settings, select **Power App**, and then select **Add a Power App**.</span></span>
    
5. <span data-ttu-id="7fde6-117">Введите или вставьте идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="7fde6-117">Enter or paste the App ID.</span></span>
    
    <span data-ttu-id="7fde6-118">Высота и ширина добавляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="7fde6-118">The height and width are automatically added.</span></span> <span data-ttu-id="7fde6-119">Закладки могут поддерживать альбомную и книжную ориентацию, но в настоящее время нельзя изменить размер.</span><span class="sxs-lookup"><span data-stu-id="7fde6-119">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="7fde6-120">Предварительный просмотр закладок показывает, как power App будет отображаться в результате закладки.</span><span class="sxs-lookup"><span data-stu-id="7fde6-120">The bookmark preview shows how the Power App will appear in the bookmark result.</span></span>
    
    <span data-ttu-id="7fde6-121">Приложение Power в предварительном просмотре полностью функционально, что позволяет легко тестировать и использовать.</span><span class="sxs-lookup"><span data-stu-id="7fde6-121">The Power App in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="7fde6-122">Нажмите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="7fde6-122">Select **Publish**.</span></span>
    
<span data-ttu-id="7fde6-123">Когда авторизованный пользователь Microsoft Search ищет [в Bing](https://Bing.com) ключевые слова или зарезервированные ключевые слова закладки, в результате закладки появится power App.</span><span class="sxs-lookup"><span data-stu-id="7fde6-123">When an authorized Microsoft Search user searches on [Bing](https://Bing.com) for any of the bookmark's keywords or reserved keywords, the Power App will appear in the bookmark result.</span></span>