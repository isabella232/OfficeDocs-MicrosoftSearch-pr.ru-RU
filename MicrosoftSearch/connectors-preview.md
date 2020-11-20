---
title: Предварительный просмотр соединителей
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
description: Дополнительные сведения о Microsoft Graph Connectors Preview for Microsoft Search.
ms.openlocfilehash: 592e108fe0333e4faf8ff2e4618f9d5216847b8a
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367670"
---
# <a name="microsoft-graph-connectors-preview-release-and-features"></a>Предварительный выпуск и функции Microsoft Graph Connectors Preview

Microsoft Graph Connectors и API службы поиска, как правило, доступны в настоящее время. Первоначальное развертывание будет выполняться для клиентов, настроенных для целевого выпуска. После развертывания на все клиенты, использование квоты индекса из контента соединителей будет подвергаться выставлению счетов. Для получения дополнительных сведений см. [требования и цены лицензирования](licensing.md) .

## <a name="set-up-targeted-release"></a>Настройка целевого выпуска

Если вы хотите использовать соединители Graph в клиенте во время развертывания, необходимо отказаться от целевого выпуска. Чтобы узнать больше о параметрах целевого выпуска и способах его установки, ознакомьтесь [со статьей Настройка стандартных или целевых вариантов выпуска в Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).

## <a name="preview-features"></a>Предварительные версии функций

Несмотря на то, что Microsoft Graph Connectors и API службы поиска Майкрософт теперь доступны, существует несколько функций, которые будут сохранены в предварительной версии.

Набор соединителей и функций в предварительной версии включает:

* [Соединитель Azure DevOps](azure-devops-connector.md)
* [Соединитель Salesforce](salesforce-connector.md)
* [Соединитель ServiceNow](servicenow.md) с разрешениями поиска, использующими исходные списки ACL
* [Управление кластером результатов](result-cluster.md)