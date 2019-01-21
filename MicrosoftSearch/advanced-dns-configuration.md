---
title: Дополнительная настройка DNS
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
description: Убедитесь, настроив DNS-сервера с помощью CNAME облегчения работы входа для пользователей
ms.openlocfilehash: f08fc4c29c4c4356a1616faab67fdebdd6c85839
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "29379148"
---
# <a name="advanced-dns-configuration"></a>Дополнительная настройка DNS

Чтобы обеспечить Bing можно всегда идентификации пользователей в вашей организации и успешно выполнить вход их работы или школы учетную запись, задайте внутренней DNS-сервере или прокси-сервера для разрешения из `www.bing.com` для `ms.bing.com`. Чтобы сделать это, создайте запись DNS для `www.bing.com` быть CNAME для `ms.bing.com`.
  
****

|**Имя**|**Тип**|**Значение**|
|:-----|:-----|:-----|
|`www.bing.com`  <br/> |CNAME  <br/> |`ms.bing.com`  <br/> |
   
С помощью CNAME, а не IP-адрес является предпочтительным, поскольку CNAME будет продолжать работать, если IP-адрес изменяется. После выполнения этих изменений DNS результатов будет отображаться для пользователей, как если бы они получены `www.bing.com`. 
  
Это не требует дополнительной настройки на клиентских компьютерах и обеспечивает удобство работы для пользователей. Когда перейдите к `bing.com`, они будут иметь автоматически входить в несколько постоянно, и если они не может быть подписан автоматически, они будет предложено сделать это.
