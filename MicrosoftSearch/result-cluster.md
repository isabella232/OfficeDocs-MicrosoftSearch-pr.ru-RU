---
title: Кластер результатов для соединителей
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
description: Сведения о соединителях для кластера результатов
ms.openlocfilehash: fa6ac2dc720ed43e40454b952526734accd45ea4
ms.sourcegitcommit: a328b9764abf5cd0c1c0a8c7def0c6e334da9a1d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/30/2020
ms.locfileid: "49477116"
---
# <a name="graph-connectors-result-cluster"></a><span data-ttu-id="4d821-103">Кластер результатов Graph Connectors</span><span class="sxs-lookup"><span data-stu-id="4d821-103">Graph connectors result cluster</span></span>

## <a name="overview-of-the-graph-connectors-result-cluster-preview"></a><span data-ttu-id="4d821-104">Общие сведения о кластере результатов Graph Connectors (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4d821-104">Overview of the Graph connectors result cluster (Preview)</span></span>  

<span data-ttu-id="4d821-105">С помощью Graph Connectors Clusters, предприятия могут искать контент из сторонних источников данных в представлении по умолчанию (вкладка "все") в SharePoint и Office.com.</span><span class="sxs-lookup"><span data-stu-id="4d821-105">With Graph connectors result clusters, enterprises can search for content from third party data sources in their default view (the All tab) in SharePoint and Office.com.</span></span>

<span data-ttu-id="4d821-106">Кластеры результатов помогают пользователям обнаруживать все сторонние материалы (превиаулси, привязанные к одному и тому же соединителю и вертикали) в одном месте.</span><span class="sxs-lookup"><span data-stu-id="4d821-106">Result clusters help users discover all third party content (previoulsy tied to a single connector and vertical) in one place.</span></span> <span data-ttu-id="4d821-107">Результаты, показанные в кластере результатов, объединяются в зависимости от того, как администратор клиента настраивает их в вертикальном поиске.</span><span class="sxs-lookup"><span data-stu-id="4d821-107">The results shown in a result cluster are grouped together based on how the tenant administrator configures them in a search vertical.</span></span>  

## <a name="how-connector-results-are-selected-and-displayed"></a><span data-ttu-id="4d821-108">Выбор и отображение результатов соединителей</span><span class="sxs-lookup"><span data-stu-id="4d821-108">How connector results are selected and displayed</span></span>

<span data-ttu-id="4d821-109">Результаты соединителя, предоставленные в кластере результатов, являются производными от отдельных вертикальных значений поиска с содержимым соединителя.</span><span class="sxs-lookup"><span data-stu-id="4d821-109">Connector results provided in the result cluster are derived from individual search verticals with connector content.</span></span> <span data-ttu-id="4d821-110">Каждый вертикаль поиска содержит набор релевантных результатов, который становится кластером результатов кандидата.</span><span class="sxs-lookup"><span data-stu-id="4d821-110">Each search vertical provides a set of relevant results which becomes a candidate result cluster.</span></span> <span data-ttu-id="4d821-111">Релевантные результаты выбираются на основе свойства Title, фрагмента результата и компонента содержимого каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="4d821-111">Relevant results are chosen based on the "title" property, result snippet, and content component of each item.</span></span>

<span data-ttu-id="4d821-112">Чтобы обеспечить обнаружение контента из вертикали поиска, мы рекомендуем предоставить осмысленные названия для элементов.</span><span class="sxs-lookup"><span data-stu-id="4d821-112">To ensure discovery of content from the search verticals, we recommend providing meaningful titles for your items.</span></span> <span data-ttu-id="4d821-113">Это положительно влияет на арбитраж кандидатов кластера результатов и вероятность того, что контент будет отображаться в кластере результатов.</span><span class="sxs-lookup"><span data-stu-id="4d821-113">This positively impacts the arbitration of result cluster candidates and the likelihood of your content showing up in a result cluster.</span></span> <span data-ttu-id="4d821-114">Например, не используйте идентификаторы в качестве значений для свойства Title, если пользователи не используют идентификаторы для поиска контента.</span><span class="sxs-lookup"><span data-stu-id="4d821-114">For example, avoid the use of IDs as values for the property "title" unless your users are using IDs to look for content.</span></span>

<span data-ttu-id="4d821-115">Частота отображения кластера зависит от факторов, таких как количество настраиваемых вертикальных элементов поиска и тип контента.</span><span class="sxs-lookup"><span data-stu-id="4d821-115">How often a result cluster is shown varies on factors such as the number of search verticals that you configure and the type of content.</span></span> <span data-ttu-id="4d821-116">Выбирая или игнорируя результаты кластера результатов, вы неявно предоставляете подсказки, которые будут настраивать срабатывание кластеров результатов с течением времени.</span><span class="sxs-lookup"><span data-stu-id="4d821-116">By either selecting or ignoring result cluster results, you will implicitly provide hints that will adjust the triggering of result clusters over time.</span></span>

<span data-ttu-id="4d821-117">Режим результатов поиска для элементов соединителя, показанных в кластере результатов, создается системой и не использует пользовательские макеты результатов.</span><span class="sxs-lookup"><span data-stu-id="4d821-117">The search result experience for connector items shown in your result cluster is system generated and does not use custom result layouts.</span></span> <span data-ttu-id="4d821-118">Если требуется, чтобы результаты отображались в кластере результатов, необходимо объявить свойство "Title" и содержимое элемента во время регистрации подключения.</span><span class="sxs-lookup"><span data-stu-id="4d821-118">You must declare the "title" property and item content during connection registration if you want results to appear in your result cluster.</span></span>

## <a name="enable-result-clusters"></a><span data-ttu-id="4d821-119">Включение кластеров результатов</span><span class="sxs-lookup"><span data-stu-id="4d821-119">Enable result clusters</span></span>
  
<span data-ttu-id="4d821-120">По умолчанию работа кластера результатов отключена.</span><span class="sxs-lookup"><span data-stu-id="4d821-120">The result cluster experience is turned off by default.</span></span>  

<span data-ttu-id="4d821-121">Чтобы включить интерфейс на уровне Организации, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4d821-121">Follow these steps to turn on the experience at the organization level:</span></span>

1. <span data-ttu-id="4d821-122">В [центре администрирования Microsoft 365](https://admin.microsoft.com/)откройте раздел **Параметры**  >  **поиска**  >  **Customization**  >  **по вертикали**& аналитики.</span><span class="sxs-lookup"><span data-stu-id="4d821-122">In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Settings** > **Search & intelligence** > **Customization** > **Verticals**.</span></span>  
2. <span data-ttu-id="4d821-123">Выберите пункт **все** по вертикали, а затем включить **Отображение результатов соединителя**.</span><span class="sxs-lookup"><span data-stu-id="4d821-123">Select  the **All** vertical, then enable **Show connector results**.</span></span> 


<span data-ttu-id="4d821-124">Чтобы включить интерфейс на уровне сайта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4d821-124">Follow these steps to turn on the experience at the site level:</span></span>

1. <span data-ttu-id="4d821-125">На сайте SharePoint, на котором вы хотите использовать кластер результатов, перейдите к разделу **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="4d821-125">On the SharePoint site where you want the result cluster experience, go to **Settings**.</span></span>
2. <span data-ttu-id="4d821-126">Перейдите на страницу **сведения о сайте** > , чтобы **Просмотреть все параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="4d821-126">Go to **Site information**>**View all site settings**.</span></span>
3. <span data-ttu-id="4d821-127">Перейдите к разделу Microsoft Search, а затем выберите **Настройка службы поиска Майкрософт для этого семейства веб-сайтов**.</span><span class="sxs-lookup"><span data-stu-id="4d821-127">Go to the Microsoft Search section, then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="4d821-128">В области навигации перейдите к **элементу пользовательский интерфейс**, а затем выберите пункт **вертикальные**.</span><span class="sxs-lookup"><span data-stu-id="4d821-128">In the navigation pane, go to **Custom experience**, then select **Verticals**.</span></span>
5. <span data-ttu-id="4d821-129">Выберите пункт **все** по вертикали, а затем включить **Отображение результатов соединителя**.</span><span class="sxs-lookup"><span data-stu-id="4d821-129">Select the **All** vertical, then enable **Show connector results**.</span></span>

## <a name="view-the-result-cluster-experience-after-it-is-enabled"></a><span data-ttu-id="4d821-130">Просмотр результатов работы кластера после его включения</span><span class="sxs-lookup"><span data-stu-id="4d821-130">View the result cluster experience after it is enabled</span></span>

<span data-ttu-id="4d821-131">После включения интерфейса кластера результатов для его просмотра может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="4d821-131">After you turn on the result cluster experience, it might take a few minutes before you can view it.</span></span> <span data-ttu-id="4d821-132">Если вы хотите немедленно использовать этот интерфейс, вы можете добавить *качеклеар = true* в URL-адрес в SharePoint и Office.</span><span class="sxs-lookup"><span data-stu-id="4d821-132">If you want the experience immediately, you can append *cacheClear=true* to the URL in SharePoint and Office.</span></span>
