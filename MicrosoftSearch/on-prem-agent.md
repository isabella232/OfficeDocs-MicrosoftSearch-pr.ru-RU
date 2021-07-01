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
# <a name="microsoft-graph-connector-agent"></a>Агент соедините Graph Microsoft

Для установки программного обеспечения агента соединительных агентов Microsoft Graph предварительного *подключения.* Это позволяет безопасно передавать данные между локальной передачей данных и API соединители. В этой статье вы можете с помощью установки и настройки агента.

## <a name="installation"></a>Установка

Скачайте последнюю версию агента Graph соединителя и установите программное обеспечение [https://aka.ms/GCAdownload](https://aka.ms/gcadownload) с помощью мастера установки. С помощью рекомендуемой конфигурации машины, описанной ниже, программное обеспечение может обрабатывать до трех подключений. Любые подключения за пределами этого могут привести к ухудшению производительности всех подключений агента.

Рекомендуемая конфигурация:

* Windows 10, Windows Server 2016 R2 и выше
* [.NET Core Desktop Runtime 3.1 (x64)](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* 8 ядер, 3 ГГц
* 16 ГБ оперативной памяти, 2 ГБ дискового пространства
* Сетевой доступ к источнику данных и Интернету через 443

После установки агента, если прокси-серверы или брандмауэры вашей организации блокируют связь с неизвестными доменами, добавьте ниже их в список допустимых.

1. *.servicebus.windows.net
2. *.events.data.microsoft.com
3. https://<span>login.microsoftonline.</span> com
4. https://<span>gcs.office.</span> com/
5. https://<span>graph.microsoft.</span> com/


## <a name="create-and-configure-an-app-for-the-agent"></a>Создание и настройка приложения для агента  

Во-первых, впишитесь и обратите внимание, что минимальная необходимая привилегия для учетной записи — администратор поиска. Затем агент попросит вас предоставить сведения о проверке подлинности. Используйте ниже шаги для создания приложения и создания необходимых сведений о проверке подлинности.

### <a name="create-an-app"></a>Создать приложение

1. Перейдите на [портал Azure и](https://portal.azure.com) войдите с учетными данными администратора для клиента.

2. Перейдите **Azure Active Directory** регистрации приложений из области навигации и  ->   выберите **новую регистрацию.**

3. Укай имя приложения и выберите **Register.**

4. Обратите внимание на ID приложения (клиента).

5. Откройте **разрешения API из** области навигации и выберите Добавить **разрешение.**

6. Выберите **microsoft Graph,** а затем **разрешения приложения**.

7. Поиск "ExternalItem.ReadWrite.All" и "Directory.Read.All" из разрешений и выберите **Добавить разрешения**.

8. Выберите **согласие администратора гранта для [TenantName]** и подтвердит, выбрав **Да**.

9. Убедитесь, что разрешения находятся в состоянии "предоставлено".

    :::image type="content" alt-text="Разрешения, показанные в зеленом цвете в правой колонке." source="media/onprem-agent/granted-state.png" lightbox="media/onprem-agent/granted-state.png":::

### <a name="configure-authentication"></a>Настроить аутентификацию

Сведения о проверке подлинности можно предоставлять с помощью клиентской тайны или сертификата. Следуйте шагам по вашему выбору.

#### <a name="configuring-the-client-secret-for-authentication"></a>Настройка секрета клиента для проверки подлинности

1. Перейдите на [портал Azure и](https://portal.azure.com) войдите с учетными данными администратора для клиента.

2. Откройте **регистрацию приложения** из области навигации и перейдите к соответствующему приложению. В **статье Управление** выберите **сертификаты и секреты.**

3. Выберите **секрет "Новый клиент"** и выберите для этого секрета период истечения срока действия. Скопируйте созданный секрет и сохраните его, так как он больше не будет показан.

4. Используйте этот секрет клиента вместе с ИД приложения для настройки агента. В поле **Имя** агента нельзя использовать пустые пробелы. Принимаются числимые символы Альфа.

#### <a name="using-a-certificate-for-authentication"></a>Использование сертификата для проверки подлинности

Существует три простых шага для использования проверки подлинности на основе сертификатов:

1. Создание или получение сертификата
1. Upload сертификат на портал Azure
1. Назначение сертификата агенту

##### <a name="step-1-get-a-certificate"></a>Шаг 1. Получить сертификат

Сценарий ниже можно использовать для создания самозаверяемого сертификата. В организации могут не разрешаться самозаверяться сертификаты. В этом случае используйте эти сведения для понимания требований и получения сертификата в соответствии с политиками организации.

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

##### <a name="step-2-upload-the-certificate-in-the-azure-portal"></a>Шаг 2. Upload сертификат на портале Azure

1. Откройте приложение и перейдите в раздел сертификаты и секреты из левой области.

1. Выберите **Upload сертификат и** загрузите файл .cer.

1. Откройте **регистрацию приложения** и **выберите сертификаты и секреты** из области навигации. Скопируйте отпечатки сертификатов.

:::image type="content" alt-text="Список сертификатов thumbrint при выборе сертификатов и секретов в левой области" source="media/onprem-agent/certificates.png" lightbox="media/onprem-agent/certificates.png":::

##### <a name="step-3-assign-the-certificate-to-the-agent"></a>Шаг 3. Назначение сертификата агенту

Если вы использовали пример сценария для создания сертификата, файл PFX можно найти в расположении, идентифицированного в скрипте.

1. Скачайте файл сертификата pfx на компьютер Agent.

1. Дважды щелкните файл pfx, чтобы запустить диалоговое окно установки сертификата.

1. Выберите **локализованную** машину для расположения магазина при установке сертификата.

1. После установки сертификата откройте **управление сертификатами компьютера** через меню .

1. Выберите недавно установленный сертификат в **личных**  >  **сертификатах.**

1. Щелкните правой кнопкой мыши на сертификате и выберите **параметр "Управление** закрытыми  >  **ключами"** всеми задачами.

1. В диалоговом окантове разрешений выберите параметр добавить. В диалоговом окне выбора пользователя напишите: **NT Service\GcaHostService** и нажмите **кнопку ОК**. Не нажимайте **кнопку Check Names.**

1. Щелкните кнопку окей в диалоговом окантовке разрешений. Машина агента теперь настроена для агента для создания маркеров с помощью сертификата.

## <a name="troubleshooting"></a>Устранение неполадок

1. Если подключение не удается с ошибкой "1011: агент соединиттеля Graph не является недоступным или автономным", войдите в машину, на которой установлен агент, и запустите приложение агента, если оно еще не запущено. Если подключение продолжает сбой, убедитесь, что сертификат или секрет клиента, предоставленный агенту во время регистрации, не истек и имеет необходимые разрешения.
