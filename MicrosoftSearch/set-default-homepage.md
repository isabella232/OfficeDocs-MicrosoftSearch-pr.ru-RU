---
title: Установка домашней страницы по умолчанию
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
ms.assetid: c020bd72-9906-4dfd-bc77-57287f5927ce
ROBOTS: NOINDEX
description: Узнайте, как установить Bing в качестве домашней страницы по умолчанию для организации при использовании Поиска (Майкрософт).
ms.openlocfilehash: 707b6fefe1bd3e096f758df92fedca28f3f1530a
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639832"
---
# <a name="make-bingcom-the-default-home-page"></a><span data-ttu-id="37e48-103">Настройка Bing.com в качестве домашней страницы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37e48-103">Make Bing.com the default home page</span></span>

<span data-ttu-id="37e48-104">В этой статье описывается, как настроить Bing.com в качестве домашней страницы по умолчанию для браузеров Microsoft Edge, Google Chrome и Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="37e48-104">This article explains how to set Bing.com as the default home page for Microsoft Edge, Google Chrome, and Internet Explorer browsers.</span></span> 
  
 
## <a name="microsoft-edge-on-windows-10-version-1511-or-later"></a><span data-ttu-id="37e48-105">Microsoft Edge в Windows 10 версии 1511 или более поздней</span><span class="sxs-lookup"><span data-stu-id="37e48-105">Microsoft Edge on Windows 10, Version 1511 or later</span></span>

<span data-ttu-id="37e48-106">Пользователи не смогут изменить настройку после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="37e48-106">Users won't be able to change the search provider after this policy is set.</span></span> 

1. <span data-ttu-id="37e48-107">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="37e48-107">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span> 
1. <span data-ttu-id="37e48-108">Перейдите к разделу **Administrative Templates\Windows Components\Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="37e48-108">Navigate to **Administrative Templates\Windows Components\Microsoft Edge**</span></span>    
1. <span data-ttu-id="37e48-109">Дважды щелкните параметр **Configure Start pages** (Настройка начальных страниц), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/business`</span><span class="sxs-lookup"><span data-stu-id="37e48-109">Double-click **Configure Start pages**, set it to **Enabled**, and enter `https://www.bing.com/business`</span></span>
1.  <span data-ttu-id="37e48-110">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="37e48-110">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>

  
## <a name="google-chrome-on-windows-xp-sp2-or-later"></a><span data-ttu-id="37e48-111">Google Chrome в Windows XP с пакетом обновления 2 (SP2) или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="37e48-111">Google Chrome on Windows XP SP2 or later</span></span>


<span data-ttu-id="37e48-112">Статью службы поддержки Майкрософт об управлении ADMX-файлами и последние версии ADMX-файлов для разных версий Windows можно найти [на сайте службы поддержки Майкрософт](https://support.microsoft.com/ru-RU/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span><span class="sxs-lookup"><span data-stu-id="37e48-112">The Windows Support article on managing ADMX files and the latest ADMX files for different versions of Windows can be found [on Microsoft Support](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>

<span data-ttu-id="37e48-113">Вам также потребуется последняя версия файла политики Google, который можно найти на сайте [справки Google Chrome Enterprise](https://support.google.com/chrome/a/answer/187202).</span><span class="sxs-lookup"><span data-stu-id="37e48-113">You'll also need the latest Google policy file, which you can find on [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span>
  
<span data-ttu-id="37e48-p101">Если в GPMC не удается найти параметры, описанные в этом разделе, скачайте соответствующие ADMX-файлы и скопируйте их в [центральное хранилище](https://docs.microsoft.com/ru-RU/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Центральное хранилище на контроллере — это папка с указанными ниже правилами именования:</span><span class="sxs-lookup"><span data-stu-id="37e48-p101">If the settings described in this section can't be found inside of GPMC, download the appropriate ADMX and copy them to the [central store](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="37e48-116">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="37e48-116">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="37e48-p102">Все домены, обслуживаемые контроллером, должны получить отдельную папку. Чтобы скопировать ADMX-файл из командной строки, можно использовать указанную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="37e48-p102">Each domain your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="37e48-119">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="37e48-119">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
1. <span data-ttu-id="37e48-120">Проверьте, что в разделе **Administrative Templates** (Административные шаблоны) для обеих конфигураций *User/Computer Configuration* (Конфигурация пользователя/компьютера) отображаются следующие папки: Google Chrome и Google Chrome – Default Settings (могут переопределяться пользователями).</span><span class="sxs-lookup"><span data-stu-id="37e48-120">Make sure the following folders appear in the **Administrative Templates** section of both *User/Computer Configuration*: Google Chrome and Google Chrome - Default Settings (users can override).</span></span>
   - <span data-ttu-id="37e48-121">Параметры первого раздела являются фиксированными, и локальный администратор не сможет их изменить.</span><span class="sxs-lookup"><span data-stu-id="37e48-121">The settings of the first section are fixed and the local administrator won't be able to change them.</span></span>
   - <span data-ttu-id="37e48-p103">Параметры последнего раздела политик могут изменяться пользователями в настройках браузера. Вы должны решить, могут ли пользователи переопределять параметр, установленный по умолчанию. В приведенных ниже действиях выполняются изменения параметра в папке в соответствии с политикой и потребностями организации. В указанных ниже действиях используются стандартные параметры Google Chrome в качестве параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37e48-p103">The settings of the latter section of policies can be changed by users in their browser settings. You should decide if users can override your default setting. In the following steps, change in the setting in the folder that corresponds to your organization policy and needs. The steps below use the Google Chrome - Default Settings as the default.</span></span>

1. <span data-ttu-id="37e48-126">Перейдите к разделу **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\Home Page**.</span><span class="sxs-lookup"><span data-stu-id="37e48-126">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\Home Page**.</span></span> 
1. <span data-ttu-id="37e48-127">Дважды щелкните параметр **Use New Tab Page as homepage** (Использовать новую вкладку в качестве домашней страницы) и установите для него значение **Enabled** (Включено).</span><span class="sxs-lookup"><span data-stu-id="37e48-127">Double-click **Use New Tab Page as homepage**, and set it to **Enabled**.</span></span> 
1. <span data-ttu-id="37e48-128">Перейдите к разделу **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\New Tab Page**.</span><span class="sxs-lookup"><span data-stu-id="37e48-128">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\New Tab Page**.</span></span> 
1. <span data-ttu-id="37e48-129">Дважды щелкните параметр **Configure the New Tab Page URL** (Настройка URL-адреса новой вкладки), установите для него значение **Enabled** (Включено) и введите `https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="37e48-129">Double-click **Configure the New Tab Page URL**, set it to **Enabled**, and enter `https://www.bing.com/business?form=BFBSPR`</span></span> 
1. <span data-ttu-id="37e48-130">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="37e48-130">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>

## <a name="internet-explorer-50-or-later"></a><span data-ttu-id="37e48-131">Internet Explorer 5.0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="37e48-131">Internet Explorer 5.0 or later</span></span>
<span data-ttu-id="37e48-132">Пользователи по-прежнему смогут сменить домашнюю страницу после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="37e48-132">Users can still change the homepage after this policy is set.</span></span> 

1. <span data-ttu-id="37e48-133">Откройте консоль управления групповыми политиками (gpmc.msc) и перейдите к редактированию любой существующей политики или созданию новой.</span><span class="sxs-lookup"><span data-stu-id="37e48-133">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="37e48-134">Перейдите к разделу **User Configuration\Preferences\Control Panel Settings\Internet Settings**.</span><span class="sxs-lookup"><span data-stu-id="37e48-134">Navigate to **User Configuration\Preferences\Control Panel Settings\Internet Settings**.</span></span>
    
3. <span data-ttu-id="37e48-135">Щелкните правой кнопкой мыши **Internet Settings** (Параметры Интернета) и выберите **Internet Explorer 10**.</span><span class="sxs-lookup"><span data-stu-id="37e48-135">Right-click on **Internet Settings** and select **Internet Explorer 10**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="37e48-136">Необходимо выбрать параметр Internet Explorer 10, чтобы применить настройки для Internet Explorer 11, так как для него применяются такие же настройки.</span><span class="sxs-lookup"><span data-stu-id="37e48-136">You need to select the option of Internet Explorer 10 to apply the settings for Internet Explorer 11 as the same settings apply to Internet Explorer 11.</span></span> 
  
4. <span data-ttu-id="37e48-p104">Параметры, подчеркнутые красным, не настроены на целевом компьютере, а подчеркнутые зеленым — настроены. Чтобы изменить подчеркивание, используйте указанные ниже функциональные клавиши:</span><span class="sxs-lookup"><span data-stu-id="37e48-p104">Settings which are underlined in red are not configured at the target machine, while settings underlined in green are configured at the target machine. To change the underlining, use the following function keys:</span></span>
    
    <span data-ttu-id="37e48-139">F5 — включение всех параметров на текущей вкладке</span><span class="sxs-lookup"><span data-stu-id="37e48-139">F5 - Enable all settings on the current tab</span></span>
    
    <span data-ttu-id="37e48-140">F6 — включение выбранных параметров</span><span class="sxs-lookup"><span data-stu-id="37e48-140">F6 - Enable the currently selected setting</span></span>
    
    <span data-ttu-id="37e48-141">F7 — отключение выбранных параметров</span><span class="sxs-lookup"><span data-stu-id="37e48-141">F7 - Disable the currently selected setting</span></span>
    
    <span data-ttu-id="37e48-142">F8 — отключение всех параметров на текущей вкладке</span><span class="sxs-lookup"><span data-stu-id="37e48-142">F8 - Disable all settings on the current tab</span></span>
    
5. <span data-ttu-id="37e48-p105">Нажмите клавишу **F8**, чтобы отключить все параметры перед выполнение любой настройки. Экран должен выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="37e48-p105">Press **F8** to disable all settings before configuring anything. The screen should look like this:</span></span> 
    
    ![Диалоговое окно свойств Internet Explorer 10](media/2fd55755-5007-4e33-a795-c42ce2fcef4a.jpg)
  
6. <span data-ttu-id="37e48-146">Нажмите клавишу **F6** в параметрах домашней страницы и введите `https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="37e48-146">Press **F6** on the Home page setting and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="37e48-147">Примените полученный объект групповой политики, привязав его к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="37e48-147">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>