---
title: Настройка макета результатов поиска
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
ms.openlocfilehash: e31be1f9c1602fcd696c99d584388facee22df74
ms.sourcegitcommit: c22e8c3dcc53857da677db98a1a2b7d5ca2c6170
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "41721780"
---
<!-- markdownlint-disable no-hard-tabs -->
# <a name="create-a-layout-to-customize-search-results"></a>Создание макета для настройки результатов поиска

Макет результатов можно спроектировать для настраиваемого вертикального элемента с помощью конструктора макета поиска. Вы можете начать разработку макета, выбрав шаблоны, предлагаемые в конструкторе макета, и используя их в соответствии с вашими требованиями. Кроме того, вы можете изменить эти шаблоны различными способами в соответствии с вашими требованиями. Например, добавлять и удалять изображения, добавлять и удалять текст и изменять текст. Если ни один из шаблонов не соответствует вашим требованиям, вы можете начать разработку макета с помощью пустого шаблона.  

После того как макет будет готов, используйте [язык шаблона "адаптивные карточки](https://docs.microsoft.com/adaptive-cards/templating/language) " для создания макета результатов JSON, который используется для определения типа результата. Свойства результатов сопоставляются с макетом с помощью шага сопоставления в конструкторе макетов.  

## <a name="create-a-layout-on-your-own"></a>Создание макета на собственном диске

Для самостоятельного создания макета необходимы сведения о [адаптивных картах](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started) и их [схемах](https://adaptivecards.io/explorer/). В макете результатов поиска используется подмножество элементов, предлагаемых адаптивными картами, и вы можете использовать конструктор макетов для получения сведений о поддерживаемых наборах элементов.  

При создании собственного макета создайте макет адаптивной карточки с помощью данных из соединителя, а затем завершите макет.
Создание собственного макета состоит из двух основных этапов:

- Разработайте макет.
- Отделение данных от шаблона.

### <a name="design-the-layout"></a>Разработка макета

В этом примере показан макет с заголовком, ссылкой и текстом описания.

![Пример макета с заголовком, ссылкой и описанием.](media/Verts-ExampleLayout.png)

А вот файл JSON, связанный с макетом:

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

### <a name="separate-the-data-from-the-layout"></a>Отделение данных от макета

Вы можете отделить данные от макета и привязывать данные.

Вот макет JSON после привязки данных:

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

Образец данных: указание образца данных в **редакторе образца данных** для просмотра карточки с привязкой к данным в **режиме предварительного просмотра**.

```json
{

    "title": "Contoso Marketing Analysis - Q3 FY18",
    "titleUrl": "https://contoso.com/hr/link",
    "link": "https://contoso.com/hr/link",
    "description": "Marketing team, and looking at the Contoso Marketing documents on the team site. Yo can't see right...Marketing Planning presentation?"

}
```

## <a name="map-the-layout-to-the-result-properties"></a>Сопоставление макета со свойствами результатов

Необходимо сопоставить каждое поле макета со свойством Result или свойством Connector, чтобы создать макет результатов JSON.

![Снимок экрана с примером макета на странице конструктора макета поиска с выбранным полем и областью свойств.](media/Verts-SearchLayoutDesigner.png)

Выберите поле в макете, чтобы выделить переменные, которые необходимо сопоставить. Можно использовать несколько переменных для одного поля, и все поля должны быть сопоставлены со свойствами результатов.

## <a name="things-to-consider"></a>Важные факторы

Прежде чем приступить к работе, необходимо выполнить несколько действий, а также не только убедиться, что ваши макеты будут успешными.

### <a name="do"></a>Правильно

- Если вы используете статические ссылки для логотипов, а не свойства результатов, измените шаблон, чтобы предоставить ссылку на логотип в макете.
- Проверка структуры результатов для сценариев, в которых не возвращаются данные для свойства Result, используемого в результирующем JSON. Используйте `$when` условие, чтобы скрыть элемент, если свойство не содержит данных.  
- Убедитесь, что типы данных `$when` условия и свойства результата совпадают. Например, не следует сравнивать `Number` с `Text` `$when` условием.  
- При проектировании структуры результатов следует учитывать требования к теме.  
- Убедитесь, что `Textblock`  элемент может обрабатывать динамическое содержимое. Для этой цели можно `wrap` использовать `maxLines` свойства элемента и.
- Правильно форматировать дату при использовании `{DATE()}` в Markdown.  

### <a name="dont"></a>Неправильно

- При связывании значений не определяйте недопустимые типы данных. Дополнительные сведения о типах данных можно найти в статье [Управление схемой поиска](https://docs.microsoft.com/sharepoint/search/manage-the-search-schema).
- Не обрезайте результат на странице результатов, следуя максимальной высоте в формате JSON. Если вы превысили максимальную высоту макета результатов, результат будет обрезан на странице результатов.
- Не используйте `px` значения в свойствах элементов.

## <a name="resources"></a>Ресурсы

[Настройка страницы результатов поиска](customize-search-page.md)

[Адаптивные карты](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started)

[Язык шаблона "адаптивные карты"](https://docs.microsoft.com/adaptive-cards/templating/language)

[Схема адаптивной карточки](https://adaptivecards.io/explorer/)
