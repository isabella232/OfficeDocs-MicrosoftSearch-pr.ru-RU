---
title: Соединители графа файлов для поиска в Microsoft Search
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NoIndex
description: Настройка соединитетеля графа файлов для поиска в Microsoft Search
ms.openlocfilehash: 792e853e5d2b7a23835dc031ff4ba4c09d619f9c
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031614"
---
<!---Previous ms.author: rusamai --->

# <a name="file-share-graph-connector"></a><span data-ttu-id="10181-103">Соединители graph share file</span><span class="sxs-lookup"><span data-stu-id="10181-103">File share Graph connector</span></span>

<span data-ttu-id="10181-104">Соединитектор File Share Graph позволяет пользователям в организации искать локальное файлообмявательное окно.</span><span class="sxs-lookup"><span data-stu-id="10181-104">The File share Graph connector allows users in your organization to search on-premise Windows file shares.</span></span>

> [!NOTE]
> <span data-ttu-id="10181-105">Ознакомьтесь [**с статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общий процесс установки соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="10181-105">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="10181-106">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="10181-106">Before you get started</span></span>

### <a name="install-the-graph-connector-agent"></a><span data-ttu-id="10181-107">Установка агента соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="10181-107">Install the Graph connector agent</span></span>

<span data-ttu-id="10181-108">Чтобы индексировать ваши акции файлов Windows, необходимо установить и зарегистрировать агент соединителя Graph.</span><span class="sxs-lookup"><span data-stu-id="10181-108">To index your Windows file shares, you must install and register the Graph connector agent.</span></span> <span data-ttu-id="10181-109">Дополнительные дополнительные данные см. в [дополнительных подробной](on-prem-agent.md) информации об установке агента соединителя Graph.</span><span class="sxs-lookup"><span data-stu-id="10181-109">See [Install the Graph connector agent](on-prem-agent.md) to learn more.</span></span>  

### <a name="content-requirements"></a><span data-ttu-id="10181-110">Требования к контенту</span><span class="sxs-lookup"><span data-stu-id="10181-110">Content requirements</span></span>

### <a name="file-types"></a><span data-ttu-id="10181-111">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="10181-111">File types</span></span>

<span data-ttu-id="10181-112">Содержимое следующих форматов можно индексировать и искать: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTM, TXT, XLB, XLC, XLSB, XLSB, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span><span class="sxs-lookup"><span data-stu-id="10181-112">Content of the following formats can be indexed and searched: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span></span> <span data-ttu-id="10181-113">Индексация только текстового контента этих форматов.</span><span class="sxs-lookup"><span data-stu-id="10181-113">Only the textual content of these formats is indexed.</span></span> <span data-ttu-id="10181-114">Все мультимедийные материалы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="10181-114">All multimedia content is ignored.</span></span> <span data-ttu-id="10181-115">Для любого файла, который не относится к этому формату, индексация только метаданных.</span><span class="sxs-lookup"><span data-stu-id="10181-115">For any file that doesn't belong to this format, the metadata alone is indexed.</span></span>

### <a name="file-size-limits"></a><span data-ttu-id="10181-116">Ограничения на размер файлов</span><span class="sxs-lookup"><span data-stu-id="10181-116">File size limits</span></span>

<span data-ttu-id="10181-117">Максимальный размер поддерживаемых файлов — 100 МБ.</span><span class="sxs-lookup"><span data-stu-id="10181-117">The maximum supported file size is 100 MB.</span></span> <span data-ttu-id="10181-118">Файлы, которые превышают 100 МБ, не индексироваться.</span><span class="sxs-lookup"><span data-stu-id="10181-118">Files that exceed 100 MB aren't indexed.</span></span> <span data-ttu-id="10181-119">Максимальное ограничение размера после обработки — 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="10181-119">The maximum post-processed size limit is 4 MB.</span></span> <span data-ttu-id="10181-120">Обработка прекращается, когда размер файла достигает 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="10181-120">Processing stops when a file's size reaches 4 MB.</span></span> <span data-ttu-id="10181-121">Поэтому некоторые фразы, присутствующие в файле, могут не работать для поиска.</span><span class="sxs-lookup"><span data-stu-id="10181-121">Therefore, some phrases present in the file might not work for search.</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="10181-122">Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="10181-122">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="10181-123">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="10181-123">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="10181-124">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="10181-124">Step 2: Name the connection</span></span>

<span data-ttu-id="10181-125">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="10181-125">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="10181-126">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="10181-126">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="10181-127">На странице **Подключение к источнику данных** выберите **файл** и укажет имя, код подключения и описание.</span><span class="sxs-lookup"><span data-stu-id="10181-127">On the **Connect to data source** page, select **File share** and provide the name, connection ID, and description.</span></span> <span data-ttu-id="10181-128">На следующей странице укажете путь к файлу и выберите ранее установленный агент соединиттеля Graph.</span><span class="sxs-lookup"><span data-stu-id="10181-128">On the next page, provide the path to the file share and select your previously installed Graph connector agent.</span></span> <span data-ttu-id="10181-129">Введите учетные данные учетной записи [пользователя Microsoft Windows](https://microsoft.com/windows) с доступом к всем файлам в файле.</span><span class="sxs-lookup"><span data-stu-id="10181-129">Enter the credentials for a [Microsoft Windows](https://microsoft.com/windows) user account with read access to all the files in the file share.</span></span>

### <a name="preserve-last-access-time"></a><span data-ttu-id="10181-130">Сохранение последнего времени доступа</span><span class="sxs-lookup"><span data-stu-id="10181-130">Preserve last access time</span></span>

<span data-ttu-id="10181-131">При попытке подключения обхода файла обновляется поле "время последнего доступа" в метаданных.</span><span class="sxs-lookup"><span data-stu-id="10181-131">When the connector attempts to crawl a file, the "last access time" field in its metadata is updated.</span></span> <span data-ttu-id="10181-132">Если вы зависите от этого поля для любых решений архивации и резервного копирования и не хотите обновлять его при доступе к нему соединителя, вы можете настроить этот параметр на странице **Расширенные параметры.**</span><span class="sxs-lookup"><span data-stu-id="10181-132">If you depend on that field for any archiving and backup solutions and doesn't want to update it when the connector accesses it, you can configure this option in the **Advanced settings** page.</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="10181-133">Шаг 4. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="10181-133">Step 4: Manage search permissions</span></span>

<span data-ttu-id="10181-134">Вы можете ограничить разрешение на поиск любого файла на основе списков управления доступом к share или списков управления доступом к новой системе доступа NTFS, выбрав нужный вариант на странице Управление разрешениями на **поиск.**</span><span class="sxs-lookup"><span data-stu-id="10181-134">You can restrict the permission to search for any file based on Share Access Control Lists or New Technology File System (NTFS) Access Control Lists, by selecting the desired option in **Manage search permissions** page.</span></span> <span data-ttu-id="10181-135">Учетные записи и группы пользователей, указанные в этих списках управления доступом, должны управляться службой Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="10181-135">The user accounts and groups provided in these Access Control Lists must be managed by Active Directory (AD).</span></span> <span data-ttu-id="10181-136">Если вы используете любую другую систему управления учетными записями пользователей, вы можете выбрать параметр "все", который позволяет пользователям искать все файлы без каких-либо ограничений доступа.</span><span class="sxs-lookup"><span data-stu-id="10181-136">If you are using any other system for user accounts management, you can select 'everyone' option, which lets users search for all the files without any access restrictions.</span></span> <span data-ttu-id="10181-137">Однако, когда пользователи пытаются открыть файл, применяются элементы управления доступом, установленные в источнике.</span><span class="sxs-lookup"><span data-stu-id="10181-137">However, when users try to open the file, access controls set at the source apply.</span></span>

<span data-ttu-id="10181-138">Обратите внимание, что windows по умолчанию предоставляет разрешение "Чтение" на "Все" в share ACLs при совместном доступе папки в сети.</span><span class="sxs-lookup"><span data-stu-id="10181-138">Note that windows by default provides 'Read' permission to 'Everyone' in Share ACLs when a folder is shared on network.</span></span> <span data-ttu-id="10181-139">Кроме того, если вы выбираете share ACLs в **Управлении** разрешениями на поиск, пользователи смогут искать все файлы.</span><span class="sxs-lookup"><span data-stu-id="10181-139">By extension, if you are choosing Share ACLs in **Manage search permissions**, users will be able to search for all the files.</span></span> <span data-ttu-id="10181-140">Если вы хотите ограничить доступ, удалите доступ "Чтение" для "Все" в файлах и предограничите доступ только нужным пользователям и группам.</span><span class="sxs-lookup"><span data-stu-id="10181-140">If you want to restrict access, remove 'Read' access for 'Everyone' in file shares and provide access only to the desired users and groups.</span></span> <span data-ttu-id="10181-141">Соединительные данные считываю эти ограничения доступа и применяем их для поиска.</span><span class="sxs-lookup"><span data-stu-id="10181-141">The connector then reads these access restrictions and applies them to search.</span></span>

<span data-ttu-id="10181-142">Вы можете выбрать ALS share только в том случае, если предоставленный путь к совместной информации следует формату пути UNC.</span><span class="sxs-lookup"><span data-stu-id="10181-142">You can choose Share ACLs only if the share path you provided follows UNC path format.</span></span> <span data-ttu-id="10181-143">Вы можете создать путь в формате UNC, переехав в раздел "Расширенный общий доступ" в разделе "Общий доступ".</span><span class="sxs-lookup"><span data-stu-id="10181-143">You can create a path in UNC format by going to 'Advanced Sharing' under 'Sharing' option.</span></span>

![Advanced_sharing](media/file-connector/file-advanced-sharing.png)

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="10181-145">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="10181-145">Step 5: Assign property labels</span></span>

<span data-ttu-id="10181-146">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="10181-146">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a><span data-ttu-id="10181-147">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="10181-147">Step 6: Manage schema</span></span>

<span data-ttu-id="10181-148">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="10181-148">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="10181-149">Шаг 7. Выбор параметров обновления</span><span class="sxs-lookup"><span data-stu-id="10181-149">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="10181-150">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="10181-150">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a><span data-ttu-id="10181-151">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="10181-151">Step 8: Review connection</span></span>

<span data-ttu-id="10181-152">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="10181-152">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->