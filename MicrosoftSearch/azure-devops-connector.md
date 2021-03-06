---
title: Соединителю Azure DevOps Graph для microsoft Search
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
description: Настройка соединителя Azure DevOps Graph для поиска в Microsoft Search
ms.openlocfilehash: 9307aabbf5ea1565e083abfefb90c590d356ae58
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508863"
---
<!---Previous ms.author: shgrover --->

# <a name="azure-devops-graph-connector-preview"></a><span data-ttu-id="bf3db-103">Соединителю Azure DevOps Graph (предварительный просмотр)</span><span class="sxs-lookup"><span data-stu-id="bf3db-103">Azure DevOps Graph connector (preview)</span></span>

<span data-ttu-id="bf3db-104">Соединителю Azure DevOps Graph позволяет организации индексировать элементы работы в экземпляре службы Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="bf3db-104">The Azure DevOps Graph connector allows your organization to index work items in its instance of the Azure DevOps service.</span></span> <span data-ttu-id="bf3db-105">После настройки соединителя и индекса контента из Azure DevOps конечные пользователи могут искать эти элементы в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="bf3db-105">After you configure the connector and index content from Azure DevOps, end users can search for those items in Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="bf3db-106">Ознакомьтесь [**с статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общие инструкции по настройке соединитений Graph.</span><span class="sxs-lookup"><span data-stu-id="bf3db-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="bf3db-107">Эта статья для всех, кто настраивает, запускает и отслеживает соединителю Azure DevOps Graph.</span><span class="sxs-lookup"><span data-stu-id="bf3db-107">This article is for anyone who configures, runs, and monitors an Azure DevOps Graph connector.</span></span> <span data-ttu-id="bf3db-108">Он дополняет общий процесс установки и показывает инструкции, применимые только к соединителю Azure DevOps Graph.</span><span class="sxs-lookup"><span data-stu-id="bf3db-108">It supplements the general setup process, and shows instructions that apply only for the Azure DevOps Graph connector.</span></span>

>[!IMPORTANT]
><span data-ttu-id="bf3db-109">Соединителю Azure DevOps поддерживается только облачная служба Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="bf3db-109">The Azure DevOps connector supports only the Azure DevOps cloud service.</span></span> <span data-ttu-id="bf3db-110">Этот соединитатель не поддерживает Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015 и TFS 2013.</span><span class="sxs-lookup"><span data-stu-id="bf3db-110">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015, and TFS 2013 are not supported by this connector.</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="bf3db-111">Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bf3db-111">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="bf3db-112">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="bf3db-112">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="bf3db-113">Шаг 2. Имя подключения</span><span class="sxs-lookup"><span data-stu-id="bf3db-113">Step 2: Name the connection</span></span>

<span data-ttu-id="bf3db-114">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="bf3db-114">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="bf3db-115">Шаг 3. Настройка параметров подключения</span><span class="sxs-lookup"><span data-stu-id="bf3db-115">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="bf3db-116">Чтобы подключиться к экземпляру Azure DevOps, [](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) необходимо имя организации Azure DevOps, его ID приложения и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="bf3db-116">To connect to your Azure DevOps instance, you need your Azure DevOps [organization](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) name, its App ID, and client secret for OAuth authentication.</span></span>

### <a name="register-an-app"></a><span data-ttu-id="bf3db-117">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="bf3db-117">Register an app</span></span>

<span data-ttu-id="bf3db-118">Зарегистрируйте приложение в Azure DevOps, чтобы приложение Microsoft Search можно было получить доступ к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="bf3db-118">Register an app in Azure DevOps so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="bf3db-119">Дополнительные новости см. в документации Azure DevOps о регистрации [приложения.](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="bf3db-119">To learn more, see Azure DevOps documentation on how to [register an app](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app&preserve-view=true).</span></span>

<span data-ttu-id="bf3db-120">В следующей таблице указаны инструкции по заполняемой форме регистрации приложений:</span><span class="sxs-lookup"><span data-stu-id="bf3db-120">The following table provides guidance on how to fill out the app registration form:</span></span>

<span data-ttu-id="bf3db-121">Обязательные поля</span><span class="sxs-lookup"><span data-stu-id="bf3db-121">Mandatory Fields</span></span> | <span data-ttu-id="bf3db-122">Описание</span><span class="sxs-lookup"><span data-stu-id="bf3db-122">Description</span></span> | <span data-ttu-id="bf3db-123">Рекомендуемое значение</span><span class="sxs-lookup"><span data-stu-id="bf3db-123">Recommended Value</span></span>
--- | --- | ---
| <span data-ttu-id="bf3db-124">Имя компании</span><span class="sxs-lookup"><span data-stu-id="bf3db-124">Company Name</span></span>         | <span data-ttu-id="bf3db-125">Имя вашей компании.</span><span class="sxs-lookup"><span data-stu-id="bf3db-125">The name of your company.</span></span> | <span data-ttu-id="bf3db-126">Использование соответствующего значения</span><span class="sxs-lookup"><span data-stu-id="bf3db-126">Use an appropriate value</span></span>   |
| <span data-ttu-id="bf3db-127">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="bf3db-127">Application name</span></span>     | <span data-ttu-id="bf3db-128">Уникальное значение, которое идентифицирует приложение, авторизуя его.</span><span class="sxs-lookup"><span data-stu-id="bf3db-128">A unique value that identifies the application that you're authorizing.</span></span>    | <span data-ttu-id="bf3db-129">Поиск (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="bf3db-129">Microsoft Search</span></span>     |
| <span data-ttu-id="bf3db-130">Веб-сайт приложения</span><span class="sxs-lookup"><span data-stu-id="bf3db-130">Application website</span></span>  | <span data-ttu-id="bf3db-131">URL-адрес приложения, который запрашивает доступ к экземпляру Azure DevOps во время установки соединителя.</span><span class="sxs-lookup"><span data-stu-id="bf3db-131">The URL of the application that will request access to your Azure DevOps instance during connector setup.</span></span> <span data-ttu-id="bf3db-132">(Обязательно).</span><span class="sxs-lookup"><span data-stu-id="bf3db-132">(Required).</span></span>  | <span data-ttu-id="bf3db-133"> https://<span>gcs.office.</span> com/</span><span class="sxs-lookup"><span data-stu-id="bf3db-133">https://<span>gcs.office.</span>com/</span></span>
| <span data-ttu-id="bf3db-134">URL-адрес вызова авторизации</span><span class="sxs-lookup"><span data-stu-id="bf3db-134">Authorization callback URL</span></span>        | <span data-ttu-id="bf3db-135">Необходимый URL-адрес вызова, на который перенаправляется сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="bf3db-135">A required callback URL that the authorization server redirects to.</span></span> | <span data-ttu-id="bf3db-136"> https://<span>gcs.office.</span> com/v1.0/admin/oauth/callback</span><span class="sxs-lookup"><span data-stu-id="bf3db-136">https://<span>gcs.office.</span>com/v1.0/admin/oauth/callback</span></span>|
| <span data-ttu-id="bf3db-137">Разрешенные области</span><span class="sxs-lookup"><span data-stu-id="bf3db-137">Authorized scopes</span></span> | <span data-ttu-id="bf3db-138">Область доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="bf3db-138">The scope of access for the application</span></span> | <span data-ttu-id="bf3db-139">Выберите следующие области: Identity (чтение), Work Items (чтение), Переменные группы (чтение), Project и Team (чтение), Graph (чтение)</span><span class="sxs-lookup"><span data-stu-id="bf3db-139">Select the following scopes: Identity (read), Work Items (read), Variable Groups (read), Project and team (read), Graph (read)</span></span>|

<span data-ttu-id="bf3db-140">При регистрации приложения с вышеуказанными сведениями вы получите  **ID** приложения и клиентскую тайну, которые будут использоваться для настройки соединитетеля.</span><span class="sxs-lookup"><span data-stu-id="bf3db-140">On registering the app with the details above, you'll get the **App ID** and **Client Secret** that will be used to configure the connector.</span></span>

>[!NOTE]
><span data-ttu-id="bf3db-141">Чтобы отопустить доступ к любому приложению, зарегистрированным в Azure DevOps, перейдите к настройкам пользователя в правой верхней части экземпляра Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="bf3db-141">To revoke access to any app registered in Azure DevOps, go to User settings at the right top of your Azure DevOps instance.</span></span> <span data-ttu-id="bf3db-142">Выберите профиль, а затем выберите авторизации в разделе Безопасность боковой области.</span><span class="sxs-lookup"><span data-stu-id="bf3db-142">Select Profile and then select Authorizations in the Security section of the side pane.</span></span> <span data-ttu-id="bf3db-143">Наведите курсор на авторизованном приложении OAuth, чтобы увидеть кнопку Revoke в углу сведений о приложении.</span><span class="sxs-lookup"><span data-stu-id="bf3db-143">Hover over an authorized OAuth app to see the Revoke button at the corner of the app details.</span></span>

### <a name="connection-settings"></a><span data-ttu-id="bf3db-144">Параметры подключения</span><span class="sxs-lookup"><span data-stu-id="bf3db-144">Connection settings</span></span>

<span data-ttu-id="bf3db-145">После регистрации приложения Microsoft Search в Azure DevOps можно выполнить шаг по настройке подключения.</span><span class="sxs-lookup"><span data-stu-id="bf3db-145">After registering the Microsoft Search app with Azure DevOps, you can complete the connection settings step.</span></span> <span data-ttu-id="bf3db-146">Введите имя организации, имя приложения и секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="bf3db-146">Enter your organization name, App ID, and Client secret.</span></span>

![Параметры приложения подключения](media/ADO_Connection_settings_2.png)

### <a name="configure-data-select-projects-and-fields"></a><span data-ttu-id="bf3db-148">Настройка данных: выбор проектов и полей</span><span class="sxs-lookup"><span data-stu-id="bf3db-148">Configure data: select projects and fields</span></span>

<span data-ttu-id="bf3db-149">Вы можете выбрать для подключения индексировать всю организацию или конкретные проекты.</span><span class="sxs-lookup"><span data-stu-id="bf3db-149">You can choose for the connection to index either the entire organization or specific projects.</span></span>

<span data-ttu-id="bf3db-150">Если вы решите индексировать всю организацию, элементы во всех проектах организации будут индексироваться.</span><span class="sxs-lookup"><span data-stu-id="bf3db-150">If you choose to index the entire organization, items in all projects in the organization will get indexed.</span></span> <span data-ttu-id="bf3db-151">Новые проекты и элементы будут индексироваться во время следующего обхода после их создания.</span><span class="sxs-lookup"><span data-stu-id="bf3db-151">New projects and items will be indexed during the next crawl after they're created.</span></span>

<span data-ttu-id="bf3db-152">Если вы выбираете отдельные проекты, индексировать будут только элементы работы в этих проектах.</span><span class="sxs-lookup"><span data-stu-id="bf3db-152">If you choose individual projects, only work items in those projects will be indexed.</span></span>

![Настройка данных](media/ADO_Configure_data.png)

<span data-ttu-id="bf3db-154">Далее выберите, в каких полях необходимо подключение для индексации и предварительного просмотра данных в этих полях перед началом.</span><span class="sxs-lookup"><span data-stu-id="bf3db-154">Next, select which fields you want the connection to index and preview data in these fields before proceeding.</span></span>

![Выбор свойств](media/ADO_choose_properties.png)

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="bf3db-156">Шаг 4. Управление разрешениями на поиск</span><span class="sxs-lookup"><span data-stu-id="bf3db-156">Step 4: Manage search permissions</span></span>

<span data-ttu-id="bf3db-157">Соединителю Azure DevOps поддерживаются разрешения на поиск, видимые только людям с доступом к этому источнику данных  **или** **каждому.**</span><span class="sxs-lookup"><span data-stu-id="bf3db-157">The Azure DevOps connector supports search permissions visible to  **Only people with access to this data source** or **Everyone**.</span></span> <span data-ttu-id="bf3db-158">Если выбрать только людей с доступом к этому источнику **данных,** индексируемые данные будут отображаться в результатах поиска для пользователей, которые имеют к ним доступ на основе разрешений для пользователей или групп на уровне пути организации, проекта или области в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="bf3db-158">If you choose **Only people with access to this data source**, indexed data will appear in the search results for users who have access to them based on permissions to users or groups at the Organization, Project or Area path level in Azure DevOps.</span></span> <span data-ttu-id="bf3db-159">Если вы **выбираете Everyone,** индексные данные будут отображаться в результатах поиска для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="bf3db-159">If you choose **Everyone**, indexed data will appear in the search results for all users.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="bf3db-160">Шаг 5. Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="bf3db-160">Step 5: Assign property labels</span></span>

<span data-ttu-id="bf3db-161">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="bf3db-161">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="bf3db-162">Шаг 6. Управление схемой</span><span class="sxs-lookup"><span data-stu-id="bf3db-162">Step 6: Manage schema</span></span>

<span data-ttu-id="bf3db-163">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="bf3db-163">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="bf3db-164">Шаг 7. Выбор параметров обновления</span><span class="sxs-lookup"><span data-stu-id="bf3db-164">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="bf3db-165">Соединителю Azure DevOps поддерживается расписание обновления для полного и постепенного обхода.</span><span class="sxs-lookup"><span data-stu-id="bf3db-165">The Azure DevOps connector supports refresh schedules for both full and incremental crawls.</span></span>
<span data-ttu-id="bf3db-166">Рекомендуемое расписание — один час для инкрементного обхода и один день для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="bf3db-166">The recommended schedule is one hour for an incremental crawl and one day for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="bf3db-167">Шаг 8. Просмотр подключения</span><span class="sxs-lookup"><span data-stu-id="bf3db-167">Step 8: Review connection</span></span>

<span data-ttu-id="bf3db-168">Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).</span><span class="sxs-lookup"><span data-stu-id="bf3db-168">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
