---
title: Расширенная конфигурация DNS
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/19/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MOE150
- MED150
ms.assetid: 47eedbb9-6da9-47e0-aac5-078d34a7fd8f
description: Убедитесь, настроив DNS-сервера с помощью CNAME облегчения работы входа для пользователей
ms.openlocfilehash: fa797b95f346d6d03bd020da146bb330c715e392
ms.sourcegitcommit: 1c038d87efab4840d97b1f367b39e2b9ecdfee4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29612444"
---
# <a name="advanced-dns-configuration"></a><span data-ttu-id="858f2-103">Расширенная конфигурация DNS</span><span class="sxs-lookup"><span data-stu-id="858f2-103">Advanced DNS configuration</span></span>

<span data-ttu-id="858f2-p101">Чтобы обеспечить Bing можно всегда идентификации пользователей в вашей организации и успешно выполнить вход их работы или школы учетную запись, задайте внутренней DNS-сервере или прокси-сервера для разрешения из `www.bing.com` для `ms.bing.com`. Чтобы сделать это, создайте запись DNS для `www.bing.com` быть CNAME для `ms.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="858f2-p101">To ensure Bing can always identify users within your organization and successfully sign them in to their work or school account, configure your internal DNS server or proxy server to resolve from `www.bing.com` to `ms.bing.com`. To do this, create a DNS entry for `www.bing.com` to be a CNAME for `ms.bing.com`.</span></span>
  
****

|<span data-ttu-id="858f2-106">**Имя**</span><span class="sxs-lookup"><span data-stu-id="858f2-106">**Name**</span></span>|<span data-ttu-id="858f2-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="858f2-107">**Type**</span></span>|<span data-ttu-id="858f2-108">**Значение**</span><span class="sxs-lookup"><span data-stu-id="858f2-108">**Value**</span></span>|
|:-----|:-----|:-----|
|`www.bing.com`  <br/> |<span data-ttu-id="858f2-109">CNAME</span><span class="sxs-lookup"><span data-stu-id="858f2-109">CNAME</span></span>  <br/> |`ms.bing.com`  <br/> |
   
<span data-ttu-id="858f2-p102">С помощью CNAME, а не IP-адрес является предпочтительным, поскольку CNAME будет продолжать работать, если IP-адрес изменяется. После выполнения этих изменений DNS результатов будет отображаться для пользователей, как если бы они получены `www.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="858f2-p102">Using a CNAME rather than the IP address is preferred since a CNAME will continue to work if the IP address changes. After you make this DNS change, results will continue to appear to your users as if they are coming from `www.bing.com`.</span></span> 
  
<span data-ttu-id="858f2-p103">Это не требует дополнительной настройки на клиентских компьютерах и обеспечивает удобство работы для пользователей. Когда перейдите к `bing.com`, они будут иметь автоматически входить в несколько постоянно, и если они не может быть подписан автоматически, они будет предложено сделать это.</span><span class="sxs-lookup"><span data-stu-id="858f2-p103">This requires no additional configuration on client machines and provides a seamless experience for your users. When they go to `bing.com`, they'll be automatically signed in more consistently, and if they can't be signed in automatically, they'll be prompted to do so.</span></span>
