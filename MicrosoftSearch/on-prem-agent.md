---
title: Локальный агент
ms.author: rusamai
author: rsamai
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NoIndex
description: Локальный агент
ms.openlocfilehash: 487c5b179e09fd99fa26ae7a237e89ca38b7be4d
ms.sourcegitcommit: 69a1c544cc8db364991cb58d7818d7158ff108b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "49408945"
---
# <a name="on-prem-agent"></a><span data-ttu-id="16bf1-103">Локальный агент</span><span class="sxs-lookup"><span data-stu-id="16bf1-103">On-Prem Agent</span></span>

## <a name="graph-connector-agent"></a><span data-ttu-id="16bf1-104">Агент соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="16bf1-104">Graph connector agent</span></span>

<span data-ttu-id="16bf1-105">Локальные графические соединители требуют установки программного обеспечения *агента Graph Connector* .</span><span class="sxs-lookup"><span data-stu-id="16bf1-105">On-prem Graph connectors require you to install *Graph connector agent* software.</span></span> <span data-ttu-id="16bf1-106">Он обеспечивает быструю и безопасную передачу данных между локальными данными и облачными службами.</span><span class="sxs-lookup"><span data-stu-id="16bf1-106">It allows quick and secure data transfer between on-premises data and cloud services.</span></span> <span data-ttu-id="16bf1-107">В этой статье описывается процесс установки и настройки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="16bf1-107">This article guides you through the steps of installing and configuring the software.</span></span> <span data-ttu-id="16bf1-108">После настройки он будет доступен для создания подключений к локальным источникам данных из [центра администрирования Microsoft 365](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="16bf1-108">Once configured, it will be available for creating connections to your on-prem data sources from the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

## <a name="installation"></a><span data-ttu-id="16bf1-109">Установка</span><span class="sxs-lookup"><span data-stu-id="16bf1-109">Installation</span></span>

<span data-ttu-id="16bf1-110">Скачайте последнюю версию агента Graph Connector с помощью [этой ссылки](https://download.microsoft.com/download/d/d/e/dde18236-9c67-437d-a864-894a0a888ef2/AgentPackage.msi) и установите программное обеспечение с помощью мастера установки.</span><span class="sxs-lookup"><span data-stu-id="16bf1-110">Download the latest version of Graph connector agent using [this link](https://download.microsoft.com/download/d/d/e/dde18236-9c67-437d-a864-894a0a888ef2/AgentPackage.msi) and install the software using the installation wizard.</span></span> <span data-ttu-id="16bf1-111">В соответствии с рекомендуемой конфигурацией компьютера это программное обеспечение может беспрепятственно обрабатывать до трех подключений.</span><span class="sxs-lookup"><span data-stu-id="16bf1-111">With the recommended configuration of the machine described below, the software can seamlessly handle up to three connections.</span></span> <span data-ttu-id="16bf1-112">Все последующие подключения могут привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="16bf1-112">Any connections beyond that might degrade the performance.</span></span>

<span data-ttu-id="16bf1-113">Рекомендуемая конфигурация:</span><span class="sxs-lookup"><span data-stu-id="16bf1-113">Recommended configuration:</span></span>

* <span data-ttu-id="16bf1-114">Windows 10, Windows Server 2012 R2 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="16bf1-114">Windows 10, Windows Server 2012 R2 and above</span></span>
* <span data-ttu-id="16bf1-115">8 ядер, 3GHz</span><span class="sxs-lookup"><span data-stu-id="16bf1-115">8 cores, 3GHz</span></span>
* <span data-ttu-id="16bf1-116">16 ГБ ОЗУ, 1 ГБ дискового пространства</span><span class="sxs-lookup"><span data-stu-id="16bf1-116">16GB RAM, 1GB Disk Space</span></span>
* <span data-ttu-id="16bf1-117">Сетевой доступ к источнику данных и Интернету через 443</span><span class="sxs-lookup"><span data-stu-id="16bf1-117">Network access to data source and internet through 443</span></span>

## <a name="creating-app-for-the-agent"></a><span data-ttu-id="16bf1-118">Создание приложения для агента</span><span class="sxs-lookup"><span data-stu-id="16bf1-118">Creating App for the agent</span></span>  

<span data-ttu-id="16bf1-119">Перед созданием подключений экземпляру агента необходимо выполнить подачу нескольких критических параметров.</span><span class="sxs-lookup"><span data-stu-id="16bf1-119">The agent instance needs to be fed few critical parameters before you create connections.</span></span> <span data-ttu-id="16bf1-120">Эти параметры включают сведения о проверке подлинности, необходимые для использования API приема графа.</span><span class="sxs-lookup"><span data-stu-id="16bf1-120">These parameters include authentication details required for using Graph ingestion APIs.</span></span>  

<span data-ttu-id="16bf1-121">Действия по созданию приложения для агента.</span><span class="sxs-lookup"><span data-stu-id="16bf1-121">Steps for creating App for the agent.</span></span>

1. <span data-ttu-id="16bf1-122">Перейдите на [портал Azure](https://portal.azure.com) и войдите в систему, используя учетные данные администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="16bf1-122">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="16bf1-123">Перейдите к разделу Регистрация приложений **Azure Active Directory** в  ->  **App registrations** области навигации и нажмите кнопку **создать регистрацию**.</span><span class="sxs-lookup"><span data-stu-id="16bf1-123">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>
3. <span data-ttu-id="16bf1-124">Укажите имя приложения и нажмите кнопку **регистр**.</span><span class="sxs-lookup"><span data-stu-id="16bf1-124">Provide a name for the app and select **Register**.</span></span>
4. <span data-ttu-id="16bf1-125">Запишите идентификатор приложения (клиента).</span><span class="sxs-lookup"><span data-stu-id="16bf1-125">Make a note of the Application (client) ID.</span></span>
5. <span data-ttu-id="16bf1-126">Откройте **разрешения на доступ к API** в области навигации и выберите **Добавить разрешение**.</span><span class="sxs-lookup"><span data-stu-id="16bf1-126">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>
6. <span data-ttu-id="16bf1-127">Выберите **Microsoft Graph** , а затем — **разрешения приложений**.</span><span class="sxs-lookup"><span data-stu-id="16bf1-127">Select **Microsoft Graph** and then **Application permissions**.</span></span>
7. <span data-ttu-id="16bf1-128">Выполните поиск по запросу "Екстерналитем. ReadWrite. ALL" и "Directory. Read. ALL" в разделе разрешения и выберите команду **Добавить разрешения**.</span><span class="sxs-lookup"><span data-stu-id="16bf1-128">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>
8. <span data-ttu-id="16bf1-129">Выберите параметр **предоставить согласие администратора для [TenantName]** и подтвердите, нажав **кнопку Да**.</span><span class="sxs-lookup"><span data-stu-id="16bf1-129">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>
9. <span data-ttu-id="16bf1-130">Убедитесь, что разрешения находятся в состоянии "предоставлено".</span><span class="sxs-lookup"><span data-stu-id="16bf1-130">Check that the permissions are in the granted state.</span></span>
     <span data-ttu-id="16bf1-131">![Разрешения, отображаемые в столбце "зеленый" в правой части.](media/onprem-agent/granted-state.png)</span><span class="sxs-lookup"><span data-stu-id="16bf1-131">![Permissions shown as granted in green on right hand column.](media/onprem-agent/granted-state.png)</span></span>

## <a name="configuring-graph-connector-agent"></a><span data-ttu-id="16bf1-132">Настройка агента соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="16bf1-132">Configuring Graph connector agent</span></span>

<span data-ttu-id="16bf1-133">После создания приложения для агента необходимо настроить агент с использованием соответствующих сведений о проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="16bf1-133">Once you have created the App for the agent, you must configure the agent with appropriate authentication details.</span></span>

<span data-ttu-id="16bf1-134">Сведения о проверке подлинности могут быть предоставлены в одной из следующих форм.</span><span class="sxs-lookup"><span data-stu-id="16bf1-134">Authentication details can be provided in one of the following forms.</span></span>

### <a name="configuring-the-client-secret-for-authentication"></a><span data-ttu-id="16bf1-135">Настройка секрета клиента для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="16bf1-135">Configuring the client secret for authentication</span></span>

1. <span data-ttu-id="16bf1-136">Перейдите на [портал Azure](https://portal.azure.com) и войдите в систему, используя учетные данные администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="16bf1-136">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="16bf1-137">Откройте **регистрацию приложений** в области навигации и перейдите к соответствующему приложению.</span><span class="sxs-lookup"><span data-stu-id="16bf1-137">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="16bf1-138">В разделе **Управление** выберите **Сертификаты и секреты**.</span><span class="sxs-lookup"><span data-stu-id="16bf1-138">Under **Manage**, select **Certificates and secrets**.</span></span>
3. <span data-ttu-id="16bf1-139">Выберите **новый секрет клиента** и выберите срок действия секрета.</span><span class="sxs-lookup"><span data-stu-id="16bf1-139">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="16bf1-140">Скопируйте созданный секрет и сохраните его, так как он больше не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="16bf1-140">Copy the generated secret and save it because it will not be shown again.</span></span>
4. <span data-ttu-id="16bf1-141">Используйте этот секрет клиента вместе с ИДЕНТИФИКАТОРом приложения, чтобы настроить агент.</span><span class="sxs-lookup"><span data-stu-id="16bf1-141">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="16bf1-142">Не используйте в поле **имя** агента пробелы.</span><span class="sxs-lookup"><span data-stu-id="16bf1-142">Do not use any blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="16bf1-143">Принимаются буквенно-цифровые символы.</span><span class="sxs-lookup"><span data-stu-id="16bf1-143">Alpha numeric characters are accepted.</span></span>

## <a name="using-thumbprint-certificate-for-authentication"></a><span data-ttu-id="16bf1-144">Использование сертификата отпечатков для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="16bf1-144">Using thumbprint certificate for authentication</span></span>

<span data-ttu-id="16bf1-145">Если вы уже настроили сведения для проверки подлинности, выполнив [настройку секрета клиента для проверки подлинности](#configuring-the-client-secret-for-authentication) , вы можете перейти непосредственно к [обзору программы установки](configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="16bf1-145">If you have already configured the authentication details by following [Configuring the client secret for authentication](#configuring-the-client-secret-for-authentication) , then you can jump directly to [Setup overview](configure-connector.md).</span></span>

1. <span data-ttu-id="16bf1-146">Откройте **регистрацию приложения** и выберите **Сертификаты и секреты** в области навигации.</span><span class="sxs-lookup"><span data-stu-id="16bf1-146">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="16bf1-147">Скопируйте отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="16bf1-147">Copy the certificate thumbprint.</span></span>
<span data-ttu-id="16bf1-148">![Список сертификатов сумбринт, когда в левой панели выбраны сертификаты и секреты](media/onprem-agent/certificates.png)</span><span class="sxs-lookup"><span data-stu-id="16bf1-148">![List of thumbrint certificates when Certificates and secrets is selected in the left pane](media/onprem-agent/certificates.png)</span></span>
2. <span data-ttu-id="16bf1-149">Чтобы зарегистрировать агент соединителя Graph, используйте секрет клиента или отпечаток.</span><span class="sxs-lookup"><span data-stu-id="16bf1-149">Use either the client secret or thumbprint to register the Graph connector agent.</span></span>
<span data-ttu-id="16bf1-150">![Регистрация формы с запросом имени, идентификатора приложения, типа учетных данных и сертификата](media/onprem-agent/register.png)</span><span class="sxs-lookup"><span data-stu-id="16bf1-150">![Register form asking for name, app id, credential type, and certificate](media/onprem-agent/register.png)</span></span>
