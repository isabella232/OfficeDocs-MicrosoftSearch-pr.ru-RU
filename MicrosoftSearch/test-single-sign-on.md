---
title: Тестирование единого входа
ms.author: dawholl
author: dawholl
manager: kellis
ms.audience: Admin
ms.topic: article
ms.service: mssearch
ms.localizationpriority: medium
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: a220c1bf-7cee-448a-90a3-310284d03e81
description: Уменьшите для пользователей Windows 10 число запросов с предложением войти в Поиск (Майкрософт) и Office 365
ms.openlocfilehash: ab4e9c8c3fc8f89abf60c9aa09671105e7c40451
ms.sourcegitcommit: cc9d743bcf5e998720ce9cd6eefb4061d913dc65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2021
ms.locfileid: "58701420"
---
# <a name="test-single-sign-on"></a>Тестирование единого входа

> [!IMPORTANT]
> Эта статья относится к порталу администрирования Поиска (Майкрософт) в Bing. Мы переносим портал в Центр администрирования Microsoft 365, после чего портал Поиска (Майкрософт) в Bing будет удален. Чтобы приступить к работе, рекомендуется использовать Центр администрирования Microsoft 365. [Обзор Поиска (Майкрософт)](overview-microsoft-search.md).
    
Единый вход сокращает количество входов для пользователей. Тестирование единого входа в небольшой группе пользователей поможет определить любые проблемы конфигурации, вызывающие блокировку. 
  
Для пользователей Chrome в Windows 10 единый вход будет работать, только если в Chrome установлено расширение для входа в AAD и Windows 10. 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a>Скачивание расширения для входа в Windows 10 и AAD, предназначенное для Chrome

Рекомендуется создать групповую политику, чтобы автоматически установить это расширение.
  
1. Перейдите на портал администрирования Поиска (Майкрософт)
    
2. В области навигации щелкните пункт **Tools** (Средства)
    
3. В списке средств скачайте **Windows 10 and AAD sign-in extension for Chrome** (Расширение для входа в AAD и Windows 10 для Chrome)
    
4. Предоставьте общий доступ к расширению пользователям Chrome в Windows 10

  

