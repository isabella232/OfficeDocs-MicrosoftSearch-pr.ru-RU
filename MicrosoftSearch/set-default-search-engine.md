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
ms.openlocfilehash: 1ac2f23a8263c01901e252e7dd830e7373380669
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508673"
---
# <a name="make-bing-the-default-search-engine"></a><span data-ttu-id="46b33-103">Установка Bing в качестве поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="46b33-103">Make Bing the default search engine</span></span>
  
<span data-ttu-id="46b33-104">В этой статье описывается, как можно сделать Bing поисковой системой по умолчанию для браузеров Microsoft Edge, Google Chrome и Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="46b33-104">This article explains how you can make Bing the default search engine for Microsoft Edge, Google Chrome, and Internet Explorer.</span></span> 
  
## <a name="microsoft-edge-on-windows-10-version-1703-or-later"></a><span data-ttu-id="46b33-105">Microsoft Edge в Windows 10 версии 1703 или более поздней</span><span class="sxs-lookup"><span data-stu-id="46b33-105">Microsoft Edge on Windows 10, Version 1703 or later</span></span>

<span data-ttu-id="46b33-106">Хотя вы настраиваете Bing в качестве поисковой системы по умолчанию, Microsoft Edge позволяет пользователям изменять свои параметры для использования другой поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="46b33-106">Although you'll set Bing as the default search engine, Microsoft Edge allows users to change their settings to use a different search engine.</span></span>
  
<span data-ttu-id="46b33-107">Последние версии ADMX-файлов для разных версий Windows см. в статье [Как создать центральное хранилище для административных шаблонов групповой политики в Windows и управлять им](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span><span class="sxs-lookup"><span data-stu-id="46b33-107">For the latest ADMX files for various versions of Windows, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>
  
<span data-ttu-id="46b33-108">Если параметр, описанный в этом разделе, не может быть найден внутри GPMC, скачайте соответствующий ADMX и скопируйте их в центральный магазин.</span><span class="sxs-lookup"><span data-stu-id="46b33-108">If the setting described in this section cannot be found inside of GPMC, download the appropriate ADMX and copy them to the central store.</span></span> <span data-ttu-id="46b33-109">Дополнительные сведения см. в Domain-Based [GPOs с помощью ADMX Files.](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)</span><span class="sxs-lookup"><span data-stu-id="46b33-109">For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="46b33-110">Центральный магазин контроллера — это папка со следующей конвенцией именования: **%systemroot%\sysvol \\<\> \policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="46b33-110">Central store on the controller is a folder with the following naming convention: **%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="46b33-p102">Все домены, обслуживаемые контроллером, должны получить отдельную папку. Чтобы скопировать ADMX-файл из командной строки, можно использовать указанную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="46b33-p102">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="46b33-113">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="46b33-113">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one.</span></span>
2. <span data-ttu-id="46b33-114">Перейдите к разделу **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="46b33-114">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span></span>
3. <span data-ttu-id="46b33-115">Дважды щелкните параметр **Set default search engine** (Задать поисковую систему по умолчанию), установите значение **Enabled** (Включено) и введите `https://www.bing.com/sa/osd/bfb.xml`</span><span class="sxs-lookup"><span data-stu-id="46b33-115">Double-click **Set default search engine**, set to **Enabled**, and enter `https://www.bing.com/sa/osd/bfb.xml`</span></span>
4. <span data-ttu-id="46b33-116">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="46b33-116">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>


## <a name="google-chrome-on-windows-10-version-1507-or-later"></a><span data-ttu-id="46b33-117">Google Chrome в Windows 10, Версии 1507 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="46b33-117">Google Chrome on Windows 10, Version 1507 or later</span></span>

<span data-ttu-id="46b33-118">Пользователи не смогут сменить поисковую систему по умолчанию после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="46b33-118">Users won't be able to change the default search engine after this policy is set.</span></span>
  
<span data-ttu-id="46b33-119">Chrome поставляется с собственным набором параметров групповой политики, которые можно скачать в виде ADMX-файла из [google Chrome Enterprise Help.](https://support.google.com/chrome/a/answer/187202)</span><span class="sxs-lookup"><span data-stu-id="46b33-119">Chrome comes with its own set of group policy settings which can be downloaded in the form of an ADMX file from [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span>
  
<span data-ttu-id="46b33-120">Скопируйте файл шаблона в центральный магазин файлов ADMX на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="46b33-120">Copy the template file to a central store for ADMX files on the domain controller.</span></span> <span data-ttu-id="46b33-121">Дополнительные сведения см. в Domain-Based [GPOs с помощью ADMX Files.](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)</span><span class="sxs-lookup"><span data-stu-id="46b33-121">For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="46b33-122">Центральный магазин контроллера — это папка со следующей конвенцией именования: **%systemroot%\sysvol \\<\> \policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="46b33-122">Central store on the controller is a folder with the following naming convention: **%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="46b33-p104">Все домены, обслуживаемые контроллером, должны получить отдельную папку. Чтобы скопировать ADMX-файл из командной строки, можно использовать указанную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="46b33-p104">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="46b33-125">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="46b33-125">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
2. <span data-ttu-id="46b33-126">Проверьте, что в разделе Administrative Templates (Административные шаблоны) для обеих конфигураций User/Computer Configuration (Конфигурация пользователя/компьютера) отображаются следующие папки: Google Chrome и Google Chrome – Default Settings.</span><span class="sxs-lookup"><span data-stu-id="46b33-126">Make sure the following folders appear in the Administrative Templates section of both User/Computer Configuration: Google Chrome and Google Chrome - Default Settings.</span></span>

    - <span data-ttu-id="46b33-127">Параметры первого раздела являются фиксированными, и локальные администраторы не смогут их изменять в браузере.</span><span class="sxs-lookup"><span data-stu-id="46b33-127">The settings of the first section are fixed and local administrators won't be able to change them in the browser.</span></span>
    - <span data-ttu-id="46b33-128">Параметры последнего раздела политик могут изменяться пользователями в настройках браузера.</span><span class="sxs-lookup"><span data-stu-id="46b33-128">The settings of the latter section of policies can be changed by users in the browser settings.</span></span>

3. <span data-ttu-id="46b33-129">Перейдите к **\<Computer/User\> configuration\Administrative Templates\Google Chrome\Default search provider**</span><span class="sxs-lookup"><span data-stu-id="46b33-129">Navigate to **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default search provider**</span></span>
4. <span data-ttu-id="46b33-130">Дважды щелкните параметр **Enable the default search provider** (Включить поставщика поиска по умолчанию) и установите для него значение **Enabled** (Включено).</span><span class="sxs-lookup"><span data-stu-id="46b33-130">Double-click **Enable the default search provider**, and set it to **Enabled**.</span></span>
5. <span data-ttu-id="46b33-131">Дважды щелкните параметр **Default search provider icon** (Значок поставщика поиска по умолчанию), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/sa/simg/bb.ico`</span><span class="sxs-lookup"><span data-stu-id="46b33-131">Double-click **Default search provider icon**, set it to **Enabled**, and enter `https://www.bing.com/sa/simg/bb.ico`</span></span>
6. <span data-ttu-id="46b33-132">Дважды щелкните параметр **Default search provider instant URL** (URL-адрес для быстрого поиска поставщика поиска по умолчанию) и введите `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="46b33-132">Double-click **Default search provider instant URL**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
7. <span data-ttu-id="46b33-133">Дважды щелкните параметр **Default search provider name** (Имя поставщика поиска по умолчанию), установите для него значение Enabled (Включено) и введите "Поиск (Майкрософт) в Bing"</span><span class="sxs-lookup"><span data-stu-id="46b33-133">Double-click **Default search provider name**, set it to Enabled, and enter 'Microsoft Search in Bing'</span></span>
8. <span data-ttu-id="46b33-134">Дважды щелкните параметр **Default search provider search URL** (Поисковый URL-адрес поставщика поиска по умолчанию), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="46b33-134">Double-click **Default search provider search URL**, set it to **Enabled**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
9. <span data-ttu-id="46b33-135">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="46b33-135">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>

## <a name="internet-explorer-11-or-later"></a><span data-ttu-id="46b33-136">Internet Explorer 11 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="46b33-136">Internet Explorer 11 or later</span></span>

<span data-ttu-id="46b33-137">Пользователи смогут сменить поставщика поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="46b33-137">Users will be able to change the search provider after this policy is set.</span></span>
  
### <a name="step-1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a><span data-ttu-id="46b33-138">ШАГ 1.</span><span class="sxs-lookup"><span data-stu-id="46b33-138">STEP 1.</span></span> <span data-ttu-id="46b33-139">Настройка локального компьютера, который будет использоваться для задания объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="46b33-139">Configure the local machine that will be used to set the GPO</span></span>

<span data-ttu-id="46b33-140">Вставьте указанный ниже текст в REG-файл (\*.reg).</span><span class="sxs-lookup"><span data-stu-id="46b33-140">Paste the following text into a reg(\*.reg) file.</span></span>
  
<span data-ttu-id="46b33-141">Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="46b33-141">Windows Registry Editor Version 5.00</span></span>
  
<pre>[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes]
"DefaultScope"="{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}"
[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes\{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}]
"Codepage"=dword:0000fde9
"DisplayName"="Microsoft Search in Bing"
"OSDFileURL"="https://www.bing.com/sa/osd/bfb.xml"
"FaviconURL"="https://www.bing.com/sa/simg/bb.ico"
"URL"="https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR"</pre>
  
<span data-ttu-id="46b33-p106">Дважды щелкните созданный файл и выполните действия для импорта файла. После успешного выполнения импорта появится указанное ниже диалоговое окно:</span><span class="sxs-lookup"><span data-stu-id="46b33-p106">Double-click the file created and follow the steps to import the file. A successful import should result in the following dialog:</span></span>
  
![Сообщение об успешном импорте в редактор реестра](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
### <a name="step-2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a><span data-ttu-id="46b33-145">ШАГ 2.</span><span class="sxs-lookup"><span data-stu-id="46b33-145">STEP 2.</span></span> <span data-ttu-id="46b33-146">Открытие консоли управления групповыми политиками (gpmc.msc) и переход к редактированию любой существующей политики или созданию новой</span><span class="sxs-lookup"><span data-stu-id="46b33-146">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one</span></span>

1. <span data-ttu-id="46b33-147">Перейдите к разделу **User Configuration\Policies\Preferences\Windows Settings**.</span><span class="sxs-lookup"><span data-stu-id="46b33-147">Navigate to **User Configuration\Policies\Preferences\Windows Settings**.</span></span>
2. <span data-ttu-id="46b33-p108">Щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра). В окне браузера реестра выберите **Local Computer** (Локальный компьютер) и нажмите кнопку **Next** (Далее).</span><span class="sxs-lookup"><span data-stu-id="46b33-p108">Right-click on **Registry\New** and select **Registry Wizard**. From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
3. <span data-ttu-id="46b33-150">Перейдите к разделу **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span><span class="sxs-lookup"><span data-stu-id="46b33-150">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span></span>
4. <span data-ttu-id="46b33-151">В этом разделе обязательно выберите имя DefaultScope.</span><span class="sxs-lookup"><span data-stu-id="46b33-151">From this key, make sure to select DefaultScope.</span></span>

    ![Браузер реестра с выбранным именем DefaultScope](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
5. <span data-ttu-id="46b33-p109">Проверьте все подразделы, содержащие идентификатор GUID для Поиска (Майкрософт) в Bing, и каждое значение в разделе, кроме путей к профилям пользователей. Прокрутите вниз, чтобы выбрать другие элементы.</span><span class="sxs-lookup"><span data-stu-id="46b33-p109">Check all sub keys containing the GUID for Microsoft Search in Bing and every value under the key except any path to user profiles. Scroll down to select other items.</span></span>
6. <span data-ttu-id="46b33-155">Нажмите кнопку "Готово", чтобы завершить настройку.</span><span class="sxs-lookup"><span data-stu-id="46b33-155">Click Finish to complete this configuration.</span></span>

### <a name="step-3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a><span data-ttu-id="46b33-156">ШАГ 3.</span><span class="sxs-lookup"><span data-stu-id="46b33-156">STEP 3.</span></span> <span data-ttu-id="46b33-157">Настройка параметров пользователя для устранения предупреждения, которое может появляться при применении поиска DefaultScope</span><span class="sxs-lookup"><span data-stu-id="46b33-157">Set up User Preferences to help eliminate a warning the user may get when DefaultScope search is enforced</span></span>

<span data-ttu-id="46b33-158">Это предупреждение является стандартным и уведомляет пользователей о программе, пытающейся изменить настройки.</span><span class="sxs-lookup"><span data-stu-id="46b33-158">This warning is by design and alerts users of a program trying to modify their settings.</span></span>
  
1. <span data-ttu-id="46b33-159">В том же объекте групповой политики щелкните правой кнопкой мыши **Registry\New** (Реестр\Создать) и выберите **Registry Wizard** (Мастер реестра).</span><span class="sxs-lookup"><span data-stu-id="46b33-159">Within the same GPO, right click on **Registry\New** and select **Registry Wizard**.</span></span>
2. <span data-ttu-id="46b33-160">Перейдите к разделу **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span><span class="sxs-lookup"><span data-stu-id="46b33-160">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span></span>
3. <span data-ttu-id="46b33-161">Выберите раздел **User Preference** (Параметры пользователя).</span><span class="sxs-lookup"><span data-stu-id="46b33-161">Select the **User Preference** key.</span></span>
4. <span data-ttu-id="46b33-162">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="46b33-162">Click **Finish**.</span></span>
5. <span data-ttu-id="46b33-p111">Щелкните созданный объект. В области справа дважды щелкните объект параметров пользователя и измените **Action** (Действие) на **Delete and Save** (Удалить и сохранить).</span><span class="sxs-lookup"><span data-stu-id="46b33-p111">Click on the newly created object. On the right-side pane double click on the User Preferences object, change the **Action** to **Delete and Save**.</span></span>
6. <span data-ttu-id="46b33-165">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="46b33-165">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
