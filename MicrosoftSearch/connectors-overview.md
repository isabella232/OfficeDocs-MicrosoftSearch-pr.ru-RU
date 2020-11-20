---
title: Обзор соединителей
ms.author: monaray
author: monaray97
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Общие сведения о Microsoft Graph Connectors for Microsoft Search
ms.openlocfilehash: 7388653927ca6a7af0ba64c3c592f2689780c181
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367526"
---
# <a name="overview-of-microsoft-graph-connectors"></a>Обзор соединителей Microsoft Graph

[Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) индексирует все данные [Microsoft 365](https://www.microsoft.com/microsoft-365) , чтобы обеспечить возможность поиска для пользователей. С помощью соединителей Microsoft Graph организация может индексировать сторонние данные, чтобы они отображались в результатах поиска Microsoft. Это расширяет типы источников контента, которые доступны для поиска в приложениях Microsoft 365 для продуктивной работы, а также в обширной экосистеме корпорации Майкрософт. Сторонние данные могут размещаться в локальной среде или в общедоступных или частных облаках.

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

Оставшаяся часть этой статьи предназначена для того, чтобы помочь администраторам Microsoft 365 найти ресурсы, которые аваиабле, чтобы ответить на следующие вопросы:

* [Какие источники данных могут быть подключены к поиску Майкрософт?](#what-data-sources-can-be-connected-to-microsoft-search)
* [Как управлять подключениями?](#how-do-i-manage-my-connections)
* [Каковы требования к лицензии и условия использования для соединителей Graph?](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [Как настроить и настроить результаты поиска?](#how-do-i-customize-and-configure-search-results)
* [Поиск данных о соединителе из настраиваемого приложения](#how-do-i-search-my-connector-data-from-a-custom-application)

<!---Modify to another note that is more accurate--->
> [!IMPORTANT]
> Microsoft Graph Connectors и API службы поиска, как правило, доступны в настоящее время. Первые развертывания будут выполняться для клиентов, настроенных для целевого выпуска. Если вы хотите использовать графический соединитель в клиенте, пользователи и администраторы должны принять участие в [целевой версии](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below**_
To create a _*connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a>Какие источники данных могут быть подключены к поиску Майкрософт?

Корпорация Майкрософт предоставляет десять графических соединителей, а наши партнеры по экосистеме создали более 100 дополнительных графических соединителей. Вы также можете создать собственный соединительный соединитель. 

### <a name="graph-connectors-by-microsoft"></a>Графические соединители корпорации Майкрософт

С помощью соединителей Graph, созданных корпорацией Майкрософт, можно подключаться к следующим источникам данных:

<!---Need to add a few links below when docs exist--->
* [Azure Data Lake Storage 2-го поколения](azure-data-lake-connector.md)
* [Azure DevOps](azure-devops-connector.md)
* Azure SQL
* [Корпоративные веб-сайты](enterprise-web-connector.md)
* [MediaWiki](mediawiki-connector.md)
* [Microsoft SQL Server](MSSQL-connector.md)
* [Файловый ресурс](fileshare-connector.md)
* Oracle (Предварительная версия)
* [SalesForce (Предварительная версия)](salesforce-connector.md)
* [ServiceNow](servicenow-connector.md)

В [галерее Graph Connectors](connectors-gallery.md) содержится краткое описание каждого из этих соединителей Graph. Если вы готовы подключить один из этих источников данных к клиенту, ознакомьтесь с [обзором программы установки](configure-connector.md) и другими статьями раздела Настройка соединителей Майкрософт, которые применимы к источнику данных.

### <a name="graph-connectors-by-our-partners"></a>Graph Connectors by наших партнеров

В [коллекции соединителей Microsoft Graph](connectors-gallery.md) содержатся краткие описания всех соединителей графов, созданных нашими партнерами, а также ссылки на веб-сайт каждого партнера. Свяжитесь с каждым партнером напрямую, чтобы узнать больше.

### <a name="build-your-own-graph-connector"></a>Создание собственного соединителя Graph

Если вы планируете создать собственный соединительный соединитель, ознакомьтесь со статьей [Обзор API Microsoft Search API в Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview) для получения дополнительных сведений.

## <a name="how-do-i-manage-my-connections"></a>Как управлять подключениями?

Вы можете управлять подключениями на [вкладке соединители](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) [центра администрирования Microsoft 365](https://admin.microsoft.com/). Дополнительные сведения можно найти [в разделе Manage Your Connections](manage-connector.md) .

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a>Каковы требования к лицензии и условия использования для соединителей Graph?

Вам необходима действительная лицензия Microsoft 365 или Office 365 и достаточная квота Graph Connectors для пользователей в вашей организации, чтобы просматривать данные из соединителей в результатах поиска.

Чтобы узнать больше, ознакомьтесь со статьей [требования к лицензии и цены](licensing.md) и [условия использования](terms-of-use.md).

## <a name="how-do-i-customize-and-configure-search-results"></a>Как настроить и настроить результаты поиска?

Существует несколько способов настройки и настройки результатов поиска. Чтобы узнать больше, ознакомьтесь со следующими статьями:

* [Управление вертикалями и типами результатов](customize-search-page.md)
* [Управление макетами результатов поиска](customize-results-layout.md)
* [Управление кластером результатов](result-cluster.md)
* [Управление настраиваемыми фильтрами](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a>Поиск данных о соединителе из настраиваемого приложения

После индексирования пользовательских данных разработчики могут [запрашивать эти данные](https://docs.microsoft.com/graph/search-concept-custom-types). Вы можете просматривать данные в любом приложении. Дополнительные сведения можно найти в [обзоре API службы поиска Microsoft Graph в Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).
