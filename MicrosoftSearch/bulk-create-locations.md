---
title: Массовое создание расположений
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
ms.assetid: 15c9fada-f7a6-4210-aa6b-028b32217830
ROBOTS: NoIndex
description: Добавляйте множество расположений одновременно с помощью инструментов импорта на портале администрирования Поиска (Майкрософт)
ms.openlocfilehash: 186f6973de1ff87b62b5f07a47eb41acdd842010
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591398"
---
# <a name="bulk-create-locations"></a><span data-ttu-id="cf767-103">Массовое создание расположений</span><span class="sxs-lookup"><span data-stu-id="cf767-103">Bulk create locations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf767-104">Эта статья относится к Поиску (Майкрософт) на портале администрирования Bing.</span><span class="sxs-lookup"><span data-stu-id="cf767-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="cf767-105">Мы переносим портал в Центр администрирования Microsoft 365 с последующим его удалением.</span><span class="sxs-lookup"><span data-stu-id="cf767-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="cf767-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf767-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="cf767-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="cf767-107">[Overview of Microsoft Search](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="cf767-108">Скачайте и используйте шаблон в CSV-формате для массового создания, изменения и сохранения расположений.</span><span class="sxs-lookup"><span data-stu-id="cf767-108">Download and use the .csv template to bulk create, edit, and save locations.</span></span> 
  
1. <span data-ttu-id="cf767-109">В правом верхнем углу раздела "Расположения" выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="cf767-109">In the upper-right corner of the Locations tab, select **Import**.</span></span>
    
2. <span data-ttu-id="cf767-110">Щелкните **Скачать шаблон расположений (.csv)**</span><span class="sxs-lookup"><span data-stu-id="cf767-110">Click **Download locations template (.csv)**</span></span>
    
3. <span data-ttu-id="cf767-111">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="cf767-111">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="cf767-112">Добавьте содержимое расположения и сохраните файл</span><span class="sxs-lookup"><span data-stu-id="cf767-112">Add the location content and save the file</span></span>

    <span data-ttu-id="cf767-113">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="cf767-113">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="cf767-114">В правом верхнем углу раздела "Расположения" выберите пункт **Импорт**</span><span class="sxs-lookup"><span data-stu-id="cf767-114">In the upper-right corner of the Locations tab, select **Import**.</span></span>
    
6. <span data-ttu-id="cf767-115">В панели импорта расположений нажмите кнопку **Обзор** и перейдите к CSV-файлу, который нужно импортировать</span><span class="sxs-lookup"><span data-stu-id="cf767-115">In the Import locations pane, select **Browse**, and then the .csv file that you want to import.</span></span> 
    
7. <span data-ttu-id="cf767-116">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="cf767-116">Click **Import**.</span></span>

<span data-ttu-id="cf767-117">Поля в шаблонах импорта и экспорта расположений одинаковы.</span><span class="sxs-lookup"><span data-stu-id="cf767-117">The fields in the import and export locations templates are the same.</span></span> <span data-ttu-id="cf767-118">Вы можете экспортировать расположения, выполнить массовое изменение и снова импортировать их или использовать пустой шаблон для массового создания новых расположений.</span><span class="sxs-lookup"><span data-stu-id="cf767-118">You can export, bulk edit, and import the edits, or start with an empty template to bulk create new locations.</span></span> <span data-ttu-id="cf767-119">Чтобы массово изменить существующие расположения, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="cf767-119">To bulk edit existing locations, export them from the Admin portal, make the necessary edits, and then import them.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="cf767-120">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="cf767-120">Prevent import errors</span></span>  
<span data-ttu-id="cf767-121">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cf767-121">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="cf767-122">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="cf767-122">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="cf767-123">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="cf767-123">Make necessary edits and try importing the file again.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf767-124">Пока не исправлены все ошибки, вы не сможете создать или изменить расположения.</span><span class="sxs-lookup"><span data-stu-id="cf767-124">Until all errors are resolved, you can't create or edit any locations.</span></span> 

<span data-ttu-id="cf767-125">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="cf767-125">To prevent errors, make sure your import file is properly formatted and:</span></span>
- <span data-ttu-id="cf767-126">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="cf767-126">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="cf767-127">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="cf767-127">Includes the header row and all the columns that were in the import template</span></span>
- <span data-ttu-id="cf767-128">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="cf767-128">The column order is the same as the import template</span></span>
- <span data-ttu-id="cf767-129">эти столбцы могут быть пустыми: Id, Last Modified, Last Modified By и Lat/Long.</span><span class="sxs-lookup"><span data-stu-id="cf767-129">These columns can be empty: Id, Last Modified, Last Modified By, and Lat/Long</span></span>  
<span data-ttu-id="cf767-130">Мы постараемся определить широту и долготу на основе адреса, если это поле не заполнено;</span><span class="sxs-lookup"><span data-stu-id="cf767-130">We'll try to determine lat/long based on the address if that field is empty</span></span>
- <span data-ttu-id="cf767-131">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="cf767-131">The State column is not empty, as this information is required</span></span>  
<span data-ttu-id="cf767-132">В зависимости от поля State расположения сохраняются в черновике, списке предложенных или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="cf767-132">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="cf767-133">Кроме того, если добавить идентификатор существующего расположения, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="cf767-133">If you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="cf767-134">Для организаций с несколькими клиентами можно экспортировать расположения из одного клиента и импортировать их в другой.</span><span class="sxs-lookup"><span data-stu-id="cf767-134">For organizations with multiple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="cf767-135">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="cf767-135">But you must remove the data in the Id column before you import.</span></span>
  
<span data-ttu-id="cf767-136">Дополнительные сведения об обязательных и рекомендуемых полях см. в статье [Добавление расположения](add-a-location.md).</span><span class="sxs-lookup"><span data-stu-id="cf767-136">To find out more about required and recommended fields, see [Add a location](add-a-location.md).</span></span>

  

