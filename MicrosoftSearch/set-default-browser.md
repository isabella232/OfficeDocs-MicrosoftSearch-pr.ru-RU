---
title: Установка браузера по умолчанию
ms.author: anfowler
author: adefowler
manager: shohara
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
description: Настройте Microsoft Edge или Internet Explorer в качестве браузера по умолчанию для пользователей Поиска (Майкрософт).
ms.openlocfilehash: ed145a1811aba0b58158ed04dd3bf8dc089a0682
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639742"
---
# <a name="make-microsoft-edge-the-default-browser"></a><span data-ttu-id="3690f-103">Настройка Microsoft Edge в качестве браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3690f-103">Make Microsoft Edge the default browser</span></span>
  
<span data-ttu-id="3690f-104">Чтобы оптимально использовать возможности Поиска (Майкрософт), вы можете сделать Microsoft Edge браузером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3690f-104">To give your users the best experience with Microsoft Search, you can make Microsoft Edge the default browser.</span></span> <span data-ttu-id="3690f-105">При этом Microsoft Edge будет настроен в качестве браузера по умолчанию только для пользователей в вашей организации. Отдельные пользователи по-прежнему смогут выбирать другие браузеры.</span><span class="sxs-lookup"><span data-stu-id="3690f-105">This will only set Microsoft Edge as the default browser for users in your org, individual users can still select a different browser.</span></span>
  
  
## <a name="windows-8-and-later"></a><span data-ttu-id="3690f-106">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3690f-106">Windows 8 and above</span></span>

<span data-ttu-id="3690f-107">В этих инструкциях показано, как настроить Microsoft Edge или Internet Explorer в качестве браузера по умолчанию для компьютеров под управлением Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3690f-107">These instructions show you how to make Microsoft Edge or Internet Explorer as the default browser for computers running Windows 8 or later.</span></span> <span data-ttu-id="3690f-108">Пользователи смогут сменить браузер после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="3690f-108">Users will be able to change the browser after this policy is set.</span></span>
  
### <a name="step-1-create-the-default-associations-file"></a><span data-ttu-id="3690f-109">ШАГ 1. Создание файла сопоставлений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3690f-109">STEP 1: Create the default associations file</span></span>
<span data-ttu-id="3690f-110">Создайте файл сопоставлений по умолчанию в папке SYSVOL контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="3690f-110">These steps try and create the default associations file in the SYSVOL folder of the domain controller.</span></span>

1. <span data-ttu-id="3690f-111">Откройте административную консоль PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3690f-111">Open an administrative PowerShell console.</span></span>
1. `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
1. `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
1. `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
  
### <a name="step-2-add-or-edit-the-default-associations-file"></a><span data-ttu-id="3690f-112">ШАГ 2.</span><span class="sxs-lookup"><span data-stu-id="3690f-112">Step 2</span></span> <span data-ttu-id="3690f-113">Добавление или изменение файла сопоставлений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3690f-113">Add or edit the default associations file</span></span>

1. `Notepad "$SettingsPath\AppAssoc.xml"`
1. <span data-ttu-id="3690f-114">Измените указанные ниже записи (.htm, .html, http, https) и удалите другие записи, если они не нужны.</span><span class="sxs-lookup"><span data-stu-id="3690f-114">Edit the following entries (.htm, .html, http, https), and remove other entries if they're not needed.</span></span>
  - <span data-ttu-id="3690f-115">**Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="3690f-115">**Microsoft Edge**</span></span>
    - `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
              
    - `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
    - `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - <span data-ttu-id="3690f-116">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="3690f-116">**Internet Explorer**</span></span>
    
    - `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`        
    - `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`

### <a name="step-3-edit-the-group-policy"></a><span data-ttu-id="3690f-117">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="3690f-117">Step 3.</span></span> <span data-ttu-id="3690f-118">Изменение групповой политики</span><span class="sxs-lookup"><span data-stu-id="3690f-118">Edit the Group Policy</span></span>

1. <span data-ttu-id="3690f-119">Откройте **консоль управления групповыми политиками** (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="3690f-119">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
1. <span data-ttu-id="3690f-120">Перейдите к разделу **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span><span class="sxs-lookup"><span data-stu-id="3690f-120">Navigate to **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span></span>
1. <span data-ttu-id="3690f-121">Дважды щелкните параметр **Set a default associations configuration file** (Задать файл конфигурации сопоставлений по умолчанию), установите для него значение **Enabled** (Включено) и введите путь к AppAssoc.xml (например, %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml). Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="3690f-121">Double-click **Set a default associations configuration file**, set it to **Enabled**, and enter the path to AppAssoc.xml (for example %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml) Enforce the resultant GPO by linking it to the appropriate domain.</span></span>

  
## <a name="windows-7"></a><span data-ttu-id="3690f-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3690f-122">Windows 7</span></span>

1. <span data-ttu-id="3690f-123">Настройте локальный компьютер, который будет использоваться для установки объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="3690f-123">Configure the local machine that will be used to set the GPO.</span></span>
    
1. <span data-ttu-id="3690f-124">Откройте **Панель управления\Программы\Программы по умолчанию\Задание программ по умолчанию** и установите Internet Explorer для использования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3690f-124">Open **Control Panel\Programs\Default Programs\Set Default Programs** and set Internet Explorer as the default.</span></span> 
    
2. <span data-ttu-id="3690f-125">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="3690f-125">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="3690f-126">Перейдите к разделу **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span><span class="sxs-lookup"><span data-stu-id="3690f-126">Navigate to **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="3690f-127">Щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра).</span><span class="sxs-lookup"><span data-stu-id="3690f-127">Right-click on **Registry\New** and select **Registry Wizard**.</span></span>
    
3. <span data-ttu-id="3690f-128">В окне браузера реестра выберите **Local Computer** (Локальный компьютер) и нажмите кнопку **Next** (Далее).</span><span class="sxs-lookup"><span data-stu-id="3690f-128">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
4. <span data-ttu-id="3690f-p105">Перейдите к разделу **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как на изображении ниже:</span><span class="sxs-lookup"><span data-stu-id="3690f-p105">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure the value looks like the one below:</span></span> 
    
    ![Выбор значения ProgID при изменении строкового параметра](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. <span data-ttu-id="3690f-p106">Перейдите к разделу **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как на изображении ниже:</span><span class="sxs-lookup"><span data-stu-id="3690f-p106">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure that the value looks like the one below:</span></span> 
    
    ![Выбор значения ProgID для HTTPS при изменении строкового параметра](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. <span data-ttu-id="3690f-135">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="3690f-135">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
