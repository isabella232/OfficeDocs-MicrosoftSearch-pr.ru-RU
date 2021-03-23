---
title: Соединитель Azure Data Lake Graph для microsoft Search
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
description: Настройка соединиттеля Azure Data Lake Storage Gen2 Graph для microsoft Search
ms.openlocfilehash: 37a035b3de9dc217f885f193992d1e74a675fb35
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031326"
---
<!---Previous ms.author: monaray --->

# <a name="azure-data-lake-storage-gen2-graph-connector"></a><span data-ttu-id="3d47f-103">Разъем Azure Data Lake Storage Gen2 Graph</span><span class="sxs-lookup"><span data-stu-id="3d47f-103">Azure Data Lake Storage Gen2 Graph connector</span></span>

<span data-ttu-id="3d47f-104">Соединитель Azure Data Lake Storage Gen2 Graph позволяет пользователям в вашей организации искать файлы, хранимые в учетных записях хранения данных [Azure Blob](/azure/storage/blobs/storage-blobs-introduction) и [Azure Data Lake Gen 2.](/azure/storage/blobs/data-lake-storage-introduction)</span><span class="sxs-lookup"><span data-stu-id="3d47f-104">The Azure Data Lake Storage Gen2 Graph connector allows users in your organization to search for files stored in [Azure Blob Storage](/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](/azure/storage/blobs/data-lake-storage-introduction) accounts.</span></span>

> [!NOTE]
> <span data-ttu-id="3d47f-105">Ознакомьтесь [**со статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общие инструкции по настройке соединитений Graph.</span><span class="sxs-lookup"><span data-stu-id="3d47f-105">Read the [**Setup your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="3d47f-106">Эта статья для всех, кто настраивает, запускает и контролирует соединитель Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="3d47f-106">This article is for anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="3d47f-107">Он дополняет общий процесс установки и показывает инструкции, которые применяются только для соединиттеля Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="3d47f-107">It supplements the general setup process, and shows instructions that apply only for the Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="3d47f-108">В этой статье также содержатся сведения об [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="3d47f-108">This article also includes information about [Limitations](#limitations).</span></span>

<span data-ttu-id="3d47f-109">В этой статье мы используем *Azure Storage* в качестве общего термина для хранения данных [Azure Blob и](/azure/storage/blobs/storage-blobs-introduction) Azure Data Lake Gen [2 Storage.](/azure/storage/blobs/data-lake-storage-introduction)</span><span class="sxs-lookup"><span data-stu-id="3d47f-109">In the article, we use *Azure Storage* as a generic term for [Azure Blob Storage](/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](/azure/storage/blobs/data-lake-storage-introduction).</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="3d47f-110">Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3d47f-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="3d47f-111">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="3d47f-111">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="3d47f-112">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="3d47f-112">Step 2: Name the connection</span></span>

<span data-ttu-id="3d47f-113">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="3d47f-113">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="3d47f-114">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="3d47f-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="3d47f-115">Введите первичную строку подключения к хранилищам.</span><span class="sxs-lookup"><span data-stu-id="3d47f-115">Enter your Primary storage connection String.</span></span> <span data-ttu-id="3d47f-116">Эта строка необходима для доступа к учетной записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="3d47f-116">This string is required to allow access to your storage account.</span></span> <span data-ttu-id="3d47f-117">Чтобы найти строку подключения, перейдите на портал [Azure](https://ms.portal.azure.com/#home) и перейдите в раздел **Ключи** соответствующей учетной записи azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3d47f-117">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of your relevant Azure Storage account.</span></span>

<span data-ttu-id="3d47f-118">Если вы предпочитаете не предоставлять **AccountKey** (параметр в строке первичного подключения к хранилищам), предоставить доступ к нашей службе соединители графа для следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="3d47f-118">If you prefer not to provide the **AccountKey** (a parameter in the primary storage connection string), grant access to our Graph Connectors Service for the following roles:</span></span>

* <span data-ttu-id="3d47f-119">Считыватель данных Blob хранилища</span><span class="sxs-lookup"><span data-stu-id="3d47f-119">Storage Blob Data Reader</span></span>
* <span data-ttu-id="3d47f-120">Вкладчик данных очереди хранения</span><span class="sxs-lookup"><span data-stu-id="3d47f-120">Storage Queue Data Contributor</span></span>
* <span data-ttu-id="3d47f-121">Делегатор Blob хранения</span><span class="sxs-lookup"><span data-stu-id="3d47f-121">Storage Blob Delegator</span></span>

<span data-ttu-id="3d47f-122">Перейдите на **вкладку Управление** доступом учетной записи Azure Storage и следуйте инструкциям, чтобы предоставить доступ к следующему приложению:</span><span class="sxs-lookup"><span data-stu-id="3d47f-122">Navigate to the **Access Control** tab of your Azure Storage account, and follow the instructions there to grant access to the following app:</span></span>

* <span data-ttu-id="3d47f-123">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="3d47f-123">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="3d47f-124">**Имя первого участника приложения:** Служба соединители графиков</span><span class="sxs-lookup"><span data-stu-id="3d47f-124">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="3d47f-125">Учетная запись хранилища и уведомления очереди (необязательный)</span><span class="sxs-lookup"><span data-stu-id="3d47f-125">Storage account and queue notifications (Optional)</span></span>

<span data-ttu-id="3d47f-126">Поддержка обработки изменений в режиме реального времени в службе соединители графа может быть добавлена в будущем.</span><span class="sxs-lookup"><span data-stu-id="3d47f-126">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="3d47f-127">В этом случае мы будем отслеживать уведомления об изменении хранилища Azure, хранимые в очереди.</span><span class="sxs-lookup"><span data-stu-id="3d47f-127">In that case, we'll monitor Azure Storage change notifications stored in a queue.</span></span> <span data-ttu-id="3d47f-128">Вам потребуется создать очередь в той же учетной записи, что и учетная запись Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3d47f-128">You'll need to create a queue in the same account as your Azure Storage account.</span></span>

<span data-ttu-id="3d47f-129">После создания очереди перейдите на вкладку **События** на странице очереди, чтобы настроить подписку **на события.**</span><span class="sxs-lookup"><span data-stu-id="3d47f-129">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="3d47f-130">Выберите все события Blob, которые получит очередь, и подключите очередь к учетной записи Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3d47f-130">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Storage account.</span></span>

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="3d47f-131">Шаг 4. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="3d47f-131">Step 4: Assign property labels</span></span>

<span data-ttu-id="3d47f-132">Вы можете назначить свойству источника для каждой метки, выбрав из меню параметры.</span><span class="sxs-lookup"><span data-stu-id="3d47f-132">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="3d47f-133">Хотя этот шаг не является обязательным, наличие некоторых меток свойств улучшит релевантность поиска и обеспечит лучшие результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3d47f-133">While this step isn't mandatory, having some property labels will improve the search relevance and ensure better search results for end users.</span></span>

## <a name="step-5-manage-schema"></a><span data-ttu-id="3d47f-134">Шаг 5. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="3d47f-134">Step 5: Manage schema</span></span>

<span data-ttu-id="3d47f-135">На экране **Управление схемой** можно изменить атрибуты схемы, связанные с свойствами, параметры **: Запрос,** **Поиск,** **Извлечение** и **Уточнение.**</span><span class="sxs-lookup"><span data-stu-id="3d47f-135">On the **Manage Schema** screen, you can change the schema attributes associated with the properties, the options are **Query**, **Search**, **Retrieve**, and **Refine**.</span></span> <span data-ttu-id="3d47f-136">Кроме того, можно добавить необязательные псевдонимы и выбрать **свойство Content.**</span><span class="sxs-lookup"><span data-stu-id="3d47f-136">You also can add optional aliases, and choose the **Content** property.</span></span>

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="3d47f-137">Шаг 6. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="3d47f-137">Step 6: Manage search permissions</span></span>

### <a name="azure-data-lake-gen-2"></a><span data-ttu-id="3d47f-138">Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="3d47f-138">Azure Data Lake Gen 2</span></span>

<span data-ttu-id="3d47f-139">Вы можете выбрать, чтобы гнать списки управления доступом (ACLs) из учетной записи [хранения данных Azure Data Lake Gen 2.](/azure/storage/blobs/data-lake-storage-introduction)</span><span class="sxs-lookup"><span data-stu-id="3d47f-139">You can choose to ingest the Access Control Lists (ACLs) from your [Azure Data Lake Gen 2 Storage](/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="3d47f-140">При наборе этих разрешений поиска содержимое поиска обрезается на основе разрешений пользователя, подписанного в [Azure Active Directory.](/azure/active-directory/)</span><span class="sxs-lookup"><span data-stu-id="3d47f-140">When these search permissions are set, search content is trimmed based on the permissions of the user signed in [Azure Active Directory](/azure/active-directory/).</span></span> <span data-ttu-id="3d47f-141">Кроме того, вы можете сделать все содержимое, индексироваться из учетной записи хранилища, видимым для всех в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="3d47f-141">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="3d47f-142">В этом случае все в вашей организации будут иметь доступ ко всем данным в учетной записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="3d47f-142">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>

<span data-ttu-id="3d47f-143">Соединитель Azure Data Lake Storage Gen2 Graph поддерживает разрешения на поиск, видимые всем или только людям с доступом **к этому источнику данных.**</span><span class="sxs-lookup"><span data-stu-id="3d47f-143">The Azure Data Lake Storage Gen2 Graph connector supports search permissions visible to **Everyone**, or **Only people with access to this data source**.</span></span> <span data-ttu-id="3d47f-144">Индексные данные, которые появляются в результатах поиска, могут быть видны пользователям в организации, которые имеют доступ к каждому элементу.</span><span class="sxs-lookup"><span data-stu-id="3d47f-144">Indexed data that appears in the search results could be visible to users in the organization who have access to each item.</span></span>

### <a name="azure-blob-storage"></a><span data-ttu-id="3d47f-145">Хранилище BLOB-объектов Azure</span><span class="sxs-lookup"><span data-stu-id="3d47f-145">Azure Blob Storage</span></span>

<span data-ttu-id="3d47f-146">Для подключения к [хранилище blob Azure](/azure/storage/blobs/storage-blobs-introduction)все содержимое, индексируемые из настроенного источника, видны всем в организации.</span><span class="sxs-lookup"><span data-stu-id="3d47f-146">For a connection to [Azure Blob Storage](/azure/storage/blobs/storage-blobs-introduction), all the content indexed from the configured source is visible to everyone in your organization.</span></span> <span data-ttu-id="3d47f-147">Списки управления доступом не поддерживаются на уровне Blob в хранилище Azure Blob.</span><span class="sxs-lookup"><span data-stu-id="3d47f-147">Access control lists aren't supported at Blob level in Azure Blob Storage.</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="3d47f-148">Шаг 7. Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="3d47f-148">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="3d47f-149">На экране **Параметры обновления** можно установить интервал инкрементного обхода и полный интервал обхода.</span><span class="sxs-lookup"><span data-stu-id="3d47f-149">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="3d47f-150">Интервалы интервалов для соединиттеля Хранения данных Azure Lake Gen2 для инкрементного обхода составляет 15 минут и одна неделя для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="3d47f-150">The default intervals for the Azure Data Lake Storage Gen2 connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="3d47f-151">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="3d47f-151">Step 8: Review connection</span></span>

<span data-ttu-id="3d47f-152">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="3d47f-152">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="3d47f-153">Ограничения</span><span class="sxs-lookup"><span data-stu-id="3d47f-153">Limitations</span></span>

<span data-ttu-id="3d47f-154">Опубликованное подключение для хранилища Blob Azure не может быть перенастройка для источника хранения данных Azure Data Lake Gen2 и наоборот.</span><span class="sxs-lookup"><span data-stu-id="3d47f-154">A published connection for Azure Blob Storage cannot be reconfigured for Azure Data Lake Storage Gen2 source and the other way around.</span></span> <span data-ttu-id="3d47f-155">В таких сценариях рекомендуется настроить новое подключение.</span><span class="sxs-lookup"><span data-stu-id="3d47f-155">In such scenarios, it's recommended to configure a new connection.</span></span>

<span data-ttu-id="3d47f-156">Кроме того, размер файлов должен быть 4 МБ или меньше для обхода.</span><span class="sxs-lookup"><span data-stu-id="3d47f-156">Also, the size of the files needs to be 4 MB or less for it to be crawled.</span></span> <span data-ttu-id="3d47f-157">В настоящее время поддерживаемые типы файлов:</span><span class="sxs-lookup"><span data-stu-id="3d47f-157">File types currently supported are:</span></span>

* <span data-ttu-id="3d47f-158">Word (docx, .docm, .dotx, .dotm)</span><span class="sxs-lookup"><span data-stu-id="3d47f-158">Word (docx, .docm, .dotx, .dotm)</span></span>
* <span data-ttu-id="3d47f-159">PowerPoint (.pptm, .pptx, .potm, .potx, .ppam, .ppsm, .ppsx)</span><span class="sxs-lookup"><span data-stu-id="3d47f-159">PowerPoint (.pptm, .pptx, .potm, .potx, .ppam, .ppsm, .ppsx)</span></span>
* <span data-ttu-id="3d47f-160">Excel (.xlsx, .xlsm)</span><span class="sxs-lookup"><span data-stu-id="3d47f-160">Excel (.xlsx, .xlsm)</span></span>
* <span data-ttu-id="3d47f-161">Устаревшие форматы Office (.doc, .dot и т.д.)</span><span class="sxs-lookup"><span data-stu-id="3d47f-161">Legacy Office formats (.doc, .dot, etc.)</span></span>
* <span data-ttu-id="3d47f-162">Текст (.txt)</span><span class="sxs-lookup"><span data-stu-id="3d47f-162">Text (.txt)</span></span>
* <span data-ttu-id="3d47f-163">HTML</span><span class="sxs-lookup"><span data-stu-id="3d47f-163">HTML</span></span>
* <span data-ttu-id="3d47f-164">PDF</span><span class="sxs-lookup"><span data-stu-id="3d47f-164">PDF</span></span>

<span data-ttu-id="3d47f-165">Двоичные файлы, такие как изображения (.jpg, bmp и т.д.), не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3d47f-165">Binary files like images (.jpg, .bmp, etc.) are not supported.</span></span> <span data-ttu-id="3d47f-166">Например, если файл .docx содержит только изображения, его можно пропустить, так как он не возвращает контент.</span><span class="sxs-lookup"><span data-stu-id="3d47f-166">For example, if a .docx file contains only images, it might be skipped because it didn't return any content.</span></span>