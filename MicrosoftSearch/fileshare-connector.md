---
title: Соединители файловой папки
ms.author: rusamai
author: rsamai
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NoIndex
description: Настройка соединители файловой папки для Поиска (Майкрософт)
ms.openlocfilehash: bf9fb730abd4ca6e42b681893525bbe3dd8a1419
ms.sourcegitcommit: 249f41723dd6fda1e93ee1a8f3f7571ef066454b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "49750900"
---
# <a name="file-share-connector"></a><span data-ttu-id="9f74b-103">Соединители файловой папки</span><span class="sxs-lookup"><span data-stu-id="9f74b-103">File share connector</span></span>

<span data-ttu-id="9f74b-104">С помощью соединители Graph с файловой папкой пользователи в организации могут искать файлы в локальной папке Windows.</span><span class="sxs-lookup"><span data-stu-id="9f74b-104">With the File share Graph connector, users in your organization can search on-premise Windows file shares.</span></span>

<span data-ttu-id="9f74b-105">Эта статья для администраторов Microsoft 365 или всех, кто настраивает, запускает и отслеживает соединители файловой папки.</span><span class="sxs-lookup"><span data-stu-id="9f74b-105">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a file share connector.</span></span> <span data-ttu-id="9f74b-106">В ней объясняется, как настроить возможности, ограничения и методы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="9f74b-106">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="install-graph-connector-agent"></a><span data-ttu-id="9f74b-107">Установка агента соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="9f74b-107">Install Graph connector agent</span></span>

<span data-ttu-id="9f74b-108">Чтобы проиндексировать файловые папки Windows, необходимо установить и зарегистрировать программное обеспечение агента [соединителя Graph.](on-prem-agent.md)</span><span class="sxs-lookup"><span data-stu-id="9f74b-108">In order to index your Windows file shares, you must install and register [Graph connector agent](on-prem-agent.md) software.</span></span>

## <a name="content-requirements"></a><span data-ttu-id="9f74b-109">Требования к контенту</span><span class="sxs-lookup"><span data-stu-id="9f74b-109">Content requirements</span></span>

### <a name="file-types"></a><span data-ttu-id="9f74b-110">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="9f74b-110">File types</span></span>

<span data-ttu-id="9f74b-111">Контент следующих форматов можно индексировать и искать: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS и ZIP.</span><span class="sxs-lookup"><span data-stu-id="9f74b-111">Content of the following formats can be indexed and searched: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span></span> <span data-ttu-id="9f74b-112">Индексироваться будет только текстовое содержимое этих форматов.</span><span class="sxs-lookup"><span data-stu-id="9f74b-112">Only the textual content of these formats is indexed.</span></span> <span data-ttu-id="9f74b-113">Все мультимедийное содержимое игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9f74b-113">All multimedia content is ignored.</span></span> <span data-ttu-id="9f74b-114">Для любого файла, который не относится к этому формату, индексирование только метаданных.</span><span class="sxs-lookup"><span data-stu-id="9f74b-114">For any file that does not belong to this format, the metadata alone is indexed.</span></span>

### <a name="file-size-limits"></a><span data-ttu-id="9f74b-115">Ограничения на размер файлов</span><span class="sxs-lookup"><span data-stu-id="9f74b-115">File size limits</span></span>

<span data-ttu-id="9f74b-116">Максимальный поддерживаемый размер файла составляет 100 МБ.</span><span class="sxs-lookup"><span data-stu-id="9f74b-116">The maximum supported file size is 100 MB.</span></span> <span data-ttu-id="9f74b-117">Файлы, которые превышают 100 МБ, не индексироваться.</span><span class="sxs-lookup"><span data-stu-id="9f74b-117">Files that exceed 100 MB are not indexed.</span></span> <span data-ttu-id="9f74b-118">Максимальный размер после обработки составляет 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="9f74b-118">The maximum post-processed size limit is 4 MB.</span></span> <span data-ttu-id="9f74b-119">Обработка останавливается, когда размер файла достигает 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="9f74b-119">Processing stops when a file's size reaches 4 MB.</span></span> <span data-ttu-id="9f74b-120">Поэтому некоторые фразы, присутствующие в файле, могут не работать для поиска.</span><span class="sxs-lookup"><span data-stu-id="9f74b-120">Therefore, some phrases present in the file might not work for search.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="9f74b-121">Подключение к источнику данных</span><span class="sxs-lookup"><span data-stu-id="9f74b-121">Connect to a data source</span></span>

<span data-ttu-id="9f74b-122">На странице  **"Подключение к источнику данных"** выберите "Файловая папка" и укажет имя, ИД подключения и описание.</span><span class="sxs-lookup"><span data-stu-id="9f74b-122">On the **Connect to data source** page, select **File share** and provide the name, connection ID, and description.</span></span> <span data-ttu-id="9f74b-123">На следующей странице укажете путь к файловой папке и выберите ранее установленный агент соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="9f74b-123">On the next page, provide the path to the file share and select your previously installed Graph connector agent.</span></span> <span data-ttu-id="9f74b-124">Введите учетные данные для учетной [записи пользователя Microsoft Windows](https://microsoft.com/windows) с доступом на чтение ко всем файлам в файловом папке.</span><span class="sxs-lookup"><span data-stu-id="9f74b-124">Enter the credentials for a [Microsoft Windows](https://microsoft.com/windows) user account with read access to all the files in the file share.</span></span>

## <a name="preserve-last-access-time"></a><span data-ttu-id="9f74b-125">Сохранение времени последнего доступа</span><span class="sxs-lookup"><span data-stu-id="9f74b-125">Preserve last access time</span></span>

<span data-ttu-id="9f74b-126">При попытке соединители обходить файл обновляется поле "Время последнего доступа" в метаданных.</span><span class="sxs-lookup"><span data-stu-id="9f74b-126">When the connector attempts to crawl a file, the "last access time" field in its metadata is updated.</span></span> <span data-ttu-id="9f74b-127">Если вы зависите от этого поля для каких-либо решений архивации и резервного копирования и не  хотите обновлять его при доступе соединителя к нему, этот параметр можно настроить на странице "Дополнительные параметры".</span><span class="sxs-lookup"><span data-stu-id="9f74b-127">If you depend on that field for any archiving and backup solutions and do not want to update it when the connector accesses it, you can configure this option in the **Advanced settings** page.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="9f74b-128">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="9f74b-128">Manage search permissions</span></span>

<span data-ttu-id="9f74b-129">Вы можете ограничить разрешение на поиск файлов на основе списков управления доступом или списков управления доступом новой файловой системы (NTFS).</span><span class="sxs-lookup"><span data-stu-id="9f74b-129">You can restrict the permission to search for any file based on Share Access Control Lists or New Technology File System (NTFS) Access Control Lists.</span></span> <span data-ttu-id="9f74b-130">Если вы хотите использовать списки управления доступом к данным, выберите соответствующий параметр на странице **"Дополнительные параметры".**</span><span class="sxs-lookup"><span data-stu-id="9f74b-130">If you want to use Share Access Control Lists, select the appropriate option on the **Advanced settings** page.</span></span> <span data-ttu-id="9f74b-131">Если вы хотите использовать списки управления доступом NTFS, выберите соответствующий параметр на странице "Управление **разрешениями поиска".**</span><span class="sxs-lookup"><span data-stu-id="9f74b-131">If you want to use NTFS Access Control Lists, select the appropriate option on the **Manage search permissions** page.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="9f74b-132">Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="9f74b-132">Assign property labels</span></span>

<span data-ttu-id="9f74b-133">Для каждой метки можно назначить свойство источника, выбрав в меню параметры.</span><span class="sxs-lookup"><span data-stu-id="9f74b-133">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="9f74b-134">Хотя этот шаг не является обязательным, наличие некоторых меток свойств улучшит релевантность поиска и обеспечит более точные результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="9f74b-134">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="9f74b-135">Управление схемой</span><span class="sxs-lookup"><span data-stu-id="9f74b-135">Manage schema</span></span>

<span data-ttu-id="9f74b-136">На  экране "Управление схемой" можно изменить атрибуты схемы(запрашиваемые, поискуемые, искомые и уточняемые), связанные со свойствами, добавить необязательные псевдонимы и выбрать свойство **Content.**  </span><span class="sxs-lookup"><span data-stu-id="9f74b-136">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="9f74b-137">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="9f74b-137">Set the refresh schedule</span></span>

<span data-ttu-id="9f74b-138">Рекомендуемый интервал по умолчанию для обновления составляет 15 минут, но вы можете изменить его в зависимости от предпочтений.</span><span class="sxs-lookup"><span data-stu-id="9f74b-138">The recommended default refresh schedule interval is 15 minutes, but you can change it based on your preferences.</span></span>

## <a name="result-layout"></a><span data-ttu-id="9f74b-139">Макет результатов</span><span class="sxs-lookup"><span data-stu-id="9f74b-139">Result layout</span></span>

<span data-ttu-id="9f74b-140">Для отображения результатов соединители Fileshare рекомендуется использовать макет результатов по умолчанию, так как он имеет соответствующие значки и элементы управления, которые помогают перейти к пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="9f74b-140">We recommend that you use the default result layout to display your Fileshare connector results because it has appropriate icons and controls that help you navigate to the file path.</span></span> <span data-ttu-id="9f74b-141">При создании нового макета результатов он переопределит значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f74b-141">If you create a new result layout, it will override the default.</span></span>
