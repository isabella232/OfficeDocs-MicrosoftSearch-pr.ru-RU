---
title: Локальное агент
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
description: On-prem Agent
ms.openlocfilehash: 7aef2ea57c92929d4d4f45e1a738c84e6a3f4bba
ms.sourcegitcommit: ab4f81ded967168689e6e81c90e115b94719335c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "50173065"
---
# <a name="graph-connector-agent"></a><span data-ttu-id="294a0-103">Агент соединители Graph</span><span class="sxs-lookup"><span data-stu-id="294a0-103">Graph connector agent</span></span>

<span data-ttu-id="294a0-104">Для использования подключений Graph на компьютере необходимо установить программное обеспечение агента *соединителя Graph.*</span><span class="sxs-lookup"><span data-stu-id="294a0-104">Using on-prem Graph connectors require you to install *Graph connector agent* software.</span></span> <span data-ttu-id="294a0-105">Он обеспечивает безопасную передачу данных между локальной данными и API соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="294a0-105">It allows for secure data transfer between on-premises data and the Graph connector APIs.</span></span> <span data-ttu-id="294a0-106">В этой статье вы можете установить и настроить агент.</span><span class="sxs-lookup"><span data-stu-id="294a0-106">This article guides you through the installing and configuring the agent.</span></span>

## <a name="installation"></a><span data-ttu-id="294a0-107">Установка</span><span class="sxs-lookup"><span data-stu-id="294a0-107">Installation</span></span>

<span data-ttu-id="294a0-108">Скачайте последнюю версию агента соединителя Graph [здесь](https://aka.ms/gcadownload) и установите программное обеспечение с помощью мастера установки.</span><span class="sxs-lookup"><span data-stu-id="294a0-108">Download the latest version of Graph connector agent [here](https://aka.ms/gcadownload) and install the software using the installation wizard.</span></span> <span data-ttu-id="294a0-109">С помощью рекомендуемой конфигурации компьютера, описанного ниже, программное обеспечение может обрабатывать до трех подключений.</span><span class="sxs-lookup"><span data-stu-id="294a0-109">Using the recommended configuration of the machine described below, the software can handle up to three connections.</span></span> <span data-ttu-id="294a0-110">Любые подключения, кроме этого, могут ухудшить производительность всех подключений агента.</span><span class="sxs-lookup"><span data-stu-id="294a0-110">Any connections beyond that might degrade the performance of all connections on the agent.</span></span>

<span data-ttu-id="294a0-111">Рекомендуемая конфигурация:</span><span class="sxs-lookup"><span data-stu-id="294a0-111">Recommended configuration:</span></span>

* <span data-ttu-id="294a0-112">Windows 10, Windows Server 2016 R2 и выше</span><span class="sxs-lookup"><span data-stu-id="294a0-112">Windows 10, Windows Server 2016 R2 and above</span></span>
* [<span data-ttu-id="294a0-113">.NET Core Desktop Runtime 3.1 (x64)</span><span class="sxs-lookup"><span data-stu-id="294a0-113">.NET Core Desktop Runtime 3.1 (x64)</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* <span data-ttu-id="294a0-114">8 ядер, 3 ГГц</span><span class="sxs-lookup"><span data-stu-id="294a0-114">8 cores, 3 GHz</span></span>
* <span data-ttu-id="294a0-115">16 ГБ ОЗУ, 2 ГБ места на диске</span><span class="sxs-lookup"><span data-stu-id="294a0-115">16 GB RAM, 2 GB Disk Space</span></span>
* <span data-ttu-id="294a0-116">Сетевой доступ к источнику данных и Интернету через 443</span><span class="sxs-lookup"><span data-stu-id="294a0-116">Network access to data source and internet through 443</span></span>

<span data-ttu-id="294a0-117">Если прокси-серверы или брандмауэры организации блокируют связь с неизвестными доменами после установки агента, добавьте их в список допустимых.</span><span class="sxs-lookup"><span data-stu-id="294a0-117">After you install the agent, if your organization's proxy servers or firewalls block communication to unknown domains, please add below ones to the allow list.</span></span>

1. <span data-ttu-id="294a0-118">\*.servicebus.windows.net</span><span class="sxs-lookup"><span data-stu-id="294a0-118">\*.servicebus.windows.net</span></span>
2. <span data-ttu-id="294a0-119">\*.events.data.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="294a0-119">\*.events.data.microsoft.com</span></span>
3. https://login.microsoftonline.com
4. https://gcs.office.com
5. https://graph.microsoft.com/


## <a name="create-and-configure-an-app-for-the-agent"></a><span data-ttu-id="294a0-120">Создание и настройка приложения для агента</span><span class="sxs-lookup"><span data-stu-id="294a0-120">Create and configure an App for the agent</span></span>  

<span data-ttu-id="294a0-121">Во-первых, во sign in and note that the minimum required privilege on the account is search administrator.</span><span class="sxs-lookup"><span data-stu-id="294a0-121">First, sign in and note that the minimum required privilege on the account is search administrator.</span></span> <span data-ttu-id="294a0-122">Затем агент попросит вас предоставить сведения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="294a0-122">The agent will then ask you to provide authentication details.</span></span> <span data-ttu-id="294a0-123">Для создания приложения и создания необходимых сведений о проверке подлинности используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="294a0-123">Use the steps below to create an app and generate the required authentication details.</span></span>

### <a name="create-an-app"></a><span data-ttu-id="294a0-124">Создать приложение</span><span class="sxs-lookup"><span data-stu-id="294a0-124">Create an app</span></span>

1. <span data-ttu-id="294a0-125">Перейдите на портал [Azure и](https://portal.azure.com) войдите с помощью учетных данных администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="294a0-125">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="294a0-126">Перейдите **к регистрации приложений Azure Active Directory** в области навигации и  ->   выберите **"Новая регистрация".**</span><span class="sxs-lookup"><span data-stu-id="294a0-126">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>
3. <span data-ttu-id="294a0-127">В качестве имени приложения выберите **"Регистрация".**</span><span class="sxs-lookup"><span data-stu-id="294a0-127">Provide a name for the app and select **Register**.</span></span>
4. <span data-ttu-id="294a0-128">Заметьте ИД приложения (клиента).</span><span class="sxs-lookup"><span data-stu-id="294a0-128">Make a note of the Application (client) ID.</span></span>
5. <span data-ttu-id="294a0-129">Откройте **разрешения API** в области навигации и выберите **"Добавить разрешение".**</span><span class="sxs-lookup"><span data-stu-id="294a0-129">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>
6. <span data-ttu-id="294a0-130">Выберите **Microsoft Graph,** а затем **разрешения приложения.**</span><span class="sxs-lookup"><span data-stu-id="294a0-130">Select **Microsoft Graph** and then **Application permissions**.</span></span>
7. <span data-ttu-id="294a0-131">Наберите в разрешениях "ExternalItem.ReadWrite.All" и "Directory.Read.All" и выберите **"Добавить разрешения".**</span><span class="sxs-lookup"><span data-stu-id="294a0-131">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>
8. <span data-ttu-id="294a0-132">Выберите **"Предоставить согласие администратора для [TenantName]** и подтвердит, выбрав **"Да".**</span><span class="sxs-lookup"><span data-stu-id="294a0-132">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>
9. <span data-ttu-id="294a0-133">Убедитесь, что разрешения находятся в состоянии "предоставлено".</span><span class="sxs-lookup"><span data-stu-id="294a0-133">Check that the permissions are in the "granted" state.</span></span>
     <span data-ttu-id="294a0-134">![Разрешения, предоставленные зеленым столбцом справа.](media/onprem-agent/granted-state.png)</span><span class="sxs-lookup"><span data-stu-id="294a0-134">![Permissions shown as granted in green on right hand column.](media/onprem-agent/granted-state.png)</span></span>

### <a name="configure-authentication"></a><span data-ttu-id="294a0-135">Настроить аутентификацию</span><span class="sxs-lookup"><span data-stu-id="294a0-135">Configure Authentication</span></span>

<span data-ttu-id="294a0-136">Сведения о проверке подлинности можно предоставлять с помощью секрета клиента или сертификата.</span><span class="sxs-lookup"><span data-stu-id="294a0-136">Authentication details can be provided using a client secret or a certificate.</span></span> <span data-ttu-id="294a0-137">Следуйте вашим шагам.</span><span class="sxs-lookup"><span data-stu-id="294a0-137">Follow the steps of your choice.</span></span>

#### <a name="configuring-the-client-secret-for-authentication"></a><span data-ttu-id="294a0-138">Настройка секрета клиента для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="294a0-138">Configuring the client secret for authentication</span></span>

1. <span data-ttu-id="294a0-139">Перейдите на портал [Azure и](https://portal.azure.com) войдите с помощью учетных данных администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="294a0-139">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="294a0-140">Откройте **регистрацию приложения** в области навигации и перейдите к соответствующему приложению.</span><span class="sxs-lookup"><span data-stu-id="294a0-140">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="294a0-141">В **области "Управление"** **выберите "Сертификаты и секреты".**</span><span class="sxs-lookup"><span data-stu-id="294a0-141">Under **Manage**, select **Certificates and secrets**.</span></span>
3. <span data-ttu-id="294a0-142">Выберите **новый секрет клиента** и выберите срок действия секрета.</span><span class="sxs-lookup"><span data-stu-id="294a0-142">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="294a0-143">Скопируйте созданный секрет и сохраните его, так как он больше не будет показан.</span><span class="sxs-lookup"><span data-stu-id="294a0-143">Copy the generated secret and save it because it won't be shown again.</span></span>
4. <span data-ttu-id="294a0-144">Используйте этот секрет клиента вместе с ИД приложения для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="294a0-144">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="294a0-145">В поле **"Имя"** агента нельзя использовать пустые пробелы.</span><span class="sxs-lookup"><span data-stu-id="294a0-145">You cannot use blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="294a0-146">Принимаются буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="294a0-146">Alpha numeric characters are accepted.</span></span>

#### <a name="using-a-certificate-for-authentication"></a><span data-ttu-id="294a0-147">Использование сертификата для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="294a0-147">Using a certificate for authentication</span></span>

<span data-ttu-id="294a0-148">Существует три простых шага для использования проверки подлинности на основе сертификатов:</span><span class="sxs-lookup"><span data-stu-id="294a0-148">There are three simple steps for using certificate-based authentication:</span></span>

1. <span data-ttu-id="294a0-149">Создание или получение сертификата</span><span class="sxs-lookup"><span data-stu-id="294a0-149">Create or obtain a certificate</span></span>
1. <span data-ttu-id="294a0-150">Отправка сертификата на портал Azure</span><span class="sxs-lookup"><span data-stu-id="294a0-150">Upload the certificate to the Azure portal</span></span>
1. <span data-ttu-id="294a0-151">Назначение сертификата агенту</span><span class="sxs-lookup"><span data-stu-id="294a0-151">Assign the certificate to the agent</span></span>

##### <a name="step-1-get-a-certificate"></a><span data-ttu-id="294a0-152">Шаг 1. Получите сертификат</span><span class="sxs-lookup"><span data-stu-id="294a0-152">Step 1: Get a certificate</span></span>

<span data-ttu-id="294a0-153">Сценарий ниже можно использовать для создания самозаверяемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="294a0-153">The script below can be used to generate a self-signed certificate.</span></span> <span data-ttu-id="294a0-154">Ваша организация может не разрешить самозаверять сертификаты.</span><span class="sxs-lookup"><span data-stu-id="294a0-154">Your organization may not allow self-signed certificates.</span></span> <span data-ttu-id="294a0-155">В этом случае используйте эту информацию для понимания требований и получения сертификата в соответствии с политиками организации.</span><span class="sxs-lookup"><span data-stu-id="294a0-155">In that case, use this information to understand the requirements and acquire a certificate in accordance to your organization's policies.</span></span>

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

##### <a name="step-2-upload-the-certificate-in-the-azure-portal"></a><span data-ttu-id="294a0-156">Шаг 2. Отправка сертификата на портал Azure</span><span class="sxs-lookup"><span data-stu-id="294a0-156">Step 2: Upload the certificate in the Azure portal</span></span>

1. <span data-ttu-id="294a0-157">Откройте приложение и перейдите в раздел "Сертификаты и секреты" на левой области</span><span class="sxs-lookup"><span data-stu-id="294a0-157">Open the application and navigate to certificates and secrets section from left pane</span></span>
1. <span data-ttu-id="294a0-158">Выберите "Отправить сертификат" и загрузите CER-файл</span><span class="sxs-lookup"><span data-stu-id="294a0-158">Select 'Upload certificate' and upload the .cer file</span></span>
1. <span data-ttu-id="294a0-159">Откройте **регистрацию приложения** и выберите **сертификаты и секреты** в области навигации.</span><span class="sxs-lookup"><span data-stu-id="294a0-159">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="294a0-160">Скопируйте отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="294a0-160">Copy the certificate thumbprint.</span></span>

![Список сертификатов thumbrint при выборе сертификатов и секретов на левой области](media/onprem-agent/certificates.png)

##### <a name="step-3-assign-the-certificate-to-the-agent"></a><span data-ttu-id="294a0-162">Шаг 3. Назначение сертификата агенту</span><span class="sxs-lookup"><span data-stu-id="294a0-162">Step 3: Assign the certificate to the agent</span></span>

<span data-ttu-id="294a0-163">Если вы использовали пример сценария для создания сертификата, PFX-файл можно найти в расположении, заданного в сценарии.</span><span class="sxs-lookup"><span data-stu-id="294a0-163">If you used the sample script to generate a certificate, the PFX file can be found in the location identified in the script.</span></span>

1. <span data-ttu-id="294a0-164">Скачайте PFX-файл сертификата на компьютер агента.</span><span class="sxs-lookup"><span data-stu-id="294a0-164">Download the certificate pfx file onto the Agent machine.</span></span>
1. <span data-ttu-id="294a0-165">Дважды щелкните PFX-файл, чтобы запустить диалоговое окно установки сертификата.</span><span class="sxs-lookup"><span data-stu-id="294a0-165">Double-click the pfx file to launch the certificate installation dialog.</span></span>
1. <span data-ttu-id="294a0-166">Выберите "Локальный компьютер" для расположения в хранилище при установке сертификата.</span><span class="sxs-lookup"><span data-stu-id="294a0-166">Select 'Local Machine' for store location while installing the certificate.</span></span>
1. <span data-ttu-id="294a0-167">После установки сертификата откройте меню "Управление сертификатами компьютера" в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="294a0-167">After installing the certificate, open 'Manage computer certificates' through Start menu</span></span>
1. <span data-ttu-id="294a0-168">Выберите только что установленный сертификат в "Personal" -> 'Certificates'</span><span class="sxs-lookup"><span data-stu-id="294a0-168">Select the newly installed certificate under 'Personal' -> 'Certificates'</span></span>
1. <span data-ttu-id="294a0-169">Щелкните сертификат правой кнопкой мыши и выберите "Все задачи" -> "Управление закрытыми ключами..."</span><span class="sxs-lookup"><span data-stu-id="294a0-169">Right click on the cert and select 'All Tasks' -> 'Manage Private Keys…'</span></span> <span data-ttu-id="294a0-170">Параметр</span><span class="sxs-lookup"><span data-stu-id="294a0-170">Option</span></span>
1. <span data-ttu-id="294a0-171">В диалоговом окте "Разрешения" выберите параметр "Добавить".</span><span class="sxs-lookup"><span data-stu-id="294a0-171">In the permissions dialog, select add option.</span></span> <span data-ttu-id="294a0-172">В диалоговом окне выбора пользователя напишите : "Служба NT\GcaHostService" и нажмите кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="294a0-172">In the user selection dialog, write: 'NT Service\GcaHostService' and click 'OK'.</span></span> <span data-ttu-id="294a0-173">Не нажимайте кнопку "Проверить имена".</span><span class="sxs-lookup"><span data-stu-id="294a0-173">Don't click the 'Check Names' button.</span></span>
1. <span data-ttu-id="294a0-174">Нажмите кнопку "ОК" в диалоговом окте разрешений.</span><span class="sxs-lookup"><span data-stu-id="294a0-174">Click okay on the permissions dialog.</span></span> <span data-ttu-id="294a0-175">Теперь на компьютере агента настроен агент для создания маркеров с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="294a0-175">The agent machine is now configured for agent to generate tokens using the certificate.</span></span>
