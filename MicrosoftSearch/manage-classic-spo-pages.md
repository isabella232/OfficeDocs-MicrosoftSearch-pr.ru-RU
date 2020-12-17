---
title: Классические страницы в SharePoint Online и Поиске (Майкрософт)
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
description: Использование Поиска (Майкрософт) на классических страницах SharePoint
ms.openlocfilehash: 605e63a30ad166c63320c7e89e1b2745e628e15d
ms.sourcegitcommit: c5fe4e01403379b3ee7ea4dbded8b31696311d79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "49700976"
---
# <a name="classic-pages-and-microsoft-search"></a><span data-ttu-id="8de5c-103">Классические страницы и Поиск (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8de5c-103">Classic pages and Microsoft Search</span></span>

<span data-ttu-id="8de5c-104">Сайты SharePoint, созданные до современных сайтов, используют классическое поле поиска и классический опыт результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="8de5c-104">SharePoint sites created prior to modern sites use a classic search box and classic search results experience.</span></span> <span data-ttu-id="8de5c-105">Мы развявем функцию, которая будет использовать классические страницы по умолчанию, чтобы начать использовать современный поиск, использующий Поиск (Майкрософт), который обеспечивает персонализированные результаты с более высокой релевантностью.</span><span class="sxs-lookup"><span data-stu-id="8de5c-105">We will be rolling out a feature that will default classic pages to start using the modern search experience that uses Microsoft Search, which provides personalized results with higher relevance.</span></span>

<span data-ttu-id="8de5c-106">Поиск (Майкрософт) рекомендуется использовать для всех сайтов, в том числе классических, но если на классических сайтах используются настраиваемые этаководные страницы и/или вы настроили классический режим результатов поиска, мы автоматически обнавим эти настройки и не переключимся на Поиск (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="8de5c-106">Using Microsoft Search is recommended for all sites, including classic, but if your classic sites use custom master pages and/or you have customized your classic search results experience, we will auto-detect these customizations and not switch to Microsoft Search.</span></span>

## <a name="classic-sites-that-will-automatically-switch-to-microsoft-search"></a><span data-ttu-id="8de5c-107">Классические сайты, которые автоматически переключаются на Поиск (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8de5c-107">Classic sites that will automatically switch to Microsoft Search</span></span>

<span data-ttu-id="8de5c-108">Классические сайты начнут использовать Поиск (Майкрософт), если все следующие узлы являются истинными.</span><span class="sxs-lookup"><span data-stu-id="8de5c-108">Classic sites will start using Microsoft Search if all of the following are true.</span></span>

* <span data-ttu-id="8de5c-109">Сайт основан на шаблоне сайта группы (например, STS#0 и STS#1).</span><span class="sxs-lookup"><span data-stu-id="8de5c-109">The site is based on the team site template (like STS#0 and STS#1).</span></span>
* <span data-ttu-id="8de5c-110">На сайте не включена функция публикации.</span><span class="sxs-lookup"><span data-stu-id="8de5c-110">The site does not have the publishing feature turned on.</span></span>
* <span data-ttu-id="8de5c-111">На сайте не используется настраиваемая этакое страница (этакое, чем oslo.master или seattle.master).</span><span class="sxs-lookup"><span data-stu-id="8de5c-111">The site does not use a custom master page (a different master page than oslo.master or seattle.master).</span></span>
* <span data-ttu-id="8de5c-112">В источнике результатов по умолчанию нет активных правил запроса, кроме правил добавления продвигаемого результата для сайта, веб-сайта или клиента.</span><span class="sxs-lookup"><span data-stu-id="8de5c-112">There are no active query rules other than those adding promoted results for the site, site collection or tenant on the default result source.</span></span>
* <span data-ttu-id="8de5c-113">В источнике результатов по умолчанию нет пользовательских типов результатов для сайта или коллекции веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="8de5c-113">There are no custom result types for the site or the site collection on the default result source.</span></span>
* <span data-ttu-id="8de5c-114">Сайт или веб-сайт, в который он входит, не отказался от переключения с помощью параметра SearchBoxInNavBar, описанного ниже.</span><span class="sxs-lookup"><span data-stu-id="8de5c-114">The site or the site collection it is part of has not opted out of the switch using the SearchBoxInNavBar setting described below.</span></span>

<span data-ttu-id="8de5c-115">После перехода на Поиск (Майкрософт) классические страницы на сайте начнут показывать поле поиска на панели навигации набора и удалять классическое поле поиска со страницы.</span><span class="sxs-lookup"><span data-stu-id="8de5c-115">After the switch to Microsoft Search, classic pages in the site will start to show the search box in the suite navigation bar and remove the classic search box from the page.</span></span> <span data-ttu-id="8de5c-116">Затем, когда пользователь ищет термин, результаты будут отображаться с использованием современного интерфейса поиска Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="8de5c-116">Then, when a user searches for a term, the results will be displayed using the modern search experience of Microsoft Search.</span></span>

## <a name="staying-with-the-classic-search-experience"></a><span data-ttu-id="8de5c-117">Оставаясь в классическом поиске</span><span class="sxs-lookup"><span data-stu-id="8de5c-117">Staying with the classic search experience</span></span>

<span data-ttu-id="8de5c-118">Если сайт соответствует перечисленным выше критериям, но вы не хотите, чтобы он переключился на поиск (Майкрософт), вы можете отказаться от использования следующих команд в качестве владельца сайта или веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="8de5c-118">If your site meets the criteria listed above, but you do not want it to switch to the Microsoft Search experience, you can opt out using the following commands, as the site or site collection owner.</span></span>

<span data-ttu-id="8de5c-119">Эту команду можно использовать в любое время, до или после переключения, чтобы можно было легко вернуться к ранее имевшийся опыт поиска.</span><span class="sxs-lookup"><span data-stu-id="8de5c-119">You can use this command at any time, before or after the switch happens, so it is easy to go back to the search experience you had previously.</span></span>

<span data-ttu-id="8de5c-120">Чтобы выполнить команды ниже, используйте PowerShell с расширениями SharePoint PnP PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8de5c-120">To run the commands below, you will use PowerShell with SharePoint PnP PowerShell extensions.</span></span> <span data-ttu-id="8de5c-121">Вы можете установить и узнать больше о том, как начать [работу здесь.](https://docs.microsoft.com/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps)</span><span class="sxs-lookup"><span data-stu-id="8de5c-121">You can install and learn more about how to get started [here](https://docs.microsoft.com/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span></span> <span data-ttu-id="8de5c-122">Чтобы войти на сайт или в его коллекцию, с помощью этой команды:</span><span class="sxs-lookup"><span data-stu-id="8de5c-122">You will sign into your site or site collection using this command:</span></span>

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign into your site. Use the site owner credentials
```

<span data-ttu-id="8de5c-123">Чтобы остаться с классическим опытом поиска для сайта, запустите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8de5c-123">To stay with classic search experience for a site, run the following command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

<span data-ttu-id="8de5c-124">Кроме того, если вы хотите установить его для всех сайтов в коллекции сайтов, можно использовать эту команду:</span><span class="sxs-lookup"><span data-stu-id="8de5c-124">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

## <a name="opting-into-microsoft-search"></a><span data-ttu-id="8de5c-125">Отказ от поиска (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8de5c-125">Opting into Microsoft Search</span></span>

<span data-ttu-id="8de5c-126">Для тех сайтов, которые не соответствуют перечисленным выше критериям, или для определенных сайтов в коллекции сайтов, которые решили использовать классический режим, можно вручную включить поиск (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="8de5c-126">For those sites that do not meet the criteria listed above, or for specific sites in a site collection that opted to stay in classic, you can manually enable the Microsoft Search experience.</span></span>

<span data-ttu-id="8de5c-127">Чтобы изменить этот параметр для определенного сайта, можно использовать команду:</span><span class="sxs-lookup"><span data-stu-id="8de5c-127">To change this setting for a specific site, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

<span data-ttu-id="8de5c-128">Если вы хотите установить его для всех сайтов в коллекции сайтов, можно использовать команду:</span><span class="sxs-lookup"><span data-stu-id="8de5c-128">If you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

> [!NOTE]
> <span data-ttu-id="8de5c-129">Поиск (Майкрософт) можно включить вручную только для сайта группы или сайта публикации (коды шаблонов, содержащие "STS", "CMSPUBLISHING", "BLANKINTERNET" и "GROUP").</span><span class="sxs-lookup"><span data-stu-id="8de5c-129">You can manually enable Microsoft Search only for a Team Site or Publishing Site (template ids that contain "STS", "CMSPUBLISHING", "BLANKINTERNET" and "GROUP").</span></span>
