---
title: Массовое создание вопросов и ответов
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
ms.assetid: 7bada218-8908-4956-aae3-6ffaeef384ca
ROBOTS: NoIndex
description: Быстрое добавление ответов на часто задаваемые вопросы с помощью средств импорта на портале администрирования Поиска (Майкрософт)
ms.openlocfilehash: 7368014f3bc2f21a788625f0bf826af963366e1b
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591371"
---
# <a name="bulk-create-qas"></a><span data-ttu-id="d13eb-103">Массовое создание вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="d13eb-103">Bulk create Q&As</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d13eb-104">Эта статья относится к Поиску (Майкрософт) на портале администрирования Bing.</span><span class="sxs-lookup"><span data-stu-id="d13eb-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="d13eb-105">Мы переносим портал в Центр администрирования Microsoft 365 с последующим его удалением.</span><span class="sxs-lookup"><span data-stu-id="d13eb-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="d13eb-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d13eb-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="d13eb-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="d13eb-107">[Overview of Microsoft Search](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="d13eb-108">Скачайте и используйте шаблон в CSV-формате для массового создания или изменения вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="d13eb-108">Download and use the .csv template to bulk create or bulk edit Q&As.</span></span> <span data-ttu-id="d13eb-109">Это также простой способ массового сохранения черновика вопросов и ответов, требующего дополнительных изменений или обновлений.</span><span class="sxs-lookup"><span data-stu-id="d13eb-109">It's also a simple way to bulk save draft Q&As that need additional edits or updates.</span></span> <span data-ttu-id="d13eb-110">Если нужно массово изменить существующие вопросы и ответы, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="d13eb-110">If you need to bulk edit existing Q&As, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="d13eb-111">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="d13eb-111">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
2. <span data-ttu-id="d13eb-112">Щелкните **Скачать шаблон вопросов и ответов (.csv)**</span><span class="sxs-lookup"><span data-stu-id="d13eb-112">Click **Download Q&A template (.csv)**</span></span>
    
3. <span data-ttu-id="d13eb-113">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="d13eb-113">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="d13eb-114">Добавьте содержимое и настройки вопросов и ответов, затем сохраните файл</span><span class="sxs-lookup"><span data-stu-id="d13eb-114">Add the Q&A content and settings and save the file</span></span>

    <span data-ttu-id="d13eb-115">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="d13eb-115">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="d13eb-116">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="d13eb-116">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
6. <span data-ttu-id="d13eb-117">В панели импорта вопросов и ответов нажмите кнопку **Обзор** и перейдите к CSV-файлу, который нужно импортировать</span><span class="sxs-lookup"><span data-stu-id="d13eb-117">In the Import locations pane, select **Browse**, and then the .csv file that you want to import.</span></span> 
    
7. <span data-ttu-id="d13eb-118">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="d13eb-118">Click **Import**.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="d13eb-119">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="d13eb-119">Prevent import errors</span></span>      
<span data-ttu-id="d13eb-120">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d13eb-120">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="d13eb-121">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="d13eb-121">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="d13eb-122">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="d13eb-122">Make necessary edits and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="d13eb-123">Пока не исправлены все ошибки, вы не сможете создать или изменить вопросы и ответы.</span><span class="sxs-lookup"><span data-stu-id="d13eb-123">Until all errors are resolved, you can't create or edit any Q&As.</span></span> 

<span data-ttu-id="d13eb-124">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="d13eb-124">To prevent errors, make sure your import file is properly formatted and:</span></span>
- <span data-ttu-id="d13eb-125">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="d13eb-125">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="d13eb-126">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="d13eb-126">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="d13eb-127">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="d13eb-127">The column order is the same as the import template</span></span>
- <span data-ttu-id="d13eb-128">эти столбцы могут быть пустыми: Id, Last Modified и Last Modified By;</span><span class="sxs-lookup"><span data-stu-id="d13eb-128">All columns have values, except the three that can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="d13eb-129">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="d13eb-129">The State column is not empty, as this information is required</span></span>  
<span data-ttu-id="d13eb-130">В зависимости от поля State вопросы и ответы сохраняются в черновике, списке предложенных или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="d13eb-130">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="d13eb-131">Кроме того, если добавить идентификатор существующего вопроса с ответом, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="d13eb-131">If you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="d13eb-132">Для организаций с несколькими клиентами можно экспортировать вопросы и ответы из одного клиента и импортировать их в другой.</span><span class="sxs-lookup"><span data-stu-id="d13eb-132">For organizations with multiple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="d13eb-133">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="d13eb-133">But you must remove the data in the Id column before you import.</span></span>

<span data-ttu-id="d13eb-134">Дополнительные сведения об обязательных и рекомендуемых полях см. в статье [Создание вопросов и ответов](create-qas.md).</span><span class="sxs-lookup"><span data-stu-id="d13eb-134">To find out more about required and recommended fields, see [Create Q&As](create-qas.md).</span></span>

  

