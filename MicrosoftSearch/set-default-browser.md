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
# <a name="set-default-browser"></a>Набор по умолчанию браузера

Настройка браузера по умолчанию, поисковую систему по умолчанию и главной страницы по умолчанию поможет пользователям обнаружения возможностей поиска Microsoft, рекомендуем Дополнительные об использовании и предоставление облегчению интерфейса.
  
Чтобы задать браузера по умолчанию для вашей организации, выполните следующие действия.
  
## <a name="windows-8-and-above"></a>Windows 8 и выше

Чтобы установить Internet Explorer или пограничного сервера Microsoft в качестве браузера по умолчанию, выполните следующие действия:
  
### <a name="create-default-associations-file"></a>Создание файла связи по умолчанию

1. Откройте консоль администрирования PowerShell.
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
Эти действия попробуйте и создайте файл связи по умолчанию в папке SYSVOL контроллера домена.
  
### <a name="add-or-edit-the-default-associations-file"></a>Добавление и редактирование файлов сопоставлений по умолчанию

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. Измените следующие записи (htm, .html, http, https) и удалить другие записи, если их не обязательно.
    
  - **Microsoft Edge**
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - **Internet Explorer**
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.
    
1. Перейдите на **компьютере Конфигурация пользователя\Административные шаблоны\Компоненты Components\File Explorer**
    
2. Дважды щелкните значок **Установка файла конфигурации связи по умолчанию**, задайте для него значение **Enabled**и введите путь к AppAssoc.xml (например %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)
    
4. Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.
    
Пользователи будут иметь возможность изменение в браузере после установки этой политики.
  
## <a name="windows-7"></a>Windows 7

1. Настройка локального компьютера, который будет использоваться для установки объекта групповой Политики.
    
1. Откройте **Элемент управления Panel\Programs\Default Programs\Set по умолчанию программы** и использовать Internet Explorer по умолчанию. 
    
2. Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.
    
1. Перейдите к ** \<компьютера или пользователя\> параметры Configuration\Policies\Preferences\Windows**.
    
2. Щелкните правой кнопкой мыши на **Registry\New** и выберите **Мастер реестра**.
    
3. В окне браузера реестра выберите **Локальный компьютер** и нажмите кнопку **Далее**.
    
4. Перейдите к **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь, что значение выглядит как показано ниже: 
    
    ![Выберите значение ProgID в Изменение строкового параметра](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. Перейдите к **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** и выберите значение ProgId. Убедитесь в том, что значение выглядит как именно ниже: 
    
    ![Выберите параметр ProgId для HTTPS в строку редактирования](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.
    
Пользователи будут иметь возможность изменение в браузере после установки этой политики.