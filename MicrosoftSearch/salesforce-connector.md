---
title: Соединители Graph salesforce для поиска в Microsoft Search
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
description: Настройка соединитетеля salesforce Graph Microsoft Search
ms.openlocfilehash: d4d19c05f82ddb28c4dc3e6719bf8ea8d7284cc3
ms.sourcegitcommit: 1b154441f3a3abba0f2719e66a767432bc9506ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2021
ms.locfileid: "52720991"
---
<!---Previous ms.author: rusamai --->

# <a name="salesforce-graph-connector-preview"></a><span data-ttu-id="0146c-103">Соединители Graph Salesforce (предварительный просмотр)</span><span class="sxs-lookup"><span data-stu-id="0146c-103">Salesforce Graph connector (preview)</span></span>

<span data-ttu-id="0146c-104">Соединитетельный Graph Salesforce позволяет организации индексировать объекты Contacts, Opportunities, Leads и Accounts в экземпляре Salesforce.</span><span class="sxs-lookup"><span data-stu-id="0146c-104">The Salesforce Graph connector, allows your organization to index Contacts, Opportunities, Leads, and Accounts objects in your Salesforce instance.</span></span> <span data-ttu-id="0146c-105">После настройки соединители и индекса контента из Salesforce конечные пользователи могут искать эти элементы из любого клиента Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="0146c-105">After you configure the connector and index content from Salesforce, end users can search for those items from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="0146c-106">Ознакомьтесь [**с статьей Установка Graph,**](configure-connector.md) чтобы понять общие инструкции Graph соединители.</span><span class="sxs-lookup"><span data-stu-id="0146c-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="0146c-107">Эта статья для всех, кто настраивает, запускает и контролирует соединители Graph Salesforce.</span><span class="sxs-lookup"><span data-stu-id="0146c-107">This article is for anyone who configures, runs, and monitors a Salesforce Graph connector.</span></span> <span data-ttu-id="0146c-108">Он дополняет общий процесс установки и показывает инструкции, которые применяются только для соединитетеля Salesforce Graph.</span><span class="sxs-lookup"><span data-stu-id="0146c-108">It supplements the general setup process, and shows instructions that apply only for the Salesforce Graph connector.</span></span> <span data-ttu-id="0146c-109">В этой статье также содержатся сведения об [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="0146c-109">This article also includes information about [Limitations](#limitations).</span></span>

>[!IMPORTANT]
><span data-ttu-id="0146c-110">Соединители salesforce Graph в настоящее время поддерживает лето '19 или более поздно.</span><span class="sxs-lookup"><span data-stu-id="0146c-110">The Salesforce Graph connector currently supports Summer '19 or later.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="0146c-111">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="0146c-111">Before you get started</span></span>

<span data-ttu-id="0146c-112">Чтобы подключиться к экземпляру Salesforce, вам потребуется URL-адрес экземпляра Salesforce, идентификация клиента и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="0146c-112">To connect to your Salesforce instance, you need your Salesforce instance URL, the Client ID, and Client Secret for OAuth authentication.</span></span> <span data-ttu-id="0146c-113">В следующих действиях объясняется, как вы или администратор Salesforce можете получать эти сведения из учетной записи Salesforce:</span><span class="sxs-lookup"><span data-stu-id="0146c-113">The following steps explain how you or your Salesforce administrator can get this information from your Salesforce account:</span></span>

- <span data-ttu-id="0146c-114">Войдите в экземпляр Salesforce и перейдите к установке</span><span class="sxs-lookup"><span data-stu-id="0146c-114">Log in to your Salesforce instance and go to Setup</span></span>

- <span data-ttu-id="0146c-115">Перейдите к Apps-> App Manager.</span><span class="sxs-lookup"><span data-stu-id="0146c-115">Navigate to Apps -> App Manager.</span></span>

- <span data-ttu-id="0146c-116">Выберите **новое подключенного приложения.**</span><span class="sxs-lookup"><span data-stu-id="0146c-116">Select **New connected app**.</span></span>

- <span data-ttu-id="0146c-117">Выполните раздел API следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0146c-117">Complete the API section as follows:</span></span>

    - <span data-ttu-id="0146c-118">Выберите почтовый ящик **для включить Oauth Параметры**.</span><span class="sxs-lookup"><span data-stu-id="0146c-118">Select the checkbox for **Enable Oauth Settings**.</span></span>

    - <span data-ttu-id="0146c-119">Укажите URL-адрес вызова в качестве: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span><span class="sxs-lookup"><span data-stu-id="0146c-119">Specify the Callback URL as: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span></span>

    - <span data-ttu-id="0146c-120">Выберите эти необходимые области OAuth.</span><span class="sxs-lookup"><span data-stu-id="0146c-120">Select these required OAuth scopes.</span></span>

        - <span data-ttu-id="0146c-121">Доступ и управление данными (aPI)</span><span class="sxs-lookup"><span data-stu-id="0146c-121">Access and manage your data (api)</span></span>

        - <span data-ttu-id="0146c-122">Выполнение запросов от вашего имени в любое время (refresh_token, offline_access)</span><span class="sxs-lookup"><span data-stu-id="0146c-122">Perform requests on your behalf at any time (refresh_token, offline_access)</span></span>

    - <span data-ttu-id="0146c-123">Выберите почтовый ящик **для секрета Require для потока веб-сервера.**</span><span class="sxs-lookup"><span data-stu-id="0146c-123">Select the checkbox for **Require secret for web server flow**.</span></span>

    - <span data-ttu-id="0146c-124">Сохраните приложение.</span><span class="sxs-lookup"><span data-stu-id="0146c-124">Save the app.</span></span>
    
      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="0146c-125">![Раздел API в экземпляре Salesforce после того, как администратор вошел во все указанные выше конфигурации.](media/salesforce-connector/sf1.png)</span><span class="sxs-lookup"><span data-stu-id="0146c-125">![API section in Salesforce instance after admin has entered all required configurations listed above.](media/salesforce-connector/sf1.png)</span></span>

- <span data-ttu-id="0146c-126">Скопируйте ключ потребителя и секрет потребителя.</span><span class="sxs-lookup"><span data-stu-id="0146c-126">Copy the consumer key and the consumer secret.</span></span> <span data-ttu-id="0146c-127">Эти сведения будут использоваться в качестве ИД клиента и секрета клиента при настройке Параметры подключения для Graph соединители на портале администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0146c-127">This information will be used as the Client ID and the Client Secret when you configure the Connection Settings for your Graph Connector in the Microsoft 365 admin portal.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0146c-128">![Результаты, возвращаемые в разделе API в экземпляре Salesforce после отправки администратором всех необходимых конфигураций.</span><span class="sxs-lookup"><span data-stu-id="0146c-128">![Results returned by API section in Salesforce instance after admin has submitted all required configurations.</span></span> <span data-ttu-id="0146c-129">Потребительский ключ находится в верхней части левого столбца, а Consumer Secret — в верхней части правой колонки.](media/salesforce-connector/clientsecret.png)</span><span class="sxs-lookup"><span data-stu-id="0146c-129">Consumer Key is at top of left column and Consumer Secret is at top of right column.](media/salesforce-connector/clientsecret.png)</span></span>
  
- <span data-ttu-id="0146c-130">Перед закрытием экземпляра Salesforce выполните следующие действия, чтобы срок действия маркеров обновления не истек:</span><span class="sxs-lookup"><span data-stu-id="0146c-130">Before closing your Salesforce instance, follow these steps to ensure that refresh tokens don't expire:</span></span>
    - <span data-ttu-id="0146c-131">Перейдите в Apps -> App Manager</span><span class="sxs-lookup"><span data-stu-id="0146c-131">Go to Apps -> App Manager</span></span>
    - <span data-ttu-id="0146c-132">Найдите созданное приложение и выберите выпадаемую справа.</span><span class="sxs-lookup"><span data-stu-id="0146c-132">Find the app you created and select the drop-down on the right.</span></span> <span data-ttu-id="0146c-133">Выберите **Управление**</span><span class="sxs-lookup"><span data-stu-id="0146c-133">Select **Manage**</span></span>
    - <span data-ttu-id="0146c-134">Выбор **политик редактирования**</span><span class="sxs-lookup"><span data-stu-id="0146c-134">Select **edit policies**</span></span>
    - <span data-ttu-id="0146c-135">Для политики обновления маркеров выберите маркер **Обновления, допустимый до отзыва**</span><span class="sxs-lookup"><span data-stu-id="0146c-135">For refresh token policy, select **Refresh token is valid until revoked**</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0146c-136">![Выберите политику маркера обновления с именем "Маркер обновления действителен до отзыва"](media/salesforce-connector/oauthpolicies.png)</span><span class="sxs-lookup"><span data-stu-id="0146c-136">![Select the Refresh Token Policy named "Refresh token is valid until revoked "](media/salesforce-connector/oauthpolicies.png)</span></span>

<span data-ttu-id="0146c-137">Теперь вы можете использовать [центр администрирования M365](https://admin.microsoft.com/) для завершения остальной части процесса установки Graph соединители.</span><span class="sxs-lookup"><span data-stu-id="0146c-137">You can now use the [M365 Admin Center](https://admin.microsoft.com/) to complete the rest of the setup process for your Graph connector.</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="0146c-138">Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0146c-138">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="0146c-139">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="0146c-139">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="0146c-140">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="0146c-140">Step 2: Name the connection</span></span>

<span data-ttu-id="0146c-141">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="0146c-141">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="0146c-142">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="0146c-142">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="0146c-143">Для URL-адреса экземпляра используйте https://[domain].my.salesforce.com, где доменом будет домен Salesforce для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0146c-143">For the Instance URL, use https://[domain].my.salesforce.com where domain would be the Salesforce domain for your organization.</span></span>

<span data-ttu-id="0146c-144">Введите ИД клиента и секрет клиента, полученные из экземпляра Salesforce, и выберите Вход.</span><span class="sxs-lookup"><span data-stu-id="0146c-144">Enter the Client ID and Client Secret you obtained from your Salesforce instance and select Sign in.</span></span>

<span data-ttu-id="0146c-145">При первой попытке входа с этими настройками вы получите всплывающее всплывающее поле с просьбой войти в Salesforce с иным и иным и паролем администратора.</span><span class="sxs-lookup"><span data-stu-id="0146c-145">The first time you've attempted to sign in with these settings, you'll get a pop-up asking you to log in to Salesforce with your admin username and password.</span></span> <span data-ttu-id="0146c-146">На скриншоте ниже показано всплывающее всплывающее изображение.</span><span class="sxs-lookup"><span data-stu-id="0146c-146">The screenshot below shows the popup.</span></span> <span data-ttu-id="0146c-147">Введите учетные данные и выберите "Вход".</span><span class="sxs-lookup"><span data-stu-id="0146c-147">Enter your credentials and select "Log In".</span></span>

  ![Всплывающее всплывающее имя пользователя и пароль.](media/salesforce-connector/sf4.png)

  >[!NOTE]
  ><span data-ttu-id="0146c-149">Если всплывающее не появится, оно может быть заблокировано в браузере, поэтому необходимо разрешить всплывающие окна и перенаправления.</span><span class="sxs-lookup"><span data-stu-id="0146c-149">If the pop up does not appear, it might be getting blocked in your browser, so you must allow pop-ups and redirects.</span></span>

<span data-ttu-id="0146c-150">Убедитесь, что подключение было успешным путем поиска зеленого баннера с надписью "Подключение успешно", как покажите на скриншоте ниже.</span><span class="sxs-lookup"><span data-stu-id="0146c-150">Check that the connection was successful by searching for a green banner that says "Connection successful" as show in the screenshot below.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0146c-151">![Снимок экрана успешного входа.</span><span class="sxs-lookup"><span data-stu-id="0146c-151">![Screenshot of successful login.</span></span> <span data-ttu-id="0146c-152">Зеленый баннер с надписью "Подключение успешно" расположен в поле для URL-адреса экземпляра Salesforce](media/salesforce-connector/sf5.png)</span><span class="sxs-lookup"><span data-stu-id="0146c-152">The green banner that says "Connection successful" is located under the field for your Salesforce Instance URL](media/salesforce-connector/sf5.png)</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="0146c-153">Шаг 4. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="0146c-153">Step 4: Manage search permissions</span></span>

<span data-ttu-id="0146c-154">Необходимо выбрать, какие пользователи будут видеть результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="0146c-154">You'll need to choose which users will see search results from this data source.</span></span> <span data-ttu-id="0146c-155">Если вы разрешаете видеть результаты поиска только определенным пользователям Azure Active Directory (Azure AD) или Non-Azure AD, убедитесь, что вы на карте удостоверений.</span><span class="sxs-lookup"><span data-stu-id="0146c-155">If you allow only certain Azure Active Directory (Azure AD) or Non-Azure AD users to see the search results, make sure you map the identities.</span></span>

### <a name="step-4a-select-permissions"></a><span data-ttu-id="0146c-156">Шаг 4.a. Выбор разрешений</span><span class="sxs-lookup"><span data-stu-id="0146c-156">Step 4.a: Select permissions</span></span>

<span data-ttu-id="0146c-157">Вы можете выбрать для получения списков управления доступом (ACLs) из экземпляра Salesforce или разрешить всем в вашей организации видеть результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="0146c-157">You can choose to ingest Access Control Lists (ACLs) from your Salesforce instance, or allow everyone in your organization to see search results from this data source.</span></span> <span data-ttu-id="0146c-158">AcLs могут включать Azure Active Directory (AAD) удостоверений (пользователей, которые являются федеративами от Azure AD до Salesforce), удостоверений нелазурной AD (местных пользователей Salesforce, которые имеют соответствующие удостоверения в Azure AD) или обоих.</span><span class="sxs-lookup"><span data-stu-id="0146c-158">ACLs can include Azure Active Directory (AAD) identities (users who are federated from Azure AD to Salesforce), non-Azure AD identities (native Salesforce users who have corresponding identities in Azure AD), or both.</span></span>

>[!NOTE]
><span data-ttu-id="0146c-159">Если используется сторонний поставщик удостоверений, например Ping ID или secureAuth, в качестве типа удостоверения следует выбрать "non-AAD".</span><span class="sxs-lookup"><span data-stu-id="0146c-159">If you use a third-party Identity Provider like Ping ID or secureAuth, you should select "non-AAD" as the identity type.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0146c-160">![Выберите экран разрешений, завершенный администратором. Администратор выбрал параметр "Только люди с доступом к этому источнику данных", а также выбрал "AAD" из выпадающего меню типов удостоверений.](media/salesforce-connector/sf6.png)</span><span class="sxs-lookup"><span data-stu-id="0146c-160">![Select permissions screen that has been completed by an admin. The admin has selected the "Only people with access to this data source" option and has also selected "AAD" from a drop down menu of identity types.](media/salesforce-connector/sf6.png)</span></span>

<span data-ttu-id="0146c-161">Если вы решили гнать ACL из экземпляра Salesforce и выбрали "non-AAD" для типа удостоверений, см. в примере Map [your non-Azure AD Identitys](map-non-aad.md) для инструкций по сопоставлению удостоверений.</span><span class="sxs-lookup"><span data-stu-id="0146c-161">If you chose to ingest an ACL from your Salesforce instance and selected "non-AAD" for the identity type, see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span>

### <a name="step-4b-map-aad-identities"></a><span data-ttu-id="0146c-162">Шаг 4.b. Идентификаторы AAD</span><span class="sxs-lookup"><span data-stu-id="0146c-162">Step 4.b: Map AAD identities</span></span>

<span data-ttu-id="0146c-163">Если вы решили гнать ACL из экземпляра Salesforce и выбрали AAD для типа удостоверений, см. в примере Map [your Azure AD Identitys](map-aad.md) для инструкций по сопоставлению удостоверений.</span><span class="sxs-lookup"><span data-stu-id="0146c-163">If you chose to ingest an ACL from your Salesforce instance and selected "AAD" for the identity type, see [Map your Azure AD Identities](map-aad.md) for instructions on mapping the identities.</span></span> <span data-ttu-id="0146c-164">Подробнее о том, как настроить SSO Azure AD для Salesforce, см. в этом [руководстве.](/azure/active-directory/saas-apps/salesforce-tutorial)</span><span class="sxs-lookup"><span data-stu-id="0146c-164">To learn how to set up Azure AD SSO for Salesforce, see this [tutorial](/azure/active-directory/saas-apps/salesforce-tutorial).</span></span>

### <a name="apply-user-mapping-to-sync-your-salesforce-identities-to-azure-ad-identities"></a><span data-ttu-id="0146c-165">Применение сопоставления пользователей для синхронизации удостоверений Salesforce с удостоверениями Azure AD</span><span class="sxs-lookup"><span data-stu-id="0146c-165">Apply user mapping to sync your Salesforce identities to Azure AD identities</span></span>

<span data-ttu-id="0146c-166">В этом видео вы можете увидеть процесс проверки подлинности в экземпляре Salesforce, синхронизировать свои удостоверения Azure Active Directory с удостоверениями Azure Active Directory и применить соответствующие обрезки безопасности для элементов Salesforce.</span><span class="sxs-lookup"><span data-stu-id="0146c-166">In this video you can see the process to authenticate to your Salesforce instance, sync your non-Azure Active Directory identities to your Azure Active Directory identities, and apply the proper security trimmings to your Salesforce items.</span></span>

> [!VIDEO https://www.youtube.com/watch?v=SZYiFxZMKcM]

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="0146c-167">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="0146c-167">Step 5: Assign property labels</span></span>

<span data-ttu-id="0146c-168">Вы можете назначить свойству источника для каждой метки, выбрав из меню параметры.</span><span class="sxs-lookup"><span data-stu-id="0146c-168">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="0146c-169">Хотя этот шаг не является обязательным, наличие некоторых меток свойств повысит релевантность поиска и обеспечит лучшие результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="0146c-169">While this step is not mandatory, having some property labels will improve the search relevance and ensure better search results for end users.</span></span> <span data-ttu-id="0146c-170">По умолчанию некоторые метки, такие как "Title", "URL", "CreatedBy" и "LastModifiedBy", уже назначены исходные свойства.</span><span class="sxs-lookup"><span data-stu-id="0146c-170">By default, some of the Labels like "Title," "URL," "CreatedBy," and  "LastModifiedBy" have already been assigned source properties.</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="0146c-171">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="0146c-171">Step 6: Manage schema</span></span>

<span data-ttu-id="0146c-172">Можно выбрать, какие исходные свойства следует проиндексировать, чтобы они были в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="0146c-172">You can select what source properties should be indexed so that they show up in search results.</span></span> <span data-ttu-id="0146c-173">Мастер подключения по умолчанию выбирает схему поиска на основе набора исходных свойств.</span><span class="sxs-lookup"><span data-stu-id="0146c-173">The connection wizard by default selects a search schema based on a set of source properties.</span></span> <span data-ttu-id="0146c-174">Вы можете изменить его, выбрав флажки для каждого свойства и атрибута на странице схемы поиска.</span><span class="sxs-lookup"><span data-stu-id="0146c-174">You can modify it by selecting the check boxes for each property and attribute in the search schema page.</span></span> <span data-ttu-id="0146c-175">Атрибуты схемы поиска включают поиск, запрос, извлечение и уточнение.</span><span class="sxs-lookup"><span data-stu-id="0146c-175">Search schema attributes include Search, Query, Retrieve, and Refine.</span></span>
<span data-ttu-id="0146c-176">Уточнение позволяет определить свойства, которые впоследствии можно использовать в качестве настраиваемой переработчики или фильтры в опытом поиска.</span><span class="sxs-lookup"><span data-stu-id="0146c-176">Refine allows you to define the properties that can be later used as custom refiners or filters in the search experience.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0146c-177">![Выберите схему для каждого свойства источника.</span><span class="sxs-lookup"><span data-stu-id="0146c-177">![Select the schema for each source property.</span></span> <span data-ttu-id="0146c-178">Параметры: Запрос, Поиск, Извлечение и Уточнение](media/salesforce-connector/sf9.png)</span><span class="sxs-lookup"><span data-stu-id="0146c-178">The options are Query, Search, Retrieve, and Refine](media/salesforce-connector/sf9.png)</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="0146c-179">Шаг 7. Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="0146c-179">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="0146c-180">Соединители Salesforce поддерживает только расписание обновления для полного обхода в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="0146c-180">The Salesforce connector only supports refresh schedules for full crawls currently.</span></span>

>[!IMPORTANT]
><span data-ttu-id="0146c-181">Полный обход находит удаленные объекты и пользователей, которые ранее синхронизировались с индексом Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="0146c-181">A full crawl finds deleted objects and users that were previously synced to the Microsoft Search index.</span></span>

<span data-ttu-id="0146c-182">Рекомендуемое расписание — одна неделя для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="0146c-182">The recommended schedule is one week for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="0146c-183">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="0146c-183">Step 8: Review connection</span></span>

<span data-ttu-id="0146c-184">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="0146c-184">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="0146c-185">Ограничения</span><span class="sxs-lookup"><span data-stu-id="0146c-185">Limitations</span></span>

- <span data-ttu-id="0146c-186">Соедините Graph в настоящее время не поддерживает совместное использование и совместное использование персональных групп из Salesforce на основе Apex.</span><span class="sxs-lookup"><span data-stu-id="0146c-186">The Graph connector doesn't currently support Apex based, territory-based sharing and sharing using personal groups from Salesforce.</span></span>
- <span data-ttu-id="0146c-187">Существует известная ошибка в API Salesforce, Graph соединительщика, где частные значения по умолчанию для лид-клиентов в настоящее время не чтются.</span><span class="sxs-lookup"><span data-stu-id="0146c-187">There's a known bug in the Salesforce API the Graph connector uses, where the private org-wide defaults for leads aren't honored currently.</span></span>  
- <span data-ttu-id="0146c-188">Если для профиля установлено полевой уровень безопасности (FLS), соединителер Graph не будет гнать это поле для профилей в этой организации Salesforce. В результате пользователи не смогут искать значения для этих полей и не будут показываться в результатах.</span><span class="sxs-lookup"><span data-stu-id="0146c-188">If a field has field level security (FLS) set for a profile, the Graph connector won't ingest that field for any profiles in that Salesforce org. As a result, users won't be able to search on values for those fields, nor will it show up in the results.</span></span>  
- <span data-ttu-id="0146c-189">В экране Управление схемой эти общие стандартные имена свойств перечислены один раз, параметры **запроса,** **поиска,** получения и уточнения **и** применяются к всем или нет.</span><span class="sxs-lookup"><span data-stu-id="0146c-189">In the Manage Schema screen these common standard property names are listed once, the options are **Query**, **Search**, **Retrieve**, and **Refine**, and apply to all or none.</span></span>
    - <span data-ttu-id="0146c-190">Имя</span><span class="sxs-lookup"><span data-stu-id="0146c-190">Name</span></span>
    - <span data-ttu-id="0146c-191">Url</span><span class="sxs-lookup"><span data-stu-id="0146c-191">Url</span></span>
    - <span data-ttu-id="0146c-192">Описание</span><span class="sxs-lookup"><span data-stu-id="0146c-192">Description</span></span>
    - <span data-ttu-id="0146c-193">Fax</span><span class="sxs-lookup"><span data-stu-id="0146c-193">Fax</span></span>
    - <span data-ttu-id="0146c-194">Phone</span><span class="sxs-lookup"><span data-stu-id="0146c-194">Phone</span></span>
    - <span data-ttu-id="0146c-195">MobilePhone</span><span class="sxs-lookup"><span data-stu-id="0146c-195">MobilePhone</span></span>
    - <span data-ttu-id="0146c-196">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="0146c-196">Email</span></span>
    - <span data-ttu-id="0146c-197">Тип</span><span class="sxs-lookup"><span data-stu-id="0146c-197">Type</span></span>
    - <span data-ttu-id="0146c-198">Название</span><span class="sxs-lookup"><span data-stu-id="0146c-198">Title</span></span>
    - <span data-ttu-id="0146c-199">AccountId</span><span class="sxs-lookup"><span data-stu-id="0146c-199">AccountId</span></span>
    - <span data-ttu-id="0146c-200">Имя учетной записи</span><span class="sxs-lookup"><span data-stu-id="0146c-200">AccountName</span></span>
    - <span data-ttu-id="0146c-201">AccountUrl</span><span class="sxs-lookup"><span data-stu-id="0146c-201">AccountUrl</span></span>
    - <span data-ttu-id="0146c-202">AccountOwner</span><span class="sxs-lookup"><span data-stu-id="0146c-202">AccountOwner</span></span>
    - <span data-ttu-id="0146c-203">AccountOwnerUrl</span><span class="sxs-lookup"><span data-stu-id="0146c-203">AccountOwnerUrl</span></span>
    - <span data-ttu-id="0146c-204">Владелец</span><span class="sxs-lookup"><span data-stu-id="0146c-204">Owner</span></span>
    - <span data-ttu-id="0146c-205">OwnerUrl</span><span class="sxs-lookup"><span data-stu-id="0146c-205">OwnerUrl</span></span>
    - <span data-ttu-id="0146c-206">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="0146c-206">CreatedBy</span></span>
    - <span data-ttu-id="0146c-207">CreatedByUrl</span><span class="sxs-lookup"><span data-stu-id="0146c-207">CreatedByUrl</span></span>
    - <span data-ttu-id="0146c-208">LastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="0146c-208">LastModifiedBy</span></span>
    - <span data-ttu-id="0146c-209">LastModifiedByUrl</span><span class="sxs-lookup"><span data-stu-id="0146c-209">LastModifiedByUrl</span></span>
    - <span data-ttu-id="0146c-210">LastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="0146c-210">LastModifiedDate</span></span>
    - <span data-ttu-id="0146c-211">ObjectName</span><span class="sxs-lookup"><span data-stu-id="0146c-211">ObjectName</span></span>
