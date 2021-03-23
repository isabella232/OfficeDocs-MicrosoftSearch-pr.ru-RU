---
title: Управление соединитетелями Microsoft Graph для поиска Майкрософт
ms.author: monaray
author: monaray97
manager: mnirkhe
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Управление соединиттелями Microsoft Graph для поиска Майкрософт.
ms.openlocfilehash: cba50d8eb558b4d74ed46554dc155d4f275b1332
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031722"
---
<!-- markdownlint-disable no-inline-html -->

# <a name="monitor-your-connections"></a><span data-ttu-id="5ea94-103">Мониторинг подключений</span><span class="sxs-lookup"><span data-stu-id="5ea94-103">Monitor your connections</span></span>

<span data-ttu-id="5ea94-104">Чтобы получить доступ к соединитетелям и управлять ими, необходимо назначить вас администратором поиска для клиента.</span><span class="sxs-lookup"><span data-stu-id="5ea94-104">To access and manage your connectors, you must be designated as a search administrator for your tenant.</span></span> <span data-ttu-id="5ea94-105">Обратитесь к администратору клиента для предоставления вам роли администратора поиска.</span><span class="sxs-lookup"><span data-stu-id="5ea94-105">Contact your tenant administrator to provision you for the search administrator role.</span></span>

## <a name="connection-operations"></a><span data-ttu-id="5ea94-106">Операции подключения</span><span class="sxs-lookup"><span data-stu-id="5ea94-106">Connection Operations</span></span>

<span data-ttu-id="5ea94-107">Перейдите на [вкладку Соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в центре администрирования [Microsoft 365.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="5ea94-107">Navigate to the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="5ea94-108">Для каждого типа соединители центр администрирования [Microsoft 365](https://admin.microsoft.com) поддерживает операции, показанные в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="5ea94-108">For each connector type, the [Microsoft 365 admin center](https://admin.microsoft.com) supports the operations shown in the following table:</span></span>

<span data-ttu-id="5ea94-109">Операция</span><span class="sxs-lookup"><span data-stu-id="5ea94-109">Operation</span></span> | <span data-ttu-id="5ea94-110">Соединители Graph от Майкрософт</span><span class="sxs-lookup"><span data-stu-id="5ea94-110">Graph connectors by Microsoft</span></span> | <span data-ttu-id="5ea94-111">Соединители партнер или граф</span><span class="sxs-lookup"><span data-stu-id="5ea94-111">Partner or Graph connectors</span></span>
--- | --- | ---
<span data-ttu-id="5ea94-112">Добавление подключения</span><span class="sxs-lookup"><span data-stu-id="5ea94-112">Add a connection</span></span> | :heavy_check_mark: <span data-ttu-id="5ea94-113">(См. [обзор установки)](configure-connector.md)</span><span class="sxs-lookup"><span data-stu-id="5ea94-113">(See [Setup overview](configure-connector.md))</span></span> | :x: <span data-ttu-id="5ea94-114">(Обратитесь к партнеру или настраиваемой соединители администратора UX)</span><span class="sxs-lookup"><span data-stu-id="5ea94-114">(Refer to your partner or custom-built connector admin UX)</span></span>
<span data-ttu-id="5ea94-115">Удаление подключения</span><span class="sxs-lookup"><span data-stu-id="5ea94-115">Delete a connection</span></span> | :heavy_check_mark: | :heavy_check_mark:
<span data-ttu-id="5ea94-118">Изменение опубликованного подключения</span><span class="sxs-lookup"><span data-stu-id="5ea94-118">Edit a published connection</span></span> | :heavy_check_mark: <span data-ttu-id="5ea94-119">имя и описание</span><span class="sxs-lookup"><span data-stu-id="5ea94-119">Name and Description</span></span><br></br> :heavy_check_mark: <span data-ttu-id="5ea94-120">параметры подключения</span><span class="sxs-lookup"><span data-stu-id="5ea94-120">Connection settings</span></span><br></br> :heavy_check_mark: <span data-ttu-id="5ea94-121">метки свойств</span><span class="sxs-lookup"><span data-stu-id="5ea94-121">Property labels</span></span><br></br> :heavy_check_mark: <span data-ttu-id="5ea94-122">схема</span><span class="sxs-lookup"><span data-stu-id="5ea94-122">Schema</span></span><br></br> :heavy_check_mark: <span data-ttu-id="5ea94-123">расписание обновления</span><span class="sxs-lookup"><span data-stu-id="5ea94-123">Refresh schedule</span></span><br></br> | :heavy_check_mark: <span data-ttu-id="5ea94-124">Имя</span><span class="sxs-lookup"><span data-stu-id="5ea94-124">Name</span></span><br></br> :heavy_check_mark: <span data-ttu-id="5ea94-125">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea94-125">Description</span></span>
<span data-ttu-id="5ea94-126">Изменение подключения к проекту</span><span class="sxs-lookup"><span data-stu-id="5ea94-126">Edit a draft connection</span></span> | :heavy_check_mark: | :x:

## <a name="monitor-your-connection-state"></a><span data-ttu-id="5ea94-129">Мониторинг состояния подключения</span><span class="sxs-lookup"><span data-stu-id="5ea94-129">Monitor your connection state</span></span>

<span data-ttu-id="5ea94-130">После создания подключения количество обработанных элементов отображается на вкладке **Соединители** на странице **Microsoft Search.**</span><span class="sxs-lookup"><span data-stu-id="5ea94-130">After you create a connection, the number of processed items shows on the **Connectors** tab on the **Microsoft Search** page.</span></span> <span data-ttu-id="5ea94-131">После успешного завершения начального полного обхода отображается прогресс для периодического инкрементного обхода.</span><span class="sxs-lookup"><span data-stu-id="5ea94-131">After the initial full crawl completes successfully, the progress for periodic incremental crawls displays.</span></span> <span data-ttu-id="5ea94-132">На этой странице представлена информация о ежедневной работе соединиттеля и обзор журналов и истории ошибок.</span><span class="sxs-lookup"><span data-stu-id="5ea94-132">This page provides information about the connector's day-to-day operations and an overview of the logs and error history.</span></span>

<span data-ttu-id="5ea94-133">Четыре состояния показываются в **столбце Состояние** для каждого подключения:</span><span class="sxs-lookup"><span data-stu-id="5ea94-133">Four states show up in the **State** column against each connection:</span></span>

* <span data-ttu-id="5ea94-134">**Синхронизация**.</span><span class="sxs-lookup"><span data-stu-id="5ea94-134">**Syncing**.</span></span> <span data-ttu-id="5ea94-135">Соединители обхода данных из источника, чтобы индексировать существующие элементы и делать какие-либо обновления.</span><span class="sxs-lookup"><span data-stu-id="5ea94-135">The connector is crawling the data from the source to index the existing items and make any updates.</span></span>

* <span data-ttu-id="5ea94-136">**Готово.** Подключение готово, и не существует активного обхода, запущенного против него.</span><span class="sxs-lookup"><span data-stu-id="5ea94-136">**Ready**: The connection is ready, and there's no active crawl running against it.</span></span> <span data-ttu-id="5ea94-137">**Последнее время синхронизации** указывает, когда был последний успешный обход.</span><span class="sxs-lookup"><span data-stu-id="5ea94-137">**Last sync time** indicates when the last successful crawl happened.</span></span> <span data-ttu-id="5ea94-138">Подключение свежо, как и время последней синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5ea94-138">The connection is as fresh as the last sync time.</span></span>

* <span data-ttu-id="5ea94-139">**Приостановлено**.</span><span class="sxs-lookup"><span data-stu-id="5ea94-139">**Paused**.</span></span> <span data-ttu-id="5ea94-140">Обходы приостановлены администраторами с помощью параметра паузы.</span><span class="sxs-lookup"><span data-stu-id="5ea94-140">The crawls are paused by the admins through the pause option.</span></span> <span data-ttu-id="5ea94-141">Следующий обход выполняется только при возобновлении вручную.</span><span class="sxs-lookup"><span data-stu-id="5ea94-141">The next crawl runs only when it's manually resumed.</span></span> <span data-ttu-id="5ea94-142">Однако данные из этого подключения по-прежнему можно искать.</span><span class="sxs-lookup"><span data-stu-id="5ea94-142">However, the data from this connection continues to be searchable.</span></span>

* <span data-ttu-id="5ea94-143">**Не удалось**.</span><span class="sxs-lookup"><span data-stu-id="5ea94-143">**Failed**.</span></span> <span data-ttu-id="5ea94-144">При подключении был критический сбой.</span><span class="sxs-lookup"><span data-stu-id="5ea94-144">The connection had a critical failure.</span></span> <span data-ttu-id="5ea94-145">Эта ошибка требует ручного вмешательства.</span><span class="sxs-lookup"><span data-stu-id="5ea94-145">This error requires manual intervention.</span></span> <span data-ttu-id="5ea94-146">Администратору необходимо принять соответствующие меры на основе показанного сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5ea94-146">The admin needs to take appropriate action based on the error message shown.</span></span> <span data-ttu-id="5ea94-147">Данные, индексируемые до момента ошибки, можно найти.</span><span class="sxs-lookup"><span data-stu-id="5ea94-147">Data that was indexed until the error occurred is searchable.</span></span>

## <a name="monitor-your-index-quota-utilization"></a><span data-ttu-id="5ea94-148">Мониторинг использования квот индекса</span><span class="sxs-lookup"><span data-stu-id="5ea94-148">Monitor your index quota utilization</span></span>

<span data-ttu-id="5ea94-149">Доступная квота индекса и потребление отображаются на странице посадки соединителов.</span><span class="sxs-lookup"><span data-stu-id="5ea94-149">The available index quota and consumption is displayed on the connectors landing page.</span></span>

![Планка использования квоты индекса](media/quota_utilization.png)
 
>[!NOTE]
><span data-ttu-id="5ea94-151">В период предварительного просмотра каждая организация, пробуя соединители Graph, была предоставлена бесплатная фиксированная квота до 2 миллионов элементов во всех подключениях.</span><span class="sxs-lookup"><span data-stu-id="5ea94-151">During the preview period, every organization trying out Graph connectors was provided a free fixed quota of up to 2 million items across all connections.</span></span> <span data-ttu-id="5ea94-152">При общем доступе соединителов Graph бесплатная квота истекает 1 апреля 2021 г. для тех организаций, которые использовали соединители Graph в предварительном просмотре.</span><span class="sxs-lookup"><span data-stu-id="5ea94-152">With Graph connectors being generally available, the free quota will expire on April 1st, 2021 for those organizations who have been using Graph connectors in preview.</span></span>
><span data-ttu-id="5ea94-153">Соединители графа, построенные Корпорацией Майкрософт, помеченные как ["Preview",](./connectors-overview.md) не будут включены в общую квоту заряженных индексов для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5ea94-153">Microsoft-built Graph connectors labeled as ["Preview"](./connectors-overview.md) will not be included in the total charged index quota for your organization.</span></span> <span data-ttu-id="5ea94-154">Однако он будет учитывать максимальное число из 10 подключений, которые можно настроить для организации, и максимальное число 7 миллионов элементов, которые организация может индексировать по подключениям; каждое подключение ограничено 700 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="5ea94-154">However, it will count towards the max number of 10 connections you can configure for your organization and the max number of 7 million items your organization can index across connections; each connection is limited 700,000 items.</span></span> 

<span data-ttu-id="5ea94-155">В панели использования квот будут указаны различные состояния, основанные на потреблении квот вашей организацией:</span><span class="sxs-lookup"><span data-stu-id="5ea94-155">The quota utilization bar will indicate various states based on consumption of quota by your organization:</span></span>

<span data-ttu-id="5ea94-156">Состояние</span><span class="sxs-lookup"><span data-stu-id="5ea94-156">State</span></span> | <span data-ttu-id="5ea94-157">Уровни использования квот</span><span class="sxs-lookup"><span data-stu-id="5ea94-157">Quota utilization levels</span></span>
--- | --- 
<span data-ttu-id="5ea94-158">Normal</span><span class="sxs-lookup"><span data-stu-id="5ea94-158">Normal</span></span> | <span data-ttu-id="5ea94-159">0-79%</span><span class="sxs-lookup"><span data-stu-id="5ea94-159">0-79%</span></span>
<span data-ttu-id="5ea94-160">Высокий</span><span class="sxs-lookup"><span data-stu-id="5ea94-160">High</span></span> | <span data-ttu-id="5ea94-161">80-89%</span><span class="sxs-lookup"><span data-stu-id="5ea94-161">80-89%</span></span>
<span data-ttu-id="5ea94-162">Критический</span><span class="sxs-lookup"><span data-stu-id="5ea94-162">Critical</span></span> | <span data-ttu-id="5ea94-163">90%-99%</span><span class="sxs-lookup"><span data-stu-id="5ea94-163">90%-99%</span></span>
<span data-ttu-id="5ea94-164">Full</span><span class="sxs-lookup"><span data-stu-id="5ea94-164">Full</span></span> | <span data-ttu-id="5ea94-165">100 %</span><span class="sxs-lookup"><span data-stu-id="5ea94-165">100%</span></span>

<!-- 
![Quota utilization levels](media/connectors-quota-utilization-levels.png)
-->

<span data-ttu-id="5ea94-166">Кроме того, с каждым подключением будет отображаться количество индексных элементов.</span><span class="sxs-lookup"><span data-stu-id="5ea94-166">The number of items indexed will also be displayed with each connection.</span></span> <span data-ttu-id="5ea94-167">Количество элементов, индекс которых индексироваться каждым подключением, вносит вклад в общую квоту, доступную для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5ea94-167">The number of items indexed by each connection contributes to the total quota available for your organization.</span></span>

<span data-ttu-id="5ea94-168">Когда квота индексов будет превышена для вашей организации, все активные подключения будут влиять, и эти подключения будут работать в **пределе, превышаемом** состоянии.</span><span class="sxs-lookup"><span data-stu-id="5ea94-168">When index quota is exceeded for your organization, all active connections will be impacted, and those connections will operate in **limit exceeded** state.</span></span> <span data-ttu-id="5ea94-169">В этом состоянии активные подключения</span><span class="sxs-lookup"><span data-stu-id="5ea94-169">In this state, your active connections</span></span>  

* <span data-ttu-id="5ea94-170">Не удастся добавить новые элементы.</span><span class="sxs-lookup"><span data-stu-id="5ea94-170">Will not be able to add new items.</span></span>

* <span data-ttu-id="5ea94-171">Сможет обновлять или удалять существующие элементы.</span><span class="sxs-lookup"><span data-stu-id="5ea94-171">Will be able to update or delete existing items.</span></span>

<span data-ttu-id="5ea94-172">Чтобы исправить это, вы можете сделать любой из следующих ниже.</span><span class="sxs-lookup"><span data-stu-id="5ea94-172">To fix this, you can do any of the following:</span></span>

* <span data-ttu-id="5ea94-173">Узнайте, как приобрести квоту индекса для организации в рамках [требований к лицензированию и ценообразования.](licensing.md)</span><span class="sxs-lookup"><span data-stu-id="5ea94-173">Learn how to purchase index quota for your organization at [Licensing requirements and pricing](licensing.md).</span></span>

* <span data-ttu-id="5ea94-174">Определение подключений, в которых слишком много контента передается, и обнови их, чтобы индексировать меньше элементов, чтобы у них было место для квоты.</span><span class="sxs-lookup"><span data-stu-id="5ea94-174">Identify connections which have too much content being ingested and update them to index fewer items to make room for quota.</span></span> <span data-ttu-id="5ea94-175">Чтобы обновить подключение, необходимо удалить и создать новое подключение с новым фильтром ingestion, который приносит меньше элементов.</span><span class="sxs-lookup"><span data-stu-id="5ea94-175">To update the connection, you must delete and create a new connection with a new ingestion filter which brings in fewer items.</span></span>

* <span data-ttu-id="5ea94-176">Постоянное удаление одного или более подключений</span><span class="sxs-lookup"><span data-stu-id="5ea94-176">Permanently delete one or more connections</span></span>