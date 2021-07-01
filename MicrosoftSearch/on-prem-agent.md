---
title: Агент локального
ms.author: rusamai
author: rsamai
manager: jameslau
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NoIndex
description: Агент on-prem
ms.openlocfilehash: d6dabbbb5ee34acedd92166564f560bbc64c7da7
ms.sourcegitcommit: 93fc70f0073ab45b4dbd702441ac2fc07a7668bc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "53230928"
---
# <a name="microsoft-graph-connector-agent"></a><span data-ttu-id="c3076-103">Агент соедините Graph Microsoft</span><span class="sxs-lookup"><span data-stu-id="c3076-103">Microsoft Graph connector agent</span></span>

<span data-ttu-id="c3076-104">Для установки программного обеспечения агента соединительных агентов Microsoft Graph предварительного *подключения.*</span><span class="sxs-lookup"><span data-stu-id="c3076-104">Using on-prem connectors require you to install *Microsoft Graph connector agent* software.</span></span> <span data-ttu-id="c3076-105">Это позволяет безопасно передавать данные между локальной передачей данных и API соединители.</span><span class="sxs-lookup"><span data-stu-id="c3076-105">It allows for secure data transfer between on-premises data and the connector APIs.</span></span> <span data-ttu-id="c3076-106">В этой статье вы можете с помощью установки и настройки агента.</span><span class="sxs-lookup"><span data-stu-id="c3076-106">This article guides you through the installing and configuring the agent.</span></span>

## <a name="installation"></a><span data-ttu-id="c3076-107">Установка</span><span class="sxs-lookup"><span data-stu-id="c3076-107">Installation</span></span>

<span data-ttu-id="c3076-108">Скачайте последнюю версию агента Graph соединителя и установите программное обеспечение [https://aka.ms/GCAdownload](https://aka.ms/gcadownload) с помощью мастера установки.</span><span class="sxs-lookup"><span data-stu-id="c3076-108">Download the latest version of the Graph connector agent from [https://aka.ms/GCAdownload](https://aka.ms/gcadownload) and install the software by using the installation wizard.</span></span> <span data-ttu-id="c3076-109">С помощью рекомендуемой конфигурации машины, описанной ниже, программное обеспечение может обрабатывать до трех подключений.</span><span class="sxs-lookup"><span data-stu-id="c3076-109">Using the recommended configuration of the machine described below, the software can handle up to three connections.</span></span> <span data-ttu-id="c3076-110">Любые подключения за пределами этого могут привести к ухудшению производительности всех подключений агента.</span><span class="sxs-lookup"><span data-stu-id="c3076-110">Any connections beyond that might degrade the performance of all connections on the agent.</span></span>

<span data-ttu-id="c3076-111">Рекомендуемая конфигурация:</span><span class="sxs-lookup"><span data-stu-id="c3076-111">Recommended configuration:</span></span>

* <span data-ttu-id="c3076-112">Windows 10, Windows Server 2016 R2 и выше</span><span class="sxs-lookup"><span data-stu-id="c3076-112">Windows 10, Windows Server 2016 R2 and above</span></span>
* [<span data-ttu-id="c3076-113">.NET Core Desktop Runtime 3.1 (x64)</span><span class="sxs-lookup"><span data-stu-id="c3076-113">.NET Core Desktop Runtime 3.1 (x64)</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* <span data-ttu-id="c3076-114">8 ядер, 3 ГГц</span><span class="sxs-lookup"><span data-stu-id="c3076-114">8 cores, 3 GHz</span></span>
* <span data-ttu-id="c3076-115">16 ГБ оперативной памяти, 2 ГБ дискового пространства</span><span class="sxs-lookup"><span data-stu-id="c3076-115">16 GB RAM, 2 GB Disk Space</span></span>
* <span data-ttu-id="c3076-116">Сетевой доступ к источнику данных и Интернету через 443</span><span class="sxs-lookup"><span data-stu-id="c3076-116">Network access to data source and internet through 443</span></span>

<span data-ttu-id="c3076-117">После установки агента, если прокси-серверы или брандмауэры вашей организации блокируют связь с неизвестными доменами, добавьте ниже их в список допустимых.</span><span class="sxs-lookup"><span data-stu-id="c3076-117">After you install the agent, if your organization's proxy servers or firewalls block communication to unknown domains, please add below ones to the allow list.</span></span>

1. <span data-ttu-id="c3076-118">\*.servicebus.windows.net</span><span class="sxs-lookup"><span data-stu-id="c3076-118">\*.servicebus.windows.net</span></span>
2. <span data-ttu-id="c3076-119">\*.events.data.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c3076-119">\*.events.data.microsoft.com</span></span>
3. <span data-ttu-id="c3076-120"> https://<span>login.microsoftonline.</span> com</span><span class="sxs-lookup"><span data-stu-id="c3076-120">https://<span>login.microsoftonline.</span>com</span></span>
4. <span data-ttu-id="c3076-121"> https://<span>gcs.office.</span> com/</span><span class="sxs-lookup"><span data-stu-id="c3076-121">https://<span>gcs.office.</span>com/</span></span>
5. <span data-ttu-id="c3076-122"> https://<span>graph.microsoft.</span> com/</span><span class="sxs-lookup"><span data-stu-id="c3076-122">https://<span>graph.microsoft.</span>com/</span></span>


## <a name="create-and-configure-an-app-for-the-agent"></a><span data-ttu-id="c3076-123">Создание и настройка приложения для агента</span><span class="sxs-lookup"><span data-stu-id="c3076-123">Create and configure an App for the agent</span></span>  

<span data-ttu-id="c3076-124">Во-первых, впишитесь и обратите внимание, что минимальная необходимая привилегия для учетной записи — администратор поиска.</span><span class="sxs-lookup"><span data-stu-id="c3076-124">First, sign in and note that the minimum required privilege on the account is search administrator.</span></span> <span data-ttu-id="c3076-125">Затем агент попросит вас предоставить сведения о проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="c3076-125">The agent will then ask you to provide authentication details.</span></span> <span data-ttu-id="c3076-126">Используйте ниже шаги для создания приложения и создания необходимых сведений о проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="c3076-126">Use the steps below to create an app and generate the required authentication details.</span></span>

### <a name="create-an-app"></a><span data-ttu-id="c3076-127">Создать приложение</span><span class="sxs-lookup"><span data-stu-id="c3076-127">Create an app</span></span>

1. <span data-ttu-id="c3076-128">Перейдите на [портал Azure и](https://portal.azure.com) войдите с учетными данными администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="c3076-128">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>

2. <span data-ttu-id="c3076-129">Перейдите **Azure Active Directory** регистрации приложений из области навигации и  ->   выберите **новую регистрацию.**</span><span class="sxs-lookup"><span data-stu-id="c3076-129">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>

3. <span data-ttu-id="c3076-130">Укай имя приложения и выберите **Register.**</span><span class="sxs-lookup"><span data-stu-id="c3076-130">Provide a name for the app and select **Register**.</span></span>

4. <span data-ttu-id="c3076-131">Обратите внимание на ID приложения (клиента).</span><span class="sxs-lookup"><span data-stu-id="c3076-131">Make a note of the Application (client) ID.</span></span>

5. <span data-ttu-id="c3076-132">Откройте **разрешения API из** области навигации и выберите Добавить **разрешение.**</span><span class="sxs-lookup"><span data-stu-id="c3076-132">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>

6. <span data-ttu-id="c3076-133">Выберите **microsoft Graph,** а затем **разрешения приложения**.</span><span class="sxs-lookup"><span data-stu-id="c3076-133">Select **Microsoft Graph** and then **Application permissions**.</span></span>

7. <span data-ttu-id="c3076-134">Поиск "ExternalItem.ReadWrite.All" и "Directory.Read.All" из разрешений и выберите **Добавить разрешения**.</span><span class="sxs-lookup"><span data-stu-id="c3076-134">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>

8. <span data-ttu-id="c3076-135">Выберите **согласие администратора гранта для [TenantName]** и подтвердит, выбрав **Да**.</span><span class="sxs-lookup"><span data-stu-id="c3076-135">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>

9. <span data-ttu-id="c3076-136">Убедитесь, что разрешения находятся в состоянии "предоставлено".</span><span class="sxs-lookup"><span data-stu-id="c3076-136">Check that the permissions are in the "granted" state.</span></span>

    :::image type="content" alt-text="Разрешения, показанные в зеленом цвете в правой колонке." source="media/onprem-agent/granted-state.png" lightbox="media/onprem-agent/granted-state.png":::

### <a name="configure-authentication"></a><span data-ttu-id="c3076-138">Настроить аутентификацию</span><span class="sxs-lookup"><span data-stu-id="c3076-138">Configure Authentication</span></span>

<span data-ttu-id="c3076-139">Сведения о проверке подлинности можно предоставлять с помощью клиентской тайны или сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3076-139">Authentication details can be provided using a client secret or a certificate.</span></span> <span data-ttu-id="c3076-140">Следуйте шагам по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="c3076-140">Follow the steps of your choice.</span></span>

#### <a name="configuring-the-client-secret-for-authentication"></a><span data-ttu-id="c3076-141">Настройка секрета клиента для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="c3076-141">Configuring the client secret for authentication</span></span>

1. <span data-ttu-id="c3076-142">Перейдите на [портал Azure и](https://portal.azure.com) войдите с учетными данными администратора для клиента.</span><span class="sxs-lookup"><span data-stu-id="c3076-142">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>

2. <span data-ttu-id="c3076-143">Откройте **регистрацию приложения** из области навигации и перейдите к соответствующему приложению.</span><span class="sxs-lookup"><span data-stu-id="c3076-143">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="c3076-144">В **статье Управление** выберите **сертификаты и секреты.**</span><span class="sxs-lookup"><span data-stu-id="c3076-144">Under **Manage**, select **Certificates and secrets**.</span></span>

3. <span data-ttu-id="c3076-145">Выберите **секрет "Новый клиент"** и выберите для этого секрета период истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="c3076-145">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="c3076-146">Скопируйте созданный секрет и сохраните его, так как он больше не будет показан.</span><span class="sxs-lookup"><span data-stu-id="c3076-146">Copy the generated secret and save it because it won't be shown again.</span></span>

4. <span data-ttu-id="c3076-147">Используйте этот секрет клиента вместе с ИД приложения для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="c3076-147">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="c3076-148">В поле **Имя** агента нельзя использовать пустые пробелы.</span><span class="sxs-lookup"><span data-stu-id="c3076-148">You cannot use blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="c3076-149">Принимаются числимые символы Альфа.</span><span class="sxs-lookup"><span data-stu-id="c3076-149">Alpha numeric characters are accepted.</span></span>

#### <a name="using-a-certificate-for-authentication"></a><span data-ttu-id="c3076-150">Использование сертификата для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="c3076-150">Using a certificate for authentication</span></span>

<span data-ttu-id="c3076-151">Существует три простых шага для использования проверки подлинности на основе сертификатов:</span><span class="sxs-lookup"><span data-stu-id="c3076-151">There are three simple steps for using certificate-based authentication:</span></span>

1. <span data-ttu-id="c3076-152">Создание или получение сертификата</span><span class="sxs-lookup"><span data-stu-id="c3076-152">Create or obtain a certificate</span></span>
1. <span data-ttu-id="c3076-153">Upload сертификат на портал Azure</span><span class="sxs-lookup"><span data-stu-id="c3076-153">Upload the certificate to the Azure portal</span></span>
1. <span data-ttu-id="c3076-154">Назначение сертификата агенту</span><span class="sxs-lookup"><span data-stu-id="c3076-154">Assign the certificate to the agent</span></span>

##### <a name="step-1-get-a-certificate"></a><span data-ttu-id="c3076-155">Шаг 1. Получить сертификат</span><span class="sxs-lookup"><span data-stu-id="c3076-155">Step 1: Get a certificate</span></span>

<span data-ttu-id="c3076-156">Сценарий ниже можно использовать для создания самозаверяемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3076-156">The script below can be used to generate a self-signed certificate.</span></span> <span data-ttu-id="c3076-157">В организации могут не разрешаться самозаверяться сертификаты.</span><span class="sxs-lookup"><span data-stu-id="c3076-157">Your organization may not allow self-signed certificates.</span></span> <span data-ttu-id="c3076-158">В этом случае используйте эти сведения для понимания требований и получения сертификата в соответствии с политиками организации.</span><span class="sxs-lookup"><span data-stu-id="c3076-158">In that case, use this information to understand the requirements and acquire a certificate in accordance to your organization's policies.</span></span>

```powershell
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

##### <a name="step-2-upload-the-certificate-in-the-azure-portal"></a><span data-ttu-id="c3076-159">Шаг 2. Upload сертификат на портале Azure</span><span class="sxs-lookup"><span data-stu-id="c3076-159">Step 2: Upload the certificate in the Azure portal</span></span>

1. <span data-ttu-id="c3076-160">Откройте приложение и перейдите в раздел сертификаты и секреты из левой области.</span><span class="sxs-lookup"><span data-stu-id="c3076-160">Open the application and navigate to certificates and secrets section from left pane.</span></span>

1. <span data-ttu-id="c3076-161">Выберите **Upload сертификат и** загрузите файл .cer.</span><span class="sxs-lookup"><span data-stu-id="c3076-161">Select **Upload certificate** and upload the .cer file.</span></span>

1. <span data-ttu-id="c3076-162">Откройте **регистрацию приложения** и **выберите сертификаты и секреты** из области навигации.</span><span class="sxs-lookup"><span data-stu-id="c3076-162">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="c3076-163">Скопируйте отпечатки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c3076-163">Copy the certificate thumbprint.</span></span>

:::image type="content" alt-text="Список сертификатов thumbrint при выборе сертификатов и секретов в левой области" source="media/onprem-agent/certificates.png" lightbox="media/onprem-agent/certificates.png":::

##### <a name="step-3-assign-the-certificate-to-the-agent"></a><span data-ttu-id="c3076-165">Шаг 3. Назначение сертификата агенту</span><span class="sxs-lookup"><span data-stu-id="c3076-165">Step 3: Assign the certificate to the agent</span></span>

<span data-ttu-id="c3076-166">Если вы использовали пример сценария для создания сертификата, файл PFX можно найти в расположении, идентифицированного в скрипте.</span><span class="sxs-lookup"><span data-stu-id="c3076-166">If you used the sample script to generate a certificate, the PFX file can be found in the location identified in the script.</span></span>

1. <span data-ttu-id="c3076-167">Скачайте файл сертификата pfx на компьютер Agent.</span><span class="sxs-lookup"><span data-stu-id="c3076-167">Download the certificate pfx file onto the Agent machine.</span></span>

1. <span data-ttu-id="c3076-168">Дважды щелкните файл pfx, чтобы запустить диалоговое окно установки сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3076-168">Double-click the pfx file to launch the certificate installation dialog.</span></span>

1. <span data-ttu-id="c3076-169">Выберите **локализованную** машину для расположения магазина при установке сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3076-169">Select **Local Machine** for store location while installing the certificate.</span></span>

1. <span data-ttu-id="c3076-170">После установки сертификата откройте **управление сертификатами компьютера** через меню .</span><span class="sxs-lookup"><span data-stu-id="c3076-170">After installing the certificate, open **Manage computer certificates** through Start menu.</span></span>

1. <span data-ttu-id="c3076-171">Выберите недавно установленный сертификат в **личных**  >  **сертификатах.**</span><span class="sxs-lookup"><span data-stu-id="c3076-171">Select the newly installed certificate under **Personal** > **Certificates**.</span></span>

1. <span data-ttu-id="c3076-172">Щелкните правой кнопкой мыши на сертификате и выберите **параметр "Управление** закрытыми  >  **ключами"** всеми задачами.</span><span class="sxs-lookup"><span data-stu-id="c3076-172">Right click on the cert and select **All Tasks** > **Manage Private Keys** Option.</span></span>

1. <span data-ttu-id="c3076-173">В диалоговом окантове разрешений выберите параметр добавить.</span><span class="sxs-lookup"><span data-stu-id="c3076-173">In the permissions dialog, select add option.</span></span> <span data-ttu-id="c3076-174">В диалоговом окне выбора пользователя напишите: **NT Service\GcaHostService** и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="c3076-174">In the user selection dialog, write: **NT Service\GcaHostService** and click **OK**.</span></span> <span data-ttu-id="c3076-175">Не нажимайте **кнопку Check Names.**</span><span class="sxs-lookup"><span data-stu-id="c3076-175">Don't click the **Check Names** button.</span></span>

1. <span data-ttu-id="c3076-176">Щелкните кнопку окей в диалоговом окантовке разрешений.</span><span class="sxs-lookup"><span data-stu-id="c3076-176">Click okay on the permissions dialog.</span></span> <span data-ttu-id="c3076-177">Машина агента теперь настроена для агента для создания маркеров с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3076-177">The agent machine is now configured for agent to generate tokens using the certificate.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c3076-178">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="c3076-178">Troubleshooting</span></span>

1. <span data-ttu-id="c3076-179">Если подключение не удается с ошибкой "1011: агент соединиттеля Graph не является недоступным или автономным", войдите в машину, на которой установлен агент, и запустите приложение агента, если оно еще не запущено.</span><span class="sxs-lookup"><span data-stu-id="c3076-179">If a connection fails with the error "1011: The Graph connector agent is not reachable or offline.", log in to the machine where agent is installed and start the agent application if it isn't running already.</span></span> <span data-ttu-id="c3076-180">Если подключение продолжает сбой, убедитесь, что сертификат или секрет клиента, предоставленный агенту во время регистрации, не истек и имеет необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="c3076-180">If the connection continues to fail, verify that the certificate or client secret provided to the agent during registration hasn't expired and has required permissions.</span></span>
