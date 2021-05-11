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
ms.openlocfilehash: 614fa241f353533b1c1e181904eb961fd55d0dfa
ms.sourcegitcommit: ea784081bc9c3ae7981a87a493d3a74503859dda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "52306073"
---
<!-- markdownlint-disable no-trailing-punctuation -->
# <a name="frequently-asked-questions"></a>Вопросы и ответы

Ниже перечислены наиболее распространенные вопросы.

> [!TIP]
> Вашего вопроса здесь нет? Задайте свой вопрос в разделе отзывов этой статьи.

## <a name="is-advanced-query-understanding-supported"></a>Поддерживается ли расширенное понимание запросов?

Да, Microsoft Search разбирает намерения запроса из более крупных фраз. Эта функция использует ИИ, чтобы узнать распространенные лишние фразы, которые пользователи добавляют в свои запросы, которые не влияют на их намерения поиска. Например, когда пользователь ищет дополнительные данные о том, как изменить *пароль,* мы извлекаем менее важные слова из запроса и запускаем на основе соответствующих паролей, таких как пароль *изменения.*
  
Эта функция не переопределит ключевые слова, заданные в центре администрирования Microsoft 365 [администратора.](https://admin.microsoft.com)
  
## <a name="can-you-search-for-files-on-premises"></a>Можно ли искать локальные файлы?

Да. Вы можете искать локальное SharePoint [файлы,](http://sharepoint.com/) если у вас есть гибридное развертывание SharePoint.
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a>Как сделать Bing поисковой системой по умолчанию для пользователей в организации?

Вот инструкции по настройке поисковой системы по умолчанию, домашней страницы по умолчанию и браузера по умолчанию, чтобы предоставить пользователям лучший опыт работы с Microsoft Search [в Bing:](https://Bing.com)

- [Настройка Microsoft Edge браузера по умолчанию](/deployedge/edge-default-browser)
- [Установка Bing в качестве поисковой системы по умолчанию](set-default-search-engine.md)
- [Настройка Bing.com в качестве корпоративной домашней страницы](set-default-homepage.md)

## <a name="how-are-my-search-results-protected"></a>Как защищаются мои результаты поиска?

Мы [Azure Active Directory](/azure/active-directory/) проверку подлинности для доступа к результатам из доверенных облаков. Пользователи, прошедшие проверку подлинности, видят в результатах поиска только тот контент, к которому у них есть доступ. Поисковые запросы деидентифицированы, а [](https://Bing.com) журналы отделены от общедоступных Bing поиска при использовании Microsoft Search в Bing.

## <a name="can-i-search-across-federated-organizations"></a>Можно ли выполнять поиск в разных федеративных организациях?

Нет.

## <a name="where-can-i-get-info-about-office-365-security-compliance-and-privacy"></a>Где можно получить сведения о Office 365 безопасности, соответствии требованиям и конфиденциальности?

Подробные сведения можно найти на страницах Центра доверия [для Office 365.](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx)

## <a name="can-guest-users-leverage-microsoft-search-in-my-organization"></a>Могут ли гостевых пользователей использовать Microsoft Search в моей организации?

Microsoft 365 позволяет тесно сотрудничать с людьми за пределами организации с помощью [гостевого доступа.](/microsoft-365/solutions/collaborate-with-people-outside-your-organization) Эти пользователи смогут выполнять операции поиска по документам, сайтам, группам, спискам и библиотекам. Однако гостевых пользователей не будет получать полный, персонализированный, Microsoft Search и может потребоваться использовать поле поиска на странице вместо единого окна Поиска Майкрософт в загоне.