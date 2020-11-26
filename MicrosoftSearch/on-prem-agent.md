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
ms.openlocfilehash: 763904f8dd96c5db8b0633e36795443502afe7d0
ms.sourcegitcommit: 0ed8ec8b3c4e0f5f669005081fd8b2219f07b4f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "49420836"
---
# <a name="graph-connector-agent"></a><span data-ttu-id="8534c-103">Агент соединителя Graph</span><span class="sxs-lookup"><span data-stu-id="8534c-103">Graph connector agent</span></span>

<span data-ttu-id="8534c-104">Использование локальных соединителей Graph требует установки программного обеспечения *агента Graph Connector* .</span><span class="sxs-lookup"><span data-stu-id="8534c-104">Using on-prem Graph connectors require you to install *Graph connector agent* software.</span></span> <span data-ttu-id="8534c-105">Обеспечивает безопасную передачу данных между локальными данными и API соединителя Graph.</span><span class="sxs-lookup"><span data-stu-id="8534c-105">It allows for secure data transfer between on-premises data and the Graph connector APIs.</span></span> <span data-ttu-id="8534c-106">В этой статье описывается установка и настройка агента.</span><span class="sxs-lookup"><span data-stu-id="8534c-106">This article guides you through the installing and configuring the agent.</span></span>

## <a name="installation"></a><span data-ttu-id="8534c-107">Установка</span><span class="sxs-lookup"><span data-stu-id="8534c-107">Installation</span></span>

<span data-ttu-id="8534c-108">Скачайте последнюю [версию агента Graph](https://aka.ms/gcadownload) Connector Agent и установите программное обеспечение с помощью мастера установки.</span><span class="sxs-lookup"><span data-stu-id="8534c-108">Download the latest version of Graph connector agent [here](https://aka.ms/gcadownload) and install the software using the installation wizard.</span></span> <span data-ttu-id="8534c-109">В соответствии с рекомендуемой конфигурацией компьютера, описанной ниже, программное обеспечение может обрабатывать до трех подключений.</span><span class="sxs-lookup"><span data-stu-id="8534c-109">Using the recommended configuration of the machine described below, the software can handle up to three connections.</span></span> <span data-ttu-id="8534c-110">Все последующие подключения могут привести к снижению производительности всех подключений в агенте.</span><span class="sxs-lookup"><span data-stu-id="8534c-110">Any connections beyond that might degrade the performance of all connections on the agent.</span></span>

<span data-ttu-id="8534c-111">Рекомендуемая конфигурация:</span><span class="sxs-lookup"><span data-stu-id="8534c-111">Recommended configuration:</span></span>

* <span data-ttu-id="8534c-112">Windows 10, Windows Server 2016 R2 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="8534c-112">Windows 10, Windows Server 2016 R2 and above</span></span>
* <span data-ttu-id="8534c-113">8 ядер, 3 ГГц</span><span class="sxs-lookup"><span data-stu-id="8534c-113">8 cores, 3 GHz</span></span>
* <span data-ttu-id="8534c-114">16 ГБ ОЗУ, 2 ГБ дискового пространства</span><span class="sxs-lookup"><span data-stu-id="8534c-114">16 GB RAM, 2 GB Disk Space</span></span>
* <span data-ttu-id="8534c-115">Сетевой доступ к источнику данных и Интернету через 443</span><span class="sxs-lookup"><span data-stu-id="8534c-115">Network access to data source and internet through 443</span></span>

## <a name="create-and-configure-an-app-for-the-agent"></a><span data-ttu-id="8534c-116">Создание и настройка приложения для агента</span><span class="sxs-lookup"><span data-stu-id="8534c-116">Create and configure an App for the agent</span></span>  

<span data-ttu-id="8534c-117">Перед использованием агента необходимо создать приложение и настроить сведения о проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="8534c-117">Before using the agent, you must create an app and configure the authentication details.</span></span>

### <a name="create-an-app"></a><span data-ttu-id="8534c-118">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="8534c-118">Create an app</span></span>

1. <span data-ttu-id="8534c-119">Перейдите на [портал Azure](https://portal.azure.com) и войдите в систему, используя учетные данные администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="8534c-119">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="8534c-120">Перейдите к разделу Регистрация приложений **Azure Active Directory** в  ->  **App registrations** области навигации и нажмите кнопку **создать регистрацию**.</span><span class="sxs-lookup"><span data-stu-id="8534c-120">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>
3. <span data-ttu-id="8534c-121">Укажите имя приложения и нажмите кнопку **регистр**.</span><span class="sxs-lookup"><span data-stu-id="8534c-121">Provide a name for the app and select **Register**.</span></span>
4. <span data-ttu-id="8534c-122">Запишите идентификатор приложения (клиента).</span><span class="sxs-lookup"><span data-stu-id="8534c-122">Make a note of the Application (client) ID.</span></span>
5. <span data-ttu-id="8534c-123">Откройте **разрешения на доступ к API** в области навигации и выберите **Добавить разрешение**.</span><span class="sxs-lookup"><span data-stu-id="8534c-123">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>
6. <span data-ttu-id="8534c-124">Выберите **Microsoft Graph** , а затем — **разрешения приложений**.</span><span class="sxs-lookup"><span data-stu-id="8534c-124">Select **Microsoft Graph** and then **Application permissions**.</span></span>
7. <span data-ttu-id="8534c-125">Выполните поиск по запросу "Екстерналитем. ReadWrite. ALL" и "Directory. Read. ALL" в разделе разрешения и выберите команду **Добавить разрешения**.</span><span class="sxs-lookup"><span data-stu-id="8534c-125">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>
8. <span data-ttu-id="8534c-126">Выберите параметр **предоставить согласие администратора для [TenantName]** и подтвердите, нажав **кнопку Да**.</span><span class="sxs-lookup"><span data-stu-id="8534c-126">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>
9. <span data-ttu-id="8534c-127">Убедитесь, что разрешения находятся в состоянии "предоставлено".</span><span class="sxs-lookup"><span data-stu-id="8534c-127">Check that the permissions are in the "granted" state.</span></span>
     <span data-ttu-id="8534c-128">![Разрешения, отображаемые в столбце "зеленый" в правой части.](media/onprem-agent/granted-state.png)</span><span class="sxs-lookup"><span data-stu-id="8534c-128">![Permissions shown as granted in green on right hand column.](media/onprem-agent/granted-state.png)</span></span>

### <a name="configure-authentication"></a><span data-ttu-id="8534c-129">Настроить аутентификацию</span><span class="sxs-lookup"><span data-stu-id="8534c-129">Configure Authentication</span></span>

<span data-ttu-id="8534c-130">Сведения о проверке подлинности можно предоставить с помощью секрета клиента или сертификата.</span><span class="sxs-lookup"><span data-stu-id="8534c-130">Authentication details can be provided using a client secret or a certificate.</span></span> <span data-ttu-id="8534c-131">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8534c-131">Follow the steps for your choice.</span></span>

#### <a name="configuring-the-client-secret-for-authentication"></a><span data-ttu-id="8534c-132">Настройка секрета клиента для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8534c-132">Configuring the client secret for authentication</span></span>

1. <span data-ttu-id="8534c-133">Перейдите на [портал Azure](https://portal.azure.com) и войдите в систему, используя учетные данные администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="8534c-133">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="8534c-134">Откройте **регистрацию приложений** в области навигации и перейдите к соответствующему приложению.</span><span class="sxs-lookup"><span data-stu-id="8534c-134">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="8534c-135">В разделе **Управление** выберите **Сертификаты и секреты**.</span><span class="sxs-lookup"><span data-stu-id="8534c-135">Under **Manage**, select **Certificates and secrets**.</span></span>
3. <span data-ttu-id="8534c-136">Выберите **новый секрет клиента** и выберите срок действия секрета.</span><span class="sxs-lookup"><span data-stu-id="8534c-136">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="8534c-137">Скопируйте созданный секрет и сохраните его, так как он больше не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="8534c-137">Copy the generated secret and save it because it won't be shown again.</span></span>
4. <span data-ttu-id="8534c-138">Используйте этот секрет клиента вместе с ИДЕНТИФИКАТОРом приложения, чтобы настроить агент.</span><span class="sxs-lookup"><span data-stu-id="8534c-138">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="8534c-139">В поле **имя** агента нельзя использовать пробелы.</span><span class="sxs-lookup"><span data-stu-id="8534c-139">You cannot use blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="8534c-140">Принимаются буквенно-цифровые символы.</span><span class="sxs-lookup"><span data-stu-id="8534c-140">Alpha numeric characters are accepted.</span></span>

#### <a name="using-a-certificate-for-authentication"></a><span data-ttu-id="8534c-141">Использование сертификата для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8534c-141">Using a certificate for authentication</span></span>

<span data-ttu-id="8534c-142">Использование проверки подлинности на основе сертификатов состоит из трех простых шагов:</span><span class="sxs-lookup"><span data-stu-id="8534c-142">There are three simple steps for using certificate-based authentication:</span></span>

1. <span data-ttu-id="8534c-143">Создание или получение сертификата</span><span class="sxs-lookup"><span data-stu-id="8534c-143">Create or obtain a certificate</span></span>
1. <span data-ttu-id="8534c-144">Отправка сертификата на портал Azure</span><span class="sxs-lookup"><span data-stu-id="8534c-144">Upload the certificate to the Azure portal</span></span>
1. <span data-ttu-id="8534c-145">Назначьте сертификат агенту</span><span class="sxs-lookup"><span data-stu-id="8534c-145">Assign the certificate to the agent</span></span>

##### <a name="step-1-get-a-certificate"></a><span data-ttu-id="8534c-146">Шаг 1: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="8534c-146">Step 1: Get a certificate</span></span>

<span data-ttu-id="8534c-147">Приведенный ниже скрипт можно использовать для создания самозаверяющего сертификата.</span><span class="sxs-lookup"><span data-stu-id="8534c-147">The script below can be used to generate a self-signed certificate.</span></span> <span data-ttu-id="8534c-148">Ваша организация может не разрешать самозаверяющие сертификаты.</span><span class="sxs-lookup"><span data-stu-id="8534c-148">Your organization may not allow self-signed certificates.</span></span> <span data-ttu-id="8534c-149">В этом случае используйте эти сведения для изучения требований и получения сертификата в соответствии с политиками вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8534c-149">In that case, use this information to understand the requirements and acquire a certificate in accordance to your organization's policies.</span></span>

```Powershell
$dnsName = "<TenantDomain like agent.onmicrosoft.com>" # Your DNS name
$password = "<password>" # Certificate password
$folderPath = "D:\New folder\" # Where do you want the files to get saved to? The folder needs to exist.
$fileName = "agentcert" # What do you want to call the cert files? without the file extension
$yearsValid = 10 # Number of years until you need to renew the certificate
$certStoreLocation = "cert:\LocalMachine\My"
$expirationDate = (Get-Date).AddYears($yearsValid)
$certificate = New-SelfSignedCertificate -DnsName $dnsName -CertStoreLocation $certStoreLocation -NotAfter $expirationDate -KeyExportPolicy Exportable -KeySpec Signature
$certificatePath = $certStoreLocation + '\' + $certificate.Thumbprint
$filePath = $folderPath + '\' + $fileName
$securePassword = ConvertTo-SecureString -String $password -Force -AsPlainText
Export-Certificate -Cert $certificatePath -FilePath ($filePath + '.cer')
Export-PfxCertificate -Cert $certificatePath -FilePath ($filePath + '.pfx') -Password $securePassword
```

##### <a name="step-2-upload-the-certificate-in-the-azure-portal"></a><span data-ttu-id="8534c-150">Шаг 2: отправка сертификата на портале Azure</span><span class="sxs-lookup"><span data-stu-id="8534c-150">Step 2: Upload the certificate in the Azure portal</span></span>

1. <span data-ttu-id="8534c-151">Откройте приложение и перейдите к разделу сертификаты и секреты из левой области</span><span class="sxs-lookup"><span data-stu-id="8534c-151">Open the application and navigate to certificates and secrets section from left pane</span></span>
1. <span data-ttu-id="8534c-152">Нажмите кнопку "отправить сертификат" и отправьте CER-файл.</span><span class="sxs-lookup"><span data-stu-id="8534c-152">Select 'Upload certificate' and upload the .cer file</span></span>
1. <span data-ttu-id="8534c-153">Откройте **регистрацию приложения** и выберите **Сертификаты и секреты** в области навигации.</span><span class="sxs-lookup"><span data-stu-id="8534c-153">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="8534c-154">Скопируйте отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="8534c-154">Copy the certificate thumbprint.</span></span>

![Список сертификатов сумбринт, когда в левой панели выбраны сертификаты и секреты](media/onprem-agent/certificates.png)

##### <a name="step-3-assign-the-certificate-to-the-agent"></a><span data-ttu-id="8534c-156">Шаг 3: назначьте сертификат агенту</span><span class="sxs-lookup"><span data-stu-id="8534c-156">Step 3: Assign the certificate to the agent</span></span>

<span data-ttu-id="8534c-157">Если для создания сертификата использовался пример сценария, PFX-файл можно найти в расположении, указанном в сценарии.</span><span class="sxs-lookup"><span data-stu-id="8534c-157">If you used the sample script to generate a certificate, the PFX file can be found in the location identified in the script.</span></span>

1. <span data-ttu-id="8534c-158">Скачайте PFX-файл сертификата на компьютер агента.</span><span class="sxs-lookup"><span data-stu-id="8534c-158">Download the certificate pfx file onto the Agent machine.</span></span>
1. <span data-ttu-id="8534c-159">Дважды щелкните PFX-файл, чтобы открыть диалоговое окно установки сертификата.</span><span class="sxs-lookup"><span data-stu-id="8534c-159">Double-click the pfx file to launch the certificate installation dialog.</span></span>
1. <span data-ttu-id="8534c-160">Выберите "локальный компьютер" для расположения хранилища при установке сертификата.</span><span class="sxs-lookup"><span data-stu-id="8534c-160">Select 'Local Machine' for store location while installing the certificate.</span></span>
1. <span data-ttu-id="8534c-161">После установки сертификата откройте меню "Управление сертификатами компьютеров" в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="8534c-161">After installing the certificate, open 'Manage computer certificates' through Start menu</span></span>
1. <span data-ttu-id="8534c-162">Выберите новый сертификат в разделе "личные" — > "сертификаты"</span><span class="sxs-lookup"><span data-stu-id="8534c-162">Select the newly installed certificate under 'Personal' -> 'Certificates'</span></span>
1. <span data-ttu-id="8534c-163">Щелкните сертификат правой кнопкой мыши и выберите пункт "все задачи" — > "Управление закрытыми ключами...".</span><span class="sxs-lookup"><span data-stu-id="8534c-163">Right click on the cert and select 'All Tasks' -> 'Manage Private Keys…'</span></span> <span data-ttu-id="8534c-164">Параметр</span><span class="sxs-lookup"><span data-stu-id="8534c-164">Option</span></span>
1. <span data-ttu-id="8534c-165">В диалоговом окне разрешения выберите команду Добавить параметр.</span><span class="sxs-lookup"><span data-stu-id="8534c-165">In the permissions dialog, select add option.</span></span> <span data-ttu-id="8534c-166">В диалоговом окне Выбор пользователя введите: "NT Сервице\гкахостсервице" и нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="8534c-166">In the user selection dialog, write: 'NT Service\GcaHostService' and click 'OK'.</span></span> <span data-ttu-id="8534c-167">Не нажимайте кнопку "проверить имена".</span><span class="sxs-lookup"><span data-stu-id="8534c-167">Don't click the 'Check Names' button.</span></span>
1. <span data-ttu-id="8534c-168">Нажмите кнопку ОК в диалоговом окне разрешения.</span><span class="sxs-lookup"><span data-stu-id="8534c-168">Click okay on the permissions dialog.</span></span> <span data-ttu-id="8534c-169">Теперь на компьютере агента настроено создание маркеров с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="8534c-169">The agent machine is now configured for agent to generate tokens using the certificate.</span></span>
