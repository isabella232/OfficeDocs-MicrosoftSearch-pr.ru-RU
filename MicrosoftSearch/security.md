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
# <a name="security-for-microsoft-search"></a>Безопасность для Microsoft Search

Система безопасности уровня предприятия Microsoft Search всегда отслеживает пользователей и данные, защищенные.
  
## <a name="secure-by-default"></a>Безопасность по умолчанию

Microsoft Search всегда гарантирует, что запросы выполняются по протоколу HTTPS. В этом защищают гарантирует, что подключение является зашифрованные сквозного для повышения безопасности.
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a>Проверка подлинности и авторизация с Azure Active Directory

Проверка подлинности для поиска Microsoft связана с Azure Active Directory. При пользователи Microsoft Search перейти Bing, заголовок будет отображение параметров входа в учетную запись Майкрософт как Bing, а рабочий также или школы учетной записи. Если Bing не может определить, является ли пользователь подходящими участника, пользователи могут перейти на страницу [Изучение Microsoft Search](https://www.bing.com/business/explore) которой они будут автоматически перенаправляться на странице входа вашей организации. 
  
Пользователей можно получить доступ к Microsoft Search только с помощью учетной записи рабочего или школы. Они должны выполнить вход с один набор учетных данных, которые они используют для доступа к службам Office 365, например, SharePoint или Outlook. Личная учетная запись Майкрософт не может использоваться для входа в Microsoft Search.
  
Пользователи не могут входить в систему Bing с помощью учетной записи Майкрософт и работы или школы учетной записи в то же время.
  
## <a name="single-sign-on"></a>Единый вход

Если пользователь прошли проверку подлинности с помощью своей учетной записи рабочего или школы в другой службы, такие как Outlook и SharePoint, они будут быть автоматически входить в систему Microsoft Search при попытке Bing в одном браузера. Кроме того при входе пользователя из Microsoft Search, они будут автоматически осуществлен от других служб браузера.
  
## <a name="communicates-with-the-trusted-cloud-from-the-browser"></a>Взаимодействует с облаком надежных в браузере

При пользователь подписывает своей работе или учетная запись школа, Bing будет загрузить необходимые клиентские библиотеки в браузере, чтобы включить результаты поиска Microsoft. Затем при выполнении поиска в браузере вызывается облаке Office 365 для получения результатов рабочих. Для этого Microsoft Search использует выделенный API-Интерфейс, который является C уровня (1 типа SOC2) спецификации этих Office 365 [Framework соответствия требованиям для действие экспортного отраслевых стандартов](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (ФАЙЛ для загрузки). Это означает, что результаты работы и рабочих данных никогда не проходят через Bing системы. 
  
## <a name="permissions"></a>Разрешения

Извлекается из рабочих нагрузок Office 365, например, SharePoint и OneDrive для бизнеса безопасности результатов рабочих обрезать в источнике. Пользователи не могут видеть ресурсы, таких как документы Word или презентации PowerPoint, они не могут видеть и доступ к с помощью Office 365. Они могут просматривать только свои собственные файлы и файлы, общие с ними автором явно или неявно (через членство в группе, например) в SharePoint.
  
## <a name="protects-user-queries-from-the-public-portion-of-bing"></a>Защищает запросы пользователей из общей части Bing

Возможно, связанные с работой поисков конфиденциальные, Microsoft Search производитель реализовал набор показателей доверия способа обработки эти результаты на общедоступных веб-части из Bing.
  
Независимо от того, ли пользовательский запрос содержит один или несколько результатов рабочих в возвращенный ответ выполняются следующие меры.
  
- Ведение журнала
    
  - Все журналы поиска, относящиеся к Microsoft Search трафика отзыва идентифицируются и храниться отдельно от общего, трафика Microsoft Search. Они будет сохраняться 18 месяцев и доступ ограничивается только для целей отладки.
    
  - Запросов в эти журналы не используется модель или концентрацию на общедоступных функции такие как автозаполнения или связанных с ними поисков для общедоступных веб-сайта.
    
  - Ограниченный доступ осуществляется с помощью различных механизмов безопасности, включая группы безопасности и других слоев в пределах система проектирования.
    
- Журнал поиска
    
  - Если вход с помощью учетной записи рабочего или школы журнал поиска не будут доступны на других компьютерах или устройствах.
    
- Рекламу
    
  - Enterprise поисковых запросов не никогда не предоставлен или предложенных рекламодателями.
    
  - Журналы Ads поиска, относящиеся к Microsoft Search хранятся отдельно от общего трафика.
    
  - Реклама никогда не предназначены для пользователей, на основе их работы удостоверения или организации.
    
## <a name="gdpr"></a>GDPR

[21 мая 2018, запись в блоге](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/) Майкрософт отражает значительные усилия для соответствия GDPR и как Майкрософт помогает организациями собственные обязательств GDPR соответствия требованиям. Дополнительные сведения можно найти в Microsoft [Вопросы и ответы Центр управления безопасностью](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs). Microsoft поисковых запросов, которые работают с данными клиента организационной клиентам в рамках веб-службы также будет выполнения обязательств процессора, как показано в [Вопросы и ответы Центр управления безопасностью](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs), описанные в статье 28. По отношению к запросов из Microsoft Search, перейдите к общедоступной Bing Корпорация Майкрософт является контроллером данных и производитель реализовал меры для отзыва определения запросов, как описано в разделе GDPR.

