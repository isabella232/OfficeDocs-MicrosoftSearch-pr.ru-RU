---
title: Соединителю Azure DevOps Graph для Поиска (Майкрософт)
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
description: Настройка соединителя Azure DevOps Graph для Поиска (Майкрософт)
ms.openlocfilehash: 8fe783c847c672223e051f4433af3e41678fe367
ms.sourcegitcommit: d53b91f8f52a4a96281b66831c2449bbffe2177c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50097406"
---
<!---Previous ms.author: shgrover --->

# <a name="azure-devops-graph-connector-preview"></a>Соединителю Azure DevOps Graph (предварительная версия)

Соединителю Azure DevOps Graph позволяет организации индексировать элементы работы в экземпляре службы Azure DevOps. После настройки соединителя и индекса контента из Azure DevOps конечные пользователи смогут искать эти элементы в Поиске (Майкрософт).

> [!NOTE]
> Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.

Эта статья для всех, кто настраивает, запускает и отслеживает соединителю Azure DevOps Graph. Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединителю Azure DevOps Graph.

>[!IMPORTANT]
>Соединителю Azure DevOps поддерживается только облачная служба Azure DevOps. Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015 и TFS 2013 не поддерживаются этим соединитетелем.

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

Чтобы подключиться к экземпляру Azure DevOps, [](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) вам потребуется имя вашей организации Azure DevOps, его ИД приложения и секрет клиента для проверки подлинности OAuth.

### <a name="register-an-app"></a>Регистрация приложения

Зарегистрируйте приложение в Azure DevOps, чтобы приложение Поиска (Майкрософт) было доступно к экземпляру. Чтобы узнать больше, см. документацию по Azure DevOps о [регистрации приложения.](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app&preserve-view=true)

В следующей таблице приводится руководство по заполните форму регистрации приложения:

Обязательные поля | Описание | Рекомендуемое значение
--- | --- | ---
| Название компании         | Название вашей компании. | Использование соответствующего значения   |
| Имя приложения     | Уникальное значение, определяющие приложение, которое вы авторизуя.    | Поиск (Майкрософт)     |
| Веб-сайт приложения  | URL-адрес приложения, которое запрашивает доступ к экземпляру Azure DevOps во время настройки соединителя. (Обязательно).  | https://<span>gcs.office.</span> com/
| URL-адрес для доступа к авторизации        | Необходимый URL-адрес для перенаправления сервера авторизации. | https://<span>gcs.office.</span> com/v1.0/admin/oauth/callback|
| Авторизованные области | Область доступа для приложения | Выберите следующие области: удостоверение (чтение), элементы работы (чтение), переменные группы (чтение), проект и группа (чтение), Graph (чтение)|

При регистрации приложения с помощью вышеперечисленной  информации вы  получите ИД приложения и секрет клиента, которые будут использоваться для настройки соединители.

>[!NOTE]
>Чтобы отопустить доступ ко всем приложениям, зарегистрированным в Azure DevOps, перейдите к настройкам пользователя в правой части экземпляра Azure DevOps. Выберите "Профиль", а затем выберите "Авторизации" в разделе "Безопасность" боковой области. Наведите курсор на авторизованные приложения OAuth, чтобы увидеть кнопку "Отоски" в углу сведений о приложении.

### <a name="connection-settings"></a>Параметры подключения

После регистрации приложения Поиска (Майкрософт) в Azure DevOps можно выполнить шаг параметров подключения. Введите название организации, ИД приложения и секрет клиента.

![Параметры приложения подключения](media/ADO_Connection_settings_2.png)

### <a name="configure-data-select-projects-and-fields"></a>Настройка данных: выбор проектов и полей

Можно выбрать подключение для индексации всей организации или отдельных проектов.

Если вы решите индексировать всю организацию, элементы во всех проектах организации будут индексироваться. Новые проекты и элементы будут индексироваться во время следующего обхода контента после их создания.

При выборе отдельных проектов индексироваться будут только элементы работы в этих проектах.

![Настройка данных](media/ADO_Configure_data.png)

Затем выберите поля, которые необходимо проиндексировать и просмотреть данные в этих полях, прежде чем ировать.

![Выбор свойств](media/ADO_choose_properties.png)

## <a name="step-4-manage-search-permissions"></a>Шаг 4. Управление разрешениями поиска

Соединителю Azure DevOps доступны разрешения поиска, видимые только тем людям, у которых есть доступ к этому источнику данных, **или** **всем.** Если выбрать только пользователей с доступом к этому источнику **данных,** индексируемые данные будут отображаться в результатах поиска для пользователей, которые имеют к ним доступ на основе разрешений для пользователей или групп на уровне "Организация", "Проект" или "Путь к области" в Azure DevOps. Если выбрать **"Все",** индексные данные будут отображаться в результатах поиска для всех пользователей.

## <a name="step-5-assign-property-labels"></a>Шаг 5. Назначение меток свойств

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)

## <a name="step-6-manage-schema"></a>Шаг 6. Управление схемой

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)

## <a name="step-7-choose-refresh-settings"></a>Шаг 7. Выбор параметров обновления

Соединителю Azure DevOps поддерживаются расписания обновления для полных и добавок обхода контента.
Рекомендуемое расписание составляет один час для добавок обхода контента и один день для полного обхода.

## <a name="step-8-review-connection"></a>Шаг 8. Проверка подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
