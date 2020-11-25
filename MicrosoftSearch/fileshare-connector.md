---
title: Соединитель файлов общего доступа
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
description: Настройка соединителя файлового ресурса для службы поиска Майкрософт
ms.openlocfilehash: a95cfe90ca35a385bb9ce3a4c565c18c5a42ec80
ms.sourcegitcommit: 69a1c544cc8db364991cb58d7818d7158ff108b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "49408936"
---
# <a name="file-share-connector"></a><span data-ttu-id="01f91-103">Соединитель файлов общего доступа</span><span class="sxs-lookup"><span data-stu-id="01f91-103">File share connector</span></span>

<span data-ttu-id="01f91-104">С помощью соединителя графа файлового ресурса пользователи организации могут выполнять поиск в локальных общих файловых ресурсах Windows.</span><span class="sxs-lookup"><span data-stu-id="01f91-104">With the File share Graph connector, users in your organization can search on-premise Windows file shares.</span></span>

<span data-ttu-id="01f91-105">Эта статья предназначена для администраторов Microsoft 365 или пользователей, которые настраивают, запускают и отслеживают файловый соединитель.</span><span class="sxs-lookup"><span data-stu-id="01f91-105">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a file share connector.</span></span> <span data-ttu-id="01f91-106">В этой статье объясняется, как настроить возможности соединителя и соединителя, ограничения и способы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="01f91-106">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="install-graph-connector-agent"></a><span data-ttu-id="01f91-107">Установка агента соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="01f91-107">Install Graph connector agent</span></span>

<span data-ttu-id="01f91-108">Чтобы индексировать файловые ресурсы Windows, необходимо установить и зарегистрировать программное обеспечение [агента соединителя Graph](on-prem-agent.md) .</span><span class="sxs-lookup"><span data-stu-id="01f91-108">In order to index your Windows file shares, you must install and register [Graph connector agent](on-prem-agent.md) software.</span></span>

## <a name="content-requirements"></a><span data-ttu-id="01f91-109">Требования к содержимому</span><span class="sxs-lookup"><span data-stu-id="01f91-109">Content requirements</span></span>

### <a name="file-types"></a><span data-ttu-id="01f91-110">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="01f91-110">File types</span></span>

<span data-ttu-id="01f91-111">Можно индексировать и искать содержимое следующих форматов: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, НВС, ОБД, ОБТ, ODP,,, ODP, ODS, PPT, PPTM, PPTX, PPS, PPT, XLC, PPTX, TXT, XLB,</span><span class="sxs-lookup"><span data-stu-id="01f91-111">Content of the following formats can be indexed and searched: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span></span> <span data-ttu-id="01f91-112">Индексируется только текстовое содержимое этих форматов.</span><span class="sxs-lookup"><span data-stu-id="01f91-112">Only the textual content of these formats is indexed.</span></span> <span data-ttu-id="01f91-113">Весь мультимедийный контент игнорируется.</span><span class="sxs-lookup"><span data-stu-id="01f91-113">All multimedia content is ignored.</span></span> <span data-ttu-id="01f91-114">Для любого файла, не принадлежащего этому формату, индексируются только метаданные.</span><span class="sxs-lookup"><span data-stu-id="01f91-114">For any file that does not belong to this format, the metadata alone is indexed.</span></span>

### <a name="file-size-limits"></a><span data-ttu-id="01f91-115">Ограничения на размер файлов</span><span class="sxs-lookup"><span data-stu-id="01f91-115">File size limits</span></span>

<span data-ttu-id="01f91-116">Максимальный поддерживаемый размер файла составляет 100 МБ.</span><span class="sxs-lookup"><span data-stu-id="01f91-116">The maximum supported file size is 100 MB.</span></span> <span data-ttu-id="01f91-117">Файлы, размер которых превышает 100 МБ, не индексируются.</span><span class="sxs-lookup"><span data-stu-id="01f91-117">Files that exceed 100 MB are not indexed.</span></span> <span data-ttu-id="01f91-118">Максимально допустимый размер обработки после обработки составляет 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="01f91-118">The maximum post-processed size limit is 4 MB.</span></span> <span data-ttu-id="01f91-119">Обработка прекратится, когда размер файла достигнет 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="01f91-119">Processing stops when a file's size reaches 4 MB.</span></span> <span data-ttu-id="01f91-120">Поэтому некоторые фразы, присутствующие в файле, могут не работать для поиска.</span><span class="sxs-lookup"><span data-stu-id="01f91-120">Therefore, some phrases present in the file might not work for search.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="01f91-121">Подключение к источнику данных</span><span class="sxs-lookup"><span data-stu-id="01f91-121">Connect to a data source</span></span>

<span data-ttu-id="01f91-122">На странице **Подключение к источнику данных** выберите **файловый ресурс** и укажите имя, идентификатор подключения и описание.</span><span class="sxs-lookup"><span data-stu-id="01f91-122">On the **Connect to data source** page, select **File share** and provide the name, connection ID, and description.</span></span> <span data-ttu-id="01f91-123">На следующей странице Укажите путь к общему файловому ресурсу и выберите ранее установленный агент соединителя Graph.</span><span class="sxs-lookup"><span data-stu-id="01f91-123">On the next page, provide the path to the file share and select your previously installed Graph connector agent.</span></span> <span data-ttu-id="01f91-124">Введите учетные данные для учетной записи пользователя [Microsoft Windows](https://microsoft.com/windows) с доступом на чтение ко всем файлам в общей папке.</span><span class="sxs-lookup"><span data-stu-id="01f91-124">Enter the credentials for a [Microsoft Windows](https://microsoft.com/windows) user account with read access to all the files in the file share.</span></span>

## <a name="preserve-last-access-time"></a><span data-ttu-id="01f91-125">Сохранение времени последнего доступа</span><span class="sxs-lookup"><span data-stu-id="01f91-125">Preserve last access time</span></span>

<span data-ttu-id="01f91-126">Когда соединитель пытается выполнить обход файла, обновляется поле "время последнего доступа" в метаданных.</span><span class="sxs-lookup"><span data-stu-id="01f91-126">When the connector attempts to crawl a file, the "last access time" field in its metadata is updated.</span></span> <span data-ttu-id="01f91-127">Если вы зависели от этого поля для всех решений для архивации и резервного копирования и не хотите обновлять его при доступе соединителя, можно настроить этот параметр на странице **Дополнительные параметры** .</span><span class="sxs-lookup"><span data-stu-id="01f91-127">If you depend on that field for any archiving and backup solutions and do not want to update it when the connector accesses it, you can configure this option in the **Advanced settings** page.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="01f91-128">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="01f91-128">Manage search permissions</span></span>

<span data-ttu-id="01f91-129">Вы можете ограничить разрешение для поиска любого файла на основе списков управления доступом к общему ресурсу или в новых списках управления доступом к файловой системе (NTFS).</span><span class="sxs-lookup"><span data-stu-id="01f91-129">You can restrict the permission to search for any file based on Share Access Control Lists or New Technology File System (NTFS) Access Control Lists.</span></span> <span data-ttu-id="01f91-130">Если вы хотите использовать общие списки управления доступом, выберите соответствующий параметр на странице **Дополнительные параметры** .</span><span class="sxs-lookup"><span data-stu-id="01f91-130">If you want to use Share Access Control Lists, select the appropriate option on the **Advanced settings** page.</span></span> <span data-ttu-id="01f91-131">Если вы хотите использовать списки управления доступом NTFS, выберите соответствующий параметр на странице " **Управление разрешениями поиска** ".</span><span class="sxs-lookup"><span data-stu-id="01f91-131">If you want to use NTFS Access Control Lists, select the appropriate option on the **Manage search permissions** page.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="01f91-132">Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="01f91-132">Assign property labels</span></span>

<span data-ttu-id="01f91-133">Можно назначить свойство источника каждой метке, выбрав в меню пункт Параметры.</span><span class="sxs-lookup"><span data-stu-id="01f91-133">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="01f91-134">Хотя это действие не является обязательным, наличие некоторых меток свойств повысит релевантность поиска и обеспечит более точные результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="01f91-134">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="01f91-135">Управление схемой</span><span class="sxs-lookup"><span data-stu-id="01f91-135">Manage schema</span></span>

<span data-ttu-id="01f91-136">На экране **Управление схемой** можно изменить атрибуты схемы (возможность **запроса**, возможность **поиска**, **Извлечение** и **уточнение**), связанные со свойствами, добавить необязательные псевдонимы и выбрать свойство **содержимого** .</span><span class="sxs-lookup"><span data-stu-id="01f91-136">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="01f91-137">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="01f91-137">Set the refresh schedule</span></span>

<span data-ttu-id="01f91-138">Рекомендуемый интервал расписания обновления по умолчанию равен 15 минутам, но его можно изменить в соответствии с вашими предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="01f91-138">The recommended default refresh schedule interval is 15 minutes, but you can change it based on your preferences.</span></span>
