---
title: Управление соединитетелями Microsoft Graph для Поиска (Майкрософт)
ms.author: monaray
author: monaray97
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Управление соединитетелями Microsoft Graph для Поиска (Майкрософт).
ms.openlocfilehash: 5258f26a5c97be4ee9f90c7a8b2b9bb8fec447bc
ms.sourcegitcommit: 39bf9f0db7f9bff2ab82c99a059b0ddcf1c98f5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/19/2021
ms.locfileid: "49905933"
---
<!-- markdownlint-disable no-inline-html -->

# <a name="monitor-your-connections"></a><span data-ttu-id="fd32a-103">Отслеживание подключений</span><span class="sxs-lookup"><span data-stu-id="fd32a-103">Monitor your connections</span></span>

<span data-ttu-id="fd32a-104">Для доступа к соединитетелям и управления ими необходимо назначить администратора поиска для клиента.</span><span class="sxs-lookup"><span data-stu-id="fd32a-104">To access and manage your connectors, you must be designated as a search administrator for your tenant.</span></span> <span data-ttu-id="fd32a-105">Обратитесь к администратору клиента, чтобы у вас была роль администратора поиска.</span><span class="sxs-lookup"><span data-stu-id="fd32a-105">Contact your tenant administrator to provision you for the search administrator role.</span></span>

## <a name="connection-operations"></a><span data-ttu-id="fd32a-106">Операции подключения</span><span class="sxs-lookup"><span data-stu-id="fd32a-106">Connection Operations</span></span>

<span data-ttu-id="fd32a-107">Перейдите на [вкладку "Соединители"](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в Центре администрирования [Microsoft 365.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="fd32a-107">Navigate to the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="fd32a-108">Для каждого типа соединители Центр администрирования [Microsoft 365](https://admin.microsoft.com) поддерживает операции, показанные в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="fd32a-108">For each connector type, the [Microsoft 365 admin center](https://admin.microsoft.com) supports the operations shown in the following table:</span></span>

<span data-ttu-id="fd32a-109">Операция</span><span class="sxs-lookup"><span data-stu-id="fd32a-109">Operation</span></span> | <span data-ttu-id="fd32a-110">Соединители, построенные корпорацией Майкрософт</span><span class="sxs-lookup"><span data-stu-id="fd32a-110">Microsoft-built connector</span></span> | <span data-ttu-id="fd32a-111">Партнерский или настраиваемый соединители</span><span class="sxs-lookup"><span data-stu-id="fd32a-111">Partner or custom-built connector</span></span>
--- | --- | ---
<span data-ttu-id="fd32a-112">Добавление подключения</span><span class="sxs-lookup"><span data-stu-id="fd32a-112">Add a connection</span></span> | :heavy_check_mark: <span data-ttu-id="fd32a-113">(См. ["Настройка соединители, построенного корпорацией Майкрософт")](configure-connector.md)</span><span class="sxs-lookup"><span data-stu-id="fd32a-113">(See [Configure your Microsoft-built connector](configure-connector.md))</span></span> | :x: <span data-ttu-id="fd32a-114">(Обратитесь к партнеру или администратору настраиваемого соединитела)</span><span class="sxs-lookup"><span data-stu-id="fd32a-114">(Refer to your partner or custom-built connector admin UX)</span></span>
<span data-ttu-id="fd32a-115">Удаление подключения</span><span class="sxs-lookup"><span data-stu-id="fd32a-115">Delete a connection</span></span> | :heavy_check_mark: | :heavy_check_mark:
<span data-ttu-id="fd32a-118">Изменение опубликованного подключения</span><span class="sxs-lookup"><span data-stu-id="fd32a-118">Edit a published connection</span></span> | :heavy_check_mark: <span data-ttu-id="fd32a-119">Имя</span><span class="sxs-lookup"><span data-stu-id="fd32a-119">Name</span></span><br></br> :heavy_check_mark: <span data-ttu-id="fd32a-120">описание</span><span class="sxs-lookup"><span data-stu-id="fd32a-120">Description</span></span><br></br> :heavy_check_mark: <span data-ttu-id="fd32a-121">учетные данные проверки подлинности для внешнего источника данных</span><span class="sxs-lookup"><span data-stu-id="fd32a-121">Authentication credentials for your external data source</span></span><br></br> :heavy_check_mark: <span data-ttu-id="fd32a-122">учетные данные шлюза для локального источника данных</span><span class="sxs-lookup"><span data-stu-id="fd32a-122">Gateway credentials for your on-premises data source</span></span><br></br> :heavy_check_mark: <span data-ttu-id="fd32a-123">обновление расписания</span><span class="sxs-lookup"><span data-stu-id="fd32a-123">Refresh schedule</span></span><br></br> | :heavy_check_mark: <span data-ttu-id="fd32a-124">Имя</span><span class="sxs-lookup"><span data-stu-id="fd32a-124">Name</span></span><br></br> :heavy_check_mark: <span data-ttu-id="fd32a-125">описание</span><span class="sxs-lookup"><span data-stu-id="fd32a-125">Description</span></span>
<span data-ttu-id="fd32a-126">Изменение черновика подключения</span><span class="sxs-lookup"><span data-stu-id="fd32a-126">Edit a draft connection</span></span> | :heavy_check_mark: | :x:

## <a name="monitor-your-connection-status"></a><span data-ttu-id="fd32a-129">Отслеживание состояния подключения</span><span class="sxs-lookup"><span data-stu-id="fd32a-129">Monitor your connection status</span></span>

<span data-ttu-id="fd32a-130">После создания подключения количество обработанных элементов будет показано на вкладке **"Соединители"** на странице **Поиска (Майкрософт).**</span><span class="sxs-lookup"><span data-stu-id="fd32a-130">After you create a connection, the number of processed items shows on the **Connectors** tab on the **Microsoft Search** page.</span></span> <span data-ttu-id="fd32a-131">После успешного завершения начального полного обхода отображается ход выполнения периодических добавок обхода контента.</span><span class="sxs-lookup"><span data-stu-id="fd32a-131">After the initial full crawl completes successfully, the progress for periodic incremental crawls displays.</span></span> <span data-ttu-id="fd32a-132">На этой странице представлена информация о ежедневной работе соединители, а также обзор журналов и журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="fd32a-132">This page provides information about the connector's day-to-day operations and an overview of the logs and error history.</span></span>

<span data-ttu-id="fd32a-133">В столбце "Состояние" для каждого подключения покажут четыре состояния: </span><span class="sxs-lookup"><span data-stu-id="fd32a-133">Four states show up in the **Status** column against each connection:</span></span>

* <span data-ttu-id="fd32a-134">**Синхронизация.**</span><span class="sxs-lookup"><span data-stu-id="fd32a-134">**Syncing**.</span></span> <span data-ttu-id="fd32a-135">Соединители обхода данных из источника для индексации существующих элементов и внести любые обновления.</span><span class="sxs-lookup"><span data-stu-id="fd32a-135">The connector is crawling the data from the source to index the existing items and make any updates.</span></span>

* <span data-ttu-id="fd32a-136">**Включено:** подключение включено, и для него не запущен активный обход контента.</span><span class="sxs-lookup"><span data-stu-id="fd32a-136">**Enabled**: The connection is enabled, and there's no active crawl running against it.</span></span> <span data-ttu-id="fd32a-137">**Время последней синхронизации** указывает время последнего успешного обхода контента.</span><span class="sxs-lookup"><span data-stu-id="fd32a-137">**Last sync time** indicates when the last successful crawl happened.</span></span> <span data-ttu-id="fd32a-138">Подключение является таким же новым, как и время последней синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd32a-138">The connection is as fresh as the last sync time.</span></span>

* <span data-ttu-id="fd32a-139">**Приостановлено.**</span><span class="sxs-lookup"><span data-stu-id="fd32a-139">**Paused**.</span></span> <span data-ttu-id="fd32a-140">Обходы приостанавлиются администраторами с помощью параметра "Приостановка".</span><span class="sxs-lookup"><span data-stu-id="fd32a-140">The crawls are paused by the admins through the pause option.</span></span> <span data-ttu-id="fd32a-141">Следующий обход выполняется только при возобновлении вручную.</span><span class="sxs-lookup"><span data-stu-id="fd32a-141">The next crawl runs only when it's manually resumed.</span></span> <span data-ttu-id="fd32a-142">Однако данные из этого подключения по-прежнему будут искаться.</span><span class="sxs-lookup"><span data-stu-id="fd32a-142">However, the data from this connection continues to be searchable.</span></span>

* <span data-ttu-id="fd32a-143">**Сбой.**</span><span class="sxs-lookup"><span data-stu-id="fd32a-143">**Failed**.</span></span> <span data-ttu-id="fd32a-144">При под соединении был критический сбой.</span><span class="sxs-lookup"><span data-stu-id="fd32a-144">The connection had a critical failure.</span></span> <span data-ttu-id="fd32a-145">Эта ошибка требует ручного вмешательства.</span><span class="sxs-lookup"><span data-stu-id="fd32a-145">This error requires manual intervention.</span></span> <span data-ttu-id="fd32a-146">Администратор должен принять соответствующие меры в зависимости от показанного сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="fd32a-146">The admin needs to take appropriate action based on the error message shown.</span></span> <span data-ttu-id="fd32a-147">Данные, индексируемые до тех пор, пока не возникла ошибка, недоступны для поиска.</span><span class="sxs-lookup"><span data-stu-id="fd32a-147">Data that was indexed until the error occurred is searchable.</span></span>

## <a name="monitor-your-index-quota-utilization"></a><span data-ttu-id="fd32a-148">Отслеживание использования квоты индекса</span><span class="sxs-lookup"><span data-stu-id="fd32a-148">Monitor your index quota utilization</span></span>

<span data-ttu-id="fd32a-149">Доступная квота индекса и потребление отображаются на странице сайта соединителя.</span><span class="sxs-lookup"><span data-stu-id="fd32a-149">The available index quota and consumption is displayed on the connectors landing page.</span></span>

![План использования квоты индекса](media/quota_utilization.png)

>[!NOTE]
><span data-ttu-id="fd32a-151">В течение периода предварительного просмотра каждой организации, которая пытается проверить соединители Graph, была предоставлена бесплатная фиксированная квота до 2 миллионов элементов во всех подключениях.</span><span class="sxs-lookup"><span data-stu-id="fd32a-151">During the preview period, every organization trying out Graph connectors was provided a free fixed quota of up to 2 million items across all connections.</span></span> <span data-ttu-id="fd32a-152">Если соединители Graph доступны в общем доступе, срок действия бесплатной квоты истекает 1 февраля 2021 г. для организаций, которые использовали соединители Graph в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="fd32a-152">With Graph connectors being generally available, the free quota will expire on Feb 1st, 2021 for those organizations who have been using Graph connectors in preview.</span></span>
><span data-ttu-id="fd32a-153">Соединители Graph, построенные корпорацией Майкрософт, помеченные как ["Предварительная](connectors-preview.md) версия", не будут включены в общую квоту индекса список для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="fd32a-153">Microsoft-built Graph connectors labeled as ["Preview"](connectors-preview.md) will not be included in the total charged index quota for your organization.</span></span> <span data-ttu-id="fd32a-154">Однако он будет учитывать максимальное число из 10 подключений, которые можно настроить для организации, и максимальное число 7 миллионов элементов, которые организация может индексировать между подключениями; каждое подключение ограничено 700 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="fd32a-154">However, it will count towards the max number of 10 connections you can configure for your organization and the max number of 7 million items your organization can index across connections; each connection is limited 700,000 items.</span></span> 

<span data-ttu-id="fd32a-155">На панели использования квоты будут указаны различные состояния в зависимости от потребления квоты в организации:</span><span class="sxs-lookup"><span data-stu-id="fd32a-155">The quota utilization bar will indicate various states based on consumption of quota by your organization:</span></span>

<span data-ttu-id="fd32a-156">Состояние</span><span class="sxs-lookup"><span data-stu-id="fd32a-156">State</span></span> | <span data-ttu-id="fd32a-157">Потребление квот</span><span class="sxs-lookup"><span data-stu-id="fd32a-157">Quota consumption</span></span>
--- | ---
<span data-ttu-id="fd32a-158">Normal</span><span class="sxs-lookup"><span data-stu-id="fd32a-158">Normal</span></span> | <span data-ttu-id="fd32a-159">1-69%</span><span class="sxs-lookup"><span data-stu-id="fd32a-159">1-69%</span></span>
<span data-ttu-id="fd32a-160">Высокие</span><span class="sxs-lookup"><span data-stu-id="fd32a-160">High</span></span> | <span data-ttu-id="fd32a-161">70-89%</span><span class="sxs-lookup"><span data-stu-id="fd32a-161">70-89%</span></span>
<span data-ttu-id="fd32a-162">Критический</span><span class="sxs-lookup"><span data-stu-id="fd32a-162">Critical</span></span> | <span data-ttu-id="fd32a-163">90%-99%</span><span class="sxs-lookup"><span data-stu-id="fd32a-163">90%-99%</span></span>
<span data-ttu-id="fd32a-164">Full</span><span class="sxs-lookup"><span data-stu-id="fd32a-164">Full</span></span> | <span data-ttu-id="fd32a-165">100 %</span><span class="sxs-lookup"><span data-stu-id="fd32a-165">100%</span></span>

<span data-ttu-id="fd32a-166">Количество индексных элементов также будет отображаться для каждого подключения.</span><span class="sxs-lookup"><span data-stu-id="fd32a-166">The number of items indexed will also be displayed with each connection.</span></span> <span data-ttu-id="fd32a-167">Количество элементов, индексироваться по каждому подключению, вносит вклад в общую квоту, доступную для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="fd32a-167">The number of items indexed by each connection contributes to the total quota available for your organization.</span></span>

<span data-ttu-id="fd32a-168">При превышении квоты индекса для организации будут влиять все активные подключения, и эти подключения будут работать в превышенном **состоянии.**</span><span class="sxs-lookup"><span data-stu-id="fd32a-168">When index quota is exceeded for your organization, all active connections will be impacted, and those connections will operate in **limit exceeded** state.</span></span> <span data-ttu-id="fd32a-169">В этом состоянии активные подключения</span><span class="sxs-lookup"><span data-stu-id="fd32a-169">In this state, your active connections</span></span>  

* <span data-ttu-id="fd32a-170">Не сможет добавлять новые элементы.</span><span class="sxs-lookup"><span data-stu-id="fd32a-170">Will not be able to add new items.</span></span>

* <span data-ttu-id="fd32a-171">Сможет обновлять или удалять существующие элементы.</span><span class="sxs-lookup"><span data-stu-id="fd32a-171">Will be able to update or delete existing items.</span></span>

<span data-ttu-id="fd32a-172">Чтобы устранить эту проблему, можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="fd32a-172">To fix this, you can do any of the following:</span></span>

* <span data-ttu-id="fd32a-173">Узнайте, как приобрести квоту индекса для организации по требованиям [лицензирования и цене.](licensing.md)</span><span class="sxs-lookup"><span data-stu-id="fd32a-173">Learn how to purchase index quota for your organization at [Licensing requirements and pricing](licensing.md).</span></span>

* <span data-ttu-id="fd32a-174">Определите подключения, в которых слишком много содержимого, и обновим их, чтобы проиндексировать меньше элементов, чтобы уместить квоту.</span><span class="sxs-lookup"><span data-stu-id="fd32a-174">Identify connections which have too much content being ingested and update them to index fewer items to make room for quota.</span></span> <span data-ttu-id="fd32a-175">Чтобы обновить подключение, необходимо удалить и создать новое подключение с помощью нового фильтра ingestion, который обеспечивает меньшее количество элементов.</span><span class="sxs-lookup"><span data-stu-id="fd32a-175">To update the connection, you must delete and create a new connection with a new ingestion filter which brings in fewer items.</span></span>

* <span data-ttu-id="fd32a-176">Окончательное удаление одного или более подключений</span><span class="sxs-lookup"><span data-stu-id="fd32a-176">Permanently delete one or more connections</span></span>