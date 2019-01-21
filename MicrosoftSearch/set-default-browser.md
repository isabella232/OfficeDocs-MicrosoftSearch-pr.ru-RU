---
title: Набор по умолчанию браузера
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/20/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 53e2b71a-348b-4dfe-a504-6e97d573effe
description: Сведения о настройке браузера по умолчанию для Microsoft Search для вашей организации.
ms.openlocfilehash: 13a0a878b3288abeb7b07defdab839a158adc2ac
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "29379161"
---
# <a name="set-default-browser"></a><span data-ttu-id="ffd77-103">Набор по умолчанию браузера</span><span class="sxs-lookup"><span data-stu-id="ffd77-103">Set default browser</span></span>

<span data-ttu-id="ffd77-104">Настройка браузера по умолчанию, поисковую систему по умолчанию и главной страницы по умолчанию поможет пользователям обнаружения возможностей поиска Microsoft, рекомендуем Дополнительные об использовании и предоставление облегчению интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ffd77-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="ffd77-105">Чтобы задать браузера по умолчанию для вашей организации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ffd77-105">To set the default browser for your organization, follow the steps below.</span></span>
  
## <a name="windows-8-and-above"></a><span data-ttu-id="ffd77-106">Windows 8 и выше</span><span class="sxs-lookup"><span data-stu-id="ffd77-106">Windows 8 and above</span></span>

<span data-ttu-id="ffd77-107">Чтобы установить Internet Explorer или пограничного сервера Microsoft в качестве браузера по умолчанию, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ffd77-107">To set Internet Explorer or Microsoft Edge as the default browser, follow these steps:</span></span>
  
### <a name="create-default-associations-file"></a><span data-ttu-id="ffd77-108">Создание файла связи по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ffd77-108">Create default associations file</span></span>

1. <span data-ttu-id="ffd77-109">Откройте консоль администрирования PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ffd77-109">Open an administrative PowerShell console.</span></span>
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
<span data-ttu-id="ffd77-110">Эти действия попробуйте и создайте файл связи по умолчанию в папке SYSVOL контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="ffd77-110">These steps try and create the default associations file in the SYSVOL folder of the domain controller.</span></span>
  
### <a name="add-or-edit-the-default-associations-file"></a><span data-ttu-id="ffd77-111">Добавление и редактирование файлов сопоставлений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ffd77-111">Add or edit the default associations file</span></span>

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. <span data-ttu-id="ffd77-112">Измените следующие записи (htm, .html, http, https) и удалить другие записи, если их не обязательно.</span><span class="sxs-lookup"><span data-stu-id="ffd77-112">Edit the following entries (.htm, .html, http, https), and remove other entries if they're not needed.</span></span>
    
  - <span data-ttu-id="ffd77-113">**Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="ffd77-113">**Microsoft Edge**</span></span>
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - <span data-ttu-id="ffd77-114">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="ffd77-114">**Internet Explorer**</span></span>
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. <span data-ttu-id="ffd77-115">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.</span><span class="sxs-lookup"><span data-stu-id="ffd77-115">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="ffd77-116">Перейдите на **компьютере Конфигурация пользователя\Административные шаблоны\Компоненты Components\File Explorer**</span><span class="sxs-lookup"><span data-stu-id="ffd77-116">Navigate to **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span></span>
    
2. <span data-ttu-id="ffd77-117">Дважды щелкните значок **Установка файла конфигурации связи по умолчанию**, задайте для него значение **Enabled**и введите путь к AppAssoc.xml (например %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span><span class="sxs-lookup"><span data-stu-id="ffd77-117">Double-click **Set a default associations configuration file**, set it to **Enabled**, and enter the path to AppAssoc.xml (for example %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span></span>
    
4. <span data-ttu-id="ffd77-118">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="ffd77-118">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="ffd77-119">Пользователи будут иметь возможность изменение в браузере после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="ffd77-119">Users will be able to change the browser after this policy is set.</span></span>
  
## <a name="windows-7"></a><span data-ttu-id="ffd77-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ffd77-120">Windows 7</span></span>

1. <span data-ttu-id="ffd77-121">Настройка локального компьютера, который будет использоваться для установки объекта групповой Политики.</span><span class="sxs-lookup"><span data-stu-id="ffd77-121">Configure the local machine that will be used to set the GPO.</span></span>
    
1. <span data-ttu-id="ffd77-122">Откройте **Элемент управления Panel\Programs\Default Programs\Set по умолчанию программы** и использовать Internet Explorer по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ffd77-122">Open **Control Panel\Programs\Default Programs\Set Default Programs** and set Internet Explorer as the default.</span></span> 
    
2. <span data-ttu-id="ffd77-123">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.</span><span class="sxs-lookup"><span data-stu-id="ffd77-123">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="ffd77-124">Перейдите к \*\* \<компьютера или пользователя\> параметры Configuration\Policies\Preferences\Windows\*\*.</span><span class="sxs-lookup"><span data-stu-id="ffd77-124">Navigate to **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="ffd77-125">Щелкните правой кнопкой мыши на **Registry\New** и выберите **Мастер реестра**.</span><span class="sxs-lookup"><span data-stu-id="ffd77-125">Right-click on **Registry\New** and select **Registry Wizard**.</span></span>
    
3. <span data-ttu-id="ffd77-126">В окне браузера реестра выберите **Локальный компьютер** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ffd77-126">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
4. <span data-ttu-id="ffd77-p101">Перейдите к **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="ffd77-p101">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure the value looks like the one below:</span></span> 
    
    ![Выберите значение ProgID в Изменение строкового параметра](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. <span data-ttu-id="ffd77-p102">Перейдите к **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь в том, что значение выглядит как именно ниже:</span><span class="sxs-lookup"><span data-stu-id="ffd77-p102">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure that the value looks like the one below:</span></span> 
    
    ![Выберите параметр ProgId для HTTPS в строку редактирования](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. <span data-ttu-id="ffd77-133">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="ffd77-133">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="ffd77-134">Пользователи будут иметь возможность изменение в браузере после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="ffd77-134">Users will be able to change the browser after this policy is set.</span></span>