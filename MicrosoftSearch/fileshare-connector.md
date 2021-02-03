---
title: Соединители Graph с файловой папкой для Поиска (Майкрософт)
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
ROBOTS: NoIndex
description: Настройка соединители Graph с файловой папкой для Поиска (Майкрософт)
ms.openlocfilehash: ae496d0a1f41dc75326b0f7ab96e54bda4ee879e
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084851"
---
<!---Previous ms.author: rusamai --->

# <a name="file-share-graph-connector"></a>Соединители Graph с файловой папкой

Соединители Graph с файловой папкой позволяют пользователям в организации искать файлы в локальной папке Windows.

> [!NOTE]
> Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.

Эта статья для всех, кто настраивает, запускает и отслеживает соединители ServiceNow Graph. Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединитеструктору MediaWiki Graph.

## <a name="before-you-get-started"></a>Перед началом работы

### <a name="install-the-graph-connector-agent"></a>Установка агента соединителя Graph

Чтобы проиндексировать файловые папки Windows, необходимо установить и зарегистрировать агент соединителя Graph. Дополнительные данные см. в подключении к агенту [соединителя Graph.](on-prem-agent.md)  

### <a name="content-requirements"></a>Требования к контенту

### <a name="file-types"></a>Типы файлов

Контент следующих форматов можно индексировать и искать: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS и ZIP. Индексироваться будет только текстовое содержимое этих форматов. Все мультимедийное содержимое игнорируется. Для любого файла, который не относится к этому формату, индексирование только метаданных.

### <a name="file-size-limits"></a>Ограничения на размер файлов

Максимальный поддерживаемый размер файла составляет 100 МБ. Файлы, объем которых превышает 100 МБ, не индексироваться. Максимальный размер после обработки составляет 4 МБ. Обработка останавливается, когда размер файла достигает 4 МБ. Поэтому некоторые фразы, присутствующие в файле, могут не работать для поиска.

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

На странице  **"Подключение к источнику данных"** выберите "Файловая папка" и укажет имя, ИД подключения и описание. На следующей странице укажете путь к файловой папке и выберите ранее установленный агент соединители Graph. Введите учетные данные для учетной [записи пользователя Microsoft Windows](https://microsoft.com/windows) с доступом на чтение ко всем файлам в файловом папке.

### <a name="preserve-last-access-time"></a>Сохранение времени последнего доступа

При попытке соединители обходить файл обновляется поле "Время последнего доступа" в метаданных. Если вы зависите от этого поля для каких-либо решений архивации и резервного копирования и не хотите  обновлять его при доступе соединителя к нему, вы можете настроить этот параметр на странице "Дополнительные параметры".

## <a name="step-4-manage-search-permissions"></a>Шаг 4. Управление разрешениями поиска

Вы можете ограничить разрешение на поиск файлов на основе списков управления доступом или списков управления доступом новой файловой системы (NTFS). Если вы хотите использовать списки управления доступом к данным, выберите соответствующий параметр на странице **"Дополнительные параметры".** Если вы хотите использовать списки управления доступом NTFS, выберите соответствующий параметр на странице "Управление **разрешениями поиска".**

## <a name="step-5-assign-property-labels"></a>Шаг 5. Назначение меток свойств

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a>Шаг 6. Управление схемой

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a>Шаг 7. Выбор параметров обновления

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a>Шаг 8. Проверка подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
