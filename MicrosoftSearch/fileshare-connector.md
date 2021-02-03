---
title: Соединители Graph с файловой папкой для Поиска (Майкрософт)
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NoIndex
description: Настройка соединители Graph с файловой папкой для Поиска (Майкрософт)
ms.openlocfilehash: ae496d0a1f41dc75326b0f7ab96e54bda4ee879e
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084851"
---
<!---Previous ms.author: rusamai --->

# <a name="file-share-graph-connector"></a><span data-ttu-id="ae048-103">Соединители Graph с файловой папкой</span><span class="sxs-lookup"><span data-stu-id="ae048-103">File share Graph connector</span></span>

<span data-ttu-id="ae048-104">Соединители Graph с файловой папкой позволяют пользователям в организации искать файлы в локальной папке Windows.</span><span class="sxs-lookup"><span data-stu-id="ae048-104">The File share Graph connector allows users in your organization to search on-premise Windows file shares.</span></span>

> [!NOTE]
> <span data-ttu-id="ae048-105">Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="ae048-105">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="ae048-106">Эта статья для всех, кто настраивает, запускает и отслеживает соединители ServiceNow Graph.</span><span class="sxs-lookup"><span data-stu-id="ae048-106">This article is for anyone who configures, runs, and monitors a ServiceNow Graph connector.</span></span> <span data-ttu-id="ae048-107">Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединитеструктору MediaWiki Graph.</span><span class="sxs-lookup"><span data-stu-id="ae048-107">It supplements the general setup process, and shows instructions that apply only for the MediaWiki Graph connector.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="ae048-108">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="ae048-108">Before you get started</span></span>

### <a name="install-the-graph-connector-agent"></a><span data-ttu-id="ae048-109">Установка агента соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="ae048-109">Install the Graph connector agent</span></span>

<span data-ttu-id="ae048-110">Чтобы проиндексировать файловые папки Windows, необходимо установить и зарегистрировать агент соединителя Graph.</span><span class="sxs-lookup"><span data-stu-id="ae048-110">To index your Windows file shares, you must install and register the Graph connector agent.</span></span> <span data-ttu-id="ae048-111">Дополнительные данные см. в подключении к агенту [соединителя Graph.](on-prem-agent.md)</span><span class="sxs-lookup"><span data-stu-id="ae048-111">See [Install the Graph connector agent](on-prem-agent.md) to learn more.</span></span>  

### <a name="content-requirements"></a><span data-ttu-id="ae048-112">Требования к контенту</span><span class="sxs-lookup"><span data-stu-id="ae048-112">Content requirements</span></span>

### <a name="file-types"></a><span data-ttu-id="ae048-113">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="ae048-113">File types</span></span>

<span data-ttu-id="ae048-114">Контент следующих форматов можно индексировать и искать: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS и ZIP.</span><span class="sxs-lookup"><span data-stu-id="ae048-114">Content of the following formats can be indexed and searched: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span></span> <span data-ttu-id="ae048-115">Индексироваться будет только текстовое содержимое этих форматов.</span><span class="sxs-lookup"><span data-stu-id="ae048-115">Only the textual content of these formats is indexed.</span></span> <span data-ttu-id="ae048-116">Все мультимедийное содержимое игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ae048-116">All multimedia content is ignored.</span></span> <span data-ttu-id="ae048-117">Для любого файла, который не относится к этому формату, индексирование только метаданных.</span><span class="sxs-lookup"><span data-stu-id="ae048-117">For any file that doesn't belong to this format, the metadata alone is indexed.</span></span>

### <a name="file-size-limits"></a><span data-ttu-id="ae048-118">Ограничения на размер файлов</span><span class="sxs-lookup"><span data-stu-id="ae048-118">File size limits</span></span>

<span data-ttu-id="ae048-119">Максимальный поддерживаемый размер файла составляет 100 МБ.</span><span class="sxs-lookup"><span data-stu-id="ae048-119">The maximum supported file size is 100 MB.</span></span> <span data-ttu-id="ae048-120">Файлы, объем которых превышает 100 МБ, не индексироваться.</span><span class="sxs-lookup"><span data-stu-id="ae048-120">Files that exceed 100 MB aren't indexed.</span></span> <span data-ttu-id="ae048-121">Максимальный размер после обработки составляет 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="ae048-121">The maximum post-processed size limit is 4 MB.</span></span> <span data-ttu-id="ae048-122">Обработка останавливается, когда размер файла достигает 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="ae048-122">Processing stops when a file's size reaches 4 MB.</span></span> <span data-ttu-id="ae048-123">Поэтому некоторые фразы, присутствующие в файле, могут не работать для поиска.</span><span class="sxs-lookup"><span data-stu-id="ae048-123">Therefore, some phrases present in the file might not work for search.</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="ae048-124">Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ae048-124">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="ae048-125">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="ae048-125">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="ae048-126">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="ae048-126">Step 2: Name the connection</span></span>

<span data-ttu-id="ae048-127">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="ae048-127">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="ae048-128">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="ae048-128">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="ae048-129">На странице  **"Подключение к источнику данных"** выберите "Файловая папка" и укажет имя, ИД подключения и описание.</span><span class="sxs-lookup"><span data-stu-id="ae048-129">On the **Connect to data source** page, select **File share** and provide the name, connection ID, and description.</span></span> <span data-ttu-id="ae048-130">На следующей странице укажете путь к файловой папке и выберите ранее установленный агент соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="ae048-130">On the next page, provide the path to the file share and select your previously installed Graph connector agent.</span></span> <span data-ttu-id="ae048-131">Введите учетные данные для учетной [записи пользователя Microsoft Windows](https://microsoft.com/windows) с доступом на чтение ко всем файлам в файловом папке.</span><span class="sxs-lookup"><span data-stu-id="ae048-131">Enter the credentials for a [Microsoft Windows](https://microsoft.com/windows) user account with read access to all the files in the file share.</span></span>

### <a name="preserve-last-access-time"></a><span data-ttu-id="ae048-132">Сохранение времени последнего доступа</span><span class="sxs-lookup"><span data-stu-id="ae048-132">Preserve last access time</span></span>

<span data-ttu-id="ae048-133">При попытке соединители обходить файл обновляется поле "Время последнего доступа" в метаданных.</span><span class="sxs-lookup"><span data-stu-id="ae048-133">When the connector attempts to crawl a file, the "last access time" field in its metadata is updated.</span></span> <span data-ttu-id="ae048-134">Если вы зависите от этого поля для каких-либо решений архивации и резервного копирования и не хотите  обновлять его при доступе соединителя к нему, вы можете настроить этот параметр на странице "Дополнительные параметры".</span><span class="sxs-lookup"><span data-stu-id="ae048-134">If you depend on that field for any archiving and backup solutions and doesn't want to update it when the connector accesses it, you can configure this option in the **Advanced settings** page.</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="ae048-135">Шаг 4. Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="ae048-135">Step 4: Manage search permissions</span></span>

<span data-ttu-id="ae048-136">Вы можете ограничить разрешение на поиск файлов на основе списков управления доступом или списков управления доступом новой файловой системы (NTFS).</span><span class="sxs-lookup"><span data-stu-id="ae048-136">You can restrict the permission to search for any file based on Share Access Control Lists or New Technology File System (NTFS) Access Control Lists.</span></span> <span data-ttu-id="ae048-137">Если вы хотите использовать списки управления доступом к данным, выберите соответствующий параметр на странице **"Дополнительные параметры".**</span><span class="sxs-lookup"><span data-stu-id="ae048-137">If you want to use Share Access Control Lists, select the appropriate option on the **Advanced settings** page.</span></span> <span data-ttu-id="ae048-138">Если вы хотите использовать списки управления доступом NTFS, выберите соответствующий параметр на странице "Управление **разрешениями поиска".**</span><span class="sxs-lookup"><span data-stu-id="ae048-138">If you want to use NTFS Access Control Lists, select the appropriate option on the **Manage search permissions** page.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="ae048-139">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="ae048-139">Step 5: Assign property labels</span></span>

<span data-ttu-id="ae048-140">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="ae048-140">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a><span data-ttu-id="ae048-141">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="ae048-141">Step 6: Manage schema</span></span>

<span data-ttu-id="ae048-142">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="ae048-142">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="ae048-143">Шаг 7. Выбор параметров обновления</span><span class="sxs-lookup"><span data-stu-id="ae048-143">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="ae048-144">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="ae048-144">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a><span data-ttu-id="ae048-145">Шаг 8. Проверка подключения</span><span class="sxs-lookup"><span data-stu-id="ae048-145">Step 8: Review connection</span></span>

<span data-ttu-id="ae048-146">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="ae048-146">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
