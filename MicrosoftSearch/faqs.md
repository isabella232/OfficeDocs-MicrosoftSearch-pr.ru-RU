---
title: Вопросы и ответы
ms.author: anfowler
author: adefowler
manager: shohara
ms.date: 10/19/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NoIndex
description: Получите ответы на часто задаваемые вопросы о поиске в корпоративной среде и Поиске (Майкрософт)
ms.openlocfilehash: d3cf7e4a6f252711f94e90a4e6561c8f25769c27
ms.sourcegitcommit: 5204b3c85e2fc190a8807d5268fb87145624a969
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2019
ms.locfileid: "37502932"
---
# <a name="frequently-asked-questions"></a><span data-ttu-id="c2008-103">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="c2008-103">Frequently asked questions</span></span>

<span data-ttu-id="c2008-104">Ниже перечислены наиболее распространенные вопросы.</span><span class="sxs-lookup"><span data-stu-id="c2008-104">Here's a list of the most common questions.</span></span>

> [!TIP]
> <span data-ttu-id="c2008-105">Вашего вопроса здесь нет?</span><span class="sxs-lookup"><span data-stu-id="c2008-105">Don't see your question answered here?</span></span> <span data-ttu-id="c2008-106">Задайте свой вопрос в разделе отзывов этой статьи.</span><span class="sxs-lookup"><span data-stu-id="c2008-106">Ask your question in this article's feedback.</span></span>

## <a name="is-advanced-query-understanding-supported"></a><span data-ttu-id="c2008-107">Поддерживается ли расширенное понимание запросов?</span><span class="sxs-lookup"><span data-stu-id="c2008-107">Is advanced query understanding supported?</span></span>

<span data-ttu-id="c2008-p102">Да, Поиск (Майкрософт) выделяет цель запроса из больших фраз. Эта функция использует ИИ для изучения распространенных избыточных фраз, которые добавляются пользователями в запросы и не влияют на цель поиска. Например, когда пользователь выполняет поиск по запросу "дополнительные сведения о том, как изменить пароль", менее важные слова извлекаются из запроса, и вызов результата осуществляется с учетом релевантных слов, таких как "изменить пароль".</span><span class="sxs-lookup"><span data-stu-id="c2008-p102">Yes, Microsoft Search parses query intent from larger phrases. This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent. For example, when a user searches for 'tell me more about how to change my password please' we extract the less important words from the query and trigger based on the relevant ones like 'change password.'</span></span>
  
<span data-ttu-id="c2008-111">Эта функция не имеет приоритета над набором ключевых слов в Центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="c2008-111">This feature will not override keywords set in the Admin portal.</span></span>
  
## <a name="can-you-search-for-files-on-premises"></a><span data-ttu-id="c2008-112">Можно ли искать локальные файлы?</span><span class="sxs-lookup"><span data-stu-id="c2008-112">Can you search for files on-premises?</span></span>

<span data-ttu-id="c2008-113">Да.</span><span class="sxs-lookup"><span data-stu-id="c2008-113">Yes.</span></span> <span data-ttu-id="c2008-114">Вы можете искать локальные файлы SharePoint, если вы используете гибридное развертывание SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c2008-114">You can search on-premises SharePoint files if you have a hybrid deployment of SharePoint.</span></span>
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a><span data-ttu-id="c2008-115">Как сделать Bing поисковой системой по умолчанию для пользователей в организации?</span><span class="sxs-lookup"><span data-stu-id="c2008-115">How do I make Bing the default search engine for people in my org?</span></span>

<span data-ttu-id="c2008-116">Ниже приведены инструкции по настройке поисковой системы по умолчанию, домашней страницы по умолчанию и браузера по умолчанию, чтобы ваши пользователи могли оптимально использовать возможности Поиска (Майкрософт) в Bing:</span><span class="sxs-lookup"><span data-stu-id="c2008-116">Here's the instructions for setting the default search engine, default homepage, and default browser to give your users the best experience with Microsoft Search in Bing:</span></span>

- [<span data-ttu-id="c2008-117">Настройка Microsoft Edge в качестве браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c2008-117">Set Edge as your default browser</span></span>](set-default-browser.md)
- [<span data-ttu-id="c2008-118">Установка Bing в качестве поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c2008-118">Make Bing the default search engine</span></span>](set-default-search-engine.md)
- [<span data-ttu-id="c2008-119">Настройка Bing.com в качестве корпоративной домашней страницы</span><span class="sxs-lookup"><span data-stu-id="c2008-119">Set Bing.com as your enterprise homepage</span></span>](set-default-homepage.md)

  
## <a name="how-are-my-search-results-protected"></a><span data-ttu-id="c2008-120">Как защищаются мои результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="c2008-120">How are my search results protected?</span></span>

<span data-ttu-id="c2008-121">Мы требуем проверки подлинности Azure Active Directory (AAD) для доступа к результатам из надежной облачной среды.</span><span class="sxs-lookup"><span data-stu-id="c2008-121">We require Azure Active Directory (AAD) authentication to access results from the Trusted Cloud.</span></span> <span data-ttu-id="c2008-122">Пользователи, прошедшие проверку подлинности, видят в результатах поиска только тот контент, к которому у них есть доступ.</span><span class="sxs-lookup"><span data-stu-id="c2008-122">Users will only see content which they have access to.</span></span> <span data-ttu-id="c2008-123">Поисковые запросы обезличиваются, а журналы отделяются от общедоступного поискового трафика Bing.</span><span class="sxs-lookup"><span data-stu-id="c2008-123">Search queries are de-identified and logs are separated from public Bing search traffic.</span></span> <span data-ttu-id="c2008-124">Подобный уровень защиты нигде больше в отрасли не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="c2008-124">This level of protection is unavailable anywhere else in the industry.</span></span>

## <a name="can-i-search-across-federated-organizations"></a><span data-ttu-id="c2008-125">Можно ли выполнять поиск в разных федеративных организациях?</span><span class="sxs-lookup"><span data-stu-id="c2008-125">Can I search across federated organizations?</span></span>

<span data-ttu-id="c2008-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="c2008-126">No.</span></span>

## <a name="where-can-i-get-info-about-office-365-and-microsoft-365-compliance-tiers-and-categories"></a><span data-ttu-id="c2008-127">Где можно получить дополнительные сведения об уровнях и категориях соответствия требованиям в Office 365 и Microsoft 365?</span><span class="sxs-lookup"><span data-stu-id="c2008-127">Where can I get info about Office 365 and Microsoft 365 compliance tiers and categories?</span></span>

<span data-ttu-id="c2008-128">Подробные сведения можно найти в статье [Инфраструктура соответствия отраслевым стандартам и нормативным требованиям](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (скачать PDF).</span><span class="sxs-lookup"><span data-stu-id="c2008-128">Details can be found in the [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (PDF download).</span></span>

## <a name="can-users-earn-microsoft-rewards-points-with-their-work-or-school-account"></a><span data-ttu-id="c2008-129">Могут ли пользователи получать баллы Microsoft Rewards, используя рабочую или учебную учетную запись?</span><span class="sxs-lookup"><span data-stu-id="c2008-129">Can users earn Microsoft Rewards points with their work or school account?</span></span>

<span data-ttu-id="c2008-130">Для использования Поиска (Майкрософт) корпоративные пользователи должны выполнять вход с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c2008-130">Microsoft Search requires that enterprise users sign in with a work or school account.</span></span> <span data-ttu-id="c2008-131">Но пользователь не может присоединиться к программе Microsoft Rewards или войти в нее, используя эти учетные записи.</span><span class="sxs-lookup"><span data-stu-id="c2008-131">But users can’t join or sign in to the Microsoft Rewards program with those accounts.</span></span> <span data-ttu-id="c2008-132">Однако существует вариант, при котором корпоративный пользователь может наблюдать начисление баллов программы Rewards.</span><span class="sxs-lookup"><span data-stu-id="c2008-132">However, there is an instance when an enterprise user may see Rewards points accrue.</span></span> <span data-ttu-id="c2008-133">Это может происходить, если у пользователя Поиска (Майкрософт) есть учетная запись Rewards, созданная с помощью <a href="https://www.microsoft.com/en-us/welcome?rtc=1">учетной записи Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="c2008-133">This can happen when a Microsoft Search user has a Rewards account that was created with a <a href="https://www.microsoft.com/en-us/welcome?rtc=1">Microsoft account</a>.</span></span> <span data-ttu-id="c2008-134">(Для связи с учетной записью Майкрософт может применяться адрес электронной почты от Outlook.com, Hotmail.com, Gmail, Yahoo или других поставщиков.) Если пользователи попеременно входят в один сеанс браузера, используя рабочую учетную запись и учетную запись Майкрософт, они могут получать баллы для своей учетной записи Rewards.</span><span class="sxs-lookup"><span data-stu-id="c2008-134">(The email address associated with a Microsoft account can be from Outlook.com, Hotmail.com, Gmail, Yahoo, or other providers.) If users sign in alternately with both their work account and Microsoft account in the same browser session, they might accrue points to their Rewards account.</span></span> <span data-ttu-id="c2008-135">Пользователи могут прекратить начисление баллов при использовании Поиска (Майкрософт), очистив свои файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="c2008-135">Users can stop accruing points while searching with Microsoft Search by clearing their cookies.</span></span> 

