---
title: Соединитель Azure Data Lake Graph для Поиска (Майкрософт)
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
description: Настройка соединитора Azure Data Lake Storage Gen2 Graph для Поиска (Майкрософт)
ms.openlocfilehash: da508694929d3c83a456c664aa4613b09a1b14a3
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084860"
---
<!---Previous ms.author: monaray --->

# <a name="azure-data-lake-storage-gen2-graph-connector"></a><span data-ttu-id="98583-103">Соединитель Azure Data Lake Storage Gen2 Graph</span><span class="sxs-lookup"><span data-stu-id="98583-103">Azure Data Lake Storage Gen2 Graph connector</span></span>

<span data-ttu-id="98583-104">Соединители Azure Data Lake Storage Gen2 Graph позволяют пользователям в организации искать файлы, хранимые в учетных записях хранилища [BLOB-файлов Azure](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) [и Azure Data Lake поколения 2.](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)</span><span class="sxs-lookup"><span data-stu-id="98583-104">The Azure Data Lake Storage Gen2 Graph connector allows users in your organization to search for files stored in [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) accounts.</span></span>

> [!NOTE]
> <span data-ttu-id="98583-105">Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="98583-105">Read the [**Setup your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="98583-106">Эта статья посвящена всем, кто настраивает, запускает и отслеживает соединитель Хранилища данных Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="98583-106">This article is for anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="98583-107">Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединитеструктору Хранилища данных Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="98583-107">It supplements the general setup process, and shows instructions that apply only for the Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="98583-108">В этой статье также содержатся сведения об [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="98583-108">This article also includes information about [Limitations](#limitations).</span></span>

<span data-ttu-id="98583-109">В этой статье мы используем *хранилище Azure в* качестве универсального термина для хранилища [BLOB-хранилищ Azure](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) и хранилища Azure Data Lake поколения [2.](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)</span><span class="sxs-lookup"><span data-stu-id="98583-109">In the article, we use *Azure Storage* as a generic term for [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction).</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="98583-110">Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="98583-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="98583-111">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="98583-111">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="98583-112">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="98583-112">Step 2: Name the connection</span></span>

<span data-ttu-id="98583-113">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="98583-113">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="98583-114">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="98583-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="98583-115">Введите строку подключения к основному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="98583-115">Enter your Primary storage connection String.</span></span> <span data-ttu-id="98583-116">Эта строка необходима, чтобы разрешить доступ к вашей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="98583-116">This string is required to allow access to your storage account.</span></span> <span data-ttu-id="98583-117">Чтобы найти строку подключения, перейдите на  портал [Azure](https://ms.portal.azure.com/#home) и перейдите в раздел "Ключи" соответствующей учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="98583-117">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of your relevant Azure Storage account.</span></span>

<span data-ttu-id="98583-118">Если вы предпочитаете не предоставлять **AccountKey** (параметр в строке основного подключения к хранилищу), предодав доступ к нашей службе соединителя Graph для следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="98583-118">If you prefer not to provide the **AccountKey** (a parameter in the primary storage connection string), grant access to our Graph Connectors Service for the following roles:</span></span>

* <span data-ttu-id="98583-119">Storage Blob Data Reader</span><span class="sxs-lookup"><span data-stu-id="98583-119">Storage Blob Data Reader</span></span>
* <span data-ttu-id="98583-120">Участник данных очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="98583-120">Storage Queue Data Contributor</span></span>
* <span data-ttu-id="98583-121">Делегатор BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="98583-121">Storage Blob Delegator</span></span>

<span data-ttu-id="98583-122">Перейдите на **вкладку "Управление** доступом" учетной записи службы хранилища Azure и следуйте инструкциям, чтобы предоставить доступ к следующему приложению:</span><span class="sxs-lookup"><span data-stu-id="98583-122">Navigate to the **Access Control** tab of your Azure Storage account, and follow the instructions there to grant access to the following app:</span></span>

* <span data-ttu-id="98583-123">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="98583-123">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="98583-124">**Имя приложения первой стороны:** Служба соединители Graph</span><span class="sxs-lookup"><span data-stu-id="98583-124">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="98583-125">Учетная запись хранения и уведомления очереди (необязательно)</span><span class="sxs-lookup"><span data-stu-id="98583-125">Storage account and queue notifications (Optional)</span></span>

<span data-ttu-id="98583-126">Поддержка обработки изменений в режиме реального времени в службе соединители Graph может быть добавлена в будущем.</span><span class="sxs-lookup"><span data-stu-id="98583-126">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="98583-127">В этом случае мы будем отслеживать уведомления об изменениях хранилища Azure, хранимые в очереди.</span><span class="sxs-lookup"><span data-stu-id="98583-127">In that case, we'll monitor Azure Storage change notifications stored in a queue.</span></span> <span data-ttu-id="98583-128">Вам потребуется создать очередь в той же учетной записи, что и учетная запись службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="98583-128">You'll need to create a queue in the same account as your Azure Storage account.</span></span>

<span data-ttu-id="98583-129">После создания очереди перейдите на вкладку **"События"** на странице очереди, чтобы настроить **подписку на события.**</span><span class="sxs-lookup"><span data-stu-id="98583-129">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="98583-130">Выберите все события BLOB, которые будет получать очередь, и подключите очередь к учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="98583-130">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Storage account.</span></span>

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="98583-131">Шаг 4. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="98583-131">Step 4: Assign property labels</span></span>

<span data-ttu-id="98583-132">Для каждой метки можно назначить свойство источника, выбрав в меню параметры.</span><span class="sxs-lookup"><span data-stu-id="98583-132">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="98583-133">Хотя этот шаг не является обязательным, наличие некоторых меток свойств повышает релевантность поиска и улучшает результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="98583-133">While this step isn't mandatory, having some property labels will improve the search relevance and ensure better search results for end users.</span></span>

## <a name="step-5-manage-schema"></a><span data-ttu-id="98583-134">Шаг 5. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="98583-134">Step 5: Manage schema</span></span>

<span data-ttu-id="98583-135">На экране **"Управление схемой"** можно изменить атрибуты схемы, связанные со свойствами. Возможные варианты: **Запрос,** **Поиск,** Извлечение и **уточнение.** </span><span class="sxs-lookup"><span data-stu-id="98583-135">On the **Manage Schema** screen, you can change the schema attributes associated with the properties, the options are **Query**, **Search**, **Retrieve**, and **Refine**.</span></span> <span data-ttu-id="98583-136">Вы также можете добавить необязательные псевдонимы и выбрать **свойство Content.**</span><span class="sxs-lookup"><span data-stu-id="98583-136">You also can add optional aliases, and choose the **Content** property.</span></span>

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="98583-137">Шаг 6. Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="98583-137">Step 6: Manage search permissions</span></span>

### <a name="azure-data-lake-gen-2"></a><span data-ttu-id="98583-138">Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="98583-138">Azure Data Lake Gen 2</span></span>

<span data-ttu-id="98583-139">Вы можете выбрать использование списков управления доступом (ALS) из учетной записи хранилища [Azure Data Lake поколения 2.](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)</span><span class="sxs-lookup"><span data-stu-id="98583-139">You can choose to ingest the Access Control Lists (ACLs) from your [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="98583-140">Когда эти разрешения поиска настроены, контент поиска обрезается на основе разрешений пользователя, выписав его в [Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/)</span><span class="sxs-lookup"><span data-stu-id="98583-140">When these search permissions are set, search content is trimmed based on the permissions of the user signed in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/).</span></span> <span data-ttu-id="98583-141">Кроме того, вы можете сделать все содержимое, индексироваться из учетной записи хранения, видимым всем в организации.</span><span class="sxs-lookup"><span data-stu-id="98583-141">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="98583-142">В этом случае все в вашей организации будут иметь доступ ко всем данным в вашей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="98583-142">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>

<span data-ttu-id="98583-143">Соединитель Azure Data Lake Storage Gen2 Graph поддерживает разрешения **поиска,** видимые всем или только людям с доступом к **этому источнику данных.**</span><span class="sxs-lookup"><span data-stu-id="98583-143">The Azure Data Lake Storage Gen2 Graph connector supports search permissions visible to **Everyone**, or **Only people with access to this data source**.</span></span> <span data-ttu-id="98583-144">Индексные данные, которые появляются в результатах поиска, могут быть видны пользователям в организации, которые имеют доступ к каждому элементу.</span><span class="sxs-lookup"><span data-stu-id="98583-144">Indexed data that appears in the search results could be visible to users in the organization who have access to each item.</span></span>

### <a name="azure-blob-storage"></a><span data-ttu-id="98583-145">Хранилище BLOB-объектов Azure</span><span class="sxs-lookup"><span data-stu-id="98583-145">Azure Blob Storage</span></span>

<span data-ttu-id="98583-146">Для подключения к хранилищу [BLOB-данных Azure](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)весь контент, индексируемый из настроенного источника, виден всем в организации.</span><span class="sxs-lookup"><span data-stu-id="98583-146">For a connection to [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction), all the content indexed from the configured source is visible to everyone in your organization.</span></span> <span data-ttu-id="98583-147">Списки управления доступом не поддерживаются на уровне BLOB-хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="98583-147">Access control lists aren't supported at Blob level in Azure Blob Storage.</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="98583-148">Шаг 7. Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="98583-148">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="98583-149">На экране **"Параметры обновления"** можно установить интервал добавоального обхода контента и интервал полного обхода.</span><span class="sxs-lookup"><span data-stu-id="98583-149">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="98583-150">По умолчанию интервалы для соединителя хранилища azure Data Lake Gen2 равны 15 минутам для добавального обхода контента и одной неделе для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="98583-150">The default intervals for the Azure Data Lake Storage Gen2 connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="98583-151">Шаг 8. Проверка подключения</span><span class="sxs-lookup"><span data-stu-id="98583-151">Step 8: Review connection</span></span>

<span data-ttu-id="98583-152">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="98583-152">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="98583-153">Ограничения</span><span class="sxs-lookup"><span data-stu-id="98583-153">Limitations</span></span>

<span data-ttu-id="98583-154">Опубликованное подключение для хранилища BLOB-хранилищ Azure невозможно перенастроить для источника Хранилища данных Azure Data Lake Gen2 и наоборот.</span><span class="sxs-lookup"><span data-stu-id="98583-154">A published connection for Azure Blob Storage cannot be reconfigured for Azure Data Lake Storage Gen2 source and the other way around.</span></span> <span data-ttu-id="98583-155">В таких сценариях рекомендуется настроить новое подключение.</span><span class="sxs-lookup"><span data-stu-id="98583-155">In such scenarios, it's recommended to configure a new connection.</span></span>

<span data-ttu-id="98583-156">Кроме того, размер файлов должен быть не менее 4 МБ для обхода.</span><span class="sxs-lookup"><span data-stu-id="98583-156">Also, the size of the files needs to be 4 MB or less for it to be crawled.</span></span> <span data-ttu-id="98583-157">Поддерживаемые в настоящее время типы файлов:</span><span class="sxs-lookup"><span data-stu-id="98583-157">File types currently supported are:</span></span>

* <span data-ttu-id="98583-158">Word (docx, DOCM, DOTX, DOTM)</span><span class="sxs-lookup"><span data-stu-id="98583-158">Word (docx, .docm, .dotx, .dotm)</span></span>
* <span data-ttu-id="98583-159">PowerPoint (PPTM, PPTX, POTM, POTX, PPAM, PPSM, PPSX)</span><span class="sxs-lookup"><span data-stu-id="98583-159">PowerPoint (.pptm, .pptx, .potm, .potx, .ppam, .ppsm, .ppsx)</span></span>
* <span data-ttu-id="98583-160">Excel (XLSX, XLSM)</span><span class="sxs-lookup"><span data-stu-id="98583-160">Excel (.xlsx, .xlsm)</span></span>
* <span data-ttu-id="98583-161">Устаревшие форматы Office (DOC, DOT и т. д.)</span><span class="sxs-lookup"><span data-stu-id="98583-161">Legacy Office formats (.doc, .dot, etc.)</span></span>
* <span data-ttu-id="98583-162">Текст (TXT)</span><span class="sxs-lookup"><span data-stu-id="98583-162">Text (.txt)</span></span>
* <span data-ttu-id="98583-163">HTML</span><span class="sxs-lookup"><span data-stu-id="98583-163">HTML</span></span>
* <span data-ttu-id="98583-164">PDF</span><span class="sxs-lookup"><span data-stu-id="98583-164">PDF</span></span>

<span data-ttu-id="98583-165">Двоичные файлы, такие как изображения (JPG, BMP и т. д.), не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="98583-165">Binary files like images (.jpg, .bmp, etc.) are not supported.</span></span> <span data-ttu-id="98583-166">Например, если DOCX-файл содержит только изображения, его можно пропустить, так как он не возвращает никакого содержимого.</span><span class="sxs-lookup"><span data-stu-id="98583-166">For example, if a .docx file contains only images, it might be skipped because it didn't return any content.</span></span>
