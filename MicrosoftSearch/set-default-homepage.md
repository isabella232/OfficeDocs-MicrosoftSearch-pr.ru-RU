---
title: Задать домашнюю страницу по умолчанию
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
ms.assetid: c020bd72-9906-4dfd-bc77-57287f5927ce
description: Узнайте, как установить Bing в качестве главной страницы по умолчанию для поиска Microsoft для вашей организации.
ms.openlocfilehash: 9190e607f5e17a0b898ab131886de12cb300a74c
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "29379120"
---
# <a name="set-default-homepage"></a><span data-ttu-id="52393-103">Задать домашнюю страницу по умолчанию</span><span class="sxs-lookup"><span data-stu-id="52393-103">Set default homepage</span></span>

<span data-ttu-id="52393-104">Настройка браузера по умолчанию, поисковую систему по умолчанию и главной страницы по умолчанию поможет пользователям обнаружения возможностей поиска Microsoft, рекомендуем Дополнительные об использовании и предоставление облегчению интерфейса.</span><span class="sxs-lookup"><span data-stu-id="52393-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search  capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="52393-105">Чтобы задать главной страницы по умолчанию для вашей организации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="52393-105">To set the default homepage for your organization, follow the steps below.</span></span>
  
## <a name="internet-explorer"></a><span data-ttu-id="52393-106">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="52393-106">Internet Explorer</span></span>

### <a name="internet-explorer-50-or-later"></a><span data-ttu-id="52393-107">Internet Explorer версии 5.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="52393-107">Internet Explorer 5.0 or later</span></span>

1. <span data-ttu-id="52393-108">Откройте консоль управления групповой политикой (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.</span><span class="sxs-lookup"><span data-stu-id="52393-108">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="52393-109">Перейдите к **настройки Settings\Internet панели Configuration\Preferences\Control пользователя**.</span><span class="sxs-lookup"><span data-stu-id="52393-109">Navigate to **User Configuration\Preferences\Control Panel Settings\Internet Settings**.</span></span>
    
3. <span data-ttu-id="52393-110">Щелкните правой кнопкой мыши на **Параметры Интернета** и выберите **Internet Explorer 10**.</span><span class="sxs-lookup"><span data-stu-id="52393-110">Right-click on **Internet Settings** and select **Internet Explorer 10**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="52393-111">Необходимо выбрать параметр Internet Explorer 10 для применения параметров для Internet Explorer 11 как те же параметры применяются к Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="52393-111">You need to select the option of Internet Explorer 10 to apply the settings for Internet Explorer 11 as the same settings apply to Internet Explorer 11.</span></span> 
  
4. <span data-ttu-id="52393-p101">Параметры, которые подчеркиваются красным цветом не настроены на конечном компьютере во время настройки параметров подчеркнуто зеленым цветом на целевом компьютере. Чтобы изменить подчеркивание, используйте следующие функциональные клавиши:</span><span class="sxs-lookup"><span data-stu-id="52393-p101">Settings which are underlined in red are not configured at the target machine, while settings underlined in green are configured at the target machine. To change the underlining, use the following function keys:</span></span>
    
    <span data-ttu-id="52393-114">F5 - включить все параметры на вкладке текущий</span><span class="sxs-lookup"><span data-stu-id="52393-114">F5 - Enable all settings on the current tab</span></span>
    
    <span data-ttu-id="52393-115">F6 - включить параметр выделенный в текущий момент</span><span class="sxs-lookup"><span data-stu-id="52393-115">F6 - Enable the currently selected setting</span></span>
    
    <span data-ttu-id="52393-116">F7 - отключить параметр выделенный в текущий момент</span><span class="sxs-lookup"><span data-stu-id="52393-116">F7 - Disable the currently selected setting</span></span>
    
    <span data-ttu-id="52393-117">F8 - отключение всех параметров на вкладке текущей</span><span class="sxs-lookup"><span data-stu-id="52393-117">F8 - Disable all settings on the current tab</span></span>
    
5. <span data-ttu-id="52393-p102">Нажмите клавишу **F8** , чтобы отключить все параметры, прежде чем настраивать все действия. Экран должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="52393-p102">Press **F8** to disable all settings before configuring anything. The screen should look like this:</span></span> 
    
    ![Диалоговое окно Свойства Internet Explorer 10](media/2fd55755-5007-4e33-a795-c42ce2fcef4a.jpg)
  
6. <span data-ttu-id="52393-121">На странице параметров домашней страницы, нажмите клавишу **F6** и введите`https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="52393-121">Press **F6** on the Home page setting and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="52393-122">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="52393-122">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!NOTE]
> <span data-ttu-id="52393-123">Пользователи могут изменять домашнюю страницу после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="52393-123">Users can still change the homepage after this policy is set.</span></span> 
  
## <a name="microsoft-edge"></a><span data-ttu-id="52393-124">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="52393-124">Microsoft Edge</span></span>

### <a name="windows-10-version-1511-or-later"></a><span data-ttu-id="52393-125">10 Windows, 1511 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="52393-125">Windows 10, Version 1511 or later</span></span>

1. <span data-ttu-id="52393-126">Откройте консоль управления групповой политикой (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.</span><span class="sxs-lookup"><span data-stu-id="52393-126">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="52393-127">Выберите пункты **Административные шаблоны\Компоненты Components\Microsoft пограничного сервера**</span><span class="sxs-lookup"><span data-stu-id="52393-127">Navigate to **Administrative Templates\Windows Components\Microsoft Edge**</span></span>
    
1. <span data-ttu-id="52393-128">Дважды щелкните **Настройка домашних страниц**, задайте для него значение **Enabled**и введите`https://www.bing.com/business`</span><span class="sxs-lookup"><span data-stu-id="52393-128">Double-click **Configure Start pages**, set it to **Enabled**, and enter `https://www.bing.com/business`</span></span>
    
3. <span data-ttu-id="52393-129">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="52393-129">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="52393-130">Пользователи не смогут изменять службу поиска после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="52393-130">Users won't be able to change the search provider after this policy is set.</span></span> 
  
## <a name="google-chrome"></a><span data-ttu-id="52393-131">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="52393-131">Google Chrome</span></span>

### <a name="windows-xp-sp2-or-later"></a><span data-ttu-id="52393-132">Windows XP с пакетом обновления 2 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="52393-132">Windows XP SP2 or later</span></span>

<span data-ttu-id="52393-133">Статьи технической поддержки по управлению ADMX-файлы и последние ADMX-файлы для различных версий Windows можно найти [в службу технической поддержки Майкрософт](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span><span class="sxs-lookup"><span data-stu-id="52393-133">The Windows Support article on managing ADMX files and the latest ADMX files for different versions of Windows can be found [on Microsoft Support](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>

<span data-ttu-id="52393-134">Вам также понадобится последние Google файл политики, можно найти на [Google Chrome Enterprise справки](https://support.google.com/chrome/a/answer/187202).</span><span class="sxs-lookup"><span data-stu-id="52393-134">You'll also need the latest Google policy file, which you can find on [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span>
  
<span data-ttu-id="52393-p103">Если параметры, описанные в этом разделе не удается найти в консоли управления групповыми Политиками, загрузите соответствующий ADMX и копировать их в [центральном хранилище](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Центральное хранилище на контроллере — это папка с следующее соглашение об именовании:</span><span class="sxs-lookup"><span data-stu-id="52393-p103">If the settings described in this section can't be found inside of GPMC, download the appropriate ADMX and copy them to the [central store](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="52393-137">**%systemroot%\Sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="52393-137">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="52393-p104">Каждый домен дескрипторам контроллера должны получить отдельную папку. Для копирования файлов ADMX из командной строки можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="52393-p104">Each domain your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="52393-140">Откройте консоль управления групповой политикой (gpmc.msc) и перейдите в редактирования любые существующие политики или создать новый.</span><span class="sxs-lookup"><span data-stu-id="52393-140">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="52393-141">Убедитесь, что в разделе **Административные шаблоны** обоих *Конфигурация пользователя/компьютера*отображаются следующие папки: Google Chrome и Google Chrome - параметры по умолчанию (пользователи могут переопределить).</span><span class="sxs-lookup"><span data-stu-id="52393-141">Make sure the following folders appear in the **Administrative Templates** section of both *User/Computer Configuration*: Google Chrome and Google Chrome - Default Settings (users can override).</span></span>
    
   - <span data-ttu-id="52393-142">Предопределенные параметры первый раздел и локальный администратор не может быть могли их изменять.</span><span class="sxs-lookup"><span data-stu-id="52393-142">The settings of the first section are fixed and the local administrator won't be able to change them.</span></span>
    
   - <span data-ttu-id="52393-p105">Можно изменить параметры последнем разделе политик пользователями в свои параметры браузера. Следует решить, если пользователи могут переопределить параметры по умолчанию. На следующем этапе перейдите на странице параметров в папке, которая соответствует требований и политики организации. Приведенные ниже действия использовать Google Chrome - параметры по умолчанию значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52393-p105">The settings of the latter section of policies can be changed by users in their browser settings. You should decide if users can override your default setting. In the following steps, change in the setting in the folder that corresponds to your organization policy and needs. The steps below use the Google Chrome - Default Settings as the default.</span></span>
    
3. <span data-ttu-id="52393-147">Перейдите к \*\* &lt;Конфигурация компьютера/пользователя&gt;\Administrative Templates\Google Chrome - страница по умолчанию Settings\Home\*\*.</span><span class="sxs-lookup"><span data-stu-id="52393-147">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\Home Page**.</span></span>
    
4. <span data-ttu-id="52393-148">Дважды щелкните **Страницу новой вкладки используется как главной страницы**и задайте для него значение **включено**.</span><span class="sxs-lookup"><span data-stu-id="52393-148">Double-click **Use New Tab Page as homepage**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="52393-149">Перейдите к \*\* &lt;Конфигурация компьютера/пользователя&gt;\Administrative Templates\Google Chrome - вкладка по умолчанию Settings\New\*\*.</span><span class="sxs-lookup"><span data-stu-id="52393-149">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\New Tab Page**.</span></span>
    
6. <span data-ttu-id="52393-150">Дважды щелкните элемент **Настройка URL-адрес новой страницы вкладки**, задайте для него значение **Enabled**и введите`https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="52393-150">Double-click **Configure the New Tab Page URL**, set it to **Enabled**, and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="52393-151">Обеспечение результирующий объект групповой Политики, путем связывания ее соответствующего домена.</span><span class="sxs-lookup"><span data-stu-id="52393-151">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="52393-152">Пользователи будут иметь возможность изменение домашней страницы после установки этой политики.</span><span class="sxs-lookup"><span data-stu-id="52393-152">Users will be able to change the home page after this policy is set.</span></span>