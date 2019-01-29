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
description: Уменьшите количество раз, когда пользователи Windows 10 запрос на вход на портал Microsoft Search и Office 365
ms.openlocfilehash: 55d359edac36020ec8cf2aad6b64ca9737ee1066
ms.sourcegitcommit: 1c038d87efab4840d97b1f367b39e2b9ecdfee4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29612362"
---
# <a name="test-single-sign-on"></a><span data-ttu-id="52980-103">Тестирование единого входа</span><span class="sxs-lookup"><span data-stu-id="52980-103">Test single sign-on</span></span>

<span data-ttu-id="52980-p101">Единый вход уменьшает количество раз, когда пользователям предлагается выполнить вход. Тестирование единого входа с небольшой группы пользователей будут помогает определить проблемы, блокирующие конфигурации.</span><span class="sxs-lookup"><span data-stu-id="52980-p101">Single sign-on reduces the number of times users are prompted to sign in. Testing single sign-on with a small group of users will help identify any blocking configuration issues.</span></span> 
  
<span data-ttu-id="52980-106">Для пользователей, Chrome на Windows 10 единого входа будет работать только в случае установки на Windows 10 и AAD входа расширение Chrome.</span><span class="sxs-lookup"><span data-stu-id="52980-106">For Chrome users on Windows 10, single sign-on will only work if the Windows 10 and AAD sign-in extension for Chrome is installed.</span></span> 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a><span data-ttu-id="52980-107">Загрузите Windows 10 и AAD расширение входа для Chrome</span><span class="sxs-lookup"><span data-stu-id="52980-107">Download the Windows 10 and AAD sign-in extension for Chrome</span></span>

<span data-ttu-id="52980-108">Рекомендуется создать групповой политики, чтобы автоматически установить это расширение.</span><span class="sxs-lookup"><span data-stu-id="52980-108">We recommend that you create a group policy to automatically install this extension.</span></span>
  
1. <span data-ttu-id="52980-109">Перейти на портал администрирования поиска Microsoft</span><span class="sxs-lookup"><span data-stu-id="52980-109">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="52980-110">На левой панели навигации откройте меню **Сервис**</span><span class="sxs-lookup"><span data-stu-id="52980-110">In the navigation pane, click **Tools**</span></span>
    
3. <span data-ttu-id="52980-111">В списке средств Загрузите **Windows 10 и AAD входа расширения для Chrome**</span><span class="sxs-lookup"><span data-stu-id="52980-111">In the Tools list, download the **Windows 10 and AAD sign-in extension for Chrome**</span></span>
    
4. <span data-ttu-id="52980-112">Совместно использовать данное расширение имени файла с пользователями хрома на Windows 10</span><span class="sxs-lookup"><span data-stu-id="52980-112">Share the extension with Chrome users on Windows 10</span></span>

  

