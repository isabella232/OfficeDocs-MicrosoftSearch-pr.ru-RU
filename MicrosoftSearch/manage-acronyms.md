---
title: Управление ответами на акронимы в Поиске (Майкрософт)
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
description: Создание и обновление ответов на аббревиатуры в Поиске (Майкрософт)
ms.openlocfilehash: 9de9de8287e3ddf206f93f53573922f3cf526580
ms.sourcegitcommit: ad225af81060a2e3d7e4c953eeb6977d54698b60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "49709685"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="cc173-103">Управление ответами на акронимы в Поиске (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="cc173-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="cc173-104">Пользователи часто бывают в незнакомых аббревиатурах и сокращениях, используемых их организацией или командой.</span><span class="sxs-lookup"><span data-stu-id="cc173-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="cc173-105">Термины, специфические для организаций или команд, могут быть новыми для людей, которые переходят из одной команды в другую, работают с внутренними партнерскими командами или являются новыми для организации.</span><span class="sxs-lookup"><span data-stu-id="cc173-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="cc173-106">Организации не всегда имеют одну ссылку на стандартную терминологию.</span><span class="sxs-lookup"><span data-stu-id="cc173-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="cc173-107">Отсутствие одной ссылки затрудняет поиск определений или расширений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="cc173-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="cc173-108">Поиск (Майкрософт) решает эту проблему с помощью аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="cc173-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="cc173-109">Впечатления от работы пользователей</span><span class="sxs-lookup"><span data-stu-id="cc173-109">What users experience</span></span>

<span data-ttu-id="cc173-110">Пользователи Поиска (Майкрософт) могут получать определения с акронимами [в Bing,](https://Bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)и [Office 365.](https://Office.com)</span><span class="sxs-lookup"><span data-stu-id="cc173-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="cc173-111">В поле **поиска** пользователи введите запросы, например:</span><span class="sxs-lookup"><span data-stu-id="cc173-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="cc173-112">*Что такое* DNN</span><span class="sxs-lookup"><span data-stu-id="cc173-112">*What is* DNN</span></span>
- <span data-ttu-id="cc173-113">*Определение* DNN</span><span class="sxs-lookup"><span data-stu-id="cc173-113">*Define* DNN</span></span>
- <span data-ttu-id="cc173-114">Определение *DNN*</span><span class="sxs-lookup"><span data-stu-id="cc173-114">DNN *definition*</span></span>
- <span data-ttu-id="cc173-115">*Expand* DNN</span><span class="sxs-lookup"><span data-stu-id="cc173-115">*Expand* DNN</span></span>
- <span data-ttu-id="cc173-116">Расширение *DNN*</span><span class="sxs-lookup"><span data-stu-id="cc173-116">DNN *expansion*</span></span>
- <span data-ttu-id="cc173-117">*Значение* DNN</span><span class="sxs-lookup"><span data-stu-id="cc173-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="cc173-118">DNN *означает*</span><span class="sxs-lookup"><span data-stu-id="cc173-118">DNN *means*</span></span>

<span data-ttu-id="cc173-119">Результат включает все значения DNN, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc173-119">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="cc173-120">Чтобы вызвать соответствующие ответы, пользователи должны ввести  запрос, включающий указанные ключевые слова аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="cc173-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="cc173-121">Запросы аббревиатуры не чувствительны к делу.</span><span class="sxs-lookup"><span data-stu-id="cc173-121">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="cc173-122">Настройка ответов на аббревиатуры</span><span class="sxs-lookup"><span data-stu-id="cc173-122">Set up Acronyms answers</span></span>

<span data-ttu-id="cc173-123">В Центре [администрирования Microsoft 365](https://admin.microsoft.com)перейдите в акронимы [**и**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)выберите "Добавить **акроним".**</span><span class="sxs-lookup"><span data-stu-id="cc173-123">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronym**.</span></span>

<span data-ttu-id="cc173-124">Поиск (Майкрософт) запрашивает два источника данных, чтобы предоставить акронимы ответы на поисковые запросы пользователей:</span><span class="sxs-lookup"><span data-stu-id="cc173-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="cc173-125">**Редакционные аббревиатуры.**</span><span class="sxs-lookup"><span data-stu-id="cc173-125">**Editorial acronyms**.</span></span> <span data-ttu-id="cc173-126">Предоставляется ИТ-администраторами в [Центре администрирования.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)</span><span class="sxs-lookup"><span data-stu-id="cc173-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="cc173-127">**Минные акронимы.**</span><span class="sxs-lookup"><span data-stu-id="cc173-127">**Mined acronyms**.</span></span> <span data-ttu-id="cc173-128">Mined by Microsoft Search from the user's personal email and documents and publicly available data within the organization.</span><span class="sxs-lookup"><span data-stu-id="cc173-128">Mined by Microsoft Search from the user’s personal email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-editorial-acronyms"></a><span data-ttu-id="cc173-129">Настройка редакционных акронимов</span><span class="sxs-lookup"><span data-stu-id="cc173-129">Set up editorial acronyms</span></span>

<span data-ttu-id="cc173-130">Администраторы поиска могут настроить редакционные акронимы на вкладке ["Акронимы"](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) в Центре администрирования Поиска [(Майкрософт).](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)</span><span class="sxs-lookup"><span data-stu-id="cc173-130">Search administrators can set up editorial acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="cc173-131">В Центр администрирования можно добавить акронимы из любого внутреннего сайта или репозитория.</span><span class="sxs-lookup"><span data-stu-id="cc173-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="cc173-132">Редакционные аббревиатуры можно добавить в состояние **"Опубликовано"** или **"Черновик":**</span><span class="sxs-lookup"><span data-stu-id="cc173-132">Editorial acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="cc173-133">**Состояние публикации.**</span><span class="sxs-lookup"><span data-stu-id="cc173-133">**Published state**.</span></span> <span data-ttu-id="cc173-134">Акронимы доступны сотрудникам организации через Поиск (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="cc173-134">Acronyms are available to the organization’s employees through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="cc173-135">Чтобы акронимы, добавленные в состояние "Опубликовано", стали доступными в Поиске (Майкрософт), может потребоваться до трех дней.</span><span class="sxs-lookup"><span data-stu-id="cc173-135">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="cc173-136">**Состояние черновика.**</span><span class="sxs-lookup"><span data-stu-id="cc173-136">**Draft state**.</span></span> <span data-ttu-id="cc173-137">Если администраторы хотят просмотреть ответы на аббревиатуры, прежде чем сделать их доступными в Поиске (Майкрософт), они могут добавить акронимы в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="cc173-137">If admins want to review Acronyms answers before making them available in Microsoft Search, they can add the acronyms to Draft state.</span></span> <span data-ttu-id="cc173-138">Акронимы, добавленные в состояние черновика, недоступны в Поиске (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="cc173-138">Acronyms added to Draft state aren’t available in Microsoft Search.</span></span> <span data-ttu-id="cc173-139">Администраторам необходимо добавить акронимы в состояние "Опубликовано", чтобы сделать их доступными.</span><span class="sxs-lookup"><span data-stu-id="cc173-139">Admins need to add the acronyms to Published state to make them available.</span></span>

<span data-ttu-id="cc173-140">Администраторы могут добавлять акронимы по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="cc173-140">Admins can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="cc173-141">Загрузите CSV-файл с полями, показанными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="cc173-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="cc173-142">Аббревиатура (обязательная)</span><span class="sxs-lookup"><span data-stu-id="cc173-142">Acronym (mandatory)</span></span> | <span data-ttu-id="cc173-143">Расширение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="cc173-143">Expansion (mandatory)</span></span> | <span data-ttu-id="cc173-144">Описание</span><span class="sxs-lookup"><span data-stu-id="cc173-144">Description</span></span>  | <span data-ttu-id="cc173-145">Source</span><span class="sxs-lookup"><span data-stu-id="cc173-145">Source</span></span> | <span data-ttu-id="cc173-146">Состояние (обязательно)</span><span class="sxs-lookup"><span data-stu-id="cc173-146">State (mandatory)</span></span> |
| --------- | --------- | ---------- | --------- |--------- |
| <span data-ttu-id="cc173-147">*XXX*</span><span class="sxs-lookup"><span data-stu-id="cc173-147">*XXX*</span></span> | <span data-ttu-id="cc173-148">*Орфографию аббревиатуры*</span><span class="sxs-lookup"><span data-stu-id="cc173-148">*Spelled out abbreviation*</span></span> |  | <span data-ttu-id="cc173-149">*URL-адрес*</span><span class="sxs-lookup"><span data-stu-id="cc173-149">*URL*</span></span> | <span data-ttu-id="cc173-150">*Опубликованные или черновики*</span><span class="sxs-lookup"><span data-stu-id="cc173-150">*Published or Draft*</span></span> |

### <a name="csv-fields"></a><span data-ttu-id="cc173-151">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="cc173-151">CSV fields</span></span>

<span data-ttu-id="cc173-152">**Аббревиатура**.</span><span class="sxs-lookup"><span data-stu-id="cc173-152">**Acronym**.</span></span> <span data-ttu-id="cc173-153">Содержит фактическую краткую форму или акроним.</span><span class="sxs-lookup"><span data-stu-id="cc173-153">Contains the actual short form or acronym.</span></span> <span data-ttu-id="cc173-154">Примером является *DNN*.</span><span class="sxs-lookup"><span data-stu-id="cc173-154">An example is *DNN*.</span></span>

<span data-ttu-id="cc173-155">**Расширение.**</span><span class="sxs-lookup"><span data-stu-id="cc173-155">**Expansion**.</span></span> <span data-ttu-id="cc173-156">Содержит расширение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="cc173-156">Contains the expansion of the acronym.</span></span> <span data-ttu-id="cc173-157">В качестве примера можно *привести deep Neural Network.*</span><span class="sxs-lookup"><span data-stu-id="cc173-157">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="cc173-158">**Описание.**</span><span class="sxs-lookup"><span data-stu-id="cc173-158">**Description**.</span></span> <span data-ttu-id="cc173-159">Краткое описание аббревиатуры, которая предоставляет пользователям дополнительные сведения об аббревиатуре и его расширении.</span><span class="sxs-lookup"><span data-stu-id="cc173-159">A brief description of the acronym that gives users more info about the acronym and its expansion.</span></span> <span data-ttu-id="cc173-160">Например, глубокая нейронная сеть — это нейронная сеть с определенным уровнем сложности, нейронная сеть с более *чем двумя уровнями.*</span><span class="sxs-lookup"><span data-stu-id="cc173-160">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="cc173-161">**Источник**</span><span class="sxs-lookup"><span data-stu-id="cc173-161">**Source**.</span></span> <span data-ttu-id="cc173-162">URL-адрес страницы или веб-сайта, где пользователи должны получить дополнительные сведения об аббревиатуре.</span><span class="sxs-lookup"><span data-stu-id="cc173-162">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="cc173-163">**State**.</span><span class="sxs-lookup"><span data-stu-id="cc173-163">**State**.</span></span> <span data-ttu-id="cc173-164">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="cc173-164">This field can take two values:</span></span>

- <span data-ttu-id="cc173-165">**Черновик**.</span><span class="sxs-lookup"><span data-stu-id="cc173-165">**Draft**.</span></span> <span data-ttu-id="cc173-166">Добавляет аббревиатуру в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="cc173-166">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="cc173-167">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="cc173-167">**Published**.</span></span> <span data-ttu-id="cc173-168">Добавляет акроним в состояние "Опубликовано" и делает его доступным в Поиске (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="cc173-168">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="mined-acronyms"></a><span data-ttu-id="cc173-169">Минные акронимы</span><span class="sxs-lookup"><span data-stu-id="cc173-169">Mined acronyms</span></span>

<span data-ttu-id="cc173-170">Администраторам может быть трудно добавить все акронимы, используемые в организации, в ответы.</span><span class="sxs-lookup"><span data-stu-id="cc173-170">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="cc173-171">Эта функция может находить аббревиатуры, о которых администраторы поиска даже не знают.</span><span class="sxs-lookup"><span data-stu-id="cc173-171">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="cc173-172">Для этого Поиск (Майкрософт) также разместит акронимы из этих источников:</span><span class="sxs-lookup"><span data-stu-id="cc173-172">To do that work, Microsoft Search also mines acronyms from these sources:</span></span>

- <span data-ttu-id="cc173-173">Сообщения электронной почты пользователей.</span><span class="sxs-lookup"><span data-stu-id="cc173-173">Users’ emails.</span></span>
- <span data-ttu-id="cc173-174">Документы в [SharePoint,](https://products.office.com/sharepoint/collaboration) [Microsoft OneDrive]( https://onedrive.live.com/about/)и [Microsoft OneNote.](https://www.onenote.com/)</span><span class="sxs-lookup"><span data-stu-id="cc173-174">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/).</span></span>
- <span data-ttu-id="cc173-175">Общедоступные документы в организации, к которые пользователи имеют доступ в SharePoint, OneDrive или OneNote.</span><span class="sxs-lookup"><span data-stu-id="cc173-175">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote.</span></span>

<span data-ttu-id="cc173-176">Поиск (Майкрософт) позволяет убедиться, что только пользователи с доступом и разрешениями на доступ к документу могут видеть акронимы, которые из него минуются.</span><span class="sxs-lookup"><span data-stu-id="cc173-176">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are mined from it.</span></span> <span data-ttu-id="cc173-177">Когда акроним минуется из почтового ящика пользователя, его может видеть только этот пользователь.</span><span class="sxs-lookup"><span data-stu-id="cc173-177">When an acronym is mined from a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="cc173-178">Для минных акронимов настройка не требуется.</span><span class="sxs-lookup"><span data-stu-id="cc173-178">No setup is needed for mined acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="cc173-179">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="cc173-179">Frequently asked questions</span></span>

<span data-ttu-id="cc173-180">**Вопрос. Как ранжирована редакционная и минированная информация?**</span><span class="sxs-lookup"><span data-stu-id="cc173-180">**Q: How is editorial and mined data ranked?**</span></span>

<span data-ttu-id="cc173-181">**О.** Ранжирование результатов может отличаться в зависимости от пользователя, так как результаты персонализированы для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc173-181">**A:** The ranking of results may vary from person to person as results are personalized for each user.</span></span>

<span data-ttu-id="cc173-182">**Вопрос. Сколько времени должно занять, чтобы редакционные акронимы были видны в Поиске (Майкрософт) после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="cc173-182">**Q: How long does it take for editorial acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="cc173-183">**О.**  Чтобы акронимы, добавленные в состояние "Опубликовано", стали доступными в Поиске (Майкрософт), требуется до трех дней.</span><span class="sxs-lookup"><span data-stu-id="cc173-183">**A:**  It takes up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="cc173-184">**Вопрос. Как пользователи вызывают ответы на аббревиатуры?**</span><span class="sxs-lookup"><span data-stu-id="cc173-184">**Q: How do users trigger Acronyms answers?**</span></span>

<span data-ttu-id="cc173-185">**Ответ.** Чтобы получить ответы на акронимы, пользователи должны ввести определенные шаблоны запросов в поле поиска [Bing,](https://bing.com) [SharePoint](https://products.office.com/sharepoint/collaboration)или [Office 365.](https://Office.com) </span><span class="sxs-lookup"><span data-stu-id="cc173-185">**A**: To get Acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="cc173-186">**Вопрос. Сколько времени займет, чтобы минные акронимы появились после получения или отправки нового сообщения электронной почты или документа?**</span><span class="sxs-lookup"><span data-stu-id="cc173-186">**Q: How long does it take for mined acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="cc173-187">**О.** На то, чтобы в результатах Поиска (Майкрософт) появлялись минные аббревиатуры из нового сообщения электронной почты или документа, необходимо до семи дней.</span><span class="sxs-lookup"><span data-stu-id="cc173-187">**A:** Mined acronyms from a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="cc173-188">**Вопрос. Должны ли документы быть в определенном формате, чтобы их можно было найти в майнинге?**</span><span class="sxs-lookup"><span data-stu-id="cc173-188">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="cc173-189">**О.** Нет.</span><span class="sxs-lookup"><span data-stu-id="cc173-189">**A:** No.</span></span> <span data-ttu-id="cc173-190">Поддерживаются все типы файлов, кроме изображений, папок и ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="cc173-190">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="cc173-191">**Вопрос. Будет ли Майкрософт доминировать акронимы из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="cc173-191">**Q: Will Microsoft mine acronyms from documents in all languages?**</span></span>

<span data-ttu-id="cc173-192">**О.** Корпорация Майкрософт поддерживает только майнинг документов на английском языке.</span><span class="sxs-lookup"><span data-stu-id="cc173-192">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="cc173-193">Поддержка других языков будет добавлена поэтапно.</span><span class="sxs-lookup"><span data-stu-id="cc173-193">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="cc173-194">**Вопрос. Что делать, если моя организация не хочет показывать минные акронимы? Можно ли перестать показывать в результатах поиска минные акронимы?**</span><span class="sxs-lookup"><span data-stu-id="cc173-194">**Q: What if my organization doesn’t want to show mined acronyms? Can I stop showing mined acronyms in search results?**</span></span>

<span data-ttu-id="cc173-195">**A.** Чтобы отключить отображение минных акронимов в результатах поиска, создайте запрос в службу поддержки клиентов, следуя инструкциям в службе поддержки по продуктам [для бизнеса.](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support)</span><span class="sxs-lookup"><span data-stu-id="cc173-195">**A**: To turn off showing mined acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span></span>
<span data-ttu-id="cc173-196">После создания запроса в службу поддержки минные акронимы перестают отображаться в результатах поиска в течение 48 часов.</span><span class="sxs-lookup"><span data-stu-id="cc173-196">After you create a support ticket, it takes up to 48 hours for mined acronyms to stop appearing in search results.</span></span>
