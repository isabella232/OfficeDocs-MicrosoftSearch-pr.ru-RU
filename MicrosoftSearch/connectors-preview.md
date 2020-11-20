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
# <a name="microsoft-graph-connectors-preview-release-and-features"></a><span data-ttu-id="7c167-103">Предварительный выпуск и функции Microsoft Graph Connectors Preview</span><span class="sxs-lookup"><span data-stu-id="7c167-103">Microsoft Graph connectors preview release and features</span></span>

<span data-ttu-id="7c167-104">Microsoft Graph Connectors и API службы поиска, как правило, доступны в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="7c167-104">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="7c167-105">Первоначальное развертывание будет выполняться для клиентов, настроенных для целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="7c167-105">The initial rollout will be to customers configured for Targeted Release.</span></span> <span data-ttu-id="7c167-106">После развертывания на все клиенты, использование квоты индекса из контента соединителей будет подвергаться выставлению счетов.</span><span class="sxs-lookup"><span data-stu-id="7c167-106">Upon rollout completion to all tenants, index quota utilization from connectors content will become subject to billing.</span></span> <span data-ttu-id="7c167-107">Для получения дополнительных сведений см. [требования и цены лицензирования](licensing.md) .</span><span class="sxs-lookup"><span data-stu-id="7c167-107">See [Licensing requirements and pricing](licensing.md) for more information.</span></span>

## <a name="set-up-targeted-release"></a><span data-ttu-id="7c167-108">Настройка целевого выпуска</span><span class="sxs-lookup"><span data-stu-id="7c167-108">Set up Targeted release</span></span>

<span data-ttu-id="7c167-109">Если вы хотите использовать соединители Graph в клиенте во время развертывания, необходимо отказаться от целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="7c167-109">If you want to use Graph connectors in your tenant during rollout, you must opt into Targeted release.</span></span> <span data-ttu-id="7c167-110">Чтобы узнать больше о параметрах целевого выпуска и способах его установки, ознакомьтесь [со статьей Настройка стандартных или целевых вариантов выпуска в Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="7c167-110">To learn more about the Targeted release option and how to set it, see [Set up the Standard or Targeted release options in Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span></span>

## <a name="preview-features"></a><span data-ttu-id="7c167-111">Предварительные версии функций</span><span class="sxs-lookup"><span data-stu-id="7c167-111">Preview features</span></span>

<span data-ttu-id="7c167-112">Несмотря на то, что Microsoft Graph Connectors и API службы поиска Майкрософт теперь доступны, существует несколько функций, которые будут сохранены в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="7c167-112">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that will remain in preview.</span></span>

<span data-ttu-id="7c167-113">Набор соединителей и функций в предварительной версии включает:</span><span class="sxs-lookup"><span data-stu-id="7c167-113">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="7c167-114">Соединитель Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="7c167-114">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="7c167-115">Соединитель Salesforce</span><span class="sxs-lookup"><span data-stu-id="7c167-115">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="7c167-116">[Соединитель ServiceNow](servicenow.md) с разрешениями поиска, использующими исходные списки ACL</span><span class="sxs-lookup"><span data-stu-id="7c167-116">[ServiceNow connector](servicenow.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="7c167-117">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="7c167-117">Manage result cluster</span></span>](result-cluster.md)