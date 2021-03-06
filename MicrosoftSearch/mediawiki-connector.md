---
title: Соединитель MediaWiki Graph для microsoft Search
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединитетеля MediaWiki Graph для поиска в Microsoft Search
ms.openlocfilehash: 1c2908de859056ccb26b862820e8b3be7a158569
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508772"
---
<!---Previous ms.author: monaray --->

# <a name="mediawiki-graph-connector"></a>Соединитель MediaWiki Graph

Соединитель MediaWiki Graph позволяет организации обнаруживть и индексировать данные из вики-сайта, созданного с помощью программного обеспечения MediaWiki. Этот соединитатель индексирует указанное содержимое в Microsoft Search и поддерживает периодические обходы, чтобы поддерживать индекс в курсе.

> [!NOTE]
> Ознакомьтесь [**с статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общие инструкции по настройке соединитений Graph.

Эта статья для всех, кто настраивает, запускает и контролирует соединитель Диаграммы MediaWiki. Он дополняет общий процесс установки и показывает инструкции, применимые только к соединитеку MediaWiki Graph. В этой статье также содержатся сведения об [ограничениях.](#limitations)

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

Введите **URL-адрес вики** и выберите **тип** проверки подлинности из выпадаемого меню параметров. Параметры **None,** **Basic** и **OAuth 2.0 AAD**.

Если вы **выбираете Basic** в качестве типа проверки подлинности, вам потребуется предоставить имя пользователя и пароль для вики.  

Если вы выбрали **AAD OAuth 2.0** в качестве типа  проверки подлинности, необходимо предоставить идентификацию ресурса вики-установки. Кроме того, необходимо предоставить секретный  **номер клиента** и клиент, созданный на странице регистрации приложений AAD.

## <a name="step-4-manage-search-permissions"></a>Шаг 4. Управление разрешениями на поиск

Соединитель MediaWiki поддерживает только разрешения поиска, видимые **каждому.** Индексные данные появляются в результатах поиска и видны всем пользователям в организации.

## <a name="step-5-assign-property-labels"></a>Шаг 5. Назначение меток свойств

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a>Шаг 6. Управление схемой

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a>Шаг 7. Выбор параметров обновления

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a>Шаг 8. Просмотр подключения

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a>Ограничения

Соединитель MediaWiki имеет эти ограничения в выпуске предварительного просмотра:

* Поддерживает только облачные вики.
* Поддерживает только Basic или OAuth 2.0 с помощью Azure Active Directory или Проверки подлинности Azure.
* Не поддерживает выбор пространства имен для индексации. Индексирует только пространства имен Main, Category и File.
* Не поддерживает списки управления доступом (ACLs). Таким образом, индексные страницы видны всем пользователям в организации.
