---
title: Управление полем поиска на сайтах SharePoint
ms.author: keremy
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
description: Настройка работы с полем поиска на сайтах SharePoint
ms.openlocfilehash: c58e7cf0a47d22fa9c6fd3abd93cc97087625690
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031362"
---
# <a name="search-box-settings-on-sharepoint-sites"></a><span data-ttu-id="e989e-103">Параметры поле поиска на сайтах SharePoint</span><span class="sxs-lookup"><span data-stu-id="e989e-103">Search box settings on SharePoint sites</span></span>

<span data-ttu-id="e989e-104">Один из нескольких способов настройки microsoft Search на сайтах SharePoint — это настройка работы окна поиска в панели навигации пакетов на сайтах SharePoint с учетом ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="e989e-104">One of the several ways Microsoft Search can be customized on SharePoint sites is to tailor how the search box in the suite navigation bar works in SharePoint sites to best fit your needs.</span></span>

<span data-ttu-id="e989e-105">Другие параметры настройки см. в странице Изменение страницы результатов [поиска Майкрософт,](customize-search-page.md)чтобы добавить настраиваемые вертикали, типы результатов и макеты и создать настраиваемую страницу [результатов поиска.](create-search-results-pages.md)</span><span class="sxs-lookup"><span data-stu-id="e989e-105">For other customization options, see [Changing the Microsoft Search results page to add custom verticals, result types and layouts](customize-search-page.md), and [Creating a custom search results page](create-search-results-pages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e989e-106">Поле поиска панели навигации suite доступно не для всех клиентов в настоящее время, но эти параметры все еще можно установить сейчас, и они вступает в силу, когда он станет доступен.</span><span class="sxs-lookup"><span data-stu-id="e989e-106">The suite navigation bar search box is not available for all customers at this time, but these options can still be set now and they will take effect when it becomes available.</span></span>

<span data-ttu-id="e989e-107">Для задач, перечисленных ниже, вы будете использовать PowerShell с расширениями SharePoint PnP PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e989e-107">For the tasks listed below, you will use PowerShell with SharePoint PnP PowerShell extensions.</span></span> <span data-ttu-id="e989e-108">Вы можете установить и узнать больше о том, как начать [работу здесь](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="e989e-108">You can install and learn more about how to get started [here](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span></span> <span data-ttu-id="e989e-109">Вы вопишитесь в свою коллекцию сайтов или сайтов с помощью этой команды:</span><span class="sxs-lookup"><span data-stu-id="e989e-109">You will sign into your site or site collection using this command:</span></span>

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign into your site. Use the site owner credentials 
```

## <a name="changing-the-scope-of-search"></a><span data-ttu-id="e989e-110">Изменение области поиска</span><span class="sxs-lookup"><span data-stu-id="e989e-110">Changing the scope of search</span></span>

<span data-ttu-id="e989e-111">При создании нового сайта в SharePoint Online и введите его в поле поиска, вы переназначитесь на страницу результатов поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e989e-111">When you create a new site in SharePoint Online today, and type into the search box, you are taken to the Microsoft Search results page.</span></span> <span data-ttu-id="e989e-112">На этой странице показаны результаты текущего сайта по умолчанию, что позволяет расширить область поиска до центра, с чем связан текущий сайт (если он есть) или всей организации.</span><span class="sxs-lookup"><span data-stu-id="e989e-112">This page shows results from your current site by default and allows you to expand the scope of your search to the hub that the current site is associated with (if there is one), or to the whole organization.</span></span>

<span data-ttu-id="e989e-113">Область, которая используется полем поиска, по умолчанию зависит от типа сайта.</span><span class="sxs-lookup"><span data-stu-id="e989e-113">The scope the search box uses, by default, depends on type of site.</span></span>

* <span data-ttu-id="e989e-114">Регулярный поиск сайтов по текущему сайту.</span><span class="sxs-lookup"><span data-stu-id="e989e-114">Regular sites search over the current site.</span></span>
* <span data-ttu-id="e989e-115">Сайты-концентраторы ищут все сайты в центре.</span><span class="sxs-lookup"><span data-stu-id="e989e-115">Hub sites search over all sites in the hub.</span></span>
* <span data-ttu-id="e989e-116">Домашние сайты ищут все содержимое.</span><span class="sxs-lookup"><span data-stu-id="e989e-116">Home sites search over all content.</span></span>

<span data-ttu-id="e989e-117">В некоторых случаях может потребоваться изменить эти значения по умолчанию, чтобы всегда искать по всей организации или по всему центру, с чем связан сайт, без необходимости дополнительного щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="e989e-117">In some cases, you may want to change these defaults to always search over the whole organization, or across the hub a site is associated with, without needing an additional click.</span></span>

<span data-ttu-id="e989e-118">Как владелец сайта вы можете изменить эти по умолчанию с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="e989e-118">As a site owner, you can change these defaults using the following command:</span></span>

```powershell
Set-PnPSearchSettings -SearchScope Tenant
# DefaultScope | Hub | Site | Tenant
```

<span data-ttu-id="e989e-119">После запуска этой команды сайт, который ранее показывал результаты текущего сайта по умолчанию, начнет показывать результаты всей организации.</span><span class="sxs-lookup"><span data-stu-id="e989e-119">After running this command, the site that was previously showing results from the current site by default will start to show results from the whole organization.</span></span>

<span data-ttu-id="e989e-120">Чтобы вернуться к параметру по умолчанию, снова запустите команду со значением "DefaultScope".</span><span class="sxs-lookup"><span data-stu-id="e989e-120">To go back to the default setting, run the command again with the value “DefaultScope".</span></span> <span data-ttu-id="e989e-121">Для поиска в концентраторе используйте значение "Концентратор" в качестве значения SearchScope.</span><span class="sxs-lookup"><span data-stu-id="e989e-121">To search across the Hub, use “Hub” as the SearchScope value.</span></span>

<span data-ttu-id="e989e-122">Этот параметр применяется на уровне отдельного сайта.</span><span class="sxs-lookup"><span data-stu-id="e989e-122">This setting applies at the individual site level.</span></span> <span data-ttu-id="e989e-123">Эквивалентных параметров для коллекций сайтов нет.</span><span class="sxs-lookup"><span data-stu-id="e989e-123">There is no equivalent setting for site collections.</span></span>

## <a name="show-or-hide-the-search-box"></a><span data-ttu-id="e989e-124">Показать или скрыть поле поиска</span><span class="sxs-lookup"><span data-stu-id="e989e-124">Show or hide the search box</span></span>

<span data-ttu-id="e989e-125">Вы можете скрыть поле поиска панели навигации пакетов, если вы хотите запретить пользователям искать или использовать настраиваемую реализацию окна поиска.</span><span class="sxs-lookup"><span data-stu-id="e989e-125">You can choose to hide the suite navigation bar search box if you want to prevent your users from searching or to use a custom search box implementation.</span></span>

<span data-ttu-id="e989e-126">Чтобы изменить этот параметр для данного сайта, используйте эту команду:</span><span class="sxs-lookup"><span data-stu-id="e989e-126">To change this setting for a given site use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar Hidden
# Hidden | Inherit
```

<span data-ttu-id="e989e-127">Кроме того, если вы хотите установить его для всех сайтов в коллекции сайтов, вы можете использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="e989e-127">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar Hidden
# Hidden | Inherit
```

<span data-ttu-id="e989e-128">После запуска этих команд поле поиска больше не будет показываться в панели навигации в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="e989e-128">After running these commands, the search box will no longer show up in the navigation bar on top of your page.</span></span> <span data-ttu-id="e989e-129">Чтобы вернуться к показу окна поиска, запустите команды снова со значением, предоставляемым параметру "SearchBoxInNavBar" на "Наследуй".</span><span class="sxs-lookup"><span data-stu-id="e989e-129">To go back to showing the search box, run the commands again with the value provided to "SearchBoxInNavBar" parameter to “Inherit”.</span></span>

<span data-ttu-id="e989e-130">Необходимо учитывать несколько моментов:</span><span class="sxs-lookup"><span data-stu-id="e989e-130">There are several points to consider:</span></span>

* <span data-ttu-id="e989e-131">Этот параметр применяется только к поле поиска в панели навигации suite.</span><span class="sxs-lookup"><span data-stu-id="e989e-131">This setting only applies to the search box in the suite navigation bar.</span></span> <span data-ttu-id="e989e-132">Он не применяется к полям поиска, которые находятся на странице, или к полям поиска на классических страницах.</span><span class="sxs-lookup"><span data-stu-id="e989e-132">It does not apply to search boxes that are in the page, or to search boxes on classic pages.</span></span>

* <span data-ttu-id="e989e-133">После отключения окна поиска в панели навигации, если вы хотите использовать функции поиска на сайте, необходимо предоставить его самостоятельно с помощью настраиваемой веб-части или расширения SharePoint Framework.</span><span class="sxs-lookup"><span data-stu-id="e989e-133">Once you’ve disabled the search box in the navigation bar, if you want search functionality in your site, you will have to provide it yourself using a custom web part or a SharePoint Framework extension.</span></span>

* <span data-ttu-id="e989e-134">Это решение также удаляет поле поиска из списков и библиотек для вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="e989e-134">This solution will remove the search box from lists and libraries for your site as well.</span></span> <span data-ttu-id="e989e-135">В пользовательском решении поиска помимо поиска по всему сайту необходимо учитывать контекстные поиски списков и библиотек SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e989e-135">Your custom search solution will need to consider contextual searches for SharePoint lists and libraries, in addition to site-wide search.</span></span>

* <span data-ttu-id="e989e-136">Если применить параметр к корневому сайту домена, на стартовой странице SharePoint также перестанут показывать поле поиска.</span><span class="sxs-lookup"><span data-stu-id="e989e-136">If you apply the setting to the root site of your domain, the SharePoint start page will also stop showing the search box.</span></span>

## <a name="changing-the-hint-displayed-in-the-search-box"></a><span data-ttu-id="e989e-137">Изменение подсказки, отображаемой в поле поиска</span><span class="sxs-lookup"><span data-stu-id="e989e-137">Changing the hint displayed in the search box</span></span>

<span data-ttu-id="e989e-138">Вы можете изменить подсказку, показанную в поле поиска для данного сайта или коллекции сайтов.</span><span class="sxs-lookup"><span data-stu-id="e989e-138">You can change the hint the search box shows for a given site or site collection.</span></span> <span data-ttu-id="e989e-139">Это текст, который отображается в поле поиска перед началом ввода в него.</span><span class="sxs-lookup"><span data-stu-id="e989e-139">This is the text that appears in the search box before they start typing into it.</span></span> <span data-ttu-id="e989e-140">Это может помочь пользователям в поиске, если вы настроили настраиваемую страницу результатов или изменили поведение поиска другими способами.</span><span class="sxs-lookup"><span data-stu-id="e989e-140">This may help guide your users about what to expect from search if you’ve configured a custom results page or changed behavior of search in other ways.</span></span>

> [!NOTE]
> <span data-ttu-id="e989e-141">Чтобы внести это изменение, необходимо разрешить запуск настраиваемой скрипты на сайте в качестве администратора клиента, который по умолчанию не разрешается.</span><span class="sxs-lookup"><span data-stu-id="e989e-141">To be able to make this change, you need to allow running custom scripts on the site in question as a tenant administrator, which is disallowed by default.</span></span> <span data-ttu-id="e989e-142">Подробные https://docs.microsoft.com/sharepoint/allow-or-prevent-custom-script сведения см. в материале.</span><span class="sxs-lookup"><span data-stu-id="e989e-142">Please see https://docs.microsoft.com/sharepoint/allow-or-prevent-custom-script for details.</span></span> <span data-ttu-id="e989e-143">Вы можете разрешить запуск настраиваемой скрипты, внести изменения, а затем вернуться к disallowing скрипты для сайта, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="e989e-143">You can allow running custom scripts, make the change, and then revert to disallowing scripts for the site if necessary.</span></span>

<span data-ttu-id="e989e-144">Чтобы изменить этот параметр для данного сайта, запустите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e989e-144">To change this setting for a given site run the following command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxPlaceholderText "my placeholder" 
```

<span data-ttu-id="e989e-145">Кроме того, если вы хотите установить его для всех сайтов в коллекции сайтов, вы можете использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="e989e-145">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxPlaceholderText "my placeholder" 
```

<span data-ttu-id="e989e-146">Чтобы вернуться к тексту задатки по умолчанию, задайте значение пустое ("").</span><span class="sxs-lookup"><span data-stu-id="e989e-146">To go back to the default placeholder text, set the value to be blank ("").</span></span>