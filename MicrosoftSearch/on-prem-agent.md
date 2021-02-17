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
ms.openlocfilehash: bd5212d42fe21583aa6a4e0dc8060d5e191a7292
ms.sourcegitcommit: 35b4246cb3e38c6fe21540686e28fe54154b33f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/16/2021
ms.locfileid: "50259432"
---
# <a name="graph-connector-agent"></a><span data-ttu-id="6fbc4-103">Агент соединители Graph</span><span class="sxs-lookup"><span data-stu-id="6fbc4-103">Graph connector agent</span></span>

<span data-ttu-id="6fbc4-104">Для использования подключений Graph на компьютере необходимо установить программное обеспечение агента *соединителя Graph.*</span><span class="sxs-lookup"><span data-stu-id="6fbc4-104">Using on-prem Graph connectors require you to install *Graph connector agent* software.</span></span> <span data-ttu-id="6fbc4-105">Он обеспечивает безопасную передачу данных между локальной данными и API соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-105">It allows for secure data transfer between on-premises data and the Graph connector APIs.</span></span> <span data-ttu-id="6fbc4-106">В этой статье вы можете установить и настроить агент.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-106">This article guides you through the installing and configuring the agent.</span></span>

## <a name="installation"></a><span data-ttu-id="6fbc4-107">Установка</span><span class="sxs-lookup"><span data-stu-id="6fbc4-107">Installation</span></span>

<span data-ttu-id="6fbc4-108">Скачайте последнюю версию агента соединителя Graph [здесь](https://aka.ms/gcadownload) и установите программное обеспечение с помощью мастера установки.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-108">Download the latest version of Graph connector agent [here](https://aka.ms/gcadownload) and install the software using the installation wizard.</span></span> <span data-ttu-id="6fbc4-109">С помощью рекомендуемой конфигурации компьютера, описанного ниже, программное обеспечение может обрабатывать до трех подключений.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-109">Using the recommended configuration of the machine described below, the software can handle up to three connections.</span></span> <span data-ttu-id="6fbc4-110">Любые подключения, кроме этого, могут ухудшить производительность всех подключений агента.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-110">Any connections beyond that might degrade the performance of all connections on the agent.</span></span>

<span data-ttu-id="6fbc4-111">Рекомендуемая конфигурация:</span><span class="sxs-lookup"><span data-stu-id="6fbc4-111">Recommended configuration:</span></span>

* <span data-ttu-id="6fbc4-112">Windows 10, Windows Server 2016 R2 и выше</span><span class="sxs-lookup"><span data-stu-id="6fbc4-112">Windows 10, Windows Server 2016 R2 and above</span></span>
* [<span data-ttu-id="6fbc4-113">.NET Core Desktop Runtime 3.1 (x64)</span><span class="sxs-lookup"><span data-stu-id="6fbc4-113">.NET Core Desktop Runtime 3.1 (x64)</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* <span data-ttu-id="6fbc4-114">8 ядер, 3 ГГц</span><span class="sxs-lookup"><span data-stu-id="6fbc4-114">8 cores, 3 GHz</span></span>
* <span data-ttu-id="6fbc4-115">16 ГБ ОЗУ, 2 ГБ места на диске</span><span class="sxs-lookup"><span data-stu-id="6fbc4-115">16 GB RAM, 2 GB Disk Space</span></span>
* <span data-ttu-id="6fbc4-116">Сетевой доступ к источнику данных и Интернету через 443</span><span class="sxs-lookup"><span data-stu-id="6fbc4-116">Network access to data source and internet through 443</span></span>

<span data-ttu-id="6fbc4-117">После установки агента, если прокси-серверы или брандмауэры вашей организации блокируют связь с неизвестными доменами, добавьте их в список допустимых.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-117">After you install the agent, if your organization's proxy servers or firewalls block communication to unknown domains, please add below ones to the allow list.</span></span>

1. <span data-ttu-id="6fbc4-118">\*.servicebus.windows.net</span><span class="sxs-lookup"><span data-stu-id="6fbc4-118">\*.servicebus.windows.net</span></span>
2. <span data-ttu-id="6fbc4-119">\*.events.data.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6fbc4-119">\*.events.data.microsoft.com</span></span>
3. <span data-ttu-id="6fbc4-120"> https://<span>login.microsoftonline.</span>com</span><span class="sxs-lookup"><span data-stu-id="6fbc4-120">https://<span>login.microsoftonline.</span>com</span></span>
4. <span data-ttu-id="6fbc4-121"> https://<span>gcs.office.</span> com/</span><span class="sxs-lookup"><span data-stu-id="6fbc4-121">https://<span>gcs.office.</span>com/</span></span>
5. <span data-ttu-id="6fbc4-122"> https://<span>graph.microsoft.</span> com/</span><span class="sxs-lookup"><span data-stu-id="6fbc4-122">https://<span>graph.microsoft.</span>com/</span></span>


## <a name="create-and-configure-an-app-for-the-agent"></a><span data-ttu-id="6fbc4-123">Создание и настройка приложения для агента</span><span class="sxs-lookup"><span data-stu-id="6fbc4-123">Create and configure an App for the agent</span></span>  

<span data-ttu-id="6fbc4-124">Во-первых, во sign in and note that the minimum required privilege on the account is search administrator.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-124">First, sign in and note that the minimum required privilege on the account is search administrator.</span></span> <span data-ttu-id="6fbc4-125">Затем агент попросит вас предоставить сведения о проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-125">The agent will then ask you to provide authentication details.</span></span> <span data-ttu-id="6fbc4-126">Чтобы создать приложение и получить необходимые сведения о проверке подлинности, воспользуйтесь действиями ниже.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-126">Use the steps below to create an app and generate the required authentication details.</span></span>

### <a name="create-an-app"></a><span data-ttu-id="6fbc4-127">Создать приложение</span><span class="sxs-lookup"><span data-stu-id="6fbc4-127">Create an app</span></span>

1. <span data-ttu-id="6fbc4-128">Перейдите на портал [Azure и](https://portal.azure.com) войдите с помощью учетных данных администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-128">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="6fbc4-129">Перейдите **к регистрации приложений Azure Active Directory** в области навигации и  ->   выберите **"Новая регистрация".**</span><span class="sxs-lookup"><span data-stu-id="6fbc4-129">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>
3. <span data-ttu-id="6fbc4-130">В качестве имени приложения выберите **"Регистрация".**</span><span class="sxs-lookup"><span data-stu-id="6fbc4-130">Provide a name for the app and select **Register**.</span></span>
4. <span data-ttu-id="6fbc4-131">Заметьте ИД приложения (клиента).</span><span class="sxs-lookup"><span data-stu-id="6fbc4-131">Make a note of the Application (client) ID.</span></span>
5. <span data-ttu-id="6fbc4-132">Откройте **разрешения API** в области навигации и выберите **"Добавить разрешение".**</span><span class="sxs-lookup"><span data-stu-id="6fbc4-132">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>
6. <span data-ttu-id="6fbc4-133">Выберите **Microsoft Graph,** а затем **разрешения приложения.**</span><span class="sxs-lookup"><span data-stu-id="6fbc4-133">Select **Microsoft Graph** and then **Application permissions**.</span></span>
7. <span data-ttu-id="6fbc4-134">Наберите в разрешениях "ExternalItem.ReadWrite.All" и "Directory.Read.All" и выберите **"Добавить разрешения".**</span><span class="sxs-lookup"><span data-stu-id="6fbc4-134">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>
8. <span data-ttu-id="6fbc4-135">Выберите **"Предоставить согласие администратора для [TenantName]** и подтвердит, выбрав **"Да".**</span><span class="sxs-lookup"><span data-stu-id="6fbc4-135">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>
9. <span data-ttu-id="6fbc4-136">Убедитесь, что разрешения находятся в состоянии "предоставлено".</span><span class="sxs-lookup"><span data-stu-id="6fbc4-136">Check that the permissions are in the "granted" state.</span></span>
     <span data-ttu-id="6fbc4-137">![Разрешения, предоставленные зеленым столбцом справа.](media/onprem-agent/granted-state.png)</span><span class="sxs-lookup"><span data-stu-id="6fbc4-137">![Permissions shown as granted in green on right hand column.](media/onprem-agent/granted-state.png)</span></span>

### <a name="configure-authentication"></a><span data-ttu-id="6fbc4-138">Настроить аутентификацию</span><span class="sxs-lookup"><span data-stu-id="6fbc4-138">Configure Authentication</span></span>

<span data-ttu-id="6fbc4-139">Сведения о проверке подлинности можно предоставлять с помощью секрета клиента или сертификата.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-139">Authentication details can be provided using a client secret or a certificate.</span></span> <span data-ttu-id="6fbc4-140">Следуйте вашим шагам.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-140">Follow the steps of your choice.</span></span>

#### <a name="configuring-the-client-secret-for-authentication"></a><span data-ttu-id="6fbc4-141">Настройка секрета клиента для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="6fbc4-141">Configuring the client secret for authentication</span></span>

1. <span data-ttu-id="6fbc4-142">Перейдите на портал [Azure и](https://portal.azure.com) войдите с помощью учетных данных администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-142">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="6fbc4-143">Откройте **регистрацию приложения** в области навигации и перейдите к соответствующему приложению.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-143">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="6fbc4-144">В **области "Управление"** **выберите сертификаты и секреты.**</span><span class="sxs-lookup"><span data-stu-id="6fbc4-144">Under **Manage**, select **Certificates and secrets**.</span></span>
3. <span data-ttu-id="6fbc4-145">Выберите **новый секрет клиента** и выберите срок действия секрета.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-145">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="6fbc4-146">Скопируйте созданный секрет и сохраните его, так как он больше не будет показан.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-146">Copy the generated secret and save it because it won't be shown again.</span></span>
4. <span data-ttu-id="6fbc4-147">Используйте этот секрет клиента вместе с ИД приложения для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-147">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="6fbc4-148">В поле **"Имя"** агента нельзя использовать пустые пробелы.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-148">You cannot use blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="6fbc4-149">Принимаются буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-149">Alpha numeric characters are accepted.</span></span>

#### <a name="using-a-certificate-for-authentication"></a><span data-ttu-id="6fbc4-150">Использование сертификата для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="6fbc4-150">Using a certificate for authentication</span></span>

<span data-ttu-id="6fbc4-151">Существует три простых шага для использования проверки подлинности на основе сертификатов:</span><span class="sxs-lookup"><span data-stu-id="6fbc4-151">There are three simple steps for using certificate-based authentication:</span></span>

1. <span data-ttu-id="6fbc4-152">Создание или получение сертификата</span><span class="sxs-lookup"><span data-stu-id="6fbc4-152">Create or obtain a certificate</span></span>
1. <span data-ttu-id="6fbc4-153">Отправка сертификата на портал Azure</span><span class="sxs-lookup"><span data-stu-id="6fbc4-153">Upload the certificate to the Azure portal</span></span>
1. <span data-ttu-id="6fbc4-154">Назначение сертификата агенту</span><span class="sxs-lookup"><span data-stu-id="6fbc4-154">Assign the certificate to the agent</span></span>

##### <a name="step-1-get-a-certificate"></a><span data-ttu-id="6fbc4-155">Шаг 1. Получите сертификат</span><span class="sxs-lookup"><span data-stu-id="6fbc4-155">Step 1: Get a certificate</span></span>

<span data-ttu-id="6fbc4-156">Сценарий ниже можно использовать для создания самозаверяемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-156">The script below can be used to generate a self-signed certificate.</span></span> <span data-ttu-id="6fbc4-157">Ваша организация может не разрешить самозаверяять сертификаты.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-157">Your organization may not allow self-signed certificates.</span></span> <span data-ttu-id="6fbc4-158">В этом случае используйте эту информацию для понимания требований и получения сертификата в соответствии с политиками организации.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-158">In that case, use this information to understand the requirements and acquire a certificate in accordance to your organization's policies.</span></span>

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

##### <a name="step-2-upload-the-certificate-in-the-azure-portal"></a><span data-ttu-id="6fbc4-159">Шаг 2. Отправка сертификата на портал Azure</span><span class="sxs-lookup"><span data-stu-id="6fbc4-159">Step 2: Upload the certificate in the Azure portal</span></span>

1. <span data-ttu-id="6fbc4-160">Откройте приложение и перейдите в раздел "Сертификаты и секреты" на левой области</span><span class="sxs-lookup"><span data-stu-id="6fbc4-160">Open the application and navigate to certificates and secrets section from left pane</span></span>
1. <span data-ttu-id="6fbc4-161">Выберите "Отправить сертификат" и загрузите CER-файл</span><span class="sxs-lookup"><span data-stu-id="6fbc4-161">Select 'Upload certificate' and upload the .cer file</span></span>
1. <span data-ttu-id="6fbc4-162">Откройте **регистрацию приложения** и выберите **сертификаты и секреты** в области навигации.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-162">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="6fbc4-163">Скопируйте отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-163">Copy the certificate thumbprint.</span></span>

![Список сертификатов thumbrint при выборе сертификатов и секретов на левой области](media/onprem-agent/certificates.png)

##### <a name="step-3-assign-the-certificate-to-the-agent"></a><span data-ttu-id="6fbc4-165">Шаг 3. Назначение сертификата агенту</span><span class="sxs-lookup"><span data-stu-id="6fbc4-165">Step 3: Assign the certificate to the agent</span></span>

<span data-ttu-id="6fbc4-166">Если вы использовали пример сценария для создания сертификата, PFX-файл можно найти в расположении, заданного в сценарии.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-166">If you used the sample script to generate a certificate, the PFX file can be found in the location identified in the script.</span></span>

1. <span data-ttu-id="6fbc4-167">Скачайте PFX-файл сертификата на компьютер агента.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-167">Download the certificate pfx file onto the Agent machine.</span></span>
1. <span data-ttu-id="6fbc4-168">Дважды щелкните PFX-файл, чтобы запустить диалоговое окно установки сертификата.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-168">Double-click the pfx file to launch the certificate installation dialog.</span></span>
1. <span data-ttu-id="6fbc4-169">Выберите "Локальный компьютер" для расположения в хранилище при установке сертификата.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-169">Select 'Local Machine' for store location while installing the certificate.</span></span>
1. <span data-ttu-id="6fbc4-170">После установки сертификата откройте меню "Управление сертификатами компьютера" в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="6fbc4-170">After installing the certificate, open 'Manage computer certificates' through Start menu</span></span>
1. <span data-ttu-id="6fbc4-171">Выберите только что установленный сертификат в "Personal" -> 'Certificates'</span><span class="sxs-lookup"><span data-stu-id="6fbc4-171">Select the newly installed certificate under 'Personal' -> 'Certificates'</span></span>
1. <span data-ttu-id="6fbc4-172">Щелкните сертификат правой кнопкой мыши и выберите "Все задачи" -> "Управление закрытыми ключами..."</span><span class="sxs-lookup"><span data-stu-id="6fbc4-172">Right click on the cert and select 'All Tasks' -> 'Manage Private Keys…'</span></span> <span data-ttu-id="6fbc4-173">Параметр</span><span class="sxs-lookup"><span data-stu-id="6fbc4-173">Option</span></span>
1. <span data-ttu-id="6fbc4-174">В диалоговом оке "Разрешения" выберите параметр "Добавить".</span><span class="sxs-lookup"><span data-stu-id="6fbc4-174">In the permissions dialog, select add option.</span></span> <span data-ttu-id="6fbc4-175">В диалоговом окне выбора пользователя напишите: "Служба NT\GcaHostService" и нажмите кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="6fbc4-175">In the user selection dialog, write: 'NT Service\GcaHostService' and click 'OK'.</span></span> <span data-ttu-id="6fbc4-176">Не нажимайте кнопку "Проверить имена".</span><span class="sxs-lookup"><span data-stu-id="6fbc4-176">Don't click the 'Check Names' button.</span></span>
1. <span data-ttu-id="6fbc4-177">Нажмите кнопку "ОК" в диалоговом окте разрешений.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-177">Click okay on the permissions dialog.</span></span> <span data-ttu-id="6fbc4-178">Теперь на компьютере агента настроен агент для создания маркеров с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-178">The agent machine is now configured for agent to generate tokens using the certificate.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="6fbc4-179">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="6fbc4-179">Troubleshooting</span></span>
1. <span data-ttu-id="6fbc4-180">Если не удается подключиться с ошибкой "1011: агент соединители Graph не удается связаться или в автономном режиме", войдите на компьютер, где установлен агент, и запустите приложение агента, если он еще не запущен.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-180">If a connection fails with the error '1011: The Graph connector agent is not reachable or offline.', log in to the machine where agent is installed and start the agent application if it isn't running already.</span></span> <span data-ttu-id="6fbc4-181">Если подключение не удается установить, убедитесь, что срок действия сертификата или секрета клиента, предоставленный агенту во время регистрации, не истек и что у него есть необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-181">If the connection continues to fail, verify that the certificate or client secret provided to the agent during registration hasn't expired and has required permissions.</span></span>
