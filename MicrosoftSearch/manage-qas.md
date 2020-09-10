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
description: Поиск и обновление ответов по отдельности или использование доступных средств поиска Microsoft для одновременного редактирования&Q.
ms.openlocfilehash: 2a8b0727ef3540a35d617cf6c8bae7b0d99767a8
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "47423003"
---
# <a name="manage-qas"></a><span data-ttu-id="5d147-103">Управление вопросами и ответами</span><span class="sxs-lookup"><span data-stu-id="5d147-103">Manage Q&As</span></span>

<span data-ttu-id="5d147-104">Создание вопросов и ответов похоже на создание закладок.</span><span class="sxs-lookup"><span data-stu-id="5d147-104">Creating a Q&A is similar to creating bookmarks.</span></span> <span data-ttu-id="5d147-105">Q&, что позволяет отвечать на вопросы пользователя, а не только для ссылки на веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="5d147-105">Q&As allow you to answer the user's questions instead of just providing a link to a webpage.</span></span> <span data-ttu-id="5d147-106">Вы также можете отформатировать ответ в формате форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="5d147-106">You can also format the answer in rich text.</span></span> <span data-ttu-id="5d147-107">Если закладка и Q&A используют одно и то же ключевое слово, сначала отображается результат закладки.</span><span class="sxs-lookup"><span data-stu-id="5d147-107">If a bookmark and a Q&A share the same keyword, the bookmark result is shown first.</span></span> <span data-ttu-id="5d147-108">Как и закладки,&Q обновляется сразу после добавления или изменения Q&A.</span><span class="sxs-lookup"><span data-stu-id="5d147-108">Like bookmarks, the Q&A index is refreshed immediately after a Q&A is added or changed.</span></span>

## <a name="add-or-edit-a-single-qa"></a><span data-ttu-id="5d147-109">Добавление и изменение одного вопроса с ответом</span><span class="sxs-lookup"><span data-stu-id="5d147-109">Add or edit a single Q&A</span></span>

1. <span data-ttu-id="5d147-110">В [центре администрирования Microsoft 365](https://admin.microsoft.com)откройте раздел [**Q&A**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/qnas)</span><span class="sxs-lookup"><span data-stu-id="5d147-110">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Q&A**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/qnas)</span></span>
1. <span data-ttu-id="5d147-111">Чтобы добавить Q&а, нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5d147-111">To add a Q&A, select **Add**.</span></span>
<span data-ttu-id="5d147-112">Чтобы изменить вопрос и ответ, выберите вопрос и ответ в соответствующем списке.</span><span class="sxs-lookup"><span data-stu-id="5d147-112">To edit a Q&A, select the Q&A in the relevant Q&A list.</span></span> <span data-ttu-id="5d147-113">При добавлении или изменении сведений предварительное изображение автоматически обновляется.</span><span class="sxs-lookup"><span data-stu-id="5d147-113">As you add or edit the information, the preview automatically updates.</span></span>
1. <span data-ttu-id="5d147-114">Сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="5d147-114">Save your changes.</span></span>

### <a name="supported-html-tags"></a><span data-ttu-id="5d147-115">Поддерживаемые теги HTML</span><span class="sxs-lookup"><span data-stu-id="5d147-115">Supported HTML tags</span></span>

<span data-ttu-id="5d147-116">В ответе (описании) можно использовать существующее HTML-содержимое или добавлять теги HTML.</span><span class="sxs-lookup"><span data-stu-id="5d147-116">You can use existing HTML content or add HTML tags to your answer (description).</span></span> <span data-ttu-id="5d147-117">Неподдерживаемые теги игнорируются.</span><span class="sxs-lookup"><span data-stu-id="5d147-117">Unsupported tags are ignored.</span></span>

<span data-ttu-id="5d147-118">Поддерживаются следующие HTML-теги:</span><span class="sxs-lookup"><span data-stu-id="5d147-118">The following HTML tags are supported:</span></span>

- <span data-ttu-id="5d147-119">blockquote</span><span class="sxs-lookup"><span data-stu-id="5d147-119">blockquote</span></span>
- <span data-ttu-id="5d147-120">div</span><span class="sxs-lookup"><span data-stu-id="5d147-120">div</span></span>
- <span data-ttu-id="5d147-121">em</span><span class="sxs-lookup"><span data-stu-id="5d147-121">em</span></span>
- <span data-ttu-id="5d147-122">h1, h2, h3 и h4</span><span class="sxs-lookup"><span data-stu-id="5d147-122">h1, h2, h3, and h4</span></span>
- <span data-ttu-id="5d147-123">ol, ul и li</span><span class="sxs-lookup"><span data-stu-id="5d147-123">ol, ul, and li</span></span>
- <span data-ttu-id="5d147-124">p</span><span class="sxs-lookup"><span data-stu-id="5d147-124">p</span></span>
- <span data-ttu-id="5d147-125">pre</span><span class="sxs-lookup"><span data-stu-id="5d147-125">pre</span></span>
- <span data-ttu-id="5d147-126">span</span><span class="sxs-lookup"><span data-stu-id="5d147-126">span</span></span>
- <span data-ttu-id="5d147-127">strong</span><span class="sxs-lookup"><span data-stu-id="5d147-127">strong</span></span>
- <span data-ttu-id="5d147-128">table, thead, tbody, tr, th и td</span><span class="sxs-lookup"><span data-stu-id="5d147-128">table, thead, tbody, tr, th, and td</span></span>
- <span data-ttu-id="5d147-129">u</span><span class="sxs-lookup"><span data-stu-id="5d147-129">u</span></span>
- <span data-ttu-id="5d147-130">a</span><span class="sxs-lookup"><span data-stu-id="5d147-130">a</span></span>
- <span data-ttu-id="5d147-131">code</span><span class="sxs-lookup"><span data-stu-id="5d147-131">code</span></span>
- <span data-ttu-id="5d147-132">br</span><span class="sxs-lookup"><span data-stu-id="5d147-132">br</span></span>
- <span data-ttu-id="5d147-133">hr</span><span class="sxs-lookup"><span data-stu-id="5d147-133">hr</span></span>
- <span data-ttu-id="5d147-134">img</span><span class="sxs-lookup"><span data-stu-id="5d147-134">img</span></span>

## <a name="add-or-edit-qas-using-browser-extensions"></a><span data-ttu-id="5d147-135">Добавление и редактирование&Q с использованием расширений браузера</span><span class="sxs-lookup"><span data-stu-id="5d147-135">Add or edit Q&As using browser extensions</span></span>

<span data-ttu-id="5d147-136">Администраторы поиска могут легко создавать контент поиска, используя расширения браузеров.</span><span class="sxs-lookup"><span data-stu-id="5d147-136">Search administrators can create search content easily by using browser extensions.</span></span> <span data-ttu-id="5d147-137">Установите расширение браузера, а затем перейдите на сайт, с которого нужно создать Q&A.</span><span class="sxs-lookup"><span data-stu-id="5d147-137">Install the browser extension, and then go to the site from which you want to generate a Q&A.</span></span> <span data-ttu-id="5d147-138">Затем можно создать Q&A и включить ссылку на исходный сайт.</span><span class="sxs-lookup"><span data-stu-id="5d147-138">You can then create the Q&A and include a link to the source site.</span></span>

<span data-ttu-id="5d147-139">В настоящее время расширения браузера доступны для Microsoft EDGE и Chrome.</span><span class="sxs-lookup"><span data-stu-id="5d147-139">Currently, browser extensions are available for Microsoft Edge and Chrome.</span></span>

- <span data-ttu-id="5d147-140">Чтобы скачать расширения для пограничной (устаревшей версии), перейдите в [Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab).</span><span class="sxs-lookup"><span data-stu-id="5d147-140">To download extensions for Edge (Legacy), go to [Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab).</span></span>
- <span data-ttu-id="5d147-141">Чтобы скачать расширения Chrome или EDGE (Чромиум), перейдите в [веб-магазин Chrome](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm).</span><span class="sxs-lookup"><span data-stu-id="5d147-141">To download extensions Chrome or Edge (Chromium), go to the [Chrome web store](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm).</span></span>

## <a name="bulk-add-or-edit-qas"></a><span data-ttu-id="5d147-142">Массовое добавление и изменение вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="5d147-142">Bulk add or edit Q&As</span></span>

<span data-ttu-id="5d147-143">Администраторы могут использовать функции импорта и экспорта для массового создания или редактирования Q&как.</span><span class="sxs-lookup"><span data-stu-id="5d147-143">Administrators can use the Import and Export features to bulk create or edit Q&As.</span></span>

<span data-ttu-id="5d147-144">С помощью функции импорта и экспорта можно:</span><span class="sxs-lookup"><span data-stu-id="5d147-144">Use the Import/Export feature to:</span></span>

- <span data-ttu-id="5d147-145">Выполните массовое добавление&Q с добавлением сведений в файл Q&шаблона, а затем импортируйте его.</span><span class="sxs-lookup"><span data-stu-id="5d147-145">Bulk add Q&As - Add details in the Q&A template file, and then import it.</span></span>
- <span data-ttu-id="5d147-146">Массовое изменение Q&AS-Export Q&как в CSV-файл, измените Q&сведения в экспортированном файле, а затем импортируйте файл.</span><span class="sxs-lookup"><span data-stu-id="5d147-146">Bulk edit Q&As - Export Q&As to a .csv file, edit the Q&A details in the exported file, and then import the file.</span></span>
- <span data-ttu-id="5d147-147">Выполните резервное копирование Q&AS-Export Q&как CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="5d147-147">Back up Q&As - Export Q&As to a .csv file.</span></span>

<span data-ttu-id="5d147-148">Чтобы импортировать или экспортировать Q&как:</span><span class="sxs-lookup"><span data-stu-id="5d147-148">To import or export Q&As:</span></span>

1. <span data-ttu-id="5d147-149">В правом верхнем углу вкладки вопросов и ответов выберите пункт **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="5d147-149">In the upper-right corner of the Q&A tab, select **Import**.</span></span>
<span data-ttu-id="5d147-150">Выберите пункт **Экспорт** , чтобы скачать все существующие&Q как в CSV-файле.</span><span class="sxs-lookup"><span data-stu-id="5d147-150">Select **Export** to download all the existing Q&As in a .csv file.</span></span>
1. <span data-ttu-id="5d147-151">В правой области выберите параметр для импорта с помощью CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="5d147-151">In the right pane, select the option to import by using a .csv file.</span></span> <span data-ttu-id="5d147-152">Скачайте файл шаблона, чтобы получить список обязательных полей и сведений.</span><span class="sxs-lookup"><span data-stu-id="5d147-152">Download the template file to get a list of the required fields and details.</span></span>
1. <span data-ttu-id="5d147-153">Добавьте или измените Q&сведения в файле шаблона и сохраните его на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="5d147-153">Add or edit Q&A details in the template file, and save it on your computer.</span></span>
1. <span data-ttu-id="5d147-154">В области **Импорт Q&A** нажмите кнопку **Обзор**, а затем выберите CSV-файл, который требуется импортировать.</span><span class="sxs-lookup"><span data-stu-id="5d147-154">In the **Import Q&A** pane, select **Browse**, and then select the .csv file that you want to import.</span></span>
1. <span data-ttu-id="5d147-155">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="5d147-155">Select **Import**.</span></span>

<span data-ttu-id="5d147-156">Важные советы по файлам шаблонов:</span><span class="sxs-lookup"><span data-stu-id="5d147-156">Important template file tips:</span></span>

- <span data-ttu-id="5d147-157">Никогда не изменяйте данные в следующих полях: **Id**, **Last Modified** и **Last Modified By**.</span><span class="sxs-lookup"><span data-stu-id="5d147-157">Never edit data in these fields: **Id**, **Last Modified**, and **Last Modified By**</span></span>
- <span data-ttu-id="5d147-158">Если добавить **идентификатор** существующей закладки, он будет заменен сведениями из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="5d147-158">If you include the **Id** of an existing bookmark, it will be replaced with the information in the import file.</span></span>
- <span data-ttu-id="5d147-159">Если у вас есть закладка с таким же названием или URL-адресом, закладка будет обновлена данными из файла импорта.</span><span class="sxs-lookup"><span data-stu-id="5d147-159">If there's an existing bookmark that has the same title or URL, the bookmark will be updated with information in the import file.</span></span>
- <span data-ttu-id="5d147-160">Не все поля в файле шаблона являются обязательными, а обязательные поля зависят от состояния закладки.</span><span class="sxs-lookup"><span data-stu-id="5d147-160">Not all fields in the template file are required, and the required fields vary depending on the bookmark state.</span></span>
- <span data-ttu-id="5d147-161">В зависимости от поля **состояние** закладки сохраняются как *Черновики*, *предложенные*или *запланированные*или автоматически публикуются.</span><span class="sxs-lookup"><span data-stu-id="5d147-161">Based on the **State** field, bookmarks are saved as *draft*, *suggested*, or *scheduled*, or they are published automatically.</span></span>
- <span data-ttu-id="5d147-162">Для партнеров, которые управляют несколькими организациями: вы можете экспортировать свои закладки из одной организации и импортировать их в другую.</span><span class="sxs-lookup"><span data-stu-id="5d147-162">For partners who manage multiple organizations: You can export your bookmarks from one org and import them into another.</span></span> <span data-ttu-id="5d147-163">Но перед импортом нужно удалить данные в столбце **Id**.</span><span class="sxs-lookup"><span data-stu-id="5d147-163">But you must remove the data in the **Id** column before you import.</span></span>

> [!NOTE]
> <span data-ttu-id="5d147-164">Вы не можете импортировать Q&так, как если бы в файле шаблона возникли ошибки.</span><span class="sxs-lookup"><span data-stu-id="5d147-164">You can't import Q&As if there are any errors in the template file.</span></span> <span data-ttu-id="5d147-165">Чтобы избежать ошибок, убедитесь, что файл импорта правильно отформатирован, и включите все необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="5d147-165">To prevent errors, make sure your import file is properly formatted, and include all the required information.</span></span>

<span data-ttu-id="5d147-166">Для получения дополнительных сведений об устранении ошибок обратитесь к разделу [предотвращение ошибок импорта](manage-bookmarks.md#prevent-import-errors).</span><span class="sxs-lookup"><span data-stu-id="5d147-166">For more information about avoiding errors, see [Prevent import errors](manage-bookmarks.md#prevent-import-errors).</span></span>
