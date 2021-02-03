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
ms.openlocfilehash: fb29fb9c14811698fb7c5d043853b57231c76a0b
ms.sourcegitcommit: d1bc6c41ecf47584373ce57543502bed55753d0c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "50080840"
---
# <a name="graph-connectors-result-cluster"></a><span data-ttu-id="4a116-103">Кластер результатов соединители Graph</span><span class="sxs-lookup"><span data-stu-id="4a116-103">Graph connectors result cluster</span></span>

## <a name="overview-of-the-graph-connectors-result-cluster-preview"></a><span data-ttu-id="4a116-104">Обзор кластера результатов соединители Graph (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4a116-104">Overview of the Graph connectors result cluster (Preview)</span></span>  

<span data-ttu-id="4a116-105">Благодаря соединитетелям Graph в кластерах результатов предприятия могут искать контент  из сторонних источников данных в представлении по умолчанию, на вкладке "Все", в SharePoint, Office.com и Поиске (Майкрософт) в Bing.</span><span class="sxs-lookup"><span data-stu-id="4a116-105">With Graph connectors result clusters, enterprises can search for content from third party data sources in their default view, the **All** tab, in SharePoint, Office.com, and Microsoft Search in Bing.</span></span>

<span data-ttu-id="4a116-106">Кластеры результатов помогают пользователям обнаруживать весь сторонний контент в одном месте.</span><span class="sxs-lookup"><span data-stu-id="4a116-106">Result clusters help users discover all third party content in one place.</span></span> <span data-ttu-id="4a116-107">Результаты, показанные в кластере результатов, группируются на основе конфигурации вертикали поиска.</span><span class="sxs-lookup"><span data-stu-id="4a116-107">The results shown in a result cluster are grouped together based on the search vertical configuration.</span></span>

## <a name="how-connector-results-are-selected-and-displayed"></a><span data-ttu-id="4a116-108">Выбор и отображение результатов соединители</span><span class="sxs-lookup"><span data-stu-id="4a116-108">How connector results are selected and displayed</span></span>

<span data-ttu-id="4a116-109">Результаты соединителя, предоставленные в кластере результатов, являются производными от отдельных вертикали поиска с содержимым соединителя.</span><span class="sxs-lookup"><span data-stu-id="4a116-109">Connector results provided in the result cluster are derived from individual search verticals with connector content.</span></span> <span data-ttu-id="4a116-110">Каждая вертикаль поиска предоставляет набор релевантного результата, который становится кандидатом кластера результатов.</span><span class="sxs-lookup"><span data-stu-id="4a116-110">Each search vertical provides a set of relevant results which becomes a candidate result cluster.</span></span> <span data-ttu-id="4a116-111">Релевантные результаты выбираются на основе свойств title и content каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="4a116-111">Relevant results are chosen based on the "title" property and "content" property of each item.</span></span> <span data-ttu-id="4a116-112">Свойство контента помечено как *isContent=true* в схеме.</span><span class="sxs-lookup"><span data-stu-id="4a116-112">The content property is marked as *isContent=true* on the schema.</span></span>

<span data-ttu-id="4a116-113">Чтобы обеспечить обнаружение контента из вертикали поиска, мы рекомендуем предоставить осмысленные заголовки для элементов.</span><span class="sxs-lookup"><span data-stu-id="4a116-113">To ensure discovery of content from the search verticals, we recommend providing meaningful titles for your items.</span></span> <span data-ttu-id="4a116-114">Это положительно влияет на арбитраж кандидатов кластера результатов и вероятность появления контента в кластере результатов.</span><span class="sxs-lookup"><span data-stu-id="4a116-114">This positively impacts the arbitration of result cluster candidates and the likelihood of your content showing up in a result cluster.</span></span> <span data-ttu-id="4a116-115">Например, избегайте использования ИД в качестве значений для свойства "title", если только пользователи не используют их для иссылки содержимого.</span><span class="sxs-lookup"><span data-stu-id="4a116-115">For example, avoid the use of IDs as values for the property "title" unless your users are using IDs to look for content.</span></span>

<span data-ttu-id="4a116-116">То, как часто отображается кластер результатов, зависит от таких факторов, как количество настраиваемых вертикали поиска и тип контента.</span><span class="sxs-lookup"><span data-stu-id="4a116-116">How often a result cluster is shown varies on factors such as the number of search verticals that you configure and the type of content.</span></span> <span data-ttu-id="4a116-117">При взаимодействии или игнорировании кластера результатов пользователи будут неявно предоставлять подсказки, которые будут регулировать его запуск с течением времени.</span><span class="sxs-lookup"><span data-stu-id="4a116-117">By either interacting or ignoring a result cluster, users will implicitly provide hints that will adjust its triggering over time.</span></span>

<span data-ttu-id="4a116-118">Для результатов поиска элементов соединители, показанных в кластере результатов, используются типы результатов, [определенные](https://docs.microsoft.com/microsoftsearch/customize-search-page#create-your-own-result-type) вами.</span><span class="sxs-lookup"><span data-stu-id="4a116-118">The search result experience for connector items shown in your result cluster uses [result types](https://docs.microsoft.com/microsoftsearch/customize-search-page#create-your-own-result-type) defined by you.</span></span> <span data-ttu-id="4a116-119">Если тип результата не настроен, используется [системный макет.](https://docs.microsoft.com/microsoftsearch/customize-search-page#default-search-result-layout)</span><span class="sxs-lookup"><span data-stu-id="4a116-119">If no result type is configured, a [system generated layout](https://docs.microsoft.com/microsoftsearch/customize-search-page#default-search-result-layout) is used.</span></span> 

<span data-ttu-id="4a116-120">Рекомендуется использовать свойство title в качестве заголовка результата поиска и свойство content в качестве описания поиска.</span><span class="sxs-lookup"><span data-stu-id="4a116-120">We recommend using the “title” property as the search result title and the "content" property as the search description.</span></span> <span data-ttu-id="4a116-121">Это обеспечит наилучшее впечатление для пользователей благодаря точному запуску кластера результатов и наиболее релевантного результата в кластере.</span><span class="sxs-lookup"><span data-stu-id="4a116-121">This will provide the best experience for your users through accurate triggering of the result cluster and most relevant results in the cluster.</span></span> 

## <a name="enable-result-clusters"></a><span data-ttu-id="4a116-122">Включить кластеры результатов</span><span class="sxs-lookup"><span data-stu-id="4a116-122">Enable result clusters</span></span>
  
<span data-ttu-id="4a116-123">По умолчанию кластер результатов отключен.</span><span class="sxs-lookup"><span data-stu-id="4a116-123">The result cluster experience is turned off by default.</span></span>  

<span data-ttu-id="4a116-124">Выполните следующие действия, чтобы включить опыт на уровне организации:</span><span class="sxs-lookup"><span data-stu-id="4a116-124">Follow these steps to turn on the experience at the organization level:</span></span>

1. <span data-ttu-id="4a116-125">В Центре [администрирования Microsoft 365](https://admin.microsoft.com)перейдите в [**"Вертикали".**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)</span><span class="sxs-lookup"><span data-stu-id="4a116-125">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Verticals**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
2. <span data-ttu-id="4a116-126">Выберите **вертикаль "Все",** а затем включении **результата "Показать результаты соединителя".**</span><span class="sxs-lookup"><span data-stu-id="4a116-126">Select  the **All** vertical, then enable **Show connector results**.</span></span> 


<span data-ttu-id="4a116-127">Выполните следующие действия, чтобы включить опытом на уровне сайта SharePoint:</span><span class="sxs-lookup"><span data-stu-id="4a116-127">Follow these steps to turn on the experience at the SharePoint site level:</span></span>

1. <span data-ttu-id="4a116-128">На сайте SharePoint, где вы хотите получить кластер результатов, перейдите в раздел **"Параметры".**</span><span class="sxs-lookup"><span data-stu-id="4a116-128">On the SharePoint site where you want the result cluster experience, go to **Settings**.</span></span>
2. <span data-ttu-id="4a116-129">Перейдите **в "Сведения о** > **сайте" "Просмотр всех параметров сайта".**</span><span class="sxs-lookup"><span data-stu-id="4a116-129">Go to **Site information**>**View all site settings**.</span></span>
3. <span data-ttu-id="4a116-130">Перейдите в раздел Поиска (Майкрософт) и выберите "Настройка **Поиска (Майкрософт) для этого веб-сайта".**</span><span class="sxs-lookup"><span data-stu-id="4a116-130">Go to the Microsoft Search section, then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="4a116-131">В области навигации перейдите к **пользовательскому опыту,** а затем выберите **"Вертикали".**</span><span class="sxs-lookup"><span data-stu-id="4a116-131">In the navigation pane, go to **Custom experience**, then select **Verticals**.</span></span>
5. <span data-ttu-id="4a116-132">Выберите **вертикаль "Все",** а затем включении **результата "Показать результаты соединителя".**</span><span class="sxs-lookup"><span data-stu-id="4a116-132">Select the **All** vertical, then enable **Show connector results**.</span></span>

## <a name="view-the-result-cluster-experience-after-it-is-enabled"></a><span data-ttu-id="4a116-133">Просмотр работы кластера результатов после включения</span><span class="sxs-lookup"><span data-stu-id="4a116-133">View the result cluster experience after it is enabled</span></span>

<span data-ttu-id="4a116-134">После того как вы включите кластер результатов, его просмотр может занять до 12 часов.</span><span class="sxs-lookup"><span data-stu-id="4a116-134">After you turn on the result cluster experience, it can take up to 12 hours before you can view it.</span></span> <span data-ttu-id="4a116-135">Если вы хотите сразу же получить нужный опыт, можно применить *cacheClear=true* к URL-адресу в SharePoint и Office.</span><span class="sxs-lookup"><span data-stu-id="4a116-135">If you want the experience immediately, you can append *cacheClear=true* to the URL in SharePoint and Office.</span></span>
