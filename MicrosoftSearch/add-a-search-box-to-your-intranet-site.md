---
title: Добавление поля поиска на сайте интрасети
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 10/31/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: f980b90f-95e2-4b66-8b21-69f601ff4b50
description: Быстрее получайте релевантные варианты поиска и находите результаты, связанные с работой, добавив поле Поиска (Майкрософт) на сайт или страницу интрасети.
ms.openlocfilehash: 699cfd9c411c9b86f3a2f8742c425aaedef1ebc5
ms.sourcegitcommit: 1c038d87efab4840d97b1f367b39e2b9ecdfee4a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29612420"
---
# <a name="add-a-search-box-to-your-intranet-site"></a>Добавление поля поиска на сайте интрасети

Чтобы обеспечить быстрый доступ к релевантным вариантам поиска и результатам, связанным с работой, добавьте поле Поиска (Майкрософт) на любой сайт или страницу интрасети.
  
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

## <a name="use-an-iframe-to-embed-a-search-box"></a>Внедрение поля поиска с помощью iFrame

Если внедрить скрипт на сайт невозможно, добавьте поле поиска с помощью iFrame:
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```
