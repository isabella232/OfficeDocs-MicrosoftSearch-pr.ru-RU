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
description: Добавление большого количества местоположений с помощью средств импорта для портала администрирования поиска Microsoft
ms.openlocfilehash: eb51b93ceaa560e5142ac46d316ba745c614fe34
ms.sourcegitcommit: 61b4b84e581d3df6045851fe6c9c1291853dea06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/16/2019
ms.locfileid: "30068413"
---
# <a name="bulk-create-locations"></a><span data-ttu-id="13d3a-103">Массовое создание расположений</span><span class="sxs-lookup"><span data-stu-id="13d3a-103">Bulk create locations</span></span>

<span data-ttu-id="13d3a-104">Скачайте и используйте CSV-шаблон для массового создания, редактирования и сохранения расположений.</span><span class="sxs-lookup"><span data-stu-id="13d3a-104">Download and use the .csv template to bulk create, edit, and save locations.</span></span> 
  
1. <span data-ttu-id="13d3a-105">В правом верхнем углу раздела "расположения" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="13d3a-105">In the upper-right corner of the Locations section, click **Import**</span></span>
    
2. <span data-ttu-id="13d3a-106">Щелкните **шаблон расположения скачивания (CSV-файл)** .</span><span class="sxs-lookup"><span data-stu-id="13d3a-106">Click **Download locations template (.csv)**</span></span>
    
3. <span data-ttu-id="13d3a-107">Сохранение и открытие CSV-файла</span><span class="sxs-lookup"><span data-stu-id="13d3a-107">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="13d3a-108">Добавление содержимого расположения и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="13d3a-108">Add the location content and save the file</span></span>
    
5. <span data-ttu-id="13d3a-109">В правом верхнем углу раздела "расположения" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="13d3a-109">In the upper-right corner of the Locations section, click **Import**</span></span>
    
6. <span data-ttu-id="13d3a-110">В области Импорт расположений нажмите кнопку **Обзор** и перейдите к CSV-файлу, который необходимо импортировать.</span><span class="sxs-lookup"><span data-stu-id="13d3a-110">In the Import locations pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="13d3a-111">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="13d3a-111">Click **Import**</span></span>

<span data-ttu-id="13d3a-p101">Поля в шаблонах расположений для импорта и экспорта одинаковы. Вы можете экспортировать, массово изменить и импортировать изменения, а также начать с пустого шаблона для массового создания новых расположений. Чтобы выполнить массовое изменение существующих расположений, экспортируйте их на портале администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="13d3a-p101">The fields in the import and export locations templates are the same. You can export, bulk edit, and import the edits, or start with an empty template to bulk create new locations. To bulk edit existing locations, export them from the Admin portal, make the necessary edits, and then import them.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="13d3a-115">Запретить ошибки импорта</span><span class="sxs-lookup"><span data-stu-id="13d3a-115">Prevent import errors</span></span>  
<span data-ttu-id="13d3a-p102">Если какие-либо необходимые данные отсутствуют или недопустимы, вы получите ошибку. В зависимости от ошибки может быть создан файл журнала с дополнительными сведениями о строках и столбцах, которые необходимо исправить. Внесите необходимые изменения и повторите попытку импорта файла.</span><span class="sxs-lookup"><span data-stu-id="13d3a-p102">You'll get an error if any required data is missing or invalid. Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected. Make any necessary edits, and try importing the file again.</span></span>
  
> [!NOTE]
> <span data-ttu-id="13d3a-119">Пока все ошибки не будут устранены, вы не сможете создавать или изменять расположения.</span><span class="sxs-lookup"><span data-stu-id="13d3a-119">Until all errors are resolved, you can't create or edit any locations.</span></span> 

<span data-ttu-id="13d3a-120">Чтобы избежать ошибок, убедитесь, что файл импорта имеет правильный формат:</span><span class="sxs-lookup"><span data-stu-id="13d3a-120">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="13d3a-121">Включает строку заголовков, находился в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="13d3a-121">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="13d3a-122">Включает все столбцы, которые были в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="13d3a-122">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="13d3a-123">Порядок столбцов совпадает с шаблоном импорта</span><span class="sxs-lookup"><span data-stu-id="13d3a-123">The column order is the same as the import template</span></span>
- <span data-ttu-id="13d3a-124">Эти столбцы могут быть пустыми: ID, Дата последнего изменения, Дата изменения и Широта/длинная</span><span class="sxs-lookup"><span data-stu-id="13d3a-124">These columns can be empty: Id, Last Modified, Last Modified By, and Lat/Long</span></span>  
<span data-ttu-id="13d3a-125">Мы попытаемся определить lat и long на основе адреса, если это поле пусто</span><span class="sxs-lookup"><span data-stu-id="13d3a-125">We'll try to determine lat/long based on the address if that field is empty</span></span>
- <span data-ttu-id="13d3a-126">Столбец State не может быть пустым, эта информация является обязательной.</span><span class="sxs-lookup"><span data-stu-id="13d3a-126">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="13d3a-127">В зависимости от поля состояние, расположения будут сохранены как черновики, предложены, запланированы или будут автоматически опубликованы.</span><span class="sxs-lookup"><span data-stu-id="13d3a-127">Based on the State field, locations will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="13d3a-128">Кроме того, если вы включили идентификатор существующего расположения, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="13d3a-128">Also, if you include the Id of an existing location, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="13d3a-p103">В организациях с несколькими клиентами можно экспортировать расположения из одного клиента и импортировать их в другой. Однако перед импортом необходимо удалить все данные в столбце Идентификатор.</span><span class="sxs-lookup"><span data-stu-id="13d3a-p103">For organizations with mulitple tenants, you can export your locations from one tenant and import it into another. But you must remove all of the data in the Id column before you import.</span></span>
  
<span data-ttu-id="13d3a-131">Чтобы узнать больше о обязательных и рекомендуемых полях, ознакомьтесь со статьей [Добавление расположения](add-a-location.md).</span><span class="sxs-lookup"><span data-stu-id="13d3a-131">To find out more about required and recommended fields, see [Add a location](add-a-location.md).</span></span>

  

