---
title: Соединитель Azure DevOps для поиска Майкрософт
ms.author: shgrover
author: shakungrover05
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединителя Azure DevOps Connector для поиска Майкрософт
ms.openlocfilehash: a0028c3b336c2b5e3d01bb14006ee0debb4524f2
ms.sourcegitcommit: 59435698bece013ae64ca2a68c43455ca10e3fdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "48927192"
---
# <a name="azure-devops-connector"></a><span data-ttu-id="79e00-103">Соединитель Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="79e00-103">Azure DevOps connector</span></span>

<span data-ttu-id="79e00-104">С помощью соединителя Azure DevOps организация может индексировать рабочие элементы в своем экземпляре службы DevOps Azure.</span><span class="sxs-lookup"><span data-stu-id="79e00-104">With the Azure DevOps connector, your organization can index work items in its instance of the Azure DevOps service.</span></span> <span data-ttu-id="79e00-105">После настройки соединителя и индексирования содержимого из Azure DevOps пользователи могут выполнять поиск этих элементов в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="79e00-105">After you configure the connector and index content from Azure DevOps, end users can search for those items in Microsoft Search.</span></span>

<span data-ttu-id="79e00-106">Эта статья предназначена для администраторов Microsoft 365 или пользователей, которые настраивают, запускают и осуществляют мониторинг соединителя Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="79e00-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors an Azure DevOps connector.</span></span> <span data-ttu-id="79e00-107">В этой статье объясняется, как настроить возможности соединителя и соединителя, ограничения и способы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="79e00-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

>[!IMPORTANT]
><span data-ttu-id="79e00-108">Соединитель Azure DevOps поддерживает только облачную службу DevOps Azure.</span><span class="sxs-lookup"><span data-stu-id="79e00-108">The Azure DevOps connector supports only the Azure DevOps cloud service.</span></span> <span data-ttu-id="79e00-109">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015 и TFS 2013 не поддерживаются этим соединителем.</span><span class="sxs-lookup"><span data-stu-id="79e00-109">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015, and TFS 2013 are not supported by this connector.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="79e00-110">Подключение к источнику данных</span><span class="sxs-lookup"><span data-stu-id="79e00-110">Connect to a data source</span></span>

<span data-ttu-id="79e00-111">Чтобы подключиться к экземпляру Azure DevOps, вам потребуется имя [Организации](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) Azure DEVOPS, идентификатор своего приложения и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="79e00-111">To connect to your Azure DevOps instance, you need your Azure DevOps [organization](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) name, its App ID, and client secret for OAuth authentication.</span></span>

### <a name="register-an-app"></a><span data-ttu-id="79e00-112">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="79e00-112">Register an app</span></span>

<span data-ttu-id="79e00-113">Необходимо зарегистрировать приложение в Azure DevOps, чтобы приложение Microsoft Search могло получить доступ к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="79e00-113">You must register an app in Azure DevOps so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="79e00-114">Чтобы узнать больше, ознакомьтесь с документацией по Azure DevOps о том, как [зарегистрировать приложение](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app).</span><span class="sxs-lookup"><span data-stu-id="79e00-114">To learn more, see Azure DevOps documentation on how to [register an app](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app).</span></span>

<span data-ttu-id="79e00-115">В следующей таблице приведены указания по заполнению регистрационной формы приложения:</span><span class="sxs-lookup"><span data-stu-id="79e00-115">The following table provides guidance on how to fill out the app registration form:</span></span>

 <span data-ttu-id="79e00-116">**Обязательные поля**</span><span class="sxs-lookup"><span data-stu-id="79e00-116">**Mandatory Fields**</span></span> | <span data-ttu-id="79e00-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="79e00-117">**Description**</span></span>      | <span data-ttu-id="79e00-118">**Рекомендуемое значение**</span><span class="sxs-lookup"><span data-stu-id="79e00-118">**Recommended Value**</span></span>
--- | --- | ---
| <span data-ttu-id="79e00-119">Название организации</span><span class="sxs-lookup"><span data-stu-id="79e00-119">Company Name</span></span>         | <span data-ttu-id="79e00-120">Это название вашей компании.</span><span class="sxs-lookup"><span data-stu-id="79e00-120">This is the name of your company.</span></span> | <span data-ttu-id="79e00-121">Использование подходящего значения</span><span class="sxs-lookup"><span data-stu-id="79e00-121">Use an appropriate value</span></span>   |
| <span data-ttu-id="79e00-122">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="79e00-122">Application name</span></span>     | <span data-ttu-id="79e00-123">Это уникальное значение определяет приложение, для которого выполняется авторизация.</span><span class="sxs-lookup"><span data-stu-id="79e00-123">This unique value identifies the application that you're authorizing.</span></span>    | <span data-ttu-id="79e00-124">Поиск (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="79e00-124">Microsoft Search</span></span>     |
| <span data-ttu-id="79e00-125">Веб-сайт приложения</span><span class="sxs-lookup"><span data-stu-id="79e00-125">Application website</span></span>  | <span data-ttu-id="79e00-126">Это обязательное поле — это URL-адрес приложения, которое будет запрашивать доступ к экземпляру Azure DevOps во время установки соединителя.</span><span class="sxs-lookup"><span data-stu-id="79e00-126">This required field is the URL of the application that will request access to your Azure DevOps instance during connector setup.</span></span>  | <https://gcs.office.com/>                |
| <span data-ttu-id="79e00-127">URL-адрес обратного вызова авторизации</span><span class="sxs-lookup"><span data-stu-id="79e00-127">Authorization callback URL</span></span>        | <span data-ttu-id="79e00-128">Обязательный URL-адрес обратного вызова, на который перенаправляется сервер проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="79e00-128">A required callback URL that the authorization server redirects to.</span></span> | <https://gcs.office.com/v1.0/admin/oauth/callback>|
| <span data-ttu-id="79e00-129">Разрешенные области</span><span class="sxs-lookup"><span data-stu-id="79e00-129">Authorized scopes</span></span> | <span data-ttu-id="79e00-130">Это область доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="79e00-130">This is the scope of access for the application</span></span> | <span data-ttu-id="79e00-131">Выберите следующие области: удостоверение (чтение), рабочие элементы (чтение), группы переменных (чтение), проект и Рабочая группа (чтение), Graph (чтение)</span><span class="sxs-lookup"><span data-stu-id="79e00-131">Select the following scopes: Identity (read), Work Items (read), Variable Groups (read), Project and team (read), Graph (read)</span></span>|

<span data-ttu-id="79e00-132">При регистрации приложения с помощью описанных выше сведений вы получите **идентификатор приложения** и **секрет клиента** , которые будут использоваться для настройки соединителя.</span><span class="sxs-lookup"><span data-stu-id="79e00-132">On registering the app with the details above, you will get the **App ID** and **Client Secret** that will be used to configure the connector.</span></span>

>[!NOTE]
><span data-ttu-id="79e00-133">Чтобы отозвать доступ к любому приложению, зарегистрированному в Azure DevOps, перейдите к разделу Параметры пользователя в правой верхней части экземпляра Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="79e00-133">To revoke access to any app registered in Azure DevOps, go to User settings at the right top of your Azure DevOps instance.</span></span> <span data-ttu-id="79e00-134">Щелкните профиль, а затем щелкните элемент проверки подлинности в разделе Безопасность боковой панели.</span><span class="sxs-lookup"><span data-stu-id="79e00-134">Click on Profile and then click on Authorizations in the Security section of the side pane.</span></span> <span data-ttu-id="79e00-135">Наведите указатель мыши на Авторизованное приложение OAuth, чтобы увидеть кнопку отозвать в углу сведений о приложении.</span><span class="sxs-lookup"><span data-stu-id="79e00-135">Hover over an authorized OAuth app to see the Revoke button at the corner of the app details.</span></span>

### <a name="connection-settings"></a><span data-ttu-id="79e00-136">Параметры подключения</span><span class="sxs-lookup"><span data-stu-id="79e00-136">Connection settings</span></span>

<span data-ttu-id="79e00-137">После регистрации приложения Microsoft Search в Azure DevOps вы можете выполнить шаг параметров подключения.</span><span class="sxs-lookup"><span data-stu-id="79e00-137">After registering the Microsoft Search app with Azure DevOps, you can complete the connection settings step.</span></span> <span data-ttu-id="79e00-138">Введите название организации, идентификатор приложения и секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="79e00-138">Enter your organization name, App ID, and Client secret.</span></span>

![Параметры приложения подключения](media/ADO_Connection_settings_2.png)

## <a name="select-projects-and-fields"></a><span data-ttu-id="79e00-140">Выбор проектов и полей</span><span class="sxs-lookup"><span data-stu-id="79e00-140">Select projects and fields</span></span>

<span data-ttu-id="79e00-141">Вы можете выбрать подключение для индексирования всей организации или конкретных проектов.</span><span class="sxs-lookup"><span data-stu-id="79e00-141">You can choose for the connection to index either the entire organization or specific projects.</span></span>

<span data-ttu-id="79e00-142">Если вы решили индексировать всю организацию, элементы для всех проектов в организации будут индексироваться.</span><span class="sxs-lookup"><span data-stu-id="79e00-142">If you choose to index the entire organization, items in all projects in the organization will get indexed.</span></span> <span data-ttu-id="79e00-143">Новые проекты и элементы будут индексироваться во время следующего обхода контента после их создания.</span><span class="sxs-lookup"><span data-stu-id="79e00-143">New projects and items will be indexed during the next crawl after they are created.</span></span> <span data-ttu-id="79e00-144">При выборе отдельных проектов будут индексироваться только рабочие элементы в этих проектах.</span><span class="sxs-lookup"><span data-stu-id="79e00-144">If you choose individual projects, only work items in those projects will be indexed.</span></span>

![Настройка данных](media/ADO_Configure_data.png)

<span data-ttu-id="79e00-146">Затем выберите поля, которые будут индексироваться и предварительно просматривать данные в этих полях перед тем, как продолжить.</span><span class="sxs-lookup"><span data-stu-id="79e00-146">Next, select which fields you want the connection to index and preview data in these fields before proceeding.</span></span>

![Выбор свойств](media/ADO_choose_properties.png)

## <a name="manage-search-permissions"></a><span data-ttu-id="79e00-148">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="79e00-148">Manage search permissions</span></span>

<span data-ttu-id="79e00-149">В настоящее время соединитель Azure DevOps поддерживает только разрешения **на поиск, видимые всем пользователям**.</span><span class="sxs-lookup"><span data-stu-id="79e00-149">The Azure DevOps connector currently only supports search permissions **Visible to Everyone**.</span></span> <span data-ttu-id="79e00-150">Индексированные данные будут отображаться в результатах поиска для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="79e00-150">Indexed data will appear in the search results for all users.</span></span>

## <a name="manage-search-schema"></a><span data-ttu-id="79e00-151">Управление схемой поиска</span><span class="sxs-lookup"><span data-stu-id="79e00-151">Manage search schema</span></span>

<span data-ttu-id="79e00-152">Настройте сопоставление схемы поиска.</span><span class="sxs-lookup"><span data-stu-id="79e00-152">Configure the search schema mapping.</span></span> <span data-ttu-id="79e00-153">Вы можете выбрать свойства, которые будут доступны для **запроса** , **поиска** и **извлечения**.</span><span class="sxs-lookup"><span data-stu-id="79e00-153">You can choose which properties to make **queryable** , **searchable** and **retrievable**.</span></span>


## <a name="set-refresh-schedule"></a><span data-ttu-id="79e00-154">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="79e00-154">Set refresh schedule</span></span>

<span data-ttu-id="79e00-155">Соединитель Azure DevOps поддерживает расписания обновления для полных и добавочных обходов контента.</span><span class="sxs-lookup"><span data-stu-id="79e00-155">The Azure DevOps connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="79e00-156">Полный обход контента находит удаленные рабочие элементы, которые ранее были синхронизированы с индексом поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="79e00-156">A full crawl finds deleted work items that were previously synced to the Microsoft Search index.</span></span> <span data-ttu-id="79e00-157">Полный обход контента выполняется для синхронизации всех рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="79e00-157">A full crawl runs to sync all the work items.</span></span> <span data-ttu-id="79e00-158">Чтобы синхронизировать новые рабочие элементы и обновления с существующими рабочими элементами, необходимо запланировать добавочные обходы контента.</span><span class="sxs-lookup"><span data-stu-id="79e00-158">To sync new work items and updates to existing work items, you need to schedule incremental crawls.</span></span>

<span data-ttu-id="79e00-159">Рекомендуемое расписание составляет один час для добавочного обхода и один день для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="79e00-159">The recommended schedule is one hour for an incremental crawl and one day for a full crawl.</span></span>
