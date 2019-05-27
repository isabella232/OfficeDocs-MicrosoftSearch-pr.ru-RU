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
description: Быстрое добавление ответов на часто задаваемые вопросы с помощью средств импорта на портале администрирования Поиска (Майкрософт)
ms.openlocfilehash: f535cb7ae843def536976cb1f05c8601de592cbb
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2019
ms.locfileid: "33968310"
---
# <a name="bulk-create-qas"></a><span data-ttu-id="45ca3-103">Массовое создание вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="45ca3-103">Bulk create Q&As</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45ca3-104">Параметры Поиска (Майкрософт) в Bing теперь доступны в Центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="45ca3-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="45ca3-105">Начните с [назначения администраторов поиска](https://docs.microsoft.com/ru-RU/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) в Центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="45ca3-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="45ca3-106">Скачайте и используйте шаблон в CSV-формате для массового создания или изменения вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="45ca3-106">Download and use the .csv template to bulk create or bulk edit Q&As.</span></span> <span data-ttu-id="45ca3-107">Это также простой способ массового сохранения черновика вопросов и ответов, требующего дополнительных изменений или обновлений.</span><span class="sxs-lookup"><span data-stu-id="45ca3-107">It's also a simple way to bulk save draft Q&As that need additional edits or updates.</span></span> <span data-ttu-id="45ca3-108">Если нужно массово изменить существующие вопросы и ответы, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="45ca3-108">If you need to bulk edit existing Q&As, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="45ca3-109">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="45ca3-109">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
2. <span data-ttu-id="45ca3-110">Щелкните **Скачать шаблон вопросов и ответов (.csv)**</span><span class="sxs-lookup"><span data-stu-id="45ca3-110">Click **Download Q&A template (.csv)**</span></span>
    
3. <span data-ttu-id="45ca3-111">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="45ca3-111">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="45ca3-112">Добавьте содержимое и настройки вопросов и ответов, затем сохраните файл</span><span class="sxs-lookup"><span data-stu-id="45ca3-112">Add the Q&A content and settings and save the file</span></span>

    <span data-ttu-id="45ca3-113">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="45ca3-113">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="45ca3-114">В правом верхнем углу раздела вопросов и ответов выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="45ca3-114">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
6. <span data-ttu-id="45ca3-115">В панели импорта вопросов и ответов нажмите кнопку **Обзор** и перейдите к CSV-файлу, который нужно импортировать</span><span class="sxs-lookup"><span data-stu-id="45ca3-115">In the Import locations pane, select **Browse**, and then the .csv file that you want to import.</span></span> 
    
7. <span data-ttu-id="45ca3-116">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="45ca3-116">Click **Import**.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="45ca3-117">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="45ca3-117">Prevent import errors</span></span>      
<span data-ttu-id="45ca3-118">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="45ca3-118">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="45ca3-119">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="45ca3-119">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="45ca3-120">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="45ca3-120">Make necessary edits and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="45ca3-121">Пока не исправлены все ошибки, вы не сможете создать или изменить вопросы и ответы.</span><span class="sxs-lookup"><span data-stu-id="45ca3-121">Until all errors are resolved, you can't create or edit any Q&As.</span></span> 

<span data-ttu-id="45ca3-122">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="45ca3-122">To prevent errors, make sure your import file is properly formatted and:</span></span>
- <span data-ttu-id="45ca3-123">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="45ca3-123">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="45ca3-124">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="45ca3-124">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="45ca3-125">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="45ca3-125">The column order is the same as the import template</span></span>
- <span data-ttu-id="45ca3-126">эти столбцы могут быть пустыми: Id, Last Modified и Last Modified By;</span><span class="sxs-lookup"><span data-stu-id="45ca3-126">All columns have values, except the three that can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="45ca3-127">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="45ca3-127">The State column is not empty, as this information is required</span></span>  
<span data-ttu-id="45ca3-128">В зависимости от поля State вопросы и ответы сохраняются в черновике, списке предложенных или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="45ca3-128">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="45ca3-129">Кроме того, если добавить идентификатор существующего вопроса с ответом, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="45ca3-129">If you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="45ca3-130">Для организаций с несколькими клиентами можно экспортировать вопросы и ответы из одного клиента и импортировать их в другой.</span><span class="sxs-lookup"><span data-stu-id="45ca3-130">For organizations with multiple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="45ca3-131">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="45ca3-131">But you must remove the data in the Id column before you import.</span></span>

<span data-ttu-id="45ca3-132">Дополнительные сведения об обязательных и рекомендуемых полях см. в статье [Создание вопросов и ответов](create-qas.md).</span><span class="sxs-lookup"><span data-stu-id="45ca3-132">To find out more about required and recommended fields, see [Create Q&As](create-qas.md).</span></span>

  

