---
title: Классические страницы в SharePoint Online и Microsoft Search
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
description: Использование microsoft Search на классических страницах SharePoint
ms.openlocfilehash: 33215c730d34c14f8ce1d55e93730615688f1e2a
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031434"
---
# <a name="classic-pages-and-microsoft-search"></a><span data-ttu-id="24e82-103">Классические страницы и microsoft Search</span><span class="sxs-lookup"><span data-stu-id="24e82-103">Classic pages and Microsoft Search</span></span>

<span data-ttu-id="24e82-104">Сайты SharePoint, созданные до современных сайтов, используют классическое поле поиска и классические результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="24e82-104">SharePoint sites created prior to modern sites use a classic search box and classic search results experience.</span></span> <span data-ttu-id="24e82-105">Мы будем развертывать функцию, которая будет по умолчанию классические страницы, чтобы начать использовать современный опыт поиска, который использует Microsoft Search, который обеспечивает персонализированные результаты с более высокой релевантности.</span><span class="sxs-lookup"><span data-stu-id="24e82-105">We will be rolling out a feature that will default classic pages to start using the modern search experience that uses Microsoft Search, which provides personalized results with higher relevance.</span></span>

<span data-ttu-id="24e82-106">Использование Microsoft Search рекомендуется для всех сайтов, в том числе классических, но если на классических сайтах используются настраиваемые мастер-страницы и/или вы настраивали классический опыт результатов поиска, мы автоматически обнаруживаем эти настройки и не переключаемся на Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="24e82-106">Using Microsoft Search is recommended for all sites, including classic, but if your classic sites use custom master pages and/or you have customized your classic search results experience, we will auto-detect these customizations and not switch to Microsoft Search.</span></span>

## <a name="classic-sites-that-will-automatically-switch-to-microsoft-search"></a><span data-ttu-id="24e82-107">Классические сайты, которые автоматически переключаются на Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="24e82-107">Classic sites that will automatically switch to Microsoft Search</span></span>

<span data-ttu-id="24e82-108">Классические сайты начнут использовать Microsoft Search, если все эти сайты верны:</span><span class="sxs-lookup"><span data-stu-id="24e82-108">Classic sites will start using Microsoft Search if all of the following are true:</span></span>

* <span data-ttu-id="24e82-109">Сайт основан на шаблоне сайта группы (например, STS#0 и STS#1).</span><span class="sxs-lookup"><span data-stu-id="24e82-109">The site is based on the team site template (like STS#0 and STS#1).</span></span>
* <span data-ttu-id="24e82-110">На сайте не включена функция публикации.</span><span class="sxs-lookup"><span data-stu-id="24e82-110">The site does not have the publishing feature turned on.</span></span>
* <span data-ttu-id="24e82-111">На сайте не используется настраиваемая мастер-страница (другая мастер-страница, чем oslo.master или seattle.master).</span><span class="sxs-lookup"><span data-stu-id="24e82-111">The site does not use a custom master page (a different master page than oslo.master or seattle.master).</span></span>
* <span data-ttu-id="24e82-112">Нет никаких правил активного запроса, кроме правил добавления продвигаемого результата для сайта, коллекции сайтов или клиента в источнике результатов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24e82-112">There are no active query rules other than those adding promoted results for the site, site collection or tenant on the default result source.</span></span>
* <span data-ttu-id="24e82-113">В источнике результатов по умолчанию не существует пользовательских типов результатов для сайта или коллекции сайтов.</span><span class="sxs-lookup"><span data-stu-id="24e82-113">There are no custom result types for the site or the site collection on the default result source.</span></span>
* <span data-ttu-id="24e82-114">Сайт или коллекция сайтов не отключались от коммутатора с помощью *параметра SearchBoxInNavBar,* описанного ниже.</span><span class="sxs-lookup"><span data-stu-id="24e82-114">The site or the site collection is not opted out of the switch using the *SearchBoxInNavBar* setting described below.</span></span>

<span data-ttu-id="24e82-115">После перехода на Microsoft Search классические страницы на сайте начнут показывать поле поиска в панели навигации пакета и удалять классическое поле поиска со страницы.</span><span class="sxs-lookup"><span data-stu-id="24e82-115">After the switch to Microsoft Search, classic pages in the site will start to show the search box in the suite navigation bar and remove the classic search box from the page.</span></span> <span data-ttu-id="24e82-116">Затем, когда пользователь ищет термин, результаты будут отображаться с помощью современного интерфейса поиска Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="24e82-116">Then, when a user searches for a term, the results will be displayed using the modern search experience of Microsoft Search.</span></span>

## <a name="staying-with-the-classic-search-experience"></a><span data-ttu-id="24e82-117">Пребывание с классическим опытом поиска</span><span class="sxs-lookup"><span data-stu-id="24e82-117">Staying with the classic search experience</span></span>

<span data-ttu-id="24e82-118">Если ваш сайт соответствует перечисленным выше критериям, но вы не хотите, чтобы он переключился на службу поиска Майкрософт, вы можете отказаться от использования следующих команд, как владелец сайта или коллекции сайтов.</span><span class="sxs-lookup"><span data-stu-id="24e82-118">If your site meets the criteria listed above, but you do not want it to switch to the Microsoft Search experience, you can opt out using the following commands, as the site or site collection owner.</span></span>

<span data-ttu-id="24e82-119">Вы можете использовать эту команду в любое время, до или после того, как произойдет переключатель, поэтому легко вернуться к опыту поиска, который был ранее.</span><span class="sxs-lookup"><span data-stu-id="24e82-119">You can use this command at any time, before or after the switch happens, so it is easy to go back to the search experience you had previously.</span></span>

<span data-ttu-id="24e82-120">Для запуска команд ниже вы будете использовать PowerShell с расширениями SharePoint PnP PowerShell.</span><span class="sxs-lookup"><span data-stu-id="24e82-120">To run the commands below, you will use PowerShell with SharePoint PnP PowerShell extensions.</span></span> <span data-ttu-id="24e82-121">Вы можете установить и узнать больше о том, как начать [работу здесь](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="24e82-121">You can install and learn more about how to get started [here](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span></span> <span data-ttu-id="24e82-122">Вы вопишитесь на свой сайт или коллекцию сайтов с помощью этой команды:</span><span class="sxs-lookup"><span data-stu-id="24e82-122">You will sign in to your site or site collection using this command:</span></span>

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign in to your site. Use the site owner credentials.
```

<span data-ttu-id="24e82-123">Чтобы остаться с классическим опытом поиска для сайта, запустите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="24e82-123">To stay with classic search experience for a site, run the following command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

<span data-ttu-id="24e82-124">Кроме того, если вы хотите установить его для всех сайтов в коллекции сайтов, вы можете использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="24e82-124">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

## <a name="opting-into-microsoft-search"></a><span data-ttu-id="24e82-125">Выбор в Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="24e82-125">Opting into Microsoft Search</span></span>

<span data-ttu-id="24e82-126">Для тех сайтов, которые не соответствуют перечисленным выше критериям, или для определенных сайтов в коллекции сайтов, которые решили остаться в классическом режиме, вы можете вручную включить функцию Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="24e82-126">For those sites that do not meet the criteria listed above, or for specific sites in a site collection that opted to stay in classic, you can manually enable the Microsoft Search experience.</span></span>

<span data-ttu-id="24e82-127">Чтобы изменить этот параметр для определенного сайта, можно использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="24e82-127">To change this setting for a specific site, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

<span data-ttu-id="24e82-128">Если вы хотите установить его для всех сайтов в коллекции сайтов, вы можете использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="24e82-128">If you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

> [!NOTE]
> <span data-ttu-id="24e82-129">Можно вручную включить Microsoft Search только для сайта группы или сайта публикации (коды шаблонов, содержащие "STS", "CMSPUBLISHING", "BLANKINTERNET" и "GROUP").</span><span class="sxs-lookup"><span data-stu-id="24e82-129">You can manually enable Microsoft Search only for a Team Site or Publishing Site (template ids that contain "STS", "CMSPUBLISHING", "BLANKINTERNET" and "GROUP").</span></span>