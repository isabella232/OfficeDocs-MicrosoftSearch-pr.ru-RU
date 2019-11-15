---
title: Обзор соединителей
ms.author: mounika.narayanan
author: monaray
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
ms.openlocfilehash: 8b46dc5150fa7f302f2d8abe98018465f2e4e1c3
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626321"
---
# <a name="overview-of-microsoft-graph-connectors"></a>Обзор соединителей Microsoft Graph

Microsoft Search индексирует все данные Microsoft 365, чтобы обеспечить возможность поиска для пользователей. С помощью Microsoft Graph Connectors в Организации можно индексировать сторонние данные, которые будут отображаться в результатах поиска Майкрософт. Сторонние данные могут размещаться в локальной среде или в общедоступных или частных облаках. Соединители расширяют типы источников контента, которые доступны для поиска в приложениях Microsoft 365 для продуктивной работы, а также в более широком наборе Microsoft экосистеме.

> [!IMPORTANT]
> **Заявление об отказе**: Microsoft Graph Connectors и API службы поиска Microsoft (индексирование и поиск) в настоящее время находятся в режиме предварительного просмотра. Дополнительные сведения о предварительной версии можно найти в [статье Microsoft Graph Connectors Preview](connectors-preview.md). Чтобы принять участие в предварительной версии, необходимо сначала добавить [форму подписки на предварительный просмотр соединителей Microsoft Graph](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u).

## <a name="architecture"></a>Архитектура
На следующей архитектурной схеме платформы Microsoft Graph показано, как соединительное содержимое проходит через индексирование содержимого для пользователей в клиентах [Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) . В этой статье описываются основные конструктивные блоки в процессе обработки поток данных Microsoft Graph Connectors.

![](media/highlevel-connectors_FINAL.png)

API создает экземпляр одного подключения для каждого источника данных. Затем API индексирует и сохраняет данные. Установленные подключения взаимодействуют с Microsoft Search, поэтому пользователи могут получать результаты поиска.

Все соединители, созданные корпорацией Майкрософт, можно настроить в [центре администрирования microsoft 365](https://admin.microsoft.com). Центр администрирования упрощает настройку соединителя с помощью простого пользовательского интерфейса.

Чтобы создать **Подключение** к источнику данных, администраторам необходим доступ с проверкой подлинности к данным и всему репозиторию контента. Данные отправляются в службу соединителя Graph для индексирования.

## <a name="available-connectors"></a>Доступные соединители
В настоящее время существует 6 соединителей, созданных корпорацией Майкрософт, и более чем через 100 соединители доступны у наших партнеров по экосистеме.

Чтобы просмотреть соединители от одного из наших партнеров по экосистеме, свяжитесь с ними напрямую. Дополнительные сведения можно найти в [коллекции соединителей Microsoft Graph](connectors-gallery.md).

Вы также можете [создать собственный соединитель](https://docs.microsoft.com/graph/search-concept-overview).

### <a name="connectors-by-microsoft"></a>Соединители корпорации Майкрософт
Ознакомительная версия Microsoft Graph Connectors содержит шесть соединителей, созданных корпорацией Майкрософт. Вы можете настроить их в [центре администрирования microsoft 365](https://admin.microsoft.com) и узнать, как [настроить соединитель, созданный корпорацией Майкрософт](configure-connector.md).

В следующих разделах приведены краткие описания для этих соединителей, созданных корпорацией Майкрософт. В связанных статьях можно получить дополнительные сведения о каждом соединителе.

- **[Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)**. С помощью этого соединителя Microsoft Graph пользователи в вашей организации могут искать файлы и контент, хранящиеся в контейнерах больших двоичных объектов Azure. Соединитель Gen2 для Azure Data Lake Storage также индексирует папки с включенной иерархией в учетных записях Azure Data Lake Storage Gen2, которые вы указали.
Дополнительные сведения о [соединителе Gen2 для Azure Data Lake Storage](azure-data-lake-connector.md).

- **Корпоративные веб-сайты**. С помощью этого соединителя Microsoft Graph пользователи в вашей организации могут выполнять поиск на страницах любого веб-сайта, отличного от SharePoint Enterprise.
Узнайте больше о [соединителе корпоративных веб-сайтов](enterprise-web-connector.md).

- **Общая папка файлов**. С помощью этого соединителя Microsoft Graph пользователи в вашей организации могут выполнять поиск файлов, хранящихся в локальных общих папках Windows.
Узнайте больше о [соединителе файлового ресурса](file-share-connector.md).

- **[Медиавики](https://www.mediawiki.org/wiki/MediaWiki)**. С помощью этого соединителя Microsoft Graph пользователи могут выполнять поиск в статьях базы знаний на вики-сайтах, создаваемых в Организации с помощью Медиавики.
Дополнительные сведения о [соединителе Медиавики](mediawiki-connector.md).

- **[Microsoft SQL Server](https://www.microsoft.com/sql-server/sql-server-2017)**. С помощью этого соединителя Microsoft Graph пользователи в вашей организации могут выполнять поиск данных в локальных базах данных SQL Server.
Дополнительные сведения о [соединителе Microsoft SQL Server](MSSQL-connector.md).

- **[ServiceNow](https://www.servicenow.com)**. С помощью этого соединителя Microsoft Graph пользователи в вашей организации могут выполнять поиск в статьях базы знаний в экземпляре ServiceNow.
Дополнительные сведения о [соединителе ServiceNow](servicenow-connector.md).

### <a name="connectors-from-our-partners"></a>Соединители от наших партнеров
Для предварительного просмотра на наших партнерах по экосистеме доступно свыше 100 соединителей. Чтобы просмотреть соединители от одного из наших партнеров по экосистеме, свяжитесь с ними напрямую.
Узнайте больше о соединителях наших партнеров в [коллекции соединителей Microsoft Graph](connectors-gallery.md).

### <a name="build-your-own-connector"></a>Создание собственного соединителя
Чтобы индексировать пользовательские типы данных или файлы, разработчики могут создавать соединители в [Microsoft Graph](https://developer.microsoft.com/graph/). Соединитель — это приложение, которое [создает подключение](https://docs.microsoft.com/graph/search-index-manage-connections) и передает элементы в индекс поиска Майкрософт. Для получения дополнительных сведений ознакомьтесь с [обзором, чтобы расширить возможности поиска Microsoft для приложений в Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).

### <a name="search-results-with-your-custom-built-connector"></a>Результаты поиска с помощью созданного настраиваемого соединителя
После индексирования пользовательских данных разработчики могут [запрашивать эти данные](https://docs.microsoft.com/graph/search-concept-custom-types). Вы можете просматривать данные в любом приложении. Для получения дополнительных сведений ознакомьтесь с [обзором, чтобы расширить возможности поиска Microsoft для приложений в Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).

## <a name="license-requirements"></a>Требования лицензирования
Чтобы просмотреть данные из соединителей в результатах поиска, у пользователей должна быть одна из следующих подписок Microsoft 365:
- <a href="https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans" target="_blank">Microsoft 365 для предприятий E3 или "е"</a>
- <a href="https://www.microsoft.com/microsoft-365/academic/compare-office-365-education-plans?activetab=tab:primaryr1" target="_blank">Microsoft 365 для образовательных учреждений a3 или A5</a>
