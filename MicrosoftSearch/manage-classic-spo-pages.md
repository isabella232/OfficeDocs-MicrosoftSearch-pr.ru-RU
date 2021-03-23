---
title: Классические страницы в SharePoint Online и Microsoft Search
ms.author: keremy
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Использование microsoft Search на классических страницах SharePoint
ms.openlocfilehash: 33215c730d34c14f8ce1d55e93730615688f1e2a
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031434"
---
# <a name="classic-pages-and-microsoft-search"></a>Классические страницы и microsoft Search

Сайты SharePoint, созданные до современных сайтов, используют классическое поле поиска и классические результаты поиска. Мы будем развертывать функцию, которая будет по умолчанию классические страницы, чтобы начать использовать современный опыт поиска, который использует Microsoft Search, который обеспечивает персонализированные результаты с более высокой релевантности.

Использование Microsoft Search рекомендуется для всех сайтов, в том числе классических, но если на классических сайтах используются настраиваемые мастер-страницы и/или вы настраивали классический опыт результатов поиска, мы автоматически обнаруживаем эти настройки и не переключаемся на Microsoft Search.

## <a name="classic-sites-that-will-automatically-switch-to-microsoft-search"></a>Классические сайты, которые автоматически переключаются на Microsoft Search

Классические сайты начнут использовать Microsoft Search, если все эти сайты верны:

* Сайт основан на шаблоне сайта группы (например, STS#0 и STS#1).
* На сайте не включена функция публикации.
* На сайте не используется настраиваемая мастер-страница (другая мастер-страница, чем oslo.master или seattle.master).
* Нет никаких правил активного запроса, кроме правил добавления продвигаемого результата для сайта, коллекции сайтов или клиента в источнике результатов по умолчанию.
* В источнике результатов по умолчанию не существует пользовательских типов результатов для сайта или коллекции сайтов.
* Сайт или коллекция сайтов не отключались от коммутатора с помощью *параметра SearchBoxInNavBar,* описанного ниже.

После перехода на Microsoft Search классические страницы на сайте начнут показывать поле поиска в панели навигации пакета и удалять классическое поле поиска со страницы. Затем, когда пользователь ищет термин, результаты будут отображаться с помощью современного интерфейса поиска Microsoft Search.

## <a name="staying-with-the-classic-search-experience"></a>Пребывание с классическим опытом поиска

Если ваш сайт соответствует перечисленным выше критериям, но вы не хотите, чтобы он переключился на службу поиска Майкрософт, вы можете отказаться от использования следующих команд, как владелец сайта или коллекции сайтов.

Вы можете использовать эту команду в любое время, до или после того, как произойдет переключатель, поэтому легко вернуться к опыту поиска, который был ранее.

Для запуска команд ниже вы будете использовать PowerShell с расширениями SharePoint PnP PowerShell. Вы можете установить и узнать больше о том, как начать [работу здесь](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps). Вы вопишитесь на свой сайт или коллекцию сайтов с помощью этой команды:

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign in to your site. Use the site owner credentials.
```

Чтобы остаться с классическим опытом поиска для сайта, запустите следующую команду:

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

Кроме того, если вы хотите установить его для всех сайтов в коллекции сайтов, вы можете использовать эту команду:

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

## <a name="opting-into-microsoft-search"></a>Выбор в Microsoft Search

Для тех сайтов, которые не соответствуют перечисленным выше критериям, или для определенных сайтов в коллекции сайтов, которые решили остаться в классическом режиме, вы можете вручную включить функцию Microsoft Search.

Чтобы изменить этот параметр для определенного сайта, можно использовать эту команду:

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

Если вы хотите установить его для всех сайтов в коллекции сайтов, вы можете использовать эту команду:

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

> [!NOTE]
> Можно вручную включить Microsoft Search только для сайта группы или сайта публикации (коды шаблонов, содержащие "STS", "CMSPUBLISHING", "BLANKINTERNET" и "GROUP").