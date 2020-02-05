---
title: Управление вопросами и ответами
ms.author: jeffkizn
author: jeffkizn
manager: parulm
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
ms.openlocfilehash: 0877de027b68589e5ba15cd8109ea7edeeae8725
ms.sourcegitcommit: c22e8c3dcc53857da677db98a1a2b7d5ca2c6170
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "41721744"
---
# <a name="manage-qas"></a><span data-ttu-id="ec6b6-103">Управление вопросами и ответами</span><span class="sxs-lookup"><span data-stu-id="ec6b6-103">Manage Q&As</span></span>

<span data-ttu-id="ec6b6-104">Создание вопросов и ответов похоже на создание закладок.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-104">Creating a Q&A is similar to creating bookmarks.</span></span> <span data-ttu-id="ec6b6-105">Вопросы и ответы позволяют отвечать на вопросы пользователя, а не только предоставлять ссылку на веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-105">Q&A allows you to answer the user's question instead of just providing a link to webpage.</span></span> <span data-ttu-id="ec6b6-106">Вы можете представить ответ в виде форматированного текста с помощью доступных средств.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-106">You can format the answer in rich text using the available tools.</span></span> <span data-ttu-id="ec6b6-107">Если закладка и вопрос с ответом используют одинаковое ключевое слово, результат закладки отображается первым.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-107">If a Bookmark and a Q&A share the same keyword, the Bookmark result is shown first.</span></span> <span data-ttu-id="ec6b6-108">Как и для закладок, индекс вопросов и ответов обновляется сразу после добавления или изменения вопроса и ответа.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-108">Like Bookmarks, the Q&A index is refreshed immediately after a Q&A is added or changed.</span></span>

## <a name="add-or-edit-a-single-qa"></a><span data-ttu-id="ec6b6-109">Добавление и изменение одного вопроса с ответом</span><span class="sxs-lookup"><span data-stu-id="ec6b6-109">Add or edit a single Q&A</span></span>

1. <span data-ttu-id="ec6b6-110">Перейдите в **Центр администрирования Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-110">Go to **Microsoft 365 admin center**.</span></span>
1. <span data-ttu-id="ec6b6-111">В области навигации перейдите в **Параметры** и выберите **Поиск (Майкрософт)**.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-111">In the navigation pane, go to **Settings** and select **Microsoft Search**.</span></span>
1. <span data-ttu-id="ec6b6-112">Выберите вкладку **Вопросы и ответы**. По умолчанию выбрана первая вкладка (**Закладки**).</span><span class="sxs-lookup"><span data-stu-id="ec6b6-112">Select **Q&A** tab. By default, the first tab (**Bookmarks**) is selected.</span></span>
1. <span data-ttu-id="ec6b6-113">Чтобы добавить вопрос и ответ, нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-113">To add a Q&A, select **Add new**.</span></span>
<span data-ttu-id="ec6b6-114">Чтобы изменить вопрос и ответ, выберите вопрос и ответ в соответствующем списке.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-114">To edit a Q&A, select the Q&A in the relevant Q&A list.</span></span>
1. <span data-ttu-id="ec6b6-115">При добавлении или изменении сведений предварительное изображение автоматически обновляется.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-115">As you add or edit the information, the preview automatically updates.</span></span>
1. <span data-ttu-id="ec6b6-116">Сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-116">Save your changes.</span></span>

### <a name="supported-html-tags"></a><span data-ttu-id="ec6b6-117">Поддерживаемые теги HTML</span><span class="sxs-lookup"><span data-stu-id="ec6b6-117">Supported HTML tags</span></span>

<span data-ttu-id="ec6b6-118">В ответе (описании) можно использовать существующее HTML-содержимое или добавлять теги HTML.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-118">You can use existing HTML content or add HTML tags to your answer (description).</span></span> <span data-ttu-id="ec6b6-119">Неподдерживаемые теги игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-119">Unsupported tags are ignored.</span></span>  
<span data-ttu-id="ec6b6-120">Поддерживаются следующие HTML-теги:</span><span class="sxs-lookup"><span data-stu-id="ec6b6-120">The following HTML tags are supported:</span></span>

- <span data-ttu-id="ec6b6-121">blockquote</span><span class="sxs-lookup"><span data-stu-id="ec6b6-121">blockquote</span></span>
- <span data-ttu-id="ec6b6-122">div</span><span class="sxs-lookup"><span data-stu-id="ec6b6-122">div</span></span>
- <span data-ttu-id="ec6b6-123">em</span><span class="sxs-lookup"><span data-stu-id="ec6b6-123">em</span></span>
- <span data-ttu-id="ec6b6-124">h1, h2, h3 и h4</span><span class="sxs-lookup"><span data-stu-id="ec6b6-124">h1, h2, h3, and h4</span></span>
- <span data-ttu-id="ec6b6-125">ol, ul и li</span><span class="sxs-lookup"><span data-stu-id="ec6b6-125">ol, ul, and li</span></span>
- <span data-ttu-id="ec6b6-126">p</span><span class="sxs-lookup"><span data-stu-id="ec6b6-126">p</span></span>
- <span data-ttu-id="ec6b6-127">pre</span><span class="sxs-lookup"><span data-stu-id="ec6b6-127">pre</span></span>
- <span data-ttu-id="ec6b6-128">span</span><span class="sxs-lookup"><span data-stu-id="ec6b6-128">span</span></span>
- <span data-ttu-id="ec6b6-129">strong</span><span class="sxs-lookup"><span data-stu-id="ec6b6-129">strong</span></span>
- <span data-ttu-id="ec6b6-130">table, thead, tbody, tr, th и td</span><span class="sxs-lookup"><span data-stu-id="ec6b6-130">table, thead, tbody, tr, th, and td</span></span>
- <span data-ttu-id="ec6b6-131">u</span><span class="sxs-lookup"><span data-stu-id="ec6b6-131">u</span></span>
- <span data-ttu-id="ec6b6-132">a</span><span class="sxs-lookup"><span data-stu-id="ec6b6-132">a</span></span>
- <span data-ttu-id="ec6b6-133">code</span><span class="sxs-lookup"><span data-stu-id="ec6b6-133">code</span></span>
- <span data-ttu-id="ec6b6-134">br</span><span class="sxs-lookup"><span data-stu-id="ec6b6-134">br</span></span>
- <span data-ttu-id="ec6b6-135">hr</span><span class="sxs-lookup"><span data-stu-id="ec6b6-135">hr</span></span>
- <span data-ttu-id="ec6b6-136">img</span><span class="sxs-lookup"><span data-stu-id="ec6b6-136">img</span></span>

## <a name="add-or-edit-qas-using-browser-extensions"></a><span data-ttu-id="ec6b6-137">Добавление и редактирование&Q с использованием расширений браузера</span><span class="sxs-lookup"><span data-stu-id="ec6b6-137">Add or edit Q&As using browser extensions</span></span>

<span data-ttu-id="ec6b6-138">Администраторы поиска могут легко создавать контент поиска, используя расширения браузеров.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-138">Search administrators can create search content easily by using browser extensions.</span></span> <span data-ttu-id="ec6b6-139">Установите расширение браузера и перейдите к сайту, с которого требуется создать Q&A.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-139">Install the browser extension and then go to the site from which you want to generate a Q&A.</span></span> <span data-ttu-id="ec6b6-140">Затем можно создать Q&A и включить ссылку на исходный сайт.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-140">You can then create the Q&A and include a link to the source site.</span></span>

<span data-ttu-id="ec6b6-141">В настоящее время расширения браузеров доступны для Microsoft Edge и Chrome.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-141">Currently, browser extensions are available for Edge and Chrome.</span></span>

- <span data-ttu-id="ec6b6-142">Чтобы скачать пограничные расширения, перейдите в [Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab) и скачайте приложение.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-142">To download Edge extensions, go to [Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab) and download the app.</span></span>
- <span data-ttu-id="ec6b6-143">Чтобы скачать расширения Chrome, перейдите в [веб-магазин Chrome](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm) и скачайте приложение.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-143">To download Chrome extensions, go to [Chrome web store](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm) and download the app.</span></span>

## <a name="bulk-add-or-edit-qas"></a><span data-ttu-id="ec6b6-144">Массовое добавление и изменение вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="ec6b6-144">Bulk add or edit Q&As</span></span>

<span data-ttu-id="ec6b6-145">Администраторы могут использовать функции импорта и экспорта для массового создания и изменения вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-145">Administrators can use the Import and Export features to bulk create or edit Q&A.</span></span> <span data-ttu-id="ec6b6-146">Это удобная функция, если администратору нужно добавить или изменить большое количество вопросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-146">This is a useful feature when administrators need to add or edit a large number of Q&A.</span></span>

<span data-ttu-id="ec6b6-147">Используйте функции импорта и экспорта для следующих действий:</span><span class="sxs-lookup"><span data-stu-id="ec6b6-147">Use the import/export feature to:</span></span>

1. <span data-ttu-id="ec6b6-148">Массовое добавление вопросов и ответов. Добавьте сведения в файл шаблона вопросов с ответами и импортируйте его.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-148">Bulk add Q&A - Add details in the Q&A template file, and then import it.</span></span>
1. <span data-ttu-id="ec6b6-149">Массовое изменение вопросов и ответов. Экспортируйте вопросы и ответы в CSV-файл, измените сведения вопросов и ответов в экспортированном CSV-файле и импортируйте CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-149">Bulk edit Q&A - Export Q&A to a .csv file, then edit the Q&A details in the exported .csv file, and then import the .csv file.</span></span>
1. <span data-ttu-id="ec6b6-150">Создание резервной копии вопросов и ответов. Экспортируйте вопросы и ответы в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-150">Backup Q&A - Export Q&A to a .csv file.</span></span>

<span data-ttu-id="ec6b6-151">Чтобы импортировать или экспортировать вопросы и ответы:</span><span class="sxs-lookup"><span data-stu-id="ec6b6-151">To import or export Q&A:</span></span>

1. <span data-ttu-id="ec6b6-152">В правом верхнем углу вкладки вопросов и ответов выберите пункт **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-152">In the upper-right corner of the Q&A tab, select **Import**.</span></span>
<span data-ttu-id="ec6b6-153">Выберите пункт **Экспорт**, чтобы скачать все существующие вопросы и ответы в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-153">Select **Export** to download all the existing Q&A in a .csv file.</span></span>
1. <span data-ttu-id="ec6b6-154">В области справа выберите параметр для импорта с помощью CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-154">In the right pane, choose the option to import using a .csv file.</span></span>
<span data-ttu-id="ec6b6-155">Скачайте файл шаблона для списка обязательных полей и сведений.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-155">Download the template file for a list of the required fields and details.</span></span>
1. <span data-ttu-id="ec6b6-156">Добавьте или измените сведения вопросов и ответов в файле шаблона и сохраните его на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-156">Add or edit Q&A details in the template file and save it on your computer.</span></span>
1. <span data-ttu-id="ec6b6-157">В панели **Импорт вопросов и ответов** нажмите кнопку **Обзор** и выберите CSV-файл, который нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-157">In the **Import Q&A** pane, select **Browse**, and then the .csv file that you want to import.</span></span>
1. <span data-ttu-id="ec6b6-158">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-158">Select **Import**.</span></span>

<span data-ttu-id="ec6b6-159">Ниже приведены некоторые важные моменты, касающиеся файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-159">Here are some important points regarding the template file:</span></span>

- <span data-ttu-id="ec6b6-160">Никогда не изменяйте данные в следующих полях: *Id*, *Last Modified* и *Last Modified By*.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-160">Never edit data in these fields: *Id*, *Last Modified*, and *Last Modified By*</span></span>
- <span data-ttu-id="ec6b6-161">Если добавить *идентификатор* существующей закладки, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-161">If you include the *Id* of an existing bookmark, it will be replaced with the information in the import file.</span></span>
- <span data-ttu-id="ec6b6-162">Если есть закладка с таким же заголовком или URL-адресом, закладка будет обновлена с использованием сведений из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-162">If there is an existing bookmark with the same title or URL, the bookmark will be updated with information in the import file.</span></span>
- <span data-ttu-id="ec6b6-163">В файле шаблона требуются не все поля, а обязательные поля различаются в зависимости от состояния закладки.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-163">Not all fields in the template file are required and required fields vary depending on the bookmark state.</span></span>
- <span data-ttu-id="ec6b6-164">В зависимости от поля State закладки сохраняются в черновике, списке рекомендуемых или запланированных или публикуются автоматически.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-164">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>
- <span data-ttu-id="ec6b6-165">Для партнеров, которые управляют несколькими организациями, вы можете экспортировать свои закладки из одной организации и импортировать их в другую.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-165">For partners who manage multiple organizations, you can export your bookmarks from one org and import them into another.</span></span> <span data-ttu-id="ec6b6-166">Но перед импортом нужно удалить данные в столбце *Id*.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-166">But you must remove the data in the *Id* column before you import.</span></span>

<span data-ttu-id="ec6b6-167">**Примечание.** Вам не удастся импортировать вопросы и ответы, если в файле шаблона есть ошибки.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-167">**Note:** You cannot import Q&A if there are any errors in the template file.</span></span> <span data-ttu-id="ec6b6-168">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован и указаны все обязательные сведения.</span><span class="sxs-lookup"><span data-stu-id="ec6b6-168">To prevent errors, make sure your import file is properly formatted and include all the required information.</span></span>

<span data-ttu-id="ec6b6-169">Дополнительные сведения о том, как избежать ошибок, см. в разделе [Предотвращение ошибок импорта](manage-bookmarks.md#prevent-import-errors).</span><span class="sxs-lookup"><span data-stu-id="ec6b6-169">For more information on how to prevent error, see [Prevent import errors](manage-bookmarks.md#prevent-import-errors).</span></span>
