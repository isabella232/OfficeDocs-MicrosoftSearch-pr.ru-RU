---
title: Расширенная конфигурация DNS
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/19/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MOE150
- MED150
ms.assetid: 47eedbb9-6da9-47e0-aac5-078d34a7fd8f
ROBOTS: NoIndex
description: Обеспечьте удобную возможность входа для пользователей путем настройки DNS-сервера с помощью CNAME
ms.openlocfilehash: 062c43cfbc8d25c263eb2402bd05191e385411b2
ms.sourcegitcommit: 6b531b2ce7253c16251c7089795dedf1d2f3fc33
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2019
ms.locfileid: "38311826"
---
# <a name="advanced-dns-configuration"></a>Расширенная конфигурация DNS

Чтобы система Bing всегда могла определять пользователей в организации и успешно выполнять их вход в рабочую или учебную учетную запись, настройте внутренний DNS-сервер или прокси-сервер для сопоставления `www.bing.com` с `ms.bing.com`. Для этого создайте запись DNS для `www.bing.com`, являющуюся CNAME для `ms.bing.com`.
  
****

|**Имя**|**Тип**|**Значение**|
|:-----|:-----|:-----|
|`www.bing.com`  <br/> |CNAME  <br/> |`ms.bing.com`  <br/> |
   
Предпочтительно использование CNAME, а не IP-адреса, так как CNAME продолжит работать при изменении IP-адреса. После внесения этого изменения в DNS результаты будут продолжать отображаться для пользователей так же, как при получении из `www.bing.com`. 
  
Для этого не требуется дополнительная настройка на клиентских компьютерах, при этом обеспечивается бесперебойная работа для пользователей. При переходе к `bing.com` постоянный вход будет выполняться автоматически, а если автоматический вход невозможен, пользователям будет предложено выполнить его.
