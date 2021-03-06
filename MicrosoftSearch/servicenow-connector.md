---
title: Соединители ServiceNow Graph для поиска в Microsoft Search
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
description: Настройка соединитетеля ServiceNow Graph для поиска в Microsoft Search
ms.openlocfilehash: eaf8014876b03c0b64c012cf7e83c4e4b84838b9
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508682"
---
<!---Previous ms.author: kam1 --->

# <a name="servicenow-graph-connector"></a>Соединители диаграммы ServiceNow

Соединители ServiceNow Graph позволяют организации индексировать статьи на основе знаний, видимые пользователям в соответствии с разрешениями пользователей в организации. После настройки соединители и индексации контента из ServiceNow пользователи могут искать статьи из любого клиента Microsoft Search.

> [!NOTE]
> Ознакомьтесь [**с статьей Настройка соединиттеля Graph,**](configure-connector.md) чтобы понять общие инструкции по настройке соединитений Graph.

Эта статья для всех, кто настраивает, запускает и отслеживает соединители ServiceNow Graph. Он дополняет общий процесс установки и показывает инструкции, применимые только к соединителу ServiceNow Graph. В этой статье также содержатся сведения о устранении [неполадок](#troubleshooting) и [ограничениях.](#limitations)
  
## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в центре администрирования Microsoft 365

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-connection-settings"></a>Шаг 3. Параметры подключения

Чтобы подключиться к данным ServiceNow, используйте URL-адрес url-адрес экземпляра **ServiceNow** вашей организации для этой учетной записи, удостоверение клиента и секрет клиента для проверки подлинности OAuth.  

URL-адрес экземпляра **ServiceNow** организации обычно https:// **&lt; домена>.service-now.com.** Наряду с этим URL-адресом необходимо создать учетную запись для настройки подключения к ServiceNow и разрешить Microsoft Search обновлять статьи из ServiceNow в соответствии с расписанием обновления. Учетная запись должна, по крайней мере, иметь <em>роль знаний.</em> [Узнайте, как назначить роль для учетных записей ServiceNow.](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)

>[!NOTE]
>Если вы хотите обхода удостоверений пользователей и групп для получения разрешений на доступ к статьям знаний в результатах поиска Майкрософт, у учетной записи должен быть доступ к следующим записям таблицы в ServiceNow:
>* kb_uc_can_contribute_mtom
>* kb_uc_can_read_mtom
>* kb_uc_cannot_read_mtom
>* kb_uc_cannot_contribute_mtom
>* sys_user
>* sys_user_has_role
>* sys_user_grmember
>* user_criteria
>* kb_knowledge_base  
> Вы можете создать и назначить роль для учетной записи, используемой для подключения к Microsoft Search. Доступ к таблицам для чтения может быть назначен в этой роли. Подробнее об установке доступа к записям таблицы для чтения см. в материале [Securing Table Records.](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls)

Чтобы проверить подлинность и синхронизировать контент из ServiceNow, выберите **один из трех** поддерживаемых методов:

1. Обычная проверка подлинности
1. ServiceNow OAuth (рекомендуется)
1. Подключение Azure AD OpenID

### <a name="basic-authentication"></a>Обычная проверка подлинности

Введите имя пользователя и пароль учетной  записи ServiceNow с ролью знаний для проверки подлинности экземпляра.

### <a name="servicenow-oauth"></a>ServiceNow OAuth

Чтобы использовать ServiceNow OAuth для проверки подлинности, уделите конечную точку в экземпляре ServiceNow. Приложение Microsoft Search будет использовать его для доступа к экземпляру. Дополнительные дополнительные возможности см. в [статью Создание конечной точки](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) для доступа клиентов к экземпляру в документации ServiceNow.

В следующей таблице приводится руководство по заполняемой форме создания конечной точки:

Поле | Описание | Рекомендуемое значение 
--- | --- | ---
Имя | Уникальное значение, которое определяет приложение, для которое требуется доступ к OAuth. | Поиск (Майкрософт)
Идентификатор клиента | Уникальный ID, созданный только для чтения, для приложения. Экземпляр использует клиентский ID при запросе маркера доступа. | Н/Д
Секрет клиента | С помощью этой общей секретной строки экземпляр ServiceNow и Microsoft Search разрешают сообщения друг с другом. | Следуйте лучшим практикам безопасности, обращаясь с секретом как с паролем.
URL-адрес перенаправления | Необходимый URL-адрес вызова, на который перенаправляется сервер авторизации. | https://gcs.office.com/v1.0/admin/oauth/callback
URL-адрес логотипа | URL-адрес, содержащий изображение для логотипа приложения. | Н/Д
Активное | Выберите контрольный ящик, чтобы сделать реестр приложений активным. | Настройка активного
Обновление срока службы маркера | Количество секунд, которые допустимы для маркера обновления. По умолчанию срок действия маркеров обновления истекает через 100 дней (8 640 000 секунд). | 31 536 000 (1 год)
Срок службы маркера доступа | Количество секунд, которые допустимы для маркера доступа. | 43 200 (12 часов)

Введите ИД клиента и секрет клиента, чтобы подключиться к экземпляру. После подключения используйте учетные данные учетной записи ServiceNow для проверки подлинности разрешения для обхода. Учетная запись должна, по крайней мере, иметь **роль знаний.**

### <a name="azure-ad-openid-connect"></a>Подключение Azure AD OpenID

Чтобы использовать Azure AD OpenID Connect для проверки подлинности, выполните следующие ниже действия.

## <a name="step-3a-register-a-new-application-in-azure-active-directory"></a>Шаг 3.a. Регистрация нового приложения в Azure Active Directory

Подробнее о регистрации нового приложения в Azure Active Directory см. в статью [Регистрация приложения.](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#register-an-application) Выберите единый организационный каталог клиента. Перенаправление URI не требуется. После регистрации обратите внимание на ID приложения (клиента) и directory (tenant).

## <a name="step-3b-create-a-client-secret"></a>Шаг 3.b. Создание секрета клиента

Дополнительные информацию о создании клиентской тайны см. в [см. в "Создание секрета клиента".](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) Обратите внимание на секрет клиента.

## <a name="step-3c-retrieve-service-principal-object-identifier"></a>Шаг 3.c. Извлечение идентификатора основного объекта службы

Выполните действия по извлечению идентификатора основного объекта службы

1. Запустите PowerShell.

2. Установите Azure PowerShell с помощью следующей команды.

   ```powershell
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
   ```

3. Подключение к Azure.

   ```powershell
   Connect-AzAccount
   ```

4. Получите идентификатор основного объекта службы.

   ```powershell
   Get-AzADServicePrincipal -ApplicationId "Application-ID"
   ```
   Замените "Application-ID" на ID приложения (клиента) (без кавычка) приложения, зарегистрированного на шаге 3.a. Обратите внимание на значение ID-объекта из вывода PowerShell. Это главный ID службы.

Теперь у вас есть все сведения, необходимые на портале Azure. Краткое описание сведений приведено в таблице ниже.

Свойство | Описание 
--- | ---
Directory ID (Tenant ID) | Уникальный ID клиента Azure Active Directory с шага 3.a.
ID приложения (Client ID) | Уникальный ID приложения, зарегистрированного в шаге 3.a.
Секрет клиента | Секретный ключ приложения (от шага 3.b). Обращайся с ним как с паролем.
ID директора службы | Удостоверение для приложения, запущенного в качестве службы. (с шага 3.c)

## <a name="step-3d-register-servicenow-application"></a>Шаг 3.d. Регистрация приложения ServiceNow

Экземпляр ServiceNow нуждается в следующей конфигурации:

1. Регистрация нового объекта OAuth OIDC. Дополнительные возможности см. [в статью Создание поставщика OAuth OIDC.](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html)

2. В следующей таблице указаны инструкции по заполняемой форме регистрации поставщика OIDC

   Поле | Описание | Рекомендуемое значение
   --- | --- | ---
   Имя | Уникальное имя, идентифицирует сущность OAuth OIDC. | Azure AD
   Идентификатор клиента | ID клиента приложения, зарегистрированного на стороннем сервере OAuth OIDC. Экземпляр использует клиентский ID при запросе маркера доступа. | ID приложения (клиента) с шага 3.a
   Секрет клиента | Секрет клиента приложения, зарегистрированного на стороннем сервере OAuth OIDC. | Секрет клиента с шага 3.b

   Все остальные значения могут быть по умолчанию.

3. В форме регистрации поставщика OIDC необходимо добавить новую конфигурацию поставщика OIDC. Выберите значок поиска в поле *конфигурации поставщика OAuth OIDC,* чтобы открыть записи конфигураций OIDC. Выберите New.

4. В следующей таблице приводится руководство по заполняемой форме конфигурации поставщика OIDC

   Поле | Рекомендуемое значение
   --- | ---
   Поставщик OIDC |  Azure AD
   URL-адрес метаданных OIDC | URL-адрес должен быть в форме \: https//login.microsoftonline.com/<tenandId">/.well-known/openid-configuration <br/>Замените "tenantID" на directory (tenant) ID с шага 3.a.
   Срок службы кэша конфигурации OIDC |  120
   Для приложений | Глобальные
   Утверждение пользователя | sub
   Пользовательское поле | Идентификатор пользователя
   Включить проверку утверждений JTI | Отключено

5. Выберите отправку и обновление формы OAuth OIDC Entity.

## <a name="step-3e-create-a-servicenow-account"></a>Шаг 3.e. Создание учетной записи ServiceNow

Обратитесь к инструкциям по созданию учетной записи ServiceNow, [созданию пользователя в ServiceNow](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html).

В следующей таблице указаны инструкции по заполняемой регистрации учетной записи пользователя ServiceNow

Поле | Рекомендуемое значение
--- | ---
Идентификатор пользователя | ID директора службы с шага 3.c
Доступ только к веб-службам | Checked

Все остальные значения можно оставить по умолчанию.

## <a name="step-3f-enable-knowledge-role-for-the-servicenow-account"></a>Шаг 3.f. Включить роль знания для учетной записи ServiceNow

Доступ к учетной записи ServiceNow, созданной с главным ИД ServiceNow в качестве пользовательского ИД, и назначьте роль знаний. Инструкции по назначению роли учетной записи ServiceNow можно найти здесь: назначить роль [пользователю.](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)

Используйте ID приложения в качестве клиентского ИД с шага 3.a и секрет клиента с шага 3.b для проверки подлинности экземпляра ServiceNow с помощью Azure AD OpenID Connect.

## <a name="step-4-select-properties-and-filter-data"></a>Шаг 4. Выбор свойств и фильтрация данных

На этом шаге можно добавить или удалить доступные свойства из источника данных ServiceNow. Microsoft 365 уже выбрал несколько свойств по умолчанию.

Со строкой запроса ServiceNow можно указать условия синхронизации статей. Это как **клаузула Where** в **заявлении SQL Select.** Например, можно индексировать только опубликованные и активные статьи. Чтобы узнать о создании собственной строки запроса, см. в статью Создание строки закодированного запроса [с помощью фильтра.](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html)

Чтобы проверить пример значений выбранных свойств и фильтра запросов, используйте кнопку "Результаты предварительного просмотра".

## <a name="step-5-manage-search-permissions"></a>Шаг 5. Управление разрешениями на поиск

Соединители ServiceNow поддерживают разрешения на  поиск, видимые всем или только людям с доступом **к этому источнику данных.** Индексация данных отображается в результатах поиска и видна пользователям организации, которые имеют к ним доступ соответственно. Соединительщик ServiceNow поддерживает разрешения пользователей по умолчанию без расширенных сценариев. Когда соединитатель находит пользовательские критерии с расширенным скриптом, все данные, использующие эти пользовательские критерии, не будут показаны в результатах поиска.

Если вы **выбираете** только людей, у которых есть доступ к этому источнику данных, вам необходимо дополнительно выбрать, имеет ли экземпляр ServiceNow предварительное предоставление пользователей Azure Active Directory (AAD) или пользователей non-AAD.

>[!NOTE]
>Соединитатель ServiceNow находится в предварительном **режиме,** если вы выбираете только людей **с доступом к этому источнику данных.**

>[!NOTE]
>Если вы выбираете AAD в качестве типа источника удостоверений, убедитесь, что вы назначаете свойство источника UPN для адресной почты в ServiceNow. Чтобы проверить или изменить сопоставления, см. в приложении Azure Active Directory параметры настройки атрибута подготовка пользователей для [приложений SaaS.](https://docs.microsoft.com/azure/active-directory/app-provisioning/customize-application-attributes)

Если вы решили гнать ACL из экземпляра ServiceNow и выбрали "non-AAD" для типа удостоверений, см. в примере Map [your non-Azure AD Identitys](map-non-aad.md) для инструкций по сопоставлению удостоверений.

## <a name="step-6-assign-property-labels"></a>Шаг 6. Назначение меток свойств

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-manage-schema"></a>Шаг 7. Управление схемой

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-choose-refresh-settings"></a>Шаг 8. Выбор параметров обновления

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

>[!NOTE]
>Для удостоверений будет применен только запланированный полный обход.

## <a name="step-9-review-connection"></a>Шаг 9. Просмотр подключения

Следуйте общим [инструкциям установки](https://docs.microsoft.com/microsoftsearch/configure-connector).
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a>Устранение неполадок

После публикации подключения, настройки страницы результатов можно просмотреть состояние в вкладке **Соединители** в центре [администрирования.](https://admin.microsoft.com) Подробнее о том, как делать обновления и удаления, см. в руб. [Управление соединитетелем.](manage-connector.md)

## <a name="limitations"></a>Ограничения

Соединители ServiceNow Graph имеют следующие ограничения в своем последнем выпуске:

- Индексация статей знаний, доступных всем в организации, является обычно доступной функцией.
- *Только люди с доступом к этой* функции источника данных в шаге Управление разрешениями поиска находятся в предварительном просмотре и обрабатывает только [разрешения пользовательских критериев.](https://hi.service-now.com/kb_view.do?sysparm_article=KB0550924) Разрешения доступа другого типа в результатах поиска не применяются.
- Пользовательские критерии с расширенными скриптами не поддерживаются в текущей версии предварительного просмотра. Статьи знаний с ограничением доступа будут индексироваться с отказом всем пользователям в доступе и не будут отображаться в результатах поиска ни для одного пользователя, пока мы их не поддерживаем.
