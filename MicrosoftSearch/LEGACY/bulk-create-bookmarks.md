---
title: Массовое создание закладок
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 09/11/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: def300e7-103c-4e92-a062-28ffa27561d7
ROBOTS: NoIndex
description: Создание большого количества закладок с помощью средств импорта для портала администрирования поиска Microsoft
ms.openlocfilehash: 2983a47a8761a2463b25497911024f9bfd069369
ms.sourcegitcommit: 6b531b2ce7253c16251c7089795dedf1d2f3fc33
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2019
ms.locfileid: "38311857"
---
# <a name="bulk-create-bookmarks"></a><span data-ttu-id="69aa7-103">Массовое создание закладок</span><span class="sxs-lookup"><span data-stu-id="69aa7-103">Bulk create bookmarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69aa7-104">Эта статья относится к порталу администрирования Поиска (Майкрософт) в Bing.</span><span class="sxs-lookup"><span data-stu-id="69aa7-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="69aa7-105">Мы переносим портал в Центр администрирования Microsoft 365, после чего портал Поиска (Майкрософт) в Bing будет удален.</span><span class="sxs-lookup"><span data-stu-id="69aa7-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="69aa7-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="69aa7-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="69aa7-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="69aa7-107">[Overview of Microsoft Search](overview-microsoft-search.md).</span></span>
    
<span data-ttu-id="69aa7-108">Скачайте и используйте CSV-шаблон для массового создания, редактирования и сохранения закладок.</span><span class="sxs-lookup"><span data-stu-id="69aa7-108">Download and use the .csv template to bulk create, edit, and save bookmarks.</span></span> <span data-ttu-id="69aa7-109">Чтобы выполнить массовое изменение существующих закладок, экспортируйте их на портале администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="69aa7-109">To bulk edit existing bookmarks, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="69aa7-110">В правом верхнем углу раздела "закладки" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="69aa7-110">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
2. <span data-ttu-id="69aa7-111">Щелкните **скачать шаблон закладок (. csv)**</span><span class="sxs-lookup"><span data-stu-id="69aa7-111">Click **Download bookmarks template (.csv)**</span></span>
    
3. <span data-ttu-id="69aa7-112">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="69aa7-112">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="69aa7-113">Добавление содержимого закладок и параметров и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="69aa7-113">Add the bookmark content and settings and save the file</span></span>

    <span data-ttu-id="69aa7-114">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="69aa7-114">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="69aa7-115">В правом верхнем углу раздела "закладки" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="69aa7-115">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
6. <span data-ttu-id="69aa7-116">В области Импорт закладок нажмите кнопку **Обзор** и перейдите к CSV-файлу, который необходимо импортировать.</span><span class="sxs-lookup"><span data-stu-id="69aa7-116">In the Import bookmarks pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="69aa7-117">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="69aa7-117">Click **Import**</span></span>

## <a name="prevent-import-errors"></a><span data-ttu-id="69aa7-118">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="69aa7-118">Prevent import errors</span></span>      
<span data-ttu-id="69aa7-119">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="69aa7-119">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="69aa7-120">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="69aa7-120">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="69aa7-121">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="69aa7-121">Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="69aa7-122">Пока все ошибки не будут устранены, вы не сможете создавать или изменять закладки.</span><span class="sxs-lookup"><span data-stu-id="69aa7-122">Until all errors are resolved, you can't create or edit any bookmarks.</span></span> 

<span data-ttu-id="69aa7-123">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="69aa7-123">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="69aa7-124">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="69aa7-124">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="69aa7-125">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="69aa7-125">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="69aa7-126">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="69aa7-126">The column order is the same as the import template</span></span>
- <span data-ttu-id="69aa7-127">эти столбцы могут быть пустыми: Id, Last Modified и Last Modified By;</span><span class="sxs-lookup"><span data-stu-id="69aa7-127">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="69aa7-128">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="69aa7-128">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="69aa7-129">В зависимости от поля State закладки сохраняются в черновике, списке рекомендуемых или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="69aa7-129">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="69aa7-130">Кроме того, если вы включили идентификатор существующей закладки, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="69aa7-130">Also, if you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="69aa7-131">Для партнеров, которые управляют несколькими организациями, вы можете экспортировать свои закладки из одной организации и импортировать их в другую.</span><span class="sxs-lookup"><span data-stu-id="69aa7-131">For partners who manage multiple organizations, you can export your bookmarks from one org and import them into another.</span></span> <span data-ttu-id="69aa7-132">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="69aa7-132">But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="69aa7-133">Чтобы получить дополнительные сведения о обязательных и рекомендуемых полях, ознакомьтесь со статьей [Создание закладок](create-bookmarks.md).</span><span class="sxs-lookup"><span data-stu-id="69aa7-133">To find out more about required and recommended fields, see [Create bookmarks](create-bookmarks.md).</span></span>
