---
title: Создание настраиваемой страницы результатов поиска в SharePoint Online
ms.author: jeffkizn
author: jeffkizn
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
description: Создайте собственную страницу результатов поиска для сайта SharePoint Online
ms.openlocfilehash: b5abb25f15795389dd8b6d5683ac336af7422e0a
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031641"
---
# <a name="create-a-custom-search-results-page-in-sharepoint-online"></a><span data-ttu-id="223b4-103">Создание настраиваемой страницы результатов поиска в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="223b4-103">Create a custom search results page in SharePoint Online</span></span>

<span data-ttu-id="223b4-104">Один из способов настройки опытом поиска в SharePoint — создать настраиваемую страницу результатов поиска для сайта.</span><span class="sxs-lookup"><span data-stu-id="223b4-104">One way to customize the search experience in SharePoint is to create a custom search results page for a site.</span></span> <span data-ttu-id="223b4-105">Это позволяет использовать созданную страницу, а не по умолчанию на странице результатов поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="223b4-105">This allows you to use a page that you created, rather than the default in Microsoft Search results page.</span></span> <span data-ttu-id="223b4-106">Это обеспечивает больше гибкости при поиске результатов поиска для пользователей.</span><span class="sxs-lookup"><span data-stu-id="223b4-106">This gives you more flexibility on how the search results experience looks for your users.</span></span>

>[!NOTE]
> <span data-ttu-id="223b4-107">Чтобы внести изменения на страницу результатов поиска Майкрософт по умолчанию, доступную по умолчанию, см. в странице [Настройка страницы результатов поиска.](customize-search-page.md)</span><span class="sxs-lookup"><span data-stu-id="223b4-107">To make changes to the default Microsoft Search results page that is available by default, please see [Customize the search results page](customize-search-page.md).</span></span>

<span data-ttu-id="223b4-108">На настраиваемой странице результатов можно создать новую страницу, которая может использоваться для управления макетом и оформлением результатов поиска для поддержки потребностей организации.</span><span class="sxs-lookup"><span data-stu-id="223b4-108">With a custom results page you can create a new page that can be used to control the layout and design of search results to support your organization's needs.</span></span> <span data-ttu-id="223b4-109">Вы можете использовать все встроенные веб-части, веб-части поиска с открытым исходным кодом из сообщества Шаблоны и практики SharePoint, а также любые настраиваемые веб-части, которые вы, возможно, разработали с помощью SharePoint Framework.</span><span class="sxs-lookup"><span data-stu-id="223b4-109">You can use any built-in web parts, open-source search web parts from SharePoint Patterns and Practices community, as well as any custom web parts that you may have developed using SharePoint Framework.</span></span>

## <a name="configure-a-results-page"></a><span data-ttu-id="223b4-110">Настройка страницы результатов</span><span class="sxs-lookup"><span data-stu-id="223b4-110">Configure a results page</span></span>

<span data-ttu-id="223b4-111">Чтобы настроить настраиваемую страницу результатов в SharePoint Online, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="223b4-111">To configure a custom results page in SharePoint Online follow the steps below:</span></span>

1. <span data-ttu-id="223b4-112">Просмотрите сайт, на котором вы хотите настроить настраиваемую страницу результатов, и перейдите к параметрам параметров сайта > параметров > **параметров поиска.**</span><span class="sxs-lookup"><span data-stu-id="223b4-112">Browse to the site where you would like to configure a custom results page and go to **Site Settings > Site Collection Settings > Search Settings**.</span></span>

2. <span data-ttu-id="223b4-113">В параметрах поиска выберите четкий выбор из параметров страницы "Использование тех же результатов, что и мои родители", выберите отправку запросов на настраиваемую страницу результатов **и** укайте значение URL-адреса страницы **"Результаты":**.</span><span class="sxs-lookup"><span data-stu-id="223b4-113">In Search Settings, clear selection from **Use the same results page settings as my parent**, choose **Send queries to a custom results page**, and provide a value for **Results page URL:**.</span></span> <span data-ttu-id="223b4-114">Затем сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="223b4-114">Then, save your changes.</span></span> <span data-ttu-id="223b4-115">URL-адрес, который вы здесь используете, должен быть для страницы, созданной для использования в качестве настраиваемой страницы результатов.</span><span class="sxs-lookup"><span data-stu-id="223b4-115">The URL you use here should be for the page that you created to use as your custom results page.</span></span>

>[!NOTE]
> <span data-ttu-id="223b4-116">Страница пользовательских результатов должна быть на том же домене, что и ваш сайт, но не должна быть в одной и той же коллекции сайтов.</span><span class="sxs-lookup"><span data-stu-id="223b4-116">The custom results page needs to be on the same domain as your site, but it does not have to be in the same site collection.</span></span>  

<span data-ttu-id="223b4-117">Кроме того, можно использовать команду [Set-PnPSearchSettings SharePoint PnP PowerShell,](/powershell/module/sharepoint-pnp/set-pnpsearchsettings?view=sharepoint-ps) чтобы задать значение, а не использовать страницу Параметры сайта.</span><span class="sxs-lookup"><span data-stu-id="223b4-117">Alternatively, you can use the [Set-PnPSearchSettings SharePoint PnP PowerShell command](/powershell/module/sharepoint-pnp/set-pnpsearchsettings?view=sharepoint-ps) to set the value instead of using the Site Settings page.</span></span>

<span data-ttu-id="223b4-118">После набора настраиваемая страница результатов поиска отображается при поиске с помощью окна Поиска Майкрософт, которое отображается в панели навигации на верхней части страницы и используется при вводе поиска со страниц сайта или домашней страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="223b4-118">Once set, the custom search results page is displayed when you search using the Microsoft Search box that appears in the navigation bar on top of the page and is used when you enter search from site pages or the home page of the site.</span></span> <span data-ttu-id="223b4-119">Он не используется при поиске в списке, библиотеке или на странице содержимого сайта.</span><span class="sxs-lookup"><span data-stu-id="223b4-119">It is not used when you are searching within a list, library, or the site contents page.</span></span> <span data-ttu-id="223b4-120">Вы можете использовать ссылку, чтобы расширить поиск из результатов поиска в списках и библиотеках, чтобы попасть на настраиваемую страницу результатов.</span><span class="sxs-lookup"><span data-stu-id="223b4-120">You may use the link to expand your search from search results in lists and libraries to get to the custom results page.</span></span>

## <a name="change-the-layout-of-your-custom-results-page"></a><span data-ttu-id="223b4-121">Изменение макета страницы пользовательских результатов</span><span class="sxs-lookup"><span data-stu-id="223b4-121">Change the layout of your custom results page</span></span>

<span data-ttu-id="223b4-122">Макет страницы с именем **HeaderlessSearchResults** можно использовать, чтобы сделать страницу результатов поиска ближе к нашему опыту результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="223b4-122">A page layout named **HeaderlessSearchResults** can be used to make the search results page appear closer to our out of box search results experience.</span></span> <span data-ttu-id="223b4-123">Эта новая схема может быть активна только для страниц, заданной для пользовательской страницы результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="223b4-123">This new layout can only be active for the pages that are set to be the custom search results page.</span></span>

<span data-ttu-id="223b4-124">Чтобы установить макет страницы, можно использовать команду [Set-PnPClientSidePSharePoint PnP PowerShell](/powershell/module/sharepoint-pnp/set-pnpclientsidepage?view=sharepoint-ps) с командой -LayoutType HeaderlessSearchResults.</span><span class="sxs-lookup"><span data-stu-id="223b4-124">To set the page layout, you can use the [Set-PnPClientSidePageSharePoint PnP PowerShell command](/powershell/module/sharepoint-pnp/set-pnpclientsidepage?view=sharepoint-ps) with -LayoutType HeaderlessSearchResults.</span></span>

## <a name="use-sharepoint-framework-query-extensions"></a><span data-ttu-id="223b4-125">Использование расширений запроса SharePoint Framework</span><span class="sxs-lookup"><span data-stu-id="223b4-125">Use SharePoint Framework Query extensions</span></span>

<span data-ttu-id="223b4-126">Пользовательские страницы результатов поиска также могут использовать расширение [запроса SharePoint Framework для](/sharepoint/dev/spfx/building-search-extensions) изменения запроса перед его отправлением в поисковую систему.</span><span class="sxs-lookup"><span data-stu-id="223b4-126">Custom search results pages can also make use of the [SharePoint Framework Query Extension](/sharepoint/dev/spfx/building-search-extensions) to modify the query before it gets sent to the search engine.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="223b4-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="223b4-127">Additional resources</span></span>

<span data-ttu-id="223b4-128">Чтобы узнать больше о настраиваемой странице результатов, ознакомьтесь с нашим сеансом настройки и разработки [Ignite 2019.](https://myignite.techcommunity.microsoft.com/sessions/85238?source=sessions)</span><span class="sxs-lookup"><span data-stu-id="223b4-128">To learn more about custom results page, check out our [Ignite 2019 Search Customization and Development session](https://myignite.techcommunity.microsoft.com/sessions/85238?source=sessions).</span></span>

<span data-ttu-id="223b4-129">Для проектов с открытым исходным кодом при работе с нашими API Поиска Майкрософт и дополнительными примерами настройки и расшифритизации посетите [веб-сайт Microsoft Search на GitHub.](https://github.com/microsoft-search)</span><span class="sxs-lookup"><span data-stu-id="223b4-129">For open source projects, getting started with our Microsoft Search APIs, and more customization and extensibility samples, visit [Microsoft Search on GitHub](https://github.com/microsoft-search).</span></span>