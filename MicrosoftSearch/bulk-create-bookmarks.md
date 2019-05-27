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
description: Создавайте множество закладок одновременно с помощью инструментов импорта на портале администрирования Поиска (Майкрософт)
ms.openlocfilehash: 560cda6f94060d428f2d18cc61bd2430cb31b474
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2019
ms.locfileid: "33968353"
---
# <a name="bulk-create-bookmarks"></a><span data-ttu-id="060c4-103">Массовое создание закладок</span><span class="sxs-lookup"><span data-stu-id="060c4-103">Bulk create bookmarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="060c4-104">Параметры Поиска (Майкрософт) в Bing теперь доступны в Центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="060c4-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="060c4-105">Начните с [назначения администраторов поиска](https://docs.microsoft.com/ru-RU/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) в Центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="060c4-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="060c4-106">Скачайте и используйте шаблон в CSV-формате для массового создания, изменения и сохранения закладок.</span><span class="sxs-lookup"><span data-stu-id="060c4-106">Download and use the .csv template to bulk create, edit, and save bookmarks.</span></span> <span data-ttu-id="060c4-107">Чтобы массово изменить существующие закладки, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="060c4-107">To bulk edit existing bookmarks, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="060c4-108">В правом верхнем углу раздела закладок выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="060c4-108">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
2. <span data-ttu-id="060c4-109">Щелкните **Скачать шаблон закладок (.csv)**</span><span class="sxs-lookup"><span data-stu-id="060c4-109">Click **Download bookmarks template (.csv)**</span></span>
    
3. <span data-ttu-id="060c4-110">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="060c4-110">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="060c4-111">Добавьте содержимое и настройки закладок, затем сохраните файл</span><span class="sxs-lookup"><span data-stu-id="060c4-111">Add the bookmark content and settings and save the file</span></span>

    <span data-ttu-id="060c4-112">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="060c4-112">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="060c4-113">В правом верхнем углу раздела закладок выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="060c4-113">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
6. <span data-ttu-id="060c4-114">В панели импорта закладок нажмите кнопку **Обзор** и перейдите к CSV-файлу, который нужно импортировать</span><span class="sxs-lookup"><span data-stu-id="060c4-114">In the Import bookmarks pane, select **Browse** and then the .csv file that you want to import.</span></span> 
    
7. <span data-ttu-id="060c4-115">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="060c4-115">Click **Import**.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="060c4-116">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="060c4-116">Prevent import errors</span></span>      
<span data-ttu-id="060c4-117">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="060c4-117">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="060c4-118">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="060c4-118">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="060c4-119">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="060c4-119">Make necessary edits and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="060c4-120">Пока не исправлены все ошибки, вы не сможете создать или изменить закладки.</span><span class="sxs-lookup"><span data-stu-id="060c4-120">Until all errors are resolved, you can't create or edit any bookmarks.</span></span> 

<span data-ttu-id="060c4-121">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="060c4-121">To prevent errors, make sure your import file is properly formatted and:</span></span>
- <span data-ttu-id="060c4-122">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="060c4-122">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="060c4-123">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="060c4-123">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="060c4-124">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="060c4-124">The column order is the same as the import template</span></span>
- <span data-ttu-id="060c4-125">эти столбцы могут быть пустыми: Id, Last Modified и Last Modified By;</span><span class="sxs-lookup"><span data-stu-id="060c4-125">All columns have values, except the three that can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="060c4-126">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="060c4-126">The State column is not empty, as this information is required</span></span>  
<span data-ttu-id="060c4-127">В зависимости от поля State закладки сохраняются в черновике, списке предложенных или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="060c4-127">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="060c4-128">Кроме того, если добавить идентификатор существующей закладки, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="060c4-128">If you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="060c4-129">Для организаций с несколькими клиентами можно экспортировать закладки из одного клиента и импортировать их в другой.</span><span class="sxs-lookup"><span data-stu-id="060c4-129">For organizations with multiple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="060c4-130">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="060c4-130">But you must remove the data in the Id column before you import.</span></span>

<span data-ttu-id="060c4-131">Дополнительные сведения об обязательных и рекомендуемых полях см. в статье [Создание закладок](create-bookmarks.md).</span><span class="sxs-lookup"><span data-stu-id="060c4-131">To find out more about required and recommended fields, see [Create bookmarks](create-bookmarks.md).</span></span>
