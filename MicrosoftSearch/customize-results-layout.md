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
description: Создание макета с помощью адаптивных карт для просмотра настраиваемых результатов поиска
ms.openlocfilehash: 425e5404c14d500f6ecd84ad449dafb05bbfd31b
ms.sourcegitcommit: 59435698bece013ae64ca2a68c43455ca10e3fdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "48927183"
---
<!-- markdownlint-disable no-hard-tabs -->
# <a name="create-a-layout-to-customize-search-results"></a><span data-ttu-id="e5922-103">Создание макета для настройки результатов поиска</span><span class="sxs-lookup"><span data-stu-id="e5922-103">Create a layout to customize search results</span></span>

<span data-ttu-id="e5922-104">Макет результатов можно спроектировать для настраиваемого вертикального элемента с помощью конструктора макета поиска.</span><span class="sxs-lookup"><span data-stu-id="e5922-104">You can design the result layout for a custom vertical using the search layout designer.</span></span> <span data-ttu-id="e5922-105">Вы можете начать разработку макета, выбрав шаблоны, предлагаемые в конструкторе макета, и используя их в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="e5922-105">You can start designing the layout by choosing templates offered in the layout designer and using them if they fit your requirements.</span></span> <span data-ttu-id="e5922-106">Кроме того, вы можете изменить эти шаблоны различными способами в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="e5922-106">Or you can choose to edit these templates in various ways to fit your requirements.</span></span> <span data-ttu-id="e5922-107">Например, добавлять и удалять изображения, добавлять и удалять текст и изменять текст.</span><span class="sxs-lookup"><span data-stu-id="e5922-107">For example, add/remove images, add/remove text, and modify text.</span></span> <span data-ttu-id="e5922-108">Если ни один из шаблонов не соответствует вашим требованиям, вы можете начать разработку макета с помощью пустого шаблона.</span><span class="sxs-lookup"><span data-stu-id="e5922-108">If none of the templates meet your requirements, you can choose to start designing your layout using a blank template.</span></span>  

<span data-ttu-id="e5922-109">После того как макет будет готов, используйте [язык шаблона "адаптивные карточки](https://docs.microsoft.com/adaptive-cards/templating/language) " для создания макета результатов JSON, который используется для определения типа результата.</span><span class="sxs-lookup"><span data-stu-id="e5922-109">After the layout is ready, use the [Adaptive Cards Template language](https://docs.microsoft.com/adaptive-cards/templating/language) to create a result layout JSON that's used to define a result type.</span></span> <span data-ttu-id="e5922-110">Свойства результатов сопоставляются с макетом с помощью шага сопоставления в конструкторе макетов.</span><span class="sxs-lookup"><span data-stu-id="e5922-110">You map the result properties to the layout using the Mapping step in the layout designer.</span></span>  

## <a name="create-a-layout-on-your-own"></a><span data-ttu-id="e5922-111">Создание макета на собственном диске</span><span class="sxs-lookup"><span data-stu-id="e5922-111">Create a layout on your own</span></span>

<span data-ttu-id="e5922-112">Для самостоятельного создания макета необходимы сведения о [адаптивных картах](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started) и их [схемах](https://adaptivecards.io/explorer/).</span><span class="sxs-lookup"><span data-stu-id="e5922-112">Creating a layout on your own requires knowledge of [adaptive cards](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started) and their [schema](https://adaptivecards.io/explorer/).</span></span> <span data-ttu-id="e5922-113">В макете результатов поиска используется подмножество элементов, предлагаемых адаптивными картами, и вы можете использовать конструктор макетов для получения сведений о поддерживаемых наборах элементов.</span><span class="sxs-lookup"><span data-stu-id="e5922-113">Search result layout uses a subset of the elements offered by adaptive cards, and you can use the layout designer to learn about the supported set of elements.</span></span>  

<span data-ttu-id="e5922-114">При создании собственного макета создайте макет адаптивной карточки с помощью данных из соединителя, а затем завершите макет.</span><span class="sxs-lookup"><span data-stu-id="e5922-114">While creating your own layout, create the adaptive card layout using data from your connector, and then finalize the layout.</span></span>
<span data-ttu-id="e5922-115">Создание собственного макета состоит из двух основных этапов:</span><span class="sxs-lookup"><span data-stu-id="e5922-115">There are two main steps in creating your own layout:</span></span>

- <span data-ttu-id="e5922-116">Разработайте макет.</span><span class="sxs-lookup"><span data-stu-id="e5922-116">Design the layout.</span></span>
- <span data-ttu-id="e5922-117">Отделение данных от шаблона.</span><span class="sxs-lookup"><span data-stu-id="e5922-117">Separate the data from the template.</span></span>

### <a name="design-the-layout"></a><span data-ttu-id="e5922-118">Разработка макета</span><span class="sxs-lookup"><span data-stu-id="e5922-118">Design the layout</span></span>

<span data-ttu-id="e5922-119">В этом примере показан макет с заголовком, ссылкой и текстом описания.</span><span class="sxs-lookup"><span data-stu-id="e5922-119">In this example, we show a layout with a header, link, and descriptive text.</span></span>

![Пример макета с заголовком, ссылкой и описанием.](media/Verts-ExampleLayout.png)

<span data-ttu-id="e5922-121">А вот файл JSON, связанный с макетом:</span><span class="sxs-lookup"><span data-stu-id="e5922-121">And here's the layout's associated JSON file:</span></span>

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

### <a name="separate-the-data-from-the-layout"></a><span data-ttu-id="e5922-122">Отделение данных от макета</span><span class="sxs-lookup"><span data-stu-id="e5922-122">Separate the data from the layout</span></span>

<span data-ttu-id="e5922-123">Вы можете отделить данные от макета и привязывать данные.</span><span class="sxs-lookup"><span data-stu-id="e5922-123">You can separate the data from the layout and bind the data.</span></span>

<span data-ttu-id="e5922-124">Вот макет JSON после привязки данных:</span><span class="sxs-lookup"><span data-stu-id="e5922-124">Here's Layout JSON after binding the data:</span></span>

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

<span data-ttu-id="e5922-125">Образец данных: указание образца данных в **редакторе образца данных** для просмотра карточки с привязкой к данным в **режиме предварительного просмотра**.</span><span class="sxs-lookup"><span data-stu-id="e5922-125">Sample data: Specify sample data in the **Sample Data Editor** to view the data-bound card when in **Preview Mode**.</span></span>

```json
{

    "title": "Contoso Marketing Analysis - Q3 FY18",
    "titleUrl": "https://contoso.com/hr/link",
    "link": "https://contoso.com/hr/link",
    "description": "Marketing team, and looking at the Contoso Marketing documents on the team site. Yo can't see right...Marketing Planning presentation?"

}
```

## <a name="map-the-layout-to-the-result-properties"></a><span data-ttu-id="e5922-126">Сопоставление макета со свойствами результатов</span><span class="sxs-lookup"><span data-stu-id="e5922-126">Map the layout to the result properties</span></span>

<span data-ttu-id="e5922-127">Необходимо сопоставить каждое поле макета со свойством Result или свойством Connector, чтобы создать макет результатов JSON.</span><span class="sxs-lookup"><span data-stu-id="e5922-127">You must map each field of the layout to a result property or a connector property to generate the result layout JSON.</span></span>

![Снимок экрана с примером макета на странице конструктора макета поиска с выбранным полем и областью свойств.](media/Verts-SearchLayoutDesigner.png)

<span data-ttu-id="e5922-129">Выберите поле в макете, чтобы выделить переменные, которые необходимо сопоставить.</span><span class="sxs-lookup"><span data-stu-id="e5922-129">Select a field in the layout to highlight the variables that need to be mapped.</span></span> <span data-ttu-id="e5922-130">Можно использовать несколько переменных для одного поля, и все поля должны быть сопоставлены со свойствами результатов.</span><span class="sxs-lookup"><span data-stu-id="e5922-130">You can use multiple variables for a single field, and all fields must be mapped to the result properties.</span></span>

### <a name="show-snippet-on-search-result"></a><span data-ttu-id="e5922-131">Показать фрагмент кода по результату поиска</span><span class="sxs-lookup"><span data-stu-id="e5922-131">Show snippet on search result</span></span>  

<span data-ttu-id="e5922-132">Динамические фрагменты, созданные в свойстве **Content** результата соединителя, могут отображаться в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="e5922-132">Dynamic snippets generated on the **content** property of the connector result can be shown on the search result.</span></span> <span data-ttu-id="e5922-133">**Ресултсниппет** — это свойство System, которое выступает в качестве свойства заполнителя для фрагментов, созданных для каждого результата соединителя.</span><span class="sxs-lookup"><span data-stu-id="e5922-133">**ResultSnippet** is the system property that acts as a placeholder property for the snippets generated for each Connector result.</span></span> <span data-ttu-id="e5922-134">Чтобы отобразить фрагменты на макете результатов, свойство системы **ресултсниппет** должно быть сопоставлено с соответствующим полем (например, описание) в макете результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="e5922-134">To show the snippets on the result layout, the **ResultSnippet** system property must be mapped to an appropriate field, for example Description, in the search result layout.</span></span> <span data-ttu-id="e5922-135">Фрагменты, созданные для каждого результата, также выделяют совпадения во фрагменте термином запроса, введенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="e5922-135">Snippets generated on each result also highlight the matches in the Snippet with the query term entered by the user.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="e5922-136">Важные факторы</span><span class="sxs-lookup"><span data-stu-id="e5922-136">Things to consider</span></span>

<span data-ttu-id="e5922-137">Прежде чем приступить к работе, необходимо выполнить несколько действий, а также не только убедиться, что ваши макеты будут успешными.</span><span class="sxs-lookup"><span data-stu-id="e5922-137">Before you get started, there are a few things that you should do and a few things you should avoid to ensure that your layouts will be successful.</span></span>

### <a name="do"></a><span data-ttu-id="e5922-138">Правильно</span><span class="sxs-lookup"><span data-stu-id="e5922-138">Do</span></span>

- <span data-ttu-id="e5922-139">Если вы используете статические ссылки для логотипов, а не свойства результатов, измените шаблон, чтобы предоставить ссылку на логотип в макете.</span><span class="sxs-lookup"><span data-stu-id="e5922-139">Edit a template to provide the logo link in the layout if you're using static links for logos and not result properties.</span></span>
- <span data-ttu-id="e5922-140">Проверка структуры результатов для сценариев, в которых не возвращаются данные для свойства Result, используемого в результирующем JSON.</span><span class="sxs-lookup"><span data-stu-id="e5922-140">Validate the result layout for scenarios where no data is returned for a result property used in the result JSON.</span></span> <span data-ttu-id="e5922-141">Используйте `$when` условие, чтобы скрыть элемент, если свойство не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="e5922-141">Use the `$when` condition to hide an element if the property doesn't contain data.</span></span>  
- <span data-ttu-id="e5922-142">Убедитесь, что типы данных `$when` условия и свойства результата совпадают.</span><span class="sxs-lookup"><span data-stu-id="e5922-142">Make sure that data types of the `$when` condition and the result property match.</span></span> <span data-ttu-id="e5922-143">Например, не следует сравнивать `Number` с `Text` `$when` условием.</span><span class="sxs-lookup"><span data-stu-id="e5922-143">For example, don't compare `Number` with `Text` in the `$when` condition.</span></span>  
- <span data-ttu-id="e5922-144">При проектировании структуры результатов следует учитывать требования к теме.</span><span class="sxs-lookup"><span data-stu-id="e5922-144">Think of theme requirements when designing a result layout.</span></span>  
- <span data-ttu-id="e5922-145">Убедитесь, что `Textblock`   элемент может обрабатывать динамическое содержимое.</span><span class="sxs-lookup"><span data-stu-id="e5922-145">Make sure that the `Textblock` element can handle dynamic content.</span></span> <span data-ttu-id="e5922-146">`wrap` `maxLines` Для этой цели можно использовать свойства элемента и.</span><span class="sxs-lookup"><span data-stu-id="e5922-146">You can use the `wrap` and `maxLines` element properties for this purpose.</span></span>
- <span data-ttu-id="e5922-147">Правильно форматировать дату при использовании `{DATE()}` в Markdown.</span><span class="sxs-lookup"><span data-stu-id="e5922-147">Properly format the date when using `{DATE()}` in Markdown.</span></span>  

### <a name="dont"></a><span data-ttu-id="e5922-148">Неправильно</span><span class="sxs-lookup"><span data-stu-id="e5922-148">Don't</span></span>

- <span data-ttu-id="e5922-149">При связывании значений не определяйте недопустимые типы данных.</span><span class="sxs-lookup"><span data-stu-id="e5922-149">Don't define invalid data types when binding values.</span></span> <span data-ttu-id="e5922-150">Дополнительные сведения о типах данных можно найти в статье [Управление схемой поиска](https://docs.microsoft.com/sharepoint/search/manage-the-search-schema).</span><span class="sxs-lookup"><span data-stu-id="e5922-150">For more information about data types, see [Manage the Search schema](https://docs.microsoft.com/sharepoint/search/manage-the-search-schema).</span></span>
- <span data-ttu-id="e5922-151">Не обрезайте результат на странице результатов, следуя максимальной высоте в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e5922-151">Avoid cropping the result on the result page by following the maximum height of the result layout JSON.</span></span> <span data-ttu-id="e5922-152">Если вы превысили максимальную высоту макета результатов, результат будет обрезан на странице результатов.</span><span class="sxs-lookup"><span data-stu-id="e5922-152">If you exceed the maximum height of the result layout, the result will be cropped on the result page.</span></span>
- <span data-ttu-id="e5922-153">Не используйте `px` значения в свойствах элементов.</span><span class="sxs-lookup"><span data-stu-id="e5922-153">Don't use `px` values in element properties.</span></span>
- <span data-ttu-id="e5922-154">Не используйте Markdown со свойством **ресултсниппет** в макете результатов, чтобы выделить поисковый запрос в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="e5922-154">Don't use markdown with the **ResultSnippet** property in the result layout to highlight query match in the search result.</span></span>

## <a name="resources"></a><span data-ttu-id="e5922-155">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="e5922-155">Resources</span></span>

[<span data-ttu-id="e5922-156">Настройка страницы результатов поиска</span><span class="sxs-lookup"><span data-stu-id="e5922-156">Customize search result page</span></span>](customize-search-page.md)

[<span data-ttu-id="e5922-157">Адаптивные карты</span><span class="sxs-lookup"><span data-stu-id="e5922-157">Adaptive cards</span></span>](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started)

[<span data-ttu-id="e5922-158">Язык шаблона "адаптивные карты"</span><span class="sxs-lookup"><span data-stu-id="e5922-158">Adaptive Cards Template language</span></span>](https://docs.microsoft.com/adaptive-cards/templating/language)

[<span data-ttu-id="e5922-159">Схема адаптивной карточки</span><span class="sxs-lookup"><span data-stu-id="e5922-159">Adaptive card schema</span></span>](https://adaptivecards.io/explorer/)