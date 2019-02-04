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
# <a name="test-single-sign-on"></a>Тестирование единого входа

Единый вход сокращает количество входов для пользователей. Тестирование единого входа в небольшой группе пользователей поможет определить любые проблемы конфигурации, вызывающие блокировку. 
  
Для пользователей Chrome в Windows 10 единый вход будет работать, только если в Chrome установлено расширение для входа в AAD и Windows 10. 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a>Скачивание расширения для входа в Windows 10 и AAD, предназначенное для Chrome

Рекомендуется создать групповую политику, чтобы автоматически установить это расширение.
  
1. Перейдите на портал администрирования Поиска (Майкрософт)
    
2. В области навигации щелкните пункт **Tools** (Средства)
    
3. В списке средств скачайте **Windows 10 and AAD sign-in extension for Chrome** (Расширение для входа в AAD и Windows 10 для Chrome)
    
4. Предоставьте общий доступ к расширению пользователям Chrome в Windows 10

  

