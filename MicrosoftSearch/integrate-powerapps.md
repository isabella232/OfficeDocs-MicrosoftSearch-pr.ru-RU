---
title: Интеграция приложений Power
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
description: Включение приложений на основе браузера в результаты закладок поиска Microsoft Search
ms.openlocfilehash: 7d3dd21758c63da14bbd3896ece1ce67a19c80a2
ms.sourcegitcommit: f4cb37fdf85b895337caee827fb72b5b7fcaa8ad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2019
ms.locfileid: "39995026"
---
# <a name="integrate-power-apps-in-microsoft-search-bookmarks"></a><span data-ttu-id="115ad-103">Интеграция приложений Power в закладки поиска Microsoft</span><span class="sxs-lookup"><span data-stu-id="115ad-103">Integrate Power Apps in Microsoft Search bookmarks</span></span>
   
<span data-ttu-id="115ad-104">Помогите пользователям выполнить задачи, например ввести время отпуска или отчеты о расходах, интегрируя существующие [приложения Майкрософт Power Apps](https://products.office.com/business/microsoft-powerapps) в закладки поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="115ad-104">Help your users complete tasks, like entering vacation time or reporting expenses, by integrating existing [Microsoft Power Apps](https://products.office.com/business/microsoft-powerapps) into your Microsoft Search bookmarks.</span></span> <span data-ttu-id="115ad-105">Интегрированные приложения управления питанием отображаются в виде Закладка, что позволяет избежать необходимости переходить на другой сайт или открыть отдельное средство, которое экономит время и усилия.</span><span class="sxs-lookup"><span data-stu-id="115ad-105">Integrated Power Apps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-power-apps"></a><span data-ttu-id="115ad-106">Что такое приложения для работы с питанием?</span><span class="sxs-lookup"><span data-stu-id="115ad-106">What are Power Apps?</span></span>

<span data-ttu-id="115ad-107">[Power Apps](https://products.office.com/business/microsoft-powerapps) — это служба, позволяющая создавать бизнес-приложения, которые запускаются в браузере или на телефоне или планшете без необходимости программирования.</span><span class="sxs-lookup"><span data-stu-id="115ad-107">[Power Apps](https://products.office.com/business/microsoft-powerapps) is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="115ad-108">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="115ad-108">Learn more:</span></span>
  
- [<span data-ttu-id="115ad-109">Интерактивное обучение</span><span class="sxs-lookup"><span data-stu-id="115ad-109">Guided Learning</span></span>](https://docs.microsoft.com/learn/browse/?products=powerapps)
    
- [<span data-ttu-id="115ad-110">Документация</span><span class="sxs-lookup"><span data-stu-id="115ad-110">Documentation</span></span>](https://docs.microsoft.com/powerapps/)
    
## <a name="add-a-power-app-to-a-bookmark"></a><span data-ttu-id="115ad-111">Добавление приложения Power App в закладку</span><span class="sxs-lookup"><span data-stu-id="115ad-111">Add a Power App to a bookmark</span></span>

<span data-ttu-id="115ad-112">[Power Apps (https://products.office.com/business/microsoft-powerapps) работа в любом браузере и на любом устройстве и требует меньше минут, которые можно добавить.</span><span class="sxs-lookup"><span data-stu-id="115ad-112">[Power Apps(https://products.office.com/business/microsoft-powerapps) work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="115ad-113">[Найдите идентификатор приложения для приложения](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) , которое вы хотите интегрировать.</span><span class="sxs-lookup"><span data-stu-id="115ad-113">[Find the App ID for the Power App](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) you want to integrate.</span></span>
    
2. <span data-ttu-id="115ad-114">В [центре администрирования](https://admin.microsoft.com)Microsoft 365 перейдите к разделу **закладки**.</span><span class="sxs-lookup"><span data-stu-id="115ad-114">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Bookmarks**.</span></span>
    
3. <span data-ttu-id="115ad-115">Добавьте закладку или найдите существующую закладку, к которой требуется добавить приложение Power.</span><span class="sxs-lookup"><span data-stu-id="115ad-115">Add a bookmark or find an existing bookmark that you want to add a Power App to.</span></span>
    
4. <span data-ttu-id="115ad-116">В разделе Параметры закладок выберите **Power App**, а затем выберите **Добавить приложение Power**.</span><span class="sxs-lookup"><span data-stu-id="115ad-116">In the bookmark settings, select **Power App**, and then select **Add a Power App**.</span></span>
    
5. <span data-ttu-id="115ad-117">Введите или вставьте идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="115ad-117">Enter or paste the App ID.</span></span>
    
    <span data-ttu-id="115ad-118">Высота и ширина добавляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="115ad-118">The height and width are automatically added.</span></span> <span data-ttu-id="115ad-119">Закладки могут поддерживать альбомную и книжную ориентацию, но в настоящее время нельзя изменить размер.</span><span class="sxs-lookup"><span data-stu-id="115ad-119">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="115ad-120">В предварительном просмотре закладка показано, как приложение Power будет отображаться в результате закладка.</span><span class="sxs-lookup"><span data-stu-id="115ad-120">The bookmark preview shows how the Power App will appear in the bookmark result.</span></span>
    
    <span data-ttu-id="115ad-121">Приложение Power App в предварительной версии полностью работоспособно, чтобы облегчить тестирование и использование.</span><span class="sxs-lookup"><span data-stu-id="115ad-121">The Power App in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="115ad-122">Нажмите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="115ad-122">Select **Publish**.</span></span>
    
<span data-ttu-id="115ad-123">Когда авторизованный пользователь поиска Microsoft выполняет поиск в [Bing](https://Bing.com) для любых ключевых слов закладки или зарезервированных ключевых слов, приложение Power App будет отображаться в результатах закладка.</span><span class="sxs-lookup"><span data-stu-id="115ad-123">When an authorized Microsoft Search user searches on [Bing](https://Bing.com) for any of the bookmark's keywords or reserved keywords, the Power App will appear in the bookmark result.</span></span>
