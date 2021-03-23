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
ms.openlocfilehash: 5677ff6915c9e43e2559964c40086cb360a05db7
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031371"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="17898-103">Управление ответами на аббревиатуры в Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="17898-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="17898-104">Пользователи часто используют незнакомые аббревиатуры и аббревиатуры, используемые их организацией или командой.</span><span class="sxs-lookup"><span data-stu-id="17898-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="17898-105">Термины, специфические для организаций или групп, могут быть новыми для людей, которые переходят из одной группы в другую, работают с внутренними группами партнеров или являются новыми для организации.</span><span class="sxs-lookup"><span data-stu-id="17898-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="17898-106">Организации не всегда имеют одну ссылку на стандартную терминологию.</span><span class="sxs-lookup"><span data-stu-id="17898-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="17898-107">Отсутствие единой ссылки затрудняет поиск определений или расширений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="17898-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="17898-108">Microsoft Search решает эту проблему с помощью аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="17898-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="17898-109">Что пользователи испытывают</span><span class="sxs-lookup"><span data-stu-id="17898-109">What users experience</span></span>

<span data-ttu-id="17898-110">Пользователи Microsoft Search могут получать определения с акронимами [в Bing,](https://Bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)и [Office 365.](https://Office.com)</span><span class="sxs-lookup"><span data-stu-id="17898-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="17898-111">В поле **Поиск** пользователи введите запросы, подобные этим примерам:</span><span class="sxs-lookup"><span data-stu-id="17898-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="17898-112">*Что такое* DNN</span><span class="sxs-lookup"><span data-stu-id="17898-112">*What is* DNN</span></span>
- <span data-ttu-id="17898-113">*Определение* DNN</span><span class="sxs-lookup"><span data-stu-id="17898-113">*Define* DNN</span></span>
- <span data-ttu-id="17898-114">Определение *DNN*</span><span class="sxs-lookup"><span data-stu-id="17898-114">DNN *definition*</span></span>
- <span data-ttu-id="17898-115">*Расширение* DNN</span><span class="sxs-lookup"><span data-stu-id="17898-115">*Expand* DNN</span></span>
- <span data-ttu-id="17898-116">Расширение *DNN*</span><span class="sxs-lookup"><span data-stu-id="17898-116">DNN *expansion*</span></span>
- <span data-ttu-id="17898-117">*Значение* DNN</span><span class="sxs-lookup"><span data-stu-id="17898-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="17898-118">DNN *означает*</span><span class="sxs-lookup"><span data-stu-id="17898-118">DNN *means*</span></span>

<span data-ttu-id="17898-119">Результат включает все значения DNN, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="17898-119">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="17898-120">Пользователи должны ввести запрос, который включает указанные  ключевые слова аббревиатуры, чтобы вызвать соответствующие ответы.</span><span class="sxs-lookup"><span data-stu-id="17898-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="17898-121">Запросы аббревиатуры не являются конфиденциальными.</span><span class="sxs-lookup"><span data-stu-id="17898-121">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="17898-122">Настройка ответов на аббревиатуры</span><span class="sxs-lookup"><span data-stu-id="17898-122">Set up acronyms answers</span></span>

<span data-ttu-id="17898-123">В центре [администрирования Microsoft 365](https://admin.microsoft.com)перейдите к аббревиатуре, а затем выберите **добавить аббревиатура**. [](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)</span><span class="sxs-lookup"><span data-stu-id="17898-123">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronym**.</span></span>

<span data-ttu-id="17898-124">Microsoft Search запрашивает два источника данных для предоставления ответов на запросы пользователей по аббревиатуре:</span><span class="sxs-lookup"><span data-stu-id="17898-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="17898-125">**Администрирование.**</span><span class="sxs-lookup"><span data-stu-id="17898-125">**Admin-curated**.</span></span> <span data-ttu-id="17898-126">Предоставляется ИТ-администраторами в [центре администрирования.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)</span><span class="sxs-lookup"><span data-stu-id="17898-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="17898-127">**System-curated**.</span><span class="sxs-lookup"><span data-stu-id="17898-127">**System-curated**.</span></span> <span data-ttu-id="17898-128">Обнаружено в Microsoft Search из электронной почты и документов пользователей, а также общедоступных данных в организации.</span><span class="sxs-lookup"><span data-stu-id="17898-128">Discovered by Microsoft Search from users' email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-admin-curated-acronyms"></a><span data-ttu-id="17898-129">Настройка акронимов, курированных администратором</span><span class="sxs-lookup"><span data-stu-id="17898-129">Set up Admin-curated acronyms</span></span>

<span data-ttu-id="17898-130">Администраторы поиска могут добавлять аббревиатуры на вкладке [Acronyms](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) в центре администрирования [Microsoft Search.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)</span><span class="sxs-lookup"><span data-stu-id="17898-130">Search administrators can add acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="17898-131">В центр администрирования можно добавить аббревиатуры из любого внутреннего сайта или репозитория.</span><span class="sxs-lookup"><span data-stu-id="17898-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="17898-132">Эти аббревиатуры можно добавить в **состояние Published** или **Draft:**</span><span class="sxs-lookup"><span data-stu-id="17898-132">These acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="17898-133">**Опубликовано состояние**.</span><span class="sxs-lookup"><span data-stu-id="17898-133">**Published state**.</span></span> <span data-ttu-id="17898-134">Аббревиатуры доступны пользователям организации с помощью Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="17898-134">Acronyms are available to the organization’s users through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="17898-135">Для того чтобы аббревиатуры, добавленные в состояние Published, стали доступными в Microsoft Search, может потребоваться до трех дней.</span><span class="sxs-lookup"><span data-stu-id="17898-135">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="17898-136">**Состояние Черновика.**</span><span class="sxs-lookup"><span data-stu-id="17898-136">**Draft state**.</span></span> <span data-ttu-id="17898-137">Если вы хотите просмотреть аббревиатуру, прежде чем сделать ее доступной в Microsoft Search, можно добавить аббревиатура в состояние Draft.</span><span class="sxs-lookup"><span data-stu-id="17898-137">If you want to review an acronym before making it available in Microsoft Search, you can add the acronym in a Draft state.</span></span> <span data-ttu-id="17898-138">Акронимы в состоянии Draft не отображаются в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="17898-138">Acronyms in the Draft state will not appear in search results.</span></span> <span data-ttu-id="17898-139">Чтобы она появлялась в результатах поиска, необходимо переместить аббревиатура в состояние Published.</span><span class="sxs-lookup"><span data-stu-id="17898-139">You will need to move the acronym to the Published state to make it appear in search results.</span></span>

<span data-ttu-id="17898-140">Вы можете добавлять аббревиатуры по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="17898-140">You can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="17898-141">Загрузите CSV-файл с полями, показанными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="17898-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="17898-142">Аббревиатура (Обязательно)</span><span class="sxs-lookup"><span data-stu-id="17898-142">Acronym (Mandatory)</span></span> | <span data-ttu-id="17898-143">Расширение (обязательное)</span><span class="sxs-lookup"><span data-stu-id="17898-143">Expansion (Mandatory)</span></span> | <span data-ttu-id="17898-144">Url</span><span class="sxs-lookup"><span data-stu-id="17898-144">Url</span></span> | <span data-ttu-id="17898-145">Описание</span><span class="sxs-lookup"><span data-stu-id="17898-145">Description</span></span>  | <span data-ttu-id="17898-146">Состояние (обязательное)</span><span class="sxs-lookup"><span data-stu-id="17898-146">State (Mandatory)</span></span> | <span data-ttu-id="17898-147">Последние изменения</span><span class="sxs-lookup"><span data-stu-id="17898-147">Last Modified</span></span> | <span data-ttu-id="17898-148">Последнее изменение путем</span><span class="sxs-lookup"><span data-stu-id="17898-148">Last Modified By</span></span> | <span data-ttu-id="17898-149">Id</span><span class="sxs-lookup"><span data-stu-id="17898-149">Id</span></span> |
| --------- | --------- | --------- | ---------- | --------- |--------- |--------- |--------- |
| <span data-ttu-id="17898-150">*XXX*</span><span class="sxs-lookup"><span data-stu-id="17898-150">*XXX*</span></span> | <span data-ttu-id="17898-151">*Написанная аббревиатура*</span><span class="sxs-lookup"><span data-stu-id="17898-151">*Spelled out abbreviation*</span></span> | <span data-ttu-id="17898-152">*Source*</span><span class="sxs-lookup"><span data-stu-id="17898-152">*Source*</span></span> |  | <span data-ttu-id="17898-153">*Опубликовано или черновик*</span><span class="sxs-lookup"><span data-stu-id="17898-153">*Published or Draft*</span></span> |  |  |  |

### <a name="csv-fields"></a><span data-ttu-id="17898-154">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="17898-154">CSV fields</span></span>

<span data-ttu-id="17898-155">**Аббревиатура**.</span><span class="sxs-lookup"><span data-stu-id="17898-155">**Acronym**.</span></span> <span data-ttu-id="17898-156">Содержит фактическую короткую форму или аббревиатура.</span><span class="sxs-lookup"><span data-stu-id="17898-156">Contains the actual short form or acronym.</span></span> <span data-ttu-id="17898-157">Пример *DNN*.</span><span class="sxs-lookup"><span data-stu-id="17898-157">An example is *DNN*.</span></span>

<span data-ttu-id="17898-158">**Расширение**.</span><span class="sxs-lookup"><span data-stu-id="17898-158">**Expansion**.</span></span> <span data-ttu-id="17898-159">Содержит расширение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="17898-159">Contains the expansion of the acronym.</span></span> <span data-ttu-id="17898-160">Пример — *глубокая нейронная сеть.*</span><span class="sxs-lookup"><span data-stu-id="17898-160">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="17898-161">**Описание**.</span><span class="sxs-lookup"><span data-stu-id="17898-161">**Description**.</span></span> <span data-ttu-id="17898-162">Краткое описание аббревиатуры, которая предоставляет пользователям дополнительные сведения о аббревиатуре и ее расширении.</span><span class="sxs-lookup"><span data-stu-id="17898-162">A brief description of the acronym that gives users more info about the acronym and its expansion.</span></span> <span data-ttu-id="17898-163">Например, *глубокая нейронная* сеть — это нейронная сеть с определенным уровнем сложности, нейронная сеть с более чем двумя слоями.</span><span class="sxs-lookup"><span data-stu-id="17898-163">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="17898-164">**Источник**</span><span class="sxs-lookup"><span data-stu-id="17898-164">**Source**.</span></span> <span data-ttu-id="17898-165">URL-адрес страницы или веб-сайта, на котором вы хотите, чтобы пользователи могли получить дополнительные сведения о аббревиатуре.</span><span class="sxs-lookup"><span data-stu-id="17898-165">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="17898-166">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="17898-166">**State**.</span></span> <span data-ttu-id="17898-167">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="17898-167">This field can take two values:</span></span>

- <span data-ttu-id="17898-168">**Проект**.</span><span class="sxs-lookup"><span data-stu-id="17898-168">**Draft**.</span></span> <span data-ttu-id="17898-169">Добавляет аббревиатура в состояние Draft.</span><span class="sxs-lookup"><span data-stu-id="17898-169">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="17898-170">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="17898-170">**Published**.</span></span> <span data-ttu-id="17898-171">Добавляет аббревиатура в состояние Published и делает ее доступной в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="17898-171">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="system-curated-acronyms"></a><span data-ttu-id="17898-172">Аббревиатуры с системной системой</span><span class="sxs-lookup"><span data-stu-id="17898-172">System-curated acronyms</span></span>

<span data-ttu-id="17898-173">Администраторам может потребоваться добавить все аббревиатуры, используемые в организации, в Answers.</span><span class="sxs-lookup"><span data-stu-id="17898-173">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="17898-174">Эта функция может найти аббревиатуры, о которых администраторы поиска даже не знают.</span><span class="sxs-lookup"><span data-stu-id="17898-174">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="17898-175">Чтобы сделать эту работу, Microsoft Search также обнаруживает и курирует аббревиатуры из этих источников:</span><span class="sxs-lookup"><span data-stu-id="17898-175">To do that work, Microsoft Search also discovers and curates acronyms from these sources:</span></span>

- <span data-ttu-id="17898-176">Сообщения электронной почты пользователей</span><span class="sxs-lookup"><span data-stu-id="17898-176">Users’ emails</span></span>
- <span data-ttu-id="17898-177">Документы в [SharePoint,](https://products.office.com/sharepoint/collaboration) [Microsoft OneDrive]( https://onedrive.live.com/about/)и [Microsoft OneNote](https://www.onenote.com/)</span><span class="sxs-lookup"><span data-stu-id="17898-177">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/)</span></span>
- <span data-ttu-id="17898-178">Общедоступные документы в организации, к которые пользователи имеют доступ в SharePoint, OneDrive или OneNote</span><span class="sxs-lookup"><span data-stu-id="17898-178">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote</span></span>

<span data-ttu-id="17898-179">В Microsoft Search убедитесь, что только пользователи с доступом и разрешениями к документу могут видеть аббревиатуры, обнаруженные в нем.</span><span class="sxs-lookup"><span data-stu-id="17898-179">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are discovered from it.</span></span> <span data-ttu-id="17898-180">При обнаружении аббревиатуры в почтовом ящике пользователя только этот пользователь может увидеть эту аббревиатуру.</span><span class="sxs-lookup"><span data-stu-id="17898-180">When an acronym is found in a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="17898-181">Для акронимов с куратором администратора настройка не требуется.</span><span class="sxs-lookup"><span data-stu-id="17898-181">No setup is needed for admin-curated acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="17898-182">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="17898-182">Frequently asked questions</span></span>

<span data-ttu-id="17898-183">**В. Как ранжировать данные, курированные администратором и системными данными?**</span><span class="sxs-lookup"><span data-stu-id="17898-183">**Q: How is admin-curated and system-curated data ranked?**</span></span>

<span data-ttu-id="17898-184">**A:** Ранжирование результатов может отличаться от человека к человеку, так как результаты персонализированы для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="17898-184">**A:** The ranking of results may vary from person to person as results are personalized for each user.</span></span> <span data-ttu-id="17898-185">Ни одна из этих категорий не всегда будет иметь приоритет над другой.</span><span class="sxs-lookup"><span data-stu-id="17898-185">Neither of these categories will always take precedence over the other.</span></span>

<span data-ttu-id="17898-186">**В. Сколько времени необходимо, чтобы акронимы, курированные администратором, были видны в Microsoft Search после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="17898-186">**Q: How long does it take for admin-curated acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="17898-187">**A:**  Для того чтобы аббревиатуры, добавленные в состояние Published, стали доступными в Microsoft Search, требуется до трех дней.</span><span class="sxs-lookup"><span data-stu-id="17898-187">**A:**  It takes up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="17898-188">**Вопрос: Как пользователи вызывают ответы на аббревиатуры?**</span><span class="sxs-lookup"><span data-stu-id="17898-188">**Q: How do users trigger acronyms answers?**</span></span>

<span data-ttu-id="17898-189">**Ответ:** Чтобы получить ответы на аббревиатуры, пользователи должны ввести определенные шаблоны запросов в поле [поиска Bing,](https://bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)или [Office 365.](https://Office.com) </span><span class="sxs-lookup"><span data-stu-id="17898-189">**A**: To get acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="17898-190">**Вопрос: Сколько времени займет от появления аббревиатур с системной системой после получения или отправки нового сообщения электронной почты или документа?**</span><span class="sxs-lookup"><span data-stu-id="17898-190">**Q: How long does it take for system-curated acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="17898-191">**A:** Аббревиатуры, найденные в новом сообщении электронной почты или документе, отображаются в результатах поиска Майкрософт до семи дней.</span><span class="sxs-lookup"><span data-stu-id="17898-191">**A:** Acronyms found in a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="17898-192">**В. Нужны ли документы в определенном формате для их подбирать?**</span><span class="sxs-lookup"><span data-stu-id="17898-192">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="17898-193">**A:** Нет.</span><span class="sxs-lookup"><span data-stu-id="17898-193">**A:** No.</span></span> <span data-ttu-id="17898-194">Мы поддерживаем все типы файлов, кроме изображений, папок и почтовых файлов.</span><span class="sxs-lookup"><span data-stu-id="17898-194">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="17898-195">**Вопрос: Будет ли Корпорация Майкрософт открывать аббревиатуры из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="17898-195">**Q: Will Microsoft discover acronyms from documents in all languages?**</span></span>

<span data-ttu-id="17898-196">**A.** Microsoft поддерживает только майнинг из документов на английском языке.</span><span class="sxs-lookup"><span data-stu-id="17898-196">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="17898-197">Поддержка других языков будет добавляться поэтапно.</span><span class="sxs-lookup"><span data-stu-id="17898-197">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="17898-198">**В. Что делать, если моя организация не хочет показывать аббревиатуры с системной системой? Можно ли перестать показывать этот тип аббревиатуры в результатах поиска?**</span><span class="sxs-lookup"><span data-stu-id="17898-198">**Q: What if my organization doesn’t want to show system-curated acronyms? Can I stop showing this type of acronym in my search results?**</span></span>

<span data-ttu-id="17898-199">**A.** Чтобы отключить отображение системных аббревиатур в результатах поиска, создайте билет поддержки клиентов, следуя инструкциям в службе поддержки контактов для [бизнес-продуктов.](/microsoft-365/admin/contact-support-for-business-products)</span><span class="sxs-lookup"><span data-stu-id="17898-199">**A**: To turn off showing system-curated acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](/microsoft-365/admin/contact-support-for-business-products).</span></span>
<span data-ttu-id="17898-200">После создания билета поддержки для остановки появления в результатах поиска аббревиатуры с системной поддержкой требуется до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="17898-200">After you create a support ticket, it takes up to 48 hours for system-curated acronyms to stop appearing in search results.</span></span>