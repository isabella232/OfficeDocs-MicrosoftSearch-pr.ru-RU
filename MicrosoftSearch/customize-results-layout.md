---
title: Управление макетами результатов поиска
ms.author: jypal
author: jypal6
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: С помощью адаптивных карт создайте макет для просмотра настраиваемых результатов поиска
ms.openlocfilehash: d29b1a45f11079f4b71f71a387cf43cbf2f48e7d
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031740"
---
<!-- markdownlint-disable no-hard-tabs -->
# <a name="create-a-layout-to-customize-search-results"></a><span data-ttu-id="3f169-103">Создание макета для настройки результатов поиска</span><span class="sxs-lookup"><span data-stu-id="3f169-103">Create a layout to customize search results</span></span>

<span data-ttu-id="3f169-104">Макет результатов можно создать для настраиваемой вертикали с помощью конструктора макета поиска.</span><span class="sxs-lookup"><span data-stu-id="3f169-104">You can design the result layout for a custom vertical using the search layout designer.</span></span> <span data-ttu-id="3f169-105">Вы можете приступить к разработке макета, выбрав шаблоны, предлагаемые в конструкторе макета, и используя их, если они соответствуют вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="3f169-105">You can start designing the layout by choosing templates offered in the layout designer and using them if they fit your requirements.</span></span> <span data-ttu-id="3f169-106">Или вы можете изменить эти шаблоны различными способами, чтобы соответствовать вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="3f169-106">Or you can choose to edit these templates in various ways to fit your requirements.</span></span> <span data-ttu-id="3f169-107">Например, добавьте или удалите изображения, добавьте или удалите текст и измените текст.</span><span class="sxs-lookup"><span data-stu-id="3f169-107">For example, add/remove images, add/remove text, and modify text.</span></span> <span data-ttu-id="3f169-108">Если ни один из шаблонов не соответствует вашим требованиям, можно приступить к разработке макета с помощью пустого шаблона.</span><span class="sxs-lookup"><span data-stu-id="3f169-108">If none of the templates meet your requirements, you can choose to start designing your layout using a blank template.</span></span>  

<span data-ttu-id="3f169-109">После готовности макета используйте язык [шаблона адаптивных](/adaptive-cards/templating/language) карт для создания макета результатов JSON, который используется для определения типа результатов.</span><span class="sxs-lookup"><span data-stu-id="3f169-109">After the layout is ready, use the [Adaptive Cards Template language](/adaptive-cards/templating/language) to create a result layout JSON that's used to define a result type.</span></span> <span data-ttu-id="3f169-110">Свойства результатов сопоставлены с макетом с помощью шага Сопоставление в конструкторе макета.</span><span class="sxs-lookup"><span data-stu-id="3f169-110">You map the result properties to the layout using the Mapping step in the layout designer.</span></span>  

## <a name="create-a-layout-on-your-own"></a><span data-ttu-id="3f169-111">Создание макета самостоятельно</span><span class="sxs-lookup"><span data-stu-id="3f169-111">Create a layout on your own</span></span>

<span data-ttu-id="3f169-112">Создание макета самостоятельно требует знаний о [адаптивных](/adaptive-cards/authoring-cards/getting-started) картах и [их схеме.](https://adaptivecards.io/explorer/)</span><span class="sxs-lookup"><span data-stu-id="3f169-112">Creating a layout on your own requires knowledge of [adaptive cards](/adaptive-cards/authoring-cards/getting-started) and their [schema](https://adaptivecards.io/explorer/).</span></span> <span data-ttu-id="3f169-113">Макет результатов поиска использует подмножество элементов, предлагаемых адаптивными картами, и вы можете использовать конструктор макета, чтобы узнать о поддерживаемом наборе элементов.</span><span class="sxs-lookup"><span data-stu-id="3f169-113">Search result layout uses a subset of the elements offered by adaptive cards, and you can use the layout designer to learn about the supported set of elements.</span></span>  

<span data-ttu-id="3f169-114">Создав собственный макет, создайте макет адаптивной карты с помощью данных из соединителя, а затем завершите макет.</span><span class="sxs-lookup"><span data-stu-id="3f169-114">While creating your own layout, create the adaptive card layout using data from your connector, and then finalize the layout.</span></span>
<span data-ttu-id="3f169-115">Существует два основных шага в создании собственного макета:</span><span class="sxs-lookup"><span data-stu-id="3f169-115">There are two main steps in creating your own layout:</span></span>

- <span data-ttu-id="3f169-116">Разработать макет.</span><span class="sxs-lookup"><span data-stu-id="3f169-116">Design the layout.</span></span>
- <span data-ttu-id="3f169-117">Отделять данные от шаблона.</span><span class="sxs-lookup"><span data-stu-id="3f169-117">Separate the data from the template.</span></span>

### <a name="design-the-layout"></a><span data-ttu-id="3f169-118">Разработка макета</span><span class="sxs-lookup"><span data-stu-id="3f169-118">Design the layout</span></span>

<span data-ttu-id="3f169-119">В этом примере мы показывем макет с загонком, ссылкой и описательным текстом.</span><span class="sxs-lookup"><span data-stu-id="3f169-119">In this example, we show a layout with a header, link, and descriptive text.</span></span>

![Пример макета с загонком, ссылкой и описанием.](media/Verts-ExampleLayout.png)

<span data-ttu-id="3f169-121">И вот связанный файл JSON макета:</span><span class="sxs-lookup"><span data-stu-id="3f169-121">And here's the layout's associated JSON file:</span></span>

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

### <a name="separate-the-data-from-the-layout"></a><span data-ttu-id="3f169-122">Отделять данные от макета</span><span class="sxs-lookup"><span data-stu-id="3f169-122">Separate the data from the layout</span></span>

<span data-ttu-id="3f169-123">Вы можете отделить данные от макета и связать данные.</span><span class="sxs-lookup"><span data-stu-id="3f169-123">You can separate the data from the layout and bind the data.</span></span>

<span data-ttu-id="3f169-124">Вот макет JSON после привязки данных:</span><span class="sxs-lookup"><span data-stu-id="3f169-124">Here's Layout JSON after binding the data:</span></span>

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

<span data-ttu-id="3f169-125">Пример данных. Укажите пример данных в редакторе **выборки** данных, чтобы просмотреть привязанную к данным карту в **режиме предварительного просмотра.**</span><span class="sxs-lookup"><span data-stu-id="3f169-125">Sample data: Specify sample data in the **Sample Data Editor** to view the data-bound card when in **Preview Mode**.</span></span>

```json
{

    "title": "Contoso Marketing Analysis - Q3 FY18",
    "titleUrl": "https://contoso.com/hr/link",
    "link": "https://contoso.com/hr/link",
    "description": "Marketing team, and looking at the Contoso Marketing documents on the team site. Yo can't see right...Marketing Planning presentation?"

}
```

## <a name="map-the-layout-to-the-result-properties"></a><span data-ttu-id="3f169-126">Наметить макет с свойствами результатов</span><span class="sxs-lookup"><span data-stu-id="3f169-126">Map the layout to the result properties</span></span>

<span data-ttu-id="3f169-127">Для создания макета результатов JSON необходимо соединять каждое поле макета с свойством результатов или соединитетелем.</span><span class="sxs-lookup"><span data-stu-id="3f169-127">You must map each field of the layout to a result property or a connector property to generate the result layout JSON.</span></span>

![Захват экрана макета примера на странице Конструктор макета поиска с выбранным полем и открытой областью свойств.](media/Verts-SearchLayoutDesigner.png)

<span data-ttu-id="3f169-129">Выберите поле в макете, чтобы выделить переменные, которые необходимо наметить.</span><span class="sxs-lookup"><span data-stu-id="3f169-129">Select a field in the layout to highlight the variables that need to be mapped.</span></span> <span data-ttu-id="3f169-130">Для одного поля можно использовать несколько переменных, и все поля должны быть соедемы с свойствами результата.</span><span class="sxs-lookup"><span data-stu-id="3f169-130">You can use multiple variables for a single field, and all fields must be mapped to the result properties.</span></span>

### <a name="show-snippet-on-search-result"></a><span data-ttu-id="3f169-131">Показать фрагмент результата поиска</span><span class="sxs-lookup"><span data-stu-id="3f169-131">Show snippet on search result</span></span>  

<span data-ttu-id="3f169-132">Динамические фрагменты, созданные **в** свойстве контента результата соединители, могут быть показаны в результате поиска.</span><span class="sxs-lookup"><span data-stu-id="3f169-132">Dynamic snippets generated on the **content** property of the connector result can be shown on the search result.</span></span> <span data-ttu-id="3f169-133">**ResultSnippet** — это свойство системы, которое выступает в качестве свойства placeholder для фрагментов, созданных для каждого результата Соединитель.</span><span class="sxs-lookup"><span data-stu-id="3f169-133">**ResultSnippet** is the system property that acts as a placeholder property for the snippets generated for each Connector result.</span></span> <span data-ttu-id="3f169-134">Чтобы показать фрагменты макета результатов, свойство **системы ResultSnippet** должно быть соописуется с соответствующим полем, например Description, в макете результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="3f169-134">To show the snippets on the result layout, the **ResultSnippet** system property must be mapped to an appropriate field, for example Description, in the search result layout.</span></span> <span data-ttu-id="3f169-135">Фрагменты, созданные для каждого результата, также выделяют совпадения в фрагменте с термином запроса, в который ввел пользователь.</span><span class="sxs-lookup"><span data-stu-id="3f169-135">Snippets generated on each result also highlight the matches in the Snippet with the query term entered by the user.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="3f169-136">Важные факторы</span><span class="sxs-lookup"><span data-stu-id="3f169-136">Things to consider</span></span>

<span data-ttu-id="3f169-137">Перед началом работы необходимо сделать несколько вещей, которые следует избегать, чтобы убедиться, что макеты будут успешными.</span><span class="sxs-lookup"><span data-stu-id="3f169-137">Before you get started, there are a few things that you should do and a few things you should avoid to ensure that your layouts will be successful.</span></span>

### <a name="do"></a><span data-ttu-id="3f169-138">Правильно</span><span class="sxs-lookup"><span data-stu-id="3f169-138">Do</span></span>

- <span data-ttu-id="3f169-139">Изменить шаблон, чтобы предоставить ссылку на логотип в макете, если вы используете статические ссылки для логотипов, а не свойства результатов.</span><span class="sxs-lookup"><span data-stu-id="3f169-139">Edit a template to provide the logo link in the layout if you're using static links for logos and not result properties.</span></span>
- <span data-ttu-id="3f169-140">Проверка макета результатов для сценариев, в которых данные не возвращаются для свойства результатов, используемой в результате JSON.</span><span class="sxs-lookup"><span data-stu-id="3f169-140">Validate the result layout for scenarios where no data is returned for a result property used in the result JSON.</span></span> <span data-ttu-id="3f169-141">Используйте `$when` условие, чтобы скрыть элемент, если свойство не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="3f169-141">Use the `$when` condition to hide an element if the property doesn't contain data.</span></span>  
- <span data-ttu-id="3f169-142">Убедитесь, что типы данных `$when` условия и свойства результатов совпадают.</span><span class="sxs-lookup"><span data-stu-id="3f169-142">Make sure that data types of the `$when` condition and the result property match.</span></span> <span data-ttu-id="3f169-143">Например, не сравнивайтесь `Number` с `Text` `$when` состоянием.</span><span class="sxs-lookup"><span data-stu-id="3f169-143">For example, don't compare `Number` with `Text` in the `$when` condition.</span></span>  
- <span data-ttu-id="3f169-144">При разработке макета результатов подумайте о требованиях к темам.</span><span class="sxs-lookup"><span data-stu-id="3f169-144">Think of theme requirements when designing a result layout.</span></span>  
- <span data-ttu-id="3f169-145">Убедитесь, что `Textblock`   элемент может обрабатывать динамическое содержимое.</span><span class="sxs-lookup"><span data-stu-id="3f169-145">Make sure that the `Textblock` element can handle dynamic content.</span></span> <span data-ttu-id="3f169-146">Для этого можно `wrap` использовать `maxLines` свойства элементов и элементов.</span><span class="sxs-lookup"><span data-stu-id="3f169-146">You can use the `wrap` and `maxLines` element properties for this purpose.</span></span>
- <span data-ttu-id="3f169-147">Правильно форматировать дату при использовании `{DATE()}` в Markdown.</span><span class="sxs-lookup"><span data-stu-id="3f169-147">Properly format the date when using `{DATE()}` in Markdown.</span></span>  

### <a name="dont"></a><span data-ttu-id="3f169-148">Неправильно</span><span class="sxs-lookup"><span data-stu-id="3f169-148">Don't</span></span>

- <span data-ttu-id="3f169-149">Не определяйте недопустимые типы данных при привязке значений.</span><span class="sxs-lookup"><span data-stu-id="3f169-149">Don't define invalid data types when binding values.</span></span> <span data-ttu-id="3f169-150">Дополнительные сведения о типах данных см. в [схеме Управление схемой поиска.](/sharepoint/search/manage-the-search-schema)</span><span class="sxs-lookup"><span data-stu-id="3f169-150">For more information about data types, see [Manage the Search schema](/sharepoint/search/manage-the-search-schema).</span></span>
- <span data-ttu-id="3f169-151">Избегайте обрезки результата на странице результатов, следуя максимальной высоте макета результатов JSON.</span><span class="sxs-lookup"><span data-stu-id="3f169-151">Avoid cropping the result on the result page by following the maximum height of the result layout JSON.</span></span> <span data-ttu-id="3f169-152">Если вы превышаете максимальную высоту макета результатов, результат будет обрезан на странице результатов.</span><span class="sxs-lookup"><span data-stu-id="3f169-152">If you exceed the maximum height of the result layout, the result will be cropped on the result page.</span></span>
- <span data-ttu-id="3f169-153">Не используйте `px` значения в свойствах элементов.</span><span class="sxs-lookup"><span data-stu-id="3f169-153">Don't use `px` values in element properties.</span></span>
- <span data-ttu-id="3f169-154">Не используйте разметку с **свойством ResultSnippet** в макете результатов для выделения совпадения запросов в результате поиска.</span><span class="sxs-lookup"><span data-stu-id="3f169-154">Don't use markdown with the **ResultSnippet** property in the result layout to highlight query match in the search result.</span></span>

## <a name="resources"></a><span data-ttu-id="3f169-155">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f169-155">Resources</span></span>

[<span data-ttu-id="3f169-156">Настройка страницы результатов поиска</span><span class="sxs-lookup"><span data-stu-id="3f169-156">Customize search result page</span></span>](customize-search-page.md)

[<span data-ttu-id="3f169-157">Адаптивные карты</span><span class="sxs-lookup"><span data-stu-id="3f169-157">Adaptive cards</span></span>](/adaptive-cards/authoring-cards/getting-started)

[<span data-ttu-id="3f169-158">Язык шаблона адаптивных карт</span><span class="sxs-lookup"><span data-stu-id="3f169-158">Adaptive Cards Template language</span></span>](/adaptive-cards/templating/language)

[<span data-ttu-id="3f169-159">Схема адаптивной карты</span><span class="sxs-lookup"><span data-stu-id="3f169-159">Adaptive card schema</span></span>](https://adaptivecards.io/explorer/)