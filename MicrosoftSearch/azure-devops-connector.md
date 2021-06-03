---
title: Azure DevOps Graph соединители для microsoft Search
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
description: Настройка соединитетеля Azure DevOps Graph microsoft Search
ms.openlocfilehash: bfe04a022360a968424b673ad03ba05f27c8c333
ms.sourcegitcommit: 1b154441f3a3abba0f2719e66a767432bc9506ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2021
ms.locfileid: "52720955"
---
<!---Previous ms.author: shgrover --->

# <a name="azure-devops-graph-connector-preview"></a>Azure DevOps Graph (предварительный просмотр)

Соедините Azure DevOps Graph позволяет организации индексировать элементы работы в экземпляре Azure DevOps службы. После настройки соединители и индексации контента из Azure DevOps конечные пользователи могут искать эти элементы в Microsoft Search.

> [!NOTE]
> Ознакомьтесь [**с статьей Установка Graph,**](configure-connector.md) чтобы понять общие инструкции Graph соединители.

Эта статья для всех, кто настраивает, запускает и отслеживает Azure DevOps Graph соединители. Он дополняет общий процесс установки и показывает инструкции, которые применяются только для Azure DevOps Graph соединители.

>[!IMPORTANT]
>Соедините Azure DevOps поддерживает только облачную службу Azure DevOps. Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015 и TFS 2013 не поддерживаются этим соединитетелем.

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям установки](./configure-connector.md).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>Шаг 3. Настройка параметров подключения

Чтобы подключиться к Azure DevOps экземпляру, необходимо Azure DevOps [](/azure/devops/organizations/accounts/create-organization) имя организации, его ID приложения и секрет клиента для проверки подлинности OAuth.

### <a name="register-an-app"></a>Регистрация приложения

Зарегистрируйте приложение в Azure DevOps, чтобы приложение Microsoft Search можно было получить доступ к экземпляру. Дополнительные дополнительные Azure DevOps документации о регистрации [приложения.](/azure/devops/integrate/get-started/authentication/oauth?preserve-view=true&view=azure-devops#register-your-app)

В следующей таблице указаны инструкции по заполняемой форме регистрации приложений:

Обязательные поля | Описание | Рекомендуемое значение
--- | --- | ---
| Имя компании         | Имя вашей компании. | Использование соответствующего значения   |
| Имя приложения     | Уникальное значение, которое идентифицирует приложение, авторизуя его.    | Поиск (Майкрософт)     |
| Веб-сайт приложения  | URL-адрес приложения, который запрашивает доступ к экземпляру Azure DevOps во время установки соединителя. (Обязательно).  | https://<span>gcs.office.</span> com/
| URL-адрес вызова авторизации        | Необходимый URL-адрес вызова, на который перенаправляется сервер авторизации. | https://<span>gcs.office.</span> com/v1.0/admin/oauth/callback|
| Разрешенные области | Область доступа для приложения | Выберите следующие области: Identity (чтение), Work Items (read), Variable Groups (чтение), Project и team (чтение), Graph (чтение)|

>[!IMPORTANT]
>Разрешенные области, выбранные для приложения, должны соответствовать тем областьм, которые указаны выше. Если вы опустить одну из разрешенных областей в списке или добавить другую область, авторизация не будет работать.

При регистрации приложения с вышеуказанными сведениями вы получите  **ID** приложения и клиентскую тайну, которые будут использоваться для настройки соединитетеля.

>[!NOTE]
>Чтобы отопустить доступ к любому приложению, Azure DevOps в Azure DevOps, перейдите к настройкам пользователя в правой верхней части Azure DevOps экземпляра. Выберите профиль, а затем выберите авторизации в разделе Безопасность боковой области. Наведите курсор на авторизованном приложении OAuth, чтобы увидеть кнопку Revoke в углу сведений о приложении.

### <a name="connection-settings"></a>Параметры подключения

После регистрации приложения Microsoft Search с Azure DevOps вы можете завершить шаг параметров подключения. Введите имя организации, имя приложения и секрет клиента.

![Приложение подключения Параметры](media/ADO_Connection_settings_2.png)

### <a name="configure-data-select-projects-and-fields"></a>Настройка данных: выбор проектов и полей

Вы можете выбрать для подключения индексировать всю организацию или конкретные проекты.

Если вы решите индексировать всю организацию, элементы во всех проектах организации будут индексироваться. Новые проекты и элементы будут индексироваться во время следующего обхода после их создания.

Если вы выбираете отдельные проекты, индексировать будут только элементы работы в этих проектах.

![Настройка данных](media/ADO_Configure_data.png)

Далее выберите, в каких полях необходимо подключение для индексации и предварительного просмотра данных в этих полях перед началом.

![Выбор свойств](media/ADO_choose_properties.png)

## <a name="step-4-manage-search-permissions"></a>Шаг 4. Управление разрешениями на поиск

Соедините Azure DevOps поддерживает разрешения на поиск, видимые только людям с доступом к этому источнику данных  **или** **каждому.** Если вы выбираете только людей с доступом к этому источнику **данных,** индексные данные будут отображаться в результатах поиска для пользователей, которые имеют к ним доступ на основе разрешений для пользователей или групп на уровне организации, Project или области пути в Azure DevOps. Если вы **выбираете Everyone,** индексные данные будут отображаться в результатах поиска для всех пользователей.

## <a name="step-5-assign-property-labels"></a>Шаг 5. Назначение меток свойств

Следуйте общим [инструкциям установки](./configure-connector.md).

## <a name="step-6-manage-schema"></a>Шаг 6. Управление схемой

Следуйте общим [инструкциям установки](./configure-connector.md).

## <a name="step-7-choose-refresh-settings"></a>Шаг 7. Выбор параметров обновления

Соедините Azure DevOps поддерживает расписание обновления для полного и постепенного обхода.
Рекомендуемое расписание — один час для инкрементного обхода и один день для полного обхода.

## <a name="step-8-review-connection"></a>Шаг 8. Просмотр подключения

Следуйте общим [инструкциям установки](./configure-connector.md).

>[!TIP]
>**Тип результата по умолчанию**
>* Соединит Azure DevOps автоматически регистрирует тип результатов [после](./customize-search-page.md#step-2-create-the-result-types) публикации соединителю. Тип результатов использует динамически созданный [макет результатов](./customize-results-layout.md) на основе полей, выбранных в шаге 3. 
>* Вы можете управлять типом результатов, переходя на типы [**результатов**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes) [в центре администрирования Microsoft 365.](https://admin.microsoft.com) Тип результатов по умолчанию будет называться `ConnectionId` "По умолчанию". Например, если у вас есть id подключения, макет результатов будет `AzureDevOps` назван: "AzureDevOpsDefault"
>* Кроме того, при необходимости можно создать собственный тип результатов.

<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->