---
title: Управление ответами на аббревиатуру в Microsoft Search
ms.author: rakkum
author: rakeshMSFT
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Создание и обновление ответов на аббревиатуры в Microsoft Search
ms.openlocfilehash: 013510da28599f41c9dc4bf74da99efa2f6c3e97
ms.sourcegitcommit: 62cb7b8c6a311760cc728f2c70a9a22ca76e977e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2021
ms.locfileid: "51408717"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="234e3-103">Управление ответами на аббревиатуры в Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="234e3-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="234e3-104">Пользователи часто используют незнакомые аббревиатуры и аббревиатуры, используемые их организацией или командой.</span><span class="sxs-lookup"><span data-stu-id="234e3-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="234e3-105">Термины, специфические для организаций или групп, могут быть новыми для людей, которые переходят из одной группы в другую, работают с внутренними группами партнеров или являются новыми для организации.</span><span class="sxs-lookup"><span data-stu-id="234e3-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="234e3-106">Организации не всегда имеют одну ссылку на стандартную терминологию.</span><span class="sxs-lookup"><span data-stu-id="234e3-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="234e3-107">Отсутствие единой ссылки затрудняет поиск определений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="234e3-107">Lack of a single reference makes it hard to find definitions for these acronyms.</span></span> <span data-ttu-id="234e3-108">Microsoft Search решает эту проблему с помощью аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="234e3-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="234e3-109">Что пользователи испытывают</span><span class="sxs-lookup"><span data-stu-id="234e3-109">What users experience</span></span>

<span data-ttu-id="234e3-110">Пользователи Microsoft Search могут получать определения с акронимами [в Bing,](https://Bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)и [Office 365.](https://Office.com)</span><span class="sxs-lookup"><span data-stu-id="234e3-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="234e3-111">В поле **Поиск** пользователи введите запросы, подобные этим примерам:</span><span class="sxs-lookup"><span data-stu-id="234e3-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="234e3-112">*Что такое* DNN</span><span class="sxs-lookup"><span data-stu-id="234e3-112">*What is* DNN</span></span>
- <span data-ttu-id="234e3-113">*Определение* DNN</span><span class="sxs-lookup"><span data-stu-id="234e3-113">*Define* DNN</span></span>
- <span data-ttu-id="234e3-114">Определение *DNN*</span><span class="sxs-lookup"><span data-stu-id="234e3-114">DNN *definition*</span></span>
- <span data-ttu-id="234e3-115">*Расширение* DNN</span><span class="sxs-lookup"><span data-stu-id="234e3-115">*Expand* DNN</span></span>
- <span data-ttu-id="234e3-116">Расширение *DNN*</span><span class="sxs-lookup"><span data-stu-id="234e3-116">DNN *expansion*</span></span>
- <span data-ttu-id="234e3-117">*Значение* DNN</span><span class="sxs-lookup"><span data-stu-id="234e3-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="234e3-118">DNN *означает*</span><span class="sxs-lookup"><span data-stu-id="234e3-118">DNN *means*</span></span>
- <span data-ttu-id="234e3-119">DNN *означает*</span><span class="sxs-lookup"><span data-stu-id="234e3-119">DNN *stands for*</span></span>

<span data-ttu-id="234e3-120">Результат включает все значения DNN, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="234e3-120">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="234e3-121">Пользователи должны ввести запрос, который включает указанные  ключевые слова аббревиатуры, чтобы вызвать соответствующие ответы.</span><span class="sxs-lookup"><span data-stu-id="234e3-121">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="234e3-122">Запросы аббревиатуры не являются конфиденциальными.</span><span class="sxs-lookup"><span data-stu-id="234e3-122">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="234e3-123">Настройка ответов на аббревиатуры</span><span class="sxs-lookup"><span data-stu-id="234e3-123">Set up acronyms answers</span></span>

<span data-ttu-id="234e3-124">В центре [администрирования Microsoft 365](https://admin.microsoft.com)перейдите к аббревиатуре, а затем выберите **добавить аббревиатура**. [](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)</span><span class="sxs-lookup"><span data-stu-id="234e3-124">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronym**.</span></span>

<span data-ttu-id="234e3-125">Microsoft Search запрашивает два источника данных для предоставления ответов на запросы пользователей по аббревиатуре:</span><span class="sxs-lookup"><span data-stu-id="234e3-125">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="234e3-126">**Администрирование.**</span><span class="sxs-lookup"><span data-stu-id="234e3-126">**Admin-curated**.</span></span> <span data-ttu-id="234e3-127">Предоставляется ИТ-администраторами в [центре администрирования.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)</span><span class="sxs-lookup"><span data-stu-id="234e3-127">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="234e3-128">**System-curated**.</span><span class="sxs-lookup"><span data-stu-id="234e3-128">**System-curated**.</span></span> <span data-ttu-id="234e3-129">Обнаружено в Microsoft Search из электронной почты и документов пользователей, а также общедоступных данных в организации.</span><span class="sxs-lookup"><span data-stu-id="234e3-129">Discovered by Microsoft Search from users' email and documents, as well as publicly available data within the organization.</span></span>

### <a name="set-up-admin-curated-acronyms"></a><span data-ttu-id="234e3-130">Настройка акронимов, курированных администратором</span><span class="sxs-lookup"><span data-stu-id="234e3-130">Set up Admin-curated acronyms</span></span>

<span data-ttu-id="234e3-131">Администраторы поиска могут добавлять аббревиатуры на вкладке [Acronyms](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) в центре администрирования [Microsoft Search.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)</span><span class="sxs-lookup"><span data-stu-id="234e3-131">Search administrators can add acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="234e3-132">В центр администрирования можно добавить аббревиатуры из любого внутреннего сайта или репозитория.</span><span class="sxs-lookup"><span data-stu-id="234e3-132">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="234e3-133">Эти аббревиатуры можно добавить в **состояние Published** или **Draft:**</span><span class="sxs-lookup"><span data-stu-id="234e3-133">These acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="234e3-134">**Опубликовано состояние**.</span><span class="sxs-lookup"><span data-stu-id="234e3-134">**Published state**.</span></span> <span data-ttu-id="234e3-135">Аббревиатуры доступны пользователям организации с помощью Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="234e3-135">Acronyms are available to the organization’s users through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="234e3-136">Для того чтобы аббревиатуры, добавленные в состояние Published, стали доступными в Microsoft Search, может потребоваться до трех дней.</span><span class="sxs-lookup"><span data-stu-id="234e3-136">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="234e3-137">**Состояние Черновика.**</span><span class="sxs-lookup"><span data-stu-id="234e3-137">**Draft state**.</span></span> <span data-ttu-id="234e3-138">Если вы хотите просмотреть аббревиатуру, прежде чем сделать ее доступной в Microsoft Search, можно добавить аббревиатура в состояние Draft.</span><span class="sxs-lookup"><span data-stu-id="234e3-138">If you want to review an acronym before making it available in Microsoft Search, you can add the acronym in a Draft state.</span></span> <span data-ttu-id="234e3-139">Акронимы в состоянии Draft не отображаются в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="234e3-139">Acronyms in the Draft state will not appear in search results.</span></span> <span data-ttu-id="234e3-140">Чтобы она появлялась в результатах поиска, необходимо переместить аббревиатура в состояние Published.</span><span class="sxs-lookup"><span data-stu-id="234e3-140">You will need to move the acronym to the Published state to make it appear in search results.</span></span>

<span data-ttu-id="234e3-141">**Исключено состояние**.</span><span class="sxs-lookup"><span data-stu-id="234e3-141">**Excluded state**.</span></span> <span data-ttu-id="234e3-142">Чтобы не допустить появления аббревиатуры в Microsoft Search, используйте **исключение** аббревиатуры, чтобы добавить ее.</span><span class="sxs-lookup"><span data-stu-id="234e3-142">If you want to prevent an acronym from appearing in Microsoft Search, use **Exclude an acronym** to add it.</span></span> <span data-ttu-id="234e3-143">Чтобы исключить аббревиатура, необходимо удалить исключенную аббревиатуру и добавить ее или проверить, есть ли она в опубликованном списке.</span><span class="sxs-lookup"><span data-stu-id="234e3-143">To stop an acronym from being excluded, you'll need to delete the excluded acronym and add it or verify it's in your published list.</span></span>

<span data-ttu-id="234e3-144">Вы можете добавлять аббревиатуры по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="234e3-144">You can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="234e3-145">Загрузите CSV-файл с полями, показанными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="234e3-145">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="234e3-146">Аббревиатура (Обязательно)</span><span class="sxs-lookup"><span data-stu-id="234e3-146">Acronym (Mandatory)</span></span> | <span data-ttu-id="234e3-147">Стойки для (обязательный)</span><span class="sxs-lookup"><span data-stu-id="234e3-147">Stands for (Mandatory)</span></span> | <span data-ttu-id="234e3-148">Url</span><span class="sxs-lookup"><span data-stu-id="234e3-148">Url</span></span> | <span data-ttu-id="234e3-149">Описание</span><span class="sxs-lookup"><span data-stu-id="234e3-149">Description</span></span>  | <span data-ttu-id="234e3-150">Состояние (обязательное)</span><span class="sxs-lookup"><span data-stu-id="234e3-150">State (Mandatory)</span></span> | <span data-ttu-id="234e3-151">Последние изменения</span><span class="sxs-lookup"><span data-stu-id="234e3-151">Last Modified</span></span> | <span data-ttu-id="234e3-152">Последнее изменение путем</span><span class="sxs-lookup"><span data-stu-id="234e3-152">Last Modified By</span></span> | <span data-ttu-id="234e3-153">Id</span><span class="sxs-lookup"><span data-stu-id="234e3-153">Id</span></span> |
| --------- | --------- | --------- | ---------- | --------- |--------- |--------- |--------- |
| <span data-ttu-id="234e3-154">*XXX*</span><span class="sxs-lookup"><span data-stu-id="234e3-154">*XXX*</span></span> | <span data-ttu-id="234e3-155">*Написанная аббревиатура*</span><span class="sxs-lookup"><span data-stu-id="234e3-155">*Spelled out abbreviation*</span></span> | <span data-ttu-id="234e3-156">*Source*</span><span class="sxs-lookup"><span data-stu-id="234e3-156">*Source*</span></span> |  | <span data-ttu-id="234e3-157">*Опубликовано, черновик или исключено*</span><span class="sxs-lookup"><span data-stu-id="234e3-157">*Published, Draft, or Excluded*</span></span> |  |  |  |

### <a name="csv-fields"></a><span data-ttu-id="234e3-158">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="234e3-158">CSV fields</span></span>

<span data-ttu-id="234e3-159">**Аббревиатура**.</span><span class="sxs-lookup"><span data-stu-id="234e3-159">**Acronym**.</span></span> <span data-ttu-id="234e3-160">Содержит фактическую короткую форму или аббревиатура.</span><span class="sxs-lookup"><span data-stu-id="234e3-160">Contains the actual short form or acronym.</span></span> <span data-ttu-id="234e3-161">Пример *DNN*.</span><span class="sxs-lookup"><span data-stu-id="234e3-161">An example is *DNN*.</span></span>

<span data-ttu-id="234e3-162">**Выступает за**.</span><span class="sxs-lookup"><span data-stu-id="234e3-162">**Stands for**.</span></span> <span data-ttu-id="234e3-163">Содержит определение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="234e3-163">Contains the definition of the acronym.</span></span> <span data-ttu-id="234e3-164">Пример — *глубокая нейронная сеть.*</span><span class="sxs-lookup"><span data-stu-id="234e3-164">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="234e3-165">**Описание**.</span><span class="sxs-lookup"><span data-stu-id="234e3-165">**Description**.</span></span> <span data-ttu-id="234e3-166">Краткое описание аббревиатуры, которая предоставляет пользователям дополнительные сведения о аббревиатуре и ее определении.</span><span class="sxs-lookup"><span data-stu-id="234e3-166">A brief description of the acronym that gives users more info about the acronym and its definition.</span></span> <span data-ttu-id="234e3-167">Например, *глубокая нейронная* сеть — это нейронная сеть с определенным уровнем сложности, нейронная сеть с более чем двумя слоями.</span><span class="sxs-lookup"><span data-stu-id="234e3-167">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="234e3-168">**Источник**</span><span class="sxs-lookup"><span data-stu-id="234e3-168">**Source**.</span></span> <span data-ttu-id="234e3-169">URL-адрес страницы или веб-сайта, на котором вы хотите, чтобы пользователи могли получить дополнительные сведения о аббревиатуре.</span><span class="sxs-lookup"><span data-stu-id="234e3-169">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="234e3-170">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="234e3-170">**State**.</span></span> <span data-ttu-id="234e3-171">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="234e3-171">This field can take two values:</span></span>

- <span data-ttu-id="234e3-172">**Проект**.</span><span class="sxs-lookup"><span data-stu-id="234e3-172">**Draft**.</span></span> <span data-ttu-id="234e3-173">Добавляет аббревиатура в состояние Draft.</span><span class="sxs-lookup"><span data-stu-id="234e3-173">Adds the acronym to the Draft state.</span></span>
- <span data-ttu-id="234e3-174">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="234e3-174">**Published**.</span></span> <span data-ttu-id="234e3-175">Добавляет аббревиатура в состояние Published и делает ее доступной в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="234e3-175">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>
- <span data-ttu-id="234e3-176">**Исключено**.</span><span class="sxs-lookup"><span data-stu-id="234e3-176">**Excluded**.</span></span> <span data-ttu-id="234e3-177">Добавляет аббревиатура в состояние Исключено и не позволяет ему отображаться в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="234e3-177">Adds the acronym to the Excluded state and prevents it from appearing in Microsoft Search.</span></span>

### <a name="system-curated-acronyms"></a><span data-ttu-id="234e3-178">Аббревиатуры с системной системой</span><span class="sxs-lookup"><span data-stu-id="234e3-178">System-curated acronyms</span></span>

<span data-ttu-id="234e3-179">Администраторам может потребоваться добавить все аббревиатуры, используемые в организации, в Answers.</span><span class="sxs-lookup"><span data-stu-id="234e3-179">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="234e3-180">Эта функция может найти аббревиатуры, о которых администраторы поиска даже не знают.</span><span class="sxs-lookup"><span data-stu-id="234e3-180">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="234e3-181">Чтобы сделать эту работу, Microsoft Search также обнаруживает и курирует аббревиатуры из этих источников:</span><span class="sxs-lookup"><span data-stu-id="234e3-181">To do that work, Microsoft Search also discovers and curates acronyms from these sources:</span></span>

- <span data-ttu-id="234e3-182">Сообщения электронной почты пользователей</span><span class="sxs-lookup"><span data-stu-id="234e3-182">Users’ emails</span></span>
- <span data-ttu-id="234e3-183">Документы в [SharePoint,](https://products.office.com/sharepoint/collaboration) [Microsoft OneDrive]( https://onedrive.live.com/about/)и [Microsoft OneNote](https://www.onenote.com/)</span><span class="sxs-lookup"><span data-stu-id="234e3-183">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/)</span></span>
- <span data-ttu-id="234e3-184">Общедоступные документы в организации, к которые пользователи имеют доступ в SharePoint, OneDrive или OneNote</span><span class="sxs-lookup"><span data-stu-id="234e3-184">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote</span></span>

<span data-ttu-id="234e3-185">В Microsoft Search убедитесь, что только пользователи с доступом и разрешениями к документу могут видеть аббревиатуры, обнаруженные в нем.</span><span class="sxs-lookup"><span data-stu-id="234e3-185">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are discovered from it.</span></span> <span data-ttu-id="234e3-186">При обнаружении аббревиатуры в почтовом ящике пользователя только этот пользователь может увидеть эту аббревиатуру.</span><span class="sxs-lookup"><span data-stu-id="234e3-186">When an acronym is found in a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="234e3-187">Для системных аббревиатур не требуется установка.</span><span class="sxs-lookup"><span data-stu-id="234e3-187">No setup is needed for system-curated acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="234e3-188">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="234e3-188">Frequently asked questions</span></span>

<span data-ttu-id="234e3-189">**В. Как ранжировать данные, курированные администратором и системными данными?**</span><span class="sxs-lookup"><span data-stu-id="234e3-189">**Q: How is admin-curated and system-curated data ranked?**</span></span>

<span data-ttu-id="234e3-190">**A:** Ранжирование результатов может отличаться от человека к человеку, так как результаты персонализированы для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="234e3-190">**A:** The ranking of results may vary from person to person as results are personalized for each user.</span></span> <span data-ttu-id="234e3-191">Ни одна из этих категорий не всегда будет иметь приоритет над другой.</span><span class="sxs-lookup"><span data-stu-id="234e3-191">Neither of these categories will always take precedence over the other.</span></span>

<span data-ttu-id="234e3-192">**В. Сколько времени необходимо, чтобы акронимы, курированные администратором, были видны в Microsoft Search после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="234e3-192">**Q: How long does it take for admin-curated acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="234e3-193">**A:**  Акронимы, добавленные в состояние Published, становятся доступными в Microsoft Search, занимает до дня.</span><span class="sxs-lookup"><span data-stu-id="234e3-193">**A:**  It takes up to a day for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="234e3-194">**Вопрос: Как пользователи вызывают ответы на аббревиатуры?**</span><span class="sxs-lookup"><span data-stu-id="234e3-194">**Q: How do users trigger acronyms answers?**</span></span>

<span data-ttu-id="234e3-195">**Ответ:** Чтобы получить ответы на аббревиатуры, пользователи должны ввести определенные шаблоны запросов в поле [поиска Bing,](https://bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)или [Office 365.](https://Office.com) </span><span class="sxs-lookup"><span data-stu-id="234e3-195">**A**: To get acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="234e3-196">**Вопрос: Сколько времени займет от появления аббревиатур с системной системой после получения или отправки нового сообщения электронной почты или документа?**</span><span class="sxs-lookup"><span data-stu-id="234e3-196">**Q: How long does it take for system-curated acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="234e3-197">**A:** Аббревиатуры, найденные в новом сообщении электронной почты или документе, отображаются в результатах поиска Майкрософт до семи дней.</span><span class="sxs-lookup"><span data-stu-id="234e3-197">**A:** Acronyms found in a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="234e3-198">**В. Что происходит, если аббревиатура исключена и опубликована?**</span><span class="sxs-lookup"><span data-stu-id="234e3-198">**Q: What happens when an acronym is both excluded and published?**</span></span>

<span data-ttu-id="234e3-199">**A:** Исключенная аббревиатура имеет приоритет и не позволяет опубликованной аббревиатуре появляться в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="234e3-199">**A:** The excluded acronym is given priority and prevents the published acronym from appearing in search results.</span></span> <span data-ttu-id="234e3-200">Он не удаляет и не удаляет опубликованную аббревиатуру.</span><span class="sxs-lookup"><span data-stu-id="234e3-200">It doesn't delete or remove the published acronym.</span></span>

<span data-ttu-id="234e3-201">**В. Сколько времени требуется для исключения аббревиатуры из результатов поиска Майкрософт?**</span><span class="sxs-lookup"><span data-stu-id="234e3-201">**Q: How long does it take for an acronym to be excluded from Microsoft Search results?**</span></span>

<span data-ttu-id="234e3-202">**A.** Для остановки появления исключенной аббревиатуры в результатах поиска требуется до дня.</span><span class="sxs-lookup"><span data-stu-id="234e3-202">**A**: It takes up to a day for an excluded acronym to stop appearing in search results.</span></span>

<span data-ttu-id="234e3-203">**В. Для системных аббревиатур документы должны быть в определенном формате?**</span><span class="sxs-lookup"><span data-stu-id="234e3-203">**Q: For system-curated acronyms, do documents need to be in a specific format?**</span></span>

<span data-ttu-id="234e3-204">**A:** Нет.</span><span class="sxs-lookup"><span data-stu-id="234e3-204">**A:** No.</span></span> <span data-ttu-id="234e3-205">Мы поддерживаем все типы файлов, кроме изображений, папок и почтовых файлов.</span><span class="sxs-lookup"><span data-stu-id="234e3-205">We support all file types except image, folder, and zip files.</span></span>

<span data-ttu-id="234e3-206">**Вопрос: Будет ли Корпорация Майкрософт открывать аббревиатуры из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="234e3-206">**Q: Will Microsoft discover acronyms from documents in all languages?**</span></span>

<span data-ttu-id="234e3-207">**A.** Microsoft поддерживает только системные аббревиатуры из документов на английском, испанском, французском, итальянском, немецком и португальском языках.</span><span class="sxs-lookup"><span data-stu-id="234e3-207">**A**: Microsoft only supports system-curated acronyms from documents in English, Spanish, French, Italian, German, and Portuguese.</span></span> <span data-ttu-id="234e3-208">Поддержка других языков будет добавляться поэтапно.</span><span class="sxs-lookup"><span data-stu-id="234e3-208">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="234e3-209">**В. Что делать, если моя организация не хочет показывать аббревиатуры с системной системой? Можно ли перестать показывать этот тип аббревиатуры в результатах поиска?**</span><span class="sxs-lookup"><span data-stu-id="234e3-209">**Q: What if my organization doesn’t want to show system-curated acronyms? Can I stop showing this type of acronym in my search results?**</span></span>

<span data-ttu-id="234e3-210">**A.** Чтобы отключить отображение системных аббревиатур в результатах поиска, создайте билет поддержки клиентов, следуя инструкциям в службе поддержки контактов для [бизнес-продуктов.](/microsoft-365/admin/contact-support-for-business-products)</span><span class="sxs-lookup"><span data-stu-id="234e3-210">**A**: To turn off showing system-curated acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](/microsoft-365/admin/contact-support-for-business-products).</span></span>
<span data-ttu-id="234e3-211">После создания билета поддержки для остановки появления в результатах поиска аббревиатуры с системной поддержкой требуется до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="234e3-211">After you create a support ticket, it takes up to 48 hours for system-curated acronyms to stop appearing in search results.</span></span>
