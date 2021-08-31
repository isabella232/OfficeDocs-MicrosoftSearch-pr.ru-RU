---
title: Azure Data Lake Graph соединитель для Поиск (Майкрософт)
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
ms.localizationpriority: medium
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединиттеля Azure Data Lake служба хранилища Gen2 Graph для Поиск (Майкрософт)
ms.openlocfilehash: f60de4252e514f84bc92daf4ea65c535cf40a13d
ms.sourcegitcommit: cc9d743bcf5e998720ce9cd6eefb4061d913dc65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2021
ms.locfileid: "58701402"
---
<!---Previous ms.author: monaray --->

# <a name="azure-data-lake-storage-gen2-graph-connector"></a>Соединитель Azure Data Lake служба хранилища Gen2 Graph

Соединитель Azure Data Lake служба хранилища Gen2 Graph позволяет пользователям в организации искать файлы, хранимые в учетных записях [Azure Blob служба хранилища](/azure/storage/blobs/storage-blobs-introduction) и [Azure Data Lake Gen 2 служба хранилища.](/azure/storage/blobs/data-lake-storage-introduction)

> [!NOTE]
> Ознакомьтесь [**с статьей Настройка Graph соединители,**](configure-connector.md) чтобы понять общие инструкции Graph соединители.

Эта статья для всех, кто настраивает, запускает и отслеживает соединитель Azure Data Lake служба хранилища Gen2. Он дополняет общий процесс установки и показывает инструкции, применимые только к соединителью Azure Data Lake служба хранилища Gen2. В этой статье также содержатся сведения об [ограничениях.](#limitations)

В статье мы  используем служба хранилища Azure как общий термин для [Azure Blob служба хранилища](/azure/storage/blobs/storage-blobs-introduction) и Azure Data Lake [Gen 2 служба хранилища.](/azure/storage/blobs/data-lake-storage-introduction)

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в Центр администрирования Microsoft 365

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

Введите первичную строку подключения к хранилищам. Эта строка необходима для доступа к учетной записи хранилища. Чтобы найти строку подключения, перейдите на портал [Azure](https://ms.portal.azure.com/#home) и перейдите в раздел **Ключи** соответствующей служба хранилища Azure учетной записи.

Если вы предпочитаете не предоставлять **AccountKey** (параметр в строке первичного подключения к хранилищам), предоставить доступ к нашей службе соединители Graph для следующих ролей:

* служба хранилища Считыватель данных Blob
* служба хранилища Автор данных очереди
* служба хранилища Делегатор Blob

Перейдите на вкладку **Управление** доступом служба хранилища Azure учетной записи и следуйте инструкциям, чтобы предоставить доступ к следующему приложению:

* **First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766
* **Имя приложения первой стороны:** Graph соединители службы

### <a name="storage-account-and-queue-notifications-optional"></a>служба хранилища учетной записи и уведомлений очереди (необязательный)

Поддержка обработки изменений в режиме реального времени в службе Graph соединители могут быть добавлены в будущем. В этом случае мы будем отслеживать служба хранилища Azure уведомления об изменении, хранимые в очереди. Вам потребуется создать очередь в той же учетной записи, что и служба хранилища Azure учетной записи.

После создания очереди перейдите на вкладку **События** на странице очереди, чтобы настроить подписку **на события.** Выберите все события Blob, которые получит очередь, и подключите очередь к служба хранилища Azure учетной записи.

## <a name="step-4-assign-property-labels"></a>Шаг 4. Назначение меток свойств

Вы можете назначить свойству источника для каждой метки, выбрав из меню параметры. Хотя этот шаг не является обязательным, наличие некоторых меток свойств улучшит релевантность поиска и обеспечит лучшие результаты поиска для конечных пользователей.

## <a name="step-5-manage-schema"></a>Шаг 5. Управление схемой

На экране **Управление схемой** можно изменить атрибуты схемы, связанные с свойствами, параметры **: Запрос,** **Поиск,** **Извлечение** и **Уточнение.** Кроме того, можно добавить необязательные псевдонимы и выбрать **свойство Content.**

## <a name="step-6-manage-search-permissions"></a>Шаг 6. Управление разрешениями на поиск

### <a name="azure-data-lake-gen-2"></a>Azure Data Lake Gen 2

Вы можете использовать списки управления доступом (ACLs) из учетной записи [Azure Data Lake Gen 2 служба хранилища.](/azure/storage/blobs/data-lake-storage-introduction) При наборе этих разрешений поиска содержимое поиска обрезается на основе разрешений пользователя, подписанного [в Azure Active Directory.](/azure/active-directory/) Кроме того, вы можете сделать все содержимое, индексироваться из учетной записи хранилища, видимым для всех в вашей организации. В этом случае все в вашей организации будут иметь доступ ко всем данным в учетной записи хранилища.

Соединитель Azure Data Lake служба хранилища Gen2 Graph поддерживает разрешения на поиск, видимые всем или только людям с доступом к этому **источнику данных.**  Индексные данные, которые появляются в результатах поиска, могут быть видны пользователям в организации, которые имеют доступ к каждому элементу.

### <a name="azure-blob-storage"></a>Хранилище BLOB-объектов Azure

Для подключения к [Azure Blob служба хранилища](/azure/storage/blobs/storage-blobs-introduction)все содержимое, индексируемые из настроенного источника, видны всем в вашей организации. Списки управления доступом не поддерживаются на уровне Blob в Azure Blob служба хранилища.

## <a name="step-7-set-the-refresh-schedule"></a>Шаг 7. Настройка расписания обновления

На экране **Параметры** обновления можно установить интервал инкрементного обхода и полный интервал обхода. Интервалы интервалов для соединиттеля Azure Data Lake служба хранилища Gen2 — 15 минут для инкрементного обхода и одна неделя для полного обхода.

## <a name="step-8-review-connection"></a>Шаг 8. Просмотр подключения

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a>Ограничения

Опубликованное подключение для azure Blob служба хранилища не может быть перенастройка для Azure Data Lake служба хранилища Gen2 и наоборот. В таких сценариях рекомендуется настроить новое подключение.

Кроме того, размер файлов должен быть 4 МБ или меньше для обхода. В настоящее время поддерживаемые типы файлов:

* Word (docx, .docm, .dotx, .dotm)
* PowerPoint (.pptm, .pptx, .potm, .potx, .ppam, .ppsm, .ppsx)
* Excel (.xlsx, xlsm)
* Устаревшие Office форматы (.doc, .dot и т.д.)
* Текст (.txt)
* HTML
* PDF

Двоичные файлы, такие как изображения (.jpg, .bmp и т.д.), не поддерживаются. Например, если файл .docx содержит только изображения, его можно пропустить, так как он не возвращает контент.