---
title: Соединитель MediaWiki для Поиска (Майкрософт)
ms.author: monaray
author: monaray97
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединители MediaWiki для Поиска (Майкрософт)
ms.openlocfilehash: 7a22fcc84f6f435bf438aa027c42c76eb8be1eaf
ms.sourcegitcommit: 39bf9f0db7f9bff2ab82c99a059b0ddcf1c98f5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/19/2021
ms.locfileid: "49905958"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="1b9a9-103">Соединитель MediaWiki</span><span class="sxs-lookup"><span data-stu-id="1b9a9-103">MediaWiki connector</span></span>

<span data-ttu-id="1b9a9-104">С помощью соединители MediaWiki ваша организация может обнаруживировать и индексировать данные из вики-сайта, созданного с помощью программного обеспечения MediaWiki.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="1b9a9-105">Этот соединитатель индексирует указанный контент в Поиск (Майкрософт) и поддерживает периодические обходы контента для поддержания индекса в оперативном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="1b9a9-106">Эта статья для администраторов Microsoft 365 или всех, кто настраивает, запускает и отслеживает соединитель MediaWiki Graph.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki Graph connector.</span></span> <span data-ttu-id="1b9a9-107">Он дополняет общие инструкции, которые предоставляются в статье ["Настройка соединители Graph".](configure-connector.md)</span><span class="sxs-lookup"><span data-stu-id="1b9a9-107">It supplements the general instructions provided in the [Set up your Graph connector](configure-connector.md) article.</span></span> <span data-ttu-id="1b9a9-108">Если это еще не сделано, прочитайте всю статью "Настройка соединители Graph", чтобы ознакомиться с общим процессом настройки.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-108">If you have not already done so, read the entire Set up your Graph connector article to understand the general setup process.</span></span>

<span data-ttu-id="1b9a9-109">Каждый этап процесса установки приведен ниже вместе с примечанием, которое указывает, что необходимо следовать общим инструкциям по настройке или другим инструкциям, которые применяются только к соединитетелям MediaWiki Graph.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-109">Each step in the setup process is listed below along with either a note that indicates you should follow the general setup instructions OR other instructions that apply to only MediaWiki Graph connectors.</span></span> <span data-ttu-id="1b9a9-110">В этой статье также содержатся сведения [об](#limitations) ограничениях для соединители MediaWiki Graph.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-110">This article also includes information about [Limitations](#limitations) for MediaWiki Graph connectors.</span></span> 

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="1b9a9-111">Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-111">Step 1: Add a Graph connector in the Microsoft 365 admin center.</span></span>
<span data-ttu-id="1b9a9-112">Следуйте общим инструкциям по настройке.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-112">Follow the general setup instructions.</span></span>

## <a name="step-2-name-the-connection"></a><span data-ttu-id="1b9a9-113">Шаг 2. Имя подключения.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-113">Step 2: Name the connection.</span></span>
<span data-ttu-id="1b9a9-114">Следуйте общим инструкциям по настройке.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-114">Follow the general setup instructions.</span></span>
 
## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="1b9a9-115">Шаг 3. Настройте параметры подключения.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-115">Step 3: Configure the connection settings.</span></span>
<span data-ttu-id="1b9a9-116">Введите **URL-адрес вики-сайта** и выберите тип проверки подлинности в меню параметров. </span><span class="sxs-lookup"><span data-stu-id="1b9a9-116">Enter your **Wiki URL** and choose the **Authentication type** from the drop-down menu of options.</span></span> <span data-ttu-id="1b9a9-117">Возможные варианты: **None,** **Basic** и **OAuth 2.0 AAD.**</span><span class="sxs-lookup"><span data-stu-id="1b9a9-117">The options are **None**, **Basic**, and **OAuth 2.0 AAD**.</span></span>

<span data-ttu-id="1b9a9-118">If you choose **Basic** as the Authentication type, you will need to provide the **Username** and **Password** for the wiki.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-118">If you choose **Basic** as the Authentication type, you will need to provide the **Username** and **Password** for the wiki.</span></span>

<span data-ttu-id="1b9a9-119">Если вы выберете **AAD OAuth 2.0** в качестве типа  проверки подлинности, вам потребуется предоставить ИД ресурса вики-установки.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-119">If you choose **OAuth 2.0 AAD** as the Authentication type, you will need to provide the **Resource ID** of the wiki installation.</span></span> <span data-ttu-id="1b9a9-120">Вам также потребуется предоставить **ИД**  клиента и секрет клиента, созданные на странице регистрации приложения AAD.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-120">You will also need to provide the **Client ID** and **Client secret** generated on the AAD Application registration page.</span></span> 

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="1b9a9-121">Шаг 4. Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="1b9a9-121">Step 4: Manage search permissions</span></span>
<span data-ttu-id="1b9a9-122">Соединитель MediaWiki поддерживает только разрешения поиска, видимые **всем.**</span><span class="sxs-lookup"><span data-stu-id="1b9a9-122">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="1b9a9-123">Индексные данные появляются в результатах поиска и видны всем пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-123">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="1b9a9-124">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="1b9a9-124">Step 5: Assign property labels</span></span>
<span data-ttu-id="1b9a9-125">Следуйте общим инструкциям по настройке.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-125">Follow the general setup instructions.</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="1b9a9-126">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="1b9a9-126">Step 6: Manage schema</span></span>
<span data-ttu-id="1b9a9-127">Следуйте общим инструкциям по настройке.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-127">Follow the general setup instructions.</span></span>

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="1b9a9-128">Шаг 7. Выбор параметров обновления</span><span class="sxs-lookup"><span data-stu-id="1b9a9-128">Step 7: Choose refresh settings</span></span>
<span data-ttu-id="1b9a9-129">Следуйте общим инструкциям по настройке.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-129">Follow the general setup instructions.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="1b9a9-130">Шаг 8. Проверка подключения</span><span class="sxs-lookup"><span data-stu-id="1b9a9-130">Step 8: Review connection</span></span>
<span data-ttu-id="1b9a9-131">Следуйте общим инструкциям по настройке.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-131">Follow the general setup instructions.</span></span>

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a><span data-ttu-id="1b9a9-132">Ограничения</span><span class="sxs-lookup"><span data-stu-id="1b9a9-132">Limitations</span></span>
<span data-ttu-id="1b9a9-133">Соединитель MediaWiki имеет указанные в предварительном выпуске ограничения:</span><span class="sxs-lookup"><span data-stu-id="1b9a9-133">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="1b9a9-134">Поддерживает только облачные вики-сайты.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-134">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="1b9a9-135">Поддерживает только Базовый или OAuth 2.0 с проверкой подлинности Azure Active Directory или Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-135">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="1b9a9-136">Не поддерживает выделение пространства имен для индексации.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-136">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="1b9a9-137">Индексирует только пространства имен Main, Category и File.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-137">Indexes only Main, Category, and File namespaces.</span></span>
* <span data-ttu-id="1b9a9-138">Не поддерживает списки управления доступом (ALS).</span><span class="sxs-lookup"><span data-stu-id="1b9a9-138">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="1b9a9-139">Таким образом, индексные страницы видны всем пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-139">Thus, indexed pages are visible to all users in the organization.</span></span>
