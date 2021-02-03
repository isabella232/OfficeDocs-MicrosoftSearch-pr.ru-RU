---
title: Соединители ServiceNow Graph для Поиска (Майкрософт)
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
description: Настройка соединители ServiceNow Graph для Поиска (Майкрософт)
ms.openlocfilehash: d1fdfb5f1aec5091fd526152de2bdc86932cfdb9
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084896"
---
<!---Previous ms.author: kam1 --->

# <a name="servicenow-graph-connector"></a>Соединители ServiceNow Graph

Соединители ServiceNow Graph позволяют организации индексировать статьи на основе знаний, видимые пользователям в соответствии с разрешениями на использование критериев пользователя в организации. После настройки соединители и индекса контента из ServiceNow пользователи смогут искать статьи в любом клиенте Поиска (Майкрософт).

> [!NOTE]
> Прочитайте [**статью "Настройка соединители Graph",**](configure-connector.md) чтобы ознакомиться с общим процессом настройки соединители Graph.

Эта статья для всех, кто настраивает, запускает и отслеживает соединители ServiceNow Graph. Он дополняет общий процесс настройки и показывает инструкции, применимые только к соединителу ServiceNow Graph. В этой статье также содержатся сведения об [устранении неполадок](#troubleshooting) [и ограничениях.](#limitations)
  
## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>Шаг 1. Добавление соединителю Graph в Центре администрирования Microsoft 365

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>Шаг 2. Имя подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-connection-settings"></a>Шаг 3. Параметры подключения

Чтобы подключиться к данным ServiceNow, используйте URL-адрес экземпляра **ServiceNow** вашей организации для этой учетной записи, ИД клиента и секрет клиента для проверки подлинности OAuth.  

URL-адрес экземпляра **ServiceNow** организации обычно https:// домене вашей организации **&lt;>.service-now.com.** Наряду с этим URL-адресом вам потребуется учетная запись для настройки подключения к ServiceNow и для того, чтобы разрешить Поиску (Майкрософт) обновлять статьи из ServiceNow на основе расписания обновления. Учетная запись должна иметь по крайней мере <em>роль</em> знаний. [Узнайте, как назначить роль для учетных записей ServiceNow.](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)

>[!NOTE]
>Если вы хотите обходить удостоверения пользователей и групп, чтобы учитывать разрешения на доступ к статьям базы знаний в результатах поиска (Майкрософт), учетная запись должна иметь доступ для чтения следующих записей таблицы в ServiceNow:
>* kb_uc_can_contribute_mtom
>* kb_uc_can_read_mtom
>* kb_uc_cannot_read_mtom
>* kb_uc_cannot_contribute_mtom
>* sys_user
>* sys_user_has_role
>* sys_user_grmember
>* user_criteria
>* kb_knowledge_base  
> Вы можете создать и назначить роль учетной записи, используемой для подключения к Поиску (Майкрософт). Для этой роли можно на назначены доступ на чтение к таблицам. Чтобы узнать о настройке доступа на чтение записей таблицы, см. [статью "Защита записей таблицы".](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls)

Чтобы проверить подлинность и синхронизировать контент из ServiceNow, выберите **один из трех поддерживаемых** методов:

1. Обычная проверка подлинности
1. ServiceNow OAuth (рекомендуется)
1. Azure AD OpenID Connect

### <a name="basic-authentication"></a>Обычная проверка подлинности

Введите имя пользователя и пароль учетной записи ServiceNow с ролью **знаний** для проверки подлинности в экземпляре.

### <a name="servicenow-oauth"></a>ServiceNow OAuth

Чтобы использовать ServiceNow OAuth для проверки подлинности, подберите конечную точку в экземпляре ServiceNow. Приложение Поиска (Майкрософт) будет использовать его для доступа к экземпляру. Дополнительные узнать см. в документе [ServiceNow](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) о создании конечной точки для клиентов, которые будут получать доступ к экземпляру.

В следующей таблице приводится руководство по заполните форму создания конечной точки:

Поле | Описание | Рекомендуемое значение 
--- | --- | ---
Имя | Уникальное значение, идентифицирует приложение, для которое требуется доступ OAuth. | Поиск (Майкрософт)
Идентификатор клиента | Автоматически созданный уникальный ИД приложения только для чтения. Экземпляр использует ИД клиента при запросе маркера доступа. | Н/Д
Секрет клиента | С помощью этой общей строки секрета экземпляр ServiceNow и Поиск (Майкрософт) разрешают взаимодействие друг с другом. | Следуйте советам по безопасности, обрабатывая секрет как пароль.
URL-адрес перенаправления | Необходимый URL-адрес для перенаправления сервера авторизации. | https://gcs.office.com/v1.0/admin/oauth/callback
URL-адрес логотипа | URL-адрес, содержащий изображение логотипа приложения. | Н/Д
Активное | Чтобы активировать реестр приложений, выберите его. | Установите в активном
Срок службы маркера обновления | Допустимый срок действия маркера обновления в секундах. По умолчанию срок действия маркеров обновления истекает через 100 дней (8 640 000 секунд). | 31 536 000 (1 год)
Срок службы маркеров доступа | Допустимый срок действия маркера доступа в секундах. | 43 200 (12 часов)

Введите ИД клиента и секрет клиента для подключения к экземпляру. После подключения используйте учетные данные учетной записи ServiceNow для проверки подлинности при обходе контента. Учетная запись должна иметь по крайней мере **роль** знаний.

### <a name="azure-ad-openid-connect"></a>Azure AD OpenID Connect

Чтобы использовать Azure AD OpenID Connect для проверки подлинности, выполните следующие действия.

## <a name="step-3a-register-a-new-application-in-azure-active-directory"></a>Шаг 3.a. Регистрация нового приложения в Azure Active Directory

Чтобы узнать о регистрации нового приложения в Azure Active Directory, см. статью ["Регистрация приложения".](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#register-an-application) Выберите каталог организации с одним клиентом. URI перенаправления не требуется. После регистрации запишите ИД приложения (клиента) и ИД каталога (клиента).

## <a name="step-3b-create-a-client-secret"></a>Шаг 3.b. Создание секрета клиента

Чтобы узнать о создании секрета клиента, см. создание [секрета клиента.](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) Заметьте секрет клиента.

## <a name="step-3c-retrieve-service-principal-object-identifier"></a>Шаг 3.c. Извлечение идентификатора объекта-службы

Выполните действия, чтобы получить идентификатор объекта-службы

1. Запустите PowerShell.

2. Установите Azure PowerShell с помощью следующей команды.

   ```powershell
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
   ```

3. Подключите к Azure.

   ```powershell
   Connect-AzAccount
   ```

4. Получить идентификатор объекта-службы.

   ```powershell
   Get-AzADServicePrincipal -ApplicationId "Application-ID"
   ```
   Замените "Application-ID" на ИД приложения (клиента) (без кавычка) приложения, зарегистрированного на шаге 3.a. Обратите внимание на значение объекта ID из выходных данных PowerShell. Это ИД основного службы.

Теперь у вас есть все сведения, необходимые для портала Azure. Краткая сводка сведений приведена в таблице ниже.

Свойство | Описание 
--- | ---
ИД каталога (ИД клиента) | Уникальный ИД клиента Azure Active Directory с шага 3.a.
ИД приложения (ИД клиента) | Уникальный ИД приложения, зарегистрированного на шаге 3.a.
Секрет клиента | Секретный ключ приложения (с шага 3.b). Обрабатывайте его как пароль.
ИД основного службы | Удостоверение приложения, запущенного в качестве службы. (с шага 3.c)

## <a name="step-3d-register-servicenow-application"></a>Шаг 3.d. Регистрация приложения ServiceNow

Экземпляру ServiceNow требуется следующая конфигурация:

1. Зарегистрируйте новый объект OAuth OIDC. Чтобы узнать, [см. статью "Создание поставщика OAuth OIDC".](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html)

2. В следующей таблице содержится руководство по заполните форму регистрации поставщика OIDC

   Поле | Описание | Рекомендуемое значение
   --- | --- | ---
   Имя | Уникальное имя, идентифицирует сущность OAuth OIDC. | Azure AD
   Идентификатор клиента | ИД клиента приложения, зарегистрированного на стороннем сервере OAuth OIDC. Экземпляр использует ИД клиента при запросе маркера доступа. | ИД приложения (клиента) из шага 3.a
   Секрет клиента | Секрет клиента приложения, зарегистрированного на стороннем сервере OAuth OIDC. | Секрет клиента из шага 3.b

   Все остальные значения могут быть значениями по умолчанию.

3. В форме регистрации поставщика OIDC необходимо добавить новую конфигурацию поставщика OIDC. Выберите значок поиска в поле "Конфигурация поставщика *OAuth OIDC",* чтобы открыть записи конфигураций OIDC. Выберите "Новый".

4. В следующей таблице содержится руководство по заполните форму конфигурации поставщика OIDC

   Поле | Рекомендуемое значение
   --- | ---
   Поставщик OIDC |  Azure AD
   URL-адрес метаданных OIDC | URL-адрес должен иметь вид https \: //login.microsoftonline.com/<tenandId">/.well-known/openid-configuration <br/>Замените "tenantID" на ИД каталога (клиента) из шага 3.a.
   Срок службы кэша конфигурации OIDC |  120
   Приложение | Глобальные
   Утверждение пользователя | sub
   Поле пользователя | Идентификатор пользователя
   Включить проверку утверждений JTI | Отключено

5. Выберите "Отправить" и обновите форму сущности OAuth OIDC.

## <a name="step-3e-create-a-servicenow-account"></a>Шаг 3.e. Создание учетной записи ServiceNow

Инструкции по созданию учетной записи ServiceNow и [созданию пользователя в ServiceNow.](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html)

В следующей таблице содержится руководство по заполните регистрацию учетной записи пользователя ServiceNow

Поле | Рекомендуемое значение
--- | ---
Идентификатор пользователя | ИД главного службы из шага 3.c
Только доступ к веб-службе | Checked

Все остальные значения можно оставить по умолчанию.

## <a name="step-3f-enable-knowledge-role-for-the-servicenow-account"></a>Шаг 3.f. Включить роль знаний для учетной записи ServiceNow

Access the ServiceNow account you created with ServiceNow Principal ID as User ID, and assign the knowledge role. Инструкции по назначению роли учетной записи ServiceNow можно найти здесь: назначение роли [пользователю.](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)

Используйте ИД приложения в качестве ИД клиента из шага 3.a и секрет клиента из шага 3.b, чтобы проверить подлинность экземпляра ServiceNow с помощью Azure AD OpenID Connect.

## <a name="step-4-select-properties-and-filter-data"></a>Шаг 4. Выбор свойств и фильтрация данных

На этом этапе можно добавить или удалить доступные свойства из источника данных ServiceNow. Microsoft 365 уже выбрал несколько свойств по умолчанию.

С помощью строки запроса ServiceNow можно указать условия для синхронизации статей. Это похоже на предложение **Where** в SQL **Select.** Например, можно выбрать индексацию только опубликованных и активных статей. Чтобы узнать о создании собственной строки запроса, см. статью "Создание закодированной строки запроса [с помощью фильтра".](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html)

Используйте кнопку результатов предварительного просмотра, чтобы проверить примеры значений выбранных свойств и фильтра запросов.

## <a name="step-5-manage-search-permissions"></a>Шаг 5. Управление разрешениями поиска

Соединители ServiceNow поддерживают разрешения поиска,  видимые всем или только людям с доступом **к этому источнику данных.** Индексные данные появляются в результатах поиска и видны пользователям в организации, которые имеют к ним доступ соответственно. ServiceNow Connector поддерживает разрешения по умолчанию для пользовательских критериев без расширенных сценариев. При поиске соединитетелем пользовательского критерия с расширенным сценарием все данные, использующие эти условия пользователя, не будут показаны в результатах поиска.

Если выбраны только пользователи, у которых есть доступ к этому источнику **данных,** необходимо дополнительно выбрать, есть ли в экземпляре ServiceNow пользователи, для которых предусмотрена подготовка Azure Active Directory (AAD), или пользователи, не в том случае, если они не AAD.

>[!NOTE]
>Соединители ServiceNow  доступны в предварительной версии, если выбрать только пользователей с доступом **к этому источнику данных.**

>[!NOTE]
>При выборе AAD в качестве типа источника удостоверений убедитесь, что вы назначаете свойство источника upN целевому свойству электронной почты в ServiceNow. Чтобы проверить или изменить сопоставления, см. пункт "Настройка сопоставлений атрибутов и атрибутов для пользовательской подготовка для [приложений SaaS в Azure Active Directory".](https://docs.microsoft.com/azure/active-directory/app-provisioning/customize-application-attributes)

Если вы решили получить ACL из экземпляра ServiceNow и выбрали "не-AAD" для типа удостоверений, см. инструкции по сопоставлению удостоверений, не относяшихся к [Azure AD.](map-non-aad.md)

## <a name="step-6-assign-property-labels"></a>Шаг 6. Назначение меток свойств

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-manage-schema"></a>Шаг 7. Управление схемой

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-choose-refresh-settings"></a>Шаг 8. Выбор параметров обновления

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

>[!NOTE]
>Для удостоверений будет применяться только запланированный полный обход контента.

## <a name="step-9-review-connection"></a>Шаг 9. Проверка подключения

Следуйте общим [инструкциям по настройке.](https://docs.microsoft.com/microsoftsearch/configure-connector)
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a>Устранение неполадок

После публикации подключения, настройки страницы результатов можно просмотреть состояние на вкладке **"Соединители"** в Центре [администрирования.](https://admin.microsoft.com) Чтобы узнать, как делать обновления и удаления, см. ["Управление соединитетелем".](manage-connector.md)

## <a name="limitations"></a>Ограничения

Соединители ServiceNow Graph имеют следующие ограничения в своем последнем выпуске:

- Индексация статей знаний, доступных всем в организации, является общедоступной функцией.
- *Только пользователи с доступом к* этой функции источника данных в шаге "Управление разрешениями поиска" находятся в режиме предварительного просмотра и обрабатывает только [разрешения на](https://hi.service-now.com/kb_view.do?sysparm_article=KB0550924) условия пользователя. Любые другие типы разрешений доступа не будут применены в результатах поиска.
- Критерии пользователя с расширенными сценариями не поддерживаются в текущей предварительной версии. Статьи базы знаний с ограничением доступа будут проиндексироваться с запретом доступа всем пользователям и не будут отображаться в результатах поиска ни для одного пользователя, пока они не будут поддерживаться.
