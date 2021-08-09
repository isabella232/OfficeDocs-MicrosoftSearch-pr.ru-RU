---
title: Обзор Graph соединители Майкрософт
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
description: Обзор соединители microsoft Graph для Поиск (Майкрософт)
ms.openlocfilehash: a7f2fe8b5278df9368c3036895450a74ad7eae8a644aedc147fb16dd0efdd46e
ms.sourcegitcommit: 71ac2a38971ca4452d1bddfc773ff8f45e1ffd77
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "54533185"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a>Обзор соединителей Microsoft Graph

[Поиск (Майкрософт)](./overview-microsoft-search.md) индексирует все [Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их поиском для пользователей. С помощью соедините Graph Microsoft организация может индексировать сторонние данные, чтобы они Поиск (Майкрософт) результатах. Эта возможность расширяет типы источников содержимого, по которым можно выполнять поиск как в ориентированных на повышение производительности приложениях Microsoft 365, так и в более широком контексте экосистемы Майкрософт. Сторонние данные могут быть организованы на локальной основе или в общедоступных или частных облаках.

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

Эта статья призвана помочь администраторам Microsoft 365 найти ресурсы, доступные для ответа на следующие вопросы:

* [Какие источники данных можно подключать к Поиск (Майкрософт)?](#what-data-sources-can-be-connected-to-microsoft-search)
* [Как управлять подключениями?](#how-do-i-manage-my-connections)
* [Каковы требования к лицензиям и условия использования для соединители Microsoft Graph?](#what-are-the-license-requirements-and-terms-of-use-for-connectors)
* [Какие функции предварительного просмотра?](#what-are-the-preview-features)
* [Как настроить и настроить результаты поиска?](#how-do-i-customize-and-configure-search-results)
* [Как искать данные соединитетеля в настраиваемом приложении?](#how-do-i-search-my-connector-data-from-a-custom-application)
* [Как настроить результаты поиска?](#how-do-i-customize-search-results)
* [Каковы ограничения соединитетеля](#what-are-the-connector-limitations)

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](./overview-microsoft-search.md) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below***
To create a **connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a>Какие источники данных можно подключать к Поиск (Майкрософт)?

Корпорация Майкрософт предоставляет 9 соединители, а наши партнеры по экосистеме создали более 100 соединители. Вы также можете создать собственный соединитектор.

### <a name="microsoft-graph-connectors-by-microsoft"></a>Соединители Graph Майкрософт

Вы можете подключиться к следующим источникам данных с помощью соединители, созданные Корпорацией Майкрософт:

<!---Add links below when new docs are created--->
* [Azure Data Lake Storage 2-го поколения](azure-data-lake-connector.md)
* [Azure DevOps](azure-devops-connector.md)
* [Azure SQL и Microsoft SQL Server](MSSQL-connector.md)
* [Корпоративные веб-сайты](enterprise-web-connector.md)
* [MediaWiki](mediawiki-connector.md)
* [Файловый ресурс](fileshare-connector.md)
* [Oracle SQL](OracleSQL-connector.md)
* [Salesforce (предварительная версия)](salesforce-connector.md)
* [ServiceNow](servicenow-connector.md)

В [галерее соедините](https://www.microsoft.com/microsoft-search/connectors) Graph Microsoft содержится краткое описание каждого из этих соединитетелей. Если вы готовы подключить один из этих источников данных к вашему клиенту, обязательно ознакомьтесь с обзором установки и другими статьями в разделе Установки в разделе Microsoft, которые применяются к источнику данных. [](configure-connector.md)

### <a name="microsoft-graph-connectors-by-our-partners"></a>Соединители Graph Майкрософт нашими партнерами

Галерея [соедините Graph](https://www.microsoft.com/microsoft-search/connectors) Майкрософт содержит краткое описание каждого из соединители, созданных нашими партнерами, и ссылку на веб-сайт каждого партнера. Чтобы узнать больше, свяжитесь с каждым партнером напрямую.

### <a name="build-your-own-microsoft-graph-connector"></a>Создание собственного соединитетеля Graph Майкрософт

При желании можно создать собственный соединититель. Дополнительные сведения о создании соединители см. в записи Сборка первого [настраиваемой соединители Microsoft Graph.](/graph/connecting-external-content-build-quickstart)

## <a name="how-do-i-manage-my-connections"></a>Как управлять подключениями?

Вы можете управлять подключениями со вкладки [Соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в [Центр администрирования Microsoft 365.](https://admin.microsoft.com/) Дополнительные сведения об управлении подключениями см. в рублях: [Управление подключениями.](manage-connector.md)

## <a name="what-are-the-license-requirements-and-terms-of-use-for-connectors"></a>Каковы требования к лицензиям и условия использования соединители?

Для просмотра данных из соединители в результатах поиска Microsoft 365 или Office 365 лицензии и достаточной квоты соединителов для пользователей в организации.

Дополнительные новости см. в дополнительных подробной информации о требованиях к [лицензиям, ценах](licensing.md) и [сроках использования.](terms-of-use.md)

## <a name="what-are-the-preview-features"></a>Какие функции предварительного просмотра?

Несмотря на Graph и Поиск (Майкрософт) API, в настоящее время доступны несколько функций, которые находятся в предварительном просмотре.

Набор соединители и функции в предварительном просмотре включают в себя:

* [Azure DevOps соединители](azure-devops-connector.md)
* [Соединители salesforce](salesforce-connector.md)
* [Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска с использованием исходных acLs
* [Управление кластером результатов](result-cluster.md)
* [Несколько подключений в вертикали](customize-search-page.md#multiple-connections-in-a-vertical)

## <a name="how-do-i-customize-and-configure-search-results"></a>Как настроить и настроить результаты поиска?

Существует множество способов настройки и настройки результатов поиска. Дополнительные статьи см. в следующих статьях:

* [Управление вертикалями и типами результатов](customize-search-page.md)
* [Управление макетами результатов поиска](customize-results-layout.md)
* [Управление кластером результатов](result-cluster.md)
* [Управление пользовательскими фильтрами](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a>Как искать данные соединитетеля в настраиваемом приложении?

После индексации пользовательских данных разработчики могут [запрашивать эти данные.](/graph/search-concept-custom-types) Вы можете просматривать данные в любом приложении. Дополнительные сведения см. в [обзоре API Поиск (Майкрософт) Microsoft Graph.](/graph/search-concept-overview)

## <a name="how-do-i-customize-search-results"></a>Как настроить результаты поиска?

Следующим шагом является настройка результатов поиска, как рекомендуется в этой статье Как настроить и [настроить результаты поиска?](#how-do-i-customize-and-configure-search-results). Дополнительные информацию о настройке результатов поиска см. в странице [Настройка страницы результатов поиска.](customize-search-page.md)

## <a name="what-are-the-connector-limitations"></a>Какие ограничения имеют соединители?

* При **публикации** соединитетеля, созданного Корпорацией Майкрософт, может занять несколько минут для создания подключения. В течение этого времени подключение будет показывать свое состояние как ожидалось.

* Пропускная способность ingestion отламеяна примерно по четырем пунктам в секунду.

* Обновления схемы не поддерживаются. После создания настройки подключения не будет возможности обновить схему. Вы можете только удалить и повторно создать подключение.

* Существует ограничение подключения. Каждый клиент может создать до 10 подключений.

* Вы не можете изменить или изменить подключение после его создания. Если вам необходимо изменить какие-либо сведения, необходимо удалить и воссоздать подключение.
