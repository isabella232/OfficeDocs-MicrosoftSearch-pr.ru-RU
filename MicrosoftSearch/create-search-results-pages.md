---
title: Создание настраиваемой страницы результатов поиска в SharePoint Online
ms.author: jeffkizn
author: jeffkizn
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
ms.localizationpriority: medium
description: Создайте собственную страницу результатов поиска для сайта SharePoint Online
ms.openlocfilehash: df99287dbdd9a82c1a8bc66b39e67a37fcb22da8
ms.sourcegitcommit: ca5ee826ba4f4bb9b9baabc9ae8a130011c2a3d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2021
ms.locfileid: "59376204"
---
# <a name="create-a-custom-search-results-page-in-sharepoint-online"></a>Создание настраиваемой страницы результатов поиска в SharePoint Online

Один из способов настройки опытом поиска в SharePoint — создать настраиваемую страницу результатов поиска для сайта. Это позволяет использовать созданную страницу, а не по умолчанию на Поиск (Майкрософт) результатов. Это обеспечивает больше гибкости при поиске результатов поиска для пользователей.

>[!NOTE]
> Чтобы внести изменения на страницу Поиск (Майкрософт) результатов, доступную по умолчанию, см. в странице Настройка страницы [результатов поиска.](customize-search-page.md)

На настраиваемой странице результатов можно создать новую страницу, которая может использоваться для управления макетом и оформлением результатов поиска для поддержки потребностей организации. Вы можете использовать все встроенные веб-части, веб-части поиска с открытым исходным кодом из сообщества SharePoint Patterns and Practices, а также любые настраиваемые веб-части, разработанные с помощью SharePoint Framework.

## <a name="configure-a-results-page"></a>Настройка страницы результатов

Чтобы настроить настраиваемую страницу результатов в SharePoint Online, выполните следующие действия:

1. Просмотрите сайт, на котором вы хотите настроить настраиваемую страницу результатов, и перейдите к Параметры > веб-Параметры > **поиска Параметры**.

2. В поисковой Параметры, четкий выбор из использования тех же параметров страницы результатов, что и мой **родитель,** выберите отправку запросов на настраиваемую страницу результатов **и** укайте значение URL-адреса страницы **Results:**. Затем сохраните изменения. URL-адрес, который вы здесь используете, должен быть для страницы, созданной для использования в качестве настраиваемой страницы результатов.

>[!NOTE]
> Страница пользовательских результатов должна быть на том же домене, что и ваш сайт, но не должна быть в одной и той же коллекции сайтов.  

Кроме того, вы можете использовать команду [Set-PnPSearchSettings SharePoint PnP PowerShell,](/powershell/module/sharepoint-pnp/set-pnpsearchsettings?view=sharepoint-ps) чтобы задать значение вместо Параметры страницы Site Параметры.

После набора настраиваемая страница результатов поиска отображается при поиске с помощью Поиск (Майкрософт), которое отображается в панели навигации на верхней части страницы и используется при вводе поиска со страниц сайта или домашней страницы сайта. Он не используется при поиске в списке, библиотеке или на странице содержимого сайта. Вы можете использовать ссылку, чтобы расширить поиск из результатов поиска в списках и библиотеках, чтобы попасть на настраиваемую страницу результатов.

## <a name="change-the-layout-of-your-custom-results-page"></a>Изменение макета страницы пользовательских результатов

Макет страницы с именем **HeaderlessSearchResults** можно использовать, чтобы сделать страницу результатов поиска ближе к нашему опыту результатов поиска. Эта новая схема может быть активна только для страниц, заданной для пользовательской страницы результатов поиска.

Чтобы установить макет страницы, можно использовать команду [Set-PnPClientSidePSharePoint PnP PowerShell](/powershell/module/sharepoint-pnp/set-pnpclientsidepage?view=sharepoint-ps) с командой -LayoutType HeaderlessSearchResults.

## <a name="use-sharepoint-framework-query-extensions"></a>Использование SharePoint Framework расширений запросов

Пользовательские страницы результатов поиска также [](/sharepoint/dev/spfx/building-search-extensions) могут использовать расширение запроса SharePoint Framework для изменения запроса, прежде чем он будет отправлен в поисковую систему.

## <a name="additional-resources"></a>Дополнительные ресурсы

Чтобы узнать больше о настраиваемой странице результатов, ознакомьтесь с нашим сеансом настройки и разработки [Ignite 2019.](https://myignite.techcommunity.microsoft.com/sessions/85238?source=sessions)

Для проектов с открытым исходным кодом, привнося Поиск (Майкрософт) API, а также дополнительные примеры настройки и возможностей, посетите Поиск (Майкрософт) на [GitHub](https://github.com/microsoft-search).