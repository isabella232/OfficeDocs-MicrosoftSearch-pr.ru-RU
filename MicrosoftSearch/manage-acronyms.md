---
title: Управление ответами на акронимы в Поиске (Майкрософт)
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
description: Создание и обновление ответов на аббревиатуры в Поиске (Майкрософт)
ms.openlocfilehash: 45d3cc7b33f27d2f4e77d8099fbfa91e01aabcbb
ms.sourcegitcommit: ef94ffd6111acb929c8343f0f4f82ea109b68fb6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "50122159"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="ece9b-103">Управление ответами на акронимы в Поиске (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="ece9b-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="ece9b-104">Пользователи часто бывают в незнакомых сокращениях и аббревиатурах, используемых их организацией или командой.</span><span class="sxs-lookup"><span data-stu-id="ece9b-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="ece9b-105">Термины, специфические для организаций или команд, могут быть новыми для людей, которые переходят из одной команды в другую, работают с внутренними партнерскими командами или являются новыми для организации.</span><span class="sxs-lookup"><span data-stu-id="ece9b-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="ece9b-106">Организации не всегда имеют одну ссылку на стандартную терминологию.</span><span class="sxs-lookup"><span data-stu-id="ece9b-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="ece9b-107">Отсутствие одной ссылки затрудняет поиск определений или расширений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="ece9b-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="ece9b-108">Поиск (Майкрософт) решает эту проблему с помощью аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="ece9b-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="ece9b-109">Впечатления от работы пользователей</span><span class="sxs-lookup"><span data-stu-id="ece9b-109">What users experience</span></span>

<span data-ttu-id="ece9b-110">Пользователи Поиска (Майкрософт) могут получать определения с акронимами [в Bing,](https://Bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)и [Office 365.](https://Office.com)</span><span class="sxs-lookup"><span data-stu-id="ece9b-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="ece9b-111">В поле **поиска** пользователи введите запросы, например:</span><span class="sxs-lookup"><span data-stu-id="ece9b-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="ece9b-112">*Что такое* DNN</span><span class="sxs-lookup"><span data-stu-id="ece9b-112">*What is* DNN</span></span>
- <span data-ttu-id="ece9b-113">*Определение* DNN</span><span class="sxs-lookup"><span data-stu-id="ece9b-113">*Define* DNN</span></span>
- <span data-ttu-id="ece9b-114">Определение *DNN*</span><span class="sxs-lookup"><span data-stu-id="ece9b-114">DNN *definition*</span></span>
- <span data-ttu-id="ece9b-115">*Expand* DNN</span><span class="sxs-lookup"><span data-stu-id="ece9b-115">*Expand* DNN</span></span>
- <span data-ttu-id="ece9b-116">Расширение *DNN*</span><span class="sxs-lookup"><span data-stu-id="ece9b-116">DNN *expansion*</span></span>
- <span data-ttu-id="ece9b-117">*Значение* DNN</span><span class="sxs-lookup"><span data-stu-id="ece9b-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="ece9b-118">DNN *означает*</span><span class="sxs-lookup"><span data-stu-id="ece9b-118">DNN *means*</span></span>

<span data-ttu-id="ece9b-119">В результате включаются все значения DNN, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="ece9b-119">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="ece9b-120">Чтобы вызвать соответствующие ответы, пользователи должны ввести  запрос, включающий указанные ключевые слова аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="ece9b-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="ece9b-121">Запросы аббревиатуры не чувствительны к делу.</span><span class="sxs-lookup"><span data-stu-id="ece9b-121">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="ece9b-122">Настройка ответов на аббревиатуры</span><span class="sxs-lookup"><span data-stu-id="ece9b-122">Set up acronyms answers</span></span>

<span data-ttu-id="ece9b-123">В Центре [администрирования Microsoft 365](https://admin.microsoft.com)перейдите в акронимы [**и**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)выберите "Добавить **акроним".**</span><span class="sxs-lookup"><span data-stu-id="ece9b-123">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronym**.</span></span>

<span data-ttu-id="ece9b-124">Поиск (Майкрософт) запрашивает два источника данных, чтобы предоставить акронимы ответов на поисковые запросы пользователей:</span><span class="sxs-lookup"><span data-stu-id="ece9b-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="ece9b-125">**Под учетом администратора.**</span><span class="sxs-lookup"><span data-stu-id="ece9b-125">**Admin-curated**.</span></span> <span data-ttu-id="ece9b-126">Предоставляется ИТ-администраторами в [Центре администрирования.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)</span><span class="sxs-lookup"><span data-stu-id="ece9b-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="ece9b-127">**Системный курсор.**</span><span class="sxs-lookup"><span data-stu-id="ece9b-127">**System-curated**.</span></span> <span data-ttu-id="ece9b-128">Обнаружен поиском (Майкрософт) из электронной почты и документов пользователей, а также общедоступных данных в организации.</span><span class="sxs-lookup"><span data-stu-id="ece9b-128">Discovered by Microsoft Search from users' email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-admin-curated-acronyms"></a><span data-ttu-id="ece9b-129">Настройка акронимов, подаваемых администратором</span><span class="sxs-lookup"><span data-stu-id="ece9b-129">Set up Admin-curated acronyms</span></span>

<span data-ttu-id="ece9b-130">Администраторы поиска могут добавлять акронимы на вкладке ["Акронимы"](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) в Центре администрирования Поиска [(Майкрософт).](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)</span><span class="sxs-lookup"><span data-stu-id="ece9b-130">Search administrators can add acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="ece9b-131">В Центр администрирования можно добавить акронимы из любого внутреннего сайта или репозитория.</span><span class="sxs-lookup"><span data-stu-id="ece9b-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="ece9b-132">Эти акронимы можно добавить в состояние **"Опубликовано"** или **"Черновик":**</span><span class="sxs-lookup"><span data-stu-id="ece9b-132">These acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="ece9b-133">**Состояние публикации.**</span><span class="sxs-lookup"><span data-stu-id="ece9b-133">**Published state**.</span></span> <span data-ttu-id="ece9b-134">Акронимы доступны пользователям организации через Поиск (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="ece9b-134">Acronyms are available to the organization’s users through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="ece9b-135">Чтобы акронимы, добавленные в состояние "Опубликовано", стали доступными в Поиске (Майкрософт), может потребоваться до трех дней.</span><span class="sxs-lookup"><span data-stu-id="ece9b-135">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="ece9b-136">**Состояние черновика.**</span><span class="sxs-lookup"><span data-stu-id="ece9b-136">**Draft state**.</span></span> <span data-ttu-id="ece9b-137">Если вы хотите просмотреть аббревиатуру, прежде чем сделать ее доступной в Поиске (Майкрософт), можно добавить акроним в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="ece9b-137">If you want to review an acronym before making it available in Microsoft Search, you can add the acronym in a Draft state.</span></span> <span data-ttu-id="ece9b-138">Акронимы в состоянии черновика не будут отображаться в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="ece9b-138">Acronyms in the Draft state will not appear in search results.</span></span> <span data-ttu-id="ece9b-139">Чтобы аббревиатура была опубликована в результатах поиска, ее необходимо переместить в состояние "Опубликовано".</span><span class="sxs-lookup"><span data-stu-id="ece9b-139">You will need to move the acronym to the Published state to make it appear in search results.</span></span>

<span data-ttu-id="ece9b-140">Вы можете добавить акронимы по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="ece9b-140">You can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="ece9b-141">Загрузите CSV-файл с полями, показанными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="ece9b-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="ece9b-142">Аббревиатура (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece9b-142">Acronym (Mandatory)</span></span> | <span data-ttu-id="ece9b-143">Расширение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece9b-143">Expansion (Mandatory)</span></span> | <span data-ttu-id="ece9b-144">Url</span><span class="sxs-lookup"><span data-stu-id="ece9b-144">Url</span></span> | <span data-ttu-id="ece9b-145">Описание</span><span class="sxs-lookup"><span data-stu-id="ece9b-145">Description</span></span>  | <span data-ttu-id="ece9b-146">Состояние (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece9b-146">State (Mandatory)</span></span> | <span data-ttu-id="ece9b-147">Last Modified</span><span class="sxs-lookup"><span data-stu-id="ece9b-147">Last Modified</span></span> | <span data-ttu-id="ece9b-148">Last Modified By</span><span class="sxs-lookup"><span data-stu-id="ece9b-148">Last Modified By</span></span> | <span data-ttu-id="ece9b-149">Id</span><span class="sxs-lookup"><span data-stu-id="ece9b-149">Id</span></span> |
| --------- | --------- | --------- | ---------- | --------- |--------- |--------- |--------- |
| <span data-ttu-id="ece9b-150">*XXX*</span><span class="sxs-lookup"><span data-stu-id="ece9b-150">*XXX*</span></span> | <span data-ttu-id="ece9b-151">*Орфографию аббревиатуры*</span><span class="sxs-lookup"><span data-stu-id="ece9b-151">*Spelled out abbreviation*</span></span> | <span data-ttu-id="ece9b-152">*Source*</span><span class="sxs-lookup"><span data-stu-id="ece9b-152">*Source*</span></span> |  | <span data-ttu-id="ece9b-153">*Опубликованные или черновики*</span><span class="sxs-lookup"><span data-stu-id="ece9b-153">*Published or Draft*</span></span> |  |  |  |

### <a name="csv-fields"></a><span data-ttu-id="ece9b-154">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="ece9b-154">CSV fields</span></span>

<span data-ttu-id="ece9b-155">**Аббревиатура**.</span><span class="sxs-lookup"><span data-stu-id="ece9b-155">**Acronym**.</span></span> <span data-ttu-id="ece9b-156">Содержит фактическую краткую форму или акроним.</span><span class="sxs-lookup"><span data-stu-id="ece9b-156">Contains the actual short form or acronym.</span></span> <span data-ttu-id="ece9b-157">Примером является *DNN*.</span><span class="sxs-lookup"><span data-stu-id="ece9b-157">An example is *DNN*.</span></span>

<span data-ttu-id="ece9b-158">**Расширение .**</span><span class="sxs-lookup"><span data-stu-id="ece9b-158">**Expansion**.</span></span> <span data-ttu-id="ece9b-159">Содержит расширение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="ece9b-159">Contains the expansion of the acronym.</span></span> <span data-ttu-id="ece9b-160">В качестве примера можно *привести deep Neural Network.*</span><span class="sxs-lookup"><span data-stu-id="ece9b-160">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="ece9b-161">**Описание.**</span><span class="sxs-lookup"><span data-stu-id="ece9b-161">**Description**.</span></span> <span data-ttu-id="ece9b-162">Краткое описание аббревиатуры, которая предоставляет пользователям дополнительные сведения об аббревиатуре и его расширении.</span><span class="sxs-lookup"><span data-stu-id="ece9b-162">A brief description of the acronym that gives users more info about the acronym and its expansion.</span></span> <span data-ttu-id="ece9b-163">Например, глубокая нейронная сеть — это нейронная сеть с определенным уровнем сложности, нейронная сеть с более *чем двумя уровнями.*</span><span class="sxs-lookup"><span data-stu-id="ece9b-163">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="ece9b-164">**Источник**</span><span class="sxs-lookup"><span data-stu-id="ece9b-164">**Source**.</span></span> <span data-ttu-id="ece9b-165">URL-адрес страницы или веб-сайта, где пользователи должны получить дополнительные сведения об аббревиатуре.</span><span class="sxs-lookup"><span data-stu-id="ece9b-165">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="ece9b-166">**State**.</span><span class="sxs-lookup"><span data-stu-id="ece9b-166">**State**.</span></span> <span data-ttu-id="ece9b-167">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="ece9b-167">This field can take two values:</span></span>

- <span data-ttu-id="ece9b-168">**Черновик**.</span><span class="sxs-lookup"><span data-stu-id="ece9b-168">**Draft**.</span></span> <span data-ttu-id="ece9b-169">Добавляет аббревиатуру в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="ece9b-169">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="ece9b-170">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="ece9b-170">**Published**.</span></span> <span data-ttu-id="ece9b-171">Добавляет акроним в состояние "Опубликовано" и делает его доступным в Поиске (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="ece9b-171">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="system-curated-acronyms"></a><span data-ttu-id="ece9b-172">Акронимы, на которые нацеливалась система</span><span class="sxs-lookup"><span data-stu-id="ece9b-172">System-curated acronyms</span></span>

<span data-ttu-id="ece9b-173">Администраторам может быть трудно добавить все акронимы, используемые в организации, в ответы.</span><span class="sxs-lookup"><span data-stu-id="ece9b-173">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="ece9b-174">Эта функция может находить аббревиатуры, о которых администраторы поиска даже не знают.</span><span class="sxs-lookup"><span data-stu-id="ece9b-174">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="ece9b-175">Для этого Поиск (Майкрософт) также обнаруживает и измерит аббревиатуры из этих источников:</span><span class="sxs-lookup"><span data-stu-id="ece9b-175">To do that work, Microsoft Search also discovers and curates acronyms from these sources:</span></span>

- <span data-ttu-id="ece9b-176">Сообщения электронной почты пользователей</span><span class="sxs-lookup"><span data-stu-id="ece9b-176">Users’ emails</span></span>
- <span data-ttu-id="ece9b-177">Документы в [SharePoint,](https://products.office.com/sharepoint/collaboration) [Microsoft OneDrive]( https://onedrive.live.com/about/)и [Microsoft OneNote](https://www.onenote.com/)</span><span class="sxs-lookup"><span data-stu-id="ece9b-177">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/)</span></span>
- <span data-ttu-id="ece9b-178">Общедоступные документы в организации, к которые пользователи имеют доступ в SharePoint, OneDrive или OneNote</span><span class="sxs-lookup"><span data-stu-id="ece9b-178">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote</span></span>

<span data-ttu-id="ece9b-179">Поиск (Майкрософт) позволяет убедиться, что только пользователи с доступом и разрешениями на доступ к документу могут видеть акронимы, обнаруженные в документе.</span><span class="sxs-lookup"><span data-stu-id="ece9b-179">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are discovered from it.</span></span> <span data-ttu-id="ece9b-180">Если в почтовом ящике пользователя найдена акронимная аббревиатура, только этот пользователь может видеть это аббревиатура.</span><span class="sxs-lookup"><span data-stu-id="ece9b-180">When an acronym is found in a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="ece9b-181">Настройка аббревиатур, подстановенных администратором, не требуется.</span><span class="sxs-lookup"><span data-stu-id="ece9b-181">No setup is needed for admin-curated acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ece9b-182">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="ece9b-182">Frequently asked questions</span></span>

<span data-ttu-id="ece9b-183">**Вопрос. Как ранжируется система и данные, на которые нацелилось администрирование?**</span><span class="sxs-lookup"><span data-stu-id="ece9b-183">**Q: How is admin-curated and system-curated data ranked?**</span></span>

<span data-ttu-id="ece9b-184">**О.** Ранжирование результатов может отличаться от пользователя к человеку, так как результаты персонализированы для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ece9b-184">**A:** The ranking of results may vary from person to person as results are personalized for each user.</span></span> <span data-ttu-id="ece9b-185">Ни одна из этих категорий не всегда имеет приоритет над другой.</span><span class="sxs-lookup"><span data-stu-id="ece9b-185">Neither of these categories will always take precedence over the other.</span></span>

<span data-ttu-id="ece9b-186">**Вопрос. Сколько времени займет просмотр акронимов, отбираемого администратором, в Поиске (Майкрософт) после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="ece9b-186">**Q: How long does it take for admin-curated acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="ece9b-187">**О.**  Чтобы акронимы, добавленные в состояние "Опубликовано", стали доступными в Поиске (Майкрософт), требуется до трех дней.</span><span class="sxs-lookup"><span data-stu-id="ece9b-187">**A:**  It takes up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="ece9b-188">**Вопрос. Как пользователи вызывают ответы на аббревиатуры?**</span><span class="sxs-lookup"><span data-stu-id="ece9b-188">**Q: How do users trigger acronyms answers?**</span></span>

<span data-ttu-id="ece9b-189">**Ответ.** Чтобы получить ответы на акронимы, пользователи должны ввести определенные шаблоны запросов в поле поиска [Bing,](https://bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)или [Office 365.](https://Office.com) </span><span class="sxs-lookup"><span data-stu-id="ece9b-189">**A**: To get acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="ece9b-190">**Вопрос. Сколько времени займет получение или отправка нового сообщения электронной почты или документа после появления акронимов, отправляемых системой?**</span><span class="sxs-lookup"><span data-stu-id="ece9b-190">**Q: How long does it take for system-curated acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="ece9b-191">**О.** Акронимы, найденные в новом сообщении электронной почты или документе, отображаются в результатах Поиска (Майкрософт) до семи дней.</span><span class="sxs-lookup"><span data-stu-id="ece9b-191">**A:** Acronyms found in a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="ece9b-192">**Вопрос. Должны ли документы быть в определенном формате, чтобы их можно было найти в майнинге?**</span><span class="sxs-lookup"><span data-stu-id="ece9b-192">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="ece9b-193">**О.** Нет.</span><span class="sxs-lookup"><span data-stu-id="ece9b-193">**A:** No.</span></span> <span data-ttu-id="ece9b-194">Поддерживаются все типы файлов, кроме изображений, папок и ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="ece9b-194">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="ece9b-195">**Вопрос. Обнаружит ли Майкрософт акронимы из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="ece9b-195">**Q: Will Microsoft discover acronyms from documents in all languages?**</span></span>

<span data-ttu-id="ece9b-196">**О.** Корпорация Майкрософт поддерживает только майнинг документов на английском языке.</span><span class="sxs-lookup"><span data-stu-id="ece9b-196">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="ece9b-197">Поддержка других языков будет добавлена поэтапно.</span><span class="sxs-lookup"><span data-stu-id="ece9b-197">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="ece9b-198">**Вопрос. Что делать, если моя организация не хочет показывать акронимы, которые высмеяли системой? Можно ли перестать показывать этот тип аббревиатуры в результатах поиска?**</span><span class="sxs-lookup"><span data-stu-id="ece9b-198">**Q: What if my organization doesn’t want to show system-curated acronyms? Can I stop showing this type of acronym in my search results?**</span></span>

<span data-ttu-id="ece9b-199">**A.** Чтобы отключить отображение акронимов, поддерживаемых системой, в результатах поиска создайте запрос в службу поддержки клиентов, следуя инструкциям в службе поддержки по продуктам [для бизнеса.](https://docs.microsoft.com/microsoft-365/admin/contact-support-for-business-products)</span><span class="sxs-lookup"><span data-stu-id="ece9b-199">**A**: To turn off showing system-curated acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/microsoft-365/admin/contact-support-for-business-products).</span></span>
<span data-ttu-id="ece9b-200">После создания запроса в службу поддержки аббревиатуры, поддерживаемые системой, перестают отображаться в результатах поиска, занимает до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="ece9b-200">After you create a support ticket, it takes up to 48 hours for system-curated acronyms to stop appearing in search results.</span></span>
