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
ms.openlocfilehash: c4b0d888e7765cf965832c252a79bdcf8aa5f6cf
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "47422967"
---
<!-- markdownlint-disable no-trailing-punctuation -->
# <a name="frequently-asked-questions"></a><span data-ttu-id="b2cc7-103">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="b2cc7-103">Frequently asked questions</span></span>

<span data-ttu-id="b2cc7-104">Ниже перечислены наиболее распространенные вопросы.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-104">Here's a list of the most common questions.</span></span>

> [!TIP]
> <span data-ttu-id="b2cc7-105">Вашего вопроса здесь нет?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-105">Don't see your question answered here?</span></span> <span data-ttu-id="b2cc7-106">Задайте свой вопрос в разделе отзывов этой статьи.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-106">Ask your question in this article's feedback.</span></span>

## <a name="is-advanced-query-understanding-supported"></a><span data-ttu-id="b2cc7-107">Поддерживается ли расширенное понимание запросов?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-107">Is advanced query understanding supported?</span></span>

<span data-ttu-id="b2cc7-p102">Да, Microsoft Search анализирует цель запроса из больших фраз. Эта функция использует AI для изучения распространенных избыточных фраз, которые добавляются к своим запросам, не влияющим на цель поиска. Например, когда пользователь *покажет дополнительные сведения о том, как изменить пароль*, мы извлекаем менее важных слов из запроса и триггера, основываясь на соответствующих параметрах, таких как " *изменить пароль*".</span><span class="sxs-lookup"><span data-stu-id="b2cc7-p102">Yes, Microsoft Search parses query intent from larger phrases. This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent. For example, when a user searches for *tell me more about how to change my password please*, we extract the less important words from the query and trigger based on the relevant ones like *change password*.</span></span>
  
<span data-ttu-id="b2cc7-111">Эта функция не переопределяет ключевые слова в [центре администрирования Microsoft 365](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b2cc7-111">This feature won't override keywords set in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
  
## <a name="can-you-search-for-files-on-premises"></a><span data-ttu-id="b2cc7-112">Можно ли искать локальные файлы?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-112">Can you search for files on-premises?</span></span>

<span data-ttu-id="b2cc7-113">Да.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-113">Yes.</span></span> <span data-ttu-id="b2cc7-114">Вы можете выполнять поиск в локальных файлах [SharePoint](http://sharepoint.com/) , если у вас есть гибридное развертывание SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-114">You can search on-premises [SharePoint](http://sharepoint.com/) files if you have a hybrid deployment of SharePoint.</span></span>
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a><span data-ttu-id="b2cc7-115">Как сделать Bing поисковой системой по умолчанию для пользователей в организации?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-115">How do I make Bing the default search engine for people in my org?</span></span>

<span data-ttu-id="b2cc7-116">Ниже приведены инструкции по настройке поисковой системы по умолчанию, домашней страницы по умолчанию и браузера по умолчанию для предоставления пользователям лучшего взаимодействия с Microsoft Search в [Bing](https://Bing.com):</span><span class="sxs-lookup"><span data-stu-id="b2cc7-116">Here's the instructions for setting the default search engine, default homepage, and default browser to give your users the best experience with Microsoft Search in [Bing](https://Bing.com):</span></span>

- [<span data-ttu-id="b2cc7-117">Установка Microsoft EDGE в качестве браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b2cc7-117">Set Microsoft Edge as your default browser</span></span>](set-default-browser.md)
- [<span data-ttu-id="b2cc7-118">Установка Bing в качестве поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b2cc7-118">Make Bing your default search engine</span></span>](set-default-search-engine.md)
- [<span data-ttu-id="b2cc7-119">Настройка Bing.com в качестве корпоративной домашней страницы</span><span class="sxs-lookup"><span data-stu-id="b2cc7-119">Set Bing.com as your enterprise homepage</span></span>](set-default-homepage.md)

## <a name="how-are-my-search-results-protected"></a><span data-ttu-id="b2cc7-120">Как защищаются мои результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-120">How are my search results protected?</span></span>

<span data-ttu-id="b2cc7-121">Для доступа к результатам из надежного облака требуется проверка подлинности [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) .</span><span class="sxs-lookup"><span data-stu-id="b2cc7-121">We require [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) authentication to access results from the Trusted Cloud.</span></span> <span data-ttu-id="b2cc7-122">Пользователи, прошедшие проверку подлинности, видят в результатах поиска только тот контент, к которому у них есть доступ.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-122">Authenticated users only see content they have access to.</span></span> <span data-ttu-id="b2cc7-123">Поисковые запросы не определены, а журналы отделены от общедоступного трафика поиска [Bing](https://Bing.com) .</span><span class="sxs-lookup"><span data-stu-id="b2cc7-123">Search queries are de-identified, and logs are separated from public [Bing](https://Bing.com) search traffic.</span></span> <span data-ttu-id="b2cc7-124">Подобный уровень защиты нигде больше в отрасли не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-124">This level of protection is unavailable anywhere else in the industry.</span></span>

## <a name="can-i-search-across-federated-organizations"></a><span data-ttu-id="b2cc7-125">Можно ли выполнять поиск в разных федеративных организациях?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-125">Can I search across federated organizations?</span></span>

<span data-ttu-id="b2cc7-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-126">No.</span></span>

## <a name="where-can-i-get-info-about-office-365-security-compliance-and-privacy"></a><span data-ttu-id="b2cc7-127">Где можно получить сведения о безопасности, соответствии требованиям и конфиденциальности Office 365?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-127">Where can I get info about Office 365 security, compliance, and privacy?</span></span>

<span data-ttu-id="b2cc7-128">Подробные сведения можно найти на [страницах центра управления безопасностью для Office 365](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="b2cc7-128">Details can be found on the [Trust Center pages for Office 365](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx).</span></span>

## <a name="can-users-earn-microsoft-rewards-points-with-their-work-or-school-account"></a><span data-ttu-id="b2cc7-129">Могут ли пользователи получать баллы Microsoft Rewards, используя рабочую или учебную учетную запись?</span><span class="sxs-lookup"><span data-stu-id="b2cc7-129">Can users earn Microsoft Rewards points with their work or school account?</span></span>

<span data-ttu-id="b2cc7-130">Для использования Поиска (Майкрософт) корпоративные пользователи должны выполнять вход с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-130">Microsoft Search requires that enterprise users sign in with a work or school account.</span></span> <span data-ttu-id="b2cc7-131">Но пользователь не может присоединиться к программе Microsoft Rewards или войти в нее, используя эти учетные записи.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-131">But users can’t join or sign in to the Microsoft Rewards program with those accounts.</span></span> <span data-ttu-id="b2cc7-132">Однако существует вариант, при котором корпоративный пользователь может наблюдать начисление баллов программы Rewards.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-132">However, there is an instance when an enterprise user may see Rewards points accrue.</span></span> <span data-ttu-id="b2cc7-133">Это может происходить, если у пользователя Поиска (Майкрософт) есть учетная запись Rewards, созданная с помощью [учетной записи Майкрософт](https://www.microsoft.com/welcome?rtc=1).</span><span class="sxs-lookup"><span data-stu-id="b2cc7-133">This can happen when a Microsoft Search user has a Rewards account that was created with a [Microsoft account](https://www.microsoft.com/welcome?rtc=1).</span></span> <span data-ttu-id="b2cc7-134">(Для связи с учетной записью Майкрософт может применяться адрес электронной почты от Outlook.com, Hotmail.com, Gmail, Yahoo или других поставщиков.) Если пользователи попеременно входят в один сеанс браузера, используя рабочую учетную запись и учетную запись Майкрософт, они могут получать баллы для своей учетной записи Rewards.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-134">(The email address associated with a Microsoft account can be from Outlook.com, Hotmail.com, Gmail, Yahoo, or other providers.) If users sign in alternately with both their work account and Microsoft account in the same browser session, they might accrue points to their Rewards account.</span></span> <span data-ttu-id="b2cc7-135">Пользователи могут прекратить начисление баллов при использовании Поиска (Майкрософт), очистив свои файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="b2cc7-135">Users can stop accruing points while searching with Microsoft Search by clearing their cookies.</span></span>
