---
title: Тестирование единого входа
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
ms.assetid: a220c1bf-7cee-448a-90a3-310284d03e81
description: Уменьшите для пользователей Windows 10 число запросов с предложением войти в Поиск (Майкрософт) и Office 365
ms.openlocfilehash: 9fa7e067a5d72b7044981491f8526e6de727cfae
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626894"
---
# <a name="test-single-sign-on"></a><span data-ttu-id="cd65c-103">Тестирование единого входа</span><span class="sxs-lookup"><span data-stu-id="cd65c-103">Test single sign-on</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd65c-104">Эта статья относится к порталу администрирования Поиска (Майкрософт) в Bing.</span><span class="sxs-lookup"><span data-stu-id="cd65c-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="cd65c-105">Мы переносим портал в Центр администрирования Microsoft 365, после чего портал Поиска (Майкрософт) в Bing будет удален.</span><span class="sxs-lookup"><span data-stu-id="cd65c-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="cd65c-106">Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cd65c-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="cd65c-107">[Обзор Поиска (Майкрософт)](overview-microsoft-search.md).</span><span class="sxs-lookup"><span data-stu-id="cd65c-107">[Overview of Microsoft Search](overview-microsoft-search.md).</span></span>
    
<span data-ttu-id="cd65c-p102">Единый вход сокращает количество входов для пользователей. Тестирование единого входа в небольшой группе пользователей поможет определить любые проблемы конфигурации, вызывающие блокировку.</span><span class="sxs-lookup"><span data-stu-id="cd65c-p102">Single sign-on reduces the number of times users are prompted to sign in. Testing single sign-on with a small group of users will help identify any blocking configuration issues.</span></span> 
  
<span data-ttu-id="cd65c-110">Для пользователей Chrome в Windows 10 единый вход будет работать, только если в Chrome установлено расширение для входа в AAD и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cd65c-110">For Chrome users on Windows 10, single sign-on will only work if the Windows 10 and AAD sign-in extension for Chrome is installed.</span></span> 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a><span data-ttu-id="cd65c-111">Скачивание расширения для входа в Windows 10 и AAD, предназначенное для Chrome</span><span class="sxs-lookup"><span data-stu-id="cd65c-111">Download the Windows 10 and AAD sign-in extension for Chrome</span></span>

<span data-ttu-id="cd65c-112">Рекомендуется создать групповую политику, чтобы автоматически установить это расширение.</span><span class="sxs-lookup"><span data-stu-id="cd65c-112">We recommend that you create a group policy to automatically install this extension.</span></span>
  
1. <span data-ttu-id="cd65c-113">Перейдите на портал администрирования Поиска (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="cd65c-113">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="cd65c-114">В области навигации щелкните пункт **Tools** (Средства)</span><span class="sxs-lookup"><span data-stu-id="cd65c-114">In the navigation pane, click **Tools**</span></span>
    
3. <span data-ttu-id="cd65c-115">В списке средств скачайте **Windows 10 and AAD sign-in extension for Chrome** (Расширение для входа в AAD и Windows 10 для Chrome)</span><span class="sxs-lookup"><span data-stu-id="cd65c-115">In the Tools list, download the **Windows 10 and AAD sign-in extension for Chrome**</span></span>
    
4. <span data-ttu-id="cd65c-116">Предоставьте общий доступ к расширению пользователям Chrome в Windows 10</span><span class="sxs-lookup"><span data-stu-id="cd65c-116">Share the extension with Chrome users on Windows 10</span></span>

  

