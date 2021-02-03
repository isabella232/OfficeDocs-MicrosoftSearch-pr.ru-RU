---
title: Соединитель MediaWiki Graph для Поиска (Майкрософт)
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединитель MediaWiki Graph для Поиска (Майкрософт)
ms.openlocfilehash: 9d9d7a1ef9aeaba079f8cccef1ec4a4836768e8d
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084986"
---
<!---Previous ms.author: monaray --->

# <a name="mediawiki-graph-connector"></a>Соединитель MediaWiki Graph

Соединитель MediaWiki Graph позволяет организации обнаруживировать и индексировать данные из вики-сайта, созданного с помощью программного обеспечения MediaWiki. Этот соединитатель индексирует указанный контент в Поиск (Майкрософт) и поддерживает периодические обходы для поддержания индекса в курсе.

> [!NOTE]
> Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.

Эта статья для всех, кто настраивает, запускает и отслеживает соединители ServiceNow Graph. Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединитеструктору MediaWiki Graph. В этой статье также содержатся сведения об [ограничениях.](#limitations)

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

Введите **URL-адрес вики-сайта** и выберите тип проверки подлинности в выпадаемом меню параметров.  Возможные варианты: **None,** **Basic** и **OAuth 2.0 AAD.**

Если в **качестве** типа проверки подлинности вы  выберете "Базовый", необходимо ввести имя пользователя и пароль **для** вики-сайта.

Если в качестве типа проверки подлинности вы выбрали **AAD OAuth 2.0,** необходимо предоставить ИД ресурса для вики-установки.  Вам также потребуется предоставить **ИД**  клиента и секрет клиента, созданные на странице регистрации приложения AAD.

## <a name="step-4-manage-search-permissions"></a>Шаг 4. Управление разрешениями поиска

Соединитель MediaWiki поддерживает только разрешения поиска, видимые **всем.** Индексные данные появляются в результатах поиска и видны всем пользователям в организации.

## <a name="step-5-assign-property-labels"></a>Шаг 5. Назначение меток свойств

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a>Шаг 6. Управление схемой

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a>Шаг 7. Выбор параметров обновления

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a>Шаг 8. Проверка подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a>Ограничения

Соединитель MediaWiki имеет указанные в предварительной версии ограничения:

* Поддерживает только облачные вики-сайты.
* Поддерживает только Базовый или OAuth 2.0 с проверкой подлинности Azure Active Directory или Azure.
* Не поддерживает выделение пространства имен для индексации. Индексирует только пространства имен Main, Category и File.
* Не поддерживает списки управления доступом (ALS). Таким образом, индексные страницы видны всем пользователям в организации.
