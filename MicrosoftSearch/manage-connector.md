---
title: Управление соединитетелями Microsoft Graph для поиска Майкрософт
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
description: Управление соединиттелями Microsoft Graph для поиска Майкрософт.
ms.openlocfilehash: 488b6e9452e381f8fc64ad06c6f063aa170ca7f5
ms.sourcegitcommit: 3ed4d21510020045d25e8c5b7e168013d96c1b7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "50464043"
---
<!-- markdownlint-disable no-inline-html -->

# <a name="monitor-your-connections"></a><span data-ttu-id="c0e3c-103">Мониторинг подключений</span><span class="sxs-lookup"><span data-stu-id="c0e3c-103">Monitor your connections</span></span>

<span data-ttu-id="c0e3c-104">Чтобы получить доступ к соединитетелям и управлять ими, необходимо назначить вас администратором поиска для клиента.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-104">To access and manage your connectors, you must be designated as a search administrator for your tenant.</span></span> <span data-ttu-id="c0e3c-105">Обратитесь к администратору клиента для предоставления вам роли администратора поиска.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-105">Contact your tenant administrator to provision you for the search administrator role.</span></span>

## <a name="connection-operations"></a><span data-ttu-id="c0e3c-106">Операции подключения</span><span class="sxs-lookup"><span data-stu-id="c0e3c-106">Connection Operations</span></span>

<span data-ttu-id="c0e3c-107">Перейдите на [вкладку Соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в центре администрирования [Microsoft 365.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="c0e3c-107">Navigate to the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="c0e3c-108">Для каждого типа соединители центр администрирования [Microsoft 365](https://admin.microsoft.com) поддерживает операции, показанные в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="c0e3c-108">For each connector type, the [Microsoft 365 admin center](https://admin.microsoft.com) supports the operations shown in the following table:</span></span>

<span data-ttu-id="c0e3c-109">Operation</span><span class="sxs-lookup"><span data-stu-id="c0e3c-109">Operation</span></span> | <span data-ttu-id="c0e3c-110">Соединитетор, построенный корпорацией Майкрософт</span><span class="sxs-lookup"><span data-stu-id="c0e3c-110">Microsoft-built connector</span></span> | <span data-ttu-id="c0e3c-111">Соединитетелем партнера или настраиваемого подключения</span><span class="sxs-lookup"><span data-stu-id="c0e3c-111">Partner or custom-built connector</span></span>
--- | --- | ---
<span data-ttu-id="c0e3c-112">Добавление подключения</span><span class="sxs-lookup"><span data-stu-id="c0e3c-112">Add a connection</span></span> | :heavy_check_mark: <span data-ttu-id="c0e3c-113">(См. [настройка соединитетеля,](configure-connector.md)построенного Корпорацией Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c0e3c-113">(See [Configure your Microsoft-built connector](configure-connector.md))</span></span> | :x: <span data-ttu-id="c0e3c-114">(Обратитесь к партнеру или настраиваемой соединители администратора UX)</span><span class="sxs-lookup"><span data-stu-id="c0e3c-114">(Refer to your partner or custom-built connector admin UX)</span></span>
<span data-ttu-id="c0e3c-115">Удаление подключения</span><span class="sxs-lookup"><span data-stu-id="c0e3c-115">Delete a connection</span></span> | :heavy_check_mark: | :heavy_check_mark:
<span data-ttu-id="c0e3c-118">Изменение опубликованного подключения</span><span class="sxs-lookup"><span data-stu-id="c0e3c-118">Edit a published connection</span></span> | :heavy_check_mark: <span data-ttu-id="c0e3c-119">Имя</span><span class="sxs-lookup"><span data-stu-id="c0e3c-119">Name</span></span><br></br> :heavy_check_mark: <span data-ttu-id="c0e3c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c0e3c-120">Description</span></span><br></br> :heavy_check_mark: <span data-ttu-id="c0e3c-121">учетные данные проверки подлинности для внешнего источника данных</span><span class="sxs-lookup"><span data-stu-id="c0e3c-121">Authentication credentials for your external data source</span></span><br></br> :heavy_check_mark: <span data-ttu-id="c0e3c-122">учетные данные шлюза для локального источника данных</span><span class="sxs-lookup"><span data-stu-id="c0e3c-122">Gateway credentials for your on-premises data source</span></span><br></br> :heavy_check_mark: <span data-ttu-id="c0e3c-123">расписание обновления</span><span class="sxs-lookup"><span data-stu-id="c0e3c-123">Refresh schedule</span></span><br></br> | :heavy_check_mark: <span data-ttu-id="c0e3c-124">Имя</span><span class="sxs-lookup"><span data-stu-id="c0e3c-124">Name</span></span><br></br> :heavy_check_mark: <span data-ttu-id="c0e3c-125">Описание</span><span class="sxs-lookup"><span data-stu-id="c0e3c-125">Description</span></span>
<span data-ttu-id="c0e3c-126">Изменение подключения к проекту</span><span class="sxs-lookup"><span data-stu-id="c0e3c-126">Edit a draft connection</span></span> | :heavy_check_mark: | :x:

## <a name="monitor-your-connection-status"></a><span data-ttu-id="c0e3c-129">Мониторинг состояния подключения</span><span class="sxs-lookup"><span data-stu-id="c0e3c-129">Monitor your connection status</span></span>

<span data-ttu-id="c0e3c-130">После создания подключения количество обработанных элементов отображается на вкладке **Соединители** на странице **Microsoft Search.**</span><span class="sxs-lookup"><span data-stu-id="c0e3c-130">After you create a connection, the number of processed items shows on the **Connectors** tab on the **Microsoft Search** page.</span></span> <span data-ttu-id="c0e3c-131">После успешного завершения начального полного обхода отображается прогресс для периодического инкрементного обхода.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-131">After the initial full crawl completes successfully, the progress for periodic incremental crawls displays.</span></span> <span data-ttu-id="c0e3c-132">На этой странице представлена информация о ежедневной работе соединиттеля и обзор журналов и истории ошибок.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-132">This page provides information about the connector's day-to-day operations and an overview of the logs and error history.</span></span>

<span data-ttu-id="c0e3c-133">Четыре состояния показываются в столбце **Состояние** для каждого подключения:</span><span class="sxs-lookup"><span data-stu-id="c0e3c-133">Four states show up in the **Status** column against each connection:</span></span>

* <span data-ttu-id="c0e3c-134">**Синхронизация**.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-134">**Syncing**.</span></span> <span data-ttu-id="c0e3c-135">Соединители обхода данных из источника, чтобы индексировать существующие элементы и делать какие-либо обновления.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-135">The connector is crawling the data from the source to index the existing items and make any updates.</span></span>

* <span data-ttu-id="c0e3c-136">**Включено.** Подключение включено, и не существует активного обхода, запущенного против него.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-136">**Enabled**: The connection is enabled, and there's no active crawl running against it.</span></span> <span data-ttu-id="c0e3c-137">**Последнее время синхронизации** указывает, когда был последний успешный обход.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-137">**Last sync time** indicates when the last successful crawl happened.</span></span> <span data-ttu-id="c0e3c-138">Подключение свежо, как и время последней синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-138">The connection is as fresh as the last sync time.</span></span>

* <span data-ttu-id="c0e3c-139">**Приостановлено**.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-139">**Paused**.</span></span> <span data-ttu-id="c0e3c-140">Обходы приостановлены администраторами с помощью параметра паузы.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-140">The crawls are paused by the admins through the pause option.</span></span> <span data-ttu-id="c0e3c-141">Следующий обход выполняется только при возобновлении вручную.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-141">The next crawl runs only when it's manually resumed.</span></span> <span data-ttu-id="c0e3c-142">Однако данные из этого подключения по-прежнему можно искать.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-142">However, the data from this connection continues to be searchable.</span></span>

* <span data-ttu-id="c0e3c-143">**Не удалось**.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-143">**Failed**.</span></span> <span data-ttu-id="c0e3c-144">При подключении был критический сбой.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-144">The connection had a critical failure.</span></span> <span data-ttu-id="c0e3c-145">Эта ошибка требует ручного вмешательства.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-145">This error requires manual intervention.</span></span> <span data-ttu-id="c0e3c-146">Администратору необходимо принять соответствующие меры на основе показанного сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-146">The admin needs to take appropriate action based on the error message shown.</span></span> <span data-ttu-id="c0e3c-147">Данные, индексируемые до момента ошибки, можно найти.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-147">Data that was indexed until the error occurred is searchable.</span></span>

## <a name="monitor-your-index-quota-utilization"></a><span data-ttu-id="c0e3c-148">Мониторинг использования квот индекса</span><span class="sxs-lookup"><span data-stu-id="c0e3c-148">Monitor your index quota utilization</span></span>

<span data-ttu-id="c0e3c-149">Доступная квота индекса и потребление отображаются на странице посадки соединителов.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-149">The available index quota and consumption is displayed on the connectors landing page.</span></span>

![Планка использования квоты индекса](media/quota_utilization.png)

>[!NOTE]
><span data-ttu-id="c0e3c-151">В период предварительного просмотра каждая организация, пробуя соединители Graph, была предоставлена бесплатная фиксированная квота до 2 миллионов элементов во всех подключениях.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-151">During the preview period, every organization trying out Graph connectors was provided a free fixed quota of up to 2 million items across all connections.</span></span> <span data-ttu-id="c0e3c-152">При общем доступе соединителов Graph бесплатная квота истекает 1 апреля 2021 г. для тех организаций, которые использовали соединители Graph в предварительном просмотре.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-152">With Graph connectors being generally available, the free quota will expire on April 1st, 2021 for those organizations who have been using Graph connectors in preview.</span></span>
><span data-ttu-id="c0e3c-153">Соединители графа, построенные Корпорацией Майкрософт, помеченные как ["Preview",](connectors-preview.md) не будут включены в общую квоту заряженных индексов для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-153">Microsoft-built Graph connectors labeled as ["Preview"](connectors-preview.md) will not be included in the total charged index quota for your organization.</span></span> <span data-ttu-id="c0e3c-154">Однако он будет учитывать максимальное число из 10 подключений, которые можно настроить для организации, и максимальное число 7 миллионов элементов, которые организация может индексировать по подключениям; каждое подключение ограничено 700 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-154">However, it will count towards the max number of 10 connections you can configure for your organization and the max number of 7 million items your organization can index across connections; each connection is limited 700,000 items.</span></span> 

<span data-ttu-id="c0e3c-155">В панели использования квот будут указаны различные состояния, основанные на потреблении квот вашей организацией:</span><span class="sxs-lookup"><span data-stu-id="c0e3c-155">The quota utilization bar will indicate various states based on consumption of quota by your organization:</span></span>

<span data-ttu-id="c0e3c-156">Состояние</span><span class="sxs-lookup"><span data-stu-id="c0e3c-156">State</span></span> | <span data-ttu-id="c0e3c-157">Потребление квот</span><span class="sxs-lookup"><span data-stu-id="c0e3c-157">Quota consumption</span></span>
--- | ---
<span data-ttu-id="c0e3c-158">Normal</span><span class="sxs-lookup"><span data-stu-id="c0e3c-158">Normal</span></span> | <span data-ttu-id="c0e3c-159">1-69%</span><span class="sxs-lookup"><span data-stu-id="c0e3c-159">1-69%</span></span>
<span data-ttu-id="c0e3c-160">Фишинговое сообщение с</span><span class="sxs-lookup"><span data-stu-id="c0e3c-160">High</span></span> | <span data-ttu-id="c0e3c-161">70-89%</span><span class="sxs-lookup"><span data-stu-id="c0e3c-161">70-89%</span></span>
<span data-ttu-id="c0e3c-162">Критический</span><span class="sxs-lookup"><span data-stu-id="c0e3c-162">Critical</span></span> | <span data-ttu-id="c0e3c-163">90%-99%</span><span class="sxs-lookup"><span data-stu-id="c0e3c-163">90%-99%</span></span>
<span data-ttu-id="c0e3c-164">Full</span><span class="sxs-lookup"><span data-stu-id="c0e3c-164">Full</span></span> | <span data-ttu-id="c0e3c-165">100 %</span><span class="sxs-lookup"><span data-stu-id="c0e3c-165">100%</span></span>

<span data-ttu-id="c0e3c-166">Кроме того, с каждым подключением будет отображаться количество индексных элементов.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-166">The number of items indexed will also be displayed with each connection.</span></span> <span data-ttu-id="c0e3c-167">Количество элементов, индекс которых индексироваться каждым подключением, вносит вклад в общую квоту, доступную для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-167">The number of items indexed by each connection contributes to the total quota available for your organization.</span></span>

<span data-ttu-id="c0e3c-168">Когда квота индексов будет превышена для вашей организации, все активные подключения будут влиять, и эти подключения будут работать в **пределе, превышаемом** состоянии.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-168">When index quota is exceeded for your organization, all active connections will be impacted, and those connections will operate in **limit exceeded** state.</span></span> <span data-ttu-id="c0e3c-169">В этом состоянии активные подключения</span><span class="sxs-lookup"><span data-stu-id="c0e3c-169">In this state, your active connections</span></span>  

* <span data-ttu-id="c0e3c-170">Не удастся добавить новые элементы.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-170">Will not be able to add new items.</span></span>

* <span data-ttu-id="c0e3c-171">Сможет обновлять или удалять существующие элементы.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-171">Will be able to update or delete existing items.</span></span>

<span data-ttu-id="c0e3c-172">Чтобы исправить это, вы можете сделать любой из следующих ниже.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-172">To fix this, you can do any of the following:</span></span>

* <span data-ttu-id="c0e3c-173">Узнайте, как приобрести квоту индекса для организации в рамках [требований к лицензированию и ценообразования.](licensing.md)</span><span class="sxs-lookup"><span data-stu-id="c0e3c-173">Learn how to purchase index quota for your organization at [Licensing requirements and pricing](licensing.md).</span></span>

* <span data-ttu-id="c0e3c-174">Определение подключений, в которых слишком много контента передается, и обнови их, чтобы индексировать меньше элементов, чтобы у них было место для квоты.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-174">Identify connections which have too much content being ingested and update them to index fewer items to make room for quota.</span></span> <span data-ttu-id="c0e3c-175">Чтобы обновить подключение, необходимо удалить и создать новое подключение с новым фильтром ingestion, который приносит меньше элементов.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-175">To update the connection, you must delete and create a new connection with a new ingestion filter which brings in fewer items.</span></span>

* <span data-ttu-id="c0e3c-176">Постоянное удаление одного или более подключений</span><span class="sxs-lookup"><span data-stu-id="c0e3c-176">Permanently delete one or more connections</span></span>
