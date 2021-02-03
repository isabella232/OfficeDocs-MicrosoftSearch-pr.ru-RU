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

# <a name="mediawiki-graph-connector"></a><span data-ttu-id="0f1ec-103">Соединитель MediaWiki Graph</span><span class="sxs-lookup"><span data-stu-id="0f1ec-103">MediaWiki Graph connector</span></span>

<span data-ttu-id="0f1ec-104">Соединитель MediaWiki Graph позволяет организации обнаруживировать и индексировать данные из вики-сайта, созданного с помощью программного обеспечения MediaWiki.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-104">The MediaWiki Graph connector allows your organization to discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="0f1ec-105">Этот соединитатель индексирует указанный контент в Поиск (Майкрософт) и поддерживает периодические обходы для поддержания индекса в курсе.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

> [!NOTE]
> <span data-ttu-id="0f1ec-106">Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="0f1ec-107">Эта статья для всех, кто настраивает, запускает и отслеживает соединители ServiceNow Graph.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-107">This article is for anyone who configures, runs, and monitors a ServiceNow Graph connector.</span></span> <span data-ttu-id="0f1ec-108">Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединитеструктору MediaWiki Graph.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-108">It supplements the general setup process, and shows instructions that apply only for the MediaWiki Graph connector.</span></span> <span data-ttu-id="0f1ec-109">В этой статье также содержатся сведения об [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="0f1ec-109">This article also includes information about [Limitations](#limitations).</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="0f1ec-110">Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0f1ec-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="0f1ec-111">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="0f1ec-111">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="0f1ec-112">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="0f1ec-112">Step 2: Name the connection</span></span>

<span data-ttu-id="0f1ec-113">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="0f1ec-113">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="0f1ec-114">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="0f1ec-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="0f1ec-115">Введите **URL-адрес вики-сайта** и выберите тип проверки подлинности в выпадаемом меню параметров. </span><span class="sxs-lookup"><span data-stu-id="0f1ec-115">Enter your **Wiki URL** and choose the **Authentication type** from the drop-down menu of options.</span></span> <span data-ttu-id="0f1ec-116">Возможные варианты: **None,** **Basic** и **OAuth 2.0 AAD.**</span><span class="sxs-lookup"><span data-stu-id="0f1ec-116">The options are **None**, **Basic**, and **OAuth 2.0 AAD**.</span></span>

<span data-ttu-id="0f1ec-117">Если в **качестве** типа проверки подлинности вы  выберете "Базовый", необходимо ввести имя пользователя и пароль **для** вики-сайта.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-117">If you choose **Basic** as the Authentication type, you will need to provide the **Username** and **Password** for the wiki.</span></span>

<span data-ttu-id="0f1ec-118">Если в качестве типа проверки подлинности вы выбрали **AAD OAuth 2.0,** необходимо предоставить ИД ресурса для вики-установки. </span><span class="sxs-lookup"><span data-stu-id="0f1ec-118">If you choose **OAuth 2.0 AAD** as the Authentication type, you will need to provide the **Resource ID** of the wiki installation.</span></span> <span data-ttu-id="0f1ec-119">Вам также потребуется предоставить **ИД**  клиента и секрет клиента, созданные на странице регистрации приложения AAD.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-119">You will also need to provide the **Client ID** and **Client secret** generated on the AAD Application registration page.</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="0f1ec-120">Шаг 4. Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="0f1ec-120">Step 4: Manage search permissions</span></span>

<span data-ttu-id="0f1ec-121">Соединитель MediaWiki поддерживает только разрешения поиска, видимые **всем.**</span><span class="sxs-lookup"><span data-stu-id="0f1ec-121">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="0f1ec-122">Индексные данные появляются в результатах поиска и видны всем пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-122">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="0f1ec-123">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="0f1ec-123">Step 5: Assign property labels</span></span>

<span data-ttu-id="0f1ec-124">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="0f1ec-124">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a><span data-ttu-id="0f1ec-125">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="0f1ec-125">Step 6: Manage schema</span></span>

<span data-ttu-id="0f1ec-126">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="0f1ec-126">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="0f1ec-127">Шаг 7. Выбор параметров обновления</span><span class="sxs-lookup"><span data-stu-id="0f1ec-127">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="0f1ec-128">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="0f1ec-128">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a><span data-ttu-id="0f1ec-129">Шаг 8. Проверка подключения</span><span class="sxs-lookup"><span data-stu-id="0f1ec-129">Step 8: Review connection</span></span>

<span data-ttu-id="0f1ec-130">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="0f1ec-130">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a><span data-ttu-id="0f1ec-131">Ограничения</span><span class="sxs-lookup"><span data-stu-id="0f1ec-131">Limitations</span></span>

<span data-ttu-id="0f1ec-132">Соединитель MediaWiki имеет указанные в предварительной версии ограничения:</span><span class="sxs-lookup"><span data-stu-id="0f1ec-132">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="0f1ec-133">Поддерживает только облачные вики-сайты.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-133">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="0f1ec-134">Поддерживает только Базовый или OAuth 2.0 с проверкой подлинности Azure Active Directory или Azure.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-134">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="0f1ec-135">Не поддерживает выделение пространства имен для индексации.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-135">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="0f1ec-136">Индексирует только пространства имен Main, Category и File.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-136">Indexes only Main, Category, and File namespaces.</span></span>
* <span data-ttu-id="0f1ec-137">Не поддерживает списки управления доступом (ALS).</span><span class="sxs-lookup"><span data-stu-id="0f1ec-137">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="0f1ec-138">Таким образом, индексные страницы видны всем пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-138">Thus, indexed pages are visible to all users in the organization.</span></span>
