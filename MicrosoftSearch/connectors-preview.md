---
title: Предварительный просмотр соединители
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
description: Узнайте о предварительной версии соединители Microsoft Graph для Поиска (Майкрософт).
ms.openlocfilehash: 47f7e1e417222c948f2916c70626278f9fe5b44a
ms.sourcegitcommit: 469be70ad295a5837978d75babf5243115257f77
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/13/2021
ms.locfileid: "49847513"
---
# <a name="microsoft-graph-connectors-preview-release-and-features"></a><span data-ttu-id="4eff6-103">Предварительный выпуск и функции соединители Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="4eff6-103">Microsoft Graph connectors preview release and features</span></span>

<span data-ttu-id="4eff6-104">Теперь соединители Microsoft Graph и API Поиска (Майкрософт) доступны в целом.</span><span class="sxs-lookup"><span data-stu-id="4eff6-104">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="4eff6-105">Первоначальное выпуск будет для клиентов, настроенных для целевого выпуска.</span><span class="sxs-lookup"><span data-stu-id="4eff6-105">The initial rollout will be to customers configured for Targeted Release.</span></span> <span data-ttu-id="4eff6-106">Это будет происходить до конца февраля 2021 г.</span><span class="sxs-lookup"><span data-stu-id="4eff6-106">This rollout will go on until the end of February 2021.</span></span> <span data-ttu-id="4eff6-107">После завершения вывоза для всех клиентов использование квоты индекса из контента соединителя станет предметом вы выставления счета.</span><span class="sxs-lookup"><span data-stu-id="4eff6-107">Upon rollout completion to all tenants, index quota utilization from connectors content will become subject to billing.</span></span> <span data-ttu-id="4eff6-108">Дополнительные [сведения см. в требованиях](licensing.md) к лицензированию и ценах.</span><span class="sxs-lookup"><span data-stu-id="4eff6-108">See [Licensing requirements and pricing](licensing.md) for more information.</span></span>

## <a name="set-up-targeted-release"></a><span data-ttu-id="4eff6-109">Настройка выпуска Targeted</span><span class="sxs-lookup"><span data-stu-id="4eff6-109">Set up Targeted release</span></span>

<span data-ttu-id="4eff6-110">Если вы хотите использовать соединители Graph в клиенте во время выпуска, **необходимо** выбрать выпуск Targeted.</span><span class="sxs-lookup"><span data-stu-id="4eff6-110">If you want to use Graph connectors in your tenant during rollout, you **must** opt into Targeted release.</span></span> <span data-ttu-id="4eff6-111">Дополнительные информацию о выпуске Targeted и его настройках см. в подстройки "Настройка стандартных или целевых [выпусков" в Office 365.](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="4eff6-111">To learn more about the Targeted release option and how to set it, see [Set up the Standard or Targeted release options in Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true).</span></span>

## <a name="preview-features"></a><span data-ttu-id="4eff6-112">Предварительные версии функций</span><span class="sxs-lookup"><span data-stu-id="4eff6-112">Preview features</span></span>

<span data-ttu-id="4eff6-113">Хотя соединители Microsoft Graph и API Поиска (Майкрософт) теперь доступны в целом, существует несколько функций, которые останутся в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="4eff6-113">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that will remain in preview.</span></span>

<span data-ttu-id="4eff6-114">Набор соединители и функции в предварительной версии включают:</span><span class="sxs-lookup"><span data-stu-id="4eff6-114">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="4eff6-115">Соединителю Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="4eff6-115">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="4eff6-116">Соединители Salesforce</span><span class="sxs-lookup"><span data-stu-id="4eff6-116">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="4eff6-117">[Соединитель ServiceNow с](servicenow-connector.md) разрешениями поиска, использующем исходные ALS</span><span class="sxs-lookup"><span data-stu-id="4eff6-117">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="4eff6-118">Управление кластером результатов</span><span class="sxs-lookup"><span data-stu-id="4eff6-118">Manage result cluster</span></span>](result-cluster.md)