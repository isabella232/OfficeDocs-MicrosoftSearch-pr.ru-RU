---
title: Соединитель Azure Data Lake Graph для Поиска (Майкрософт)
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Настройка соединитора Azure Data Lake Storage Gen2 Graph для Поиска (Майкрософт)
ms.openlocfilehash: da508694929d3c83a456c664aa4613b09a1b14a3
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084860"
---
<!---Previous ms.author: monaray --->

# <a name="azure-data-lake-storage-gen2-graph-connector"></a>Соединитель Azure Data Lake Storage Gen2 Graph

Соединители Azure Data Lake Storage Gen2 Graph позволяют пользователям в организации искать файлы, хранимые в учетных записях хранилища [BLOB-файлов Azure](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) [и Azure Data Lake поколения 2.](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)

> [!NOTE]
> Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.

Эта статья посвящена всем, кто настраивает, запускает и отслеживает соединитель Хранилища данных Azure Data Lake Gen2. Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединитеструктору Хранилища данных Azure Data Lake Gen2. В этой статье также содержатся сведения об [ограничениях.](#limitations)

В этой статье мы используем *хранилище Azure в* качестве универсального термина для хранилища [BLOB-хранилищ Azure](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) и хранилища Azure Data Lake поколения [2.](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

Введите строку подключения к основному хранилищу. Эта строка необходима, чтобы разрешить доступ к вашей учетной записи хранения. Чтобы найти строку подключения, перейдите на  портал [Azure](https://ms.portal.azure.com/#home) и перейдите в раздел "Ключи" соответствующей учетной записи хранилища Azure.

Если вы предпочитаете не предоставлять **AccountKey** (параметр в строке основного подключения к хранилищу), предодав доступ к нашей службе соединителя Graph для следующих ролей:

* Storage Blob Data Reader
* Участник данных очереди хранилища
* Делегатор BLOB-хранилищ

Перейдите на **вкладку "Управление** доступом" учетной записи службы хранилища Azure и следуйте инструкциям, чтобы предоставить доступ к следующему приложению:

* **First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766
* **Имя приложения первой стороны:** Служба соединители Graph

### <a name="storage-account-and-queue-notifications-optional"></a>Учетная запись хранения и уведомления очереди (необязательно)

Поддержка обработки изменений в режиме реального времени в службе соединители Graph может быть добавлена в будущем. В этом случае мы будем отслеживать уведомления об изменениях хранилища Azure, хранимые в очереди. Вам потребуется создать очередь в той же учетной записи, что и учетная запись службы хранилища Azure.

После создания очереди перейдите на вкладку **"События"** на странице очереди, чтобы настроить **подписку на события.** Выберите все события BLOB, которые будет получать очередь, и подключите очередь к учетной записи хранилища Azure.

## <a name="step-4-assign-property-labels"></a>Шаг 4. Назначение меток свойств

Для каждой метки можно назначить свойство источника, выбрав в меню параметры. Хотя этот шаг не является обязательным, наличие некоторых меток свойств повышает релевантность поиска и улучшает результаты поиска для конечных пользователей.

## <a name="step-5-manage-schema"></a>Шаг 5. Управление схемой

На экране **"Управление схемой"** можно изменить атрибуты схемы, связанные со свойствами. Возможные варианты: **Запрос,** **Поиск,** Извлечение и **уточнение.**  Вы также можете добавить необязательные псевдонимы и выбрать **свойство Content.**

## <a name="step-6-manage-search-permissions"></a>Шаг 6. Управление разрешениями поиска

### <a name="azure-data-lake-gen-2"></a>Azure Data Lake Gen 2

Вы можете выбрать использование списков управления доступом (ALS) из учетной записи хранилища [Azure Data Lake поколения 2.](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) Когда эти разрешения поиска настроены, контент поиска обрезается на основе разрешений пользователя, выписав его в [Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/) Кроме того, вы можете сделать все содержимое, индексироваться из учетной записи хранения, видимым всем в организации. В этом случае все в вашей организации будут иметь доступ ко всем данным в вашей учетной записи хранения.

Соединитель Azure Data Lake Storage Gen2 Graph поддерживает разрешения **поиска,** видимые всем или только людям с доступом к **этому источнику данных.** Индексные данные, которые появляются в результатах поиска, могут быть видны пользователям в организации, которые имеют доступ к каждому элементу.

### <a name="azure-blob-storage"></a>Хранилище BLOB-объектов Azure

Для подключения к хранилищу [BLOB-данных Azure](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)весь контент, индексируемый из настроенного источника, виден всем в организации. Списки управления доступом не поддерживаются на уровне BLOB-хранилищ Azure.

## <a name="step-7-set-the-refresh-schedule"></a>Шаг 7. Настройка расписания обновления

На экране **"Параметры обновления"** можно установить интервал добавоального обхода контента и интервал полного обхода. По умолчанию интервалы для соединителя хранилища azure Data Lake Gen2 равны 15 минутам для добавального обхода контента и одной неделе для полного обхода.

## <a name="step-8-review-connection"></a>Шаг 8. Проверка подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a>Ограничения

Опубликованное подключение для хранилища BLOB-хранилищ Azure невозможно перенастроить для источника Хранилища данных Azure Data Lake Gen2 и наоборот. В таких сценариях рекомендуется настроить новое подключение.

Кроме того, размер файлов должен быть не менее 4 МБ для обхода. Поддерживаемые в настоящее время типы файлов:

* Word (docx, DOCM, DOTX, DOTM)
* PowerPoint (PPTM, PPTX, POTM, POTX, PPAM, PPSM, PPSX)
* Excel (XLSX, XLSM)
* Устаревшие форматы Office (DOC, DOT и т. д.)
* Текст (TXT)
* HTML
* PDF

Двоичные файлы, такие как изображения (JPG, BMP и т. д.), не поддерживаются. Например, если DOCX-файл содержит только изображения, его можно пропустить, так как он не возвращает никакого содержимого.
