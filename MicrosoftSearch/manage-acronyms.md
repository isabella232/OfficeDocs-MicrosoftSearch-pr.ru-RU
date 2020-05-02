---
title: Управление сокращениями ответов в Microsoft Search
ms.author: v-pamcna
author: TrishaMc1
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Создание и обновление аббревиатур ответов в Microsoft Search
ms.openlocfilehash: aa857cefe9a2a40a8519a91829e327d01a3f2391
ms.sourcegitcommit: 25cdb5e6111ec6bc6c130a36aa5f13a6328e1092
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "42928232"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="7b831-103">Управление сокращениями ответов в Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="7b831-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="7b831-104">Сотрудники часто работают в незнакомых акронимах и аббревиатурах, используемых в организации или группе.</span><span class="sxs-lookup"><span data-stu-id="7b831-104">Employees often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="7b831-105">Термины, относящиеся к организациям или командам, могут быть новыми для людей, которые переходят от одной команды к другой, кто работает с внутренними партнерами или новые сотрудники.</span><span class="sxs-lookup"><span data-stu-id="7b831-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, those who work with internal partner teams, or new employees.</span></span>

<span data-ttu-id="7b831-106">Организации не всегда имеют одну ссылку для стандартных терминов.</span><span class="sxs-lookup"><span data-stu-id="7b831-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="7b831-107">Отсутствие одной ссылки затрудняет поиск определений или расширений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="7b831-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="7b831-108">Служба поиска Майкрософт решает эту проблему с акронимами.</span><span class="sxs-lookup"><span data-stu-id="7b831-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="7b831-109">Взаимодействие с пользователями</span><span class="sxs-lookup"><span data-stu-id="7b831-109">What users experience</span></span>
<span data-ttu-id="7b831-110">Пользователи службы поиска Майкрософт могут получать определения с акронимами в [Bing](https://Bing.com), [Microsoft Office 365](https://Office.com)и [Microsoft SharePoint Online](https://products.office.com/sharepoint/collaboration).</span><span class="sxs-lookup"><span data-stu-id="7b831-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [Microsoft Office 365](https://Office.com), and [Microsoft SharePoint Online](https://products.office.com/sharepoint/collaboration).</span></span> <span data-ttu-id="7b831-111">В полях **поиска** в строках заголовков пользователи вводят запросы, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="7b831-111">In the **Search** boxes in the header bars, users enter queries like these examples:</span></span>

- <span data-ttu-id="7b831-112">*Что такое* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-112">*What is* DNN</span></span>
- <span data-ttu-id="7b831-113">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-113">*Define* DNN</span></span>
- <span data-ttu-id="7b831-114">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-114">DNN *definition*</span></span>
- <span data-ttu-id="7b831-115">*Разверните узел* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-115">*Expand* DNN</span></span>
- <span data-ttu-id="7b831-116">*Расширение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-116">DNN *expansion*</span></span>
- <span data-ttu-id="7b831-117">*Значение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="7b831-118">ДНН *означает*</span><span class="sxs-lookup"><span data-stu-id="7b831-118">DNN *means*</span></span>

<span data-ttu-id="7b831-119">Предлагаемые результаты включают все значения ДНН, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b831-119">The suggested results include all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="7b831-120">Пользователи должны ввести запрос, включающий указанные *Ключевые слова* аббревиатуры, чтобы активировать соответствующие ответы.</span><span class="sxs-lookup"><span data-stu-id="7b831-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="7b831-121">В запросах акронимов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="7b831-121">Acronym queries are not case sensitive.</span></span> 

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="7b831-122">Настройка аббревиатур ответов</span><span class="sxs-lookup"><span data-stu-id="7b831-122">Set up Acronyms answers</span></span>
<span data-ttu-id="7b831-123">В [центре администрирования](https://admin.microsoft.com)Microsoft 365 откройте раздел **Параметры** > **Microsoft Search** >**акронимы**, а затем выберите команду **Добавить акронимы**.</span><span class="sxs-lookup"><span data-stu-id="7b831-123">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Settings** > **Microsoft Search** >**Acronyms**, and then select **Add acronyms**.</span></span> 

<span data-ttu-id="7b831-124">Служба поиска Microsoft выполняет запрос двух источников данных для сокращения ответов на запросы пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b831-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1.  <span data-ttu-id="7b831-125">**Редакционные акронимы**.</span><span class="sxs-lookup"><span data-stu-id="7b831-125">**Editorial acronyms**.</span></span> <span data-ttu-id="7b831-126">Предоставляется ИТ администраторами в [центре администрирования](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7b831-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com).</span></span>
2.  <span data-ttu-id="7b831-127">**Аббревиатуры mined**.</span><span class="sxs-lookup"><span data-stu-id="7b831-127">**Mined acronyms**.</span></span> <span data-ttu-id="7b831-128">Mined Microsoft Search из личной электронной почты и документов пользователя и общедоступных данных в Организации.</span><span class="sxs-lookup"><span data-stu-id="7b831-128">Mined by Microsoft Search from the user’s personal email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-editorial-acronyms"></a><span data-ttu-id="7b831-129">Настройка редакционных аббревиатур</span><span class="sxs-lookup"><span data-stu-id="7b831-129">Set up editorial acronyms</span></span>
<span data-ttu-id="7b831-130">ИТ администраторы могут настроить редакционные сокращения на [вкладке аббревиатуры](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch) [центра администрирования Microsoft 365]( https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7b831-130">IT admins can set up editorial acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch) in the  [Microsoft 365 admin center]( https://admin.microsoft.com).</span></span> <span data-ttu-id="7b831-131">Вы можете добавлять акронимы из любого внутреннего сайта или репозитория в центр администрирования.</span><span class="sxs-lookup"><span data-stu-id="7b831-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="7b831-132">Редакционные сокращения можно добавлять в состояние **опубликованных** или **черновиков** :</span><span class="sxs-lookup"><span data-stu-id="7b831-132">Editorial acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="7b831-133">**Опубликованное состояние**.</span><span class="sxs-lookup"><span data-stu-id="7b831-133">**Published state**.</span></span> <span data-ttu-id="7b831-134">Аббревиатуры доступны для сотрудников Организации в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="7b831-134">Acronyms are available to the organization’s employees through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="7b831-135">Аббревиатуры, добавленные в опубликованное состояние для получения в Microsoft поиске, могут быть доступны в течение трех дней.</span><span class="sxs-lookup"><span data-stu-id="7b831-135">It might take up  to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="7b831-136">**Состояние черновика**.</span><span class="sxs-lookup"><span data-stu-id="7b831-136">**Draft state**.</span></span> <span data-ttu-id="7b831-137">Если администраторы хотят просмотреть акронимы, прежде чем сделать их доступными в Microsoft Search, они могут добавить аббревиатуры в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="7b831-137">If admins want to review Acronyms answers before making them available in Microsoft Search, they can add the acronyms to Draft state.</span></span> <span data-ttu-id="7b831-138">Аббревиатуры, добавленные в состояние черновика, не поддерживаются в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="7b831-138">Acronyms added to Draft state aren’t available in Microsoft Search.</span></span> <span data-ttu-id="7b831-139">Администраторы должны добавить аббревиатуры в опубликованное состояние, чтобы сделать их доступными.</span><span class="sxs-lookup"><span data-stu-id="7b831-139">Admins need to add the acronyms to Published state to make them available.</span></span>

<span data-ttu-id="7b831-140">Администраторы могут добавлять акронимы по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="7b831-140">Admins can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="7b831-141">Отправьте CSV-файл с полями, приведенными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="7b831-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="7b831-142">Аббревиатура (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7b831-142">Acronym (mandatory)</span></span> | <span data-ttu-id="7b831-143">Расширение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7b831-143">Expansion (mandatory)</span></span> | <span data-ttu-id="7b831-144">Описание</span><span class="sxs-lookup"><span data-stu-id="7b831-144">Description</span></span>  | <span data-ttu-id="7b831-145">Источник</span><span class="sxs-lookup"><span data-stu-id="7b831-145">Source</span></span> | <span data-ttu-id="7b831-146">State (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7b831-146">State (mandatory)</span></span> |
| --------- | --------- | ---------- | --------- |--------- |
| <span data-ttu-id="7b831-147">*XXX*</span><span class="sxs-lookup"><span data-stu-id="7b831-147">*XXX*</span></span> | <span data-ttu-id="7b831-148">*Сокращенное сокращение*</span><span class="sxs-lookup"><span data-stu-id="7b831-148">*Spelled out abbreviation*</span></span> |  | <span data-ttu-id="7b831-149">*URL*</span><span class="sxs-lookup"><span data-stu-id="7b831-149">*URL*</span></span> | <span data-ttu-id="7b831-150">*Опубликовано или черновик*</span><span class="sxs-lookup"><span data-stu-id="7b831-150">*Published or Draft*</span></span> |

### <a name="csv-fields"></a><span data-ttu-id="7b831-151">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="7b831-151">CSV fields</span></span>
<span data-ttu-id="7b831-152">**Акроним**.</span><span class="sxs-lookup"><span data-stu-id="7b831-152">**Acronym**.</span></span> <span data-ttu-id="7b831-153">Содержит собственно краткую форму или аббревиатуру.</span><span class="sxs-lookup"><span data-stu-id="7b831-153">Contains the actual short form or acronym.</span></span> <span data-ttu-id="7b831-154">Пример: *днн*.</span><span class="sxs-lookup"><span data-stu-id="7b831-154">An example is *DNN*.</span></span>

<span data-ttu-id="7b831-155">**Расширение**.</span><span class="sxs-lookup"><span data-stu-id="7b831-155">**Expansion**.</span></span> <span data-ttu-id="7b831-156">Содержит расширение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="7b831-156">Contains the expansion of the acronym.</span></span> <span data-ttu-id="7b831-157">Примером является *глубокая нейронная сеть*.</span><span class="sxs-lookup"><span data-stu-id="7b831-157">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="7b831-158">**Description**.</span><span class="sxs-lookup"><span data-stu-id="7b831-158">**Description**.</span></span> <span data-ttu-id="7b831-159">Краткое описание аббревиатуры, которое дает пользователям подробные сведения о том, что аббревиатура и его расширение.</span><span class="sxs-lookup"><span data-stu-id="7b831-159">A brief description of the acronym that gives users quick insight into what the acronym and its expansion mean.</span></span> <span data-ttu-id="7b831-160">Например, *глубокая нейронная сеть — это нейронная сеть с определенным уровнем сложности и нейронной сетью с более чем двумя уровнями*.</span><span class="sxs-lookup"><span data-stu-id="7b831-160">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="7b831-161">**Источник**.</span><span class="sxs-lookup"><span data-stu-id="7b831-161">**Source**.</span></span> <span data-ttu-id="7b831-162">URL-адрес страницы или веб-сайта, на который необходимо перейти, для получения дополнительных сведений об акрониме.</span><span class="sxs-lookup"><span data-stu-id="7b831-162">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="7b831-163">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="7b831-163">**State**.</span></span> <span data-ttu-id="7b831-164">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="7b831-164">This field can take two values:</span></span>

- <span data-ttu-id="7b831-165">**Черновик**.</span><span class="sxs-lookup"><span data-stu-id="7b831-165">**Draft**.</span></span> <span data-ttu-id="7b831-166">Добавляет аббревиатуру в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="7b831-166">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="7b831-167">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="7b831-167">**Published**.</span></span> <span data-ttu-id="7b831-168">Добавляет акроним к опубликованному состоянию и делает его доступным в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="7b831-168">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="mined-acronyms"></a><span data-ttu-id="7b831-169">Аббревиатуры mined</span><span class="sxs-lookup"><span data-stu-id="7b831-169">Mined acronyms</span></span>
<span data-ttu-id="7b831-170">Администраторам может быть трудно добавить все аббревиатуры, используемые в Организации, для ответа.</span><span class="sxs-lookup"><span data-stu-id="7b831-170">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="7b831-171">Эта функция может находить акронимы, которые даже не знают администраторам поиска.</span><span class="sxs-lookup"><span data-stu-id="7b831-171">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="7b831-172">Для этого в Microsoft Search также не включены акронимы из этих источников:</span><span class="sxs-lookup"><span data-stu-id="7b831-172">To do that work, Microsoft Search also mines acronyms from these sources:</span></span>

- <span data-ttu-id="7b831-173">Сообщения электронной почты пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b831-173">Users’ emails.</span></span>
- <span data-ttu-id="7b831-174">Документы в [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/) и [Microsoft OneNote](http://www.onenote.com/).</span><span class="sxs-lookup"><span data-stu-id="7b831-174">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/) and [Microsoft OneNote](http://www.onenote.com/).</span></span>
- <span data-ttu-id="7b831-175">Общедоступные документы в Организации, к которым пользователи имеют доступ в SharePoint, OneDrive или OneNote.</span><span class="sxs-lookup"><span data-stu-id="7b831-175">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote.</span></span>

<span data-ttu-id="7b831-176">Служба поиска Майкрософт гарантирует, что только те пользователи, у которых есть доступ и разрешения на доступ к документу, смогут видеть акронимы, mined от него.</span><span class="sxs-lookup"><span data-stu-id="7b831-176">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are mined from it.</span></span> <span data-ttu-id="7b831-177">Аббревиатуры mined из папки "Входящие" пользователя и хранятся в сегментах пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b831-177">The acronyms are mined from a user’s inbox and stored in the user shard.</span></span> <span data-ttu-id="7b831-178">Только пользователь может получить доступ к акронимам mined из папки "Входящие" пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b831-178">Only the user can access the acronyms mined from the user’s own inbox.</span></span>

> [!NOTE]
> <span data-ttu-id="7b831-179">Для акронимов mined не требуется настройка ИТ-администратора.</span><span class="sxs-lookup"><span data-stu-id="7b831-179">No IT admin setup is needed for mined acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7b831-180">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="7b831-180">Frequently asked questions</span></span>
<span data-ttu-id="7b831-181">**Вопрос: как редакционные и mined-данные ранжированы?**</span><span class="sxs-lookup"><span data-stu-id="7b831-181">**Q: How is editorial and mined data ranked?**</span></span>

<span data-ttu-id="7b831-182">**A:** В настоящее время функция, в настоящее время, ранжирует акронимы над акронимами mined.</span><span class="sxs-lookup"><span data-stu-id="7b831-182">**A:** The feature currently ranks editorial acronyms above mined acronyms.</span></span>

<span data-ttu-id="7b831-183">**В. Сколько времени займет отображение редакционных аббревиатур в Microsoft Search после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="7b831-183">**Q: How long does it take for editorial acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="7b831-184">**A:**  Аббревиатуры, добавленные к опубликованному состоянию, становятся доступны в Microsoft Search в течение трех дней.</span><span class="sxs-lookup"><span data-stu-id="7b831-184">**A:**  It takes up  to three days for acronyms added to Published state to become available in Microsoft Search.</span></span> 

<span data-ttu-id="7b831-185">**Вопрос: как пользователи инициируют акронимы?**</span><span class="sxs-lookup"><span data-stu-id="7b831-185">**Q: How do users trigger Acronyms answers?**</span></span>

<span data-ttu-id="7b831-186">Ответ: чтобы получить акронимы **, пользователи**должны ввести определенные шаблоны запросов в поле поиска [Bing](https://bing.com), [Office 365](https://Office.com)или [SharePoint](https://products.office.com/sharepoint/collaboration) **Search** .</span><span class="sxs-lookup"><span data-stu-id="7b831-186">**A**: To get Acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [Office 365](https://Office.com), or [SharePoint](https://products.office.com/sharepoint/collaboration) **Search** box.</span></span> <span data-ttu-id="7b831-187">Ниже приведены примеры запросов, в которых можно найти ответы на термин *днн* .</span><span class="sxs-lookup"><span data-stu-id="7b831-187">Examples of queries that find answers for the term *DNN* are as follows:</span></span>

- <span data-ttu-id="7b831-188">*Что такое* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-188">*What is* DNN</span></span>
- <span data-ttu-id="7b831-189">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-189">*Define* DNN</span></span>
- <span data-ttu-id="7b831-190">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-190">DNN *definition*</span></span>
- <span data-ttu-id="7b831-191">*Разверните узел* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-191">*Expand* DNN</span></span>
- <span data-ttu-id="7b831-192">*Расширение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-192">DNN *expansion*</span></span>
- <span data-ttu-id="7b831-193">*Значение* днн</span><span class="sxs-lookup"><span data-stu-id="7b831-193">*Meaning of* DNN</span></span>
- <span data-ttu-id="7b831-194">ДНН *означает*</span><span class="sxs-lookup"><span data-stu-id="7b831-194">DNN *means*</span></span>

<span data-ttu-id="7b831-195">**В. Сколько времени займет отображение аббревиатур mined после получения или отправки нового сообщения или документа?**</span><span class="sxs-lookup"><span data-stu-id="7b831-195">**Q: How long does it take for mined acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="7b831-196">**A:** Mined сокращения из нового сообщения электронной почты или документа составляют до семи дней, чтобы они отображались в результатах поиска Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b831-196">**A:** Mined acronyms from a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="7b831-197">**Вопрос: должны ли документы относиться к определенному формату для интеллектуального анализа данных?**</span><span class="sxs-lookup"><span data-stu-id="7b831-197">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="7b831-198">**A:** Нет.</span><span class="sxs-lookup"><span data-stu-id="7b831-198">**A:** No.</span></span> <span data-ttu-id="7b831-199">Мы поддерживаем все типы файлов, за исключением изображений, папок и ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="7b831-199">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="7b831-200">**В.: будут акронимы из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="7b831-200">**Q: Will Microsoft mine acronyms from documents in all languages?**</span></span>

<span data-ttu-id="7b831-201">О **. Корпорация**Майкрософт поддерживает интеллектуальную анализ только из документов на английском языке.</span><span class="sxs-lookup"><span data-stu-id="7b831-201">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="7b831-202">Поддержка других языков будет добавляться поэтапно.</span><span class="sxs-lookup"><span data-stu-id="7b831-202">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="7b831-203">**Вопрос: что делать, если в Организации не требуется показывать акронимы mined? Можно ли остановить показ аббревиатур mined в результатах поиска?**</span><span class="sxs-lookup"><span data-stu-id="7b831-203">**Q: What if my organization doesn’t want to show mined acronyms? Can I stop showing mined acronyms in search results?**</span></span>

<span data-ttu-id="7b831-204">**А**: чтобы отключить отображение акронимов mined в результатах поиска, создайте билет поддержки клиентов, следуя инструкциям в статье [Поддержка для бизнеса](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span><span class="sxs-lookup"><span data-stu-id="7b831-204">**A**: To turn off showing mined acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span></span>
<span data-ttu-id="7b831-205">После создания билета в службу поддержки для аббревиатур mined в результатах поиска потребуется до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="7b831-205">After you create a support ticket, it takes up to 48 hours for mined acronyms to stop appearing in search results.</span></span> 

<span data-ttu-id="7b831-206">**В. когда я буду видеть акронимы ответы в [Office 365](https://Office.com) и [SharePoint Online](https://products.office.com/sharepoint/collaboration)?**</span><span class="sxs-lookup"><span data-stu-id="7b831-206">**Q: When will I see Acronyms answers in [Office 365](https://Office.com) and [SharePoint Online](https://products.office.com/sharepoint/collaboration)?**</span></span>

<span data-ttu-id="7b831-207">**A**: в настоящее время ответы на аббревиатуры доступны только в Microsoft Search в [Bing](https://bing.com).</span><span class="sxs-lookup"><span data-stu-id="7b831-207">**A**: Acronyms answers are currently only available in Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="7b831-208">Они будут сведены в Office 365 и SharePoint Online в 2020.</span><span class="sxs-lookup"><span data-stu-id="7b831-208">They’ll be rolled out to Office 365 and SharePoint Online in 2020.</span></span>
