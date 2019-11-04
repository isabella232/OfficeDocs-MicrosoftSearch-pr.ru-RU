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
description: Добавление большого количества местоположений с помощью средств импорта для портала администрирования поиска Microsoft
ms.openlocfilehash: e01c3774439a931dc81f850d8cbee76cc6128a53
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "37948981"
---
# <a name="bulk-create-locations"></a><span data-ttu-id="e41fe-103">Массовое создание расположений</span><span class="sxs-lookup"><span data-stu-id="e41fe-103">Bulk create locations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e41fe-104">Эта статья относится к порталу администрирования Поиска (Майкрософт) в Bing.</span><span class="sxs-lookup"><span data-stu-id="e41fe-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="e41fe-105">Мы переносим портал в Центр администрирования Microsoft 365, после чего портал Поиска (Майкрософт) в Bing будет удален.</span><span class="sxs-lookup"><span data-stu-id="e41fe-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="e41fe-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e41fe-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="e41fe-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="e41fe-107">[Overview of Microsoft Search](overview-microsoft-search.md).</span></span>
    
<span data-ttu-id="e41fe-108">Скачайте и используйте CSV-шаблон для массового создания, редактирования и сохранения расположений.</span><span class="sxs-lookup"><span data-stu-id="e41fe-108">Download and use the .csv template to bulk create, edit, and save locations.</span></span> 
  
1. <span data-ttu-id="e41fe-109">В правом верхнем углу раздела "расположения" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="e41fe-109">In the upper-right corner of the Locations section, click **Import**</span></span>
    
2. <span data-ttu-id="e41fe-110">Щелкните **шаблон расположения скачивания (CSV-файл)** .</span><span class="sxs-lookup"><span data-stu-id="e41fe-110">Click **Download locations template (.csv)**</span></span>
    
3. <span data-ttu-id="e41fe-111">Сохраните и откройте CSV-файл</span><span class="sxs-lookup"><span data-stu-id="e41fe-111">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="e41fe-112">Добавление содержимого расположения и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="e41fe-112">Add the location content and save the file</span></span>

    <span data-ttu-id="e41fe-113">CSV-файл следует сохранить в виде файла CSV UTF-8. Другие типы файлов и кодировки могут приводить к ошибкам импорта</span><span class="sxs-lookup"><span data-stu-id="e41fe-113">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="e41fe-114">В правом верхнем углу раздела "расположения" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="e41fe-114">In the upper-right corner of the Locations section, click **Import**</span></span>
    
6. <span data-ttu-id="e41fe-115">В области Импорт расположений нажмите кнопку **Обзор** и перейдите к CSV-файлу, который необходимо импортировать.</span><span class="sxs-lookup"><span data-stu-id="e41fe-115">In the Import locations pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="e41fe-116">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="e41fe-116">Click **Import**</span></span>

<span data-ttu-id="e41fe-117">Поля в шаблонах расположений для импорта и экспорта одинаковы.</span><span class="sxs-lookup"><span data-stu-id="e41fe-117">The fields in the import and export locations templates are the same.</span></span> <span data-ttu-id="e41fe-118">Вы можете экспортировать, массово изменить и импортировать изменения, а также начать с пустого шаблона для массового создания новых расположений.</span><span class="sxs-lookup"><span data-stu-id="e41fe-118">You can export, bulk edit, and import the edits, or start with an empty template to bulk create new locations.</span></span> <span data-ttu-id="e41fe-119">Чтобы выполнить массовое изменение существующих расположений, экспортируйте их на портале администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="e41fe-119">To bulk edit existing locations, export them from the Admin portal, make the necessary edits, and then import them.</span></span>

## <a name="prevent-import-errors"></a><span data-ttu-id="e41fe-120">Предотвращение ошибок импорта</span><span class="sxs-lookup"><span data-stu-id="e41fe-120">Prevent import errors</span></span>  
<span data-ttu-id="e41fe-121">Если необходимые данные отсутствуют или недействительны, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e41fe-121">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="e41fe-122">В зависимости от ошибки может быть создан файл журнала с дополнительной информацией о том, какие строки и столбцы нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="e41fe-122">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="e41fe-123">Внесите необходимые изменения и повторите импорт файла.</span><span class="sxs-lookup"><span data-stu-id="e41fe-123">Make any necessary edits, and try importing the file again.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e41fe-124">Пока все ошибки не будут устранены, вы не сможете создавать или изменять расположения.</span><span class="sxs-lookup"><span data-stu-id="e41fe-124">Until all errors are resolved, you can't create or edit any locations.</span></span> 

<span data-ttu-id="e41fe-125">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован:</span><span class="sxs-lookup"><span data-stu-id="e41fe-125">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="e41fe-126">включает строку заголовков в шаблоне импорта;</span><span class="sxs-lookup"><span data-stu-id="e41fe-126">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="e41fe-127">включает все столбцы из шаблона импорта;</span><span class="sxs-lookup"><span data-stu-id="e41fe-127">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="e41fe-128">порядок столбцов совпадает с шаблоном импорта;</span><span class="sxs-lookup"><span data-stu-id="e41fe-128">The column order is the same as the import template</span></span>
- <span data-ttu-id="e41fe-129">Эти столбцы могут быть пустыми: ID, Дата последнего изменения, Дата изменения и Широта/длинная</span><span class="sxs-lookup"><span data-stu-id="e41fe-129">These columns can be empty: Id, Last Modified, Last Modified By, and Lat/Long</span></span>  
<span data-ttu-id="e41fe-130">Мы попытаемся определить lat и long на основе адреса, если это поле пусто</span><span class="sxs-lookup"><span data-stu-id="e41fe-130">We'll try to determine lat/long based on the address if that field is empty</span></span>
- <span data-ttu-id="e41fe-131">столбец State не может быть пустым, так как это обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="e41fe-131">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="e41fe-132">В зависимости от поля состояние, расположения будут сохранены как черновики, предложены, запланированы или будут автоматически опубликованы.</span><span class="sxs-lookup"><span data-stu-id="e41fe-132">Based on the State field, locations will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="e41fe-133">Кроме того, если вы включили идентификатор существующего расположения, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="e41fe-133">Also, if you include the Id of an existing location, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="e41fe-134">Для партнеров, которые управляют несколькими организациями, вы можете экспортировать расположения из одной организации и импортировать их в другую.</span><span class="sxs-lookup"><span data-stu-id="e41fe-134">For partners who manage multiple organizations, you can export your locations from one org and import them into another.</span></span> <span data-ttu-id="e41fe-135">Но перед импортом нужно удалить все данные в столбце Id.</span><span class="sxs-lookup"><span data-stu-id="e41fe-135">But you must remove all of the data in the Id column before you import.</span></span>
  
<span data-ttu-id="e41fe-136">Чтобы узнать больше о обязательных и рекомендуемых полях, ознакомьтесь со статьей [Добавление расположения](add-a-location.md).</span><span class="sxs-lookup"><span data-stu-id="e41fe-136">To find out more about required and recommended fields, see [Add a location](add-a-location.md).</span></span>

  

