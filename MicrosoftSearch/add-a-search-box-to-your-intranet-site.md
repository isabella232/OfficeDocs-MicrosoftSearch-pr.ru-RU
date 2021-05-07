---
title: Добавление поля поиска на сайте интрасети
ms.author: dawholl
author: dawholl
manager: kellis
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: f980b90f-95e2-4b66-8b21-69f601ff4b50
ROBOTS: NoIndex
description: Получите соответствующие предложения по поиску и быстрее найдите результаты работы, добавив поле поиска Майкрософт на сайт или страницу интрасети.
ms.openlocfilehash: c71f61971bf69c2eaa5fb7a48d0cb3d26af0ad07
ms.sourcegitcommit: 5f0a8bdf274d02132a3b5211fb4738eb38d159db
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2021
ms.locfileid: "52247768"
---
# <a name="add-a-search-box-to-your-intranet-site"></a>Добавление поля поиска на сайте интрасети

Чтобы предоставить пользователям легкий доступ к результатам организации, добавьте в поле поиска microsoft Search Bing на любой сайт или страницу интрасети. Вот некоторые из преимуществ:

- Поле поиска на портале SharePoint или интрасети предоставляет знакомую и доверяемую точку входа для начала поиска
- Поддерживает все основные веб-браузеры, включая Google Chrome и Microsoft Edge
- Отображаются только предложения поиска из организации, веб-предложения никогда не включаются
- Принимает пользователей на страницу Microsoft Search в Bing результатов работы, которая исключает рекламу и веб-результаты
- Вы контролируете внешний вид и поведение окна поиска, включая возможность посадки пользователей по умолчанию по вертикали или созданной вами настраиваемой вертикали.
  
## <a name="add-a-search-box-to-an-intranet-page"></a>Добавление поля поиска на странице интрасети

Нужно добавить на страницу два элемента: контейнер для поля поиска и скрипт, который его запустит.
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

На классическом сайте SharePoint добавьте веб-часть редактора скриптов и вставьте в нее этот скрипт.
  
## <a name="enable-the-search-box-for-mobile"></a>Включение поля поиска для мобильных устройств

Для сайтов и страниц интрасети, которые доступны пользователям мобильных устройств, добавьте в объект параметров строку "isMobile: true":
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox", 
        isMobile: true
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="put-focus-on-the-search-box-by-default"></a>Установка фокуса в поле поиска по умолчанию

Чтобы пользователи быстрее находили нужную информацию, установите курсор в поле поиска, когда страница или сайт загружается. Для этого добавьте в объект параметров строку "focus: true":
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox",
        focus: true
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="customize-the-appearance-of-the-search-box"></a>Настройка внешнего вида поля поиска 

Чтобы поле поиска лучше подходило стилю вашей интрасети, можно использовать различные параметры настройки. Комбинируйте параметры в соответствии со своими потребностями.

```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox",
        width: 560,                             // default: 560, min: 360, max: 650
        height: 40,                             // default: 40, min: 40, max: 72
        cornerRadius: 6,                        // default: 6, min: 0, max: 25                                   
        strokeOutline: true,                    // default: true
        dropShadow: true,                       // default: false
        iconColor: "#067FA6",                   // default: #067FA6
        title: "Search box",                    // default: "Search box"
        vertical: "Person-people",              // default: not specified, search box directs to the All vertical on the WORK results page
        companyNameInGhostText: "Contoso"       // default: not specified
                                                // when absent, ghost text will be "Search work"
                                                // when specified, text will be "Search <companyNameInGhostText>"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="direct-users-to-a-default-or-custom-vertical"></a>Перенаправляем пользователей на вертикаль по умолчанию или настраиваемую

Чтобы обеспечить простую интеграцию между бизнес-приложениями или сайтами интрасети и результатами работы, вы также можете настроить поле поиска, указав по умолчанию или настраиваемую вертикаль, на которую пользователи должны приземлиться при нажатии предложения поиска.

Для определения нужной вертикали используйте вертикальный параметр в bfbSearchBoxConfig. Например, если вы хотите, чтобы пользователи всегда приземлялись на вертикали Сайтов, одной из вертикали по умолчанию, используйте значение "Site-sites".

![Снимок экрана страницы результатов работы в Microsoft Search в Bing с указанием вертикальных результатов сайтов и URL-адреса](media/sites-vertical-esb.png)

Для настраиваемой вертикали используйте hash в конце URL-адреса. Эти значения можно найти с помощью поиска на странице Bing, нажав вертикальную метку и скопив значение после знака номера (#).

![Снимок экрана страницы результатов работы в Microsoft Search в Bing с пользовательскими вертикальными результатами презентации и URL-адресом](media/custom-vertical-esb.png)

## <a name="use-an-iframe-to-embed-a-search-box"></a>Внедрение поля поиска с помощью iFrame

Если внедрить скрипт на сайт невозможно, добавьте поле поиска с помощью iFrame. Вы не сможете настроить поле поиска.
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```

## <a name="inprivate-mode-and-conditional-access"></a>Режим InPrivate и условный доступ

Встроенное поле поиска будет отключено, если страница или сайт будут открыты в окне InPrivate. Кроме того, с поддержкой условного доступа Azure AD в Microsoft Edge, Bing.com не поддерживает вход AAD при использовании режима InPrivate. Дополнительные сведения об условном доступе в Edge [см. в Microsoft Edge и условном доступе.](https://docs.microsoft.com/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge) 