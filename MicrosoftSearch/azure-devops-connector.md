---
title: Azure DevOps Graph соединители для microsoft Search
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
description: Настройка соединитетеля Azure DevOps Graph microsoft Search
ms.openlocfilehash: bfe04a022360a968424b673ad03ba05f27c8c333
ms.sourcegitcommit: 1b154441f3a3abba0f2719e66a767432bc9506ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2021
ms.locfileid: "52720955"
---
<!---Previous ms.author: shgrover --->

# <a name="azure-devops-graph-connector-preview"></a><span data-ttu-id="60a70-103">Azure DevOps Graph (предварительный просмотр)</span><span class="sxs-lookup"><span data-stu-id="60a70-103">Azure DevOps Graph connector (preview)</span></span>

<span data-ttu-id="60a70-104">Соедините Azure DevOps Graph позволяет организации индексировать элементы работы в экземпляре Azure DevOps службы.</span><span class="sxs-lookup"><span data-stu-id="60a70-104">The Azure DevOps Graph connector allows your organization to index work items in its instance of the Azure DevOps service.</span></span> <span data-ttu-id="60a70-105">После настройки соединители и индексации контента из Azure DevOps конечные пользователи могут искать эти элементы в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="60a70-105">After you configure the connector and index content from Azure DevOps, end users can search for those items in Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="60a70-106">Ознакомьтесь [**с статьей Установка Graph,**](configure-connector.md) чтобы понять общие инструкции Graph соединители.</span><span class="sxs-lookup"><span data-stu-id="60a70-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="60a70-107">Эта статья для всех, кто настраивает, запускает и отслеживает Azure DevOps Graph соединители.</span><span class="sxs-lookup"><span data-stu-id="60a70-107">This article is for anyone who configures, runs, and monitors an Azure DevOps Graph connector.</span></span> <span data-ttu-id="60a70-108">Он дополняет общий процесс установки и показывает инструкции, которые применяются только для Azure DevOps Graph соединители.</span><span class="sxs-lookup"><span data-stu-id="60a70-108">It supplements the general setup process, and shows instructions that apply only for the Azure DevOps Graph connector.</span></span>

>[!IMPORTANT]
><span data-ttu-id="60a70-109">Соедините Azure DevOps поддерживает только облачную службу Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="60a70-109">The Azure DevOps connector supports only the Azure DevOps cloud service.</span></span> <span data-ttu-id="60a70-110">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015 и TFS 2013 не поддерживаются этим соединитетелем.</span><span class="sxs-lookup"><span data-stu-id="60a70-110">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015, and TFS 2013 are not supported by this connector.</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="60a70-111">Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="60a70-111">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="60a70-112">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="60a70-112">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="60a70-113">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="60a70-113">Step 2: Name the connection</span></span>

<span data-ttu-id="60a70-114">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="60a70-114">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="60a70-115">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="60a70-115">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="60a70-116">Чтобы подключиться к Azure DevOps экземпляру, необходимо Azure DevOps [](/azure/devops/organizations/accounts/create-organization) имя организации, его ID приложения и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="60a70-116">To connect to your Azure DevOps instance, you need your Azure DevOps [organization](/azure/devops/organizations/accounts/create-organization) name, its App ID, and client secret for OAuth authentication.</span></span>

### <a name="register-an-app"></a><span data-ttu-id="60a70-117">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="60a70-117">Register an app</span></span>

<span data-ttu-id="60a70-118">Зарегистрируйте приложение в Azure DevOps, чтобы приложение Microsoft Search можно было получить доступ к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="60a70-118">Register an app in Azure DevOps so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="60a70-119">Дополнительные дополнительные Azure DevOps документации о регистрации [приложения.](/azure/devops/integrate/get-started/authentication/oauth?preserve-view=true&view=azure-devops#register-your-app)</span><span class="sxs-lookup"><span data-stu-id="60a70-119">To learn more, see Azure DevOps documentation on how to [register an app](/azure/devops/integrate/get-started/authentication/oauth?preserve-view=true&view=azure-devops#register-your-app).</span></span>

<span data-ttu-id="60a70-120">В следующей таблице указаны инструкции по заполняемой форме регистрации приложений:</span><span class="sxs-lookup"><span data-stu-id="60a70-120">The following table provides guidance on how to fill out the app registration form:</span></span>

<span data-ttu-id="60a70-121">Обязательные поля</span><span class="sxs-lookup"><span data-stu-id="60a70-121">Mandatory Fields</span></span> | <span data-ttu-id="60a70-122">Описание</span><span class="sxs-lookup"><span data-stu-id="60a70-122">Description</span></span> | <span data-ttu-id="60a70-123">Рекомендуемое значение</span><span class="sxs-lookup"><span data-stu-id="60a70-123">Recommended Value</span></span>
--- | --- | ---
| <span data-ttu-id="60a70-124">Имя компании</span><span class="sxs-lookup"><span data-stu-id="60a70-124">Company Name</span></span>         | <span data-ttu-id="60a70-125">Имя вашей компании.</span><span class="sxs-lookup"><span data-stu-id="60a70-125">The name of your company.</span></span> | <span data-ttu-id="60a70-126">Использование соответствующего значения</span><span class="sxs-lookup"><span data-stu-id="60a70-126">Use an appropriate value</span></span>   |
| <span data-ttu-id="60a70-127">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="60a70-127">Application name</span></span>     | <span data-ttu-id="60a70-128">Уникальное значение, которое идентифицирует приложение, авторизуя его.</span><span class="sxs-lookup"><span data-stu-id="60a70-128">A unique value that identifies the application that you're authorizing.</span></span>    | <span data-ttu-id="60a70-129">Поиск (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="60a70-129">Microsoft Search</span></span>     |
| <span data-ttu-id="60a70-130">Веб-сайт приложения</span><span class="sxs-lookup"><span data-stu-id="60a70-130">Application website</span></span>  | <span data-ttu-id="60a70-131">URL-адрес приложения, который запрашивает доступ к экземпляру Azure DevOps во время установки соединителя.</span><span class="sxs-lookup"><span data-stu-id="60a70-131">The URL of the application that will request access to your Azure DevOps instance during connector setup.</span></span> <span data-ttu-id="60a70-132">(Обязательно).</span><span class="sxs-lookup"><span data-stu-id="60a70-132">(Required).</span></span>  | <span data-ttu-id="60a70-133"> https://<span>gcs.office.</span> com/</span><span class="sxs-lookup"><span data-stu-id="60a70-133">https://<span>gcs.office.</span>com/</span></span>
| <span data-ttu-id="60a70-134">URL-адрес вызова авторизации</span><span class="sxs-lookup"><span data-stu-id="60a70-134">Authorization callback URL</span></span>        | <span data-ttu-id="60a70-135">Необходимый URL-адрес вызова, на который перенаправляется сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="60a70-135">A required callback URL that the authorization server redirects to.</span></span> | <span data-ttu-id="60a70-136"> https://<span>gcs.office.</span> com/v1.0/admin/oauth/callback</span><span class="sxs-lookup"><span data-stu-id="60a70-136">https://<span>gcs.office.</span>com/v1.0/admin/oauth/callback</span></span>|
| <span data-ttu-id="60a70-137">Разрешенные области</span><span class="sxs-lookup"><span data-stu-id="60a70-137">Authorized scopes</span></span> | <span data-ttu-id="60a70-138">Область доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="60a70-138">The scope of access for the application</span></span> | <span data-ttu-id="60a70-139">Выберите следующие области: Identity (чтение), Work Items (read), Variable Groups (чтение), Project и team (чтение), Graph (чтение)</span><span class="sxs-lookup"><span data-stu-id="60a70-139">Select the following scopes: Identity (read), Work Items (read), Variable Groups (read), Project and team (read), Graph (read)</span></span>|

>[!IMPORTANT]
><span data-ttu-id="60a70-140">Разрешенные области, выбранные для приложения, должны соответствовать тем областьм, которые указаны выше.</span><span class="sxs-lookup"><span data-stu-id="60a70-140">The authorized scopes that you select for the app should match the scopes exactly as listed above.</span></span> <span data-ttu-id="60a70-141">Если вы опустить одну из разрешенных областей в списке или добавить другую область, авторизация не будет работать.</span><span class="sxs-lookup"><span data-stu-id="60a70-141">If you omit one of the authorized scopes in the list, or add another scope, the authorization will fail.</span></span>

<span data-ttu-id="60a70-142">При регистрации приложения с вышеуказанными сведениями вы получите  **ID** приложения и клиентскую тайну, которые будут использоваться для настройки соединитетеля.</span><span class="sxs-lookup"><span data-stu-id="60a70-142">On registering the app with the details above, you'll get the **App ID** and **Client Secret** that will be used to configure the connector.</span></span>

>[!NOTE]
><span data-ttu-id="60a70-143">Чтобы отопустить доступ к любому приложению, Azure DevOps в Azure DevOps, перейдите к настройкам пользователя в правой верхней части Azure DevOps экземпляра.</span><span class="sxs-lookup"><span data-stu-id="60a70-143">To revoke access to any app registered in Azure DevOps, go to User settings at the right top of your Azure DevOps instance.</span></span> <span data-ttu-id="60a70-144">Выберите профиль, а затем выберите авторизации в разделе Безопасность боковой области.</span><span class="sxs-lookup"><span data-stu-id="60a70-144">Select Profile and then select Authorizations in the Security section of the side pane.</span></span> <span data-ttu-id="60a70-145">Наведите курсор на авторизованном приложении OAuth, чтобы увидеть кнопку Revoke в углу сведений о приложении.</span><span class="sxs-lookup"><span data-stu-id="60a70-145">Hover over an authorized OAuth app to see the Revoke button at the corner of the app details.</span></span>

### <a name="connection-settings"></a><span data-ttu-id="60a70-146">Параметры подключения</span><span class="sxs-lookup"><span data-stu-id="60a70-146">Connection settings</span></span>

<span data-ttu-id="60a70-147">После регистрации приложения Microsoft Search с Azure DevOps вы можете завершить шаг параметров подключения.</span><span class="sxs-lookup"><span data-stu-id="60a70-147">After registering the Microsoft Search app with Azure DevOps, you can complete the connection settings step.</span></span> <span data-ttu-id="60a70-148">Введите имя организации, имя приложения и секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="60a70-148">Enter your organization name, App ID, and Client secret.</span></span>

![Приложение подключения Параметры](media/ADO_Connection_settings_2.png)

### <a name="configure-data-select-projects-and-fields"></a><span data-ttu-id="60a70-150">Настройка данных: выбор проектов и полей</span><span class="sxs-lookup"><span data-stu-id="60a70-150">Configure data: select projects and fields</span></span>

<span data-ttu-id="60a70-151">Вы можете выбрать для подключения индексировать всю организацию или конкретные проекты.</span><span class="sxs-lookup"><span data-stu-id="60a70-151">You can choose for the connection to index either the entire organization or specific projects.</span></span>

<span data-ttu-id="60a70-152">Если вы решите индексировать всю организацию, элементы во всех проектах организации будут индексироваться.</span><span class="sxs-lookup"><span data-stu-id="60a70-152">If you choose to index the entire organization, items in all projects in the organization will get indexed.</span></span> <span data-ttu-id="60a70-153">Новые проекты и элементы будут индексироваться во время следующего обхода после их создания.</span><span class="sxs-lookup"><span data-stu-id="60a70-153">New projects and items will be indexed during the next crawl after they're created.</span></span>

<span data-ttu-id="60a70-154">Если вы выбираете отдельные проекты, индексировать будут только элементы работы в этих проектах.</span><span class="sxs-lookup"><span data-stu-id="60a70-154">If you choose individual projects, only work items in those projects will be indexed.</span></span>

![Настройка данных](media/ADO_Configure_data.png)

<span data-ttu-id="60a70-156">Далее выберите, в каких полях необходимо подключение для индексации и предварительного просмотра данных в этих полях перед началом.</span><span class="sxs-lookup"><span data-stu-id="60a70-156">Next, select which fields you want the connection to index and preview data in these fields before proceeding.</span></span>

![Выбор свойств](media/ADO_choose_properties.png)

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="60a70-158">Шаг 4. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="60a70-158">Step 4: Manage search permissions</span></span>

<span data-ttu-id="60a70-159">Соедините Azure DevOps поддерживает разрешения на поиск, видимые только людям с доступом к этому источнику данных  **или** **каждому.**</span><span class="sxs-lookup"><span data-stu-id="60a70-159">The Azure DevOps connector supports search permissions visible to  **Only people with access to this data source** or **Everyone**.</span></span> <span data-ttu-id="60a70-160">Если вы выбираете только людей с доступом к этому источнику **данных,** индексные данные будут отображаться в результатах поиска для пользователей, которые имеют к ним доступ на основе разрешений для пользователей или групп на уровне организации, Project или области пути в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="60a70-160">If you choose **Only people with access to this data source**, indexed data will appear in the search results for users who have access to them based on permissions to users or groups at the Organization, Project or Area path level in Azure DevOps.</span></span> <span data-ttu-id="60a70-161">Если вы **выбираете Everyone,** индексные данные будут отображаться в результатах поиска для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="60a70-161">If you choose **Everyone**, indexed data will appear in the search results for all users.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="60a70-162">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="60a70-162">Step 5: Assign property labels</span></span>

<span data-ttu-id="60a70-163">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="60a70-163">Follow the general [setup instructions](./configure-connector.md).</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="60a70-164">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="60a70-164">Step 6: Manage schema</span></span>

<span data-ttu-id="60a70-165">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="60a70-165">Follow the general [setup instructions](./configure-connector.md).</span></span>

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="60a70-166">Шаг 7. Выбор параметров обновления</span><span class="sxs-lookup"><span data-stu-id="60a70-166">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="60a70-167">Соедините Azure DevOps поддерживает расписание обновления для полного и постепенного обхода.</span><span class="sxs-lookup"><span data-stu-id="60a70-167">The Azure DevOps connector supports refresh schedules for both full and incremental crawls.</span></span>
<span data-ttu-id="60a70-168">Рекомендуемое расписание — один час для инкрементного обхода и один день для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="60a70-168">The recommended schedule is one hour for an incremental crawl and one day for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="60a70-169">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="60a70-169">Step 8: Review connection</span></span>

<span data-ttu-id="60a70-170">Следуйте общим [инструкциям установки](./configure-connector.md).</span><span class="sxs-lookup"><span data-stu-id="60a70-170">Follow the general [setup instructions](./configure-connector.md).</span></span>

>[!TIP]
><span data-ttu-id="60a70-171">**Тип результата по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="60a70-171">**Default Result type**</span></span>
>* <span data-ttu-id="60a70-172">Соединит Azure DevOps автоматически регистрирует тип результатов [после](./customize-search-page.md#step-2-create-the-result-types) публикации соединителю.</span><span class="sxs-lookup"><span data-stu-id="60a70-172">The Azure DevOps connector automatically registers a [result type](./customize-search-page.md#step-2-create-the-result-types) once the connector is published.</span></span> <span data-ttu-id="60a70-173">Тип результатов использует динамически созданный [макет результатов](./customize-results-layout.md) на основе полей, выбранных в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="60a70-173">The result type uses a dynamically generated [result layout](./customize-results-layout.md) based on the fields selected in step 3.</span></span> 
>* <span data-ttu-id="60a70-174">Вы можете управлять типом результатов, переходя на типы [**результатов**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes) [в центре администрирования Microsoft 365.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="60a70-174">You can manage the result type by navigating to [**Result types**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="60a70-175">Тип результатов по умолчанию будет называться `ConnectionId` "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="60a70-175">The default result type will be named as "`ConnectionId`Default".</span></span> <span data-ttu-id="60a70-176">Например, если у вас есть id подключения, макет результатов будет `AzureDevOps` назван: "AzureDevOpsDefault"</span><span class="sxs-lookup"><span data-stu-id="60a70-176">For example, if your connection id is `AzureDevOps`, your result layout will be named: "AzureDevOpsDefault"</span></span>
>* <span data-ttu-id="60a70-177">Кроме того, при необходимости можно создать собственный тип результатов.</span><span class="sxs-lookup"><span data-stu-id="60a70-177">Also, you can choose to create your own result type if needed.</span></span>

<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->