---
title: Предварительный просмотр соединителей
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
description: Дополнительные сведения о Microsoft Graph Connectors Preview for Microsoft Search.
ms.openlocfilehash: 4bcd8360957be69bc701e8b356cd222de32bfc5f
ms.sourcegitcommit: 64eea81f8c1db9ee955013462a7b51612fb7d0b7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "44604386"
---
# <a name="microsoft-graph-connectors-preview"></a><span data-ttu-id="430e2-103">Предварительная версия соединителей Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="430e2-103">Microsoft Graph connectors preview</span></span>

<span data-ttu-id="430e2-104">Microsoft Graph Connectors и API службы поиска Microsoft (запрос и индекс) в настоящее время находятся в состоянии предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="430e2-104">Microsoft Graph connectors and Microsoft Search APIs (query and index) are currently in preview status.</span></span> <span data-ttu-id="430e2-105">Чтобы получить доступ к функциональным возможностям соединителей, необходимо включить параметр целевого выпуска в клиенте.</span><span class="sxs-lookup"><span data-stu-id="430e2-105">To gain access to connectors functionality, you must turn on the Targeted release option in your tenant.</span></span> <span data-ttu-id="430e2-106">Это раннее Предварительная версия, и отсутствует гарантия уровня обслуживания.</span><span class="sxs-lookup"><span data-stu-id="430e2-106">This is an early preview, and there's no service level guarantee.</span></span> <span data-ttu-id="430e2-107">Мы рекомендуем пользователям попытаться воспользоваться функциями соединителей и отправить свои отзывы.</span><span class="sxs-lookup"><span data-stu-id="430e2-107">We encourage customers to try connectors functionality and provide feedback.</span></span> <span data-ttu-id="430e2-108">Мы не рекомендуем использовать соединители для производственных целей во время ознакомительного периода.</span><span class="sxs-lookup"><span data-stu-id="430e2-108">We don’t recommend using connectors for production purposes during the preview period.</span></span>

## <a name="set-up-targeted-release"></a><span data-ttu-id="430e2-109">Настройка целевого выпуска</span><span class="sxs-lookup"><span data-stu-id="430e2-109">Set up Targeted release</span></span>

<span data-ttu-id="430e2-110">Чтобы попробовать соединители, для всех пользователей в Организации должен быть установлен параметр **целевой выпуск** .</span><span class="sxs-lookup"><span data-stu-id="430e2-110">To try connectors, you must have the **Targeted release** option set for all users in your organization.</span></span> <span data-ttu-id="430e2-111">Чтобы узнать больше о параметрах целевого выпуска и способах его установки, ознакомьтесь [со статьей Настройка стандартных или целевых вариантов выпуска в Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="430e2-111">To learn more about the Targeted release option and how to set it, see [Set up the Standard or Targeted release options in Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span></span>

## <a name="choose-a-preview-environment"></a><span data-ttu-id="430e2-112">Выбор среды предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="430e2-112">Choose a preview environment</span></span>

<span data-ttu-id="430e2-113">Чтобы испытать соединители, API индексирования и API поиска, рекомендуется использовать следующие два метода:</span><span class="sxs-lookup"><span data-stu-id="430e2-113">To try connectors, indexing APIs, and search APIs, we recommend these two methods:</span></span>

1. <span data-ttu-id="430e2-114">**Тестового клиента**.</span><span class="sxs-lookup"><span data-stu-id="430e2-114">**Test tenant**.</span></span>  <span data-ttu-id="430e2-115">Мы рекомендуем использовать тестовый клиент, чтобы попробовать предварительную версию Microsoft Graph Connectors.</span><span class="sxs-lookup"><span data-stu-id="430e2-115">We encourage you to use a test tenant to try the Microsoft Graph connectors preview.</span></span>

2. <span data-ttu-id="430e2-116">**Проверка семейства веб-сайтов**.</span><span class="sxs-lookup"><span data-stu-id="430e2-116">**Test site collection**.</span></span> <span data-ttu-id="430e2-117">Если у вас нет тестового клиента, вы можете создать тестовое семейство веб-сайтов, чтобы испытать функциональные возможности соединителей.</span><span class="sxs-lookup"><span data-stu-id="430e2-117">If you don't have a test tenant, you can create a test site collection to try out connectors functionality.</span></span> <span data-ttu-id="430e2-118">Чтобы показать результаты из соединителей, не влияя страницы поиска в любом месте Организации, настройте поисковый интерфейс только для этого семейства веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="430e2-118">To show results from connectors without impacting the search pages anywhere else in your organization, customize the search experience of only that site collection.</span></span>

## <a name="preview-limitations"></a><span data-ttu-id="430e2-119">Ограничения на предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="430e2-119">Preview limitations</span></span>

<span data-ttu-id="430e2-120">Предварительный выпуск имеет следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="430e2-120">The preview release has the following limitations:</span></span>

* <span data-ttu-id="430e2-121">Пропускная способность приема регулируется около четырех элементов в секунду.</span><span class="sxs-lookup"><span data-stu-id="430e2-121">Ingestion throughput is throttled at about four items per second.</span></span>

* <span data-ttu-id="430e2-122">Обновления схемы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="430e2-122">There's no support for schema updates.</span></span> <span data-ttu-id="430e2-123">После создания настройки подключения невозможно обновить схему.</span><span class="sxs-lookup"><span data-stu-id="430e2-123">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="430e2-124">Вы можете удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="430e2-124">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="430e2-125">Индексированное содержимое отображается только на странице результатов поиска под пользовательским вертикальным расположением.</span><span class="sxs-lookup"><span data-stu-id="430e2-125">Indexed content only shows up in the search results page under a custom vertical.</span></span> <span data-ttu-id="430e2-126">Это ограничение применяется к контенту с пользовательскими типами.</span><span class="sxs-lookup"><span data-stu-id="430e2-126">This restriction applies to content with custom types.</span></span>

* <span data-ttu-id="430e2-127">Все подключения, настроенные в течение периода предварительного просмотра, могут потребоваться для удаления и повторного создания.</span><span class="sxs-lookup"><span data-stu-id="430e2-127">Any connection you set up during the preview period might need to be deleted and re-created.</span></span> <span data-ttu-id="430e2-128">Эти подключения больше не будут работать, если они несовместимы с изменениями, внесенными для усовершенствования продукта.</span><span class="sxs-lookup"><span data-stu-id="430e2-128">Those connections won't work anymore if they're incompatible with changes made to improve the product.</span></span>

* <span data-ttu-id="430e2-129">Превышено максимальное число подключений.</span><span class="sxs-lookup"><span data-stu-id="430e2-129">There's a connections limit.</span></span> <span data-ttu-id="430e2-130">Каждый клиент может создать до 10 подключений.</span><span class="sxs-lookup"><span data-stu-id="430e2-130">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="430e2-131">Размер исходного репозитория.</span><span class="sxs-lookup"><span data-stu-id="430e2-131">Source repository size.</span></span> <span data-ttu-id="430e2-132">Рекомендуется предварительно просмотреть соединители с исходным репозиторием около 200 000 элементов, так как это проверенный предельный размер шкалы поиска.</span><span class="sxs-lookup"><span data-stu-id="430e2-132">We recommend that you preview connectors with a source repository of about 200,000 items as this is our tested search scale limit.</span></span> <span data-ttu-id="430e2-133">Мы работаем над улучшением производительности поиска, и мы планируем поддерживать более крупные размеры репозитория в ближайшем будущем.</span><span class="sxs-lookup"><span data-stu-id="430e2-133">We are working on improving the performance of search, and we expect to support for larger repository sizes in the near future.</span></span>

* <span data-ttu-id="430e2-134">Изменение поддержки для подключения недоступно.</span><span class="sxs-lookup"><span data-stu-id="430e2-134">Edit support for connection is not available.</span></span> <span data-ttu-id="430e2-135">После создания подключения его нельзя изменить или изменить.</span><span class="sxs-lookup"><span data-stu-id="430e2-135">Once the connection has been created, you cannot edit or change it.</span></span> <span data-ttu-id="430e2-136">Если вам нужно изменить какие бы то ни было сведения, необходимо удалить и повторно создать подключение.</span><span class="sxs-lookup"><span data-stu-id="430e2-136">If you need to change any details, you must delete and recreate the connection.</span></span>

* <span data-ttu-id="430e2-137">Содержимое соединителя можно искать только на пользовательских вертикальных чертах.</span><span class="sxs-lookup"><span data-stu-id="430e2-137">Connector content can only be searched on custom verticals.</span></span>

* <span data-ttu-id="430e2-138">Содержимое соединителя только для одного подключения может отображаться в каждом настраиваемом вертикальном расположении и требует создания типа результатов.</span><span class="sxs-lookup"><span data-stu-id="430e2-138">Connector content from only one connection can be displayed in each custom vertical and requires result type creation.</span></span>
