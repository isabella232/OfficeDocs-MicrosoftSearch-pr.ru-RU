---
title: Enterprise веб-Graph соединители для Поиск (Майкрософт)
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка Enterprise веб Graph соединители для Поиск (Майкрософт)
ms.openlocfilehash: f986736218768b4979e6e8aa474081c6aa87cb75
ms.sourcegitcommit: 56e6c0706067e383d826ec97feb80f0742a726e0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/14/2021
ms.locfileid: "53419898"
---
<!---Previous ms.author: monaray --->

<!-- markdownlint-disable no-inline-html -->

# <a name="enterprise-websites-graph-connector"></a><span data-ttu-id="6e2c3-103">Enterprise веб Graph соединители</span><span class="sxs-lookup"><span data-stu-id="6e2c3-103">Enterprise websites Graph connector</span></span>

<span data-ttu-id="6e2c3-104">Соедините Enterprise веб-Graph позволяет организации индексировать статьи и контент с внутренних **веб-сайтов.**</span><span class="sxs-lookup"><span data-stu-id="6e2c3-104">The Enterprise websites Graph connector allows your organization to index articles and **content from its internal-facing websites**.</span></span> <span data-ttu-id="6e2c3-105">После настройки соединители и синхронизации контента с веб-сайта конечные пользователи могут искать этот контент из любого Поиск (Майкрософт) клиента.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-105">After you configure the connector and sync content from the website, end users can search for that content from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="6e2c3-106">Ознакомьтесь [**с статьей Настройка Graph соединители,**](configure-connector.md) чтобы понять общие инструкции Graph соединители.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-106">Read the [**Setup your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="6e2c3-107">Эта статья для всех, кто настраивает, запускает и отслеживает соединители Enterprise веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-107">This article is for anyone who configures, runs, and monitors an Enterprise websites connector.</span></span> <span data-ttu-id="6e2c3-108">Он дополняет общий процесс установки и показывает инструкции, которые применяются только для соединитетеля Enterprise веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-108">It supplements the general setup process, and shows instructions that apply only for the Enterprise websites connector.</span></span> <span data-ttu-id="6e2c3-109">В этой статье также содержатся сведения о устранении [неполадок](#troubleshooting) и [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-109">This article also includes information about [Troubleshooting](#troubleshooting) and [Limitations](#limitations).</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e2c3-110">Шаг 1. Добавление соединителю Graph в Центр администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6e2c3-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="6e2c3-111">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="6e2c3-111">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="6e2c3-112">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="6e2c3-112">Step 2: Name the connection</span></span>

<span data-ttu-id="6e2c3-113">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="6e2c3-113">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="6e2c3-114">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="6e2c3-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="6e2c3-115">Чтобы подключиться к источнику данных, заполните корневой URL-адрес веб-сайта, выберите источник обхода и тип проверки подлинности, который вы хотите использовать: None, Basic Authentication или OAuth 2.0 с [помощью Azure Active Directory (Azure AD).](/azure/active-directory/)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-115">To connect to your data source, fill in the root URL of the website, select a crawl source, and the type of authentication you'd like to use: None, Basic Authentication, or OAuth 2.0 with [Azure Active Directory (Azure AD)](/azure/active-directory/).</span></span> <span data-ttu-id="6e2c3-116">После получения этих сведений выберите тест-подключение для проверки параметров.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-116">After you complete this information, select Test Connection to verify your settings.</span></span>

### <a name="url"></a><span data-ttu-id="6e2c3-117">URL</span><span class="sxs-lookup"><span data-stu-id="6e2c3-117">URL</span></span>

<span data-ttu-id="6e2c3-118">Используйте поле URL-адресов, чтобы указать корень веб-сайта, который необходимо обходить.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-118">Use the URL field to specify the root of the website that you'd like to crawl.</span></span> <span data-ttu-id="6e2c3-119">Соединителя веб-сайтов предприятия будет использовать этот URL-адрес в качестве отправной точки и следовать всем ссылкам из этого URL-адреса для обхода.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-119">The enterprise websites connector will use this URL as the starting point and follow all the links from this URL for its crawl.</span></span>

### <a name="crawl-websites-listed-in-the-sitemap"></a><span data-ttu-id="6e2c3-120">Веб-сайты обхода, указанные в карте сайта</span><span class="sxs-lookup"><span data-stu-id="6e2c3-120">Crawl websites listed in the sitemap</span></span>

<span data-ttu-id="6e2c3-121">При выборе соединитель будет обходать URL-адреса, указанные в карте сайта.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-121">When selected the connector will only crawl the URLs listed in the sitemap.</span></span> <span data-ttu-id="6e2c3-122">Если не выбрана или не найдена карта сайта, соединителя будет глубоко обхода всех ссылок, найденных на корневом URL-адресе сайта.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-122">If not selected or no site map is found, the connector will do a deep crawl of all the links found on the root URL of the site.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="6e2c3-123">![Снимок экрана Параметры подключения для Enterprise соединители](media/enterprise-web-connector/connectors-enterpriseweb-connectionsettings-with-sitemap.png)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-123">![Screenshot of Connection Settings pane for Enterprise Web connector](media/enterprise-web-connector/connectors-enterpriseweb-connectionsettings-with-sitemap.png)</span></span>

### <a name="crawl-mode-cloud-or-on-premises"></a><span data-ttu-id="6e2c3-124">Режим обхода: облако или локальное</span><span class="sxs-lookup"><span data-stu-id="6e2c3-124">Crawl mode: Cloud or On-premises</span></span>

<span data-ttu-id="6e2c3-125">Режим обхода определяет тип веб-сайтов, которые необходимо индексировать, облачные или локально.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-125">The crawl mode determines the type of websites you want to index, either cloud or on-premises.</span></span> <span data-ttu-id="6e2c3-126">Для облачных веб-сайтов выберите **Облако** в качестве режима обхода.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-126">For your cloud websites, select **Cloud** as the crawl mode.</span></span>

<span data-ttu-id="6e2c3-127">Кроме того, соединители теперь поддерживает обход локального веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-127">Also, the connector now supports crawling of on-premises websites.</span></span> <span data-ttu-id="6e2c3-128">Чтобы получить доступ к локальной информации, сначала необходимо установить и настроить Graph соединителя.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-128">To access your on-premises data, you must first install and configure the Graph connector agent.</span></span> <span data-ttu-id="6e2c3-129">Подробнее см. в [Graph агент соединители.](./on-prem-agent.md)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-129">To learn more, see [Graph connector agent](./on-prem-agent.md).</span></span>

<span data-ttu-id="6e2c3-130">Для локального веб-сайтов выберите  Агент в режиме обхода и в поле **On-prem Agent** выберите агент соединительных Graph, который был установлен и настроен ранее.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-130">For your on-premises websites, select **Agent** as the crawl mode and in the **On-prem Agent** field, choose the Graph connector agent that you installed and configured earlier.</span></span>  

### <a name="authentication"></a><span data-ttu-id="6e2c3-131">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="6e2c3-131">Authentication</span></span>

<span data-ttu-id="6e2c3-132">Для базовой проверки подлинности требуется имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-132">Basic Authentication requires a username and password.</span></span> <span data-ttu-id="6e2c3-133">Создайте эту учетную запись бота с помощью [Центр администрирования Microsoft 365.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-133">Create this bot account by using the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="6e2c3-134">OAuth 2.0 с [Azure AD](/azure/active-directory/) требует ИД ресурса, ИД клиента и секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-134">OAuth 2.0 with [Azure AD](/azure/active-directory/) requires a resource ID, Client ID, and Client Secret.</span></span> <span data-ttu-id="6e2c3-135">OAuth 2.0 работает только в облачном режиме.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-135">OAuth 2.0 only works with Cloud mode.</span></span>

<span data-ttu-id="6e2c3-136">Дополнительные сведения см. в странице Авторизованный доступ к Azure Active Directory веб-приложениям с помощью потока грантов кода [OAuth 2.0.](/azure/active-directory/develop/v1-protocols-oauth-code)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-136">For more information, see [Authorize access to Azure Active Directory web applications using OAuth 2.0 code grant flow](/azure/active-directory/develop/v1-protocols-oauth-code).</span></span> <span data-ttu-id="6e2c3-137">Зарегистрируйтесь со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="6e2c3-137">Register with the following values:</span></span>

<span data-ttu-id="6e2c3-138">**Имя:** Поиск (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-138">**Name:** Microsoft Search</span></span> <br/>
<span data-ttu-id="6e2c3-139">**Redirect_URI:**`https://gcs.office.com/v1.0/admin/oauth/callback`</span><span class="sxs-lookup"><span data-stu-id="6e2c3-139">**Redirect_URI:** `https://gcs.office.com/v1.0/admin/oauth/callback`</span></span>

<span data-ttu-id="6e2c3-140">Чтобы получить значения для ресурса, client_id и client_secret перейдите к  коду авторизации для запроса маркера доступа на веб-странице URL-адреса перенаправления.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-140">To get the values for the resource, client_id, and client_secret, go to **Use the authorization code to request an access token** on the redirect URL webpage.</span></span>

<span data-ttu-id="6e2c3-141">Дополнительные сведения см. в [сайте Quickstart: Регистрация](/azure/active-directory/develop/quickstart-register-app)приложения с помощью платформа удостоверений Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-141">For even more information, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

## <a name="step-3a-add-urls-to-exclude-optional-crawl-restrictions"></a><span data-ttu-id="6e2c3-142">Шаг 3a. Добавление URL-адресов для исключения (необязательные ограничения обхода)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-142">Step 3a: Add URLs to exclude (Optional crawl restrictions)</span></span>

<span data-ttu-id="6e2c3-143">Существует два способа предотвратить обход страниц: запретить их в файле robots.txt или добавить их в список исключений.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-143">There are two ways to prevent pages from being crawled: disallow them in your robots.txt file or add them to the Exclusion list.</span></span>

### <a name="support-for-robotstxt"></a><span data-ttu-id="6e2c3-144">Поддержка robots.txt</span><span class="sxs-lookup"><span data-stu-id="6e2c3-144">Support for robots.txt</span></span>

<span data-ttu-id="6e2c3-145">Соединитатель проверяет наличие файла robots.txt корневого сайта и, если он существует, он будет следовать указаниям, найденным в этом файле, и соблюдать их.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-145">The connector checks to see if there is a robots.txt file for your root site and, if one exists, it will follow and respect the directions found within that file.</span></span> <span data-ttu-id="6e2c3-146">Если вы не хотите, чтобы соединитель обходал определенные страницы или каталоги на вашем сайте, вы можете вызвать эти страницы или каталоги в объявлениях "Disallow" в robots.txt файле.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-146">If you do not want the connector to crawl certain pages or directories on your site, you can call out those pages or directories in the "Disallow" declarations in your robots.txt file.</span></span>

### <a name="add-urls-to-exclude"></a><span data-ttu-id="6e2c3-147">Добавление URL-адресов для исключения</span><span class="sxs-lookup"><span data-stu-id="6e2c3-147">Add URLs to exclude</span></span>

<span data-ttu-id="6e2c3-148">Можно дополнительно создать  список исключений, чтобы исключить обход некоторых URL-адресов, если этот контент является конфиденциальным или не стоит обхода.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-148">You can optionally create an **Exclusion list** to exclude some URLs from getting crawled if that content is sensitive or not worth crawling.</span></span> <span data-ttu-id="6e2c3-149">Чтобы создать список исключений, просмотрите корневой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-149">To create an exclusion list, browse through the root URL.</span></span> <span data-ttu-id="6e2c3-150">Исключенные URL-адреса можно добавить в список во время процесса настройки.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-150">You can add the excluded URLs to the list during the configuration process.</span></span>

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="6e2c3-151">Шаг 4. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="6e2c3-151">Step 4: Assign property labels</span></span>

<span data-ttu-id="6e2c3-152">Вы можете назначить свойству источника для каждой метки, выбрав из меню параметры.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-152">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="6e2c3-153">Хотя этот шаг не является обязательным, наличие меток свойств повысит релевантность поиска и обеспечит более точные результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-153">While this step isn't mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="step-5-manage-schema"></a><span data-ttu-id="6e2c3-154">Шаг 5. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="6e2c3-154">Step 5: Manage schema</span></span>

<span data-ttu-id="6e2c3-155">На экране Manage **Schema** можно изменить атрибуты схемы (это параметры **Запрос,** **Поиск,** Извлечение и уточнение), связанные с свойствами, добавить необязательные псевдонимы и выбрать свойство **Content.**  </span><span class="sxs-lookup"><span data-stu-id="6e2c3-155">On the **Manage Schema** screen, you can change the schema attributes (the options are **Query**, **Search**, **Retrieve**, and **Refine**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="6e2c3-156">Шаг 6. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="6e2c3-156">Step 6: Manage search permissions</span></span>

<span data-ttu-id="6e2c3-157">Соедините Enterprise веб-сайтов поддерживает только разрешения поиска, видимые **каждому.**</span><span class="sxs-lookup"><span data-stu-id="6e2c3-157">The Enterprise websites connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="6e2c3-158">Индексные данные появляются в результатах поиска и видны всем пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-158">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="6e2c3-159">Шаг 7. Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="6e2c3-159">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="6e2c3-160">Соедините Enterprise веб-сайтов поддерживает только полное обновление.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-160">The Enterprise websites connector only supports a full refresh.</span></span> <span data-ttu-id="6e2c3-161">Это означает, что соединителер будет повторно заснять все содержимое веб-сайта во время каждого обновления.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-161">This means that the connector will recrawl all the website's content during every refresh.</span></span> <span data-ttu-id="6e2c3-162">Чтобы соединитатель получил достаточно времени для обхода контента, рекомендуется установить большой интервал расписания обновления.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-162">To make sure the connector gets enough time to crawl the content, we recommend that you set a large refresh schedule interval.</span></span> <span data-ttu-id="6e2c3-163">Рекомендуется запланированное обновление от одной до двух недель.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-163">We recommend a scheduled refresh between one and two weeks.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="6e2c3-164">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="6e2c3-164">Step 8: Review connection</span></span>

<span data-ttu-id="6e2c3-165">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="6e2c3-165">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a><span data-ttu-id="6e2c3-166">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="6e2c3-166">Troubleshooting</span></span>

<span data-ttu-id="6e2c3-167">При чтении контента веб-сайта обход может столкнуться с некоторыми исходными ошибками, которые представлены подробными кодами ошибок ниже.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-167">When reading the website's content, the crawl may encounter some source errors, which are represented by the detailed error codes below.</span></span> <span data-ttu-id="6e2c3-168">Чтобы получить дополнительные сведения о типах  ошибок, перейдите на страницу сведения об ошибках после выбора подключения.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-168">To get more information on the types of errors, go to the **error details** page after selecting the connection.</span></span> <span data-ttu-id="6e2c3-169">Выберите код **ошибки,** чтобы увидеть более подробные ошибки.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-169">Select the **error code** to see more detailed errors.</span></span> <span data-ttu-id="6e2c3-170">Кроме того, [обратитесь к управлению соединитетелем,](./manage-connector.md) чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-170">Also refer to [Manage your connector](./manage-connector.md) to learn more.</span></span>

 <span data-ttu-id="6e2c3-171">Подробный код ошибки</span><span class="sxs-lookup"><span data-stu-id="6e2c3-171">Detailed Error code</span></span> | <span data-ttu-id="6e2c3-172">Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="6e2c3-172">Error message</span></span>
 --- | ---
 <span data-ttu-id="6e2c3-173">6001</span><span class="sxs-lookup"><span data-stu-id="6e2c3-173">6001</span></span> | <span data-ttu-id="6e2c3-174">Сайт, который пытаются индексировать, не досяжим</span><span class="sxs-lookup"><span data-stu-id="6e2c3-174">The site that is being tried to index is not reachable</span></span>
 <span data-ttu-id="6e2c3-175">6005</span><span class="sxs-lookup"><span data-stu-id="6e2c3-175">6005</span></span> | <span data-ttu-id="6e2c3-176">Исходные страницы, которые пытаются индексировать, заблокированы по robots.txt конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-176">The source page that is being tried to index has been blocked by as per robots.txt configuration.</span></span>
 <span data-ttu-id="6e2c3-177">6008</span><span class="sxs-lookup"><span data-stu-id="6e2c3-177">6008</span></span> | <span data-ttu-id="6e2c3-178">Невозможно разрешить DNS</span><span class="sxs-lookup"><span data-stu-id="6e2c3-178">Unable to resolve the DNS</span></span>
 <span data-ttu-id="6e2c3-179">6009</span><span class="sxs-lookup"><span data-stu-id="6e2c3-179">6009</span></span> | <span data-ttu-id="6e2c3-180">Для всех клиентских ошибок (кроме HTTP 404, 408) обратитесь к кодам ошибок HTTP 4xx.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-180">For all client-side errors (Except HTTP 404, 408), refer to HTTP 4xx error codes for details.</span></span>
 <span data-ttu-id="6e2c3-181">6013</span><span class="sxs-lookup"><span data-stu-id="6e2c3-181">6013</span></span> | <span data-ttu-id="6e2c3-182">Исходные страницы, которые пытаются индексировать, не удалось найти.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-182">The source page that is being tried to index could not be found.</span></span> <span data-ttu-id="6e2c3-183">(ошибка HTTP 404)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-183">(HTTP 404 error)</span></span>
 <span data-ttu-id="6e2c3-184">6018</span><span class="sxs-lookup"><span data-stu-id="6e2c3-184">6018</span></span> | <span data-ttu-id="6e2c3-185">Исходные страницы не отвечают, и запрос был ото времени. (ОШИБКА HTTP 408)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-185">The source page is not responding, and the request has timed out. (HTTP 408 error)</span></span>
 <span data-ttu-id="6e2c3-186">6021</span><span class="sxs-lookup"><span data-stu-id="6e2c3-186">6021</span></span> | <span data-ttu-id="6e2c3-187">На первой странице, которую пытаются индексировать, нет текстового контента на странице.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-187">The source page that is being tried to index has no textual content on the page.</span></span>
 <span data-ttu-id="6e2c3-188">6023</span><span class="sxs-lookup"><span data-stu-id="6e2c3-188">6023</span></span> | <span data-ttu-id="6e2c3-189">Исходные страницы, которые пытаются индексировать, неподтверчены (не HTML-страница)</span><span class="sxs-lookup"><span data-stu-id="6e2c3-189">The source page that is being tried to index is unsupported (not an HTML page)</span></span>
 <span data-ttu-id="6e2c3-190">6024</span><span class="sxs-lookup"><span data-stu-id="6e2c3-190">6024</span></span> | <span data-ttu-id="6e2c3-191">На первой странице, которую пытаются индексировать, есть неподтверченное содержимое.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-191">The source page that is being tried to index has unsupported content.</span></span>

* <span data-ttu-id="6e2c3-192">Ошибки 6001-6013 возникают, когда источник данных не может быть достигнут из-за проблемы с сетью или при удалении, перемещении или переименовании самого источника данных.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-192">Errors 6001-6013 occur when the data source is not reachable due to a network issue or when the data source itself is deleted, moved, or renamed.</span></span> <span data-ttu-id="6e2c3-193">Проверьте, действительны ли предоставленные сведения о источнике данных.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-193">Check if the data source details provided are still valid.</span></span>
* <span data-ttu-id="6e2c3-194">Ошибки 6021-6024 возникают, когда источник данных содержит не текстовый контент на странице или когда страница не является HTML.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-194">Errors 6021-6024 occur when the data source contains non-textual content on the page or when the page is not an HTML.</span></span> <span data-ttu-id="6e2c3-195">Проверьте источник данных и добавьте эту страницу в список исключений или игнорируйте ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-195">Check the data source and add this page in exclusion list or ignore the error.</span></span>

## <a name="limitations"></a><span data-ttu-id="6e2c3-196">Ограничения</span><span class="sxs-lookup"><span data-stu-id="6e2c3-196">Limitations</span></span>

<span data-ttu-id="6e2c3-197">Соедините Enterprise веб-сайтов не поддерживает поиск данных на **динамических веб-сайтах.**</span><span class="sxs-lookup"><span data-stu-id="6e2c3-197">The Enterprise websites connector doesn't support searching data on **dynamic webpages**.</span></span> <span data-ttu-id="6e2c3-198">Примеры этих веб-страниц живут в системах управления контентом, таких как [Confluence](https://www.atlassian.com/software/confluence) и [Unily,](https://www.unily.com/) или базах данных, которые хранят содержимое веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="6e2c3-198">Examples of those webpages live in content management systems like [Confluence](https://www.atlassian.com/software/confluence) and [Unily](https://www.unily.com/) or databases that store website content.</span></span>