---
title: Кластер результатов соединители
ms.author: manusi
author: manusi
manager: ruppala
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Сведения о кластере результатов соединители
ms.openlocfilehash: ae5528f2e12c9e331b66e821f2a9c03947d788df
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031776"
---
# <a name="graph-connectors-result-cluster"></a><span data-ttu-id="c4f1f-103">Кластер результатов соединители графиков</span><span class="sxs-lookup"><span data-stu-id="c4f1f-103">Graph connectors result cluster</span></span>

## <a name="overview-of-the-graph-connectors-result-cluster-preview"></a><span data-ttu-id="c4f1f-104">Обзор кластера результатов соединители Graph (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="c4f1f-104">Overview of the Graph connectors result cluster (Preview)</span></span>  

<span data-ttu-id="c4f1f-105">С кластерами результатов графа предприятия могут искать контент из сторонних источников данных в представлении по умолчанию, вкладке **All** в SharePoint, Office.com и Microsoft Search in Bing.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-105">With Graph connectors result clusters, enterprises can search for content from third party data sources in their default view, the **All** tab, in SharePoint, Office.com, and Microsoft Search in Bing.</span></span>

<span data-ttu-id="c4f1f-106">Кластеры результатов помогают пользователям открывать все сторонние контенты в одном месте.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-106">Result clusters help users discover all third party content in one place.</span></span> <span data-ttu-id="c4f1f-107">Результаты, показанные в кластере результатов, сгруппируются в зависимости от вертикальной конфигурации поиска.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-107">The results shown in a result cluster are grouped together based on the search vertical configuration.</span></span>

## <a name="how-connector-results-are-selected-and-displayed"></a><span data-ttu-id="c4f1f-108">Выбор и отображение результатов соединители</span><span class="sxs-lookup"><span data-stu-id="c4f1f-108">How connector results are selected and displayed</span></span>

<span data-ttu-id="c4f1f-109">Результаты соединителя, предоставляемые в кластере результатов, получены из отдельных вертикали поиска с содержимым соединителя.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-109">Connector results provided in the result cluster are derived from individual search verticals with connector content.</span></span> <span data-ttu-id="c4f1f-110">Каждая вертикаль поиска предоставляет набор соответствующих результатов, которые становятся кластером результатов кандидатов.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-110">Each search vertical provides a set of relevant results which becomes a candidate result cluster.</span></span> <span data-ttu-id="c4f1f-111">Соответствующие результаты выбираются в зависимости от свойства "title" и "content" каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-111">Relevant results are chosen based on the "title" property and "content" property of each item.</span></span> <span data-ttu-id="c4f1f-112">Свойство контента помечено как *isContent=true* на схеме.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-112">The content property is marked as *isContent=true* on the schema.</span></span>

<span data-ttu-id="c4f1f-113">Чтобы обеспечить обнаружение контента из вертикали поиска, рекомендуется предоставить значимые заголовки для элементов.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-113">To ensure discovery of content from the search verticals, we recommend providing meaningful titles for your items.</span></span> <span data-ttu-id="c4f1f-114">Это положительно влияет на арбитраж кандидатов кластера результатов и вероятность появления контента в кластере результатов.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-114">This positively impacts the arbitration of result cluster candidates and the likelihood of your content showing up in a result cluster.</span></span> <span data-ttu-id="c4f1f-115">Например, не используйте ID в качестве значений для свойства "title", если только пользователи не будут использовать ID-объекты, чтобы искать контент.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-115">For example, avoid the use of IDs as values for the property "title" unless your users are using IDs to look for content.</span></span>

<span data-ttu-id="c4f1f-116">Как часто отображается кластер результатов, зависит от таких факторов, как количество вертикали поиска, которые вы настраиваете, и тип контента.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-116">How often a result cluster is shown varies on factors such as the number of search verticals that you configure and the type of content.</span></span> <span data-ttu-id="c4f1f-117">Взаимодействуя или игнорируя кластер результатов, пользователи будут неявно предоставлять подсказки, которые будут корректировать его запуск с течением времени.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-117">By either interacting or ignoring a result cluster, users will implicitly provide hints that will adjust its triggering over time.</span></span>

<span data-ttu-id="c4f1f-118">В результате поиска элементов соединители, [](./customize-search-page.md#create-your-own-result-type) показанных в кластере результатов, используются типы результатов, определенные вами.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-118">The search result experience for connector items shown in your result cluster uses [result types](./customize-search-page.md#create-your-own-result-type) defined by you.</span></span> <span data-ttu-id="c4f1f-119">Если тип результатов не настроен, используется [схема, созданная](./customize-search-page.md#default-search-result-layout) системой.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-119">If no result type is configured, a [system generated layout](./customize-search-page.md#default-search-result-layout) is used.</span></span> 

<span data-ttu-id="c4f1f-120">Мы рекомендуем использовать свойство "title" в качестве заголовка результатов поиска, а свойство "контент" в качестве описания поиска.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-120">We recommend using the “title” property as the search result title and the "content" property as the search description.</span></span> <span data-ttu-id="c4f1f-121">Это обеспечит наилучший опыт для пользователей путем точного запуска кластера результатов и наиболее релевантных результатов в кластере.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-121">This will provide the best experience for your users through accurate triggering of the result cluster and most relevant results in the cluster.</span></span> 

## <a name="enable-result-clusters"></a><span data-ttu-id="c4f1f-122">Включить кластеры результатов</span><span class="sxs-lookup"><span data-stu-id="c4f1f-122">Enable result clusters</span></span>
  
<span data-ttu-id="c4f1f-123">По умолчанию отключается кластер результатов.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-123">The result cluster experience is turned off by default.</span></span>  

<span data-ttu-id="c4f1f-124">Выполните следующие действия, чтобы включить опыт на уровне организации:</span><span class="sxs-lookup"><span data-stu-id="c4f1f-124">Follow these steps to turn on the experience at the organization level:</span></span>

1. <span data-ttu-id="c4f1f-125">В центре [администрирования Microsoft 365](https://admin.microsoft.com)перейдите к [**вертикалям**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span><span class="sxs-lookup"><span data-stu-id="c4f1f-125">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Verticals**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
2. <span data-ttu-id="c4f1f-126">Выберите  все вертикали, а затем включении **результатов соединителя Показать**.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-126">Select  the **All** vertical, then enable **Show connector results**.</span></span> 


<span data-ttu-id="c4f1f-127">Выполните следующие действия, чтобы включить опыт на уровне сайта SharePoint:</span><span class="sxs-lookup"><span data-stu-id="c4f1f-127">Follow these steps to turn on the experience at the SharePoint site level:</span></span>

1. <span data-ttu-id="c4f1f-128">На сайте SharePoint, где необходимо создать кластер результатов, перейдите в **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-128">On the SharePoint site where you want the result cluster experience, go to **Settings**.</span></span>
2. <span data-ttu-id="c4f1f-129">Перейдите **к сведениям о** > **сайте Просмотр всех параметров сайта.**</span><span class="sxs-lookup"><span data-stu-id="c4f1f-129">Go to **Site information**>**View all site settings**.</span></span>
3. <span data-ttu-id="c4f1f-130">Перейдите в раздел Microsoft Search, а затем выберите **Настройка Microsoft Search для этой коллекции сайтов.**</span><span class="sxs-lookup"><span data-stu-id="c4f1f-130">Go to the Microsoft Search section, then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="c4f1f-131">В области навигации перейдите к **настраиваемой области,** а затем выберите **Вертикали.**</span><span class="sxs-lookup"><span data-stu-id="c4f1f-131">In the navigation pane, go to **Custom experience**, then select **Verticals**.</span></span>
5. <span data-ttu-id="c4f1f-132">Выберите  все вертикали, а затем включении **результатов соединителя Показать**.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-132">Select the **All** vertical, then enable **Show connector results**.</span></span>

## <a name="view-the-result-cluster-experience-after-it-is-enabled"></a><span data-ttu-id="c4f1f-133">Просмотр кластера результатов после включения</span><span class="sxs-lookup"><span data-stu-id="c4f1f-133">View the result cluster experience after it is enabled</span></span>

<span data-ttu-id="c4f1f-134">После включаем кластера результатов может занять до 12 часов, прежде чем вы сможете просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-134">After you turn on the result cluster experience, it can take up to 12 hours before you can view it.</span></span> <span data-ttu-id="c4f1f-135">Если вы хотите, чтобы этот опыт был немедленно, можно применить *кэшClear=true* к URL-адресу в SharePoint и Office.</span><span class="sxs-lookup"><span data-stu-id="c4f1f-135">If you want the experience immediately, you can append *cacheClear=true* to the URL in SharePoint and Office.</span></span>