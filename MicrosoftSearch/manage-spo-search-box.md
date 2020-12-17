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
ms.openlocfilehash: 6ebd084aadb38acb5475b7e43d7c4092ffc09eb8
ms.sourcegitcommit: c5fe4e01403379b3ee7ea4dbded8b31696311d79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "49700967"
---
# <a name="search-box-settings-on-sharepoint-sites"></a><span data-ttu-id="40f13-103">Параметры полей поиска на сайтах SharePoint</span><span class="sxs-lookup"><span data-stu-id="40f13-103">Search box settings on SharePoint sites</span></span>

<span data-ttu-id="40f13-104">Один из нескольких способов настройки Поиска (Майкрософт) на сайтах SharePoint — настройка работы полей поиска на панели навигации набора на сайтах SharePoint в наилучшим образом.</span><span class="sxs-lookup"><span data-stu-id="40f13-104">One of the several ways Microsoft Search can be customized on SharePoint sites is to tailor how the search box in the suite navigation bar works in SharePoint sites to best fit your needs.</span></span>

<span data-ttu-id="40f13-105">Другие параметры настройки см. в подстройке "Изменение страницы результатов поиска [(Майкрософт)",](customize-search-page.md)чтобы добавить настраиваемые вертикали, типы результатов и макеты, а также в подстройке "Создание настраиваемой страницы [результатов поиска".](create-search-results-pages.md)</span><span class="sxs-lookup"><span data-stu-id="40f13-105">For other customization options, see [Changing the Microsoft Search results page to add custom verticals, result types and layouts](customize-search-page.md), and [Creating a custom search results page](create-search-results-pages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="40f13-106">Поле поиска панели навигации набора в настоящее время не доступно для всех пользователей, но эти параметры можно установить сейчас, и они вступает в силу, когда он станет доступным.</span><span class="sxs-lookup"><span data-stu-id="40f13-106">The suite navigation bar search box is not available for all customers at this time, but these options can still be set now and they will take effect when it becomes available.</span></span>

<span data-ttu-id="40f13-107">Для задач, перечисленных ниже, вы будете использовать PowerShell с расширениями SharePoint PnP PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40f13-107">For the tasks listed below, you will use PowerShell with SharePoint PnP PowerShell extensions.</span></span> <span data-ttu-id="40f13-108">Вы можете установить и узнать больше о том, как начать [работу здесь.](https://docs.microsoft.com/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps)</span><span class="sxs-lookup"><span data-stu-id="40f13-108">You can install and learn more about how to get started [here](https://docs.microsoft.com/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span></span> <span data-ttu-id="40f13-109">Чтобы войти на сайт или в его коллекцию, с помощью этой команды:</span><span class="sxs-lookup"><span data-stu-id="40f13-109">You will sign into your site or site collection using this command:</span></span>

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign into your site. Use the site owner credentials 
```

## <a name="changing-the-scope-of-search"></a><span data-ttu-id="40f13-110">Изменение области поиска</span><span class="sxs-lookup"><span data-stu-id="40f13-110">Changing the scope of search</span></span>

<span data-ttu-id="40f13-111">При создании нового сайта в SharePoint Online сегодня и введите в поле поиска, вы будете переназначаем на страницу результатов Поиска (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="40f13-111">When you create a new site in SharePoint Online today, and type into the search box, you are taken to the Microsoft Search results page.</span></span> <span data-ttu-id="40f13-112">На этой странице по умолчанию показаны результаты с текущего сайта, и вы можете расширить область поиска до концентратора, с чем связан текущий сайт (если он существует) или всей организации.</span><span class="sxs-lookup"><span data-stu-id="40f13-112">This page shows results from your current site by default and allows you to expand the scope of your search to the hub that the current site is associated with (if there is one), or to the whole organization.</span></span>

<span data-ttu-id="40f13-113">Область, которая используется полем поиска по умолчанию, зависит от типа сайта.</span><span class="sxs-lookup"><span data-stu-id="40f13-113">The scope the search box uses, by default, depends on type of site.</span></span>

* <span data-ttu-id="40f13-114">Регулярный поиск сайтов по текущему сайту.</span><span class="sxs-lookup"><span data-stu-id="40f13-114">Regular sites search over the current site.</span></span>
* <span data-ttu-id="40f13-115">Поиск на центральном сайте по всем сайтам в концентраторах.</span><span class="sxs-lookup"><span data-stu-id="40f13-115">Hub sites search over all sites in the hub.</span></span>
* <span data-ttu-id="40f13-116">Домашние сайты ведут поиск по всему контенту.</span><span class="sxs-lookup"><span data-stu-id="40f13-116">Home sites search over all content.</span></span>

<span data-ttu-id="40f13-117">В некоторых случаях может потребоваться изменить эти значения по умолчанию, чтобы всегда искать по всей организации или по всему центральному сайту, связанному с сайтом, без необходимости дополнительного щелчка.</span><span class="sxs-lookup"><span data-stu-id="40f13-117">In some cases, you may want to change these defaults to always search over the whole organization, or across the hub a site is associated with, without needing an additional click.</span></span>

<span data-ttu-id="40f13-118">Как владелец сайта вы можете изменить эти значения по умолчанию с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="40f13-118">As a site owner, you can change these defaults using the following command:</span></span>

```powershell
Set-PnPSearchSettings -SearchScope Tenant
# DefaultScope | Hub | Site | Tenant
```

<span data-ttu-id="40f13-119">После запуска этой команды на сайте, на котором ранее по умолчанию отображаются результаты с текущего сайта, будут показаны результаты из всей организации.</span><span class="sxs-lookup"><span data-stu-id="40f13-119">After running this command, the site that was previously showing results from the current site by default will start to show results from the whole organization.</span></span>

<span data-ttu-id="40f13-120">Чтобы вернуться к параметру по умолчанию, снова запустите команду со значением DefaultScope.</span><span class="sxs-lookup"><span data-stu-id="40f13-120">To go back to the default setting, run the command again with the value “DefaultScope".</span></span> <span data-ttu-id="40f13-121">Для поиска в центре используйте значение SearchScope с помощью "Hub".</span><span class="sxs-lookup"><span data-stu-id="40f13-121">To search across the Hub, use “Hub” as the SearchScope value.</span></span>

<span data-ttu-id="40f13-122">Этот параметр применяется на уровне отдельного сайта.</span><span class="sxs-lookup"><span data-stu-id="40f13-122">This setting applies at the individual site level.</span></span> <span data-ttu-id="40f13-123">Эквивалентные параметры для коллекций веб-сайтов не существуют.</span><span class="sxs-lookup"><span data-stu-id="40f13-123">There is no equivalent setting for site collections.</span></span>

## <a name="show-or-hide-the-search-box"></a><span data-ttu-id="40f13-124">Показать или скрыть поле поиска</span><span class="sxs-lookup"><span data-stu-id="40f13-124">Show or hide the search box</span></span>

<span data-ttu-id="40f13-125">Вы можете скрыть поле поиска панели навигации набора, если хотите запретить пользователям искать или использовать настраиваемую реализацию полей поиска.</span><span class="sxs-lookup"><span data-stu-id="40f13-125">You can choose to hide the suite navigation bar search box if you want to prevent your users from searching or to use a custom search box implementation.</span></span>

<span data-ttu-id="40f13-126">Чтобы изменить этот параметр для заданного сайта, используйте команду:</span><span class="sxs-lookup"><span data-stu-id="40f13-126">To change this setting for a given site use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar Hidden
# Hidden | Inherit
```

<span data-ttu-id="40f13-127">Кроме того, если вы хотите установить его для всех сайтов в коллекции сайтов, можно использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="40f13-127">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar Hidden
# Hidden | Inherit
```

<span data-ttu-id="40f13-128">После запуска этих команд поле поиска больше не будет показываться на панели навигации в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="40f13-128">After running these commands, the search box will no longer show up in the navigation bar on top of your page.</span></span> <span data-ttu-id="40f13-129">Чтобы вернуться к от показанию окна поиска, снова запустите команды со значением "SearchBoxInNavBar" в "Inherit".</span><span class="sxs-lookup"><span data-stu-id="40f13-129">To go back to showing the search box, run the commands again with the value provided to "SearchBoxInNavBar" parameter to “Inherit”.</span></span>

<span data-ttu-id="40f13-130">Следует учесть несколько моментов.</span><span class="sxs-lookup"><span data-stu-id="40f13-130">There are several points to consider:</span></span>

* <span data-ttu-id="40f13-131">Этот параметр применяется только к поле поиска на панели навигации набора.</span><span class="sxs-lookup"><span data-stu-id="40f13-131">This setting only applies to the search box in the suite navigation bar.</span></span> <span data-ttu-id="40f13-132">Он не применяется к полям поиска, которые находятся на странице, или к полям поиска на классических страницах.</span><span class="sxs-lookup"><span data-stu-id="40f13-132">It does not apply to search boxes that are in the page, or to search boxes on classic pages.</span></span>

* <span data-ttu-id="40f13-133">Если вы отключите поле поиска на панели навигации, если вам нужны функции поиска на сайте, вам придется предоставить его самостоятельно с помощью настраиваемой веб-части или расширения SharePoint Framework.</span><span class="sxs-lookup"><span data-stu-id="40f13-133">Once you’ve disabled the search box in the navigation bar, if you want search functionality in your site, you will have to provide it yourself using a custom web part or a SharePoint Framework extension.</span></span>

* <span data-ttu-id="40f13-134">Это решение также удалит поле поиска из списков и библиотек сайта.</span><span class="sxs-lookup"><span data-stu-id="40f13-134">This solution will remove the search box from lists and libraries for your site as well.</span></span> <span data-ttu-id="40f13-135">В пользовательском решении поиска помимо поиска на уровне сайта необходимо учитывать контекстный поиск для списков и библиотек SharePoint.</span><span class="sxs-lookup"><span data-stu-id="40f13-135">Your custom search solution will need to consider contextual searches for SharePoint lists and libraries, in addition to site-wide search.</span></span>

* <span data-ttu-id="40f13-136">Если применить этот параметр к корневому сайту домена, начальная страница SharePoint также перестанет показывать поле поиска.</span><span class="sxs-lookup"><span data-stu-id="40f13-136">If you apply the setting to the root site of your domain, the SharePoint start page will also stop showing the search box.</span></span>

## <a name="changing-the-hint-displayed-in-the-search-box"></a><span data-ttu-id="40f13-137">Изменение подсказки, отображаемой в поле поиска</span><span class="sxs-lookup"><span data-stu-id="40f13-137">Changing the hint displayed in the search box</span></span>

<span data-ttu-id="40f13-138">Вы можете изменить подсказку, отображаемую в поле поиска для заданного сайта или веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="40f13-138">You can change the hint the search box shows for a given site or site collection.</span></span> <span data-ttu-id="40f13-139">Это текст, который отображается в поле поиска, прежде чем они начнут вводить в него текст.</span><span class="sxs-lookup"><span data-stu-id="40f13-139">This is the text that appears in the search box before they start typing into it.</span></span> <span data-ttu-id="40f13-140">Это может помочь пользователям получить информацию о том, чего ожидать от поиска, если вы настроили пользовательскую страницу результатов или изменили поведение поиска другими способами.</span><span class="sxs-lookup"><span data-stu-id="40f13-140">This may help guide your users about what to expect from search if you’ve configured a custom results page or changed behavior of search in other ways.</span></span>

> [!NOTE]
> <span data-ttu-id="40f13-141">Чтобы внести это изменение, необходимо разрешить запуск пользовательских сценариев на сайте, о котором идет речь, как администратор клиента, что по умолчанию не допускается.</span><span class="sxs-lookup"><span data-stu-id="40f13-141">To be able to make this change, you need to allow running custom scripts on the site in question as a tenant administrator, which is disallowed by default.</span></span> <span data-ttu-id="40f13-142">Подробные https://docs.microsoft.com/sharepoint/allow-or-prevent-custom-script сведения см. в этой теме.</span><span class="sxs-lookup"><span data-stu-id="40f13-142">Please see https://docs.microsoft.com/sharepoint/allow-or-prevent-custom-script for details.</span></span> <span data-ttu-id="40f13-143">Вы можете разрешить запуск пользовательских сценариев, внести изменения, а затем при необходимости отменить их для сайта.</span><span class="sxs-lookup"><span data-stu-id="40f13-143">You can allow running custom scripts, make the change, and then revert to disallowing scripts for the site if necessary.</span></span>

<span data-ttu-id="40f13-144">Чтобы изменить этот параметр для данного сайта, запустите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="40f13-144">To change this setting for a given site run the following command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxPlaceholderText "my placeholder" 
```

<span data-ttu-id="40f13-145">Кроме того, если вы хотите установить его для всех сайтов в коллекции сайтов, можно использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="40f13-145">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxPlaceholderText "my placeholder" 
```

<span data-ttu-id="40f13-146">Чтобы вернуться к тексту-замещику по умолчанию, задайте пустое значение ("").</span><span class="sxs-lookup"><span data-stu-id="40f13-146">To go back to the default placeholder text, set the value to be blank ("").</span></span>
