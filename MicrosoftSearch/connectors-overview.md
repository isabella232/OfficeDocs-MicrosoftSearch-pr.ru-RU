---
title: Обзор соединители Microsoft Graph
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
description: Обзор соединители Microsoft Graph для Поиска (Майкрософт)
ms.openlocfilehash: 13127d092fe4e624ed448037d83f16f83ddc560a
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084878"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a>Обзор соединители Microsoft Graph

[Поиск (Майкрософт)](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) индексирует [все ваши данные Microsoft 365,](https://www.microsoft.com/microsoft-365) чтобы сделать их поиском пользователей. С помощью соединители Microsoft Graph ваша организация может индексировать сторонние данные, чтобы они появляются в результатах Поиска (Майкрософт). Эта функция расширяет типы источников контента, доступных для поиска в приложениях Для повышения производительности Microsoft 365 и в экосистеме Майкрософт. Сторонние данные могут быть локально или в общедоступных или закрытых облаках.

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

Эта статья предназначена для помощи администраторам Microsoft 365 в поиске ресурсов, доступных для ответа на следующие вопросы:

* [Какие источники данных можно подключать к Поиску (Майкрософт)?](#what-data-sources-can-be-connected-to-microsoft-search)
* [Как управлять подключениями?](#how-do-i-manage-my-connections)
* [Каковы требования к лицензиям и условия использования соединители Graph?](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [Что такое функции предварительного просмотра?](#what-are-the-preview-features)
* [Как настроить и настроить результаты поиска?](#how-do-i-customize-and-configure-search-results)
* [Как искать данные соединители из пользовательского приложения?](#how-do-i-search-my-connector-data-from-a-custom-application)

<!---Modify to another note that is more accurate after rollout completion--->
> [!IMPORTANT]
> Теперь соединители Microsoft Graph и API Поиска (Майкрософт) доступны в целом. Первый выпуск будет для клиентов, настроенных для целевого выпуска. Если вы хотите использовать соединители Graph в клиенте, пользователи и администраторы должны выбрать выпуск [Targeted.](https://docs.microsoft.com/microsoft-365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below***
To create a **connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a>Какие источники данных можно подключать к Поиску (Майкрософт)?

Корпорация Майкрософт предоставляет 9 соединители Graph, и наши партнеры по экосистеме создали более 100 дополнительных соединители Graph. Вы также можете создать собственный соединител Graph.

### <a name="graph-connectors-by-microsoft"></a>Соединители Graph от Майкрософт

Вы можете подключаться к следующим источникам данных, используя соединители Graph, созданные корпорацией Майкрософт:

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

В [коллекции соединители Graph](connectors-gallery.md) содержится краткое описание каждого из этих соединитеителей Graph. Если вы готовы подключить один из этих источников данных к вашему арендатору, ознакомьтесь с обзором программы установки и другими статьями в разделе "Соединители установки" корпорации Майкрософт, которые относятся к вашему источнику данных. [](configure-connector.md)

### <a name="graph-connectors-by-our-partners"></a>Соединители Graph от наших партнеров

В [коллекции соединитеев Microsoft Graph](connectors-gallery.md) содержится краткое описание каждого соединители Graph, созданных нашими партнерами, и ссылка на веб-сайт каждого партнера. Чтобы узнать больше, свяжитесь с каждым партнером напрямую.

### <a name="build-your-own-graph-connector"></a>Создание собственного соединитела Graph

При желании вы можете создать собственный соединититель Graph. Дополнительные сведения о создании соединителов Graph см. в обзоре [API Поиска (Майкрософт) в Microsoft Graph.](https://docs.microsoft.com/graph/search-concept-overview)

## <a name="how-do-i-manage-my-connections"></a>Как управлять подключениями?

Вы можете управлять подключениями на вкладке ["Соединители"](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) в Центре администрирования [Microsoft 365.](https://admin.microsoft.com/) Дополнительные сведения об управлении подключениями см. в под [управлении подключениями.](manage-connector.md)

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a>Каковы требования к лицензиям и условия использования соединители Graph?

Для просмотра данных соединителов в результатах поиска пользователям в организации необходима действующая лицензия Microsoft 365 или Office 365 и достаточная квота соединителов Graph.

Дополнительные узнать [см. в требованиях к лицензиям, ценах](licensing.md) [и условиях использования.](terms-of-use.md)

## <a name="what-are-the-preview-features"></a>Что такое функции предварительного просмотра?

Хотя соединители Microsoft Graph и API Поиска (Майкрософт) теперь доступны в целом, существует несколько функций, доступных в предварительной версии.

Набор соединители и функции в предварительной версии включают:

* [Соединителю Azure DevOps](azure-devops-connector.md)
* [Соединители Salesforce](salesforce-connector.md)
* [Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска, использующем исходные ALS
* [Управление кластером результатов](result-cluster.md)

## <a name="how-do-i-customize-and-configure-search-results"></a>Как настроить и настроить результаты поиска?

Существует множество способов настройки и настройки результатов поиска. Подробнее см. в следующих статьях:

* [Управление вертикалями и типами результатов](customize-search-page.md)
* [Управление макетами результатов поиска](customize-results-layout.md)
* [Управление кластером результатов](result-cluster.md)
* [Управление пользовательскими фильтрами](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a>Как искать данные соединители из пользовательского приложения?

После индексации пользовательских данных разработчики могут [запросить эти данные.](https://docs.microsoft.com/graph/search-concept-custom-types) Вы можете просматривать данные в любом приложении. Дополнительные сведения см. в [обзоре API Поиска (Майкрософт) в Microsoft Graph.](https://docs.microsoft.com/graph/search-concept-overview)

## <a name="next-steps"></a>Дальнейшие действия

Убедитесь, что вы настроили результаты поиска согласно рекомендациям в этой статье Как настроить и настроить [результаты поиска?](#how-do-i-customize-and-configure-search-results). Дополнительные узнать о настройке результатов поиска см. на странице "Настройка [результатов поиска".](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page)

## <a name="limitations"></a>Ограничения

* При **публикации** соединители, созданного корпорацией Майкрософт, может потребоваться несколько минут для создания подключения. В течение этого времени подключение будет отложено.

* Центр [администрирования Microsoft 365](https://admin.microsoft.com) не поддерживает  редактирование схемы поиска после публикации подключения. Чтобы изменить схему поиска, удалите подключение и создайте новое.

* Пропускная способность при входеть в нее отлажается примерно при четырех пунктах в секунду.

* Обновления схемы не поддерживаются. После создания настройки подключения обновить схему нельзя. Можно только удалить и повторно создать подключение.

* Существует ограничение подключений. Каждый клиент может создать до 10 подключений.

* Поддержка редактирования подключения недоступна. После создания подключения изменить или изменить его нельзя. Если необходимо изменить какие-либо сведения, необходимо удалить и повторно создать подключение.
