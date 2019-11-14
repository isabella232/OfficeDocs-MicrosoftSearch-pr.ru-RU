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
# <a name="advanced-dns-configuration"></a><span data-ttu-id="68a7f-103">Расширенная конфигурация DNS</span><span class="sxs-lookup"><span data-stu-id="68a7f-103">Advanced DNS configuration</span></span>

<span data-ttu-id="68a7f-p101">Чтобы система Bing всегда могла определять пользователей в организации и успешно выполнять их вход в рабочую или учебную учетную запись, настройте внутренний DNS-сервер или прокси-сервер для сопоставления `www.bing.com` с `ms.bing.com`. Для этого создайте запись DNS для `www.bing.com`, являющуюся CNAME для `ms.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="68a7f-p101">To ensure Bing can always identify users within your organization and successfully sign them in to their work or school account, configure your internal DNS server or proxy server to resolve from `www.bing.com` to `ms.bing.com`. To do this, create a DNS entry for `www.bing.com` to be a CNAME for `ms.bing.com`.</span></span>
  
****

|<span data-ttu-id="68a7f-106">**Имя**</span><span class="sxs-lookup"><span data-stu-id="68a7f-106">**Name**</span></span>|<span data-ttu-id="68a7f-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="68a7f-107">**Type**</span></span>|<span data-ttu-id="68a7f-108">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68a7f-108">**Value**</span></span>|
|:-----|:-----|:-----|
|`www.bing.com`  <br/> |<span data-ttu-id="68a7f-109">CNAME</span><span class="sxs-lookup"><span data-stu-id="68a7f-109">CNAME</span></span>  <br/> |`ms.bing.com`  <br/> |
   
<span data-ttu-id="68a7f-p102">Предпочтительно использование CNAME, а не IP-адреса, так как CNAME продолжит работать при изменении IP-адреса. После внесения этого изменения в DNS результаты будут продолжать отображаться для пользователей так же, как при получении из `www.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="68a7f-p102">Using a CNAME rather than the IP address is preferred since a CNAME will continue to work if the IP address changes. After you make this DNS change, results will continue to appear to your users as if they are coming from `www.bing.com`.</span></span> 
  
<span data-ttu-id="68a7f-p103">Для этого не требуется дополнительная настройка на клиентских компьютерах, при этом обеспечивается бесперебойная работа для пользователей. При переходе к `bing.com` постоянный вход будет выполняться автоматически, а если автоматический вход невозможен, пользователям будет предложено выполнить его.</span><span class="sxs-lookup"><span data-stu-id="68a7f-p103">This requires no additional configuration on client machines and provides a seamless experience for your users. When they go to `bing.com`, they'll be automatically signed in more consistently, and if they can't be signed in automatically, they'll be prompted to do so.</span></span>
