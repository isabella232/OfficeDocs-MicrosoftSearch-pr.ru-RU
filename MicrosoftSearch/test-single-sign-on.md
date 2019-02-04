---
title: Тестирование единого входа
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 09/11/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: a220c1bf-7cee-448a-90a3-310284d03e81
description: Уменьшите для пользователей Windows 10 число запросов с предложением войти в Поиск (Майкрософт) и Office 365
ms.openlocfilehash: 55d359edac36020ec8cf2aad6b64ca9737ee1066
ms.sourcegitcommit: 1c038d87efab4840d97b1f367b39e2b9ecdfee4a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29612362"
---
# <a name="test-single-sign-on"></a><span data-ttu-id="ef246-103">Тестирование единого входа</span><span class="sxs-lookup"><span data-stu-id="ef246-103">Test single sign-on</span></span>

<span data-ttu-id="ef246-p101">Единый вход сокращает количество входов для пользователей. Тестирование единого входа в небольшой группе пользователей поможет определить любые проблемы конфигурации, вызывающие блокировку.</span><span class="sxs-lookup"><span data-stu-id="ef246-p101">Single sign-on reduces the number of times users are prompted to sign in. Testing single sign-on with a small group of users will help identify any blocking configuration issues.</span></span> 
  
<span data-ttu-id="ef246-106">Для пользователей Chrome в Windows 10 единый вход будет работать, только если в Chrome установлено расширение для входа в AAD и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ef246-106">For Chrome users on Windows 10, single sign-on will only work if the Windows 10 and AAD sign-in extension for Chrome is installed.</span></span> 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a><span data-ttu-id="ef246-107">Скачивание расширения для входа в Windows 10 и AAD, предназначенное для Chrome</span><span class="sxs-lookup"><span data-stu-id="ef246-107">Download the Windows 10 and AAD sign-in extension for Chrome</span></span>

<span data-ttu-id="ef246-108">Рекомендуется создать групповую политику, чтобы автоматически установить это расширение.</span><span class="sxs-lookup"><span data-stu-id="ef246-108">We recommend that you create a group policy to automatically install this extension.</span></span>
  
1. <span data-ttu-id="ef246-109">Перейдите на портал администрирования Поиска (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="ef246-109">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="ef246-110">В области навигации щелкните пункт **Tools** (Средства)</span><span class="sxs-lookup"><span data-stu-id="ef246-110">In the navigation pane, click **ADSI Edit**.</span></span>
    
3. <span data-ttu-id="ef246-111">В списке средств скачайте **Windows 10 and AAD sign-in extension for Chrome** (Расширение для входа в AAD и Windows 10 для Chrome)</span><span class="sxs-lookup"><span data-stu-id="ef246-111">In the Tools list, download the **Windows 10 and AAD sign-in extension for Chrome**</span></span>
    
4. <span data-ttu-id="ef246-112">Предоставьте общий доступ к расширению пользователям Chrome в Windows 10</span><span class="sxs-lookup"><span data-stu-id="ef246-112">Share the extension with Chrome users on Windows 10</span></span>

  

