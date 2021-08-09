---
title: Соедините Graph для Поиск (Майкрософт)
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NoIndex
description: Настройка соединитетеля Graph файла для Поиск (Майкрософт)
ms.openlocfilehash: af4c3996fdc8ac753404f4b4519175a9054fa18bce3862b0c5841c7bd5369cdd
ms.sourcegitcommit: 71ac2a38971ca4452d1bddfc773ff8f45e1ffd77
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "54533030"
---
<!---Previous ms.author: rusamai --->

# <a name="file-share-graph-connector"></a>Соедините Graph файла

Соединители Graph файла позволяют пользователям в организации искать локальное Windows файл.

> [!NOTE]
> Ознакомьтесь [**с статьей Установка Graph,**](configure-connector.md) чтобы понять общий Graph соединители.

## <a name="before-you-get-started"></a>Перед началом работы

### <a name="install-the-graph-connector-agent"></a>Установка агента Graph соединителя

Чтобы индексировать Windows файл, необходимо установить и зарегистрировать агент Graph соединителя. Дополнительные [Graph](graph-connector-agent.md) см. в Graph агенте соединителя.  

### <a name="content-requirements"></a>Требования к контенту

### <a name="file-types"></a>Типы файлов

Содержимое следующих форматов можно индексировать и искать: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTM, TXT, XLB, XLC, XLSB, XLSB, XLSX, XLT, XLXM, XML, XPS, and ZIP. Индексация только текстового контента этих форматов. Все мультимедийные материалы игнорируются. Для любого файла, который не относится к этому формату, индексация только метаданных.

### <a name="file-size-limits"></a>Ограничения на размер файлов

Максимальный размер поддерживаемых файлов — 100 МБ. Файлы, которые превышают 100 МБ, не индексироваться. Максимальное ограничение размера после обработки — 4 МБ. Обработка прекращается, когда размер файла достигает 4 МБ. Поэтому некоторые фразы, присутствующие в файле, могут не работать для поиска.

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в Центр администрирования Microsoft 365

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

На странице **Подключение** для источника данных  выберите файл и укай имя, код подключения и описание. На следующей странице укажете путь к файлу и выберите ранее установленный агент Graph соединители. Введите учетные данные для [учетной](https://microsoft.com/windows) записи Windows Microsoft с доступом к всем файлам в файле.

### <a name="preserve-last-access-time"></a>Сохранение последнего времени доступа

При попытке подключения обхода файла обновляется поле "время последнего доступа" в метаданных. Если вы зависите от этого поля для любых решений архивации и резервного копирования и не хотите обновлять его при доступе к нему соединителя, вы можете настроить этот параметр на странице **Расширенные параметры.**

## <a name="step-4-manage-search-permissions"></a>Шаг 4. Управление разрешениями на поиск

Вы можете ограничить разрешение на поиск любого файла на основе списков управления доступом к share или списков управления доступом к новой системе доступа NTFS, выбрав нужный вариант на странице Управление разрешениями на **поиск.** Учетные записи и группы пользователей, указанные в этих списках управления доступом, должны управляться службой Active Directory (AD). Если вы используете любую другую систему управления учетными записями пользователей, вы можете выбрать параметр "все", который позволяет пользователям искать все файлы без каких-либо ограничений доступа. Однако, когда пользователи пытаются открыть файл, применяются элементы управления доступом, установленные в источнике.

Обратите внимание, что windows по умолчанию предоставляет разрешение "Чтение" на "Все" в share ACLs при совместном доступе папки в сети. Кроме того, если вы выбираете share ACLs в **Управлении** разрешениями на поиск, пользователи смогут искать все файлы. Если вы хотите ограничить доступ, удалите доступ "Чтение" для "Все" в файлах и предограничите доступ только нужным пользователям и группам. Соединительные данные считываю эти ограничения доступа и применяем их для поиска.

Вы можете выбрать ALS share только в том случае, если предоставленный путь к совместной информации следует формату пути UNC. Вы можете создать путь в формате UNC, переехав в раздел "Расширенный общий доступ" в разделе "Общий доступ".

![Advanced_sharing](media/file-connector/file-advanced-sharing.png)

## <a name="step-5-assign-property-labels"></a>Шаг 5. Назначение меток свойств

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a>Шаг 6. Управление схемой

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a>Шаг 7. Выбор параметров обновления

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a>Шаг 8. Просмотр подключения

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->