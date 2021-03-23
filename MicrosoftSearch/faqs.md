---
title: Вопросы и ответы
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Получите ответы на часто задаваемые вопросы о поиске в корпоративной среде и Поиске (Майкрософт)
ms.openlocfilehash: 98128297047d50e2d418a8ed062066ab9e86749e
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031623"
---
<!-- markdownlint-disable no-trailing-punctuation -->
# <a name="frequently-asked-questions"></a><span data-ttu-id="f92e3-103">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="f92e3-103">Frequently asked questions</span></span>

<span data-ttu-id="f92e3-104">Ниже перечислены наиболее распространенные вопросы.</span><span class="sxs-lookup"><span data-stu-id="f92e3-104">Here's a list of the most common questions.</span></span>

> [!TIP]
> <span data-ttu-id="f92e3-105">Вашего вопроса здесь нет?</span><span class="sxs-lookup"><span data-stu-id="f92e3-105">Don't see your question answered here?</span></span> <span data-ttu-id="f92e3-106">Задайте свой вопрос в разделе отзывов этой статьи.</span><span class="sxs-lookup"><span data-stu-id="f92e3-106">Ask your question in this article's feedback.</span></span>

## <a name="is-advanced-query-understanding-supported"></a><span data-ttu-id="f92e3-107">Поддерживается ли расширенное понимание запросов?</span><span class="sxs-lookup"><span data-stu-id="f92e3-107">Is advanced query understanding supported?</span></span>

<span data-ttu-id="f92e3-108">Да, Microsoft Search разбирает намерения запроса из более крупных фраз.</span><span class="sxs-lookup"><span data-stu-id="f92e3-108">Yes, Microsoft Search parses query intent from larger phrases.</span></span> <span data-ttu-id="f92e3-109">Эта функция использует ИИ, чтобы узнать распространенные лишние фразы, которые пользователи добавляют в свои запросы, которые не влияют на их намерения поиска.</span><span class="sxs-lookup"><span data-stu-id="f92e3-109">This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent.</span></span> <span data-ttu-id="f92e3-110">Например, когда пользователь ищет дополнительные данные о том, как изменить *пароль,* мы извлекаем менее важные слова из запроса и запускаем на основе соответствующих паролей, таких как пароль *изменения.*</span><span class="sxs-lookup"><span data-stu-id="f92e3-110">For example, when a user searches for *tell me more about how to change my password*, we extract the less important words from the query and trigger based on the relevant ones like *change password*.</span></span>
  
<span data-ttu-id="f92e3-111">Эта функция не переопределяет ключевые слова, заданные в центре администрирования [Microsoft 365.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="f92e3-111">This feature won't override keywords set in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
  
## <a name="can-you-search-for-files-on-premises"></a><span data-ttu-id="f92e3-112">Можно ли искать локальные файлы?</span><span class="sxs-lookup"><span data-stu-id="f92e3-112">Can you search for files on-premises?</span></span>

<span data-ttu-id="f92e3-113">Да.</span><span class="sxs-lookup"><span data-stu-id="f92e3-113">Yes.</span></span> <span data-ttu-id="f92e3-114">Если у вас есть гибридное развертывание [SharePoint,](http://sharepoint.com/) можно искать локально файлы SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f92e3-114">You can search on-premises [SharePoint](http://sharepoint.com/) files if you have a hybrid deployment of SharePoint.</span></span>
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a><span data-ttu-id="f92e3-115">Как сделать Bing поисковой системой по умолчанию для пользователей в организации?</span><span class="sxs-lookup"><span data-stu-id="f92e3-115">How do I make Bing the default search engine for people in my org?</span></span>

<span data-ttu-id="f92e3-116">Вот инструкции по настройке поисковой системы по умолчанию, домашней страницы по умолчанию и браузера по умолчанию, чтобы предоставить пользователям лучший опыт работы с Microsoft Search в [Bing](https://Bing.com):</span><span class="sxs-lookup"><span data-stu-id="f92e3-116">Here's the instructions for setting the default search engine, default homepage, and default browser to give your users the best experience with Microsoft Search in [Bing](https://Bing.com):</span></span>

- [<span data-ttu-id="f92e3-117">Установите Microsoft Edge в качестве браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f92e3-117">Set Microsoft Edge as your default browser</span></span>](/deployedge/edge-default-browser)
- [<span data-ttu-id="f92e3-118">Установка Bing в качестве поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f92e3-118">Make Bing your default search engine</span></span>](set-default-search-engine.md)
- [<span data-ttu-id="f92e3-119">Настройка Bing.com в качестве корпоративной домашней страницы</span><span class="sxs-lookup"><span data-stu-id="f92e3-119">Set Bing.com as your enterprise homepage</span></span>](set-default-homepage.md)

## <a name="how-are-my-search-results-protected"></a><span data-ttu-id="f92e3-120">Как защищаются мои результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="f92e3-120">How are my search results protected?</span></span>

<span data-ttu-id="f92e3-121">Для доступа к результатам из надежного облака требуется проверка подлинности [Azure Active Directory.](/azure/active-directory/)</span><span class="sxs-lookup"><span data-stu-id="f92e3-121">We require [Azure Active Directory](/azure/active-directory/) authentication to access results from the Trusted Cloud.</span></span> <span data-ttu-id="f92e3-122">Пользователи, прошедшие проверку подлинности, видят в результатах поиска только тот контент, к которому у них есть доступ.</span><span class="sxs-lookup"><span data-stu-id="f92e3-122">Authenticated users only see content they have access to.</span></span> <span data-ttu-id="f92e3-123">Поисковые запросы деидентифицированы, а журналы отделены от общего поискового трафика [Bing](https://Bing.com) при использовании Microsoft Search в Bing.</span><span class="sxs-lookup"><span data-stu-id="f92e3-123">Search queries are de-identified, and logs are separated from public [Bing](https://Bing.com) search traffic when you use Microsoft Search in Bing.</span></span>

## <a name="can-i-search-across-federated-organizations"></a><span data-ttu-id="f92e3-124">Можно ли выполнять поиск в разных федеративных организациях?</span><span class="sxs-lookup"><span data-stu-id="f92e3-124">Can I search across federated organizations?</span></span>

<span data-ttu-id="f92e3-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="f92e3-125">No.</span></span>

## <a name="where-can-i-get-info-about-office-365-security-compliance-and-privacy"></a><span data-ttu-id="f92e3-126">Где можно получить сведения о безопасности, соответствии требованиям и конфиденциальности Office 365?</span><span class="sxs-lookup"><span data-stu-id="f92e3-126">Where can I get info about Office 365 security, compliance, and privacy?</span></span>

<span data-ttu-id="f92e3-127">Подробные сведения можно найти на страницах [Центра доверия для Office 365.](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx)</span><span class="sxs-lookup"><span data-stu-id="f92e3-127">Details can be found on the [Trust Center pages for Office 365](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx).</span></span>

## <a name="can-users-earn-microsoft-rewards-points-with-their-work-or-school-account"></a><span data-ttu-id="f92e3-128">Могут ли пользователи получать баллы Microsoft Rewards, используя рабочую или учебную учетную запись?</span><span class="sxs-lookup"><span data-stu-id="f92e3-128">Can users earn Microsoft Rewards points with their work or school account?</span></span>

<span data-ttu-id="f92e3-129">Для использования Поиска (Майкрософт) корпоративные пользователи должны выполнять вход с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f92e3-129">Microsoft Search requires that enterprise users sign in with a work or school account.</span></span> <span data-ttu-id="f92e3-130">Но пользователь не может присоединиться к программе Microsoft Rewards или войти в нее, используя эти учетные записи.</span><span class="sxs-lookup"><span data-stu-id="f92e3-130">But users can’t join or sign in to the Microsoft Rewards program with those accounts.</span></span> <span data-ttu-id="f92e3-131">Однако существует вариант, при котором корпоративный пользователь может наблюдать начисление баллов программы Rewards.</span><span class="sxs-lookup"><span data-stu-id="f92e3-131">However, there is an instance when an enterprise user may see Rewards points accrue.</span></span> <span data-ttu-id="f92e3-132">Это может происходить, если у пользователя Поиска (Майкрософт) есть учетная запись Rewards, созданная с помощью [учетной записи Майкрософт](https://www.microsoft.com/welcome?rtc=1).</span><span class="sxs-lookup"><span data-stu-id="f92e3-132">This can happen when a Microsoft Search user has a Rewards account that was created with a [Microsoft account](https://www.microsoft.com/welcome?rtc=1).</span></span> <span data-ttu-id="f92e3-133">(Для связи с учетной записью Майкрософт может применяться адрес электронной почты от Outlook.com, Hotmail.com, Gmail, Yahoo или других поставщиков.) Если пользователи попеременно входят в один сеанс браузера, используя рабочую учетную запись и учетную запись Майкрософт, они могут получать баллы для своей учетной записи Rewards.</span><span class="sxs-lookup"><span data-stu-id="f92e3-133">(The email address associated with a Microsoft account can be from Outlook.com, Hotmail.com, Gmail, Yahoo, or other providers.) If users sign in alternately with both their work account and Microsoft account in the same browser session, they might accrue points to their Rewards account.</span></span> <span data-ttu-id="f92e3-134">Пользователи могут прекратить начисление баллов при использовании Поиска (Майкрософт), очистив свои файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="f92e3-134">Users can stop accruing points while searching with Microsoft Search by clearing their cookies.</span></span>

## <a name="can-guest-users-leverage-microsoft-search-in-my-organization"></a><span data-ttu-id="f92e3-135">Могут ли гостевых пользователей использовать Microsoft Search в моей организации?</span><span class="sxs-lookup"><span data-stu-id="f92e3-135">Can guest users leverage Microsoft Search in my organization?</span></span>

<span data-ttu-id="f92e3-136">Microsoft 365 позволяет тесно сотрудничать с людьми за пределами организации с помощью [гостевого доступа.](/microsoft-365/solutions/collaborate-with-people-outside-your-organization)</span><span class="sxs-lookup"><span data-stu-id="f92e3-136">Microsoft 365 enables rich collaboration with people outside of your organization through [guest access.](/microsoft-365/solutions/collaborate-with-people-outside-your-organization)</span></span> <span data-ttu-id="f92e3-137">Эти пользователи смогут выполнять операции поиска по документам, сайтам, группам, спискам и библиотекам.</span><span class="sxs-lookup"><span data-stu-id="f92e3-137">These users will be able to perform search operations on documents, sites, groups, lists, and libraries.</span></span> <span data-ttu-id="f92e3-138">Однако гостевых пользователей не будет получать полный, персонализированный, Microsoft Search и может потребоваться использовать поле поиска на странице вместо единого окна Поиска Майкрософт в загоне.</span><span class="sxs-lookup"><span data-stu-id="f92e3-138">However, guest users will not get the full, personalized, Microsoft Search experience and may need to leverage the on-page search box instead of the unified Microsoft Search box in the header.</span></span>