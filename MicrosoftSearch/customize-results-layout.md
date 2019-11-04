---
title: Настройка макета результатов поиска
ms.author: anfowler
author: adefowler
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Создание макета с помощью адаптивных карт для просмотра настраиваемых результатов поиска
ms.openlocfilehash: 2ca53f2e2dc207acdf48542f39ee4f448bdeb90e
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949973"
---
# <a name="create-a-layout-to-customize-search-results"></a><span data-ttu-id="9af1f-103">Создание макета для настройки результатов поиска</span><span class="sxs-lookup"><span data-stu-id="9af1f-103">Create a layout to customize search results</span></span>

<span data-ttu-id="9af1f-104">Макет результатов можно спроектировать для настраиваемого вертикального элемента с помощью конструктора макета поиска.</span><span class="sxs-lookup"><span data-stu-id="9af1f-104">You can design the result layout for a custom vertical using the search layout designer.</span></span> <span data-ttu-id="9af1f-105">Вы можете начать разработку макета, выбрав шаблоны, предлагаемые в конструкторе макета, и используя их в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="9af1f-105">You can start designing the layout by choosing templates offered in the layout designer and using them if they fit your requirements.</span></span> <span data-ttu-id="9af1f-106">Кроме того, вы можете изменить эти шаблоны различными способами в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="9af1f-106">Or you can choose to edit these templates in various ways to fit your requirements.</span></span> <span data-ttu-id="9af1f-107">Например, добавлять и удалять изображения, добавлять и удалять текст, изменять текст.</span><span class="sxs-lookup"><span data-stu-id="9af1f-107">For example, add/remove images, add/remove text, modify text.</span></span> <span data-ttu-id="9af1f-108">Если ни один из шаблонов не соответствует вашему требованию, вы можете начать разработку макета с помощью пустого шаблона.</span><span class="sxs-lookup"><span data-stu-id="9af1f-108">If none of the templates meet your requirement, you can choose to start designing your layout using a blank template.</span></span>  

 

<span data-ttu-id="9af1f-109">После того как макет будет готов, используйте [язык шаблона "адаптивные карты](https://docs.microsoft.com/adaptive-cards/templating/language) ", чтобы создать JSON Layout Layout Layout, который используется для определения типа результата.</span><span class="sxs-lookup"><span data-stu-id="9af1f-109">Once the layout is ready, you use the [Adaptive Cards Template language](https://docs.microsoft.com/adaptive-cards/templating/language)  to create thea result layout JSON which is used to define a result type.</span></span> <span data-ttu-id="9af1f-110">Свойства результатов сопоставляются с макетом с помощью шага сопоставления в конструкторе макетов.</span><span class="sxs-lookup"><span data-stu-id="9af1f-110">You map the result properties to the layout using the Mapping step in the layout designer.</span></span>  

## <a name="create-a-layout-on-your-own"></a><span data-ttu-id="9af1f-111">Создание макета на собственном диске</span><span class="sxs-lookup"><span data-stu-id="9af1f-111">Create a layout on your own</span></span>
<span data-ttu-id="9af1f-112">Для самостоятельного создания макета необходимы сведения о [адаптивных картах](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started) и их [схемах](https://adaptivecards.io/explorer/).</span><span class="sxs-lookup"><span data-stu-id="9af1f-112">Creating a layout on your own requires knowledge of [adaptive cards](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started) and their [schema](https://adaptivecards.io/explorer/).</span></span> <span data-ttu-id="9af1f-113">В макете результатов поиска используется подмножество элементов, предлагаемых адаптивными картами, и вы можете использовать конструктор макетов для получения сведений о поддерживаемых наборах элементов.</span><span class="sxs-lookup"><span data-stu-id="9af1f-113">Search result layout uses a subset of the elements offered by adaptive cards and you can use the layout designer to learn about the supported set of elements.</span></span>  

<span data-ttu-id="9af1f-114">При создании собственного макета создайте макет адаптивной карточки с помощью данных из, а затем завершите макет.</span><span class="sxs-lookup"><span data-stu-id="9af1f-114">While creating your own layout, create the adaptive card layout using data from your , and then finalize the layout.</span></span>
<span data-ttu-id="9af1f-115">Создание собственного макета состоит из двух основных этапов.</span><span class="sxs-lookup"><span data-stu-id="9af1f-115">There are two main steps in creating your own layout</span></span>
- <span data-ttu-id="9af1f-116">Разработка макета</span><span class="sxs-lookup"><span data-stu-id="9af1f-116">Designing the layout</span></span>
- <span data-ttu-id="9af1f-117">Отделение данных от шаблона</span><span class="sxs-lookup"><span data-stu-id="9af1f-117">Separating the data from the template</span></span>

#### <a name="designing-the-layout"></a><span data-ttu-id="9af1f-118">Разработка макета</span><span class="sxs-lookup"><span data-stu-id="9af1f-118">Designing the layout</span></span>

<span data-ttu-id="9af1f-119">В этом примере показан макет с заголовком, ссылкой и текстом описания.</span><span class="sxs-lookup"><span data-stu-id="9af1f-119">In this example, we're showing a layout with a header, link, and descriptive text.</span></span>

![Пример макета с заголовком, ссылкой и описанием.](media/Verts-ExampleLayout.png)

<span data-ttu-id="9af1f-121">А вот файл JSON, связанный с макетом:</span><span class="sxs-lookup"><span data-stu-id="9af1f-121">And here's the layout's associated JSON file:</span></span>


```json
{ 
    "type": "AdaptiveCard", 
    "version": "1.0", 
     "body": [ 
{ 

            "type": "ColumnSet", 
             "columns": [ 
                 { 
                     "type": "Column", 
                     "width": 8, 
                     "items": [ 
                         { 
                             "type": "TextBlock", 
                             "text": "Contoso Marketing Analysis - Q3 FY18", 
                             "color": "Accent", 
                             "size": "Medium", 
                             "spacing": "None", 
                             "$when": "{title != \"\"}", 
                             "weight": "Bolder" 
                        }, 
                        { 
                        "type": "TextBlock",  
                        "text": "https://contoso.com/hr/link", 
                        "spacing": "None",  
                        "color": "Dark", 
                        "weight": "Bolder" 

                        }, 

                        {  
                        "type": "TextBlock", 
                        "text": "Marketing team at Contoso.., and looking at the Contoso Marketing documents on the team site. This contains the data from FY20 and will taken over to FY21...Marketing Planning is ongoing for FY20..",  
                        "wrap": true, 
                        "maxLines": 2, 
                        "spacing": "Medium" 
                        } 
                        ], 

                    "horizontalAlignment": "Center", 
                    "spacing": "None" 

                } 

            ] 

        } 
        ], 

    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json" 
}
```

#### <a name="separating-the-data-from-the-layout"></a><span data-ttu-id="9af1f-122">Отделение данных от макета</span><span class="sxs-lookup"><span data-stu-id="9af1f-122">Separating the data from the layout</span></span>

<span data-ttu-id="9af1f-123">Вы можете отделить данные от макета и привязывать данные.</span><span class="sxs-lookup"><span data-stu-id="9af1f-123">You can separate the data from the layout and bind the data.</span></span> 

<span data-ttu-id="9af1f-124">Вот макет JSON после привязки данных:</span><span class="sxs-lookup"><span data-stu-id="9af1f-124">Here's Layout JSON after binding the data:</span></span>


```json
{ 

    "type": "AdaptiveCard", 
    "version": "1.0", 
    "body": [ 
    { 
    "type": "ColumnSet", 
"columns": [ 

                { 
                "type": "Column", 
                "width": 8, 
                "items": [ 
                { 
                "type": "TextBlock", 
                "text": "[{title}]({titleUrl})", 
                "color": "Accent", 
                "size": "Medium",
                "spacing": "None", 
                "weight": "Bolder" 

                 }, 
                 { 
                 "type": "TextBlock", 
                 "text": "{link}",
                 "spacing": "None", 
                 "color": "Dark",
                 "weight": "Bolder" 
                 }, 
                 { 
                 "type": "TextBlock",
                 "text": "{description}",
                 "wrap": true,
                 "maxLines": 2, 
                 "spacing": "Medium" 
                 } 
                 ], 
                 "horizontalAlignment": "Center", 
                 "spacing": "None" 
                 } 
                 ] 

        } 

    ], 

    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json" 
}
```

<span data-ttu-id="9af1f-125">Образец данных: указание образца данных в **редакторе образца данных** для просмотра карточки с привязкой к данным в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="9af1f-125">Sample data: Specify sample data in the **Sample Data Editor** to view the data-bound card when in "Preview Mode".</span></span>

```json
{ 

    "title": "Contoso Marketing Analysis - Q3 FY18", 
    "titleUrl": "https://contoso.com/hr/link", 
    "link": "https://contoso.com/hr/link", 
    "description": "Marketing team, and looking at the Contoso Marketing documents on the team site. Yo can't see right...Marketing Planning presentation?" 

} 
```

## <a name="map-the-layout-to-the-result-properties"></a><span data-ttu-id="9af1f-126">Сопоставление макета со свойствами результатов</span><span class="sxs-lookup"><span data-stu-id="9af1f-126">Map the layout to the result properties</span></span>

<span data-ttu-id="9af1f-127">Необходимо сопоставить каждое поле макета со свойством Result или свойством Connector, чтобы создать макет результатов JSON.</span><span class="sxs-lookup"><span data-stu-id="9af1f-127">You must map each field of the layout to a result property or a connector property to generate the result layout JSON.</span></span>

![Вертс-сеарчлайаутдесигнер. png](media/Verts-SearchLayoutDesigner.png)

<span data-ttu-id="9af1f-129">Выберите поле в макете, чтобы выделить переменные, которые необходимо сопоставить.</span><span class="sxs-lookup"><span data-stu-id="9af1f-129">Select a field in the layout to highlight the variables that need to be mapped.</span></span> <span data-ttu-id="9af1f-130">Можно использовать несколько переменных для одного поля, и все поля должны быть сопоставлены со свойствами результатов.</span><span class="sxs-lookup"><span data-stu-id="9af1f-130">You can use multiple variables for a single field and all fields must be mapped to the result properties.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="9af1f-131">Факторы, которые необходимо учитывать...</span><span class="sxs-lookup"><span data-stu-id="9af1f-131">Things to consider...</span></span>

<span data-ttu-id="9af1f-132">Прежде чем приступить к работе, необходимо выполнить несколько действий, а также не только убедиться, что ваши макеты будут успешными.</span><span class="sxs-lookup"><span data-stu-id="9af1f-132">Before you get started, there are a few things that you should do and a few things you should avoid to ensure that your layouts will be successful.</span></span>

### <a name="do"></a><span data-ttu-id="9af1f-133">Правильно</span><span class="sxs-lookup"><span data-stu-id="9af1f-133">Do</span></span>

- <span data-ttu-id="9af1f-134">Если вы используете статические ссылки для логотипов, а не свойства результатов, измените шаблон, чтобы предоставить ссылку на логотип в макете.</span><span class="sxs-lookup"><span data-stu-id="9af1f-134">Edit a template to provide the logo link in the layout if you are using static links for logos and not result properties.</span></span>   
- <span data-ttu-id="9af1f-135">Проверка структуры результатов для сценариев, в которых не возвращаются данные для свойства Result, используемого в результирующем JSON.</span><span class="sxs-lookup"><span data-stu-id="9af1f-135">Validate the result layout for scenarios where no data is returned for a result property used in the result JSON.</span></span> <span data-ttu-id="9af1f-136">Используйте `$when` условие, чтобы скрыть элемент, если свойство не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="9af1f-136">Use `$when` condition to hide an element if the property doesn't contain data.</span></span>  
- <span data-ttu-id="9af1f-137">Убедитесь, что типы данных `$when` условия и свойства результата совпадают.</span><span class="sxs-lookup"><span data-stu-id="9af1f-137">Make sure that data types of the `$when` condition and the result property match.</span></span> <span data-ttu-id="9af1f-138">Например, не следует сравнивать `Number` с `Text` условием в `$when` .</span><span class="sxs-lookup"><span data-stu-id="9af1f-138">For example, don't compare `Number` with `Text` in `$when` condition.</span></span>  
- <span data-ttu-id="9af1f-139">При проектировании структуры результатов следует учитывать требования к теме.</span><span class="sxs-lookup"><span data-stu-id="9af1f-139">Think of theme requirements when designing a result layout.</span></span>  
- <span data-ttu-id="9af1f-140">Убедитесь, `Textblock`  что элемент может обрабатывать динамическое содержимое.</span><span class="sxs-lookup"><span data-stu-id="9af1f-140">Make sure that `Textblock` element can handle dynamic content.</span></span> <span data-ttu-id="9af1f-141">Для этой цели можно `wrap` использовать `maxLines` свойства элемента и.</span><span class="sxs-lookup"><span data-stu-id="9af1f-141">You can use the `wrap` and `maxLines` element properties for this purpose.</span></span> 
- <span data-ttu-id="9af1f-142">Правильно форматировать дату при использовании `{DATE()}` в Markdown.</span><span class="sxs-lookup"><span data-stu-id="9af1f-142">Properly format the date when using `{DATE()}` in markdown.</span></span>  

### <a name="dont"></a><span data-ttu-id="9af1f-143">Неправильно</span><span class="sxs-lookup"><span data-stu-id="9af1f-143">Don't</span></span>

- <span data-ttu-id="9af1f-144">При связывании значений не определяйте недопустимые типы данных.</span><span class="sxs-lookup"><span data-stu-id="9af1f-144">Don't define invalid data types when binding values.</span></span> <span data-ttu-id="9af1f-145">Дополнительные сведения о типах данных можно найти в статье [Управление схемой поиска](https://docs.microsoft.com/sharepoint/search/manage-the-search-schema ).</span><span class="sxs-lookup"><span data-stu-id="9af1f-145">For more information about the data types, see [Manage the Search schema](https://docs.microsoft.com/sharepoint/search/manage-the-search-schema ).</span></span>
- <span data-ttu-id="9af1f-146">Не обрезайте результат на странице результатов, следуя максимальной высоте в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="9af1f-146">Avoid cropping the result on the result page by following the maximum height of the result layout JSON.</span></span> <span data-ttu-id="9af1f-147">Если вы превысили максимальную высоту структуры результатов, результат будет обрезан на странице результатов.</span><span class="sxs-lookup"><span data-stu-id="9af1f-147">If you exceed the maximum height of the result layout the result will be cropped on the result page.</span></span>
- <span data-ttu-id="9af1f-148">Не используйте `px` значения в свойствах element.</span><span class="sxs-lookup"><span data-stu-id="9af1f-148">Don't use `px` values in properties of element.</span></span>


## <a name="resources"></a><span data-ttu-id="9af1f-149">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="9af1f-149">Resources</span></span>
[<span data-ttu-id="9af1f-150">Настройка страницы результатов поиска</span><span class="sxs-lookup"><span data-stu-id="9af1f-150">Customize search result page</span></span>](customize-search-page.md)

[<span data-ttu-id="9af1f-151">Адаптивные карты</span><span class="sxs-lookup"><span data-stu-id="9af1f-151">Adaptive cards</span></span>](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started)

[<span data-ttu-id="9af1f-152">Язык шаблона "адаптивные карты"</span><span class="sxs-lookup"><span data-stu-id="9af1f-152">Adaptive Cards Template language</span></span>](https://docs.microsoft.com/adaptive-cards/templating/language)

[<span data-ttu-id="9af1f-153">Схема адаптивной карточки</span><span class="sxs-lookup"><span data-stu-id="9af1f-153">Adaptive card schema</span></span>](https://adaptivecards.io/explorer/)
