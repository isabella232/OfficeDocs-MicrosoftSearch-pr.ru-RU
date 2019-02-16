---
title: Массовое создание К_амп_ас
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
description: Быстрое добавление ответов на часто задаваемые вопросы о средствах импорта на портале администрирования поиска Microsoft
ms.openlocfilehash: 53f1d167948f6b621ad139620553df51b0cb91c2
ms.sourcegitcommit: 61b4b84e581d3df6045851fe6c9c1291853dea06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/16/2019
ms.locfileid: "30068397"
---
# <a name="bulk-create-qas"></a><span data-ttu-id="1cbed-103">Массовое создание К_амп_ас</span><span class="sxs-lookup"><span data-stu-id="1cbed-103">Bulk create Q&As</span></span>

<span data-ttu-id="1cbed-p101">Скачайте и используйте CSV-шаблон для массового создания или массового редактирования К_амп_ас. Кроме того, это простой способ массового сохранения черновиков К_амп_ас, требующих дополнительных изменений или обновлений. Если требуется массово изменить существующую К_амп_ас, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="1cbed-p101">Download and use the .csv template to bulk create or bulk edit Q&As. It's also a simple way to bulk save draft Q&As that need additional edits or updates. If you need to bulk edit existing Q&As, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="1cbed-107">В правом верхнем углу раздела К_амп_ас щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="1cbed-107">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
2. <span data-ttu-id="1cbed-108">Щелкните **скачать шаблон к_амп_а (. csv)**</span><span class="sxs-lookup"><span data-stu-id="1cbed-108">Click **Download Q&A template (.csv)**</span></span>
    
3. <span data-ttu-id="1cbed-109">Сохранение и открытие CSV-файла</span><span class="sxs-lookup"><span data-stu-id="1cbed-109">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="1cbed-110">Добавление содержимого и параметров К_амп_а и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="1cbed-110">Add the Q&A content and settings and save the file</span></span>
    
5. <span data-ttu-id="1cbed-111">В правом верхнем углу раздела К_амп_ас щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="1cbed-111">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
6. <span data-ttu-id="1cbed-112">В области Импорт К_амп_ас нажмите кнопку **Обзор** и перейдите к CSV-файлу, который необходимо импортировать.</span><span class="sxs-lookup"><span data-stu-id="1cbed-112">In the Import Q&As pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="1cbed-113">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="1cbed-113">Click **Import**</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="1cbed-114">Запретить ошибки импорта</span><span class="sxs-lookup"><span data-stu-id="1cbed-114">Prevent import errors</span></span>      
<span data-ttu-id="1cbed-p102">Если какие-либо необходимые данные отсутствуют или недопустимы, вы получите ошибку. В зависимости от ошибки может быть создан файл журнала с дополнительными сведениями о строках и столбцах, которые необходимо исправить. Внесите необходимые изменения и повторите попытку импорта файла.</span><span class="sxs-lookup"><span data-stu-id="1cbed-p102">You'll get an error if any required data is missing or invalid. Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected. Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="1cbed-118">Пока все ошибки не будут устранены, вы не сможете создавать или изменять К_амп_ас.</span><span class="sxs-lookup"><span data-stu-id="1cbed-118">Until all errors are resolved, you can't create or edit any Q&As.</span></span> 

<span data-ttu-id="1cbed-119">Чтобы избежать ошибок, убедитесь, что файл импорта имеет правильный формат:</span><span class="sxs-lookup"><span data-stu-id="1cbed-119">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="1cbed-120">Включает строку заголовков, находился в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="1cbed-120">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="1cbed-121">Включает все столбцы, которые были в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="1cbed-121">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="1cbed-122">Порядок столбцов совпадает с шаблоном импорта</span><span class="sxs-lookup"><span data-stu-id="1cbed-122">The column order is the same as the import template</span></span>
- <span data-ttu-id="1cbed-123">Эти столбцы могут быть пустыми: ID, Дата последнего изменения и Последнее изменение</span><span class="sxs-lookup"><span data-stu-id="1cbed-123">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="1cbed-124">Столбец State не может быть пустым, эта информация является обязательной.</span><span class="sxs-lookup"><span data-stu-id="1cbed-124">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="1cbed-125">В зависимости от поля State, К_амп_ас будет сохранена как черновик, предложено, запланировано или они будут автоматически опубликованы.</span><span class="sxs-lookup"><span data-stu-id="1cbed-125">Based on the State field, Q&As will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="1cbed-126">Кроме того, если вы включили идентификатор существующего К_амп_а, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="1cbed-126">Also, if you include the Id of an existing Q&A, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="1cbed-p103">Для организаций с несколькими клиентами можно экспортировать К_амп_ас из одного клиента и импортировать в другой. Однако перед импортом необходимо удалить все данные в столбце Идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1cbed-p103">For organizations with mulitple tenants, you can export your Q&As from one tenant and import it into another. But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="1cbed-129">Более подробную информацию о обязательных и рекомендуемых полях можно узнать в статье [CREATE к_амп_ас](create-qas.md).</span><span class="sxs-lookup"><span data-stu-id="1cbed-129">To find out more about required and recommended fields, see [Create Q&As](create-qas.md).</span></span>

  

