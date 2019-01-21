---
title: Безопасность для Microsoft Search
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 9/12/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 50461cb9-8707-46c1-935a-1b9608a98800
description: Защита корпоративных данных и пользователей одновременно поддерживая сведения у авторизованных пользователей, с помощью Microsoft Search
ms.openlocfilehash: 65cf1d49e32edbb8061a06f8da7ba644c2145e24
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "29379158"
---
# <a name="security-for-microsoft-search"></a><span data-ttu-id="6a8a4-103">Безопасность для Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="6a8a4-103">Security for Microsoft Search</span></span>

<span data-ttu-id="6a8a4-104">Система безопасности уровня предприятия Microsoft Search всегда отслеживает пользователей и данные, защищенные.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-104">With enterprise-grade security, Microsoft Search always keeps your users and data protected.</span></span>
  
## <a name="secure-by-default"></a><span data-ttu-id="6a8a4-105">Безопасность по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6a8a4-105">Secure by default</span></span>

<span data-ttu-id="6a8a4-p101">Microsoft Search всегда гарантирует, что запросы выполняются по протоколу HTTPS. В этом защищают гарантирует, что подключение является зашифрованные сквозного для повышения безопасности.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p101">Microsoft Search always ensures requests are made over HTTPS. This safeguard ensures the connection is encrypted end-to-end for enhanced security.</span></span>
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a><span data-ttu-id="6a8a4-108">Проверка подлинности и авторизация с Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6a8a4-108">Authentication and authorization with Azure Active Directory</span></span>

<span data-ttu-id="6a8a4-p102">Проверка подлинности для поиска Microsoft связана с Azure Active Directory. При пользователи Microsoft Search перейти Bing, заголовок будет отображение параметров входа в учетную запись Майкрософт как Bing, а рабочий также или школы учетной записи. Если Bing не может определить, является ли пользователь подходящими участника, пользователи могут перейти на страницу [Изучение Microsoft Search](https://www.bing.com/business/explore) которой они будут автоматически перенаправляться на странице входа вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p102">Authentication for Microsoft Search is tied to Azure Active Directory. When Microsoft Search users go to Bing, the Bing header will show sign-in options for a Microsoft account as well as a work or school account. If Bing can't determine whether a user is an eligible participant, users can go to the [Explore Microsoft Search](https://www.bing.com/business/explore) page, where they'll be automatically redirected to your organization's sign-in page.</span></span> 
  
<span data-ttu-id="6a8a4-p103">Пользователей можно получить доступ к Microsoft Search только с помощью учетной записи рабочего или школы. Они должны выполнить вход с один набор учетных данных, которые они используют для доступа к службам Office 365, например, SharePoint или Outlook. Личная учетная запись Майкрософт не может использоваться для входа в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p103">Users can access Microsoft Search only through a work or school account. They need to sign in with the same credentials they use to access Office 365 services such as SharePoint or Outlook. A personal Microsoft account can't be used to sign in to Microsoft Search.</span></span>
  
<span data-ttu-id="6a8a4-115">Пользователи не могут входить в систему Bing с помощью учетной записи Майкрософт и работы или школы учетной записи в то же время.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-115">Users can't be signed in to Bing with both a Microsoft account and a work or school account at the same time.</span></span>
  
## <a name="single-sign-on"></a><span data-ttu-id="6a8a4-116">Единый вход</span><span class="sxs-lookup"><span data-stu-id="6a8a4-116">Single sign-on</span></span>

<span data-ttu-id="6a8a4-p104">Если пользователь прошли проверку подлинности с помощью своей учетной записи рабочего или школы в другой службы, такие как Outlook и SharePoint, они будут быть автоматически входить в систему Microsoft Search при попытке Bing в одном браузера. Кроме того при входе пользователя из Microsoft Search, они будут автоматически осуществлен от других служб браузера.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p104">If a user is already authenticated with their work or school account in another service, such as Outlook or SharePoint, they'll be automatically signed in to Microsoft Search when they go to Bing in the same browser. Also, when the user signs out of Microsoft Search, they'll be automatically signed out from other services in the same browser.</span></span>
  
## <a name="communicates-with-the-trusted-cloud-from-the-browser"></a><span data-ttu-id="6a8a4-119">Взаимодействует с облаком надежных в браузере</span><span class="sxs-lookup"><span data-stu-id="6a8a4-119">Communicates with the Trusted Cloud from the browser</span></span>

<span data-ttu-id="6a8a4-p105">При пользователь подписывает своей работе или учетная запись школа, Bing будет загрузить необходимые клиентские библиотеки в браузере, чтобы включить результаты поиска Microsoft. Затем при выполнении поиска в браузере вызывается облаке Office 365 для получения результатов рабочих. Для этого Microsoft Search использует выделенный API-Интерфейс, который является C уровня (1 типа SOC2) спецификации этих Office 365 [Framework соответствия требованиям для действие экспортного отраслевых стандартов](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (ФАЙЛ для загрузки). Это означает, что результаты работы и рабочих данных никогда не проходят через Bing системы.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p105">When a user signs in with their work or school account, Bing will download the necessary client libraries to the browser to enable Microsoft Search results. Then, when they search, the in-browser code calls the Office 365 cloud to get work results. To do this, Microsoft Search uses a dedicated API that is Tier C (SOC2 Type 1) compliant pursuant to the Office 365 [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (PDF download). This means work results and work data never flow through non-compliant Bing systems.</span></span> 
  
## <a name="permissions"></a><span data-ttu-id="6a8a4-124">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6a8a4-124">Permissions</span></span>

<span data-ttu-id="6a8a4-p106">Извлекается из рабочих нагрузок Office 365, например, SharePoint и OneDrive для бизнеса безопасности результатов рабочих обрезать в источнике. Пользователи не могут видеть ресурсы, таких как документы Word или презентации PowerPoint, они не могут видеть и доступ к с помощью Office 365. Они могут просматривать только свои собственные файлы и файлы, общие с ними автором явно или неявно (через членство в группе, например) в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p106">Work results retrieved from Office 365 workloads such as SharePoint and OneDrive for Business are security trimmed at the source. Users can't see resources such as Word documents or PowerPoint presentations they can't see and access through Office 365. They can only see their own files and files that have been shared with them by the author explicitly or implicitly (through a group membership, for example) in SharePoint.</span></span>
  
## <a name="protects-user-queries-from-the-public-portion-of-bing"></a><span data-ttu-id="6a8a4-128">Защищает запросы пользователей из общей части Bing</span><span class="sxs-lookup"><span data-stu-id="6a8a4-128">Protects user queries from the public portion of Bing</span></span>

<span data-ttu-id="6a8a4-129">Возможно, связанные с работой поисков конфиденциальные, Microsoft Search производитель реализовал набор показателей доверия способа обработки эти результаты на общедоступных веб-части из Bing.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-129">Because work-related searches may be sensitive, Microsoft Search has implemented a set of trust measures for how these are handled by the public web results part of Bing.</span></span>
  
<span data-ttu-id="6a8a4-130">Независимо от того, ли пользовательский запрос содержит один или несколько результатов рабочих в возвращенный ответ выполняются следующие меры.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-130">Regardless of whether a user query contains one or more work results in the returned response, the following measures are taken:</span></span>
  
- <span data-ttu-id="6a8a4-131">Ведение журнала</span><span class="sxs-lookup"><span data-stu-id="6a8a4-131">Logging</span></span>
    
  - <span data-ttu-id="6a8a4-p107">Все журналы поиска, относящиеся к Microsoft Search трафика отзыва идентифицируются и храниться отдельно от общего, трафика Microsoft Search. Они будет сохраняться 18 месяцев и доступ ограничивается только для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p107">All search logs pertaining to Microsoft Search traffic are de-identified and stored separately from public, non-Microsoft Search traffic. They're retained for 18 months, and access is restricted for debugging purposes only.</span></span>
    
  - <span data-ttu-id="6a8a4-134">Запросов в эти журналы не используется модель или концентрацию на общедоступных функции такие как автозаполнения или связанных с ними поисков для общедоступных веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-134">The queries in these logs are not used to model or train public features such as autosuggest or related searches for the public web.</span></span>
    
  - <span data-ttu-id="6a8a4-135">Ограниченный доступ осуществляется с помощью различных механизмов безопасности, включая группы безопасности и других слоев в пределах система проектирования.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-135">Restricted access is managed via various secure mechanisms, including security groups and other layers within the engineering system.</span></span>
    
- <span data-ttu-id="6a8a4-136">Журнал поиска</span><span class="sxs-lookup"><span data-stu-id="6a8a4-136">Search history</span></span>
    
  - <span data-ttu-id="6a8a4-137">Если вход с помощью учетной записи рабочего или школы журнал поиска не будут доступны на других компьютерах или устройствах.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-137">When signed in with a work or school account, a user's search history won't be available on other computers or devices.</span></span>
    
- <span data-ttu-id="6a8a4-138">Рекламу</span><span class="sxs-lookup"><span data-stu-id="6a8a4-138">Advertising</span></span>
    
  - <span data-ttu-id="6a8a4-139">Enterprise поисковых запросов не никогда не предоставлен или предложенных рекламодателями.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-139">Enterprise search queries are never shared with or suggested to advertisers.</span></span>
    
  - <span data-ttu-id="6a8a4-140">Журналы Ads поиска, относящиеся к Microsoft Search хранятся отдельно от общего трафика.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-140">Search Ads logs pertaining to Microsoft Search are stored separately from public traffic.</span></span>
    
  - <span data-ttu-id="6a8a4-141">Реклама никогда не предназначены для пользователей, на основе их работы удостоверения или организации.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-141">Ads are never targeted to a user based on their work identity or organization.</span></span>
    
## <a name="gdpr"></a><span data-ttu-id="6a8a4-142">GDPR</span><span class="sxs-lookup"><span data-stu-id="6a8a4-142">GDPR</span></span>

<span data-ttu-id="6a8a4-p108">[21 мая 2018, запись в блоге](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/) Майкрософт отражает значительные усилия для соответствия GDPR и как Майкрософт помогает организациями собственные обязательств GDPR соответствия требованиям. Дополнительные сведения можно найти в Microsoft [Вопросы и ответы Центр управления безопасностью](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs). Microsoft поисковых запросов, которые работают с данными клиента организационной клиентам в рамках веб-службы также будет выполнения обязательств процессора, как показано в [Вопросы и ответы Центр управления безопасностью](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs), описанные в статье 28. По отношению к запросов из Microsoft Search, перейдите к общедоступной Bing Корпорация Майкрософт является контроллером данных и производитель реализовал меры для отзыва определения запросов, как описано в разделе GDPR.</span><span class="sxs-lookup"><span data-stu-id="6a8a4-p108">The [May 21, 2018, blog post](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/) from Microsoft reflects our commitment to GDPR compliance and how Microsoft helps businesses and organizations with their own GDPR compliance obligations. You can find additional detail in the Microsoft [Trust Center FAQ](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs). Microsoft Search queries that operate against organizational customers' Customer Data within the Online Services will also meet the processor commitments outlined in Article 28 as reflected in the [Trust Center FAQ](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs). With respect to queries from Microsoft Search that go to public Bing, Microsoft is a data controller and has implemented measures to de-identify the queries as outlined under GDPR.</span></span>


