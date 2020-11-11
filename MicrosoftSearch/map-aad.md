---
title: Сопоставление удостоверений AAD
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NOINDEX, NOFOLLOW
description: инструкции по сопоставлению удостоверений AAD
ms.openlocfilehash: e373302314e3044f6bd6b874a341c8a1ada77556
ms.sourcegitcommit: 77ec27736f3c8434b2ac47e10897ac2606ee8a03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2020
ms.locfileid: "48992905"
---
# <a name="map-your-azure-ad-identities"></a><span data-ttu-id="63fbb-103">Сопоставление удостоверений Azure AD</span><span class="sxs-lookup"><span data-stu-id="63fbb-103">Map your Azure AD Identities</span></span>  

<span data-ttu-id="63fbb-104">В этой статье описано, как выполнить сопоставление удостоверений Azure AD с уникальным идентификатором для источника данных (не Azure AD Identity), чтобы пользователи в списке управления доступом (ACL) с удостоверениями, не являющимися Azure AD, могли видеть область результатов поиска в соединителе.</span><span class="sxs-lookup"><span data-stu-id="63fbb-104">This article walks you through the steps of mapping your Azure AD identities to a unique identifier for your data source (non-Azure AD identity) so that people in your Access Control List (ACL) with non-Azure AD identities can see connector search results scoped to them.</span></span>

<span data-ttu-id="63fbb-105">Эти действия относятся только к администраторам поиска, которые настраивают соединитель [Salesforce](salesforce-connector.md) корпорации Майкрософт с разрешениями поиска "только для пользователей с доступом к этому источнику данных" и типом удостоверения "AAD".</span><span class="sxs-lookup"><span data-stu-id="63fbb-105">These steps are only relevant to search administrators who are setting up a [Salesforce](salesforce-connector.md) connector by Microsoft with search permissions for "Only people with access to this data source" and identity type "AAD."</span></span> <span data-ttu-id="63fbb-106">Следующие действия покажут, как сопоставить свойства пользователя Azure AD с **идентификаторами Федерации** пользователей.</span><span class="sxs-lookup"><span data-stu-id="63fbb-106">The following steps walk you through how to map your Azure AD user properties to your users' **Federation IDs**.</span></span>

>[!NOTE]
><span data-ttu-id="63fbb-107">Если вы настраиваете [соединитель Salesforce](salesforce-connector.md) и выбираете **только пользователей с доступом к этому источнику данных** и типу удостоверения, **не являющемуся AAD** на экране "разрешения поиска", ознакомьтесь со статьей Сопоставление удостоверений, [не являющихся Azure AD](map-non-aad.md) , для указания способа СОПОСТАВЛЕНИЯ удостоверений, не являющихся Azure AD.</span><span class="sxs-lookup"><span data-stu-id="63fbb-107">If you are setting up a [Salesforce connector](salesforce-connector.md) and select **Only people with access to this data source** and identity type **non-AAD** on the search permissions screen, refer to the [Map your non-Azure AD Identities](map-non-aad.md) article for steps on how to map non-Azure AD identities.</span></span>  

## <a name="steps-for-mapping-your-azure-ad-properties"></a><span data-ttu-id="63fbb-108">Действия по сопоставлению свойств Azure AD</span><span class="sxs-lookup"><span data-stu-id="63fbb-108">Steps for mapping your Azure AD properties</span></span>

### <a name="1-select-azure-ad-user-properties-to-map"></a><span data-ttu-id="63fbb-109">1. Выберите свойства пользователя Azure AD для сопоставления</span><span class="sxs-lookup"><span data-stu-id="63fbb-109">1. Select Azure AD user properties to map</span></span>

<span data-ttu-id="63fbb-110">Вы можете выбрать свойства Azure AD, которые необходимо сопоставить с ИДЕНТИФИКАТОРом Федерации.</span><span class="sxs-lookup"><span data-stu-id="63fbb-110">You can select the Azure AD properties you need to map to the Federation ID.</span></span>

<span data-ttu-id="63fbb-111">Вы можете выбрать свойство пользователя Azure AD из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="63fbb-111">You can select an Azure AD user property from the dropdown.</span></span> <span data-ttu-id="63fbb-112">Вы также можете добавить столько свойств пользователя Azure AD, сколько необходимо, если эти свойства необходимы для создания сопоставления идентификатора Федерации для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="63fbb-112">You can also add as many Azure AD user properties as you would like if these properties are necessary to create the Federation ID mapping for your organization.</span></span>

### <a name="2-create-formula-to-complete-mapping"></a><span data-ttu-id="63fbb-113">2. Создание формулы для завершения сопоставления</span><span class="sxs-lookup"><span data-stu-id="63fbb-113">2. Create formula to complete mapping</span></span>

<span data-ttu-id="63fbb-114">Можно объединить значения свойств пользователя Azure AD, чтобы сформировать уникальный идентификатор Федерации.</span><span class="sxs-lookup"><span data-stu-id="63fbb-114">You can combine the values of the Azure AD user properties to form the unique Federation ID.</span></span>

<span data-ttu-id="63fbb-115">В поле Формула " {0} " соответствует *первому* выбранному свойству Azure AD.</span><span class="sxs-lookup"><span data-stu-id="63fbb-115">In the formula box, "{0}" corresponds to the *first* Azure AD property you selected.</span></span> <span data-ttu-id="63fbb-116">" {1} " соответствует *второму* выбранному свойству Azure AD.</span><span class="sxs-lookup"><span data-stu-id="63fbb-116">"{1}" corresponds to the *second* Azure AD property you selected.</span></span> <span data-ttu-id="63fbb-117">" {2} " соответствует *третьему* свойству Azure AD и т. д.</span><span class="sxs-lookup"><span data-stu-id="63fbb-117">"{2}" corresponds to the *third* Azure AD property, and so on.</span></span>  

<span data-ttu-id="63fbb-118">Ниже приведено несколько примеров формул с примерами выходов регулярных выражений и выводом формул:</span><span class="sxs-lookup"><span data-stu-id="63fbb-118">Below are some examples of formulas with sample regular expression outputs and formula outputs:</span></span>

| <span data-ttu-id="63fbb-119">Пример формулы</span><span class="sxs-lookup"><span data-stu-id="63fbb-119">Sample formula</span></span>                  | <span data-ttu-id="63fbb-120">Значение свойства {0} для примера пользователя</span><span class="sxs-lookup"><span data-stu-id="63fbb-120">Value of property {0} for a sample user</span></span>                 | <span data-ttu-id="63fbb-121">Значение свойства {1} для примера пользователя</span><span class="sxs-lookup"><span data-stu-id="63fbb-121">Value of property {1} for a sample user</span></span>           | <span data-ttu-id="63fbb-122">Выходные данные формулы</span><span class="sxs-lookup"><span data-stu-id="63fbb-122">Output of formula</span></span>                  |
| :------------------- | :------------------- |:---------------|:---------------|
| <span data-ttu-id="63fbb-123">{0}.{1} @contoso. com</span><span class="sxs-lookup"><span data-stu-id="63fbb-123">{0}.{1}@contoso.com</span></span>  | <span data-ttu-id="63fbb-124">имя</span><span class="sxs-lookup"><span data-stu-id="63fbb-124">firstname</span></span> | <span data-ttu-id="63fbb-125">Фамили</span><span class="sxs-lookup"><span data-stu-id="63fbb-125">lastname</span></span> |<span data-ttu-id="63fbb-126">firstname.lastname@contoso.com</span><span class="sxs-lookup"><span data-stu-id="63fbb-126">firstname.lastname@contoso.com</span></span>
| <span data-ttu-id="63fbb-127">{0}@domain. com</span><span class="sxs-lookup"><span data-stu-id="63fbb-127">{0}@domain.com</span></span>                 | <span data-ttu-id="63fbb-128">UserID</span><span class="sxs-lookup"><span data-stu-id="63fbb-128">userid</span></span>                 |             |<span data-ttu-id="63fbb-129">userid@domain.com</span><span class="sxs-lookup"><span data-stu-id="63fbb-129">userid@domain.com</span></span>

<span data-ttu-id="63fbb-130">После того как вы задаете формулу, вы можете нажать кнопку **Предварительный просмотр** , чтобы просмотреть 5 случайных пользователей из источника данных с применением соответствующих сопоставлений пользователей.</span><span class="sxs-lookup"><span data-stu-id="63fbb-130">After you provide your formula, you can optionally click **Preview** to see a preview of 5 random users from your data source with their respective user mappings applied.</span></span> <span data-ttu-id="63fbb-131">В выходных данных предварительного просмотра содержатся значения пользовательских свойств Azure AD, выбранных на шаге 1 для этих пользователей, и выходные данные итоговой формулы, предоставленной на шаге 2 для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="63fbb-131">The output of the preview includes the value of the Azure AD user properties selected in step 1 for those users and the output of the final formula provided in step 2 for that user.</span></span> <span data-ttu-id="63fbb-132">Кроме того, он указывает, можно ли разрешить выход формулы пользователю Azure AD в клиенте с помощью значка "Success" или "Failed".</span><span class="sxs-lookup"><span data-stu-id="63fbb-132">It also indicates whether the output of the formula could be resolved to an Azure AD user in your tenant via a "Success" or "Failed" icon.</span></span>  

>[!NOTE]
><span data-ttu-id="63fbb-133">Вы по-прежнему можете продолжить создание подключения, если при нажатии кнопки **Предварительный просмотр** одно или несколько сопоставлений пользователей имеют состояние "ошибка".</span><span class="sxs-lookup"><span data-stu-id="63fbb-133">You can still proceed with creating your connection if one or more user mappings have a "Failed" status after you click **Preview**.</span></span> <span data-ttu-id="63fbb-134">В предварительной версии отображаются 5 случайных пользователей и их сопоставления из источника данных.</span><span class="sxs-lookup"><span data-stu-id="63fbb-134">The preview shows 5 random users and their mappings from your data source.</span></span> <span data-ttu-id="63fbb-135">Если вы сопоставлению не удается сопоставить всех пользователей, может возникнуть такая ситуация.</span><span class="sxs-lookup"><span data-stu-id="63fbb-135">If the mapping you provide does not map all users, you may experience this case.</span></span>

## <a name="sample-azure-ad-mapping"></a><span data-ttu-id="63fbb-136">Пример сопоставления Azure AD</span><span class="sxs-lookup"><span data-stu-id="63fbb-136">Sample Azure AD mapping</span></span>

<span data-ttu-id="63fbb-137">Ниже приведен моментальный снимок примера сопоставления Azure AD.</span><span class="sxs-lookup"><span data-stu-id="63fbb-137">See the snapshot below for a sample Azure AD mapping.</span></span>

![Пример моментального снимка, в котором описывается заполнение страницы сопоставления Azure AD](media/aad-mapping.png)

## <a name="limitations"></a><span data-ttu-id="63fbb-139">Ограничения</span><span class="sxs-lookup"><span data-stu-id="63fbb-139">Limitations</span></span>  

- <span data-ttu-id="63fbb-140">Для всех пользователей поддерживается только одно сопоставление.</span><span class="sxs-lookup"><span data-stu-id="63fbb-140">Only one mapping is supported for all users.</span></span> <span data-ttu-id="63fbb-141">Условные сопоставления не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="63fbb-141">Conditional mappings are not supported.</span></span>  

- <span data-ttu-id="63fbb-142">Вы не можете изменить сопоставление после публикации подключения.</span><span class="sxs-lookup"><span data-stu-id="63fbb-142">You cannot change your mapping once the connection is published.</span></span>  

- <span data-ttu-id="63fbb-143">Выражения на основе Regex для свойств пользователя Azure AD не поддерживаются для преобразования идентификатора Федерации Azure AD.</span><span class="sxs-lookup"><span data-stu-id="63fbb-143">Regex-based expressions against the Azure AD user properties are not supported for the Azure AD to Federation ID transformation.</span></span>