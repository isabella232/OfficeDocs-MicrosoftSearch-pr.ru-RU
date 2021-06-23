---
title: Динамический поиск федерации 365 (предварительный просмотр)
ms.author: dawholl
author: dawholl
manager: kellis
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
description: Управление тем, как контент Dynamics 365 отображается в результатах поиска
ms.openlocfilehash: 5f642bcb026358e57258e5e736fc263616fc4b05
ms.sourcegitcommit: f07a2e578b6c9ed5a1a3b22266cca371782870a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "53067935"
---
# <a name="dynamics-365-federation-search-preview"></a><span data-ttu-id="82c7d-103">Динамический поиск федерации 365 (предварительный просмотр)</span><span class="sxs-lookup"><span data-stu-id="82c7d-103">Dynamics 365 federation search (preview)</span></span>

## <a name="microsoft-search-federation-and-connectors"></a><span data-ttu-id="82c7d-104">Поиск (Майкрософт) Федерации и соединители</span><span class="sxs-lookup"><span data-stu-id="82c7d-104">Microsoft Search Federation and connectors</span></span>

<span data-ttu-id="82c7d-105">Чтобы сделать Поиск (Майкрософт) более полезными, мы представляем Поиск (Майкрософт) Федерации.</span><span class="sxs-lookup"><span data-stu-id="82c7d-105">To help make Microsoft Search more useful, we're introducing Microsoft Search Federation.</span></span> <span data-ttu-id="82c7d-106">С помощью федератного поиска организации могут сделать данные в этих сценариях доступными в Поиск (Майкрософт):</span><span class="sxs-lookup"><span data-stu-id="82c7d-106">With federated search, organizations can make data in these scenarios accessible in Microsoft Search:</span></span>

* <span data-ttu-id="82c7d-107">Данные в системах, которые подчиняются строгим требованиям соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="82c7d-107">Data in systems that are subject to strict compliance requirements</span></span>
* <span data-ttu-id="82c7d-108">Данные, которые не могут оставить границы системы</span><span class="sxs-lookup"><span data-stu-id="82c7d-108">Data that can't leave system boundaries</span></span>
* <span data-ttu-id="82c7d-109">Конфиденциальные данные, хранимые на преме, которые организация не хочет индексировать в облаке</span><span class="sxs-lookup"><span data-stu-id="82c7d-109">Sensitive data stored on-prem that your organization doesn’t want indexed on the cloud</span></span>

<span data-ttu-id="82c7d-110">Данные, полученные с помощью федератного поискового подключения, не индексированы в Поиск (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="82c7d-110">Data accessed through a federated search connection isn't indexed in Microsoft Search.</span></span> <span data-ttu-id="82c7d-111">Кроме того, с помощью встроенных соединителеров от Microsoft легко настроить федераированные подключения к поискам.</span><span class="sxs-lookup"><span data-stu-id="82c7d-111">Also, using built-in connectors from Microsoft, it's easy to set up federated search connections.</span></span> <span data-ttu-id="82c7d-112">Наш соединитатель Dynamics 365 в настоящее время находится в предварительном режиме.</span><span class="sxs-lookup"><span data-stu-id="82c7d-112">Our Dynamics 365 connector is currently in preview.</span></span> <span data-ttu-id="82c7d-113">Если вы заинтересованы в присоединении к предварительному просмотру, дайте нам знать в [aka.ms/D365FederationSearchPreview](https://aka.ms/D365FederationSearchPreview).</span><span class="sxs-lookup"><span data-stu-id="82c7d-113">If you're interested in joining the preview, let us know at [aka.ms/D365FederationSearchPreview](https://aka.ms/D365FederationSearchPreview).</span></span>

## <a name="dynamics-365-federation-connector"></a><span data-ttu-id="82c7d-114">Соединители федерации Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="82c7d-114">Dynamics 365 federation connector</span></span>

<span data-ttu-id="82c7d-115">Microsoft Dynamics 365 — это линейка интеллектуальных бизнес-приложений, предназначенных для планирования ресурсов предприятия и управления отношениями с клиентами.</span><span class="sxs-lookup"><span data-stu-id="82c7d-115">Microsoft Dynamics 365 is a line of intelligent business applications designed for enterprise resource planning and customer relationship management.</span></span> <span data-ttu-id="82c7d-116">С помощью федерации Dynamics 365 Поиск (Майкрософт) обеспечивает бесшовный поиск, что позволяет пользователям легко находить наиболее релевантные клиенты и бизнес-данные, хранимые в Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82c7d-116">With Dynamics 365 federation, Microsoft Search provides a seamless search experience, enabling users to easily find the most relevant customer and business data stored in Dynamics 365.</span></span> <span data-ttu-id="82c7d-117">Соединители федерации Dynamics 365 предоставляют некоторые ключевые преимущества:</span><span class="sxs-lookup"><span data-stu-id="82c7d-117">The Dynamics 365 federation connector provides some key benefits:</span></span>

* <span data-ttu-id="82c7d-118">**Простое администрирование:** Упрощенный процесс настройки и обслуживания подключения поиска к экземпляру Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82c7d-118">**Easy to administer:** Streamlined process to configure and maintain the search connection to a Dynamics 365 instance.</span></span>
* <span data-ttu-id="82c7d-119">**Простой в использовании:** Пользователи могут легко и быстро найти ключевые сведения, хранимые в Dynamics 365, включая учетные записи, контакты, открытые возможности и другие.</span><span class="sxs-lookup"><span data-stu-id="82c7d-119">**Easy to use:** Users can easily and quickly find key information stored in Dynamics 365, including accounts, contacts, open opportunities, and more.</span></span>
* <span data-ttu-id="82c7d-120">**Более богатый контент:** Чтобы сделать результаты поиска Dynamics 365 более полезными, они включают ключевые сведения, такие как руководства, контакты и сведения о учетной записи.</span><span class="sxs-lookup"><span data-stu-id="82c7d-120">**Richer content:** To make Dynamics 365 search results more useful, they include key information like leads, contacts, and account details.</span></span>
* <span data-ttu-id="82c7d-121">**Встроенная защита данных:** Результаты Dynamics 365 будут отображаться только для пользователей, которые имеют доступ к подключенным экземплярам.</span><span class="sxs-lookup"><span data-stu-id="82c7d-121">**Built-in data protection:** Dynamics 365 results will only appear for users that have access to the connected instance.</span></span>
* <span data-ttu-id="82c7d-122">**Унифицированный поиск:** Для сохранения согласованности результаты Dynamics 365 согласованы во всех точках входа в поиск.</span><span class="sxs-lookup"><span data-stu-id="82c7d-122">**Unified search experience:** To maintain a cohesive experience, Dynamics 365 results are consistent across all search entry points.</span></span> <span data-ttu-id="82c7d-123">Где бы вы ни искали, вы получите одинаковые результаты с одинаковым внешний вид.</span><span class="sxs-lookup"><span data-stu-id="82c7d-123">Wherever you search, you'll get the same results with the same look and feel.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="82c7d-124">Что пользователи испытывают</span><span class="sxs-lookup"><span data-stu-id="82c7d-124">What users experience</span></span>

<span data-ttu-id="82c7d-125">Ответы Dynamics 365 отображаются в результатах поиска во всех Поиск (Майкрософт) холстах, включая SharePoint Online, Bing и Office.</span><span class="sxs-lookup"><span data-stu-id="82c7d-125">Dynamics 365 answers appear in search results across all Microsoft Search canvases, including SharePoint Online, Bing, and Office.</span></span>

:::image type="content" alt-text="Снимок экрана ответов Dynamics 365 на SharePoint, Bing и Office" source="media/dynamics365/dynamics365-answer.png" lightbox="media/dynamics365/dynamics365-answer.png":::

<span data-ttu-id="82c7d-127">В ответе легко увидеть больше результатов поиска Dynamics 365 с помощью ссылки **More Dynamics 365.**</span><span class="sxs-lookup"><span data-stu-id="82c7d-127">From the answer, it's easy to see more Dynamics 365 search results by using the **More Dynamics 365 results** link.</span></span> <span data-ttu-id="82c7d-128">Он принимает пользователей на выделенную страницу результатов Dynamics 365 с дополнительными результатами, соответствующими их запросу.</span><span class="sxs-lookup"><span data-stu-id="82c7d-128">It takes users to a dedicated Dynamics 365 results page with more results relevant to their query.</span></span>

:::image type="content" alt-text="Снимок экрана вертикальной динамики 365 и результаты SharePoint, Bing и Office" source="media/dynamics365/dynamics365-vertical.png" lightbox="media/dynamics365/dynamics365-vertical.png":::

<span data-ttu-id="82c7d-130">Щелкнув или нажав любой результат, откроет Dynamics 365 и покажет подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="82c7d-130">Clicking or tapping any result opens Dynamics 365 and shows the detailed information.</span></span>

:::image type="content" alt-text="Снимок экрана страницы подробно в Dynamics 365" source="media/dynamics365/dynamics365-detail-page.png" lightbox="media/dynamics365/dynamics365-detail-page.png":::

<span data-ttu-id="82c7d-132">Независимо от того, где пользователи начинают поиск, их опыт будет последовательным и позволит им быстро найти наиболее релевантные результаты Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82c7d-132">No matter where your users start their search their experience will be consistent and enable them to quickly find the most relevant Dynamics 365 results.</span></span> <span data-ttu-id="82c7d-133">Ознакомьтесь с видеороликом Microsoft Build 2021 для демонстрации.</span><span class="sxs-lookup"><span data-stu-id="82c7d-133">Check out our Microsoft Build 2021 video for a demonstration.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4P83t]

## <a name="supported-query-patterns"></a><span data-ttu-id="82c7d-134">Поддерживаемые шаблоны запросов</span><span class="sxs-lookup"><span data-stu-id="82c7d-134">Supported query patterns</span></span>

<span data-ttu-id="82c7d-135">Запросы на естественный язык и имя продукта поддерживаются при использовании Поиск (Майкрософт) для поиска результатов Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82c7d-135">Both natural language and product name queries are supported when using Microsoft Search to find Dynamics 365 results.</span></span> <span data-ttu-id="82c7d-136">Кроме того, запросы Dynamics 365 не являются конфиденциальными.</span><span class="sxs-lookup"><span data-stu-id="82c7d-136">Also, Dynamics 365 queries aren't case sensitive.</span></span> <span data-ttu-id="82c7d-137">Используйте естественные языковые шаблоны для поиска контактов, учетных записей и возможностей по имени клиента или расположению и другим часто используемым запросам.</span><span class="sxs-lookup"><span data-stu-id="82c7d-137">Use natural language patterns to find contact, account, and opportunities--by customer name or location--and other frequently used queries.</span></span> <span data-ttu-id="82c7d-138">Вот несколько примеров:</span><span class="sxs-lookup"><span data-stu-id="82c7d-138">Here are a few examples:</span></span>

* <span data-ttu-id="82c7d-139">Кто является контактом для Contoso</span><span class="sxs-lookup"><span data-stu-id="82c7d-139">Who is the contact for Contoso</span></span>
* <span data-ttu-id="82c7d-140">Открытые возможности для Contoso</span><span class="sxs-lookup"><span data-stu-id="82c7d-140">Open opportunities for Contoso</span></span>
* <span data-ttu-id="82c7d-141">Что такое открытые возможности в Сиэтле</span><span class="sxs-lookup"><span data-stu-id="82c7d-141">What are open opportunities in Seattle</span></span>
* <span data-ttu-id="82c7d-142">Какие учетные записи в Сиэтле</span><span class="sxs-lookup"><span data-stu-id="82c7d-142">What are the accounts in Seattle</span></span>
* <span data-ttu-id="82c7d-143">Контакты в Сиэтле</span><span class="sxs-lookup"><span data-stu-id="82c7d-143">What are the contacts in Seattle</span></span>
* <span data-ttu-id="82c7d-144">Каковы мои руководства закрытия в этом месяце</span><span class="sxs-lookup"><span data-stu-id="82c7d-144">What are my leads closing this month</span></span>
* <span data-ttu-id="82c7d-145">Телефонный звонок с высоким приоритетом</span><span class="sxs-lookup"><span data-stu-id="82c7d-145">High priority phone call</span></span>
* <span data-ttu-id="82c7d-146">Контактные отсутствующие сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="82c7d-146">Contact missing emails</span></span>

<span data-ttu-id="82c7d-147">Шаблоны имен продуктов поддерживают диапазон приложений Dynamics 365 и вызывают результаты Dynamics 365 независимо от того, где они отображаются в запросе:</span><span class="sxs-lookup"><span data-stu-id="82c7d-147">Product name patterns support a range of Dynamics 365 applications and will trigger Dynamics 365 results regardless of where they appear in a query:</span></span>

* <span data-ttu-id="82c7d-148">D365</span><span class="sxs-lookup"><span data-stu-id="82c7d-148">D365</span></span>
* <span data-ttu-id="82c7d-149">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="82c7d-149">Dynamics 365</span></span>
* <span data-ttu-id="82c7d-150">Dynamics365</span><span class="sxs-lookup"><span data-stu-id="82c7d-150">Dynamics365</span></span>
* <span data-ttu-id="82c7d-151">Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="82c7d-151">Dynamics CRM</span></span>
* <span data-ttu-id="82c7d-152">Динамика продаж</span><span class="sxs-lookup"><span data-stu-id="82c7d-152">Dynamics Sales</span></span>
* <span data-ttu-id="82c7d-153">Служба клиентов Dynamics</span><span class="sxs-lookup"><span data-stu-id="82c7d-153">Dynamics Customer Service</span></span>
* <span data-ttu-id="82c7d-154">Служба dynamics</span><span class="sxs-lookup"><span data-stu-id="82c7d-154">Dynamics Service</span></span>
* <span data-ttu-id="82c7d-155">Полевая служба Dynamics</span><span class="sxs-lookup"><span data-stu-id="82c7d-155">Dynamics Field Service</span></span>

## <a name="configure-the-dynamics-365-connector"></a><span data-ttu-id="82c7d-156">Настройка соединиттеля Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="82c7d-156">Configure the Dynamics 365 connector</span></span>

<span data-ttu-id="82c7d-157">С помощью этой простой конфигурации вы можете включить возможности поиска по федерации Dynamics 365 для людей в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="82c7d-157">With this simple configuration, you can enable the Dynamics 365 federation search experience for people in your organization.</span></span>

1. <span data-ttu-id="82c7d-158">В [Центр администрирования Microsoft 365](https://admin.microsoft.com)перейдите к [источникам данных.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/connectors)</span><span class="sxs-lookup"><span data-stu-id="82c7d-158">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [Data sources](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/connectors).</span></span>

2. <span data-ttu-id="82c7d-159">В разделе Приложения и службы Майкрософт в разделе Microsoft  Dynamics 365 выберите Управление открытием панели Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82c7d-159">In the Microsoft apps and services section, under Microsoft Dynamics 365, select **Manage** to open the Microsoft Dynamics 365 panel.</span></span>

3. <span data-ttu-id="82c7d-160">Включении соединитетеля для организации.</span><span class="sxs-lookup"><span data-stu-id="82c7d-160">Enable the connector for your organization.</span></span>

4. <span data-ttu-id="82c7d-161">В **списке Конечные точки** выберите среду Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82c7d-161">In the **Endpoints** list, select your Dynamics 365 environment.</span></span>

5. <span data-ttu-id="82c7d-162">В **ID подключения** введите уникальный ID для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="82c7d-162">In the **Connection ID**, enter a unique ID for this connection.</span></span>

6. <span data-ttu-id="82c7d-163">Просмотрите и выберите поле согласия.</span><span class="sxs-lookup"><span data-stu-id="82c7d-163">Review and select the consent check box.</span></span>

7. <span data-ttu-id="82c7d-164">Выберите **Сохранить,** чтобы завершить настройку подключения.</span><span class="sxs-lookup"><span data-stu-id="82c7d-164">Select **Save** to finish the connection setup.</span></span>

:::image type="content" alt-text="Снимок экрана панели настройка Dynamics 365 в Центр администрирования Microsoft 365" source="media/dynamics365/dynamic365-connection-setup.png" lightbox="media/dynamics365/dynamic365-connection-setup.png":::

<span data-ttu-id="82c7d-166">После завершения установки ответы и вертикаль Dynamics 365 будут отображаться только для пользователей с действительной лицензией Dynamics 365 и доступом к подключенной среде Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82c7d-166">When the setup is complete, Dynamics 365 answers and vertical will only appear for users with a valid Dynamics 365 license and access to the connected Dynamics 365 environment.</span></span> <span data-ttu-id="82c7d-167">В любое время вы можете вернуться к этим настройкам и изменить среду конечной точки подключения или отключить подключение.</span><span class="sxs-lookup"><span data-stu-id="82c7d-167">At any time, you can return to these settings and change the connection endpoint environment or deactivate the connection.</span></span>
