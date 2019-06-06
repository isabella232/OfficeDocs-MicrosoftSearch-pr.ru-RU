---
title: Установка поисковой системы по умолчанию
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
ms.assetid: ee40010e-5d7f-4ba8-a3f8-d240dab3af6d
ROBOTS: NOINDEX
description: Узнайте, как настроить Bing в вашей организации в качестве поисковой системы по умолчанию с использованием Поиска (Майкрософт).
ms.openlocfilehash: 36e8a50a7b6acda553b82d4b95a57a378818f7ec
ms.sourcegitcommit: fe7f3dae4edba97071a4d127e8a27bdf4fa00d81
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2019
ms.locfileid: "34727990"
---
# <a name="set-default-search-engine"></a><span data-ttu-id="a017a-103">Установка поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a017a-103">Set default search engine</span></span>

  
<span data-ttu-id="a017a-104">Настройка браузера, поисковой системы и домашней страницы по умолчанию поможет пользователям раскрыть возможности Поиска (Майкрософт), поддерживает дополнительное использование и обеспечивает удобный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a017a-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="a017a-105">Чтобы установить поисковую систему по умолчанию для организации, следуйте указанным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="a017a-105">To set the default search engine for your organization, follow the steps below.</span></span>
  
## <a name="internet-explorer"></a><span data-ttu-id="a017a-106">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a017a-106">Internet Explorer</span></span>

### <a name="internet-explorer-11"></a><span data-ttu-id="a017a-107">Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="a017a-107">Internet Explorer 11</span></span>

<span data-ttu-id="a017a-108">Пользователи смогут сменить поставщика поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="a017a-108">Users will be able to change the search provider after this policy is set.</span></span>
  
#### <a name="1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a><span data-ttu-id="a017a-109">1. Настройте локальный компьютер, который будет использоваться для установки объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="a017a-109">1. Configure the local machine that will be used to set the GPO</span></span>

<span data-ttu-id="a017a-110">Вставьте указанный ниже текст в REG-файл (\*.reg).</span><span class="sxs-lookup"><span data-stu-id="a017a-110">Paste the following text into a reg(\*.reg) file.</span></span>
  
<span data-ttu-id="a017a-111">Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="a017a-111">Windows Registry Editor Version 5.00</span></span>
  
<pre>[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes]
"DefaultScope"="{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}"
[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes\{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}]
"Codepage"=dword:0000fde9
"DisplayName"="Microsoft Search in Bing"
"OSDFileURL"="https://www.bing.com/sa/osd/bfb.xml"
"FaviconURL"="https://www.bing.com/sa/simg/bb.ico"
"SuggestionsURL_JSON"="https://business.ing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA"
"ShowSearchSuggestions"=dword:00000001
"URL"="https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR"</pre>
  
<span data-ttu-id="a017a-p101">Дважды щелкните созданный файл и выполните действия для импорта файла. После успешного выполнения импорта появится указанное ниже диалоговое окно:</span><span class="sxs-lookup"><span data-stu-id="a017a-p101">Double-click the file created and follow the steps to import the file. A successful import should result in the following dialog:</span></span>
  
![Сообщение об успешном импорте в редактор реестра](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
#### <a name="2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a><span data-ttu-id="a017a-115">2. Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="a017a-115">2. Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one</span></span>

1. <span data-ttu-id="a017a-116">Перейдите к разделу **User Configuration\Policies\Preferences\Windows Settings**.</span><span class="sxs-lookup"><span data-stu-id="a017a-116">Navigate to **User Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="a017a-p102">Щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра). В окне браузера реестра выберите **Local Computer** (Локальный компьютер) и нажмите кнопку **Next** (Далее).</span><span class="sxs-lookup"><span data-stu-id="a017a-p102">Right-click on **Registry\New** and select **Registry Wizard**. From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
3. <span data-ttu-id="a017a-119">Перейдите к разделу **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span><span class="sxs-lookup"><span data-stu-id="a017a-119">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span></span>
    
4. <span data-ttu-id="a017a-120">В этом разделе обязательно выберите имя DefaultScope.</span><span class="sxs-lookup"><span data-stu-id="a017a-120">From this key, make sure to select DefaultScope.</span></span>
    
    ![Браузер реестра с выбранным именем DefaultScope](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
  
5. <span data-ttu-id="a017a-p103">Проверьте все подразделы, содержащие идентификатор GUID для Поиска (Майкрософт) в Bing, и каждое значение в разделе, кроме путей к профилям пользователей. Прокрутите вниз, чтобы выбрать другие элементы.</span><span class="sxs-lookup"><span data-stu-id="a017a-p103">Check all sub keys containing the GUID for Microsoft Search in Bing and every value under the key except any path to user profiles. Scroll down to select other items.</span></span>
    
    ![Браузер реестра с выбранными дополнительными значениями](media/7eef7690-8bc5-46cf-9cd8-bd134fc77a02.png)
  
6. <span data-ttu-id="a017a-125">Нажмите кнопку "Готово", чтобы завершить настройку.</span><span class="sxs-lookup"><span data-stu-id="a017a-125">Click Finish to complete this configuration.</span></span>
    
#### <a name="3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a><span data-ttu-id="a017a-126">3. Настройка параметров пользователя для устранения предупреждения, которое может появляться при применении поиска DefaultScope</span><span class="sxs-lookup"><span data-stu-id="a017a-126">3. Set up User Preferences to help eliminate a warning the user may get when DefaultScope search is enforced</span></span>

<span data-ttu-id="a017a-127">Это предупреждение является стандартным и уведомляет пользователей о программе, пытающейся изменить настройки.</span><span class="sxs-lookup"><span data-stu-id="a017a-127">This warning is by design and alerts users of a program trying to modify their settings.</span></span>
  
1. <span data-ttu-id="a017a-128">В том же объекте групповой политики щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра).</span><span class="sxs-lookup"><span data-stu-id="a017a-128">Within the same GPO, right click on **Registry\New** and select **Registry Wizard**.</span></span>
    
2. <span data-ttu-id="a017a-129">Перейдите к разделу **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span><span class="sxs-lookup"><span data-stu-id="a017a-129">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span></span>
    
3. <span data-ttu-id="a017a-130">Выберите раздел **User Preference** (Параметры пользователя).</span><span class="sxs-lookup"><span data-stu-id="a017a-130">Select the **User Preference** key.</span></span>
    
4. <span data-ttu-id="a017a-131">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="a017a-131">Click **Finish**.</span></span>
    
5. <span data-ttu-id="a017a-p104">Щелкните созданный объект. В области справа дважды щелкните объект параметров пользователя и измените **Action** (Действие) на **Delete and Save** (Удалить и сохранить).</span><span class="sxs-lookup"><span data-stu-id="a017a-p104">Click on the newly created object. On the right-side pane double click on the User Preferences object, change the **Action** to **Delete and Save**.</span></span>
    
<span data-ttu-id="a017a-134">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="a017a-134">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
  
## <a name="microsoft-edge"></a><span data-ttu-id="a017a-135">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a017a-135">Microsoft Edge</span></span>

### <a name="windows-10-version-1703-or-later"></a><span data-ttu-id="a017a-136">Windows 10 версии 1703 или более поздней</span><span class="sxs-lookup"><span data-stu-id="a017a-136">Windows 10, Version 1703 or later</span></span>

<span data-ttu-id="a017a-137">Пользователи смогут сменить поставщика поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="a017a-137">Users will be able to change the search provider after this policy is set.</span></span>
  
<span data-ttu-id="a017a-138">Последние версии ADMX-файлов для разных версий Windows см. в статье [Как создать центральное хранилище для административных шаблонов групповой политики в Windows и управлять им](https://support.microsoft.com/ru-RU/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span><span class="sxs-lookup"><span data-stu-id="a017a-138">For the latest ADMX files for various versions of Windows, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>
  
<span data-ttu-id="a017a-p105">Если в GPMC не удается найти параметр, описанный в этом разделе, скачайте соответствующие ADMX-файлы и скопируйте их в центральное хранилище. Дополнительные сведения см. в статье [Изменение объектов GPO на основе домена с помощью ADMX-файлов](https://docs.microsoft.com/ru-RU/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Центральное хранилище на контроллере — это папка с указанными ниже правилами именования:</span><span class="sxs-lookup"><span data-stu-id="a017a-p105">If the setting described in this section cannot be found inside of GPMC, download the appropriate ADMX and copy them to the central store. For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="a017a-142">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a017a-142">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="a017a-p106">Все домены, обслуживаемые контроллером, должны получить отдельную папку. Чтобы скопировать ADMX-файл из командной строки, можно использовать указанную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="a017a-p106">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="a017a-145">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="a017a-145">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="a017a-146">Перейдите к разделу **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="a017a-146">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span></span>
    
1. <span data-ttu-id="a017a-147">Дважды щелкните параметр **Set default search engine** (Задать поисковую систему по умолчанию), установите значение **Enabled** (Включено) и введите `https://www.bing.com/sa/osd/bfb.xml`</span><span class="sxs-lookup"><span data-stu-id="a017a-147">Double-click **Set default search engine**, set to **Enabled**, and enter `https://www.bing.com/sa/osd/bfb.xml`</span></span>
    
3. <span data-ttu-id="a017a-148">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="a017a-148">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
## <a name="google-chrome"></a><span data-ttu-id="a017a-149">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="a017a-149">Google Chrome</span></span>

### <a name="windows-xp-sp2-or-later"></a><span data-ttu-id="a017a-150">Windows XP с пакетом обновления 2 (SP2) или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="a017a-150">Windows XP SP2 or later</span></span>

<span data-ttu-id="a017a-151">Пользователи не смогут сменить поставщика поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="a017a-151">Users won't be able to change the search provider after this policy is set.</span></span>
  
<span data-ttu-id="a017a-p107">Chrome содержит собственный набор параметров групповой политики, которые можно скачать в виде ADMX-файла с сайта [справки Google Chrome Enterprise](https://support.google.com/chrome/a/answer/187202). Если для управления объектом GPO для домена используются операционные системы Windows Vista/Server 2008 или более поздней версии, ADMX-файл, поставляемый в этом пакете, позаботится о настройках Chrome на Windows XP SP2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a017a-p107">Chrome comes with its own set of group policy settings which can be downloaded in the form of an ADMX file from [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202). If operating systems Windows Vista/Server 2008 or later are used to manage GPO's for the domain, the ADMX file provided in this package takes care of Chrome settings on Windows XP SP2 or later.</span></span>
  
<span data-ttu-id="a017a-p108">Скопируйте файл шаблона в центральное хранилище для ADMX-файлов на контроллере домена. Дополнительные сведения см. в статье [Изменение объектов GPO на основе домена с помощью ADMX-файлов](https://docs.microsoft.com/ru-RU/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Центральное хранилище на контроллере — это папка с указанными ниже правилами именования:</span><span class="sxs-lookup"><span data-stu-id="a017a-p108">Copy the template file to a central store for ADMX files on the domain controller. For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="a017a-157">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a017a-157">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="a017a-p109">Все домены, обслуживаемые контроллером, должны получить отдельную папку. Чтобы скопировать ADMX-файл из командной строки, можно использовать указанную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="a017a-p109">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="a017a-160">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="a017a-160">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="a017a-161">Проверьте, что в разделе Administrative Templates (Административные шаблоны) для обеих конфигураций User/Computer Configuration (Конфигурация пользователя/компьютера) отображаются следующие папки: Google Chrome и Google Chrome – Default Settings.</span><span class="sxs-lookup"><span data-stu-id="a017a-161">Make sure the following folders appear in the Administrative Templates section of both User/Computer Configuration: Google Chrome and Google Chrome - Default Settings.</span></span>
    
  - <span data-ttu-id="a017a-162">Параметры первого раздела являются фиксированными, и локальные администраторы не смогут их изменять в браузере.</span><span class="sxs-lookup"><span data-stu-id="a017a-162">The settings of the first section are fixed and local administrators won't be able to change them in the browser.</span></span>
    
  - <span data-ttu-id="a017a-163">Параметры последнего раздела политик могут изменяться пользователями в настройках браузера.</span><span class="sxs-lookup"><span data-stu-id="a017a-163">The settings of the latter section of policies can be changed by users in the browser settings.</span></span>
    
3. <span data-ttu-id="a017a-164">Перейдите к разделу **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default search provider**</span><span class="sxs-lookup"><span data-stu-id="a017a-164">Navigate to **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default search provider**</span></span>
    
4. <span data-ttu-id="a017a-165">Дважды щелкните параметр **Enable the default search provider** (Включить поставщика поиска по умолчанию) и установите для него значение **Enabled** (Включено).</span><span class="sxs-lookup"><span data-stu-id="a017a-165">Double-click **Enable the default search provider**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="a017a-166">Дважды щелкните параметр **Default search provider icon** (Значок поставщика поиска по умолчанию), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/sa/simg/bb.ico`</span><span class="sxs-lookup"><span data-stu-id="a017a-166">Double-click **Default search provider icon**, set it to **Enabled**, and enter `https://www.bing.com/sa/simg/bb.ico`</span></span>
    
6. <span data-ttu-id="a017a-167">Дважды щелкните параметр **Default search provider instant URL** (URL-адрес для быстрого поиска поставщика поиска по умолчанию) и введите `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="a017a-167">Double-click **Default search provider instant URL**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
7. <span data-ttu-id="a017a-168">Дважды щелкните параметр **Default search provider name** (Имя поставщика поиска по умолчанию), установите для него значение Enabled (Включено) и введите "Поиск (Майкрософт) в Bing"</span><span class="sxs-lookup"><span data-stu-id="a017a-168">Double-click **Default search provider name**, set it to Enabled, and enter 'Microsoft Search in Bing'</span></span>
    
8. <span data-ttu-id="a017a-169">Дважды щелкните параметр **Default search provider search URL** (Поисковый URL-адрес поставщика поиска по умолчанию), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="a017a-169">Double-click **Default search provider search URL**, set it to **Enabled**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
9. <span data-ttu-id="a017a-170">Дважды щелкните параметр **Default search provider suggest URL** (Рекомендуемый URL-адрес поставщика поиска по умолчанию), установите для него значение **Enabled** (Включено) и введите `https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span><span class="sxs-lookup"><span data-stu-id="a017a-170">Double-click **Default search provider suggest URL**, set it to **Enabled**, and enter `https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span></span>
    
10. <span data-ttu-id="a017a-171">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="a017a-171">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="a017a-p110">Настройка поисковой системы по умолчанию добавит функцию поисковых вариантов Поиска (Майкрософт) в адресной строке браузера. В настоящее время она поддерживается только для закладок. При вводе в адресной строке пользователи увидят две самые популярные рекомендации для закладок над предложениями из Интернета.</span><span class="sxs-lookup"><span data-stu-id="a017a-p110">Setting the default search engine will add the Microsoft Search search suggestions feature in the browser address bar. Currently, this supports bookmarks only. Users will see the top two bookmark suggestions above public web suggestions as they type in the address bar.</span></span>