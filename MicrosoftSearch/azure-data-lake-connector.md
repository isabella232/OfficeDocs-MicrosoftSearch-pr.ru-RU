---
title: Azure Data Lake Connector для поиска Майкрософт
ms.author: mounika.narayanan
author: monaray
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединителя Gen2 для Azure Data Lake Storage для поиска Майкрософт
ms.openlocfilehash: 392960a5f7e6c93442ac7e1f60245217e194b42b
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626474"
---
# <a name="azure-data-lake-storage-gen2-connector-for-microsoft-search"></a><span data-ttu-id="83901-103">Соединитель Gen2 для Azure Data Lake Storage для поиска Майкрософт</span><span class="sxs-lookup"><span data-stu-id="83901-103">Azure Data Lake Storage Gen2 connector for Microsoft Search</span></span>

<span data-ttu-id="83901-104">С помощью соединителя [Gen2 Azure Data Lake Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) пользователи в вашей организации могут искать файлы и их содержимое.</span><span class="sxs-lookup"><span data-stu-id="83901-104">With the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector, users in your organization can search for files and their content.</span></span> <span data-ttu-id="83901-105">Этот соединитель получает доступ к данным, хранящимся в контейнерах больших двоичных объектов Azure и папках с включенной поддержкой иерархии, в учетной записи Azure Data Lake Storage поколения 2.</span><span class="sxs-lookup"><span data-stu-id="83901-105">This connector accesses data stored in Azure Blob containers and hierarchy-enabled folders within an Azure Data Lake Storage Gen 2 account.</span></span>

<span data-ttu-id="83901-106">Эта статья предназначена для администраторов [Microsoft 365](https://www.microsoft.com/microsoft-365) или пользователей, которые настраивают, запускают и отслеживают соединитель Gen2 для Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="83901-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="83901-107">В этой статье объясняется, как настроить возможности соединителя и соединителя, ограничения и способы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="83901-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="83901-108">Подключение к источнику данных</span><span class="sxs-lookup"><span data-stu-id="83901-108">Connect to a data source</span></span>

### <a name="primary-storage-connection-string"></a><span data-ttu-id="83901-109">Строка подключения к основному хранилищу</span><span class="sxs-lookup"><span data-stu-id="83901-109">Primary storage connection string</span></span> 
<span data-ttu-id="83901-110">На экране **Проверка подлинности и настройка** введите строку подключения к основному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="83901-110">On the **Authentication and config** screen, provide the Primary Storage Connection String.</span></span> <span data-ttu-id="83901-111">Эта строка необходима для предоставления доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="83901-111">That string is required to allow access to your storage account.</span></span> <span data-ttu-id="83901-112">Чтобы найти строку подключения, перейдите на [портал Azure](https://ms.portal.azure.com/#home) и перейдите к разделу " **ключи** " учетной записи [Gen2 Azure Data Lake Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) .</span><span class="sxs-lookup"><span data-stu-id="83901-112">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="83901-113">Скопируйте и вставьте строку подключения в соответствующее поле на экране.</span><span class="sxs-lookup"><span data-stu-id="83901-113">Copy and paste the connection string in the appropriate field on the screen.</span></span>

<span data-ttu-id="83901-114">Если вы не хотите предоставлять **AccountKey** (параметр в основной строке подключения хранилища), необходимо предоставить доступ на чтение к службе соединителей Graph.</span><span class="sxs-lookup"><span data-stu-id="83901-114">If you don't want to provide the **AccountKey** (a parameter in the primary storage connection string), you have to grant read access to our Graph Connectors Service.</span></span> <span data-ttu-id="83901-115">На вкладке **Управление доступом** в учетной записи Gen2 Azure Data Lake Storage следуйте инструкциям на этой странице, чтобы предоставить доступ к следующему приложению:</span><span class="sxs-lookup"><span data-stu-id="83901-115">In the **Access Control** tab of your Azure Data Lake Storage Gen2 account, follow the instructions on that page to grant access to the following app:</span></span>
* <span data-ttu-id="83901-116">**Идентификатор приложения первой стороны:** 56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="83901-116">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="83901-117">**Имя приложения первой стороны:** Служба соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="83901-117">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="83901-118">Учетная запись хранения и уведомления об очередях (необязательно)</span><span class="sxs-lookup"><span data-stu-id="83901-118">Storage account and queue notifications (Optional)</span></span>
<span data-ttu-id="83901-119">Поддержка обработки изменений в режиме реального времени в службе соединителей Graph может быть добавлена в будущем.</span><span class="sxs-lookup"><span data-stu-id="83901-119">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="83901-120">В этом случае мы отслеживаем уведомления об изменениях [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) , хранящиеся в очереди.</span><span class="sxs-lookup"><span data-stu-id="83901-120">In that case, we'll monitor [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) change notifications stored in a queue.</span></span> <span data-ttu-id="83901-121">Вам потребуется создать очередь в той же учетной записи, в которой находится Azure Data Lake Storage Gen2 или в другой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="83901-121">You'll need to create a queue in the same account as your Azure Data Lake Storage Gen2 or in another storage account.</span></span>

<span data-ttu-id="83901-122">После создания очереди перейдите на вкладку **события** на странице очередь, чтобы настроить **подписку на события**.</span><span class="sxs-lookup"><span data-stu-id="83901-122">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="83901-123">Выберите все события больших двоичных объектов, которые будут получены в очереди, и подключите ее к учетной записи Gen2 Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="83901-123">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Data Lake Storage Gen2 account.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="83901-124">Управление схемой поиска</span><span class="sxs-lookup"><span data-stu-id="83901-124">Manage the search schema</span></span>
<span data-ttu-id="83901-125">На экране **Управление схемой** можно изменить атрибуты схемы (возможность**запроса**, **Поиск**и возможность **извлечения**), связанные с управляемыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="83901-125">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, and **retrievable**) associated with the managed properties.</span></span> <span data-ttu-id="83901-126">Эти атрибуты управляемых свойств — это данные, индексируемые из учетной записи [Gen2 Azure Data Lake Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) .</span><span class="sxs-lookup"><span data-stu-id="83901-126">These managed property attributes are data indexed from your [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="83901-127">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="83901-127">Manage search permissions</span></span>
<span data-ttu-id="83901-128">На экране " **Управление разрешениями поиска** " можно выбрать, следует использовать для учетной записи хранения списки управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="83901-128">On the **Manage search permissions** screen, you can choose to ingest the Access Control Lists (ACLs) from your storage account.</span></span> <span data-ttu-id="83901-129">При задании этих разрешений поиска усечение контента выполняется в соответствии с разрешениями, назначенными вошедшего пользователя [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) , в котором выполняется поиск контента.</span><span class="sxs-lookup"><span data-stu-id="83901-129">When these search permissions are set, search content is trimmed based on the permissions assigned to the signed-in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) user searching the content.</span></span> <span data-ttu-id="83901-130">Кроме того, вы можете сделать так, чтобы весь контент, индексируемый из учетной записи хранения, был виден всем пользователям в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="83901-130">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="83901-131">В этом случае всем пользователям в Организации будет доступен доступ ко всем данным в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="83901-131">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>
 
## <a name="set-the-refresh-schedule"></a><span data-ttu-id="83901-132">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="83901-132">Set the refresh schedule</span></span>
<span data-ttu-id="83901-133">На экране **Параметры обновления** можно задать интервал добавочного обхода контента и интервал полного обхода контента.</span><span class="sxs-lookup"><span data-stu-id="83901-133">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="83901-134">Интервалы по умолчанию для соединителя [Gen2 Azure Data Lake Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) задаются 15 минут для добавочного обхода и на одну неделю для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="83901-134">The default intervals for the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>
 
## <a name="limitations"></a><span data-ttu-id="83901-135">Ограничения</span><span class="sxs-lookup"><span data-stu-id="83901-135">Limitations</span></span>
<span data-ttu-id="83901-136">В настоящее время доступ к [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) предоставляется только в Центральной территории США, Западная Центральная часть США, для Канады, Восточной США, Восточной Азии, Северной Европы, восток США, Юго-Восточной Азии, Западная Европа, Запад США, Восток, Япония, Западная US2 и Южная Бразилия.</span><span class="sxs-lookup"><span data-stu-id="83901-136">Currently, [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) Multi-Protocol Access is available only in the Central US, West Central US, Canada Central, East US, East Asia, North Europe, East US2, South East Asia, West Europe, West US, Australia East, Japan East, West US2, and Brazil South.</span></span>

<span data-ttu-id="83901-137">За обновлениями и дополнительными сведениями можно ознакомиться [в статье поддержка нескольких протоколов в Azure Data Lake Storage (Предварительная версия)](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access).</span><span class="sxs-lookup"><span data-stu-id="83901-137">For updates and more information, see  [Multi-protocol access on Azure Data Lake Storage (preview)](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access).</span></span>

