---
title: Соединитель salesforce для службы поиска Майкрософт
ms.author: rusamai
author: rsamai
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединителя salesforce для поиска Майкрософт
ms.openlocfilehash: 149d1d9a297e09e9b895aeb0947c7ff4a3cbdf84
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367652"
---
# <a name="salesforce-connector-preview"></a><span data-ttu-id="6710d-103">Соединитель Salesforce (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="6710d-103">Salesforce connector (preview)</span></span>

<span data-ttu-id="6710d-104">С помощью соединителя диаграмм Salesforce организация может индексировать объекты Contacts, возможные сделки, интересы и Организации в экземпляре Salesforce.</span><span class="sxs-lookup"><span data-stu-id="6710d-104">With the Salesforce Graph connector, your organization can index Contacts, Opportunities, Leads and Accounts objects in your Salesforce instance.</span></span> <span data-ttu-id="6710d-105">После настройки соединителя и индексирования содержимого из Salesforce пользователи могут выполнять поиск этих элементов в любом клиенте Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="6710d-105">After you configure the connector and index content from Salesforce, end users can search for those items from any Microsoft Search client.</span></span>

<span data-ttu-id="6710d-106">Эта статья предназначена для администраторов [Microsoft 365](https://www.microsoft.com/microsoft-365) или пользователей, которые настраивают, запускают и отслеживают соединитель Salesforce.</span><span class="sxs-lookup"><span data-stu-id="6710d-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors a Salesforce connector.</span></span> <span data-ttu-id="6710d-107">В этой статье объясняется, как настроить возможности соединителя и соединителя, ограничения и способы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="6710d-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

>[!IMPORTANT]
><span data-ttu-id="6710d-108">В настоящее время соединитель графа Salesforce поддерживает 19 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="6710d-108">The Salesforce Graph connector currently supports Summer '19 or later.</span></span>

## <a name="connection-settings"></a><span data-ttu-id="6710d-109">Параметры подключения</span><span class="sxs-lookup"><span data-stu-id="6710d-109">Connection settings</span></span>

<span data-ttu-id="6710d-110">Чтобы подключиться к экземпляру Salesforce, вам потребуются URL-адрес экземпляра Salesforce, идентификатор клиента и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="6710d-110">To connect to your Salesforce instance, you need your Salesforce instance URL, the Client ID, and Client Secret for OAuth authentication.</span></span> <span data-ttu-id="6710d-111">В следующих шагах описывается, как вы или ваш администратор Salesforce может получить эту информацию из вашей учетной записи Salesforce:</span><span class="sxs-lookup"><span data-stu-id="6710d-111">The following steps explain how you or your Salesforce administrator can get this information from your Salesforce account:</span></span>

- <span data-ttu-id="6710d-112">Выполните вход в экземпляр Salesforce и перейдите к разделу "Настройка".</span><span class="sxs-lookup"><span data-stu-id="6710d-112">Log in to your Salesforce instance and go to Setup</span></span>

- <span data-ttu-id="6710d-113">Перейдите в раздел Appss — > App Manager.</span><span class="sxs-lookup"><span data-stu-id="6710d-113">Navigate to Apps -> App Manager.</span></span>

- <span data-ttu-id="6710d-114">Выберите **новое подключенное приложение**.</span><span class="sxs-lookup"><span data-stu-id="6710d-114">Select **New connected app**.</span></span>

- <span data-ttu-id="6710d-115">Заполните раздел API следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6710d-115">Complete the API section as follows:</span></span>

    - <span data-ttu-id="6710d-116">Установите флажок **включить параметры OAuth**.</span><span class="sxs-lookup"><span data-stu-id="6710d-116">Select the checkbox for **Enable Oauth Settings**.</span></span>

    - <span data-ttu-id="6710d-117">Укажите URL-адрес обратного вызова как: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span><span class="sxs-lookup"><span data-stu-id="6710d-117">Specify the Callback URL as: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span></span>

    - <span data-ttu-id="6710d-118">Выберите необходимые области OAuth.</span><span class="sxs-lookup"><span data-stu-id="6710d-118">Select these required OAuth scopes.</span></span> 

        - <span data-ttu-id="6710d-119">Доступ к данным и управление ими (API)</span><span class="sxs-lookup"><span data-stu-id="6710d-119">Access and manage your data (api)</span></span> 

        - <span data-ttu-id="6710d-120">Выполнение запросов от вашего имени в любое время (refresh_token, offline_access)</span><span class="sxs-lookup"><span data-stu-id="6710d-120">Perform requests on your behalf at any time (refresh_token, offline_access)</span></span> 

    - <span data-ttu-id="6710d-121">Установите флажок **требовать секрет для веб-сервера**.</span><span class="sxs-lookup"><span data-stu-id="6710d-121">Select the checkbox for **Require secret for web server flow**.</span></span>

    - <span data-ttu-id="6710d-122">Сохраните приложение.</span><span class="sxs-lookup"><span data-stu-id="6710d-122">Save the app.</span></span>
    
      ![В разделе API в экземпляре Salesforce после того, как администратор ввел все необходимые конфигурации, перечисленные выше.](media/salesforce-connector/sf1.png)

- <span data-ttu-id="6710d-124">Скопируйте ключ потребителя и секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="6710d-124">Copy the consumer key and the consumer secret.</span></span> <span data-ttu-id="6710d-125">Они будут использоваться в качестве идентификатора клиента и секрета клиента при настройке параметров подключения для графического соединителя на портале администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6710d-125">These will be used as the Client ID and the Client Secret when you configure the Connection Settings for your Graph Connector in the Microsoft 365 admin portal.</span></span>

  ![Результаты, возвращаемые по разделу API в экземпляре Salesforce, после того как администратор отправил все необходимые конфигурации.](media/salesforce-connector/clientsecret.png)
- <span data-ttu-id="6710d-128">Перед закрытием экземпляра Salesforce выполните следующие действия, чтобы убедиться, что срок действия маркеров обновления не истек:</span><span class="sxs-lookup"><span data-stu-id="6710d-128">Before closing your Salesforce instance, perform the following steps to ensure that refresh tokens do not expire:</span></span>
    - <span data-ttu-id="6710d-129">Переход в раздел Appss — > App Manager</span><span class="sxs-lookup"><span data-stu-id="6710d-129">Go to Apps -> App Manager</span></span>
    - <span data-ttu-id="6710d-130">Найдите только что созданное приложение и выберите раскрывающийся список справа.</span><span class="sxs-lookup"><span data-stu-id="6710d-130">Find the app you just created and select the drop down on the right.</span></span> <span data-ttu-id="6710d-131">Выберите **Управление**</span><span class="sxs-lookup"><span data-stu-id="6710d-131">Select **Manage**</span></span>
    - <span data-ttu-id="6710d-132">Выбор параметра " **изменить политики** "</span><span class="sxs-lookup"><span data-stu-id="6710d-132">Select **edit policies**</span></span>
    - <span data-ttu-id="6710d-133">Для политики маркеров обновления выберите **маркер обновления действителен до отзыва**</span><span class="sxs-lookup"><span data-stu-id="6710d-133">For refresh token policy, select **Refresh token is valid until revoked**</span></span>

  ![Выберите политику маркеров обновления с именем "маркер обновления действителен до отзыва"](media/salesforce-connector/oauthpolicies.png)

<span data-ttu-id="6710d-135">Теперь вы можете использовать [центр администрирования M365](https://admin.microsoft.com/) для завершения оставшейся части процесса установки для графического соединителя.</span><span class="sxs-lookup"><span data-stu-id="6710d-135">You can now use the [M365 Admin Center](https://admin.microsoft.com/) to complete the rest of the setup process for your Graph connector.</span></span>  

<span data-ttu-id="6710d-136">Настройте параметры подключения для соединителя Graph следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6710d-136">Configure the Connection settings for your Graph connector as follows:</span></span>

- <span data-ttu-id="6710d-137">В качестве URL-адреса экземпляра используйте HTTPS://[домен]. My. Salesforce. com, где Domain — это домен salesforce для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6710d-137">For the Instance URL, use https://[domain].my.salesforce.com where domain would be the Salesforce domain for your organization.</span></span> 
- <span data-ttu-id="6710d-138">Введите идентификатор клиента и секрет клиента, полученные из экземпляра Salesforce, и нажмите кнопку войти.</span><span class="sxs-lookup"><span data-stu-id="6710d-138">Enter the Client ID and Client Secret you obtained from your Salesforce instance and select Sign in.</span></span>
- <span data-ttu-id="6710d-139">Если вы впервые попытались войти с помощью этих параметров, вы получите всплывающее окно с запросом на вход в SalesForce с помощью имени пользователя и пароля администратора.</span><span class="sxs-lookup"><span data-stu-id="6710d-139">If this is the first time you have attempted to Sign in with these settings, you will get a pop up asking you to login to Salesforce with your admin username and password.</span></span> <span data-ttu-id="6710d-140">На снимке экрана ниже показано всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="6710d-140">The screenshot below shows the popup.</span></span> <span data-ttu-id="6710d-141">Введите свои учетные данные и нажмите кнопку войти.</span><span class="sxs-lookup"><span data-stu-id="6710d-141">Enter your credentials and select Log in.</span></span>

  ![При входе в систему появляется запрос имени пользователя и пароля.](media/salesforce-connector/sf4.png)

  >[!NOTE]
  ><span data-ttu-id="6710d-143">Если всплывающее окно не отображается, оно может быть заблокировано в браузере, поэтому необходимо разрешить всплывающие окна и перенаправление.</span><span class="sxs-lookup"><span data-stu-id="6710d-143">If the pop up does not appear, it might be getting blocked in your browser, so you must allow pop-ups and redirects.</span></span>

  >[!NOTE]
  ><span data-ttu-id="6710d-144">Если в вашей организации используется единый вход (SSO), в нижнем правом углу интерфейса входа можно выбрать **использовать личный домен** .</span><span class="sxs-lookup"><span data-stu-id="6710d-144">If your organization uses single sign-on (SSO), you can select **Use Custom Domain** in the bottom, right-hand corner of the login interface.</span></span> <span data-ttu-id="6710d-145">Введите домен и нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="6710d-145">Enter the domain and then select **Continue**.</span></span> <span data-ttu-id="6710d-146">Она будет переходить на страницу входа, относящуюся к конкретной организации, где у вас будет возможность входа с помощью единого входа.</span><span class="sxs-lookup"><span data-stu-id="6710d-146">It will go to your organization specific login page where you will have an option to login with SSO.</span></span>

- <span data-ttu-id="6710d-147">Убедитесь, что подключение было успешным, выполнив поиск зеленого баннера с текстом "подключение успешно", как показано на снимке экрана ниже.</span><span class="sxs-lookup"><span data-stu-id="6710d-147">Check that the connection was successful by searching for a green banner that says "Connection successful" as show in the screenshot below.</span></span>

  ![Снимок экрана с успешным входом.](media/salesforce-connector/sf5.png)

## <a name="manage-search-permissions"></a><span data-ttu-id="6710d-150">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="6710d-150">Manage search permissions</span></span>
<span data-ttu-id="6710d-151">Вам потребуется выбрать, какие пользователи будут видеть результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="6710d-151">You will need to choose which users will see search results from this data source.</span></span> <span data-ttu-id="6710d-152">Если вы разрешаете просматривать результаты поиска только определенным пользователям Azure Active Directory (Azure AD) или пользователям, не являющимся пользователями Azure AD, вам потребуется сопоставить удостоверения.</span><span class="sxs-lookup"><span data-stu-id="6710d-152">If you allow only certain Azure Active Directory (Azure AD) or Non-Azure AD users to see the search results, you will then need to map the identities.</span></span>

### <a name="select-permissions"></a><span data-ttu-id="6710d-153">Выбор разрешений</span><span class="sxs-lookup"><span data-stu-id="6710d-153">Select Permissions</span></span>
<span data-ttu-id="6710d-154">Вы можете использовать списки управления доступом (ACL) из экземпляра Salesforce или разрешить всем пользователям в организации просматривать результаты поиска из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="6710d-154">You can choose to ingest Access Control Lists (ACLs) from your Salesforce instance, or you can allow everyone in your organization to see search results from this data source.</span></span> <span data-ttu-id="6710d-155">Списки управления доступом могут включать удостоверения Azure Active Directory (AAD) (пользователи, Федеративные из Azure AD в Salesforce), идентификаторы, не относящиеся к Azure AD (собственные пользователи Salesforce, имеющие соответствующие удостоверения в Azure AD), или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="6710d-155">ACLs can include Azure Active Directory (AAD) identities (users who are federated from Azure AD to Salesforce), non-Azure AD identities (native Salesforce users who have corresponding identities in Azure AD), or both.</span></span>

![Экран "Выбор разрешений", выполненный администратором. Администратор выбрал параметр "только пользователи с доступом к этому источнику данных", а также выбрал "AAD" из раскрывающегося меню типов удостоверений.](media/salesforce-connector/sf6.png)

### <a name="map-non-aad-identities"></a><span data-ttu-id="6710d-157">Сопоставление удостоверений, не являющихся AAD</span><span class="sxs-lookup"><span data-stu-id="6710d-157">Map non-AAD identities</span></span> 
<span data-ttu-id="6710d-158">Если вы решили присвоить список управления доступом из экземпляра Salesforce и выбрать "не AAD" для типа удостоверения, ознакомьтесь с инструкциями по сопоставлению удостоверений в статье [Map of Azure AD](map-non-aad.md) identitys.</span><span class="sxs-lookup"><span data-stu-id="6710d-158">If you chose to ingest an ACL from your Salesforce instance and selected "non-AAD" for the identity type see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span>

### <a name="map-aad-identities"></a><span data-ttu-id="6710d-159">Сопоставление удостоверений AAD</span><span class="sxs-lookup"><span data-stu-id="6710d-159">Map AAD identities</span></span>
<span data-ttu-id="6710d-160">Если вы решили присвоить список управления доступом из экземпляра Salesforce и выбрать "AAD" для типа удостоверения, ознакомьтесь со статьей Сопоставление удостоверений [Azure AD](map-aad.md) для получения инструкций по сопоставлению удостоверений.</span><span class="sxs-lookup"><span data-stu-id="6710d-160">If you chose to ingest an ACL from your Salesforce instance and selected "AAD" for the identity type see [Map your Azure AD Identities](map-aad.md) for instructions on mapping the identities.</span></span> <span data-ttu-id="6710d-161">Сведения о том, как настроить единый вход Azure AD для Salesforce, можно найти в этом [руководстве](https://docs.microsoft.com/en-us/azure/active-directory/saas-apps/salesforce-tutorial).</span><span class="sxs-lookup"><span data-stu-id="6710d-161">To learn how to set up Azure AD SSO for Salesforce, see this [tutorial](https://docs.microsoft.com/en-us/azure/active-directory/saas-apps/salesforce-tutorial).</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="6710d-162">Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="6710d-162">Assign property labels</span></span> 
<span data-ttu-id="6710d-163">Можно назначить свойство источника каждой метке, выбрав в меню пункт Параметры.</span><span class="sxs-lookup"><span data-stu-id="6710d-163">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="6710d-164">Хотя это действие не является обязательным, наличие некоторых меток свойств повысит релевантность поиска и обеспечит более точные результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="6710d-164">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span> <span data-ttu-id="6710d-165">По умолчанию для некоторых меток, таких как "Title", "URL", "CreatedBy" и "Ластмодифиедби", уже были назначены исходные свойства.</span><span class="sxs-lookup"><span data-stu-id="6710d-165">By default, some of the Labels like "Title," "URL," "CreatedBy," and  "LastModifiedBy" have already been assigned source properties.</span></span>

![Окно назначения меток свойств, в котором показаны свойства источника по умолчанию.](media/salesforce-connector/sf8.png)

## <a name="manage-schema"></a><span data-ttu-id="6710d-167">Управление схемой</span><span class="sxs-lookup"><span data-stu-id="6710d-167">Manage Schema</span></span>
<span data-ttu-id="6710d-168">Вы можете выбрать, какие исходные свойства следует индексировать, чтобы они могли отображаться в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="6710d-168">You can select what source properties should be indexed so that they can show up in search results.</span></span> <span data-ttu-id="6710d-169">По умолчанию в мастере подключения выбирается схема поиска на основе набора свойств источника.</span><span class="sxs-lookup"><span data-stu-id="6710d-169">The connection wizard by default selects a search schema based on a set of source properties.</span></span> <span data-ttu-id="6710d-170">Его можно изменить, установив флажки для каждого свойства и атрибута на странице схема поиска.</span><span class="sxs-lookup"><span data-stu-id="6710d-170">You can modify it by selecting the check boxes for each property and attribute in the search schema page.</span></span> <span data-ttu-id="6710d-171">Атрибуты схемы поиска включают поиск, запрос, получение и уточнение.</span><span class="sxs-lookup"><span data-stu-id="6710d-171">Search schema attributes include Search, Query, Retrieve and Refine.</span></span> <span data-ttu-id="6710d-172">Уточнение позволяет определить свойства, которые позднее можно использовать в качестве настраиваемых уточнений или фильтров в интерфейсе поиска.</span><span class="sxs-lookup"><span data-stu-id="6710d-172">Refine allows you to define the properties which can be later used as custom refiners or filters in the search experience.</span></span>  

![Выберите схему для каждого свойства источника.](media/salesforce-connector/sf9.png)

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="6710d-175">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="6710d-175">Set the refresh schedule</span></span>

<span data-ttu-id="6710d-176">Соединитель Salesforce поддерживает только расписания обновления для полного обхода в текущий момент.</span><span class="sxs-lookup"><span data-stu-id="6710d-176">The Salesforce connector only supports refresh schedules for full crawls currently.</span></span>

>[!IMPORTANT]
><span data-ttu-id="6710d-177">Полный обход контента выполняет поиск удаленных объектов и пользователей, которые ранее были синхронизированы с индексом поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6710d-177">A full crawl finds deleted objects and users that were previously synced to the Microsoft Search index.</span></span>

<span data-ttu-id="6710d-178">Для полного обхода рекомендуется использовать расписание на одну неделю.</span><span class="sxs-lookup"><span data-stu-id="6710d-178">The recommended schedule is one week for a full crawl.</span></span>

## <a name="limitations"></a><span data-ttu-id="6710d-179">Ограничения</span><span class="sxs-lookup"><span data-stu-id="6710d-179">Limitations</span></span>

- <span data-ttu-id="6710d-180">Соединитель Graph в настоящее время не поддерживает общий доступ к Апекс, основанный на территориях, и общий доступ с использованием личных групп Salesforce.</span><span class="sxs-lookup"><span data-stu-id="6710d-180">The Graph connector does not currently support Apex based , territory-based sharing and sharing using personal groups from Salesforce.</span></span>
- <span data-ttu-id="6710d-181">В API Salesforce обнаружена известная ошибка, в которой соединитель Graph использует, где в настоящее время не поддерживаются частные географические параметры по умолчанию для интересов.</span><span class="sxs-lookup"><span data-stu-id="6710d-181">There is a known bug in the Salesforce API that the Graph connector uses where the private org wide defaults for leads is not honored currently.</span></span>  
- <span data-ttu-id="6710d-182">Если для профиля задана защита на уровне полей (ФЛС), соединитель Graph не будет использовать это поле для всех профилей в этой Организации Salesforce. Таким образом, пользователи не смогут выполнять поиск по значениям для этих полей, и они не будут отображаться в результатах.</span><span class="sxs-lookup"><span data-stu-id="6710d-182">If a field has field level security (FLS) set for a profile, the Graph connector will not ingest that field for any profiles in that Salesforce org. Users will thus not be able to search on values for those fields, nor will it  show up in the results.</span></span>  
- <span data-ttu-id="6710d-183">В окне Управление схемой эти стандартные имена стандартных свойств указаны один раз, и выбранные элементы, позволяющие сделать их запросами, доступны для поиска и извлечения, применяются ко всем или нет.</span><span class="sxs-lookup"><span data-stu-id="6710d-183">In the Manage Schema screen these common standard property names are listed once and the selection done to make them queryable, searchable and retrievable apply to all or none.</span></span>
    - <span data-ttu-id="6710d-184">Имя</span><span class="sxs-lookup"><span data-stu-id="6710d-184">Name</span></span>
    - <span data-ttu-id="6710d-185">Url</span><span class="sxs-lookup"><span data-stu-id="6710d-185">Url</span></span> 
    - <span data-ttu-id="6710d-186">Описание</span><span class="sxs-lookup"><span data-stu-id="6710d-186">Description</span></span>
    - <span data-ttu-id="6710d-187">Fax</span><span class="sxs-lookup"><span data-stu-id="6710d-187">Fax</span></span>
    - <span data-ttu-id="6710d-188">Phone</span><span class="sxs-lookup"><span data-stu-id="6710d-188">Phone</span></span>
    - <span data-ttu-id="6710d-189">MobilePhone</span><span class="sxs-lookup"><span data-stu-id="6710d-189">MobilePhone</span></span>
    - <span data-ttu-id="6710d-190">Электронный адрес</span><span class="sxs-lookup"><span data-stu-id="6710d-190">Email</span></span>
    - <span data-ttu-id="6710d-191">Тип</span><span class="sxs-lookup"><span data-stu-id="6710d-191">Type</span></span>
    - <span data-ttu-id="6710d-192">Название</span><span class="sxs-lookup"><span data-stu-id="6710d-192">Title</span></span>
    - <span data-ttu-id="6710d-193">AccountId</span><span class="sxs-lookup"><span data-stu-id="6710d-193">AccountId</span></span>
    - <span data-ttu-id="6710d-194">Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6710d-194">AccountName</span></span>
    - <span data-ttu-id="6710d-195">аккаунтурл</span><span class="sxs-lookup"><span data-stu-id="6710d-195">AccountUrl</span></span>
    - <span data-ttu-id="6710d-196">аккаунтовнер</span><span class="sxs-lookup"><span data-stu-id="6710d-196">AccountOwner</span></span>
    - <span data-ttu-id="6710d-197">аккаунтовнерурл</span><span class="sxs-lookup"><span data-stu-id="6710d-197">AccountOwnerUrl</span></span>
    - <span data-ttu-id="6710d-198">Владелец</span><span class="sxs-lookup"><span data-stu-id="6710d-198">Owner</span></span>
    - <span data-ttu-id="6710d-199">овнерурл</span><span class="sxs-lookup"><span data-stu-id="6710d-199">OwnerUrl</span></span>
    - <span data-ttu-id="6710d-200">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="6710d-200">CreatedBy</span></span> 
    - <span data-ttu-id="6710d-201">креатедбюрл</span><span class="sxs-lookup"><span data-stu-id="6710d-201">CreatedByUrl</span></span> 
    - <span data-ttu-id="6710d-202">LastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="6710d-202">LastModifiedBy</span></span> 
    - <span data-ttu-id="6710d-203">ластмодифиедбюрл</span><span class="sxs-lookup"><span data-stu-id="6710d-203">LastModifiedByUrl</span></span> 
    - <span data-ttu-id="6710d-204">LastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="6710d-204">LastModifiedDate</span></span>
    - <span data-ttu-id="6710d-205">ObjectName</span><span class="sxs-lookup"><span data-stu-id="6710d-205">ObjectName</span></span> 
