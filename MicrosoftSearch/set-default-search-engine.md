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
description: Узнайте, как назначить Bing поисковая система вашей компании по умолчанию с помощью Microsoft Search.
ms.openlocfilehash: a0798da94f4433bb754c71b9e0d00e09ba5a543b
ms.sourcegitcommit: 1c038d87efab4840d97b1f367b39e2b9ecdfee4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29612532"
---
# <a name="set-default-search-engine"></a><span data-ttu-id="ca9de-103">Установка поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ca9de-103">Set default search engine</span></span>

<span data-ttu-id="ca9de-104">Настройка браузера по умолчанию, поисковую систему по умолчанию и главной страницы по умолчанию поможет пользователям обнаружения возможностей поиска Microsoft, рекомендуем Дополнительные об использовании и предоставление облегчению интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ca9de-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="ca9de-105">Чтобы установить средство поиска по умолчанию для вашей организации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ca9de-105">To set the default search engine for your organization, follow the steps below.</span></span>
  
## <a name="internet-explorer"></a><span data-ttu-id="ca9de-106">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ca9de-106">Internet Explorer</span></span>

### <a name="internet-explorer-11"></a><span data-ttu-id="ca9de-107">Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="ca9de-107">Internet Explorer 11</span></span>

<span data-ttu-id="ca9de-108">Пользователи смогут изменять службу поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="ca9de-108">Users will be able to change the search provider after this policy is set.</span></span>
  
#### <a name="1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a><span data-ttu-id="ca9de-109">1. Настройте локальный компьютер, который будет использоваться для установки объекта групповой Политики</span><span class="sxs-lookup"><span data-stu-id="ca9de-109">1. Configure the local machine that will be used to set the GPO</span></span>

<span data-ttu-id="ca9de-110">Вставьте следующий текст в reg (\*реестра) файла.</span><span class="sxs-lookup"><span data-stu-id="ca9de-110">Paste the following text into a reg(\*.reg) file.</span></span>
  
<span data-ttu-id="ca9de-111">Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="ca9de-111">Windows Registry Editor Version 5.00</span></span>
  
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
  
<span data-ttu-id="ca9de-p101">Дважды щелкните файл, созданный и выполните действия, чтобы импортировать файл. В следующем диалоговом окне должно привести к успешного импорта:</span><span class="sxs-lookup"><span data-stu-id="ca9de-p101">Double-click the file created and follow the steps to import the file. A successful import should result in the following dialog:</span></span>
  
![Сообщение успешного импорта редактор реестра](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
#### <a name="2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a><span data-ttu-id="ca9de-115">2. Откройте консоль управления групповой политикой (gpmc.msc) и перейдите в изменении существующей политики или создание нового</span><span class="sxs-lookup"><span data-stu-id="ca9de-115">2. Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one</span></span>

1. <span data-ttu-id="ca9de-116">Перейдите к **Configuration\Policies\Preferences\Windows параметров пользователя**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-116">Navigate to **User Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="ca9de-p102">Щелкните правой кнопкой мыши на **Registry\New** и выберите **Мастер реестра**. В окне браузера реестра выберите **Локальный компьютер** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-p102">Right-click on **Registry\New** and select **Registry Wizard**. From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
3. <span data-ttu-id="ca9de-119">Перейдите к **Explorer\SearchScopes того**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-119">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span></span>
    
4. <span data-ttu-id="ca9de-120">Из данного раздела убедитесь в том выбрать DefaultScope.</span><span class="sxs-lookup"><span data-stu-id="ca9de-120">From this key, make sure to select DefaultScope.</span></span>
    
    ![Браузер реестра с DefaultScope выбранные](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
  
5. <span data-ttu-id="ca9de-p103">Проверьте все разделы sub, содержащая GUID для Microsoft поиска в Bing и каждое значение в раздел, за исключением любой путь к профилям пользователей. Прокрутите список вниз, чтобы выбрать другие элементы.</span><span class="sxs-lookup"><span data-stu-id="ca9de-p103">Check all sub keys containing the GUID for Microsoft Search in Bing and every value under the key except any path to user profiles. Scroll down to select other items.</span></span>
    
    ![Браузер реестра на дополнительные выбранные значения](media/7eef7690-8bc5-46cf-9cd8-bd134fc77a02.png)
  
6. <span data-ttu-id="ca9de-125">Нажмите кнопку Готово для завершения этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ca9de-125">Click Finish to complete this configuration.</span></span>
    
#### <a name="3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a><span data-ttu-id="ca9de-126">3. Настройка пользовательских параметров для предотвращения появления предупреждений, которые пользователь может получить при DefaultScope поиска</span><span class="sxs-lookup"><span data-stu-id="ca9de-126">3. Set up User Preferences to help eliminate a warning the user may get when DefaultScope search is enforced</span></span>

<span data-ttu-id="ca9de-127">Это предупреждение — это предусмотрено при проектировании и оповещений пользователям программы для изменения их параметров.</span><span class="sxs-lookup"><span data-stu-id="ca9de-127">This warning is by design and alerts users of a program trying to modify their settings.</span></span>
  
1. <span data-ttu-id="ca9de-128">В рамках одного объекта групповой Политики щелкните правой кнопкой мыши **Registry\New** и выберите **Мастер реестра**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-128">Within the same GPO, right click on **Registry\New** and select **Registry Wizard**.</span></span>
    
2. <span data-ttu-id="ca9de-129">Перейдите к **того Explorer\User предпочтения**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-129">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span></span>
    
3. <span data-ttu-id="ca9de-130">Выберите раздел **Настроек пользователя** .</span><span class="sxs-lookup"><span data-stu-id="ca9de-130">Select the **User Preference** key.</span></span>
    
4. <span data-ttu-id="ca9de-131">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-131">Click **Finish**.</span></span>
    
5. <span data-ttu-id="ca9de-p104">Щелкните только что созданный объект. На правой панели дважды щелкните на объекте пользовательские настройки, **действия** для **удаления и сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-p104">Click on the newly created object. On the right-side pane double click on the User Preferences object, change the **Action** to **Delete and Save**.</span></span>
    
<span data-ttu-id="ca9de-134">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="ca9de-134">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
  
## <a name="microsoft-edge"></a><span data-ttu-id="ca9de-135">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ca9de-135">Microsoft Edge</span></span>

### <a name="windows-10-version-1703-or-later"></a><span data-ttu-id="ca9de-136">10 Windows, 1703 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="ca9de-136">Windows 10, Version 1703 or later</span></span>

<span data-ttu-id="ca9de-137">Пользователи смогут изменять службу поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="ca9de-137">Users will be able to change the search provider after this policy is set.</span></span>
  
<span data-ttu-id="ca9de-138">Для последних ADMX-файлы для различных версий Windows Узнайте, [как создавать и управлять ими центрального хранилища для административных шаблонов групповой политики в Windows](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span><span class="sxs-lookup"><span data-stu-id="ca9de-138">For the latest ADMX files for various versions of Windows, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>
  
<span data-ttu-id="ca9de-p105">Если параметр, описанных в данном разделе не удается найти в консоли управления групповыми Политиками, загрузите соответствующий ADMX и копировать их в центральном хранилище. Для получения дополнительных сведений см [Editing Domain-Based объектов групповой политики с помощью ADMX-файлы](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Центральное хранилище на контроллере — это папка с следующее соглашение об именовании:</span><span class="sxs-lookup"><span data-stu-id="ca9de-p105">If the setting described in this section cannot be found inside of GPMC, download the appropriate ADMX and copy them to the central store. For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="ca9de-142">**%systemroot%\Sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="ca9de-142">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="ca9de-p106">Каждого, обрабатывающего контроллере домена должны получить отдельную папку. Для копирования файлов ADMX из командной строки можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ca9de-p106">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="ca9de-145">Откройте консоль управления групповой политикой (gpmc.msc) и перейдите в изменении существующей политики или создать новый.</span><span class="sxs-lookup"><span data-stu-id="ca9de-145">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="ca9de-146">Перейдите к \*\* &lt;Конфигурация компьютера/пользователя&gt;\Administrative Templates\Windows Components\Microsoft Edge\*\*.</span><span class="sxs-lookup"><span data-stu-id="ca9de-146">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span></span>
    
1. <span data-ttu-id="ca9de-147">Дважды щелкните значок **Установка поисковой системы по умолчанию**, **включена**и введите`https://www.bing.com/sa/osd/bfb.xml`</span><span class="sxs-lookup"><span data-stu-id="ca9de-147">Double-click **Set default search engine**, set to **Enabled**, and enter `https://www.bing.com/sa/osd/bfb.xml`</span></span>
    
3. <span data-ttu-id="ca9de-148">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="ca9de-148">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
## <a name="google-chrome"></a><span data-ttu-id="ca9de-149">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="ca9de-149">Google Chrome</span></span>

### <a name="windows-xp-sp2-or-later"></a><span data-ttu-id="ca9de-150">Windows XP с пакетом обновления 2 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ca9de-150">Windows XP SP2 or later</span></span>

<span data-ttu-id="ca9de-151">Пользователи не смогут изменять службу поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="ca9de-151">Users won't be able to change the search provider after this policy is set.</span></span>
  
<span data-ttu-id="ca9de-p107">Chrome, поступающие собственный набор параметров групповой политики, которые можно загрузить в виде ADMX-файл справки [Google Chrome Enterprise](https://support.google.com/chrome/a/answer/187202). Если операционных системах Windows Vista/Server 2008 или более поздней версии используются для управления в объект групповой Политики для домена, файлов ADMX, представленные в этот пакет отвечает за параметры хрома на Windows XP с пакетом обновления 2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ca9de-p107">Chrome comes with its own set of group policy settings which can be downloaded in the form of an ADMX file from [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202). If operating systems Windows Vista/Server 2008 or later are used to manage GPO's for the domain, the ADMX file provided in this package takes care of Chrome settings on Windows XP SP2 or later.</span></span>
  
<span data-ttu-id="ca9de-p108">Скопируйте файл шаблона центральное хранилище для ADMX-файлы на контроллере домена. Для получения дополнительных сведений см [Editing Domain-Based объектов групповой политики с помощью ADMX-файлы](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Центральное хранилище на контроллере — это папка с следующее соглашение об именовании:</span><span class="sxs-lookup"><span data-stu-id="ca9de-p108">Copy the template file to a central store for ADMX files on the domain controller. For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="ca9de-157">**%systemroot%\Sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="ca9de-157">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="ca9de-p109">Каждого, обрабатывающего контроллере домена должны получить отдельную папку. Для копирования файлов ADMX из командной строки можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ca9de-p109">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="ca9de-160">Откройте консоль управления групповой политикой (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.</span><span class="sxs-lookup"><span data-stu-id="ca9de-160">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="ca9de-161">Убедитесь, что в разделе Административные шаблоны обоих Конфигурация пользователя/компьютера отображаются следующие папки: Google Chrome и Google Chrome - параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca9de-161">Make sure the following folders appear in the Administrative Templates section of both User/Computer Configuration: Google Chrome and Google Chrome - Default Settings.</span></span>
    
  - <span data-ttu-id="ca9de-162">Предопределенные параметры первый раздел и локальных администраторов не сможет изменить их в браузере.</span><span class="sxs-lookup"><span data-stu-id="ca9de-162">The settings of the first section are fixed and local administrators won't be able to change them in the browser.</span></span>
    
  - <span data-ttu-id="ca9de-163">Можно изменить параметры последнем разделе политик пользователями в настройки браузера.</span><span class="sxs-lookup"><span data-stu-id="ca9de-163">The settings of the latter section of policies can be changed by users in the browser settings.</span></span>
    
3. <span data-ttu-id="ca9de-164">Перейдите к \*\* \<компьютера или пользователя\> Chrome\Default Templates\Google Конфигурация пользователя\Административные поставщика поиска\*\*</span><span class="sxs-lookup"><span data-stu-id="ca9de-164">Navigate to **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default search provider**</span></span>
    
4. <span data-ttu-id="ca9de-165">Дважды щелкните **Включить службу поиска по умолчанию**и задайте для него значение **включено**.</span><span class="sxs-lookup"><span data-stu-id="ca9de-165">Double-click **Enable the default search provider**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="ca9de-166">Дважды щелкните **значок поставщика поиска по умолчанию**, задайте для него значение **Enabled**и введите`https://www.bing.com/sa/simg/bb.ico`</span><span class="sxs-lookup"><span data-stu-id="ca9de-166">Double-click **Default search provider icon**, set it to **Enabled**, and enter `https://www.bing.com/sa/simg/bb.ico`</span></span>
    
6. <span data-ttu-id="ca9de-167">Дважды щелкните значок **мгновенного URL-адреса поиска поставщика по умолчанию**и введите`https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="ca9de-167">Double-click **Default search provider instant URL**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
7. <span data-ttu-id="ca9de-168">Дважды щелкните **имя поставщика поиска по умолчанию**, задайте для него значение Enabled и введите «Microsoft поиска в Bing»</span><span class="sxs-lookup"><span data-stu-id="ca9de-168">Double-click **Default search provider name**, set it to Enabled, and enter 'Microsoft Search in Bing'</span></span>
    
8. <span data-ttu-id="ca9de-169">Дважды щелкните значок **по умолчанию URL-адреса поиска поставщика поиска**, задайте для него значение **Enabled**и введите`https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="ca9de-169">Double-click **Default search provider search URL**, set it to **Enabled**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
9. <span data-ttu-id="ca9de-170">Дважды щелкните значок **службы поиска по умолчанию предложить URL-адрес**, задайте для него значение **Enabled**и введите`https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span><span class="sxs-lookup"><span data-stu-id="ca9de-170">Double-click **Default search provider suggest URL**, set it to **Enabled**, and enter `https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span></span>
    
10. <span data-ttu-id="ca9de-171">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="ca9de-171">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="ca9de-p110">Установка по умолчанию поисковая система добавит функции предложения поиска Microsoft Search в адресной строке браузера. На данный момент поддерживает только закладки. Пользователи будут видеть верхней предложений два закладку выше предложений общедоступных веб, как они введите в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="ca9de-p110">Setting the default search engine will add the Microsoft Search search suggestions feature in the browser address bar. Currently, this supports bookmarks only. Users will see the top two bookmark suggestions above public web suggestions as they type in the address bar.</span></span>