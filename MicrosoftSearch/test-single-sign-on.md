---
title: Тестирование единого входа
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 09/11/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: a220c1bf-7cee-448a-90a3-310284d03e81
description: Уменьшите количество раз, когда пользователи Windows 10 запрос на вход на портал Microsoft Search и Office 365
ms.openlocfilehash: 4157707d58ead304449805c8fd16578690ac01a6
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "29379220"
---
# <a name="test-single-sign-on"></a><span data-ttu-id="27b78-103">Тестирование единого входа</span><span class="sxs-lookup"><span data-stu-id="27b78-103">Test single sign-on</span></span>

<span data-ttu-id="27b78-p101">Единый вход уменьшает количество раз, когда пользователям предлагается выполнить вход. Тестирование единого входа с небольшой группы пользователей будут помогает определить проблемы, блокирующие конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27b78-p101">Single sign-on reduces the number of times users are prompted to sign in. Testing single sign-on with a small group of users will help identify any blocking configuration issues.</span></span> 
  
<span data-ttu-id="27b78-106">Для пользователей, Chrome на Windows 10 единого входа будет работать только в случае установки на Windows 10 и AAD входа расширение Chrome.</span><span class="sxs-lookup"><span data-stu-id="27b78-106">For Chrome users on Windows 10, single sign-on will only work if the Windows 10 and AAD sign-in extension for Chrome is installed.</span></span> 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a><span data-ttu-id="27b78-107">Загрузите Windows 10 и AAD расширение входа для Chrome</span><span class="sxs-lookup"><span data-stu-id="27b78-107">Download the Windows 10 and AAD sign-in extension for Chrome</span></span>

<span data-ttu-id="27b78-108">Рекомендуется создать групповой политики, чтобы автоматически установить это расширение.</span><span class="sxs-lookup"><span data-stu-id="27b78-108">We recommend that you create a group policy to automatically install this extension.</span></span>
  
1. <span data-ttu-id="27b78-109">Перейти на портал администрирования поиска Microsoft</span><span class="sxs-lookup"><span data-stu-id="27b78-109">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="27b78-110">На левой панели навигации откройте меню **Сервис**</span><span class="sxs-lookup"><span data-stu-id="27b78-110">In the navigation pane, click **Tools**</span></span>
    
3. <span data-ttu-id="27b78-111">В списке средств Загрузите **Windows 10 и AAD входа расширения для Chrome**</span><span class="sxs-lookup"><span data-stu-id="27b78-111">In the Tools list, download the **Windows 10 and AAD sign-in extension for Chrome**</span></span>
    
4. <span data-ttu-id="27b78-112">Совместно использовать данное расширение имени файла с пользователями хрома на Windows 10</span><span class="sxs-lookup"><span data-stu-id="27b78-112">Share the extension with Chrome users on Windows 10</span></span>

  

