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
description: Создание большого количества закладок с помощью средств импорта для портала администрирования поиска Microsoft
ms.openlocfilehash: 07694de1f546a1431f371fa24ffc5721ea66337c
ms.sourcegitcommit: 61b4b84e581d3df6045851fe6c9c1291853dea06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/16/2019
ms.locfileid: "30068405"
---
# <a name="bulk-create-bookmarks"></a><span data-ttu-id="84ef3-103">Массовое создание закладок</span><span class="sxs-lookup"><span data-stu-id="84ef3-103">Bulk create bookmarks</span></span>

<span data-ttu-id="84ef3-p101">Скачайте и используйте CSV-шаблон для массового создания, редактирования и сохранения закладок. Чтобы выполнить массовое изменение существующих закладок, экспортируйте их на портале администрирования, внесите необходимые изменения, а затем импортируйте их.</span><span class="sxs-lookup"><span data-stu-id="84ef3-p101">Download and use the .csv template to bulk create, edit, and save bookmarks. To bulk edit existing bookmarks, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="84ef3-106">В правом верхнем углу раздела "закладки" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="84ef3-106">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
2. <span data-ttu-id="84ef3-107">Щелкните **скачать шаблон закладок (. csv)**</span><span class="sxs-lookup"><span data-stu-id="84ef3-107">Click **Download bookmarks template (.csv)**</span></span>
    
3. <span data-ttu-id="84ef3-108">Сохранение и открытие CSV-файла</span><span class="sxs-lookup"><span data-stu-id="84ef3-108">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="84ef3-109">Добавление содержимого закладок и параметров и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="84ef3-109">Add the bookmark content and settings and save the file</span></span>
    
5. <span data-ttu-id="84ef3-110">В правом верхнем углу раздела "закладки" щелкните **Импорт**</span><span class="sxs-lookup"><span data-stu-id="84ef3-110">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
6. <span data-ttu-id="84ef3-111">В области Импорт закладок нажмите кнопку **Обзор** и перейдите к CSV-файлу, который необходимо импортировать.</span><span class="sxs-lookup"><span data-stu-id="84ef3-111">In the Import bookmarks pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="84ef3-112">Нажмите кнопку **Импорт**</span><span class="sxs-lookup"><span data-stu-id="84ef3-112">Click **Import**</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="84ef3-113">Запретить ошибки импорта</span><span class="sxs-lookup"><span data-stu-id="84ef3-113">Prevent import errors</span></span>      
<span data-ttu-id="84ef3-p102">Если какие-либо необходимые данные отсутствуют или недопустимы, вы получите ошибку. В зависимости от ошибки может быть создан файл журнала с дополнительными сведениями о строках и столбцах, которые необходимо исправить. Внесите необходимые изменения и повторите попытку импорта файла.</span><span class="sxs-lookup"><span data-stu-id="84ef3-p102">You'll get an error if any required data is missing or invalid. Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected. Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="84ef3-117">Пока все ошибки не будут устранены, вы не сможете создавать или изменять закладки.</span><span class="sxs-lookup"><span data-stu-id="84ef3-117">Until all errors are resolved, you can't create or edit any bookmarks.</span></span> 

<span data-ttu-id="84ef3-118">Чтобы избежать ошибок, убедитесь, что файл импорта имеет правильный формат:</span><span class="sxs-lookup"><span data-stu-id="84ef3-118">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="84ef3-119">Включает строку заголовков, находился в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="84ef3-119">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="84ef3-120">Включает все столбцы, которые были в шаблоне импорта</span><span class="sxs-lookup"><span data-stu-id="84ef3-120">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="84ef3-121">Порядок столбцов совпадает с шаблоном импорта</span><span class="sxs-lookup"><span data-stu-id="84ef3-121">The column order is the same as the import template</span></span>
- <span data-ttu-id="84ef3-122">Эти столбцы могут быть пустыми: ID, Дата последнего изменения и Последнее изменение</span><span class="sxs-lookup"><span data-stu-id="84ef3-122">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="84ef3-123">Столбец State не может быть пустым, эта информация является обязательной.</span><span class="sxs-lookup"><span data-stu-id="84ef3-123">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="84ef3-124">В зависимости от поля State закладки будут сохранены как черновики, предложены, запланированы или автоматически опубликованы.</span><span class="sxs-lookup"><span data-stu-id="84ef3-124">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="84ef3-125">Кроме того, если вы включили идентификатор существующей закладки, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="84ef3-125">Also, if you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="84ef3-p103">Для организаций с несколькими клиентами можно экспортировать закладки из одного клиента и импортировать их в другой. Однако перед импортом необходимо удалить все данные в столбце Идентификатор.</span><span class="sxs-lookup"><span data-stu-id="84ef3-p103">For organizations with mulitple tenants, you can export your bookmarks from one tenant and import it into another. But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="84ef3-128">Чтобы получить дополнительные сведения о обязательных и рекомендуемых полях, ознакомьтесь со статьей [Создание закладок](create-bookmarks.md).</span><span class="sxs-lookup"><span data-stu-id="84ef3-128">To find out more about required and recommended fields, see [Create bookmarks](create-bookmarks.md).</span></span>
