---
title: Установка поисковой системы по умолчанию
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: ee40010e-5d7f-4ba8-a3f8-d240dab3af6d
description: Узнайте, как настроить Bing в вашей организации в качестве поисковой системы по умолчанию с использованием Поиска (Майкрософт).
ms.openlocfilehash: 346bf3bf2da10178a8bd19390920db2d9de2629e
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031758"
---
# <a name="make-bing-the-default-search-engine"></a>Установка Bing в качестве поисковой системы по умолчанию
  
В этой статье описывается, как можно сделать Bing поисковой системой по умолчанию для браузеров Microsoft Edge, Google Chrome и Internet Explorer. 
  
## <a name="microsoft-edge-on-windows-10-version-1703-or-later"></a>Microsoft Edge в Windows 10 версии 1703 или более поздней

Хотя вы настраиваете Bing в качестве поисковой системы по умолчанию, Microsoft Edge позволяет пользователям изменять свои параметры для использования другой поисковой системы.
  
Последние версии ADMX-файлов для разных версий Windows см. в статье [Как создать центральное хранилище для административных шаблонов групповой политики в Windows и управлять им](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
  
Если параметр, описанный в этом разделе, не может быть найден внутри GPMC, скачайте соответствующий ADMX и скопируйте их в центральный магазин. Дополнительные сведения см. в Domain-Based [GPOs с помощью ADMX Files.](/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29) Центральный магазин контроллера — это папка со следующей конвенцией именования: **%systemroot%\sysvol \\<\> \policies\PolicyDefinitions**
  
Все домены, обслуживаемые контроллером, должны получить отдельную папку. Чтобы скопировать ADMX-файл из командной строки, можно использовать указанную ниже команду:
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.
2. Перейдите к разделу **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.
3. Дважды щелкните параметр **Set default search engine** (Задать поисковую систему по умолчанию), установите значение **Enabled** (Включено) и введите `https://www.bing.com/sa/osd/bfb.xml`
4. Примените полученный объект групповой политики, привязав его к нужному домену.


## <a name="google-chrome-on-windows-10-version-1507-or-later"></a>Google Chrome в Windows 10, Версии 1507 или более поздней версии

Пользователи не смогут сменить поисковую систему по умолчанию после установки этой политики.
  
Chrome поставляется с собственным набором параметров групповой политики, которые можно скачать в виде ADMX-файла из [google Chrome Enterprise Help.](https://support.google.com/chrome/a/answer/187202)
  
Скопируйте файл шаблона в центральный магазин файлов ADMX на контроллере домена. Дополнительные сведения см. в Domain-Based [GPOs с помощью ADMX Files.](/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29) Центральный магазин контроллера — это папка со следующей конвенцией именования: **%systemroot%\sysvol \\<\> \policies\PolicyDefinitions**
  
Все домены, обслуживаемые контроллером, должны получить отдельную папку. Чтобы скопировать ADMX-файл из командной строки, можно использовать указанную ниже команду:
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.
2. Проверьте, что в разделе Administrative Templates (Административные шаблоны) для обеих конфигураций User/Computer Configuration (Конфигурация пользователя/компьютера) отображаются следующие папки: Google Chrome и Google Chrome – Default Settings.

    - Параметры первого раздела являются фиксированными, и локальные администраторы не смогут их изменять в браузере.
    - Параметры последнего раздела политик могут изменяться пользователями в настройках браузера.

3. Перейдите к **\<Computer/User\> configuration\Administrative Templates\Google Chrome\Default search provider**
4. Дважды щелкните параметр **Enable the default search provider** (Включить поставщика поиска по умолчанию) и установите для него значение **Enabled** (Включено).
5. Дважды щелкните параметр **Default search provider icon** (Значок поставщика поиска по умолчанию), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/sa/simg/bb.ico`
6. Дважды щелкните параметр **Default search provider instant URL** (URL-адрес для быстрого поиска поставщика поиска по умолчанию) и введите `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`
7. Дважды щелкните параметр **Default search provider name** (Имя поставщика поиска по умолчанию), установите для него значение Enabled (Включено) и введите "Поиск (Майкрософт) в Bing"
8. Дважды щелкните параметр **Default search provider search URL** (Поисковый URL-адрес поставщика поиска по умолчанию), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`
9. Примените полученный объект групповой политики, привязав его к нужному домену.

## <a name="internet-explorer-11-or-later"></a>Internet Explorer 11 или более поздняя версия

Пользователи смогут сменить поставщика поиска после установки этой политики.
  
### <a name="step-1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a>ШАГ 1. Настройка локального компьютера, который будет использоваться для задания объекта групповой политики

Вставьте указанный ниже текст в REG-файл (\*.reg).
  
Windows Registry Editor Version 5.00
  
<pre>[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes]
"DefaultScope"="{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}"
[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes\{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}]
"Codepage"=dword:0000fde9
"DisplayName"="Microsoft Search in Bing"
"OSDFileURL"="https://www.bing.com/sa/osd/bfb.xml"
"FaviconURL"="https://www.bing.com/sa/simg/bb.ico"
"URL"="https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR"</pre>
  
Дважды щелкните созданный файл и выполните действия для импорта файла. После успешного выполнения импорта появится указанное ниже диалоговое окно:
  
![Сообщение об успешном импорте в редактор реестра](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
### <a name="step-2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a>ШАГ 2. Открытие консоли управления групповыми политиками (gpmc.msc) и переход к редактированию любой существующей политики или созданию новой

1. Перейдите к разделу **User Configuration\Policies\Preferences\Windows Settings**.
2. Щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра). В окне браузера реестра выберите **Local Computer** (Локальный компьютер) и нажмите кнопку **Next** (Далее).
3. Перейдите к разделу **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.
4. В этом разделе обязательно выберите имя DefaultScope.

    ![Браузер реестра с выбранным именем DefaultScope](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
5. Проверьте все подразделы, содержащие идентификатор GUID для Поиска (Майкрософт) в Bing, и каждое значение в разделе, кроме путей к профилям пользователей. Прокрутите вниз, чтобы выбрать другие элементы.
6. Нажмите кнопку "Готово", чтобы завершить настройку.

### <a name="step-3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a>ШАГ 3. Настройка параметров пользователя для устранения предупреждения, которое может появляться при применении поиска DefaultScope

Это предупреждение является стандартным и уведомляет пользователей о программе, пытающейся изменить настройки.
  
1. В том же объекте групповой политики щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра).
2. Перейдите к разделу **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.
3. Выберите раздел **User Preference** (Параметры пользователя).
4. Нажмите кнопку **Готово**.
5. Щелкните созданный объект. В области справа дважды щелкните объект параметров пользователя и измените **Action** (Действие) на **Delete and Save** (Удалить и сохранить).
6. Примените полученный объект групповой политики, привязав его к нужному домену.