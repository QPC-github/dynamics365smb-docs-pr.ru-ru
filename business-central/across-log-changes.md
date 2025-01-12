---
title: Аудит изменений
description: 'Вы можете активизировать журнал пользователя, чтобы у вас была история всех изменений, внесенных в данные в отслеживаемых таблицах. Также можно отслеживать действия с помощью определенных типов журналов действий.'
author: edupont04
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 03/24/2022
ms.author: edupont
---
# <a name="auditing-changes-in-business-central" />Изменение аудита в Business Central

Общей задачей многих приложений для управления бизнесом является предотвращение нежелательных изменений данных. Это может быть все что угодно — от неправильно введенного номера телефона клиента, до неправильного учета в Главной книге. В этом разделе описываются возможности узнать, что изменилось, кто это изменил и когда это изменение было внесено.

## <a name="about-the-change-log" />О журнале изменений

Журнал изменений позволяет отслеживать все изменения, внесенные пользователем непосредственно в данные базы данных. Необходимо указать каждую таблицу и поле, которые система должна записывать в журнал, после чего следует активировать журнал изменений. Журнал изменений основывается на изменениях, внесенных в данные таблиц, по которым выполняется отслеживание. На странице **Операции журнала изменений** операции хронологически упорядочены, а также показывает все изменения, примененные к значениям в полях в указанных таблицах. 

Отслеживание изменений может негативно сказаться на быстродействии (что может стоить вам времени), а также привести к увеличению размера базы данных (что может стоить вам денег). Чтобы свести эти затраты к минимуму, помните о следующем:

- Выбирайте таблицы и операции с осторожностью.
- Не добавляйте операции книг и учтенные документы. Вместо этого отдавайте приоритет системным полям, таким как "Кем создано" и "Дата создания".
- Не используйте тип отслеживания "Все поля". Вместо этого выберите тип "Некоторые поля" и отслеживайте только самые важные из полей.

Также по соображениям производительности журнал изменений отключается в процессе обновления [!INCLUDE [prod_short](includes/prod_short.md)] на следующую версию. Помимо ускорения процесса обновления, это также помогает уменьшить беспорядок в журнале изменений. Как только обновление завершится, журнал снова начнет отслеживать изменения.

> [!Important]
> Изменения отображаются в **Записи журнала изменений** только после перезапуска сеанса пользователя, что происходит следующим образом:
>
> * Срок действия сеанса завершился и сеанс был обновлен.
> * Пользователь выбрал другую организацию или ролевой центр.
> * Пользователь выполнил выход, затем снова вход.

### <a name="work-with-the-change-log" />Работа с журналом изменений
Можно активировать и деактивировать журнал изменений на странице **Настройка журнала изменений**. Когда пользователь активирует или деактивирует журнал изменений, это действие регистрируется, чтобы всегда можно было просмотреть, какой пользователь деактивировал или повторно активировал журнал изменений.

На странице **Настройка журнала изменений**, если выбрать действие **Таблицы**, можно указать, для каких таблиц требуется отслеживать изменения и какие изменения требуется отслеживаться. [!INCLUDE[prod_short](includes/prod_short.md)] также отслеживает несколько системных таблиц.

> [!NOTE]
> Вы можете отслеживать изменения в определенных полях, например в полях, содержащих конфиденциальные данные, путем настройки мониторинга полей. Если вы это сделаете, чтобы избежать избыточности, таблица, содержащая это поле, не будет доступна для настройки журнала изменений. Для получения дополнительной информации см. [Мониторинг конфиденциальных полей](across-log-changes.md#monitoring-sensitive-fields).

После настройки журнала изменений, его активации и внесения изменений в данные можно просмотреть и отфильтровать изменения на странице **Операции журнала изменений**. Если требуется удалить операции, это можно сделать на странице **Удалить операции журнала изменений**, в котором можно установить фильтры на основе времени и даты.  

## <a name="about-activity-logs" />О журналах действий

С некоторых страниц в [!INCLUDE [prod_short](includes/prod_short.md)] можно просмотреть журнал действий, в котором указаны состояние и возможные ошибки из файлов, которые вы экспортируете или импортируете в [!INCLUDE [prod_short](includes/prod_short.md)],  

### <a name="work-with-activity-logs" />Работа с журналами действий
Эта информация отображается на странице **Журнал действий** в соответствии с контекстом, из которого открыта страница. Например, можно открыть страницу со страниц **Настройка службы обмена документами**, **Входящий документ**, **Учтенный счет продажи** и **Учтенная кредит-нота продажи**. Вы можете очистить список записей журнала или просто удалить из него записи старше семи дней.  

## <a name="monitoring-sensitive-fields" />Мониторинг конфиденциальных полей

Обеспечение безопасности и конфиденциальности конфиденциальных данных является основной задачей для большинства организаций. Чтобы добавить уровень безопасности, вы можете отслеживать важные поля и получать уведомления по электронной почте, когда кто-то меняет значение. Например, вы можете захотеть получать уведомления, если кто-то изменит номер IBAN вашей компании.

> [!NOTE]
> Для отправки уведомлений по электронной почте необходимо настроить функцию электронной почты в [!INCLUDE[prod_short](includes/prod_short.md)]. Дополнительные сведения см. в разделе [Настройка электронной почты](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring" />Настройка мониторинга полей

Вы можете использовать руководство мастера настройки **Настройка мониторинга изменений полей**, чтобы указать поля, которые вы хотите отслеживать на основе критериев фильтрации, таких как классификация данных для полей. Дополнительные сведения см. в разделе [Классификация конфиденциальности данных](admin-classifying-data-sensitivity.md). В руководстве также можно указать человека, который будет получать уведомление по электронной почте при изменении, и учетную запись электронной почты, которая будет отправлять уведомление по электронной почте. Укажите как уведомление пользователя, так и учетную запись, с которой будет отправлено уведомление. После того, как вы закончите работу с руководством, вы можете управлять настройками мониторинга полей на странице **Настройка мониторинга полей**. 

> [!NOTE]
> При указании учетной записи электронной почты для отправки уведомлений необходимо добавить типы учетных записей **Microsoft 365** или **SMTP**. Уведомления следует отправлять из учетной записи, которая не связана с фактическим пользователем. Поэтому вы не можете выбрать тип учетной записи **Текущий пользователь**. В противном случае уведомления отправляться не будут. 

Со временем список записей на странице **Записи журнала отслеживаемых полей** будет расти. Чтобы уменьшить количество записей, вы можете создать политику хранения, которая будет удалять записи по прошествии определенного периода времени. Дополнительные сведения см. в разделе [Определение политик хранения](admin-data-retention-policies.md).

Когда вы настраиваете мониторинг полей или что-то меняете в настройке, для ваших изменений создаются записи. Вы можете указать, следует ли отображать записи, относящиеся к настройке мониторинга, путем их отображения или скрытия. 

Вы можете управлять настройками для мониторинга полей, например отправлять ли уведомление по электронной почте или просто регистрировать изменение, для каждого поля на странице **Лист отслеживаемых полей**. На странице также можно добавлять или удалять поля для мониторинга.

> [!NOTE]
> После добавления одного или нескольких полей и начала мониторинга вы должны выйти из и снова войти [!INCLUDE[prod_short](includes/prod_short.md)], чтобы применить свои настройки.

### <a name="work-with-field-monitoring" />Работа с мониторингом полей

Записи для всех измененных значений для отслеживаемых полей доступны на странице **Записи журнала отслеживаемых полей**. Например, записи содержат следующие сведения:

* Поле, для которого было изменено значение.
* Оригинальные и новые значения.
* Кто внес изменения и когда это сделано. 

Для дальнейшего изучения изменения выберите значение, чтобы открыть страницу, на которой оно было внесено. Чтобы просмотреть список всех записей, выберите **Записи об изменении поля**.

### <a name="viewing-field-monitoring-telemetry" />Просмотр телеметрии мониторинга полей

Вы можете настроить [!INCLUDE[prod_short](includes/prod_short.md)], чтобы отправить действие мониторинга полей в ресурс Application Insights в Microsoft Azure. Затем с помощью Azure Monitor вы создаете отчеты и настраиваете оповещения о собранных данных. Дополнительные сведения см. в следующих статьях в справке для разработчиков и ИТ-специалистов [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Мониторинг и анализ телеметрии — включение Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Анализ телеметрии мониторинга полей](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies" />Определение политик хранения

Вы можете создать политики хранения для удаления ненужных данных в журналах по истечении указанного вами периода времени. Например, со временем количество записей в журнале может увеличиваться. Удаляя старые записи, вы можете улучшить концентрацию на более свежих и, возможно, более актуальных записях. Дополнительные сведения см. в разделе [Определение политик хранения](admin-data-retention-policies.md).

## <a name="see-also" />См. также

[Изменение базовых настроек](ui-change-basic-settings.md)  
[Сортировка, поиск и фильтрация](ui-enter-criteria-filters.md)  
[Поиск страниц и информации с помощью функции "Что вы хотите сделать"](ui-search.md)  
[Назначение разрешений пользователям и группам](ui-define-granular-permissions.md)    
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Определение политик хранения](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
