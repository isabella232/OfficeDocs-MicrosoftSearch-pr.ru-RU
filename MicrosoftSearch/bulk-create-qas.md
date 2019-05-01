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
description: Быстрое добавление ответов на часто задаваемые вопросы о средствах импорта на портале администрирования поиска Microsoft
ms.openlocfilehash: 28fcf57c44f809e7f9b0c1b27042f4549067a0f8
ms.sourcegitcommit: a5fd9d4f46bbb7c539630735ac16e0c786939e5d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2019
ms.locfileid: "33508676"
---
# <a name="bulk-create-qas"></a><span data-ttu-id="7fe0a-103">Массовое создание вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="7fe0a-103">Bulk create Q&As</span></span>

<span data-ttu-id="7fe0a-104">Скачайте и используйте CSV-шаблон для массового создания или массового редактирования К_амп_ас.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-104">Download and use the .csv template to bulk create or bulk edit Q&As.</span></span> <span data-ttu-id="7fe0a-105">Кроме того, это простой способ массового сохранения черновиков К_амп_ас, требующих дополнительных изменений или обновлений.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-105">It's also a simple way to bulk save draft Q&As that need additional edits or updates.</span></span> <span data-ttu-id="7fe0a-106">Если требуется массово изменить существующую К_амп_ас, экспортируйте их из портала администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-106">If you need to bulk edit existing Q&As, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="7fe0a-107">В правом верхнем углу раздела К_амп_ас щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="7fe0a-107">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
2. <span data-ttu-id="7fe0a-108">Щелкните **скачать шаблон к_амп_а (. csv)**</span><span class="sxs-lookup"><span data-stu-id="7fe0a-108">Click **Download Q&A template (.csv)**</span></span>
    
3. <span data-ttu-id="7fe0a-109">Сохранение и открытие CSV-файла</span><span class="sxs-lookup"><span data-stu-id="7fe0a-109">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="7fe0a-110">Добавление содержимого и параметров К_амп_а и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="7fe0a-110">Add the Q&A content and settings and save the file</span></span>

    <span data-ttu-id="7fe0a-111">CSV-файл должен быть сохранен в виде файла CSV UTF-8, другие типы файлов и кодировки могут вызывать ошибки импорта</span><span class="sxs-lookup"><span data-stu-id="7fe0a-111">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="7fe0a-112">В правом верхнем углу раздела К_амп_ас щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="7fe0a-112">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
6. <span data-ttu-id="7fe0a-113">В области Импорт К_амп_ас нажмите кнопку **Обзор** и перейдите к CSV-файлу, который необходимо импортировать.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-113">In the Import Q&As pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="7fe0a-114">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="7fe0a-114">Click **Import**</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="7fe0a-115">Запретить ошибки импорта</span><span class="sxs-lookup"><span data-stu-id="7fe0a-115">Prevent import errors</span></span>      
<span data-ttu-id="7fe0a-116">Если какие-либо необходимые данные отсутствуют или недопустимы, вы получите ошибку.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-116">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="7fe0a-117">В зависимости от ошибки может быть создан файл журнала с дополнительными сведениями о строках и столбцах, которые необходимо исправить.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-117">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="7fe0a-118">Внесите необходимые изменения и повторите попытку импорта файла.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-118">Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="7fe0a-119">Пока все ошибки не будут устранены, вы не сможете создавать или изменять К_амп_ас.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-119">Until all errors are resolved, you can't create or edit any Q&As.</span></span> 

<span data-ttu-id="7fe0a-120">Чтобы избежать ошибок, убедитесь, что файл импорта имеет правильный формат:</span><span class="sxs-lookup"><span data-stu-id="7fe0a-120">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="7fe0a-121">Включает строку заголовков, находился в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="7fe0a-121">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="7fe0a-122">Включает все столбцы, которые были в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="7fe0a-122">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="7fe0a-123">Порядок столбцов совпадает с шаблоном импорта</span><span class="sxs-lookup"><span data-stu-id="7fe0a-123">The column order is the same as the import template</span></span>
- <span data-ttu-id="7fe0a-124">Эти столбцы могут быть пустыми: ID, Дата последнего изменения и Последнее изменение</span><span class="sxs-lookup"><span data-stu-id="7fe0a-124">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="7fe0a-125">Столбец State не может быть пустым, эта информация является обязательной.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-125">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="7fe0a-126">В зависимости от поля State, К_амп_ас будет сохранена как черновик, предложено, запланировано или они будут автоматически опубликованы.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-126">Based on the State field, Q&As will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="7fe0a-127">Кроме того, если вы включили идентификатор существующего К_амп_а, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-127">Also, if you include the Id of an existing Q&A, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="7fe0a-128">Для организаций с несколькими клиентами можно экспортировать К_амп_ас из одного клиента и импортировать в другой.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-128">For organizations with mulitple tenants, you can export your Q&As from one tenant and import it into another.</span></span> <span data-ttu-id="7fe0a-129">Однако перед импортом необходимо удалить все данные в столбце Идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7fe0a-129">But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="7fe0a-130">Более подробную информацию о обязательных и рекомендуемых полях можно узнать в статье [CREATE к_амп_ас](create-qas.md).</span><span class="sxs-lookup"><span data-stu-id="7fe0a-130">To find out more about required and recommended fields, see [Create Q&As](create-qas.md).</span></span>

  

