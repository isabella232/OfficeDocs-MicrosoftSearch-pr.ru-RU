---
title: Соединитель Azure Data Lake Graph для microsoft Search
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
description: Настройка соединиттеля Azure Data Lake Storage Gen2 Graph для microsoft Search
ms.openlocfilehash: 37a035b3de9dc217f885f193992d1e74a675fb35
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031326"
---
<!---Previous ms.author: monaray --->

# <a name="azure-data-lake-storage-gen2-graph-connector"></a>Разъем Azure Data Lake Storage Gen2 Graph

Соединитель Azure Data Lake Storage Gen2 Graph позволяет пользователям в вашей организации искать файлы, хранимые в учетных записях хранения данных [Azure Blob](/azure/storage/blobs/storage-blobs-introduction) и [Azure Data Lake Gen 2.](/azure/storage/blobs/data-lake-storage-introduction)

> [!NOTE]
> Ознакомьтесь [**со статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общие инструкции по настройке соединитений Graph.

Эта статья для всех, кто настраивает, запускает и контролирует соединитель Azure Data Lake Storage Gen2. Он дополняет общий процесс установки и показывает инструкции, которые применяются только для соединиттеля Azure Data Lake Storage Gen2. В этой статье также содержатся сведения об [ограничениях.](#limitations)

В этой статье мы используем *Azure Storage* в качестве общего термина для хранения данных [Azure Blob и](/azure/storage/blobs/storage-blobs-introduction) Azure Data Lake Gen [2 Storage.](/azure/storage/blobs/data-lake-storage-introduction)

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

Введите первичную строку подключения к хранилищам. Эта строка необходима для доступа к учетной записи хранилища. Чтобы найти строку подключения, перейдите на портал [Azure](https://ms.portal.azure.com/#home) и перейдите в раздел **Ключи** соответствующей учетной записи azure Storage.

Если вы предпочитаете не предоставлять **AccountKey** (параметр в строке первичного подключения к хранилищам), предоставить доступ к нашей службе соединители графа для следующих ролей:

* Считыватель данных Blob хранилища
* Вкладчик данных очереди хранения
* Делегатор Blob хранения

Перейдите на **вкладку Управление** доступом учетной записи Azure Storage и следуйте инструкциям, чтобы предоставить доступ к следующему приложению:

* **First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766
* **Имя первого участника приложения:** Служба соединители графиков

### <a name="storage-account-and-queue-notifications-optional"></a>Учетная запись хранилища и уведомления очереди (необязательный)

Поддержка обработки изменений в режиме реального времени в службе соединители графа может быть добавлена в будущем. В этом случае мы будем отслеживать уведомления об изменении хранилища Azure, хранимые в очереди. Вам потребуется создать очередь в той же учетной записи, что и учетная запись Azure Storage.

После создания очереди перейдите на вкладку **События** на странице очереди, чтобы настроить подписку **на события.** Выберите все события Blob, которые получит очередь, и подключите очередь к учетной записи Azure Storage.

## <a name="step-4-assign-property-labels"></a>Шаг 4. Назначение меток свойств

Вы можете назначить свойству источника для каждой метки, выбрав из меню параметры. Хотя этот шаг не является обязательным, наличие некоторых меток свойств улучшит релевантность поиска и обеспечит лучшие результаты поиска для конечных пользователей.

## <a name="step-5-manage-schema"></a>Шаг 5. Управление схемой

На экране **Управление схемой** можно изменить атрибуты схемы, связанные с свойствами, параметры **: Запрос,** **Поиск,** **Извлечение** и **Уточнение.** Кроме того, можно добавить необязательные псевдонимы и выбрать **свойство Content.**

## <a name="step-6-manage-search-permissions"></a>Шаг 6. Управление разрешениями на поиск

### <a name="azure-data-lake-gen-2"></a>Azure Data Lake Gen 2

Вы можете выбрать, чтобы гнать списки управления доступом (ACLs) из учетной записи [хранения данных Azure Data Lake Gen 2.](/azure/storage/blobs/data-lake-storage-introduction) При наборе этих разрешений поиска содержимое поиска обрезается на основе разрешений пользователя, подписанного в [Azure Active Directory.](/azure/active-directory/) Кроме того, вы можете сделать все содержимое, индексироваться из учетной записи хранилища, видимым для всех в вашей организации. В этом случае все в вашей организации будут иметь доступ ко всем данным в учетной записи хранилища.

Соединитель Azure Data Lake Storage Gen2 Graph поддерживает разрешения на поиск, видимые всем или только людям с доступом **к этому источнику данных.** Индексные данные, которые появляются в результатах поиска, могут быть видны пользователям в организации, которые имеют доступ к каждому элементу.

### <a name="azure-blob-storage"></a>Хранилище BLOB-объектов Azure

Для подключения к [хранилище blob Azure](/azure/storage/blobs/storage-blobs-introduction)все содержимое, индексируемые из настроенного источника, видны всем в организации. Списки управления доступом не поддерживаются на уровне Blob в хранилище Azure Blob.

## <a name="step-7-set-the-refresh-schedule"></a>Шаг 7. Настройка расписания обновления

На экране **Параметры обновления** можно установить интервал инкрементного обхода и полный интервал обхода. Интервалы интервалов для соединиттеля Хранения данных Azure Lake Gen2 для инкрементного обхода составляет 15 минут и одна неделя для полного обхода.

## <a name="step-8-review-connection"></a>Шаг 8. Просмотр подключения

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a>Ограничения

Опубликованное подключение для хранилища Blob Azure не может быть перенастройка для источника хранения данных Azure Data Lake Gen2 и наоборот. В таких сценариях рекомендуется настроить новое подключение.

Кроме того, размер файлов должен быть 4 МБ или меньше для обхода. В настоящее время поддерживаемые типы файлов:

* Word (docx, .docm, .dotx, .dotm)
* PowerPoint (.pptm, .pptx, .potm, .potx, .ppam, .ppsm, .ppsx)
* Excel (.xlsx, .xlsm)
* Устаревшие форматы Office (.doc, .dot и т.д.)
* Текст (.txt)
* HTML
* PDF

Двоичные файлы, такие как изображения (.jpg, bmp и т.д.), не поддерживаются. Например, если файл .docx содержит только изображения, его можно пропустить, так как он не возвращает контент.