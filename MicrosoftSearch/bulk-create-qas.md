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
ms.openlocfilehash: 660f5663ff6238f4ab59dab36d51f1311d5c7260
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949035"
---
# <a name="bulk-create-qas"></a><span data-ttu-id="59e8a-103">Массовое создание вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="59e8a-103">Bulk create Q&As</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59e8a-104">Эта статья относится к порталу администрирования Поиска (Майкрософт) в Bing.</span><span class="sxs-lookup"><span data-stu-id="59e8a-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="59e8a-105">Мы переносим портал в Центр администрирования Microsoft 365, после чего портал Поиска (Майкрософт) в Bing будет удален.</span><span class="sxs-lookup"><span data-stu-id="59e8a-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="59e8a-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="59e8a-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="59e8a-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="59e8a-107">[Overview of Microsoft Search](overview-microsoft-search.md).</span></span>
    
<span data-ttu-id="59e8a-108">Скачайте и используйте шаблон в CSV-формате для массового создания или изменения вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="59e8a-108">Download and use the .csv template to bulk create or bulk edit Q&As.</span></span> <span data-ttu-id="59e8a-109">Это также простой способ массового сохранения черновика вопросов и ответов, требующего дополнительных изменений или обновлений.</span><span class="sxs-lookup"><span data-stu-id="59e8a-109">It's also a simple way to bulk save draft Q&As that need additional edits or updates.</span></span> <span data-ttu-id="59e8a-110">Если нужно массово изменить существующие вопросы и ответы, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="59e8a-110">If you need to bulk edit existing Q&As, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="59e8a-111">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="59e8a-111">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
2. <span data-ttu-id="59e8a-112">Щелкните **Скачать шаблон вопросов и ответов (.csv)**</span><span class="sxs-lookup"><span data-stu-id="59e8a-112">Click **Download Q&A template (.csv)**</span></span>
    
3. <span data-ttu-id="59e8a-113">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="59e8a-113">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="59e8a-114">Добавьте содержимое и настройки вопросов и ответов, затем сохраните файл</span><span class="sxs-lookup"><span data-stu-id="59e8a-114">Add the Q&A content and settings and save the file</span></span>

    <span data-ttu-id="59e8a-115">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="59e8a-115">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="59e8a-116">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="59e8a-116">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
6. <span data-ttu-id="59e8a-117">В панели импорта вопросов и ответов нажмите кнопку **Обзор** и перейдите к CSV-файлу, который нужно импортировать</span><span class="sxs-lookup"><span data-stu-id="59e8a-117">In the Import Q&As pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="59e8a-118">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="59e8a-118">Click **Import**</span></span>

## <a name="prevent-import-errors"></a><span data-ttu-id="59e8a-119">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="59e8a-119">Prevent import errors</span></span>      
<span data-ttu-id="59e8a-120">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="59e8a-120">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="59e8a-121">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="59e8a-121">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="59e8a-122">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="59e8a-122">Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="59e8a-123">Пока не исправлены все ошибки, вы не сможете создать или изменить вопросы и ответы.</span><span class="sxs-lookup"><span data-stu-id="59e8a-123">Until all errors are resolved, you can't create or edit any Q&As.</span></span> 

<span data-ttu-id="59e8a-124">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="59e8a-124">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="59e8a-125">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="59e8a-125">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="59e8a-126">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="59e8a-126">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="59e8a-127">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="59e8a-127">The column order is the same as the import template</span></span>
- <span data-ttu-id="59e8a-128">эти столбцы могут быть пустыми: Id, Last Modified и Last Modified By;</span><span class="sxs-lookup"><span data-stu-id="59e8a-128">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="59e8a-129">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="59e8a-129">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="59e8a-130">В зависимости от поля State вопросы и ответы сохраняются в черновике, списке предложенных или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="59e8a-130">Based on the State field, Q&As will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="59e8a-131">Кроме того, если добавить идентификатор существующего вопроса с ответом, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="59e8a-131">Also, if you include the Id of an existing Q&A, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="59e8a-132">Для партнеров, управляющих несколькими организациями, можно экспортировать&Q как из одной организации и импортировать их в другую.</span><span class="sxs-lookup"><span data-stu-id="59e8a-132">For partners who manage multiple organizations, you can export your Q&As from one org and import them into another.</span></span> <span data-ttu-id="59e8a-133">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="59e8a-133">But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="59e8a-134">Дополнительные сведения об обязательных и рекомендуемых полях см. в статье [Создание вопросов и ответов](create-qas.md).</span><span class="sxs-lookup"><span data-stu-id="59e8a-134">To find out more about required and recommended fields, see [Create Q&As](create-qas.md).</span></span>

  

