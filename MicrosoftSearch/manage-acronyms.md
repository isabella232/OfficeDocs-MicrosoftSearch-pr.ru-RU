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
description: Создание и обновление ответов на акронимы в Поиске (Майкрософт)
ms.openlocfilehash: ff79e3d741e10d401873c29d86739e61c9f53329
ms.sourcegitcommit: e6ceb07cae208648dadd5452a077414ab5a4513f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2020
ms.locfileid: "49728009"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="3c48e-103">Управление ответами на акронимы в Поиске (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="3c48e-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="3c48e-104">Пользователи часто бывают в незнакомых сокращениях и аббревиатурах, используемых их организацией или командой.</span><span class="sxs-lookup"><span data-stu-id="3c48e-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="3c48e-105">Термины, специфические для организаций или команд, могут быть новыми для людей, которые переходят из одной команды в другую, работают с внутренними партнерскими командами или являются новыми для организации.</span><span class="sxs-lookup"><span data-stu-id="3c48e-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="3c48e-106">Организации не всегда имеют одну ссылку на стандартную терминологию.</span><span class="sxs-lookup"><span data-stu-id="3c48e-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="3c48e-107">Отсутствие одной ссылки затрудняет поиск определений или расширений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="3c48e-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="3c48e-108">Поиск (Майкрософт) решает эту проблему с помощью аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="3c48e-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="3c48e-109">Впечатления от работы пользователей</span><span class="sxs-lookup"><span data-stu-id="3c48e-109">What users experience</span></span>

<span data-ttu-id="3c48e-110">Пользователи Поиска (Майкрософт) могут получать определения с акронимами [в Bing,](https://Bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)и [Office 365.](https://Office.com)</span><span class="sxs-lookup"><span data-stu-id="3c48e-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="3c48e-111">В поле **поиска** пользователи введите запросы, например:</span><span class="sxs-lookup"><span data-stu-id="3c48e-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="3c48e-112">*Что такое* DNN</span><span class="sxs-lookup"><span data-stu-id="3c48e-112">*What is* DNN</span></span>
- <span data-ttu-id="3c48e-113">*Определение* DNN</span><span class="sxs-lookup"><span data-stu-id="3c48e-113">*Define* DNN</span></span>
- <span data-ttu-id="3c48e-114">Определение *DNN*</span><span class="sxs-lookup"><span data-stu-id="3c48e-114">DNN *definition*</span></span>
- <span data-ttu-id="3c48e-115">*Expand* DNN</span><span class="sxs-lookup"><span data-stu-id="3c48e-115">*Expand* DNN</span></span>
- <span data-ttu-id="3c48e-116">Расширение *DNN*</span><span class="sxs-lookup"><span data-stu-id="3c48e-116">DNN *expansion*</span></span>
- <span data-ttu-id="3c48e-117">*Значение* DNN</span><span class="sxs-lookup"><span data-stu-id="3c48e-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="3c48e-118">DNN *означает*</span><span class="sxs-lookup"><span data-stu-id="3c48e-118">DNN *means*</span></span>

<span data-ttu-id="3c48e-119">В результате включаются все значения DNN, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c48e-119">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="3c48e-120">Чтобы вызвать соответствующие ответы, пользователи должны ввести  запрос, включающий указанные ключевые слова аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="3c48e-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="3c48e-121">Запросы аббревиатуры не чувствительны к делу.</span><span class="sxs-lookup"><span data-stu-id="3c48e-121">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="3c48e-122">Настройка ответов на аббревиатуры</span><span class="sxs-lookup"><span data-stu-id="3c48e-122">Set up acronyms answers</span></span>

<span data-ttu-id="3c48e-123">В Центре [администрирования Microsoft 365](https://admin.microsoft.com)перейдите в акронимы [**и**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)выберите "Добавить **акроним".**</span><span class="sxs-lookup"><span data-stu-id="3c48e-123">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronym**.</span></span>

<span data-ttu-id="3c48e-124">Поиск (Майкрософт) запрашивает два источника данных, чтобы предоставить акронимы ответов на поисковые запросы пользователей:</span><span class="sxs-lookup"><span data-stu-id="3c48e-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="3c48e-125">**Под учетом администратора.**</span><span class="sxs-lookup"><span data-stu-id="3c48e-125">**Admin-curated**.</span></span> <span data-ttu-id="3c48e-126">Предоставляется ИТ-администраторами в [Центре администрирования.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)</span><span class="sxs-lookup"><span data-stu-id="3c48e-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="3c48e-127">**Системный курсор**.</span><span class="sxs-lookup"><span data-stu-id="3c48e-127">**System-curated**.</span></span> <span data-ttu-id="3c48e-128">Обнаружен поиском (Майкрософт) из электронной почты и документов пользователей, а также общедоступных данных в организации.</span><span class="sxs-lookup"><span data-stu-id="3c48e-128">Discovered by Microsoft Search from users' email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-admin-curated-acronyms"></a><span data-ttu-id="3c48e-129">Настройка акронимов, подаваемых администратором</span><span class="sxs-lookup"><span data-stu-id="3c48e-129">Set up Admin-curated acronyms</span></span>

<span data-ttu-id="3c48e-130">Администраторы поиска могут добавлять акронимы на вкладке ["Акронимы"](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) в Центре администрирования Поиска [(Майкрософт).](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)</span><span class="sxs-lookup"><span data-stu-id="3c48e-130">Search administrators can add acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="3c48e-131">В Центр администрирования можно добавить акронимы из любого внутреннего сайта или репозитория.</span><span class="sxs-lookup"><span data-stu-id="3c48e-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="3c48e-132">Эти акронимы можно добавить в состояние **"Опубликовано"** или **"Черновик":**</span><span class="sxs-lookup"><span data-stu-id="3c48e-132">These acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="3c48e-133">**Состояние публикации.**</span><span class="sxs-lookup"><span data-stu-id="3c48e-133">**Published state**.</span></span> <span data-ttu-id="3c48e-134">Акронимы доступны пользователям организации через Поиск (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="3c48e-134">Acronyms are available to the organization’s users through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="3c48e-135">Чтобы акронимы, добавленные в состояние "Опубликовано", стали доступными в Поиске (Майкрософт), может потребоваться до трех дней.</span><span class="sxs-lookup"><span data-stu-id="3c48e-135">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="3c48e-136">**Состояние черновика.**</span><span class="sxs-lookup"><span data-stu-id="3c48e-136">**Draft state**.</span></span> <span data-ttu-id="3c48e-137">Если вы хотите просмотреть аббревиатуру, прежде чем сделать ее доступной в Поиске (Майкрософт), можно добавить акроним в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="3c48e-137">If you want to review an acronym before making it available in Microsoft Search, you can add the acronym in a Draft state.</span></span> <span data-ttu-id="3c48e-138">Акронимы в состоянии черновика не будут отображаться в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="3c48e-138">Acronyms in the Draft state will not appear in search results.</span></span> <span data-ttu-id="3c48e-139">Чтобы аббревиатура была опубликована в результатах поиска, ее необходимо переместить в состояние "Опубликовано".</span><span class="sxs-lookup"><span data-stu-id="3c48e-139">You will need to move the acronym to the Published state to make it appear in search results.</span></span>

<span data-ttu-id="3c48e-140">Вы можете добавить акронимы по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="3c48e-140">You can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="3c48e-141">Загрузите CSV-файл с полями, показанными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="3c48e-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="3c48e-142">Аббревиатура (обязательная)</span><span class="sxs-lookup"><span data-stu-id="3c48e-142">Acronym (mandatory)</span></span> | <span data-ttu-id="3c48e-143">Расширение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="3c48e-143">Expansion (mandatory)</span></span> | <span data-ttu-id="3c48e-144">Описание</span><span class="sxs-lookup"><span data-stu-id="3c48e-144">Description</span></span>  | <span data-ttu-id="3c48e-145">Source</span><span class="sxs-lookup"><span data-stu-id="3c48e-145">Source</span></span> | <span data-ttu-id="3c48e-146">Состояние (обязательно)</span><span class="sxs-lookup"><span data-stu-id="3c48e-146">State (mandatory)</span></span> |
| --------- | --------- | ---------- | --------- |--------- |
| <span data-ttu-id="3c48e-147">*XXX*</span><span class="sxs-lookup"><span data-stu-id="3c48e-147">*XXX*</span></span> | <span data-ttu-id="3c48e-148">*Написанная аббревиатура*</span><span class="sxs-lookup"><span data-stu-id="3c48e-148">*Spelled out abbreviation*</span></span> |  | <span data-ttu-id="3c48e-149">*URL-адрес*</span><span class="sxs-lookup"><span data-stu-id="3c48e-149">*URL*</span></span> | <span data-ttu-id="3c48e-150">*Опубликованные или черновики*</span><span class="sxs-lookup"><span data-stu-id="3c48e-150">*Published or Draft*</span></span> |

### <a name="csv-fields"></a><span data-ttu-id="3c48e-151">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="3c48e-151">CSV fields</span></span>

<span data-ttu-id="3c48e-152">**Аббревиатура**.</span><span class="sxs-lookup"><span data-stu-id="3c48e-152">**Acronym**.</span></span> <span data-ttu-id="3c48e-153">Содержит фактическую краткую форму или акроним.</span><span class="sxs-lookup"><span data-stu-id="3c48e-153">Contains the actual short form or acronym.</span></span> <span data-ttu-id="3c48e-154">Примером является *DNN*.</span><span class="sxs-lookup"><span data-stu-id="3c48e-154">An example is *DNN*.</span></span>

<span data-ttu-id="3c48e-155">**Расширение .**</span><span class="sxs-lookup"><span data-stu-id="3c48e-155">**Expansion**.</span></span> <span data-ttu-id="3c48e-156">Содержит расширение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="3c48e-156">Contains the expansion of the acronym.</span></span> <span data-ttu-id="3c48e-157">В качестве примера можно *привести deep Neural Network.*</span><span class="sxs-lookup"><span data-stu-id="3c48e-157">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="3c48e-158">**Описание.**</span><span class="sxs-lookup"><span data-stu-id="3c48e-158">**Description**.</span></span> <span data-ttu-id="3c48e-159">Краткое описание аббревиатуры, которая предоставляет пользователям дополнительные сведения об аббревиатуре и его расширении.</span><span class="sxs-lookup"><span data-stu-id="3c48e-159">A brief description of the acronym that gives users more info about the acronym and its expansion.</span></span> <span data-ttu-id="3c48e-160">Например, глубокая нейронная сеть — это нейронная сеть с определенным уровнем сложности, нейронная сеть с более *чем двумя уровнями.*</span><span class="sxs-lookup"><span data-stu-id="3c48e-160">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="3c48e-161">**Источник**</span><span class="sxs-lookup"><span data-stu-id="3c48e-161">**Source**.</span></span> <span data-ttu-id="3c48e-162">URL-адрес страницы или веб-сайта, на который пользователи должны переходить для получения дополнительных сведений об аббревиатуре.</span><span class="sxs-lookup"><span data-stu-id="3c48e-162">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="3c48e-163">**State**.</span><span class="sxs-lookup"><span data-stu-id="3c48e-163">**State**.</span></span> <span data-ttu-id="3c48e-164">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="3c48e-164">This field can take two values:</span></span>

- <span data-ttu-id="3c48e-165">**Черновик**.</span><span class="sxs-lookup"><span data-stu-id="3c48e-165">**Draft**.</span></span> <span data-ttu-id="3c48e-166">Добавляет аббревиатуру в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="3c48e-166">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="3c48e-167">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="3c48e-167">**Published**.</span></span> <span data-ttu-id="3c48e-168">Добавляет акроним в состояние "Опубликовано" и делает его доступным в Поиске (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="3c48e-168">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="system-curated-acronyms"></a><span data-ttu-id="3c48e-169">Акронимы, на которые нацеливалась система</span><span class="sxs-lookup"><span data-stu-id="3c48e-169">System-curated acronyms</span></span>

<span data-ttu-id="3c48e-170">Администраторам может быть трудно добавить все акронимы, используемые в организации, в ответы.</span><span class="sxs-lookup"><span data-stu-id="3c48e-170">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="3c48e-171">Эта функция может находить аббревиатуры, о которых администраторы поиска даже не знают.</span><span class="sxs-lookup"><span data-stu-id="3c48e-171">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="3c48e-172">Для этого Поиск (Майкрософт) также обнаруживает и измерит аббревиатуры из этих источников:</span><span class="sxs-lookup"><span data-stu-id="3c48e-172">To do that work, Microsoft Search also discovers and curates acronyms from these sources:</span></span>

- <span data-ttu-id="3c48e-173">Сообщения электронной почты пользователей</span><span class="sxs-lookup"><span data-stu-id="3c48e-173">Users’ emails</span></span>
- <span data-ttu-id="3c48e-174">Документы в [SharePoint,](https://products.office.com/sharepoint/collaboration) [Microsoft OneDrive]( https://onedrive.live.com/about/)и [Microsoft OneNote](https://www.onenote.com/)</span><span class="sxs-lookup"><span data-stu-id="3c48e-174">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/)</span></span>
- <span data-ttu-id="3c48e-175">Общедоступные документы в организации, к которые пользователи имеют доступ в SharePoint, OneDrive или OneNote</span><span class="sxs-lookup"><span data-stu-id="3c48e-175">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote</span></span>

<span data-ttu-id="3c48e-176">Поиск (Майкрософт) позволяет убедиться, что только пользователи с доступом и разрешениями на доступ к документу могут видеть акронимы, обнаруженные в документе.</span><span class="sxs-lookup"><span data-stu-id="3c48e-176">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are discovered from it.</span></span> <span data-ttu-id="3c48e-177">Если в почтовом ящике пользователя найдена акронимная аббревиатура, только этот пользователь может видеть его.</span><span class="sxs-lookup"><span data-stu-id="3c48e-177">When an acronym is found in a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="3c48e-178">Настройка аббревиатур, подстановенных администратором, не требуется.</span><span class="sxs-lookup"><span data-stu-id="3c48e-178">No setup is needed for admin-curated acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="3c48e-179">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="3c48e-179">Frequently asked questions</span></span>

<span data-ttu-id="3c48e-180">**Вопрос. Как ранжируется система и данные, на которые нацелилось администрирование?**</span><span class="sxs-lookup"><span data-stu-id="3c48e-180">**Q: How is admin-curated and system-curated data ranked?**</span></span>

<span data-ttu-id="3c48e-181">**О.** Ранжирование результатов может отличаться в зависимости от пользователя, так как результаты персонализированы для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c48e-181">**A:** The ranking of results may vary from person to person as results are personalized for each user.</span></span> <span data-ttu-id="3c48e-182">Ни одна из этих категорий не всегда имеет приоритет над другой.</span><span class="sxs-lookup"><span data-stu-id="3c48e-182">Neither of these categories will always take precedence over the other.</span></span>

<span data-ttu-id="3c48e-183">**Вопрос. Сколько времени займет просмотр акронимов, отбираемого администратором, в Поиске (Майкрософт) после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="3c48e-183">**Q: How long does it take for admin-curated acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="3c48e-184">**О.**  Чтобы акронимы, добавленные в состояние "Опубликовано", стали доступными в Поиске (Майкрософт), требуется до трех дней.</span><span class="sxs-lookup"><span data-stu-id="3c48e-184">**A:**  It takes up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="3c48e-185">**Вопрос. Как пользователи вызывают ответы на аббревиатуры?**</span><span class="sxs-lookup"><span data-stu-id="3c48e-185">**Q: How do users trigger acronyms answers?**</span></span>

<span data-ttu-id="3c48e-186">**Ответ.** Чтобы получить ответы на акронимы, пользователи должны ввести определенные шаблоны запросов в поле поиска [Bing,](https://bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)или [Office 365.](https://Office.com) </span><span class="sxs-lookup"><span data-stu-id="3c48e-186">**A**: To get acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="3c48e-187">**Вопрос. Сколько времени займет получение или отправка нового сообщения электронной почты или документа после появления акронимов, отправляемых системой?**</span><span class="sxs-lookup"><span data-stu-id="3c48e-187">**Q: How long does it take for system-curated acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="3c48e-188">**О.** Акронимы, найденные в новом сообщении электронной почты или документе, отображаются в результатах Поиска (Майкрософт) до семи дней.</span><span class="sxs-lookup"><span data-stu-id="3c48e-188">**A:** Acronyms found in a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="3c48e-189">**Вопрос. Должны ли документы быть в определенном формате, чтобы их можно было найти в майнинге?**</span><span class="sxs-lookup"><span data-stu-id="3c48e-189">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="3c48e-190">**О.** Нет.</span><span class="sxs-lookup"><span data-stu-id="3c48e-190">**A:** No.</span></span> <span data-ttu-id="3c48e-191">Поддерживаются все типы файлов, кроме изображений, папок и ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="3c48e-191">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="3c48e-192">**Вопрос. Обнаружит ли Майкрософт акронимы из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="3c48e-192">**Q: Will Microsoft discover acronyms from documents in all languages?**</span></span>

<span data-ttu-id="3c48e-193">**О.** Корпорация Майкрософт поддерживает только майнинг документов на английском языке.</span><span class="sxs-lookup"><span data-stu-id="3c48e-193">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="3c48e-194">Поддержка других языков будет добавлена поэтапно.</span><span class="sxs-lookup"><span data-stu-id="3c48e-194">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="3c48e-195">**Вопрос. Что делать, если моя организация не хочет показывать акронимы, которые высмеяли системой? Можно ли перестать показывать этот тип аббревиатуры в результатах поиска?**</span><span class="sxs-lookup"><span data-stu-id="3c48e-195">**Q: What if my organization doesn’t want to show system-curated acronyms? Can I stop showing this type of acronym in my search results?**</span></span>

<span data-ttu-id="3c48e-196">**A.** Чтобы отключить отображение акронимов, поддерживаемых системой, в результатах поиска создайте запрос в службу поддержки клиентов, следуя инструкциям в службе поддержки по продуктам [для бизнеса.](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support)</span><span class="sxs-lookup"><span data-stu-id="3c48e-196">**A**: To turn off showing system-curated acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span></span>
<span data-ttu-id="3c48e-197">После создания запроса в службу поддержки аббревиатуры, поддерживаемые системой, перестают отображаться в результатах поиска, занимает до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="3c48e-197">After you create a support ticket, it takes up to 48 hours for system-curated acronyms to stop appearing in search results.</span></span>
