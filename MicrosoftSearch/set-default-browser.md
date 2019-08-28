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
# <a name="make-microsoft-edge-the-default-browser"></a>Настройка Microsoft Edge в качестве браузера по умолчанию
  
Чтобы оптимально использовать возможности Поиска (Майкрософт), вы можете сделать Microsoft Edge браузером по умолчанию. При этом Microsoft Edge будет настроен в качестве браузера по умолчанию только для пользователей в вашей организации. Отдельные пользователи по-прежнему смогут выбирать другие браузеры.
  
  
## <a name="windows-8-and-later"></a>Windows 8 и более поздние версии

В этих инструкциях показано, как настроить Microsoft Edge или Internet Explorer в качестве браузера по умолчанию для компьютеров под управлением Windows 8 и более поздних версий. Пользователи смогут сменить браузер после установки этой политики.
  
### <a name="step-1-create-the-default-associations-file"></a>ШАГ 1. Создание файла сопоставлений по умолчанию
Создайте файл сопоставлений по умолчанию в папке SYSVOL контроллера домена.

1. Откройте административную консоль PowerShell.
1. `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
1. `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
1. `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
  
### <a name="step-2-add-or-edit-the-default-associations-file"></a>ШАГ 2. Добавление или изменение файла сопоставлений по умолчанию

1. `Notepad "$SettingsPath\AppAssoc.xml"`
1. Измените указанные ниже записи (.htm, .html, http, https) и удалите другие записи, если они не нужны.
  - **Microsoft Edge**
    - `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
              
    - `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
    - `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - **Internet Explorer**
    
    - `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`        
    - `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`

### <a name="step-3-edit-the-group-policy"></a>Шаг 3. Изменение групповой политики

1. Откройте **консоль управления групповыми политиками** (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.
1. Перейдите к разделу **Computer Configuration\Administrative Templates\Windows Components\File Explorer**
1. Дважды щелкните параметр **Set a default associations configuration file** (Задать файл конфигурации сопоставлений по умолчанию), установите для него значение **Enabled** (Включено) и введите путь к AppAssoc.xml (например, %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml). Примените полученный объект групповой политики, привязав его к нужному домену.

  
## <a name="windows-7"></a>Windows 7

1. Настройте локальный компьютер, который будет использоваться для установки объекта групповой политики.
    
1. Откройте **Панель управления\Программы\Программы по умолчанию\Задание программ по умолчанию** и установите Internet Explorer для использования по умолчанию. 
    
2. Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.
    
1. Перейдите к разделу **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.
    
2. Щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра).
    
3. В окне браузера реестра выберите **Local Computer** (Локальный компьютер) и нажмите кнопку **Next** (Далее).
    
4. Перейдите к разделу **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как на изображении ниже: 
    
    ![Выбор значения ProgID при изменении строкового параметра](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. Перейдите к разделу **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как на изображении ниже: 
    
    ![Выбор значения ProgID для HTTPS при изменении строкового параметра](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. Примените полученный объект групповой политики, привязав его к нужному домену.
    
