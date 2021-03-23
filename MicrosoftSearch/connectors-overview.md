---
title: Обзор соединители Microsoft Graph
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
description: Обзор соединители Microsoft Graph для microsoft Search
ms.openlocfilehash: 2d49471c703b765f6e99324f39dbe730f6dea814
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031659"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a>Обзор соединители Microsoft Graph

[Microsoft Search](./overview-microsoft-search.md) индексирует все данные [Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их более понятными для пользователей. С помощью соединители Microsoft Graph ваша организация может индексировать сторонние данные, чтобы они фигурали в результатах поиска Майкрософт. Эта функция расширяет типы источников контента, доступных для поиска в приложениях производительности Microsoft 365, и более широкую экосистему Майкрософт. Сторонние данные могут быть организованы на локальной основе или в общедоступных или частных облаках.

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

Эта статья предназначена для того, чтобы помочь администраторам Microsoft 365 найти ресурсы, доступные для ответа на следующие вопросы:

* [Какие источники данных можно подключать к Microsoft Search?](#what-data-sources-can-be-connected-to-microsoft-search)
* [Как управлять подключениями?](#how-do-i-manage-my-connections)
* [Каковы требования к лицензиям и условия использования для соединители Graph?](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [Какие функции предварительного просмотра?](#what-are-the-preview-features)
* [Как настроить и настроить результаты поиска?](#how-do-i-customize-and-configure-search-results)
* [Как искать данные соединитетеля в настраиваемом приложении?](#how-do-i-search-my-connector-data-from-a-custom-application)
* [Как настроить результаты поиска?](#how-do-i-customize-search-results)
* [Каковы ограничения соединитетеля](#what-are-the-connector-limitations)

<!---Modify to another note that is more accurate after rollout completion--->
> [!IMPORTANT]
> Теперь в общем доступе доступны соединители Microsoft Graph и API поиска Майкрософт. Первыми выкатами будут клиенты, настроенные для целевого выпуска. Если вы хотите использовать соединители Graph в клиенте, пользователи и администраторы должны выбрать [целевой выпуск.](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide)

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

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a>Какие источники данных можно подключать к Microsoft Search?

Корпорация Майкрософт предоставляет 9 соединители Graph, а наши партнеры по экосистеме создали более 100 соединители Graph. Вы также можете создать собственный соединитатель Graph.

### <a name="graph-connectors-by-microsoft"></a>Соединители Graph от Майкрософт

Вы можете подключиться к следующим источникам данных с помощью соединители Graph, созданные Корпорацией Майкрософт:

<!---Add links below when new docs are created--->
* [Azure Data Lake Storage 2-го поколения](azure-data-lake-connector.md)
* [Azure DevOps](azure-devops-connector.md)
* [Azure SQL и Microsoft SQL Server](MSSQL-connector.md)
* [Корпоративные веб-сайты](enterprise-web-connector.md)
* [MediaWiki](mediawiki-connector.md)
* [Файловый ресурс](fileshare-connector.md)
* [Oracle SQL (предварительная версия)](OracleSQL-connector.md)
* [Salesforce (предварительная версия)](salesforce-connector.md)
* [ServiceNow](servicenow-connector.md)

Галерея [соединители Graph](connectors-gallery.md) содержит краткое описание каждого из этих соединителеров Graph. Если вы готовы подключить один из этих источников данных к вашему клиенту, обязательно ознакомьтесь с обзором установки и другими статьями в разделе Установки в разделе Microsoft, которые применяются к источнику данных. [](configure-connector.md)

### <a name="graph-connectors-by-our-partners"></a>Соединители графов нашими партнерами

В [галерее](connectors-gallery.md) соединители Microsoft Graph содержится краткое описание каждого из соединители Graph, созданных нашими партнерами, и ссылка на веб-сайт каждого партнера. Чтобы узнать больше, свяжитесь с каждым партнером напрямую.

### <a name="build-your-own-graph-connector"></a>Создание собственного соединитетеля Graph

При желании можно создать собственный соединититель Graph. Дополнительные сведения о создании соединителов Graph см. в обзоре [API поиска Майкрософт в Microsoft Graph.](/graph/search-concept-overview)

## <a name="how-do-i-manage-my-connections"></a>Как управлять подключениями?

Вы можете управлять подключениями со вкладки [Соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в центре администрирования [Microsoft 365.](https://admin.microsoft.com/) Дополнительные сведения об управлении подключениями см. в рублях: [Управление подключениями.](manage-connector.md)

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a>Каковы требования к лицензиям и условия использования для соединители Graph?

Вам нужна действительная лицензия Microsoft 365 или Office 365 и достаточную квоту соединителов графа для пользователей в организации для просмотра данных соединителов в результатах поиска.

Дополнительные новости см. в дополнительных подробной информации о требованиях к [лицензиям, ценах](licensing.md) и [сроках использования.](terms-of-use.md)

## <a name="what-are-the-preview-features"></a>Какие функции предварительного просмотра?

Несмотря на то что соединители Microsoft Graph и API поиска в Microsoft Search теперь доступны, существует несколько функций, которые находятся в предварительном просмотре.

Набор соединители и функции в предварительном просмотре включают в себя:

* [Соединителю Azure DevOps](azure-devops-connector.md)
* [Соединители salesforce](salesforce-connector.md)
* [Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска с использованием исходных acLs
* [Управление кластером результатов](result-cluster.md)

## <a name="how-do-i-customize-and-configure-search-results"></a>Как настроить и настроить результаты поиска?

Существует множество способов настройки и настройки результатов поиска. Дополнительные статьи см. в следующих статьях:

* [Управление вертикалями и типами результатов](customize-search-page.md)
* [Управление макетами результатов поиска](customize-results-layout.md)
* [Управление кластером результатов](result-cluster.md)
* [Управление пользовательскими фильтрами](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a>Как искать данные соединитетеля в настраиваемом приложении?

После индексации пользовательских данных разработчики могут [запрашивать эти данные.](/graph/search-concept-custom-types) Вы можете просматривать данные в любом приложении. Дополнительные сведения см. в [обзоре API поиска Майкрософт в Microsoft Graph.](/graph/search-concept-overview)

## <a name="how-do-i-customize-search-results"></a>Как настроить результаты поиска?

Следующим шагом является настройка результатов поиска, как рекомендуется в этой статье Как настроить и [настроить результаты поиска?](#how-do-i-customize-and-configure-search-results). Дополнительные информацию о настройке результатов поиска см. в странице [Настройка страницы результатов поиска.](./configure-connector.md#next-steps-customize-the-search-results-page)

## <a name="what-are-the-connector-limitations"></a>Какие ограничения имеют соединители?

* При **публикации** соединитетеля, созданного Корпорацией Майкрософт, может потребоваться несколько минут для создания подключения. В течение этого времени подключение будет показывать свое состояние как ожидалось.

* Центр [администрирования Microsoft 365](https://admin.microsoft.com) не поддерживает  редактирование схемы поиска после публикации подключения. Чтобы изменить схему поиска, удалите подключение и создайте новую.

* Пропускная способность ingestion отламеяна примерно со 4 элементами в секунду.

* Обновления схемы не поддерживаются. После создания настройки подключения не будет возможности обновить схему. Вы можете только удалить и повторно создать подключение.

* Существует ограничение подключения. Каждый клиент может создать до 10 подключений.

* Поддержка редактирования подключения недоступна. После создания подключения изменить или изменить его нельзя. Если вам необходимо изменить какие-либо сведения, необходимо удалить и воссоздать подключение.