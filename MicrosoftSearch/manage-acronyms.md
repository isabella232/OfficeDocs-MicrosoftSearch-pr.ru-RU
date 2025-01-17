---
title: Управление ответами по аббревиатуре в Поиск (Майкрософт)
ms.author: rakkum
author: rakeshMSFT
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
ms.localizationpriority: medium
search.appverid:
- BFB160
- MET150
- MOE150
description: Создание и обновление ответов на аббревиатуры в Поиск (Майкрософт)
ms.openlocfilehash: b7b3272ba98bbce7d43562811389df0a35e9f7a2
ms.sourcegitcommit: ca5ee826ba4f4bb9b9baabc9ae8a130011c2a3d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2021
ms.locfileid: "59376104"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a>Управление ответами на аббревиатуры в Поиск (Майкрософт)

Пользователи часто используют незнакомые аббревиатуры и аббревиатуры, используемые их организацией или командой. Термины, специфические для организаций или групп, могут быть новыми для людей, которые переходят из одной группы в другую, работают с внутренними группами партнеров или являются новыми для организации.

Организации не всегда имеют одну ссылку на стандартную терминологию. Отсутствие единой ссылки затрудняет поиск определений для этих аббревиатур. Поиск (Майкрософт) решает эту проблему с помощью аббревиатур.

## <a name="what-users-experience"></a>Что пользователи испытывают

Поиск (Майкрософт) пользователи могут получать определения с акронимами в [Bing,](https://Bing.com) [SharePoint,](https://products.office.com/sharepoint/collaboration) [Office 365,](https://Office.com)Outlook в Интернете, Outlook Mobile (Android) и Teams Mobile (iOS и Android). В поле **Поиск** пользователи введите запросы, подобные этим примерам:

- *Что такое* DNN
- *Определение* DNN
- Определение *DNN*
- *Расширение* DNN
- Расширение *DNN*
- *Значение* DNN
- DNN *означает*
- DNN *означает*

Результат включает все значения DNN, присутствующие в организации пользователя.

> [!NOTE]
> Пользователи должны ввести запрос, который включает указанные  ключевые слова аббревиатуры, чтобы вызвать соответствующие ответы. Запросы аббревиатуры не являются конфиденциальными.

## <a name="set-up-acronyms-answers"></a>Настройка ответов на аббревиатуры

В [Центр администрирования Microsoft 365](https://admin.microsoft.com)перейдите к [](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)аббревиатурам, а затем выберите **Добавить аббревиатура**.

Поиск (Майкрософт) запрашивает два источника данных для предоставления ответов на запросы пользователей по аббревиатуре:

1. **Администрирование.** Предоставляется ИТ-администраторами в [центре администрирования.](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)
2. **System-curated**. Обнаружено Поиск (Майкрософт) электронной почты и документов пользователей, а также общедоступных данных в организации.

### <a name="set-up-admin-curated-acronyms"></a>Настройка акронимов, курированных администратором

Администраторы поиска могут добавлять аббревиатуры на вкладке [Acronyms](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) в центре [администрирования Поиск (Майкрософт).](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch) В центр администрирования можно добавить аббревиатуры из любого внутреннего сайта или репозитория. Эти аббревиатуры можно добавить в **состояние Published** или **Draft:**

**Опубликовано состояние**. Аббревиатуры доступны пользователям организации через Поиск (Майкрософт).

> [!NOTE]
> Акронимы, добавленные в состояние Published, становятся доступными в Поиск (Майкрософт).

**Состояние Черновика.** Если вы хотите просмотреть аббревиатура, прежде чем сделать ее доступной в Поиск (Майкрософт), можно добавить аббревиатура в состояние Draft. Акронимы в состоянии Draft не отображаются в результатах поиска. Чтобы она появлялась в результатах поиска, необходимо переместить аббревиатура в состояние Published.

**Исключено состояние**. Если вы хотите, чтобы аббревиатура не появлялись в Поиск (Майкрософт), используйте исключение аббревиатуры, **чтобы** добавить ее. Чтобы исключить аббревиатура, необходимо удалить исключенную аббревиатуру и добавить ее или проверить, есть ли она в опубликованном списке.

Вы можете добавлять аббревиатуры по отдельности или массово импортировать их в CSV-файл. Upload CSV-файл с полями, показанными в следующей таблице:

| Аббревиатура (Обязательно) | Стойки для (обязательный) | Url | Описание  | Состояние (обязательное) | Последние изменения | Последнее изменение путем | Id |
| --------- | --------- | --------- | ---------- | --------- |--------- |--------- |--------- |
| *XXX* | *Написанная аббревиатура* | *Source* |  | *Опубликовано, черновик или исключено* |  |  |  |

### <a name="csv-fields"></a>Поля CSV

**Аббревиатура**. Содержит фактическую короткую форму или аббревиатура. Пример *DNN*.

**Выступает за**. Содержит определение аббревиатуры. Пример — *глубокая нейронная сеть.*

**Описание**. Краткое описание аббревиатуры, которая предоставляет пользователям дополнительные сведения о аббревиатуре и ее определении. Например, *глубокая нейронная* сеть — это нейронная сеть с определенным уровнем сложности, нейронная сеть с более чем двумя слоями.

**Источник** URL-адрес страницы или веб-сайта, на котором вы хотите, чтобы пользователи могли получить дополнительные сведения о аббревиатуре.

**Состояние**. Это поле может принимать два значения:

- **Проект**. Добавляет аббревиатура в состояние Draft.
- **Опубликовано**. Добавляет аббревиатура в состояние Published и делает ее доступной в Поиск (Майкрософт).
- **Исключено**. Добавляет аббревиатура в состояние Исключено и не позволяет ему отображаться в Поиск (Майкрософт).

### <a name="system-curated-acronyms"></a>Аббревиатуры с системной системой

Администраторам может потребоваться добавить все аббревиатуры, используемые в организации, в Answers. Эта функция может найти аббревиатуры, о которых администраторы поиска даже не знают. Чтобы сделать эту работу, Поиск (Майкрософт) также обнаруживает и курирует аббревиатуры из этих источников:

- Сообщения электронной почты пользователей
- Документы в [SharePoint,](https://products.office.com/sharepoint/collaboration) [Microsoft OneDrive]( https://onedrive.live.com/about/)и [Microsoft OneNote](https://www.onenote.com/)
- Общедоступные документы в организации, к SharePoint, OneDrive или OneNote

Поиск (Майкрософт), чтобы только пользователи с доступом и разрешениями к документу могли видеть аббревиатуры, обнаруженные в нем. При обнаружении аббревиатуры в почтовом ящике пользователя только этот пользователь может увидеть эту аббревиатуру.

> [!NOTE]
> Для системных аббревиатур не требуется установка.

## <a name="frequently-asked-questions"></a>Вопросы и ответы

**В. Как ранжировать данные, курированные администратором и системными данными?**

**A:** Ранжирование результатов может отличаться от человека к человеку, так как результаты персонализированы для каждого пользователя. Ни одна из этих категорий не всегда будет иметь приоритет над другой.

**Вопрос: Как пользователи вызывают ответы на аббревиатуры?**

**A:** Чтобы получить ответы на аббревиатуры, пользователи должны ввести определенные шаблоны запросов в поле поиска [Bing,](https://bing.com) [SharePoint,](https://products.office.com/sharepoint/collaboration) [Office 365,](https://Office.com)Outlook в Интернете, Outlook Mobile (Android)  или Teams Mobile (iOS и Android).

**В. Могут ли пользователи вводить только аббревиатура при поиске?**

**A:** В Bing теперь пользователи могут находить ответы на аббревиатуру только путем поиска аббревиатуры, ключевое слово больше не требуется. Этот же опыт будет включен для других точек Поиск (Майкрософт) на этапах.

**В. Сколько времени необходимо, чтобы аббревиатуры, курированные администратором, были видны в Поиск (Майкрософт) после их публикации?**

**A:** Акронимы, добавленные в состояние Published, становятся доступными в Поиск (Майкрософт).

**Вопрос: Сколько времени займет от появления аббревиатур с системной системой после получения или отправки нового сообщения электронной почты или документа?**

**A:** Аббревиатуры, найденные в новой электронной почте или документе, могут отображаться в Поиск (Майкрософт) течение семи дней.

**В. Что происходит, если аббревиатура исключена и опубликована?**

**A:** Исключенная аббревиатура имеет приоритет и не позволяет опубликованной аббревиатуре появляться в результатах поиска. Он не удаляет и не удаляет опубликованную аббревиатуру.

**В. Сколько времени требуется для исключения аббревиатуры из Поиск (Майкрософт) результатов?**

**A:** Для остановки появления исключенной аббревиатуры в результатах поиска требуется до дня.

**В. Для системных аббревиатур документы должны быть в определенном формате?**

**A:** Нет. Мы поддерживаем все типы файлов, кроме изображений, папок и почтовых файлов.

**Вопрос: Будет ли Корпорация Майкрософт открывать аббревиатуры из документов на всех языках?**

**A:** Корпорация Майкрософт поддерживает только системные аббревиатуры из документов на английском, испанском, французском, итальянском, немецком и португальском языках. Поддержка других языков будет добавляться поэтапно.

**В. Что делать, если моя организация не хочет показывать аббревиатуры с системной системой? Можно ли перестать показывать этот тип аббревиатуры в результатах поиска?**

**A:** Чтобы отключить отображение системных аббревиатур в результатах поиска, создайте билет на поддержку клиентов, следуя инструкциям в службе поддержки [контактов для бизнес-продуктов.](/microsoft-365/admin/contact-support-for-business-products)
После создания билета поддержки для остановки появления в результатах поиска аббревиатуры с системной поддержкой требуется до 48 часов.
