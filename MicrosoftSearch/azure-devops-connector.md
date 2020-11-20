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
ms.openlocfilehash: b9c566e3e07bfca6d4d25b14915f0160f3928b15
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367553"
---
# <a name="azure-devops-connector-preview"></a><span data-ttu-id="8f1fb-103">Соединитель Azure DevOps (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="8f1fb-103">Azure DevOps connector (preview)</span></span>

<span data-ttu-id="8f1fb-104">С помощью соединителя Azure DevOps организация может индексировать рабочие элементы в своем экземпляре службы DevOps Azure.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-104">With the Azure DevOps connector, your organization can index work items in its instance of the Azure DevOps service.</span></span> <span data-ttu-id="8f1fb-105">После настройки соединителя и индексирования содержимого из Azure DevOps пользователи могут выполнять поиск этих элементов в Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-105">After you configure the connector and index content from Azure DevOps, end users can search for those items in Microsoft Search.</span></span>

<span data-ttu-id="8f1fb-106">Эта статья предназначена для администраторов Microsoft 365 или пользователей, которые настраивают, запускают и осуществляют мониторинг соединителя Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors an Azure DevOps connector.</span></span> <span data-ttu-id="8f1fb-107">В этой статье объясняется, как настроить возможности соединителя и соединителя, ограничения и способы устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

>[!IMPORTANT]
><span data-ttu-id="8f1fb-108">Соединитель Azure DevOps поддерживает только облачную службу DevOps Azure.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-108">The Azure DevOps connector supports only the Azure DevOps cloud service.</span></span> <span data-ttu-id="8f1fb-109">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015 и TFS 2013 не поддерживаются этим соединителем.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-109">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015, and TFS 2013 are not supported by this connector.</span></span> 

## <a name="connect-to-a-data-source"></a><span data-ttu-id="8f1fb-110">Подключение к источнику данных</span><span class="sxs-lookup"><span data-stu-id="8f1fb-110">Connect to a data source</span></span>

<span data-ttu-id="8f1fb-111">Чтобы подключиться к экземпляру Azure DevOps, вам потребуется имя [Организации](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) Azure DEVOPS, идентификатор своего приложения и секрет клиента для проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-111">To connect to your Azure DevOps instance, you need your Azure DevOps [organization](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) name, its App ID, and client secret for OAuth authentication.</span></span>

### <a name="register-an-app"></a><span data-ttu-id="8f1fb-112">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="8f1fb-112">Register an app</span></span>

<span data-ttu-id="8f1fb-113">Необходимо зарегистрировать приложение в Azure DevOps, чтобы приложение Microsoft Search могло получить доступ к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-113">You must register an app in Azure DevOps so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="8f1fb-114">Чтобы узнать больше, ознакомьтесь с документацией по Azure DevOps о том, как [зарегистрировать приложение](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app).</span><span class="sxs-lookup"><span data-stu-id="8f1fb-114">To learn more, see Azure DevOps documentation on how to [register an app](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app).</span></span> 

<span data-ttu-id="8f1fb-115">В следующей таблице приведены указания по заполнению регистрационной формы приложения:</span><span class="sxs-lookup"><span data-stu-id="8f1fb-115">The following table provides guidance on how to fill out the app registration form:</span></span>

 <span data-ttu-id="8f1fb-116">**Обязательные поля**</span><span class="sxs-lookup"><span data-stu-id="8f1fb-116">**Mandatory Fields**</span></span> | <span data-ttu-id="8f1fb-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f1fb-117">**Description**</span></span>      | <span data-ttu-id="8f1fb-118">**Рекомендуемое значение**</span><span class="sxs-lookup"><span data-stu-id="8f1fb-118">**Recommended Value**</span></span> 
--- | --- | --- 
| <span data-ttu-id="8f1fb-119">Название организации</span><span class="sxs-lookup"><span data-stu-id="8f1fb-119">Company Name</span></span>         | <span data-ttu-id="8f1fb-120">Это название вашей компании.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-120">This is the name of your company.</span></span> | <span data-ttu-id="8f1fb-121">Использование подходящего значения</span><span class="sxs-lookup"><span data-stu-id="8f1fb-121">Use an appropriate value</span></span>   | 
| <span data-ttu-id="8f1fb-122">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="8f1fb-122">Application name</span></span>     | <span data-ttu-id="8f1fb-123">Это уникальное значение определяет приложение, для которого выполняется авторизация.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-123">This unique value identifies the application that you're authorizing.</span></span>    | <span data-ttu-id="8f1fb-124">Поиск (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8f1fb-124">Microsoft Search</span></span>     | 
| <span data-ttu-id="8f1fb-125">Веб-сайт приложения</span><span class="sxs-lookup"><span data-stu-id="8f1fb-125">Application website</span></span>  | <span data-ttu-id="8f1fb-126">Это обязательное поле — это URL-адрес приложения, которое будет запрашивать доступ к экземпляру Azure DevOps во время установки соединителя.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-126">This required field is the URL of the application that will request access to your Azure DevOps instance during connector setup.</span></span>  | <https://gcs.office.com/>                | 
| <span data-ttu-id="8f1fb-127">URL-адрес обратного вызова авторизации</span><span class="sxs-lookup"><span data-stu-id="8f1fb-127">Authorization callback URL</span></span>        | <span data-ttu-id="8f1fb-128">Обязательный URL-адрес обратного вызова, на который перенаправляется сервер проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-128">A required callback URL that the authorization server redirects to.</span></span> | <https://gcs.office.com/v1.0/admin/oauth/callback>| 
| <span data-ttu-id="8f1fb-129">Разрешенные области</span><span class="sxs-lookup"><span data-stu-id="8f1fb-129">Authorized scopes</span></span> | <span data-ttu-id="8f1fb-130">Это область доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="8f1fb-130">This is the scope of access for the application</span></span> | <span data-ttu-id="8f1fb-131">Выберите следующие области: удостоверение (чтение), рабочие элементы (чтение), группы переменных (чтение), проект и Рабочая группа (чтение), Graph (чтение)</span><span class="sxs-lookup"><span data-stu-id="8f1fb-131">Select the following scopes: Identity (read), Work Items (read), Variable Groups (read), Project and team (read), Graph (read)</span></span>| 

<span data-ttu-id="8f1fb-132">При регистрации приложения с помощью описанных выше сведений вы получите **идентификатор приложения** и **секрет клиента** , которые будут использоваться для настройки соединителя.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-132">On registering the app with the details above, you will get the **App ID** and **Client Secret** that will be used to configure the connector.</span></span>

>[!NOTE]
><span data-ttu-id="8f1fb-133">Чтобы отозвать доступ к любому приложению, зарегистрированному в Azure DevOps, перейдите к разделу Параметры пользователя в правой верхней части экземпляра Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-133">To revoke access to any app registered in Azure DevOps, go to User settings at the right top of your Azure DevOps instance.</span></span> <span data-ttu-id="8f1fb-134">Щелкните профиль, а затем щелкните элемент проверки подлинности в разделе Безопасность боковой панели.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-134">Click on Profile and then click on Authorizations in the Security section of the side pane.</span></span> <span data-ttu-id="8f1fb-135">Наведите указатель мыши на Авторизованное приложение OAuth, чтобы увидеть кнопку отозвать в углу сведений о приложении.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-135">Hover over an authorized OAuth app to see the Revoke button at the corner of the app details.</span></span>

### <a name="connection-settings"></a><span data-ttu-id="8f1fb-136">Параметры подключения</span><span class="sxs-lookup"><span data-stu-id="8f1fb-136">Connection settings</span></span>

<span data-ttu-id="8f1fb-137">После регистрации приложения Microsoft Search в Azure DevOps вы можете выполнить шаг параметров подключения.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-137">After registering the Microsoft Search app with Azure DevOps, you can complete the connection settings step.</span></span> <span data-ttu-id="8f1fb-138">Введите название организации, идентификатор приложения и секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-138">Enter your organization name, App ID, and Client secret.</span></span>

![Параметры приложения подключения](media/ADO_Connection_settings_2.png)

## <a name="select-projects-and-fields"></a><span data-ttu-id="8f1fb-140">Выбор проектов и полей</span><span class="sxs-lookup"><span data-stu-id="8f1fb-140">Select projects and fields</span></span>

<span data-ttu-id="8f1fb-141">Вы можете выбрать подключение для индексирования всей организации или конкретных проектов.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-141">You can choose for the connection to index either the entire organization or specific projects.</span></span>

<span data-ttu-id="8f1fb-142">Если вы решили индексировать всю организацию, элементы для всех проектов в организации будут индексироваться.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-142">If you choose to index the entire organization, items in all projects in the organization will get indexed.</span></span> <span data-ttu-id="8f1fb-143">Новые проекты и элементы будут индексироваться во время следующего обхода контента после их создания.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-143">New projects and items will be indexed during the next crawl after they are created.</span></span> <span data-ttu-id="8f1fb-144">При выборе отдельных проектов будут индексироваться только рабочие элементы в этих проектах.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-144">If you choose individual projects, only work items in those projects will be indexed.</span></span>

![Настройка данных](media/ADO_Configure_data.png)

<span data-ttu-id="8f1fb-146">Затем выберите поля, которые будут индексироваться и предварительно просматривать данные в этих полях перед тем, как продолжить.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-146">Next, select which fields you want the connection to index and preview data in these fields before proceeding.</span></span>

![Выбор свойств](media/ADO_choose_properties.png)

## <a name="manage-search-permissions"></a><span data-ttu-id="8f1fb-148">Управление разрешениями поиска</span><span class="sxs-lookup"><span data-stu-id="8f1fb-148">Manage search permissions</span></span>

<span data-ttu-id="8f1fb-149">Соединитель Azure DevOps поддерживает разрешения поиска, видимые  **только пользователям, у которых есть доступ к этому источнику данных** или **всем**.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-149">The Azure DevOps connector supports search permissions visible to  **Only people with access to this data source** or **Everyone**.</span></span> <span data-ttu-id="8f1fb-150">Если вы выбрали **только тех пользователей, у которых есть доступ к этому источнику данных**, индексированные данные будут отображаться в результатах поиска для пользователей, имеющих доступ к ним на основе разрешений для пользователей или групп на уровне Организации, проекта или области в каталоге Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-150">If you choose **Only people with access to this data source**,indexed data will appear in the search results for users who have access to them based on permissions to users or groups at the Organization, Project or Area path level in Azure DevOps.</span></span> <span data-ttu-id="8f1fb-151">Если выбран параметр **все**, индексированные данные будут отображаться в результатах поиска для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-151">If you choose **Everyone**, indexed data will appear in the search results for all users.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="8f1fb-152">Назначение меток свойств</span><span class="sxs-lookup"><span data-stu-id="8f1fb-152">Assign property labels</span></span>

<span data-ttu-id="8f1fb-153">Можно назначить свойство источника каждой метке, выбрав в меню пункт Параметры.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-153">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="8f1fb-154">Хотя это действие не является обязательным, наличие некоторых меток свойств повысит релевантность поиска и обеспечит более точные результаты поиска для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-154">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="8f1fb-155">Управление схемой</span><span class="sxs-lookup"><span data-stu-id="8f1fb-155">Manage schema</span></span>

<span data-ttu-id="8f1fb-156">На экране **Управление схемой** можно изменить атрибуты схемы (возможность **запроса**, возможность **поиска**, **Извлечение** и **уточнение**), связанные со свойствами, добавить необязательные псевдонимы и выбрать свойство **содержимого** .</span><span class="sxs-lookup"><span data-stu-id="8f1fb-156">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="8f1fb-157">Настройка расписания обновления</span><span class="sxs-lookup"><span data-stu-id="8f1fb-157">Set the refresh schedule</span></span>

<span data-ttu-id="8f1fb-158">Соединитель Azure DevOps поддерживает расписания обновления для полных и добавочных обходов контента.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-158">The Azure DevOps connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="8f1fb-159">Полный обход контента находит удаленные рабочие элементы, которые ранее были синхронизированы с индексом поиска Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-159">A full crawl finds deleted work items that were previously synced to the Microsoft Search index.</span></span> <span data-ttu-id="8f1fb-160">Полный обход контента выполняется для синхронизации всех рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-160">A full crawl runs to sync all the work items.</span></span> <span data-ttu-id="8f1fb-161">Чтобы синхронизировать новые рабочие элементы и обновления с существующими рабочими элементами, необходимо запланировать добавочные обходы контента.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-161">To sync new work items and updates to existing work items, you need to schedule incremental crawls.</span></span>

<span data-ttu-id="8f1fb-162">Рекомендуемое расписание составляет один час для добавочного обхода и один день для полного обхода.</span><span class="sxs-lookup"><span data-stu-id="8f1fb-162">The recommended schedule is one hour for an incremental crawl and one day for a full crawl.</span></span> 