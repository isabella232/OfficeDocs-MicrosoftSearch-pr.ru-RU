---
title: Соединители Salesforce Graph для Поиска (Майкрософт)
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединители Salesforce Graph для Поиска (Майкрософт)
ms.openlocfilehash: 0b80bf7d3296236887d1cc1bf8e75da976b6a1f1
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50085023"
---
<!---Previous ms.author: rusamai --->

# <a name="salesforce-graph-connector-preview"></a><span data-ttu-id="fb093-103">Соединители Salesforce Graph (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fb093-103">Salesforce Graph connector (preview)</span></span>

<span data-ttu-id="fb093-104">Соединители Salesforce Graph позволяют организации индексировать объекты Contacts, Opportunities, Leads и Accounts в экземпляре Salesforce.</span><span class="sxs-lookup"><span data-stu-id="fb093-104">The Salesforce Graph connector, allows your organization to index Contacts, Opportunities, Leads, and Accounts objects in your Salesforce instance.</span></span> <span data-ttu-id="fb093-105">После настройки соединители и индекса контента из Salesforce конечные пользователи могут искать эти элементы из любого клиента Поиска (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="fb093-105">After you configure the connector and index content from Salesforce, end users can search for those items from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="fb093-106">Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="fb093-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="fb093-107">Эта статья для всех, кто настраивает, запускает и отслеживает соединители ServiceNow Graph.</span><span class="sxs-lookup"><span data-stu-id="fb093-107">This article is for anyone who configures, runs, and monitors a ServiceNow Graph connector.</span></span> <span data-ttu-id="fb093-108">Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединитену Salesforce Graph.</span><span class="sxs-lookup"><span data-stu-id="fb093-108">It supplements the general setup process, and shows instructions that apply only for the Salesforce Graph connector.</span></span> <span data-ttu-id="fb093-109">В этой статье также содержатся сведения об [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="fb093-109">This article also includes information about [Limitations](#limitations).</span></span>

>[!IMPORTANT]
><span data-ttu-id="fb093-110">The Salesforce Graph connector currently supports Summer '19 or later.</span><span class="sxs-lookup"><span data-stu-id="fb093-110">The Salesforce Graph connector currently supports Summer '19 or later.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="fb093-111">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="fb093-111">Before you get started</span></span>

<span data-ttu-id="fb093-112">Чтобы подключиться к экземпляру Salesforce, вам потребуется URL-адрес экземпляра Salesforce, ИД клиента и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="fb093-112">To connect to your Salesforce instance, you need your Salesforce instance URL, the Client ID, and Client Secret for OAuth authentication.</span></span> <span data-ttu-id="fb093-113">Ниже объясняется, как вы или ваш администратор Salesforce можете получить эти сведения из своей учетной записи Salesforce:</span><span class="sxs-lookup"><span data-stu-id="fb093-113">The following steps explain how you or your Salesforce administrator can get this information from your Salesforce account:</span></span>

- <span data-ttu-id="fb093-114">Войдите в экземпляр Salesforce и перейдите к настройке</span><span class="sxs-lookup"><span data-stu-id="fb093-114">Log in to your Salesforce instance and go to Setup</span></span>

- <span data-ttu-id="fb093-115">Перейдите в app -> App Manager.</span><span class="sxs-lookup"><span data-stu-id="fb093-115">Navigate to Apps -> App Manager.</span></span>

- <span data-ttu-id="fb093-116">Выберите **новое подключенный приложение.**</span><span class="sxs-lookup"><span data-stu-id="fb093-116">Select **New connected app**.</span></span>

- <span data-ttu-id="fb093-117">Заполняйте раздел API следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fb093-117">Complete the API section as follows:</span></span>

    - <span data-ttu-id="fb093-118">Выберите параметр "Включить **параметры Oauth".**</span><span class="sxs-lookup"><span data-stu-id="fb093-118">Select the checkbox for **Enable Oauth Settings**.</span></span>

    - <span data-ttu-id="fb093-119">Укажите URL-адрес для вызова в качестве: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span><span class="sxs-lookup"><span data-stu-id="fb093-119">Specify the Callback URL as: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span></span>

    - <span data-ttu-id="fb093-120">Выберите эти необходимые области OAuth.</span><span class="sxs-lookup"><span data-stu-id="fb093-120">Select these required OAuth scopes.</span></span>

        - <span data-ttu-id="fb093-121">Доступ к данным (api) и управление ими</span><span class="sxs-lookup"><span data-stu-id="fb093-121">Access and manage your data (api)</span></span>

        - <span data-ttu-id="fb093-122">Выполнять запросы от вашего имени в любое время (refresh_token, offline_access)</span><span class="sxs-lookup"><span data-stu-id="fb093-122">Perform requests on your behalf at any time (refresh_token, offline_access)</span></span>

    - <span data-ttu-id="fb093-123">Select the checkbox for **Require secret for web server flow**.</span><span class="sxs-lookup"><span data-stu-id="fb093-123">Select the checkbox for **Require secret for web server flow**.</span></span>

    - <span data-ttu-id="fb093-124">Сохраните приложение.</span><span class="sxs-lookup"><span data-stu-id="fb093-124">Save the app.</span></span>
    
      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="fb093-125">![Раздел API в экземпляре Salesforce после того, как администратор ввели все необходимые конфигурации, перечисленные выше.](media/salesforce-connector/sf1.png)</span><span class="sxs-lookup"><span data-stu-id="fb093-125">![API section in Salesforce instance after admin has entered all required configurations listed above.](media/salesforce-connector/sf1.png)</span></span>

- <span data-ttu-id="fb093-126">Скопируйте ключ потребителя и секрет потребителя.</span><span class="sxs-lookup"><span data-stu-id="fb093-126">Copy the consumer key and the consumer secret.</span></span> <span data-ttu-id="fb093-127">Эти сведения будут использоваться в качестве ИД клиента и секрета клиента при настройке параметров подключения для соединители Graph на портале администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fb093-127">This information will be used as the Client ID and the Client Secret when you configure the Connection Settings for your Graph Connector in the Microsoft 365 admin portal.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="fb093-128">![Результаты, возвращаемые разделом API в экземпляре Salesforce после того, как администратор отправил все необходимые конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fb093-128">![Results returned by API section in Salesforce instance after admin has submitted all required configurations.</span></span> <span data-ttu-id="fb093-129">Ключ потребителя находится вверху левого столбца, а секрет потребителя — вверху правого столбца.](media/salesforce-connector/clientsecret.png)</span><span class="sxs-lookup"><span data-stu-id="fb093-129">Consumer Key is at top of left column and Consumer Secret is at top of right column.](media/salesforce-connector/clientsecret.png)</span></span>
  
- <span data-ttu-id="fb093-130">Перед закрытием экземпляра Salesforce выполните следующие действия, чтобы срок действия маркеров обновления не истекал:</span><span class="sxs-lookup"><span data-stu-id="fb093-130">Before closing your Salesforce instance, follow these steps to ensure that refresh tokens don't expire:</span></span>
    - <span data-ttu-id="fb093-131">Go to Apps -> App Manager</span><span class="sxs-lookup"><span data-stu-id="fb093-131">Go to Apps -> App Manager</span></span>
    - <span data-ttu-id="fb093-132">Найдите созданное приложение и выберите его справа.</span><span class="sxs-lookup"><span data-stu-id="fb093-132">Find the app you created and select the drop-down on the right.</span></span> <span data-ttu-id="fb093-133">Выберите **"Управление"**</span><span class="sxs-lookup"><span data-stu-id="fb093-133">Select **Manage**</span></span>
    - <span data-ttu-id="fb093-134">Выбор **политик редактирования**</span><span class="sxs-lookup"><span data-stu-id="fb093-134">Select **edit policies**</span></span>
    - <span data-ttu-id="fb093-135">Для политики маркеров обновления выберите "Маркер **обновления" действительным, пока не будет отозван**</span><span class="sxs-lookup"><span data-stu-id="fb093-135">For refresh token policy, select **Refresh token is valid until revoked**</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="fb093-136">![Выберите политику маркеров обновления с именем "Маркер обновления действителен до отзыва"](media/salesforce-connector/oauthpolicies.png)</span><span class="sxs-lookup"><span data-stu-id="fb093-136">![Select the Refresh Token Policy named "Refresh token is valid until revoked "](media/salesforce-connector/oauthpolicies.png)</span></span>

<span data-ttu-id="fb093-137">Теперь вы можете использовать Центр администрирования [M365](https://admin.microsoft.com/) для завершения остального процесса настройки соединители Graph.</span><span class="sxs-lookup"><span data-stu-id="fb093-137">You can now use the [M365 Admin Center](https://admin.microsoft.com/) to complete the rest of the setup process for your Graph connector.</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="fb093-138">Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fb093-138">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="fb093-139">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="fb093-139">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="fb093-140">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="fb093-140">Step 2: Name the connection</span></span>

<span data-ttu-id="fb093-141">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="fb093-141">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="fb093-142">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="fb093-142">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="fb093-143">Для URL-адреса экземпляра используйте https://[domain].my.salesforce.com, где доменом будет домен Salesforce для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="fb093-143">For the Instance URL, use https://[domain].my.salesforce.com where domain would be the Salesforce domain for your organization.</span></span>

<span data-ttu-id="fb093-144">Введите ИД клиента и секрет клиента, полученные из экземпляра Salesforce, и выберите "Вход".</span><span class="sxs-lookup"><span data-stu-id="fb093-144">Enter the Client ID and Client Secret you obtained from your Salesforce instance and select Sign in.</span></span>

<span data-ttu-id="fb093-145">При первой попытке входа с помощью этих параметров вы получите всплывающее всплывающее поле с запросом на вход в Salesforce с помощью имени пользователя и пароля администратора.</span><span class="sxs-lookup"><span data-stu-id="fb093-145">The first time you've attempted to sign in with these settings, you'll get a pop-up asking you to log in to Salesforce with your admin username and password.</span></span> <span data-ttu-id="fb093-146">На снимке экрана ниже показано всплывающее изображение.</span><span class="sxs-lookup"><span data-stu-id="fb093-146">The screenshot below shows the popup.</span></span> <span data-ttu-id="fb093-147">Введите свои учетные данные и выберите "Войти".</span><span class="sxs-lookup"><span data-stu-id="fb093-147">Enter your credentials and select "Log In".</span></span>

  ![Всплывающее всплывающее поле с запросом имени пользователя и пароля.](media/salesforce-connector/sf4.png)

  >[!NOTE]
  ><span data-ttu-id="fb093-149">Если всплывающее окна не отображаются, оно может быть заблокировано в браузере, поэтому необходимо разрешить всплывающие окна и перенаправления.</span><span class="sxs-lookup"><span data-stu-id="fb093-149">If the pop up does not appear, it might be getting blocked in your browser, so you must allow pop-ups and redirects.</span></span>

<span data-ttu-id="fb093-150">Убедитесь, что подключение успешно с помощью поиска зеленого баннера с надписью "Подключение успешно", как покажите на снимке экрана ниже.</span><span class="sxs-lookup"><span data-stu-id="fb093-150">Check that the connection was successful by searching for a green banner that says "Connection successful" as show in the screenshot below.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="fb093-151">![Снимок экрана: успешный вход.</span><span class="sxs-lookup"><span data-stu-id="fb093-151">![Screenshot of successful login.</span></span> <span data-ttu-id="fb093-152">Зеленый баннер с надписью "Подключение успешно" находится в поле URL-адреса экземпляра Salesforce](media/salesforce-connector/sf5.png)</span><span class="sxs-lookup"><span data-stu-id="fb093-152">The green banner that says "Connection successful" is located under the field for your Salesforce Instance URL](media/salesforce-connector/sf5.png)</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="fb093-153">Шаг 4. Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="fb093-153">Step 4: Manage search permissions</span></span>

<span data-ttu-id="fb093-154">Вам потребуется выбрать, какие пользователи будут видеть результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="fb093-154">You'll need to choose which users will see search results from this data source.</span></span> <span data-ttu-id="fb093-155">Если вы разрешаете только определенным пользователям Azure Active Directory (Azure AD) или пользователям, не относящемся к Azure AD, видеть результаты поиска, убедитесь, что вы соедиав удостоверения.</span><span class="sxs-lookup"><span data-stu-id="fb093-155">If you allow only certain Azure Active Directory (Azure AD) or Non-Azure AD users to see the search results, make sure you map the identities.</span></span>

## <a name="step-4a-select-permissions"></a><span data-ttu-id="fb093-156">Шаг 4а. Выбор разрешений</span><span class="sxs-lookup"><span data-stu-id="fb093-156">Step 4a: Select permissions</span></span>

<span data-ttu-id="fb093-157">Вы можете выбрать доступ к спискам управления доступом (ALS) из экземпляра Salesforce или разрешить всем пользователям в организации видеть результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="fb093-157">You can choose to ingest Access Control Lists (ACLs) from your Salesforce instance, or allow everyone in your organization to see search results from this data source.</span></span> <span data-ttu-id="fb093-158">ALS могут включать удостоверения Azure Active Directory (AAD) (пользователей, которые являются федеративными из Azure AD в Salesforce), удостоверения, не включавшие Azure AD (у пользователей Salesforce, у которых есть соответствующие удостоверения в Azure AD) или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="fb093-158">ACLs can include Azure Active Directory (AAD) identities (users who are federated from Azure AD to Salesforce), non-Azure AD identities (native Salesforce users who have corresponding identities in Azure AD), or both.</span></span>

>[!NOTE]
><span data-ttu-id="fb093-159">Если используется сторонний поставщик удостоверений, например Ping ID или secureAuth, следует выбрать тип удостоверения " non-AAD".</span><span class="sxs-lookup"><span data-stu-id="fb093-159">If you use a third-party Identity Provider like Ping ID or secureAuth, you should select "non-AAD" as the identity type.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="fb093-160">![Выберите экран разрешений, который был завершен администратором. Администратор выбрал параметр "Только люди с доступом к этому источнику данных" и также выбрал "AAD" в выпадающего меню типов удостоверений.](media/salesforce-connector/sf6.png)</span><span class="sxs-lookup"><span data-stu-id="fb093-160">![Select permissions screen that has been completed by an admin. The admin has selected the "Only people with access to this data source" option and has also selected "AAD" from a drop down menu of identity types.](media/salesforce-connector/sf6.png)</span></span>

<span data-ttu-id="fb093-161">Если вы решили получить ACL из экземпляра Salesforce и выбрали "не AAD" для типа удостоверений, см. инструкции по сопоставлению удостоверений, не относяшихся к [Azure AD.](map-non-aad.md)</span><span class="sxs-lookup"><span data-stu-id="fb093-161">If you chose to ingest an ACL from your Salesforce instance and selected "non-AAD" for the identity type, see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span>

## <a name="step-4b-map-aad-identities"></a><span data-ttu-id="fb093-162">Шаг 4b. Карта удостоверений AAD</span><span class="sxs-lookup"><span data-stu-id="fb093-162">Step 4b: Map AAD identities</span></span>

<span data-ttu-id="fb093-163">Если вы решили получить ACL из экземпляра Salesforce и выбрали "AAD" для типа удостоверения, см. инструкции по сопоставлению удостоверений в сопоставлении удостоверений с использованием удостоверений [Azure AD.](map-aad.md)</span><span class="sxs-lookup"><span data-stu-id="fb093-163">If you chose to ingest an ACL from your Salesforce instance and selected "AAD" for the identity type, see [Map your Azure AD Identities](map-aad.md) for instructions on mapping the identities.</span></span> <span data-ttu-id="fb093-164">Чтобы узнать, как настроить службу SSO Azure AD для Salesforce, см. этот [учебник.](https://docs.microsoft.com/azure/active-directory/saas-apps/salesforce-tutorial)</span><span class="sxs-lookup"><span data-stu-id="fb093-164">To learn how to set up Azure AD SSO for Salesforce, see this [tutorial](https://docs.microsoft.com/azure/active-directory/saas-apps/salesforce-tutorial).</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="fb093-165">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="fb093-165">Step 5: Assign property labels</span></span>

<span data-ttu-id="fb093-166">Для каждой метки можно назначить свойство источника, выбрав в меню параметры.</span><span class="sxs-lookup"><span data-stu-id="fb093-166">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="fb093-167">Хотя этот шаг не является обязательным, наличие некоторых меток свойств улучшит релевантность поиска и обеспечит более лучшие результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="fb093-167">While this step is not mandatory, having some property labels will improve the search relevance and ensure better search results for end users.</span></span> <span data-ttu-id="fb093-168">По умолчанию некоторые метки, такие как "Title", "URL", "CreatedBy" и "LastModifiedBy", уже назначены свойства источника.</span><span class="sxs-lookup"><span data-stu-id="fb093-168">By default, some of the Labels like "Title," "URL," "CreatedBy," and  "LastModifiedBy" have already been assigned source properties.</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="fb093-169">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="fb093-169">Step 6: Manage schema</span></span>

<span data-ttu-id="fb093-170">Можно выбрать, какие свойства источника должны быть проиндексироваться, чтобы они отображились в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="fb093-170">You can select what source properties should be indexed so that they show up in search results.</span></span> <span data-ttu-id="fb093-171">Мастер подключения по умолчанию выбирает схему поиска на основе набора свойств источника.</span><span class="sxs-lookup"><span data-stu-id="fb093-171">The connection wizard by default selects a search schema based on a set of source properties.</span></span> <span data-ttu-id="fb093-172">Вы можете изменить его, выбрав флажки для каждого свойства и атрибута на странице схемы поиска.</span><span class="sxs-lookup"><span data-stu-id="fb093-172">You can modify it by selecting the check boxes for each property and attribute in the search schema page.</span></span> <span data-ttu-id="fb093-173">К атрибутам схемы поиска относятся поиск, запрос, извлечение и уточнение.</span><span class="sxs-lookup"><span data-stu-id="fb093-173">Search schema attributes include Search, Query, Retrieve, and Refine.</span></span>
<span data-ttu-id="fb093-174">Уточнение позволяет определить свойства, которые впоследствии можно использовать в качестве настраиваемой уточнения или фильтров в окне поиска.</span><span class="sxs-lookup"><span data-stu-id="fb093-174">Refine allows you to define the properties that can be later used as custom refiners or filters in the search experience.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="fb093-175">![Выберите схему для каждого свойства источника.</span><span class="sxs-lookup"><span data-stu-id="fb093-175">![Select the schema for each source property.</span></span> <span data-ttu-id="fb093-176">Возможные варианты: запрос, поиск, извлечение и уточнение](media/salesforce-connector/sf9.png)</span><span class="sxs-lookup"><span data-stu-id="fb093-176">The options are Query, Search, Retrieve, and Refine](media/salesforce-connector/sf9.png)</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="fb093-177">Шаг 7. Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="fb093-177">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="fb093-178">В настоящее время соединители Salesforce поддерживают только расписания обновления для полных обходов.</span><span class="sxs-lookup"><span data-stu-id="fb093-178">The Salesforce connector only supports refresh schedules for full crawls currently.</span></span>

>[!IMPORTANT]
><span data-ttu-id="fb093-179">При полном обходе находятся удаленные объекты и пользователи, которые ранее синхронизировались с индексом Поиска (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="fb093-179">A full crawl finds deleted objects and users that were previously synced to the Microsoft Search index.</span></span>

<span data-ttu-id="fb093-180">Рекомендуемое расписание составляет одну неделю для полного обхода контента.</span><span class="sxs-lookup"><span data-stu-id="fb093-180">The recommended schedule is one week for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="fb093-181">Шаг 8. Проверка подключения</span><span class="sxs-lookup"><span data-stu-id="fb093-181">Step 8: Review connection</span></span>

<span data-ttu-id="fb093-182">Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)</span><span class="sxs-lookup"><span data-stu-id="fb093-182">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="fb093-183">Ограничения</span><span class="sxs-lookup"><span data-stu-id="fb093-183">Limitations</span></span>

- <span data-ttu-id="fb093-184">В настоящее время соединители Graph не поддерживают общий доступ и общий доступ на основе Apex на основе территории с помощью личных групп из Salesforce.</span><span class="sxs-lookup"><span data-stu-id="fb093-184">The Graph connector doesn't currently support Apex based, territory-based sharing and sharing using personal groups from Salesforce.</span></span>
- <span data-ttu-id="fb093-185">В API Salesforce, который используется соединитетелем Graph, существует известная ошибка, из-за которой в настоящее время не используются значения по умолчанию для частных организаций для клиентов.</span><span class="sxs-lookup"><span data-stu-id="fb093-185">There's a known bug in the Salesforce API the Graph connector uses, where the private org-wide defaults for leads aren't honored currently.</span></span>  
- <span data-ttu-id="fb093-186">Если для профиля в поле установлена служба безопасности уровня поля (FLS), соединителевая служба Graph не будет вламять это поле для профилей в этой организации Salesforce. В результате пользователи не смогут искать значения для этих полей и не будут отыщите их в результатах.</span><span class="sxs-lookup"><span data-stu-id="fb093-186">If a field has field level security (FLS) set for a profile, the Graph connector won't ingest that field for any profiles in that Salesforce org. As a result, users won't be able to search on values for those fields, nor will it show up in the results.</span></span>  
- <span data-ttu-id="fb093-187">На экране "Управление схемой" эти стандартные имена свойств перечислены один раз: "Запрос", "Поиск", **"Извлечение"** и **"Уточнение"** и будут применяться к всем или нет.</span><span class="sxs-lookup"><span data-stu-id="fb093-187">In the Manage Schema screen these common standard property names are listed once, the options are **Query**, **Search**, **Retrieve**, and **Refine**, and apply to all or none.</span></span>
    - <span data-ttu-id="fb093-188">Имя</span><span class="sxs-lookup"><span data-stu-id="fb093-188">Name</span></span>
    - <span data-ttu-id="fb093-189">Url</span><span class="sxs-lookup"><span data-stu-id="fb093-189">Url</span></span>
    - <span data-ttu-id="fb093-190">Описание</span><span class="sxs-lookup"><span data-stu-id="fb093-190">Description</span></span>
    - <span data-ttu-id="fb093-191">Fax</span><span class="sxs-lookup"><span data-stu-id="fb093-191">Fax</span></span>
    - <span data-ttu-id="fb093-192">Phone</span><span class="sxs-lookup"><span data-stu-id="fb093-192">Phone</span></span>
    - <span data-ttu-id="fb093-193">MobilePhone</span><span class="sxs-lookup"><span data-stu-id="fb093-193">MobilePhone</span></span>
    - <span data-ttu-id="fb093-194">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="fb093-194">Email</span></span>
    - <span data-ttu-id="fb093-195">Тип</span><span class="sxs-lookup"><span data-stu-id="fb093-195">Type</span></span>
    - <span data-ttu-id="fb093-196">Название</span><span class="sxs-lookup"><span data-stu-id="fb093-196">Title</span></span>
    - <span data-ttu-id="fb093-197">AccountId</span><span class="sxs-lookup"><span data-stu-id="fb093-197">AccountId</span></span>
    - <span data-ttu-id="fb093-198">AccountName</span><span class="sxs-lookup"><span data-stu-id="fb093-198">AccountName</span></span>
    - <span data-ttu-id="fb093-199">AccountUrl</span><span class="sxs-lookup"><span data-stu-id="fb093-199">AccountUrl</span></span>
    - <span data-ttu-id="fb093-200">AccountOwner</span><span class="sxs-lookup"><span data-stu-id="fb093-200">AccountOwner</span></span>
    - <span data-ttu-id="fb093-201">AccountOwnerUrl</span><span class="sxs-lookup"><span data-stu-id="fb093-201">AccountOwnerUrl</span></span>
    - <span data-ttu-id="fb093-202">Владелец</span><span class="sxs-lookup"><span data-stu-id="fb093-202">Owner</span></span>
    - <span data-ttu-id="fb093-203">OwnerUrl</span><span class="sxs-lookup"><span data-stu-id="fb093-203">OwnerUrl</span></span>
    - <span data-ttu-id="fb093-204">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="fb093-204">CreatedBy</span></span>
    - <span data-ttu-id="fb093-205">CreatedByUrl</span><span class="sxs-lookup"><span data-stu-id="fb093-205">CreatedByUrl</span></span>
    - <span data-ttu-id="fb093-206">LastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="fb093-206">LastModifiedBy</span></span>
    - <span data-ttu-id="fb093-207">LastModifiedByUrl</span><span class="sxs-lookup"><span data-stu-id="fb093-207">LastModifiedByUrl</span></span>
    - <span data-ttu-id="fb093-208">LastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="fb093-208">LastModifiedDate</span></span>
    - <span data-ttu-id="fb093-209">ObjectName</span><span class="sxs-lookup"><span data-stu-id="fb093-209">ObjectName</span></span>
