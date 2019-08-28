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
ms.openlocfilehash: c0ec4aaa0ee93e94c8569dc383456018ccc6679d
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639778"
---
# <a name="bulk-create-qas"></a><span data-ttu-id="bd554-103">Массовое создание вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="bd554-103">Bulk create Q&As</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd554-104">Эта статья относится к порталу администрирования Поиска (Майкрософт) в Bing.</span><span class="sxs-lookup"><span data-stu-id="bd554-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="bd554-105">Мы переносим портал в Центр администрирования Microsoft 365, после чего портал Поиска (Майкрософт) в Bing будет удален.</span><span class="sxs-lookup"><span data-stu-id="bd554-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="bd554-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bd554-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="bd554-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="bd554-107">[Overview of Microsoft Search](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="bd554-108">Скачайте и используйте шаблон в CSV-формате для массового создания или изменения вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="bd554-108">Download and use the .csv template to bulk create or bulk edit Q&As.</span></span> <span data-ttu-id="bd554-109">Это также простой способ массового сохранения черновика вопросов и ответов, требующего дополнительных изменений или обновлений.</span><span class="sxs-lookup"><span data-stu-id="bd554-109">It's also a simple way to bulk save draft Q&As that need additional edits or updates.</span></span> <span data-ttu-id="bd554-110">Если нужно массово изменить существующие вопросы и ответы, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="bd554-110">If you need to bulk edit existing Q&As, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="bd554-111">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="bd554-111">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
2. <span data-ttu-id="bd554-112">Щелкните **Скачать шаблон вопросов и ответов (.csv)**</span><span class="sxs-lookup"><span data-stu-id="bd554-112">Click **Download Q&A template (.csv)**</span></span>
    
3. <span data-ttu-id="bd554-113">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="bd554-113">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="bd554-114">Добавьте содержимое и настройки вопросов и ответов, затем сохраните файл</span><span class="sxs-lookup"><span data-stu-id="bd554-114">Add the Q&A content and settings and save the file</span></span>

    <span data-ttu-id="bd554-115">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="bd554-115">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="bd554-116">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="bd554-116">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
6. <span data-ttu-id="bd554-117">В панели импорта вопросов и ответов нажмите кнопку **Обзор** и перейдите к CSV-файлу, который нужно импортировать</span><span class="sxs-lookup"><span data-stu-id="bd554-117">In the Import locations pane, select **Browse**, and then the .csv file that you want to import.</span></span> 
    
7. <span data-ttu-id="bd554-118">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="bd554-118">Click **Import**.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="bd554-119">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="bd554-119">Prevent import errors</span></span>      
<span data-ttu-id="bd554-120">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="bd554-120">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="bd554-121">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="bd554-121">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="bd554-122">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="bd554-122">Make necessary edits and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="bd554-123">Пока не исправлены все ошибки, вы не сможете создать или изменить вопросы и ответы.</span><span class="sxs-lookup"><span data-stu-id="bd554-123">Until all errors are resolved, you can't create or edit any Q&As.</span></span> 

<span data-ttu-id="bd554-124">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="bd554-124">To prevent errors, make sure your import file is properly formatted and:</span></span>
- <span data-ttu-id="bd554-125">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="bd554-125">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="bd554-126">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="bd554-126">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="bd554-127">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="bd554-127">The column order is the same as the import template</span></span>
- <span data-ttu-id="bd554-128">эти столбцы могут быть пустыми: Id, Last Modified и Last Modified By;</span><span class="sxs-lookup"><span data-stu-id="bd554-128">All columns have values, except the three that can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="bd554-129">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="bd554-129">The State column is not empty, as this information is required</span></span>  
<span data-ttu-id="bd554-130">В зависимости от поля State вопросы и ответы сохраняются в черновике, списке предложенных или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="bd554-130">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="bd554-131">Кроме того, если добавить идентификатор существующего вопроса с ответом, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="bd554-131">If you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="bd554-132">Для организаций с несколькими клиентами можно экспортировать вопросы и ответы из одного клиента и импортировать их в другой.</span><span class="sxs-lookup"><span data-stu-id="bd554-132">For organizations with multiple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="bd554-133">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="bd554-133">But you must remove the data in the Id column before you import.</span></span>

<span data-ttu-id="bd554-134">Дополнительные сведения об обязательных и рекомендуемых полях см. в статье [Создание вопросов и ответов](create-qas.md).</span><span class="sxs-lookup"><span data-stu-id="bd554-134">To find out more about required and recommended fields, see [Create Q&As](create-qas.md).</span></span>

  

