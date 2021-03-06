---
title: Соединитель MediaWiki Graph для microsoft Search
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
description: Настройка соединитетеля MediaWiki Graph для поиска в Microsoft Search
ms.openlocfilehash: 1c2908de859056ccb26b862820e8b3be7a158569
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508772"
---
<!---Previous ms.author: monaray --->

# <a name="mediawiki-graph-connector"></a><span data-ttu-id="984a5-103">Соединитель MediaWiki Graph</span><span class="sxs-lookup"><span data-stu-id="984a5-103">MediaWiki Graph connector</span></span>

<span data-ttu-id="984a5-104">Соединитель MediaWiki Graph позволяет организации обнаруживть и индексировать данные из вики-сайта, созданного с помощью программного обеспечения MediaWiki.</span><span class="sxs-lookup"><span data-stu-id="984a5-104">The MediaWiki Graph connector allows your organization to discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="984a5-105">Этот соединитатель индексирует указанное содержимое в Microsoft Search и поддерживает периодические обходы, чтобы поддерживать индекс в курсе.</span><span class="sxs-lookup"><span data-stu-id="984a5-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

> [!NOTE]
> <span data-ttu-id="984a5-106">Ознакомьтесь [**с статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общие инструкции по настройке соединитений Graph.</span><span class="sxs-lookup"><span data-stu-id="984a5-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="984a5-107">Эта статья для всех, кто настраивает, запускает и контролирует соединитель Диаграммы MediaWiki.</span><span class="sxs-lookup"><span data-stu-id="984a5-107">This article is for anyone who configures, runs, and monitors a MediaWiki Graph connector.</span></span> <span data-ttu-id="984a5-108">Он дополняет общий процесс установки и показывает инструкции, применимые только к соединитеку MediaWiki Graph.</span><span class="sxs-lookup"><span data-stu-id="984a5-108">It supplements the general setup process, and shows instructions that apply only for the MediaWiki Graph connector.</span></span> <span data-ttu-id="984a5-109">В этой статье также содержатся сведения об [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="984a5-109">This article also includes information about [Limitations](#limitations).</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="984a5-110">Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="984a5-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="984a5-111">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="984a5-111">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="984a5-112">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="984a5-112">Step 2: Name the connection</span></span>

<span data-ttu-id="984a5-113">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="984a5-113">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="984a5-114">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="984a5-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="984a5-115">Введите **URL-адрес вики** и выберите **тип** проверки подлинности из выпадаемого меню параметров.</span><span class="sxs-lookup"><span data-stu-id="984a5-115">Enter your **Wiki URL** and choose the **Authentication type** from the drop-down menu of options.</span></span> <span data-ttu-id="984a5-116">Параметры **None,** **Basic** и **OAuth 2.0 AAD**.</span><span class="sxs-lookup"><span data-stu-id="984a5-116">The options are **None**, **Basic**, and **OAuth 2.0 AAD**.</span></span>

<span data-ttu-id="984a5-117">Если вы **выбираете Basic** в качестве типа проверки подлинности, вам потребуется предоставить имя пользователя и пароль для вики.  </span><span class="sxs-lookup"><span data-stu-id="984a5-117">If you choose **Basic** as the Authentication type, you will need to provide the **Username** and **Password** for the wiki.</span></span>

<span data-ttu-id="984a5-118">Если вы выбрали **AAD OAuth 2.0** в качестве типа  проверки подлинности, необходимо предоставить идентификацию ресурса вики-установки.</span><span class="sxs-lookup"><span data-stu-id="984a5-118">If you choose **OAuth 2.0 AAD** as the Authentication type, you will need to provide the **Resource ID** of the wiki installation.</span></span> <span data-ttu-id="984a5-119">Кроме того, необходимо предоставить секретный  **номер клиента** и клиент, созданный на странице регистрации приложений AAD.</span><span class="sxs-lookup"><span data-stu-id="984a5-119">You will also need to provide the **Client ID** and **Client secret** generated on the AAD Application registration page.</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="984a5-120">Шаг 4. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="984a5-120">Step 4: Manage search permissions</span></span>

<span data-ttu-id="984a5-121">Соединитель MediaWiki поддерживает только разрешения поиска, видимые **каждому.**</span><span class="sxs-lookup"><span data-stu-id="984a5-121">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="984a5-122">Индексные данные появляются в результатах поиска и видны всем пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="984a5-122">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="984a5-123">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="984a5-123">Step 5: Assign property labels</span></span>

<span data-ttu-id="984a5-124">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="984a5-124">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a><span data-ttu-id="984a5-125">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="984a5-125">Step 6: Manage schema</span></span>

<span data-ttu-id="984a5-126">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="984a5-126">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="984a5-127">Шаг 7. Выбор параметров обновления</span><span class="sxs-lookup"><span data-stu-id="984a5-127">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="984a5-128">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="984a5-128">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a><span data-ttu-id="984a5-129">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="984a5-129">Step 8: Review connection</span></span>

<span data-ttu-id="984a5-130">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="984a5-130">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a><span data-ttu-id="984a5-131">Ограничения</span><span class="sxs-lookup"><span data-stu-id="984a5-131">Limitations</span></span>

<span data-ttu-id="984a5-132">Соединитель MediaWiki имеет эти ограничения в выпуске предварительного просмотра:</span><span class="sxs-lookup"><span data-stu-id="984a5-132">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="984a5-133">Поддерживает только облачные вики.</span><span class="sxs-lookup"><span data-stu-id="984a5-133">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="984a5-134">Поддерживает только Basic или OAuth 2.0 с помощью Azure Active Directory или Проверки подлинности Azure.</span><span class="sxs-lookup"><span data-stu-id="984a5-134">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="984a5-135">Не поддерживает выбор пространства имен для индексации.</span><span class="sxs-lookup"><span data-stu-id="984a5-135">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="984a5-136">Индексирует только пространства имен Main, Category и File.</span><span class="sxs-lookup"><span data-stu-id="984a5-136">Indexes only Main, Category, and File namespaces.</span></span>
* <span data-ttu-id="984a5-137">Не поддерживает списки управления доступом (ACLs).</span><span class="sxs-lookup"><span data-stu-id="984a5-137">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="984a5-138">Таким образом, индексные страницы видны всем пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="984a5-138">Thus, indexed pages are visible to all users in the organization.</span></span>
