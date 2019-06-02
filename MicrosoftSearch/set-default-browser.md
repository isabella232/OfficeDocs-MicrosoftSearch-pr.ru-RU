---
title: Установка браузера по умолчанию
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/20/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 53e2b71a-348b-4dfe-a504-6e97d573effe
ROBOTS: NOINDEX
description: Узнайте, как настроить браузер по умолчанию для организации при использовании Поиска (Майкрософт).
ms.openlocfilehash: daff7f66bd38bdd56179e44c36092a2c4fd42b42
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591164"
---
# <a name="set-default-browser"></a><span data-ttu-id="d8c47-103">Установка браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d8c47-103">Set default browser</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8c47-104">Эта статья относится к Поиску (Майкрософт) на портале администрирования Bing.</span><span class="sxs-lookup"><span data-stu-id="d8c47-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="d8c47-105">Мы переносим портал в Центр администрирования Microsoft 365 с последующим его удалением.</span><span class="sxs-lookup"><span data-stu-id="d8c47-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="d8c47-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8c47-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="d8c47-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="d8c47-107">[Overview of Microsoft Search](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="d8c47-108">Настройка браузера, поисковой системы и домашней страницы по умолчанию поможет пользователям раскрыть возможности Поиска (Майкрософт), поддерживает дополнительное использование и обеспечивает удобный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d8c47-108">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="d8c47-109">Чтобы установить браузер по умолчанию для организации, следуйте указанным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="d8c47-109">To set the default browser for your organization, follow the steps below.</span></span>
  
## <a name="windows-8-and-above"></a><span data-ttu-id="d8c47-110">Windows 8 и более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="d8c47-110">Windows 8 and above</span></span>

<span data-ttu-id="d8c47-111">Чтобы установить Internet Explorer или Microsoft Edge в качестве браузера по умолчанию, выполните указанные ниже действия:</span><span class="sxs-lookup"><span data-stu-id="d8c47-111">To set Internet Explorer or Microsoft Edge as the default browser, follow these steps:</span></span>
  
### <a name="create-default-associations-file"></a><span data-ttu-id="d8c47-112">Создание файла сопоставлений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d8c47-112">Create default associations file</span></span>

1. <span data-ttu-id="d8c47-113">Откройте административную консоль PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d8c47-113">Open an administrative PowerShell console.</span></span>
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
<span data-ttu-id="d8c47-114">Эти действия создают файл сопоставлений по умолчанию в папке SYSVOL контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="d8c47-114">These steps try and create the default associations file in the SYSVOL folder of the domain controller.</span></span>
  
### <a name="add-or-edit-the-default-associations-file"></a><span data-ttu-id="d8c47-115">Добавление или изменение файла сопоставлений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d8c47-115">Add or edit the default associations file</span></span>

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. <span data-ttu-id="d8c47-116">Измените указанные ниже записи (.htm, .html, http, https) и удалите другие записи, если они не нужны.</span><span class="sxs-lookup"><span data-stu-id="d8c47-116">Edit the following entries (.htm, .html, http, https), and remove other entries if they're not needed.</span></span>
    
  - <span data-ttu-id="d8c47-117">**Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="d8c47-117">**Microsoft Edge**</span></span>
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - <span data-ttu-id="d8c47-118">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="d8c47-118">**Internet Explorer**</span></span>
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. <span data-ttu-id="d8c47-119">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="d8c47-119">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="d8c47-120">Перейдите к разделу **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span><span class="sxs-lookup"><span data-stu-id="d8c47-120">Navigate to **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span></span>
    
2. <span data-ttu-id="d8c47-121">Дважды щелкните параметр **Set a default associations configuration file** (Задать файл конфигурации сопоставлений по умолчанию), установите для него значение **Enabled** (Включено) и введите путь к AppAssoc.xml (например, %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span><span class="sxs-lookup"><span data-stu-id="d8c47-121">Double-click **Set a default associations configuration file**, set it to **Enabled**, and enter the path to AppAssoc.xml (for example %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span></span>
    
4. <span data-ttu-id="d8c47-122">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="d8c47-122">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="d8c47-123">Пользователи смогут сменить браузер после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="d8c47-123">Users will be able to change the browser after this policy is set.</span></span>
  
## <a name="windows-7"></a><span data-ttu-id="d8c47-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8c47-124">Windows 7</span></span>

1. <span data-ttu-id="d8c47-125">Настройте локальный компьютер, который будет использоваться для установки объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="d8c47-125">Configure the local machine that will be used to set the GPO.</span></span>
    
1. <span data-ttu-id="d8c47-126">Откройте **Панель управления\Программы\Программы по умолчанию\Задание программ по умолчанию** и установите Internet Explorer для использования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8c47-126">Open **Control Panel\Programs\Default Programs\Set Default Programs** and set Internet Explorer as the default.</span></span> 
    
2. <span data-ttu-id="d8c47-127">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="d8c47-127">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="d8c47-128">Перейдите к разделу **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span><span class="sxs-lookup"><span data-stu-id="d8c47-128">Navigate to **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="d8c47-129">Щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра).</span><span class="sxs-lookup"><span data-stu-id="d8c47-129">Right-click on **Registry\New** and select **Registry Wizard**.</span></span>
    
3. <span data-ttu-id="d8c47-130">В окне браузера реестра выберите **Local Computer** (Локальный компьютер) и нажмите кнопку **Next** (Далее).</span><span class="sxs-lookup"><span data-stu-id="d8c47-130">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
4. <span data-ttu-id="d8c47-p102">Перейдите к разделу **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как на изображении ниже:</span><span class="sxs-lookup"><span data-stu-id="d8c47-p102">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure the value looks like the one below:</span></span> 
    
    ![Выбор значения ProgID при изменении строкового параметра](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. <span data-ttu-id="d8c47-p103">Перейдите к разделу **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как на изображении ниже:</span><span class="sxs-lookup"><span data-stu-id="d8c47-p103">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure that the value looks like the one below:</span></span> 
    
    ![Выбор значения ProgID для HTTPS при изменении строкового параметра](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. <span data-ttu-id="d8c47-137">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="d8c47-137">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="d8c47-138">Пользователи смогут сменить браузер после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="d8c47-138">Users will be able to change the browser after this policy is set.</span></span>