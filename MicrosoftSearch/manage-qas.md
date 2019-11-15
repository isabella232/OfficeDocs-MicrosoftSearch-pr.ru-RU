---
title: Управление вопросами и ответами
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 7e3432e6-5317-4d63-90b0-52da6fddd343
description: Находите и обновляйте ответы по отдельности или используйте имеющиеся инструменты Поиска (Майкрософт), чтобы изменить их все одновременно
ms.openlocfilehash: 903aab52e8d51e45588a390b5ccdccbaae2cf04a
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626777"
---
# <a name="manage-qas"></a><span data-ttu-id="b7ec7-103">Управление вопросами и ответами</span><span class="sxs-lookup"><span data-stu-id="b7ec7-103">Manage Q&As</span></span>

<span data-ttu-id="b7ec7-104">Создание вопросов и ответов похоже на создание закладок.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-104">Creating a Q&A is similar to creating bookmarks.</span></span> <span data-ttu-id="b7ec7-105">Вопросы и ответы позволяют отвечать на вопросы пользователя, а не только предоставлять ссылку на веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-105">Q&A allows you to answer the user's question instead of just providing a link to webpage.</span></span> <span data-ttu-id="b7ec7-106">Вы можете представить ответ в виде форматированного текста с помощью доступных средств.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-106">You can format the answer in rich text using the available tools.</span></span> <span data-ttu-id="b7ec7-107">Если закладка и вопрос с ответом используют одинаковое ключевое слово, результат закладки отображается первым.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-107">If a Bookmark and a Q&A share the same keyword, the Bookmark result is shown first.</span></span> <span data-ttu-id="b7ec7-108">Как и для закладок, индекс вопросов и ответов обновляется сразу после добавления или изменения вопроса и ответа.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-108">Like Bookmarks, the Q&A index is refreshed immediately after a Q&A is added or changed.</span></span> 

## <a name="add-or-edit-a-single-qa"></a><span data-ttu-id="b7ec7-109">Добавление и изменение одного вопроса с ответом</span><span class="sxs-lookup"><span data-stu-id="b7ec7-109">Add or edit a single Q&A</span></span>
1. <span data-ttu-id="b7ec7-110">Перейдите в **Центр администрирования Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-110">Go to **Microsoft 365 admin center**.</span></span>
1. <span data-ttu-id="b7ec7-111">В области навигации перейдите в **Параметры** и выберите **Поиск (Майкрософт)**.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-111">In the navigation pane, go to **Settings** and select **Microsoft Search**.</span></span>
1. <span data-ttu-id="b7ec7-112">Выберите вкладку **Вопросы и ответы**. По умолчанию выбрана первая вкладка (**Закладки**).</span><span class="sxs-lookup"><span data-stu-id="b7ec7-112">Select **Q&A** tab. By default, the first tab (**Bookmarks**) is selected.</span></span>
1. <span data-ttu-id="b7ec7-113">Чтобы добавить вопрос и ответ, нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-113">To add a Q&A, select **Add new**.</span></span>
<span data-ttu-id="b7ec7-114">Чтобы изменить вопрос и ответ, выберите вопрос и ответ в соответствующем списке.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-114">To edit a Q&A, select the Q&A in the relevant Q&A list.</span></span>
1. <span data-ttu-id="b7ec7-115">При добавлении или изменении сведений предварительное изображение автоматически обновляется.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-115">As you add or edit the information, the preview automatically updates.</span></span>
1. <span data-ttu-id="b7ec7-116">Сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-116">Save your changes.</span></span>

### <a name="supported-html-tags"></a><span data-ttu-id="b7ec7-117">Поддерживаемые теги HTML</span><span class="sxs-lookup"><span data-stu-id="b7ec7-117">Supported HTML tags</span></span>
<span data-ttu-id="b7ec7-118">В ответе (описании) можно использовать существующее HTML-содержимое или добавлять теги HTML.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-118">You can use existing HTML content or add HTML tags to your answer (description).</span></span> <span data-ttu-id="b7ec7-119">Неподдерживаемые теги игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-119">Unsupported tags are ignored.</span></span>  
<span data-ttu-id="b7ec7-120">Поддерживаются следующие HTML-теги:</span><span class="sxs-lookup"><span data-stu-id="b7ec7-120">The following HTML tags are supported:</span></span>
- <span data-ttu-id="b7ec7-121">blockquote</span><span class="sxs-lookup"><span data-stu-id="b7ec7-121">blockquote</span></span>
- <span data-ttu-id="b7ec7-122">div</span><span class="sxs-lookup"><span data-stu-id="b7ec7-122">div</span></span>
- <span data-ttu-id="b7ec7-123">em</span><span class="sxs-lookup"><span data-stu-id="b7ec7-123">em</span></span>
- <span data-ttu-id="b7ec7-124">h1, h2, h3 и h4</span><span class="sxs-lookup"><span data-stu-id="b7ec7-124">h1, h2, h3, and h4</span></span>
- <span data-ttu-id="b7ec7-125">ol, ul и li</span><span class="sxs-lookup"><span data-stu-id="b7ec7-125">ol, ul, and li</span></span>
- <span data-ttu-id="b7ec7-126">p</span><span class="sxs-lookup"><span data-stu-id="b7ec7-126">p</span></span>
- <span data-ttu-id="b7ec7-127">pre</span><span class="sxs-lookup"><span data-stu-id="b7ec7-127">pre</span></span>
- <span data-ttu-id="b7ec7-128">span</span><span class="sxs-lookup"><span data-stu-id="b7ec7-128">span</span></span>
- <span data-ttu-id="b7ec7-129">strong</span><span class="sxs-lookup"><span data-stu-id="b7ec7-129">strong</span></span>
- <span data-ttu-id="b7ec7-130">table, thead, tbody, tr, th и td</span><span class="sxs-lookup"><span data-stu-id="b7ec7-130">table, thead, tbody, tr, th, and td</span></span>
- <span data-ttu-id="b7ec7-131">u</span><span class="sxs-lookup"><span data-stu-id="b7ec7-131">u</span></span>
- <span data-ttu-id="b7ec7-132">a</span><span class="sxs-lookup"><span data-stu-id="b7ec7-132">a</span></span>
- <span data-ttu-id="b7ec7-133">code</span><span class="sxs-lookup"><span data-stu-id="b7ec7-133">code</span></span>
- <span data-ttu-id="b7ec7-134">br</span><span class="sxs-lookup"><span data-stu-id="b7ec7-134">br</span></span>
- <span data-ttu-id="b7ec7-135">hr</span><span class="sxs-lookup"><span data-stu-id="b7ec7-135">hr</span></span>
- <span data-ttu-id="b7ec7-136">img</span><span class="sxs-lookup"><span data-stu-id="b7ec7-136">img</span></span>

## <a name="bulk-add-or-edit-qas"></a><span data-ttu-id="b7ec7-137">Массовое добавление и изменение вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="b7ec7-137">Bulk add or edit Q&As</span></span>
<span data-ttu-id="b7ec7-138">Администраторы могут использовать функции импорта и экспорта для массового создания и изменения вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-138">Administrators can use the Import and Export features to bulk create or edit Q&A.</span></span> <span data-ttu-id="b7ec7-139">Это удобная функция, если администратору нужно добавить или изменить большое количество вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-139">This is a useful feature when administrators need to add or edit a large number of Q&A.</span></span> 

<span data-ttu-id="b7ec7-140">Используйте функции импорта и экспорта для следующих действий:</span><span class="sxs-lookup"><span data-stu-id="b7ec7-140">Use the import/export feature to:</span></span>
1. <span data-ttu-id="b7ec7-141">Массовое добавление вопросов и ответов. Добавьте сведения в файл шаблона вопросов с ответами и импортируйте его.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-141">Bulk add Q&A - Add details in the Q&A template file, and then import it.</span></span>
1. <span data-ttu-id="b7ec7-142">Массовое изменение вопросов и ответов. Экспортируйте вопросы и ответы в CSV-файл, измените сведения вопросов и ответов в экспортированном CSV-файле и импортируйте CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-142">Bulk edit Q&A - Export Q&A to a .csv file, then edit the Q&A details in the exported .csv file, and then import the .csv file.</span></span>
1. <span data-ttu-id="b7ec7-143">Создание резервной копии вопросов и ответов. Экспортируйте вопросы и ответы в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-143">Backup Q&A - Export Q&A to a .csv file.</span></span>

<span data-ttu-id="b7ec7-144">Чтобы импортировать или экспортировать вопросы и ответы:</span><span class="sxs-lookup"><span data-stu-id="b7ec7-144">To import or export Q&A:</span></span>
1. <span data-ttu-id="b7ec7-145">В правом верхнем углу вкладки вопросов и ответов выберите пункт **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-145">In the upper-right corner of the Q&A tab, select **Import**.</span></span> <span data-ttu-id="b7ec7-146">Выберите пункт **Экспорт**, чтобы скачать все существующие вопросы и ответы в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-146">Select **Export** to download all the existing Q&A in a .csv file.</span></span>
1. <span data-ttu-id="b7ec7-147">В области справа выберите параметр для импорта с помощью CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-147">In the right pane, choose the option to import using a .csv file.</span></span>
<span data-ttu-id="b7ec7-148">Скачайте файл шаблона для списка обязательных полей и сведений.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-148">Download the template file for a list of the required fields and details.</span></span> 
1. <span data-ttu-id="b7ec7-149">Добавьте или измените сведения вопросов и ответов в файле шаблона и сохраните его на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-149">Add or edit Q&A details in the template file and save it on your computer.</span></span> 
1. <span data-ttu-id="b7ec7-150">В панели **Импорт вопросов и ответов** нажмите кнопку **Обзор** и выберите CSV-файл, который нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-150">In the **Import Q&A** pane, select **Browse**, and then the .csv file that you want to import.</span></span>
1. <span data-ttu-id="b7ec7-151">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-151">Select **Import**.</span></span>

<span data-ttu-id="b7ec7-152">Ниже приведены некоторые важные моменты, касающиеся файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-152">Here are some important points regarding the template file:</span></span>
- <span data-ttu-id="b7ec7-153">Никогда не изменяйте данные в следующих полях: *Id*, *Last Modified* и *Last Modified By*.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-153">Never edit data in these fields: *Id*, *Last Modified*, and *Last Modified By*</span></span>
- <span data-ttu-id="b7ec7-154">Если добавить *идентификатор* существующей закладки, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-154">If you include the *Id* of an existing bookmark, it will be replaced with the information in the import file.</span></span>
- <span data-ttu-id="b7ec7-155">Если есть закладка с таким же заголовком или URL-адресом, закладка будет обновлена с использованием сведений из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-155">If there is an existing bookmark with the same title or URL, the bookmark will be updated with information in the import file.</span></span>
- <span data-ttu-id="b7ec7-156">В файле шаблона требуются не все поля, а обязательные поля различаются в зависимости от состояния закладки.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-156">Not all fields in the template file are required and required fields vary depending on the bookmark state.</span></span>
- <span data-ttu-id="b7ec7-157">В зависимости от поля State закладки сохраняются в черновике, списке рекомендуемых или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-157">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>
- <span data-ttu-id="b7ec7-158">Для партнеров, которые управляют несколькими организациями, вы можете экспортировать свои закладки из одной организации и импортировать их в другую.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-158">For partners who manage multiple organizations, you can export your bookmarks from one org and import them into another.</span></span> <span data-ttu-id="b7ec7-159">Но перед импортом нужно удалить данные в столбце *Id*.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-159">But you must remove the data in the *Id* column before you import.</span></span>

<span data-ttu-id="b7ec7-160">**Примечание.** Вам не удастся импортировать вопросы и ответы, если в файле шаблона есть ошибки.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-160">**Note:** You cannot import Q&A if there are any errors in the template file.</span></span> <span data-ttu-id="b7ec7-161">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован и указаны все обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-161">To prevent errors, make sure your import file is properly formatted and include all the required information.</span></span> 

<span data-ttu-id="b7ec7-162">Дополнительные сведения о том, как избежать ошибок, см. в разделе [Предотвращение ошибок импорта](manage-bookmarks.md#prevent-import-errors).</span><span class="sxs-lookup"><span data-stu-id="b7ec7-162">For more information on how to prevent error, see [Prevent import errors](manage-bookmarks.md#prevent-import-errors).</span></span>