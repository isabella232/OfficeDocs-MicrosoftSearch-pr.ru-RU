---
title: Управление сокращениями ответов в Microsoft Search
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
description: Создание и обновление аббревиатур ответов в Microsoft Search
ms.openlocfilehash: 68e62884898e3aa081fc32438ad9a80068092738
ms.sourcegitcommit: b3738f5ab02bfba9dedf099e035f3850607be480
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/07/2020
ms.locfileid: "46591511"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="548a1-103">Управление сокращениями ответов в Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="548a1-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="548a1-104">Пользователи часто работают в незнакомых акронимах и сокращениях, используемых в организации или группе.</span><span class="sxs-lookup"><span data-stu-id="548a1-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="548a1-105">Термины, относящиеся к организациям или командам, могут быть новыми для людей, которые переходят из одной команды в другую, работают с внутренними участниками группы или являются новыми для Организации.</span><span class="sxs-lookup"><span data-stu-id="548a1-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="548a1-106">Организации не всегда имеют одну ссылку для стандартных терминов.</span><span class="sxs-lookup"><span data-stu-id="548a1-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="548a1-107">Отсутствие одной ссылки затрудняет поиск определений или расширений для этих аббревиатур.</span><span class="sxs-lookup"><span data-stu-id="548a1-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="548a1-108">Служба поиска Майкрософт решает эту проблему с акронимами.</span><span class="sxs-lookup"><span data-stu-id="548a1-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="548a1-109">Взаимодействие с пользователями</span><span class="sxs-lookup"><span data-stu-id="548a1-109">What users experience</span></span>

<span data-ttu-id="548a1-110">Пользователи службы поиска Майкрософт могут получать определения с акронимами в [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration)и [Office 365](https://Office.com).</span><span class="sxs-lookup"><span data-stu-id="548a1-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="548a1-111">В поле **поиска** пользователи вводят запросы, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="548a1-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="548a1-112">*Что такое* днн</span><span class="sxs-lookup"><span data-stu-id="548a1-112">*What is* DNN</span></span>
- <span data-ttu-id="548a1-113">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="548a1-113">*Define* DNN</span></span>
- <span data-ttu-id="548a1-114">*Определение* днн</span><span class="sxs-lookup"><span data-stu-id="548a1-114">DNN *definition*</span></span>
- <span data-ttu-id="548a1-115">*Разверните узел* днн</span><span class="sxs-lookup"><span data-stu-id="548a1-115">*Expand* DNN</span></span>
- <span data-ttu-id="548a1-116">*Расширение* днн</span><span class="sxs-lookup"><span data-stu-id="548a1-116">DNN *expansion*</span></span>
- <span data-ttu-id="548a1-117">*Значение* днн</span><span class="sxs-lookup"><span data-stu-id="548a1-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="548a1-118">ДНН *означает*</span><span class="sxs-lookup"><span data-stu-id="548a1-118">DNN *means*</span></span>

<span data-ttu-id="548a1-119">Результат включает все значения ДНН, присутствующие в организации пользователя.</span><span class="sxs-lookup"><span data-stu-id="548a1-119">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="548a1-120">Пользователи должны ввести запрос, включающий указанные *Ключевые слова* аббревиатуры, чтобы активировать соответствующие ответы.</span><span class="sxs-lookup"><span data-stu-id="548a1-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="548a1-121">В запросах акронимов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="548a1-121">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="548a1-122">Настройка аббревиатур ответов</span><span class="sxs-lookup"><span data-stu-id="548a1-122">Set up Acronyms answers</span></span>

<span data-ttu-id="548a1-123">В [центре администрирования](https://admin.microsoft.com)Microsoft 365 перейдите к разделу **Параметры**  >  **Microsoft Search**  >  **Answers**  >  [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), а затем нажмите кнопку **Добавить акронимы**.</span><span class="sxs-lookup"><span data-stu-id="548a1-123">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Settings** > **Microsoft Search** > **Answers** > [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronyms**.</span></span>

<span data-ttu-id="548a1-124">Служба поиска Microsoft выполняет запрос двух источников данных для сокращения ответов на запросы пользователей.</span><span class="sxs-lookup"><span data-stu-id="548a1-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="548a1-125">**Редакционные акронимы**.</span><span class="sxs-lookup"><span data-stu-id="548a1-125">**Editorial acronyms**.</span></span> <span data-ttu-id="548a1-126">Предоставляется ИТ администраторами в [центре администрирования](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span><span class="sxs-lookup"><span data-stu-id="548a1-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="548a1-127">**Аббревиатуры mined**.</span><span class="sxs-lookup"><span data-stu-id="548a1-127">**Mined acronyms**.</span></span> <span data-ttu-id="548a1-128">Mined Microsoft Search из личной электронной почты и документов пользователя и общедоступных данных в Организации.</span><span class="sxs-lookup"><span data-stu-id="548a1-128">Mined by Microsoft Search from the user’s personal email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-editorial-acronyms"></a><span data-ttu-id="548a1-129">Настройка редакционных аббревиатур</span><span class="sxs-lookup"><span data-stu-id="548a1-129">Set up editorial acronyms</span></span>

<span data-ttu-id="548a1-130">Администраторы поиска могут настроить редакционные сокращения на [вкладке сокращения](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) в [центре администрирования поиска Майкрософт](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span><span class="sxs-lookup"><span data-stu-id="548a1-130">Search administrators can set up editorial acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="548a1-131">Вы можете добавлять акронимы из любого внутреннего сайта или репозитория в центр администрирования.</span><span class="sxs-lookup"><span data-stu-id="548a1-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="548a1-132">Редакционные сокращения можно добавлять в состояние **опубликованных** или **черновиков** :</span><span class="sxs-lookup"><span data-stu-id="548a1-132">Editorial acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="548a1-133">**Опубликованное состояние**.</span><span class="sxs-lookup"><span data-stu-id="548a1-133">**Published state**.</span></span> <span data-ttu-id="548a1-134">Аббревиатуры доступны для сотрудников Организации в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="548a1-134">Acronyms are available to the organization’s employees through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="548a1-135">Аббревиатуры, добавленные в опубликованное состояние для получения в Microsoft поиске, могут быть доступны в течение трех дней.</span><span class="sxs-lookup"><span data-stu-id="548a1-135">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="548a1-136">**Состояние черновика**.</span><span class="sxs-lookup"><span data-stu-id="548a1-136">**Draft state**.</span></span> <span data-ttu-id="548a1-137">Если администраторы хотят просмотреть акронимы, прежде чем сделать их доступными в Microsoft Search, они могут добавить аббревиатуры в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="548a1-137">If admins want to review Acronyms answers before making them available in Microsoft Search, they can add the acronyms to Draft state.</span></span> <span data-ttu-id="548a1-138">Аббревиатуры, добавленные в состояние черновика, не поддерживаются в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="548a1-138">Acronyms added to Draft state aren’t available in Microsoft Search.</span></span> <span data-ttu-id="548a1-139">Администраторы должны добавить аббревиатуры в опубликованное состояние, чтобы сделать их доступными.</span><span class="sxs-lookup"><span data-stu-id="548a1-139">Admins need to add the acronyms to Published state to make them available.</span></span>

<span data-ttu-id="548a1-140">Администраторы могут добавлять акронимы по отдельности или массово импортировать их в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="548a1-140">Admins can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="548a1-141">Отправьте CSV-файл с полями, приведенными в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="548a1-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="548a1-142">Аббревиатура (обязательно)</span><span class="sxs-lookup"><span data-stu-id="548a1-142">Acronym (mandatory)</span></span> | <span data-ttu-id="548a1-143">Расширение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="548a1-143">Expansion (mandatory)</span></span> | <span data-ttu-id="548a1-144">Описание</span><span class="sxs-lookup"><span data-stu-id="548a1-144">Description</span></span>  | <span data-ttu-id="548a1-145">Источник</span><span class="sxs-lookup"><span data-stu-id="548a1-145">Source</span></span> | <span data-ttu-id="548a1-146">State (обязательно)</span><span class="sxs-lookup"><span data-stu-id="548a1-146">State (mandatory)</span></span> |
| --------- | --------- | ---------- | --------- |--------- |
| <span data-ttu-id="548a1-147">*XXX*</span><span class="sxs-lookup"><span data-stu-id="548a1-147">*XXX*</span></span> | <span data-ttu-id="548a1-148">*Сокращенное сокращение*</span><span class="sxs-lookup"><span data-stu-id="548a1-148">*Spelled out abbreviation*</span></span> |  | <span data-ttu-id="548a1-149">*URL-адрес*</span><span class="sxs-lookup"><span data-stu-id="548a1-149">*URL*</span></span> | <span data-ttu-id="548a1-150">*Опубликовано или черновик*</span><span class="sxs-lookup"><span data-stu-id="548a1-150">*Published or Draft*</span></span> |

### <a name="csv-fields"></a><span data-ttu-id="548a1-151">Поля CSV</span><span class="sxs-lookup"><span data-stu-id="548a1-151">CSV fields</span></span>

<span data-ttu-id="548a1-152">**Акроним**.</span><span class="sxs-lookup"><span data-stu-id="548a1-152">**Acronym**.</span></span> <span data-ttu-id="548a1-153">Содержит собственно краткую форму или аббревиатуру.</span><span class="sxs-lookup"><span data-stu-id="548a1-153">Contains the actual short form or acronym.</span></span> <span data-ttu-id="548a1-154">Пример: *днн*.</span><span class="sxs-lookup"><span data-stu-id="548a1-154">An example is *DNN*.</span></span>

<span data-ttu-id="548a1-155">**Расширение**.</span><span class="sxs-lookup"><span data-stu-id="548a1-155">**Expansion**.</span></span> <span data-ttu-id="548a1-156">Содержит расширение аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="548a1-156">Contains the expansion of the acronym.</span></span> <span data-ttu-id="548a1-157">Примером является *глубокая нейронная сеть*.</span><span class="sxs-lookup"><span data-stu-id="548a1-157">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="548a1-158">**Description**.</span><span class="sxs-lookup"><span data-stu-id="548a1-158">**Description**.</span></span> <span data-ttu-id="548a1-159">Краткое описание аббревиатуры, предоставляющее пользователям дополнительные сведения об акрониме и его расширении.</span><span class="sxs-lookup"><span data-stu-id="548a1-159">A brief description of the acronym that gives users more info about the acronym and its expansion.</span></span> <span data-ttu-id="548a1-160">Например, *глубокая нейронная сеть — это нейронная сеть с определенным уровнем сложности и нейронной сетью с более чем двумя уровнями*.</span><span class="sxs-lookup"><span data-stu-id="548a1-160">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="548a1-161">**Источник**.</span><span class="sxs-lookup"><span data-stu-id="548a1-161">**Source**.</span></span> <span data-ttu-id="548a1-162">URL-адрес страницы или веб-сайта, на который необходимо перейти, для получения дополнительных сведений об акрониме.</span><span class="sxs-lookup"><span data-stu-id="548a1-162">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="548a1-163">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="548a1-163">**State**.</span></span> <span data-ttu-id="548a1-164">Это поле может принимать два значения:</span><span class="sxs-lookup"><span data-stu-id="548a1-164">This field can take two values:</span></span>

- <span data-ttu-id="548a1-165">**Черновик**.</span><span class="sxs-lookup"><span data-stu-id="548a1-165">**Draft**.</span></span> <span data-ttu-id="548a1-166">Добавляет аббревиатуру в состояние черновика.</span><span class="sxs-lookup"><span data-stu-id="548a1-166">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="548a1-167">**Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="548a1-167">**Published**.</span></span> <span data-ttu-id="548a1-168">Добавляет акроним к опубликованному состоянию и делает его доступным в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="548a1-168">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="mined-acronyms"></a><span data-ttu-id="548a1-169">Аббревиатуры mined</span><span class="sxs-lookup"><span data-stu-id="548a1-169">Mined acronyms</span></span>

<span data-ttu-id="548a1-170">Администраторам может быть трудно добавить все аббревиатуры, используемые в Организации, для ответа.</span><span class="sxs-lookup"><span data-stu-id="548a1-170">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="548a1-171">Эта функция может находить акронимы, которые даже не знают администраторам поиска.</span><span class="sxs-lookup"><span data-stu-id="548a1-171">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="548a1-172">Для этого в Microsoft Search также не включены акронимы из этих источников:</span><span class="sxs-lookup"><span data-stu-id="548a1-172">To do that work, Microsoft Search also mines acronyms from these sources:</span></span>

- <span data-ttu-id="548a1-173">Сообщения электронной почты пользователей.</span><span class="sxs-lookup"><span data-stu-id="548a1-173">Users’ emails.</span></span>
- <span data-ttu-id="548a1-174">Документы в [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/)и [Microsoft OneNote](https://www.onenote.com/).</span><span class="sxs-lookup"><span data-stu-id="548a1-174">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/).</span></span>
- <span data-ttu-id="548a1-175">Общедоступные документы в Организации, к которым пользователи имеют доступ в SharePoint, OneDrive или OneNote.</span><span class="sxs-lookup"><span data-stu-id="548a1-175">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote.</span></span>

<span data-ttu-id="548a1-176">Служба поиска Майкрософт гарантирует, что только те пользователи, у которых есть доступ и разрешения на доступ к документу, смогут видеть акронимы, mined от него.</span><span class="sxs-lookup"><span data-stu-id="548a1-176">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are mined from it.</span></span> <span data-ttu-id="548a1-177">Если аббревиатура mined из почтового ящика пользователя, она может быть видна только этому пользователю.</span><span class="sxs-lookup"><span data-stu-id="548a1-177">When an acronym is mined from a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="548a1-178">Для аббревиатур mined не требуется установка.</span><span class="sxs-lookup"><span data-stu-id="548a1-178">No setup is needed for mined acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="548a1-179">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="548a1-179">Frequently asked questions</span></span>

<span data-ttu-id="548a1-180">**Вопрос: как редакционные и mined-данные ранжированы?**</span><span class="sxs-lookup"><span data-stu-id="548a1-180">**Q: How is editorial and mined data ranked?**</span></span>

<span data-ttu-id="548a1-181">**A:** В настоящее время функция, в настоящее время, ранжирует акронимы над акронимами mined.</span><span class="sxs-lookup"><span data-stu-id="548a1-181">**A:** The feature currently ranks editorial acronyms above mined acronyms.</span></span>

<span data-ttu-id="548a1-182">**В. Сколько времени займет отображение редакционных аббревиатур в Microsoft Search после их публикации?**</span><span class="sxs-lookup"><span data-stu-id="548a1-182">**Q: How long does it take for editorial acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="548a1-183">**A:**  Аббревиатуры, добавленные к опубликованному состоянию, становятся доступны в Microsoft Search в течение трех дней.</span><span class="sxs-lookup"><span data-stu-id="548a1-183">**A:**  It takes up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="548a1-184">**Вопрос: как пользователи инициируют акронимы?**</span><span class="sxs-lookup"><span data-stu-id="548a1-184">**Q: How do users trigger Acronyms answers?**</span></span>

<span data-ttu-id="548a1-185">Ответ: чтобы получить акронимы **, пользователи**должны ввести определенные шаблоны запросов в поле поиска [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration)или [Office 365](https://Office.com) **Search** .</span><span class="sxs-lookup"><span data-stu-id="548a1-185">**A**: To get Acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="548a1-186">**В. Сколько времени займет отображение аббревиатур mined после получения или отправки нового сообщения или документа?**</span><span class="sxs-lookup"><span data-stu-id="548a1-186">**Q: How long does it take for mined acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="548a1-187">**A:** Mined сокращения из нового сообщения электронной почты или документа составляют до семи дней, чтобы они отображались в результатах поиска Microsoft.</span><span class="sxs-lookup"><span data-stu-id="548a1-187">**A:** Mined acronyms from a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="548a1-188">**Вопрос: должны ли документы относиться к определенному формату для интеллектуального анализа данных?**</span><span class="sxs-lookup"><span data-stu-id="548a1-188">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="548a1-189">**A:** Нет.</span><span class="sxs-lookup"><span data-stu-id="548a1-189">**A:** No.</span></span> <span data-ttu-id="548a1-190">Мы поддерживаем все типы файлов, за исключением изображений, папок и ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="548a1-190">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="548a1-191">**В.: будут акронимы из документов на всех языках?**</span><span class="sxs-lookup"><span data-stu-id="548a1-191">**Q: Will Microsoft mine acronyms from documents in all languages?**</span></span>

<span data-ttu-id="548a1-192">О **. Корпорация**Майкрософт поддерживает интеллектуальную анализ только из документов на английском языке.</span><span class="sxs-lookup"><span data-stu-id="548a1-192">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="548a1-193">Поддержка других языков будет добавляться поэтапно.</span><span class="sxs-lookup"><span data-stu-id="548a1-193">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="548a1-194">**Вопрос: что делать, если в Организации не требуется показывать акронимы mined? Можно ли остановить показ аббревиатур mined в результатах поиска?**</span><span class="sxs-lookup"><span data-stu-id="548a1-194">**Q: What if my organization doesn’t want to show mined acronyms? Can I stop showing mined acronyms in search results?**</span></span>

<span data-ttu-id="548a1-195">**А**: чтобы отключить отображение акронимов mined в результатах поиска, создайте билет поддержки клиентов, следуя инструкциям в статье [Поддержка для бизнеса](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span><span class="sxs-lookup"><span data-stu-id="548a1-195">**A**: To turn off showing mined acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span></span>
<span data-ttu-id="548a1-196">После создания билета в службу поддержки для аббревиатур mined в результатах поиска потребуется до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="548a1-196">After you create a support ticket, it takes up to 48 hours for mined acronyms to stop appearing in search results.</span></span>
