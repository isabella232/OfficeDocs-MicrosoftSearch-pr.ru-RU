---
title: Соединителе Salesforce Graph для поиска в Microsoft Search
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
description: Настройка соединитетеля Salesforce Graph для поиска в Microsoft Search
ms.openlocfilehash: 59cc321a40655a1c1e5edf615dd43a2a56c8ddbc
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031686"
---
<!---Previous ms.author: rusamai --->

# <a name="salesforce-graph-connector-preview"></a><span data-ttu-id="28d87-103">Соединитетор Salesforce Graph (предварительный просмотр)</span><span class="sxs-lookup"><span data-stu-id="28d87-103">Salesforce Graph connector (preview)</span></span>

<span data-ttu-id="28d87-104">Соединитатель Salesforce Graph позволяет организации индексировать объекты Contacts, Opportunities, Leads и Accounts в экземпляре Salesforce.</span><span class="sxs-lookup"><span data-stu-id="28d87-104">The Salesforce Graph connector, allows your organization to index Contacts, Opportunities, Leads, and Accounts objects in your Salesforce instance.</span></span> <span data-ttu-id="28d87-105">После настройки соединители и индекса контента из Salesforce конечные пользователи могут искать эти элементы из любого клиента Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="28d87-105">After you configure the connector and index content from Salesforce, end users can search for those items from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="28d87-106">Ознакомьтесь [**с статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общие инструкции по настройке соединитений Graph.</span><span class="sxs-lookup"><span data-stu-id="28d87-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="28d87-107">Эта статья для всех, кто настраивает, запускает и отслеживает соединители Salesforce Graph.</span><span class="sxs-lookup"><span data-stu-id="28d87-107">This article is for anyone who configures, runs, and monitors a Salesforce Graph connector.</span></span> <span data-ttu-id="28d87-108">Он дополняет общий процесс установки и показывает инструкции, применимые только к соединитеку Salesforce Graph.</span><span class="sxs-lookup"><span data-stu-id="28d87-108">It supplements the general setup process, and shows instructions that apply only for the Salesforce Graph connector.</span></span> <span data-ttu-id="28d87-109">В этой статье также содержатся сведения об [ограничениях.](#limitations)</span><span class="sxs-lookup"><span data-stu-id="28d87-109">This article also includes information about [Limitations](#limitations).</span></span>

>[!IMPORTANT]
><span data-ttu-id="28d87-110">Соединители Диаграмма Salesforce в настоящее время поддерживает лето '19 или более поздно.</span><span class="sxs-lookup"><span data-stu-id="28d87-110">The Salesforce Graph connector currently supports Summer '19 or later.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="28d87-111">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="28d87-111">Before you get started</span></span>

<span data-ttu-id="28d87-112">Чтобы подключиться к экземпляру Salesforce, вам потребуется URL-адрес экземпляра Salesforce, идентификация клиента и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="28d87-112">To connect to your Salesforce instance, you need your Salesforce instance URL, the Client ID, and Client Secret for OAuth authentication.</span></span> <span data-ttu-id="28d87-113">В следующих действиях объясняется, как вы или администратор Salesforce можете получать эти сведения из учетной записи Salesforce:</span><span class="sxs-lookup"><span data-stu-id="28d87-113">The following steps explain how you or your Salesforce administrator can get this information from your Salesforce account:</span></span>

- <span data-ttu-id="28d87-114">Войдите в экземпляр Salesforce и перейдите к установке</span><span class="sxs-lookup"><span data-stu-id="28d87-114">Log in to your Salesforce instance and go to Setup</span></span>

- <span data-ttu-id="28d87-115">Перейдите к Apps-> App Manager.</span><span class="sxs-lookup"><span data-stu-id="28d87-115">Navigate to Apps -> App Manager.</span></span>

- <span data-ttu-id="28d87-116">Выберите **новое подключенного приложения.**</span><span class="sxs-lookup"><span data-stu-id="28d87-116">Select **New connected app**.</span></span>

- <span data-ttu-id="28d87-117">Выполните раздел API следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28d87-117">Complete the API section as follows:</span></span>

    - <span data-ttu-id="28d87-118">Выберите почтовый ящик **для включить параметры Oauth.**</span><span class="sxs-lookup"><span data-stu-id="28d87-118">Select the checkbox for **Enable Oauth Settings**.</span></span>

    - <span data-ttu-id="28d87-119">Укажите URL-адрес вызова в качестве: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span><span class="sxs-lookup"><span data-stu-id="28d87-119">Specify the Callback URL as: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span></span>

    - <span data-ttu-id="28d87-120">Выберите эти необходимые области OAuth.</span><span class="sxs-lookup"><span data-stu-id="28d87-120">Select these required OAuth scopes.</span></span>

        - <span data-ttu-id="28d87-121">Доступ и управление данными (aPI)</span><span class="sxs-lookup"><span data-stu-id="28d87-121">Access and manage your data (api)</span></span>

        - <span data-ttu-id="28d87-122">Выполнение запросов от вашего имени в любое время (refresh_token, offline_access)</span><span class="sxs-lookup"><span data-stu-id="28d87-122">Perform requests on your behalf at any time (refresh_token, offline_access)</span></span>

    - <span data-ttu-id="28d87-123">Выберите почтовый ящик **для секрета Require для потока веб-сервера.**</span><span class="sxs-lookup"><span data-stu-id="28d87-123">Select the checkbox for **Require secret for web server flow**.</span></span>

    - <span data-ttu-id="28d87-124">Сохраните приложение.</span><span class="sxs-lookup"><span data-stu-id="28d87-124">Save the app.</span></span>
    
      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="28d87-125">![Раздел API в экземпляре Salesforce после того, как администратор вошел во все указанные выше конфигурации.](media/salesforce-connector/sf1.png)</span><span class="sxs-lookup"><span data-stu-id="28d87-125">![API section in Salesforce instance after admin has entered all required configurations listed above.](media/salesforce-connector/sf1.png)</span></span>

- <span data-ttu-id="28d87-126">Скопируйте ключ потребителя и секрет потребителя.</span><span class="sxs-lookup"><span data-stu-id="28d87-126">Copy the consumer key and the consumer secret.</span></span> <span data-ttu-id="28d87-127">Эти сведения будут использоваться в качестве ИД клиента и секрета клиента при настройке параметров подключения для вашего соединители графа на портале администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="28d87-127">This information will be used as the Client ID and the Client Secret when you configure the Connection Settings for your Graph Connector in the Microsoft 365 admin portal.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="28d87-128">![Результаты, возвращаемые в разделе API в экземпляре Salesforce после отправки администратором всех необходимых конфигураций.</span><span class="sxs-lookup"><span data-stu-id="28d87-128">![Results returned by API section in Salesforce instance after admin has submitted all required configurations.</span></span> <span data-ttu-id="28d87-129">Потребительский ключ находится в верхней части левого столбца, а Consumer Secret — в верхней части правой колонки.](media/salesforce-connector/clientsecret.png)</span><span class="sxs-lookup"><span data-stu-id="28d87-129">Consumer Key is at top of left column and Consumer Secret is at top of right column.](media/salesforce-connector/clientsecret.png)</span></span>
  
- <span data-ttu-id="28d87-130">Перед закрытием экземпляра Salesforce выполните следующие действия, чтобы срок действия маркеров обновления не истек:</span><span class="sxs-lookup"><span data-stu-id="28d87-130">Before closing your Salesforce instance, follow these steps to ensure that refresh tokens don't expire:</span></span>
    - <span data-ttu-id="28d87-131">Перейдите в Apps -> App Manager</span><span class="sxs-lookup"><span data-stu-id="28d87-131">Go to Apps -> App Manager</span></span>
    - <span data-ttu-id="28d87-132">Найдите созданное приложение и выберите выпадаемую справа.</span><span class="sxs-lookup"><span data-stu-id="28d87-132">Find the app you created and select the drop-down on the right.</span></span> <span data-ttu-id="28d87-133">Выберите **Управление**</span><span class="sxs-lookup"><span data-stu-id="28d87-133">Select **Manage**</span></span>
    - <span data-ttu-id="28d87-134">Выбор **политик редактирования**</span><span class="sxs-lookup"><span data-stu-id="28d87-134">Select **edit policies**</span></span>
    - <span data-ttu-id="28d87-135">Для политики обновления маркеров выберите маркер **Обновления, допустимый до отзыва**</span><span class="sxs-lookup"><span data-stu-id="28d87-135">For refresh token policy, select **Refresh token is valid until revoked**</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="28d87-136">![Выберите политику маркера обновления с именем "Маркер обновления действителен до отзыва"](media/salesforce-connector/oauthpolicies.png)</span><span class="sxs-lookup"><span data-stu-id="28d87-136">![Select the Refresh Token Policy named "Refresh token is valid until revoked "](media/salesforce-connector/oauthpolicies.png)</span></span>

<span data-ttu-id="28d87-137">Теперь вы можете использовать [центр администрирования M365](https://admin.microsoft.com/) для завершения остальной части процесса настройки соединиттеля Graph.</span><span class="sxs-lookup"><span data-stu-id="28d87-137">You can now use the [M365 Admin Center](https://admin.microsoft.com/) to complete the rest of the setup process for your Graph connector.</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="28d87-138">Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="28d87-138">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="28d87-139">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="28d87-139">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="28d87-140">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="28d87-140">Step 2: Name the connection</span></span>

<span data-ttu-id="28d87-141">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="28d87-141">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="28d87-142">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="28d87-142">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="28d87-143">Для URL-адреса экземпляра используйте https://[domain].my.salesforce.com, где доменом будет домен Salesforce для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="28d87-143">For the Instance URL, use https://[domain].my.salesforce.com where domain would be the Salesforce domain for your organization.</span></span>

<span data-ttu-id="28d87-144">Введите ИД клиента и секрет клиента, полученные из экземпляра Salesforce, и выберите Вход.</span><span class="sxs-lookup"><span data-stu-id="28d87-144">Enter the Client ID and Client Secret you obtained from your Salesforce instance and select Sign in.</span></span>

<span data-ttu-id="28d87-145">При первой попытке входа с этими настройками вы получите всплывающее всплывающее поле с просьбой войти в Salesforce с иным и иным и паролем администратора.</span><span class="sxs-lookup"><span data-stu-id="28d87-145">The first time you've attempted to sign in with these settings, you'll get a pop-up asking you to log in to Salesforce with your admin username and password.</span></span> <span data-ttu-id="28d87-146">На скриншоте ниже показано всплывающее всплывающее изображение.</span><span class="sxs-lookup"><span data-stu-id="28d87-146">The screenshot below shows the popup.</span></span> <span data-ttu-id="28d87-147">Введите учетные данные и выберите "Вход".</span><span class="sxs-lookup"><span data-stu-id="28d87-147">Enter your credentials and select "Log In".</span></span>

  ![Всплывающее всплывающее имя пользователя и пароль.](media/salesforce-connector/sf4.png)

  >[!NOTE]
  ><span data-ttu-id="28d87-149">Если всплывающее не появится, оно может быть заблокировано в браузере, поэтому необходимо разрешить всплывающие окна и перенаправления.</span><span class="sxs-lookup"><span data-stu-id="28d87-149">If the pop up does not appear, it might be getting blocked in your browser, so you must allow pop-ups and redirects.</span></span>

<span data-ttu-id="28d87-150">Убедитесь, что подключение было успешным путем поиска зеленого баннера с надписью "Подключение успешно", как покажите на скриншоте ниже.</span><span class="sxs-lookup"><span data-stu-id="28d87-150">Check that the connection was successful by searching for a green banner that says "Connection successful" as show in the screenshot below.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="28d87-151">![Снимок экрана успешного входа.</span><span class="sxs-lookup"><span data-stu-id="28d87-151">![Screenshot of successful login.</span></span> <span data-ttu-id="28d87-152">Зеленый баннер с надписью "Подключение успешно" расположен в поле для URL-адреса экземпляра Salesforce](media/salesforce-connector/sf5.png)</span><span class="sxs-lookup"><span data-stu-id="28d87-152">The green banner that says "Connection successful" is located under the field for your Salesforce Instance URL](media/salesforce-connector/sf5.png)</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="28d87-153">Шаг 4. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="28d87-153">Step 4: Manage search permissions</span></span>

<span data-ttu-id="28d87-154">Необходимо выбрать, какие пользователи будут видеть результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="28d87-154">You'll need to choose which users will see search results from this data source.</span></span> <span data-ttu-id="28d87-155">Если вы разрешаете видеть результаты поиска только определенным пользователям Azure Active Directory (Azure AD) или Non-Azure AD, убедитесь, что вы на карте удостоверений.</span><span class="sxs-lookup"><span data-stu-id="28d87-155">If you allow only certain Azure Active Directory (Azure AD) or Non-Azure AD users to see the search results, make sure you map the identities.</span></span>

## <a name="step-4a-select-permissions"></a><span data-ttu-id="28d87-156">Шаг 4a. Выбор разрешений</span><span class="sxs-lookup"><span data-stu-id="28d87-156">Step 4a: Select permissions</span></span>

<span data-ttu-id="28d87-157">Вы можете выбрать для получения списков управления доступом (ACLs) из экземпляра Salesforce или разрешить всем в вашей организации видеть результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="28d87-157">You can choose to ingest Access Control Lists (ACLs) from your Salesforce instance, or allow everyone in your organization to see search results from this data source.</span></span> <span data-ttu-id="28d87-158">Идентификаторы ACLs могут включать идентификаторы Azure Active Directory (AAD) (пользователи, которые являются федеративами от Azure AD до Salesforce), удостоверения без Azure AD (местные пользователи Salesforce, которые имеют соответствующие удостоверения в Azure AD) или оба.</span><span class="sxs-lookup"><span data-stu-id="28d87-158">ACLs can include Azure Active Directory (AAD) identities (users who are federated from Azure AD to Salesforce), non-Azure AD identities (native Salesforce users who have corresponding identities in Azure AD), or both.</span></span>

>[!NOTE]
><span data-ttu-id="28d87-159">Если используется сторонний поставщик удостоверений, например Ping ID или secureAuth, в качестве типа удостоверения следует выбрать "non-AAD".</span><span class="sxs-lookup"><span data-stu-id="28d87-159">If you use a third-party Identity Provider like Ping ID or secureAuth, you should select "non-AAD" as the identity type.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="28d87-160">![Выберите экран разрешений, завершенный администратором. Администратор выбрал параметр "Только люди с доступом к этому источнику данных", а также выбрал "AAD" из выпадающего меню типов удостоверений.](media/salesforce-connector/sf6.png)</span><span class="sxs-lookup"><span data-stu-id="28d87-160">![Select permissions screen that has been completed by an admin. The admin has selected the "Only people with access to this data source" option and has also selected "AAD" from a drop down menu of identity types.](media/salesforce-connector/sf6.png)</span></span>

<span data-ttu-id="28d87-161">Если вы решили гнать ACL из экземпляра Salesforce и выбрали "non-AAD" для типа удостоверений, см. в примере Map [your non-Azure AD Identitys](map-non-aad.md) для инструкций по сопоставлению удостоверений.</span><span class="sxs-lookup"><span data-stu-id="28d87-161">If you chose to ingest an ACL from your Salesforce instance and selected "non-AAD" for the identity type, see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span>

## <a name="step-4b-map-aad-identities"></a><span data-ttu-id="28d87-162">Шаг 4b: идентификаторы AAD</span><span class="sxs-lookup"><span data-stu-id="28d87-162">Step 4b: Map AAD identities</span></span>

<span data-ttu-id="28d87-163">Если вы решили гнать ACL из экземпляра Salesforce и выбрали AAD для типа удостоверений, см. в примере Map [your Azure AD Identitys](map-aad.md) для инструкций по сопоставлению удостоверений.</span><span class="sxs-lookup"><span data-stu-id="28d87-163">If you chose to ingest an ACL from your Salesforce instance and selected "AAD" for the identity type, see [Map your Azure AD Identities](map-aad.md) for instructions on mapping the identities.</span></span> <span data-ttu-id="28d87-164">Подробнее о том, как настроить SSO Azure AD для Salesforce, см. в этом [руководстве.](/azure/active-directory/saas-apps/salesforce-tutorial)</span><span class="sxs-lookup"><span data-stu-id="28d87-164">To learn how to set up Azure AD SSO for Salesforce, see this [tutorial](/azure/active-directory/saas-apps/salesforce-tutorial).</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="28d87-165">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="28d87-165">Step 5: Assign property labels</span></span>

<span data-ttu-id="28d87-166">Вы можете назначить свойству источника для каждой метки, выбрав из меню параметры.</span><span class="sxs-lookup"><span data-stu-id="28d87-166">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="28d87-167">Хотя этот шаг не является обязательным, наличие некоторых меток свойств повысит релевантность поиска и обеспечит лучшие результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="28d87-167">While this step is not mandatory, having some property labels will improve the search relevance and ensure better search results for end users.</span></span> <span data-ttu-id="28d87-168">По умолчанию некоторые метки, такие как "Title", "URL", "CreatedBy" и "LastModifiedBy", уже назначены исходные свойства.</span><span class="sxs-lookup"><span data-stu-id="28d87-168">By default, some of the Labels like "Title," "URL," "CreatedBy," and  "LastModifiedBy" have already been assigned source properties.</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="28d87-169">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="28d87-169">Step 6: Manage schema</span></span>

<span data-ttu-id="28d87-170">Можно выбрать, какие исходные свойства следует проиндексировать, чтобы они были в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="28d87-170">You can select what source properties should be indexed so that they show up in search results.</span></span> <span data-ttu-id="28d87-171">Мастер подключения по умолчанию выбирает схему поиска на основе набора исходных свойств.</span><span class="sxs-lookup"><span data-stu-id="28d87-171">The connection wizard by default selects a search schema based on a set of source properties.</span></span> <span data-ttu-id="28d87-172">Вы можете изменить его, выбрав флажки для каждого свойства и атрибута на странице схемы поиска.</span><span class="sxs-lookup"><span data-stu-id="28d87-172">You can modify it by selecting the check boxes for each property and attribute in the search schema page.</span></span> <span data-ttu-id="28d87-173">Атрибуты схемы поиска включают поиск, запрос, извлечение и уточнение.</span><span class="sxs-lookup"><span data-stu-id="28d87-173">Search schema attributes include Search, Query, Retrieve, and Refine.</span></span>
<span data-ttu-id="28d87-174">Уточнение позволяет определить свойства, которые впоследствии можно использовать в качестве настраиваемой переработчики или фильтры в опытом поиска.</span><span class="sxs-lookup"><span data-stu-id="28d87-174">Refine allows you to define the properties that can be later used as custom refiners or filters in the search experience.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="28d87-175">![Выберите схему для каждого свойства источника.</span><span class="sxs-lookup"><span data-stu-id="28d87-175">![Select the schema for each source property.</span></span> <span data-ttu-id="28d87-176">Параметры: Запрос, Поиск, Извлечение и Уточнение](media/salesforce-connector/sf9.png)</span><span class="sxs-lookup"><span data-stu-id="28d87-176">The options are Query, Search, Retrieve, and Refine](media/salesforce-connector/sf9.png)</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="28d87-177">Шаг 7. Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="28d87-177">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="28d87-178">Соединители Salesforce поддерживает только расписание обновления для полного обхода в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="28d87-178">The Salesforce connector only supports refresh schedules for full crawls currently.</span></span>

>[!IMPORTANT]
><span data-ttu-id="28d87-179">Полный обход находит удаленные объекты и пользователей, которые ранее синхронизировались с индексом Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="28d87-179">A full crawl finds deleted objects and users that were previously synced to the Microsoft Search index.</span></span>

<span data-ttu-id="28d87-180">Рекомендуемое расписание — одна неделя для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="28d87-180">The recommended schedule is one week for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="28d87-181">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="28d87-181">Step 8: Review connection</span></span>

<span data-ttu-id="28d87-182">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="28d87-182">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="28d87-183">Ограничения</span><span class="sxs-lookup"><span data-stu-id="28d87-183">Limitations</span></span>

- <span data-ttu-id="28d87-184">Соединитатель Graph в настоящее время не поддерживает обмен и совместное использование персональных групп из Salesforce на основе Apex, а также общий доступ к данным на основе территорий.</span><span class="sxs-lookup"><span data-stu-id="28d87-184">The Graph connector doesn't currently support Apex based, territory-based sharing and sharing using personal groups from Salesforce.</span></span>
- <span data-ttu-id="28d87-185">В API Salesforce, который используется соединитетелем Graph, существует известная ошибка, в которой частные по умолчанию для лид-клиентов в настоящее время не чтются.</span><span class="sxs-lookup"><span data-stu-id="28d87-185">There's a known bug in the Salesforce API the Graph connector uses, where the private org-wide defaults for leads aren't honored currently.</span></span>  
- <span data-ttu-id="28d87-186">Если для профиля установлено полевой уровень безопасности (FLS), соединителер Graph не будет гнать это поле для любых профилей в этой организации Salesforce. В результате пользователи не смогут искать значения для этих полей и не будут показываться в результатах.</span><span class="sxs-lookup"><span data-stu-id="28d87-186">If a field has field level security (FLS) set for a profile, the Graph connector won't ingest that field for any profiles in that Salesforce org. As a result, users won't be able to search on values for those fields, nor will it show up in the results.</span></span>  
- <span data-ttu-id="28d87-187">В экране Управление схемой эти общие стандартные имена свойств перечислены один раз, параметры **запроса,** **поиска,** получения и уточнения **и** применяются к всем или нет.</span><span class="sxs-lookup"><span data-stu-id="28d87-187">In the Manage Schema screen these common standard property names are listed once, the options are **Query**, **Search**, **Retrieve**, and **Refine**, and apply to all or none.</span></span>
    - <span data-ttu-id="28d87-188">Имя</span><span class="sxs-lookup"><span data-stu-id="28d87-188">Name</span></span>
    - <span data-ttu-id="28d87-189">Url</span><span class="sxs-lookup"><span data-stu-id="28d87-189">Url</span></span>
    - <span data-ttu-id="28d87-190">Описание</span><span class="sxs-lookup"><span data-stu-id="28d87-190">Description</span></span>
    - <span data-ttu-id="28d87-191">Fax</span><span class="sxs-lookup"><span data-stu-id="28d87-191">Fax</span></span>
    - <span data-ttu-id="28d87-192">Phone</span><span class="sxs-lookup"><span data-stu-id="28d87-192">Phone</span></span>
    - <span data-ttu-id="28d87-193">MobilePhone</span><span class="sxs-lookup"><span data-stu-id="28d87-193">MobilePhone</span></span>
    - <span data-ttu-id="28d87-194">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="28d87-194">Email</span></span>
    - <span data-ttu-id="28d87-195">Тип</span><span class="sxs-lookup"><span data-stu-id="28d87-195">Type</span></span>
    - <span data-ttu-id="28d87-196">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28d87-196">Title</span></span>
    - <span data-ttu-id="28d87-197">AccountId</span><span class="sxs-lookup"><span data-stu-id="28d87-197">AccountId</span></span>
    - <span data-ttu-id="28d87-198">Имя учетной записи</span><span class="sxs-lookup"><span data-stu-id="28d87-198">AccountName</span></span>
    - <span data-ttu-id="28d87-199">AccountUrl</span><span class="sxs-lookup"><span data-stu-id="28d87-199">AccountUrl</span></span>
    - <span data-ttu-id="28d87-200">AccountOwner</span><span class="sxs-lookup"><span data-stu-id="28d87-200">AccountOwner</span></span>
    - <span data-ttu-id="28d87-201">AccountOwnerUrl</span><span class="sxs-lookup"><span data-stu-id="28d87-201">AccountOwnerUrl</span></span>
    - <span data-ttu-id="28d87-202">Владелец</span><span class="sxs-lookup"><span data-stu-id="28d87-202">Owner</span></span>
    - <span data-ttu-id="28d87-203">OwnerUrl</span><span class="sxs-lookup"><span data-stu-id="28d87-203">OwnerUrl</span></span>
    - <span data-ttu-id="28d87-204">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="28d87-204">CreatedBy</span></span>
    - <span data-ttu-id="28d87-205">CreatedByUrl</span><span class="sxs-lookup"><span data-stu-id="28d87-205">CreatedByUrl</span></span>
    - <span data-ttu-id="28d87-206">LastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="28d87-206">LastModifiedBy</span></span>
    - <span data-ttu-id="28d87-207">LastModifiedByUrl</span><span class="sxs-lookup"><span data-stu-id="28d87-207">LastModifiedByUrl</span></span>
    - <span data-ttu-id="28d87-208">LastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="28d87-208">LastModifiedDate</span></span>
    - <span data-ttu-id="28d87-209">ObjectName</span><span class="sxs-lookup"><span data-stu-id="28d87-209">ObjectName</span></span>