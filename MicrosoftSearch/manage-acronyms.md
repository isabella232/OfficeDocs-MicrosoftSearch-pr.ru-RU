---
title: Управление сокращениями ответов в Microsoft Search
ms.author: v-pamcna
author: TrishaMc1
manager: mnirkhe
ms.date: 10/28/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Создание и обновление аббревиатур ответов в Microsoft Search
ms.openlocfilehash: 8ff48f1eaa4ef8dab83411fad2f0ee4367158cd1
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "37950018"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="ffb0d-103">Управление сокращениями ответов в Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="ffb0d-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="ffb0d-104">Сотрудники часто работают в незнакомых акронимах и аббревиатурах, используемых в организации или группе.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-104">Employees often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="ffb0d-105">Термины, относящиеся к организациям или командам, могут быть новыми для людей, которые переходят от одной команды к другой, кто работает с внутренними партнерами или новые сотрудники.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, those who work with internal partner teams, or new employees.</span></span>

<span data-ttu-id="ffb0d-106">Организации не всегда имеют одну ссылку для стандартных терминов.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="ffb0d-107">Отсутствие одной ссылки затрудняет поиск определений или расширений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="ffb0d-108">Служба поиска Майкрософт решает эту проблему с акронимами.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="ffb0d-109">Взаимодействие с пользователями</span><span class="sxs-lookup"><span data-stu-id="ffb0d-109">What users experience</span></span>
<span data-ttu-id="ffb0d-110">Пользователи службы поиска Майкрософт могут получать определения с акронимами в [Bing](https://Bing.com), [Microsoft Office 365](https://Office.com)и [Microsoft SharePoint Online](https://products.office.com/sharepoint/collaboration).</span><span class="sxs-lookup"><span data-stu-id="ffb0d-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [Microsoft Office 365](https://Office.com), and [Microsoft SharePoint Online](https://products.office.com/sharepoint/collaboration).</span></span> <span data-ttu-id="ffb0d-111">В полях **поиска** в строках заголовков пользователи вводят запросы, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="ffb0d-111">In the **Search** boxes in the header bars, users enter queries like these examples:</span></span>

- <span data-ttu-id="ffb0d-112">*Что такое* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-112">*What is* DNN</span></span>
- <span data-ttu-id="ffb0d-113">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-113">*Define* DNN</span></span>
- <span data-ttu-id="ffb0d-114">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-114">DNN *definition*</span></span>
- <span data-ttu-id="ffb0d-115">*Разверните узел* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-115">*Expand* DNN</span></span>
- <span data-ttu-id="ffb0d-116">*Расширение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-116">DNN *expansion*</span></span>
- <span data-ttu-id="ffb0d-117">*Значение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="ffb0d-118">ДНН *означает*</span><span class="sxs-lookup"><span data-stu-id="ffb0d-118">DNN *means*</span></span>

<span data-ttu-id="ffb0d-119">Предлагаемые результаты включают все значения ДНН, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-119">The suggested results include all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb0d-120">Пользователи должны ввести запрос, включающий указанные *Ключевые слова* аббревиатуры, чтобы активировать соответствующие ответы.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span>  

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="ffb0d-121">Настройка аббревиатур ответов</span><span class="sxs-lookup"><span data-stu-id="ffb0d-121">Set up Acronyms answers</span></span>
<span data-ttu-id="ffb0d-122">В [центре администрирования](https://admin.microsoft.com)Microsoft 365 откройте раздел **Параметры** > **Microsoft Search** >**акронимы**, а затем выберите команду **Добавить акронимы**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-122">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Settings** > **Microsoft Search** >**Acronyms**, and then select **Add acronyms**.</span></span> 

<span data-ttu-id="ffb0d-123">Служба поиска Microsoft выполняет запрос двух источников данных для сокращения ответов на запросы пользователей.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-123">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1.  <span data-ttu-id="ffb0d-124">**Редакционные акронимы**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-124">**Editorial acronyms**.</span></span> <span data-ttu-id="ffb0d-125">Предоставляется ИТ администраторами в [центре администрирования](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ffb0d-125">Provided by IT administrators in the [admin center](https://admin.microsoft.com).</span></span>
2.  <span data-ttu-id="ffb0d-126">**Аббревиатуры mined**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-126">**Mined acronyms**.</span></span> <span data-ttu-id="ffb0d-127">Mined Microsoft Search из личной электронной почты и документов пользователя и общедоступных данных в Организации.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-127">Mined by Microsoft Search from the user’s personal email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-editorial-acronyms"></a><span data-ttu-id="ffb0d-128">Настройка редакционных аббревиатур</span><span class="sxs-lookup"><span data-stu-id="ffb0d-128">Set up editorial acronyms</span></span>
<span data-ttu-id="ffb0d-129">ИТ администраторы могут настроить редакционные сокращения на [вкладке аббревиатуры](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch) [центра администрирования Microsoft 365]( https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ffb0d-129">IT admins can set up editorial acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch) in the  [Microsoft 365 admin center]( https://admin.microsoft.com).</span></span> <span data-ttu-id="ffb0d-130">Вы можете добавлять акронимы из любого внутреннего сайта или репозитория в центр администрирования.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-130">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="ffb0d-131">Редакционные сокращения можно добавлять в состояние **опубликованных** или **черновиков** :</span><span class="sxs-lookup"><span data-stu-id="ffb0d-131">Editorial acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="ffb0d-132">**Опубликованное состояние**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-132">**Published state**.</span></span> <span data-ttu-id="ffb0d-133">Аббревиатуры доступны для сотрудников Организации в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-133">Acronyms are available to the organization’s employees through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb0d-134">Аббревиатуры, добавленные в опубликованное состояние для получения в Microsoft поиске, могут быть доступны в течение трех дней.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-134">It might take up  to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="ffb0d-135">**Состояние черновика**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-135">**Draft state**.</span></span> <span data-ttu-id="ffb0d-136">Если администраторы хотят просмотреть акронимы, прежде чем сделать их доступными в Microsoft Search, они могут добавить аббревиатуры в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-136">If admins want to review Acronyms answers before making them available in Microsoft Search, they can add the acronyms to Draft state.</span></span> <span data-ttu-id="ffb0d-137">Аббревиатуры, добавленные в состояние черновика, не поддерживаются в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-137">Acronyms added to Draft state aren’t available in Microsoft Search.</span></span> <span data-ttu-id="ffb0d-138">Администраторы должны добавить аббревиатуры в опубликованное состояние, чтобы сделать их доступными.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-138">Admins need to add the acronyms to Published state to make them available.</span></span>

<span data-ttu-id="ffb0d-139">Администраторы могут добавлять акронимы по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-139">Admins can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="ffb0d-140">Отправьте CSV-файл с полями, приведенными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="ffb0d-140">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="ffb0d-141">Аббревиатура (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ffb0d-141">Acronym (mandatory)</span></span> | <span data-ttu-id="ffb0d-142">Расширение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ffb0d-142">Expansion (mandatory)</span></span> | <span data-ttu-id="ffb0d-143">Описание</span><span class="sxs-lookup"><span data-stu-id="ffb0d-143">Description</span></span>  | <span data-ttu-id="ffb0d-144">Источник</span><span class="sxs-lookup"><span data-stu-id="ffb0d-144">Source</span></span> | <span data-ttu-id="ffb0d-145">State (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ffb0d-145">State (mandatory)</span></span> |
| --------- | --------- | ---------- | --------- |--------- |
| <span data-ttu-id="ffb0d-146">*XXX*</span><span class="sxs-lookup"><span data-stu-id="ffb0d-146">*XXX*</span></span> | <span data-ttu-id="ffb0d-147">*Сокращенное сокращение*</span><span class="sxs-lookup"><span data-stu-id="ffb0d-147">*Spelled out abbreviation*</span></span> |  | <span data-ttu-id="ffb0d-148">*URL*</span><span class="sxs-lookup"><span data-stu-id="ffb0d-148">*URL*</span></span> | <span data-ttu-id="ffb0d-149">*Опубликовано или черновик*</span><span class="sxs-lookup"><span data-stu-id="ffb0d-149">*Published or Draft*</span></span> |

### <a name="csv-fields"></a><span data-ttu-id="ffb0d-150">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="ffb0d-150">CSV fields</span></span>
<span data-ttu-id="ffb0d-151">**Акроним**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-151">**Acronym**.</span></span> <span data-ttu-id="ffb0d-152">Содержит собственно краткую форму или аббревиатуру.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-152">Contains the actual short form or acronym.</span></span> <span data-ttu-id="ffb0d-153">Пример: *днн*.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-153">An example is *DNN*.</span></span>

<span data-ttu-id="ffb0d-154">**Расширение**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-154">**Expansion**.</span></span> <span data-ttu-id="ffb0d-155">Содержит расширение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-155">Contains the expansion of the acronym.</span></span> <span data-ttu-id="ffb0d-156">Примером является *глубокая нейронная сеть*.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-156">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="ffb0d-157">**Description**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-157">**Description**.</span></span> <span data-ttu-id="ffb0d-158">Краткое описание аббревиатуры, которое дает пользователям подробные сведения о том, что аббревиатура и его расширение.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-158">A brief description of the acronym that gives users quick insight into what the acronym and its expansion mean.</span></span> <span data-ttu-id="ffb0d-159">Например, *глубокая нейронная сеть — это нейронная сеть с определенным уровнем сложности и нейронной сетью с более чем двумя уровнями*.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-159">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="ffb0d-160">**Источник**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-160">**Source**.</span></span> <span data-ttu-id="ffb0d-161">URL-адрес страницы или веб-сайта, на который необходимо перейти, для получения дополнительных сведений об акрониме.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-161">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="ffb0d-162">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-162">**State**.</span></span> <span data-ttu-id="ffb0d-163">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="ffb0d-163">This field can take two values:</span></span>

- <span data-ttu-id="ffb0d-164">**Черновик**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-164">**Draft**.</span></span> <span data-ttu-id="ffb0d-165">Добавляет аббревиатуру в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-165">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="ffb0d-166">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-166">**Published**.</span></span> <span data-ttu-id="ffb0d-167">Добавляет акроним к опубликованному состоянию и делает его доступным в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-167">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="mined-acronyms"></a><span data-ttu-id="ffb0d-168">Аббревиатуры mined</span><span class="sxs-lookup"><span data-stu-id="ffb0d-168">Mined acronyms</span></span>
<span data-ttu-id="ffb0d-169">Администраторам может быть трудно добавить все аббревиатуры, используемые в Организации, для ответа.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-169">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="ffb0d-170">Эта функция может находить акронимы, которые даже не знают администраторам поиска.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-170">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="ffb0d-171">Для этого в Microsoft Search также не включены акронимы из этих источников:</span><span class="sxs-lookup"><span data-stu-id="ffb0d-171">To do that work, Microsoft Search also mines acronyms from these sources:</span></span>

- <span data-ttu-id="ffb0d-172">Сообщения электронной почты пользователей.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-172">Users’ emails.</span></span>
- <span data-ttu-id="ffb0d-173">Документы в [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/) и [Microsoft OneNote](http://www.onenote.com/).</span><span class="sxs-lookup"><span data-stu-id="ffb0d-173">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/) and [Microsoft OneNote](http://www.onenote.com/).</span></span>
- <span data-ttu-id="ffb0d-174">Общедоступные документы в Организации, к которым пользователи имеют доступ в SharePoint, OneDrive или OneNote.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-174">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote.</span></span>

<span data-ttu-id="ffb0d-175">Служба поиска Майкрософт гарантирует, что только те пользователи, у которых есть доступ и разрешения на доступ к документу, смогут видеть акронимы, mined от него.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-175">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are mined from it.</span></span> <span data-ttu-id="ffb0d-176">Аббревиатуры mined из папки "Входящие" пользователя и хранятся в сегментах пользователей.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-176">The acronyms are mined from a user’s inbox and stored in the user shard.</span></span> <span data-ttu-id="ffb0d-177">Только пользователь может получить доступ к акронимам mined из папки "Входящие" пользователя.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-177">Only the user can access the acronyms mined from the user’s own inbox.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb0d-178">Для акронимов mined не требуется настройка ИТ-администратора.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-178">No IT admin setup is needed for mined acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ffb0d-179">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="ffb0d-179">Frequently asked questions</span></span>
<span data-ttu-id="ffb0d-180">**Вопрос: как редакционные и mined-данные ранжированы?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-180">**Q: How is editorial and mined data ranked?**</span></span>

<span data-ttu-id="ffb0d-181">**A:** В настоящее время функция, в настоящее время, ранжирует акронимы над акронимами mined.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-181">**A:** The feature currently ranks editorial acronyms above mined acronyms.</span></span>

<span data-ttu-id="ffb0d-182">**В. Сколько времени займет отображение редакционных аббревиатур в Microsoft Search после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-182">**Q: How long does it take for editorial acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="ffb0d-183">**A:**  Аббревиатуры, добавленные к опубликованному состоянию, становятся доступны в Microsoft Search в течение трех дней.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-183">**A:**  It takes up  to three days for acronyms added to Published state to become available in Microsoft Search.</span></span> 

<span data-ttu-id="ffb0d-184">**Вопрос: как пользователи инициируют акронимы?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-184">**Q: How do users trigger Acronyms answers?**</span></span>

<span data-ttu-id="ffb0d-185">Ответ: чтобы получить акронимы **, пользователи**должны ввести определенные шаблоны запросов в поле поиска [Bing](https://bing.com), [Office 365](https://Office.com)или [SharePoint](https://products.office.com/sharepoint/collaboration) \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="ffb0d-185">**A**: To get Acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [Office 365](https://Office.com), or [SharePoint](https://products.office.com/sharepoint/collaboration) **Search** box.</span></span> <span data-ttu-id="ffb0d-186">Ниже приведены примеры запросов, в которых можно найти ответы на термин *днн* .</span><span class="sxs-lookup"><span data-stu-id="ffb0d-186">Examples of queries that find answers for the term *DNN* are as follows:</span></span>

- <span data-ttu-id="ffb0d-187">*Что такое* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-187">*What is* DNN</span></span>
- <span data-ttu-id="ffb0d-188">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-188">*Define* DNN</span></span>
- <span data-ttu-id="ffb0d-189">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-189">DNN *definition*</span></span>
- <span data-ttu-id="ffb0d-190">*Разверните узел* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-190">*Expand* DNN</span></span>
- <span data-ttu-id="ffb0d-191">*Расширение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-191">DNN *expansion*</span></span>
- <span data-ttu-id="ffb0d-192">*Значение* днн</span><span class="sxs-lookup"><span data-stu-id="ffb0d-192">*Meaning of* DNN</span></span>
- <span data-ttu-id="ffb0d-193">ДНН *означает*</span><span class="sxs-lookup"><span data-stu-id="ffb0d-193">DNN *means*</span></span>

<span data-ttu-id="ffb0d-194">**В. Сколько времени займет отображение аббревиатур mined после получения или отправки нового сообщения или документа?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-194">**Q: How long does it take for mined acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="ffb0d-195">**A:** Mined сокращения из нового сообщения электронной почты или документа составляют до семи дней, чтобы они отображались в результатах поиска Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-195">**A:** Mined acronyms from a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="ffb0d-196">**Вопрос: должны ли документы относиться к определенному формату для интеллектуального анализа данных?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-196">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="ffb0d-197">**A:** Нет.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-197">**A:** No.</span></span> <span data-ttu-id="ffb0d-198">Мы поддерживаем все типы файлов, за исключением изображений, папок и ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-198">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="ffb0d-199">**В.: будут акронимы из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-199">**Q: Will Microsoft mine acronyms from documents in all languages?**</span></span>

<span data-ttu-id="ffb0d-200">О **. Корпорация**Майкрософт поддерживает интеллектуальную анализ только из документов на английском языке.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-200">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="ffb0d-201">Поддержка других языков будет добавляться поэтапно.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-201">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="ffb0d-202">**Вопрос: что делать, если в Организации не требуется показывать акронимы mined? Можно ли остановить показ аббревиатур mined в результатах поиска?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-202">**Q: What if my organization doesn’t want to show mined acronyms? Can I stop showing mined acronyms in search results?**</span></span>

<span data-ttu-id="ffb0d-203">**А**: чтобы отключить отображение акронимов mined в результатах поиска, создайте билет поддержки клиентов, следуя инструкциям в статье [Поддержка для бизнеса](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span><span class="sxs-lookup"><span data-stu-id="ffb0d-203">**A**: To turn off showing mined acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span></span>
<span data-ttu-id="ffb0d-204">После создания билета в службу поддержки для аббревиатур mined в результатах поиска потребуется до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-204">After you create a support ticket, it takes up to 48 hours for mined acronyms to stop appearing in search results.</span></span> 

<span data-ttu-id="ffb0d-205">**В. когда я буду видеть акронимы ответы в [Office 365](https://Office.com) и [SharePoint Online](https://products.office.com/sharepoint/collaboration)?**</span><span class="sxs-lookup"><span data-stu-id="ffb0d-205">**Q: When will I see Acronyms answers in [Office 365](https://Office.com) and [SharePoint Online](https://products.office.com/sharepoint/collaboration)?**</span></span>

<span data-ttu-id="ffb0d-206">**A**: в настоящее время ответы на аббревиатуры доступны только в Microsoft Search в [Bing](https://bing.com).</span><span class="sxs-lookup"><span data-stu-id="ffb0d-206">**A**: Acronyms answers are currently only available in Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="ffb0d-207">Они будут сведены в Office 365 и SharePoint Online в 2020.</span><span class="sxs-lookup"><span data-stu-id="ffb0d-207">They’ll be rolled out to Office 365 and SharePoint Online in 2020.</span></span>
