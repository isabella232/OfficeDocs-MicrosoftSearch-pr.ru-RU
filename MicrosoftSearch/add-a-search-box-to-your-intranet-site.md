---
title: Добавить поле поиска на сайте интрасети
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 10/31/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: f980b90f-95e2-4b66-8b21-69f601ff4b50
description: Получайте предложения поиска и поиск результатов рабочих быстрее, добавив поле поиска Microsoft Search в интрасети или страницы.
ms.openlocfilehash: a27b4d79e8795cdd2749c12119709f97710061e7
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "29379221"
---
# <a name="add-a-search-box-to-your-intranet-site"></a>Добавить поле поиска на сайте интрасети

Для быстрого доступа к предложений поиска и результатов рабочих добавьте поле поиска Microsoft Search для любого сайта интрасети или страницы.
  
## <a name="add-a-search-box-to-an-intranet-page"></a>Добавить поле поиска на страницу интрасети

Необходимо добавить два элемента на страницу: контейнер для поля поиска и скрипт, который включает его.
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

Классический сайта SharePoint добавьте веб-часть редактора сценариев и поместите сценарий в нем.
  
## <a name="enable-the-search-box-for-mobile"></a>Включить поле «Поиск» для мобильных устройств

Для сайтов интрасети или страницы, доступные для пользователей мобильных устройств, добавьте isMobile: ИСТИНА объект параметров:
  
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

## <a name="put-focus-on-the-search-box-by-default"></a>Переход на поле поиска по умолчанию

Чтобы помочь пользователям поиск быстрее, если загружает страницу или сайта поместите курсор в поле «Поиск», добавив фокус: ИСТИНА объект параметров:
  
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

## <a name="use-an-iframe-to-embed-a-search-box"></a>Используйте элемент iFrame для внедрения поля поиска

Если внедрение сценария не вариант для сайта, используйте элемент iFrame для добавления поля поиска:
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```
