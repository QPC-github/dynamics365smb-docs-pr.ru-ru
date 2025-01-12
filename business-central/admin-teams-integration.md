---
title: Управление интеграцией Microsoft Teams с Business Central | Документация Майкрософт
description: Управление интеграцией Business Central с Microsoft Teams.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics365-business-central
---

# <a name="managing-microsoft-teams-integration-with-include-prodshortincludesprodshortmd" />Управление интеграцией Microsoft Teams с [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

В этой статье представлен обзор того, что вы можете делать как администратор для управления интеграцией Microsoft Teams с [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams" />В Microsoft Teams

### <a name="minimum-requirements" />Минимальные требования

В этом разделе описаны минимальные требования для работы функций приложения [!INCLUDE [prod_short](includes/prod_short.md)] в Teams.

- Необходимые лицензии

    Для приложения [!INCLUDE[prod_short](includes/prod_short.md)] требуется лицензия Teams через подписку Microsoft 365 Business или Enterprise. Отельные подписки на Teams, такие как Microsoft Teams (бесплатно) или Microsoft Teams Essentials, не поддерживаются.

    Большинство функций приложения [!INCLUDE[prod_short](includes/prod_short.md)] для Teams также требуют лицензии [!INCLUDE [prod_short](includes/prod_short.md)], как показано в следующей таблице.

    |Какая|Лицензия [!INCLUDE [prod_short](includes/prod_short.md)]|
    |----|---|
    |Поиск контактов [!INCLUDE [prod_short](includes/prod_short.md)].|![флажок](media/check.png "галочка")|
    |Вставьте ссылку в запись [!INCLUDE [prod_short](includes/prod_short.md)] в беседу и отправьте как карточку.|![флажок](media/check.png "галочка")|
    |Поделиться ссылкой со страницы в [!INCLUDE [prod_short](includes/prod_short.md)] в беседе Teams.|![флажок](media/check.png "галочка")|
    |Посмотреть карточку записи [!INCLUDE [prod_short](includes/prod_short.md)] в разговоре.||
    |Посмотреть подробности карточки записи [!INCLUDE [prod_short](includes/prod_short.md)] в разговоре.|![флажок](media/check.png "галочка")|
    |Откройте ссылку на страницу в [!INCLUDE [prod_short](includes/prod_short.md)] из беседы.|![флажок](media/check.png "галочка")|

- Разрешить предварительный просмотр URL-адресов

    Параметр политики **Разрешить предварительный просмотр URL-адресов** должен быть включен. В противном случае невозможно создать карточку для ссылок [!INCLUDE [prod_short](includes/prod_short.md)], вставленных в беседу Teams. Для получения дополнительной информации об этом параметре см. [Управляйте политиками обмена сообщениями в Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-include-prodshortincludesprodshortmd-app-optional" />Управление приложением [!INCLUDE [prod_short](includes/prod_short.md)] (необязательно)

Как администратор Teams вы можете управлять всеми приложениями для своей организации, включая приложение [!INCLUDE [prod_short](includes/prod_short.md)]. Вы можете утвердить или установить приложение [!INCLUDE [prod_short](includes/prod_short.md)] для вашей организации, запретить пользователю устанавливать приложение и т. д.

Для получения дополнительной информации см. следующие статьи в документации Microsoft Teams:

- [Управляйте своими приложениями в центре администрирования Microsoft Teams](/MicrosoftTeams/manage-apps)
- [Управляйте политиками настройки приложений в Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## <a name="in-include-prodshortincludesprodshortmd" />В [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements" />Минимальные требования

- Версия [!INCLUDE [prod_short](includes/prod_short.md)]:

    [!INCLUDE [prod_short](includes/prod_short.md)] выпуск 2021, волна 1, или новее. Интеграция Teams поддерживается только для [!INCLUDE [prod_short](includes/prod_short.md)] (онлайн); не локально.

- Codeunit **2718, поставщик сводки по страницам** публикуется как веб-сервис:

    Этот codeunit публикуется как веб-служба по умолчанию. codeunit является частью системного приложения [!INCLUDE [prod_short](includes/prod_short.md)]. Он используется для получения данных поля для страницы [!INCLUDE [prod_short](includes/prod_short.md)], добавленной в беседу Teams. Сведения о публикации веб-служб см. в разделе [Публикация веб-службы](across-how-publish-web-service.md).

- <a name="permissions"></a>Разрешения пользователя:

    Как правило, поиск контактов, страницы и данные, которые пользователи могут просматривать и редактировать в беседе Teams, контролируются их разрешениями в [!INCLUDE [prod_short](includes/prod_short.md)].

    - Для поиска контактов пользователи должны иметь как минимум разрешение на чтение для таблицы **Контакты**. 
    - Чтобы вставить ссылку [!INCLUDE [prod_short](includes/prod_short.md)] в беседу Teams и развернуть ее в карточку, пользователи должны иметь как минимум разрешение на чтение страницы и ее данных.
    - После того, как карточка отправлена в беседу, любой пользователь в этой беседе может просматривать эту карточку без разрешения [!INCLUDE [prod_short](includes/prod_short.md)].
    - Чтобы просмотреть подробную информацию о карте или открыть запись в [!INCLUDE [prod_short](includes/prod_short.md)], пользователи должны иметь разрешение на чтение страницы и ее данных.
    - Чтобы изменить данные, пользователю необходимо изменить разрешения.
    
    Сведения о разрешениях см. в разделе [Назначение разрешений пользователям и группам](ui-define-granular-permissions.md).

## <a name="installing-the-business-central-app-by-using-centralized-deployment" />Установка приложения Business Central с помощью централизованного развертывания

В центре администрирования Microsoft Teams — это место, где вы настраиваете политики установки приложений Teams для организации. В центре администрирования Teams вы можете использовать функцию централизованного развертывания для автоматической установки приложения Business Central в Teams для всех пользователей в вашей организации, определенных групп или отдельных пользователей.

> [!NOTE]
> Чтобы настроить централизованное развертывание, ваша учетная запись Teams должна иметь роль **Администратор службы Teams** или **Глобальный администратор**.

1. В Business Central выберите ![Лупа, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") введите **Централизованное развертывание приложений Teams** и выберите связанную ссылку. Или нажмите [здесь](https://businesscentral.dynamics.com/?page=1833), чтобы открыть страницу напрямую.
2. Прочтите информацию в **Настройка приложения Business Central для Teams**, затем выберите **Далее**, когда готовы.
3. Откройте [Центр администрирования Teams](https://go.microsoft.com/fwlink/?linkid=2163970) и выполните следующие шаги.
    1. Перейдите **Приложения Teams** > **Политики настройки**.
    2. Создайте новую политику или выберите политику, которую вы хотите использовать для установки приложения Business Central, затем выберите **Добавить приложения**.
    3. На странице **Добавить установленные приложения** найдите и выберите **Business Central**.
    4. Нажмите **Добавить**.

       Business Central теперь должен отображаться в **Установленные приложения** для политики.
    5. При необходимости настройте дополнительные параметры и выберите **Сохранить**.

    Дополнительные сведения о политиках настройки в Teams см. в разделе [Управляйте политиками настройки приложений в Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) в документации Teams.
4. Вернитесь в **Централизованное развертывание приложений Teams** в Business Central и выберите **Готово**.

> [!IMPORTANT]
> Применение политики настройки приложения и развертывание приложения для пользователей может занять до 24 часов.

## <a name="managing-privacy-and-compliance" />Управление конфиденциальностью и соблюдением требований

Microsoft Teams обеспечивает обширный контроль за соблюдением и управлением конфиденциальными или личными данными &mdash; включая данные, добавленные в чаты и каналы приложением [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="understanding-where-include-prodshortincludesprodshortmd-cards-are-stored" />Сведения о том, где хранятся карточки [!INCLUDE [prod_short](includes/prod_short.md)]

После отправки карточки в чат она и поля, отображаемые на карточке, копируются в Teams. Эта информация регулируется политиками Teams для вашей организации, такими как политики хранения данных. При отображении сведений карточки никакие данные в окне сведений не хранятся в Teams. Данные остаются в [!INCLUDE [prod_short](includes/prod_short.md)] и будут извлечены Teams только тогда, когда пользователь решит просмотреть сведения. 

- Чтобы узнать больше о том, где Teams хранит эти данные, см. раздел [Расположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Чтобы узнать больше о политиках хранения в Teams, см. раздел [Политики хранения в Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards" />Ограничение доступа к карточкам

Вы запрещаете отдельным пользователям или группам отправлять карточки в чаты или каналы, настраивая политики обмена сообщениями, которые отключают настройку **Предварительный просмотр URL-адресов**. Для получения дополнительной информации об этом параметре см. [Управление политиками обмена сообщениями в Teams](/microsoftteams/messaging-policies-in-teams). 

Вы также можете использовать информационные барьеры, чтобы люди или группы не могли общаться друг с другом. Дополнительные сведения см. в разделе [Информационные барьеры в Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Функции предотвращения потери данных в Центре безопасности и соответствия требованиям Microsoft 365 нельзя применять к самим карточкам. Но их можно применить к сообщениям чата, содержащим карточки. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests" />Ответы на запросы данных

Вы разрешаете членам групп и владельцам групп удалять сообщения, содержащие конфиденциальные карточки, путем настройки политик обмена сообщениями, например: **Владельцы могут удалять отправленные сообщения** и **Пользователи могут удалять отправленные сообщения**. Дополнительные сведения см. в разделе [Управление политиками обмена сообщениями в Teams](/microsoftteams/messaging-policies-in-teams).

Функции поиска содержимого и соответствия eDiscovery в Центре безопасности и соответствия требованиям Microsoft 365 можно также применять к карточкам.

Поскольку данные карточек в Teams являются копией данных в [!INCLUDE [prod_short](includes/prod_short.md)], вы также можете использовать функции [!INCLUDE [prod_short](includes/prod_short.md)] для экспорта данных клиента по запросу. Дополнительные сведения о конфиденциальности в [!INCLUDE [prod_short](includes/prod_short.md)] см. в разделе [Вопросы и ответы о конфиденциальности для клиентов Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="show-or-hide-record-data-on-cards" />Отображение или скрытие данных записей на карточках

Когда кто-то делится записью с другими пользователями в чате или канале Teams, отображается карточка с полями, содержащими данные об этой записи. По умолчанию эти данные (или сводку записи) могут просматривать все получатели, независимо от имеющихся у них лицензий или разрешений в Business Central. Если вы являетесь администратором, вы можете использовать мастер настройки **Параметры карточек**, чтобы запретить отображение сводки записи на карточках в Teams. При скрытии сводки записи удаляются все поля и изображения, но на карточке по-прежнему отображается кнопка **Подробности** и другая не относящаяся к записи информация.

|Включить сводку записи|Выключить сводку записи|
|-|-|
|![Изображение, на котором показана карточка в Teams при включенном отображении сводки записи.](media/card-settings-example-on.png)|![Изображение, на котором показана карточка в Teams при выключенном отображении сводки записи.](media/card-settings-example-off.png)|

Этот параметр настраивается отдельно для каждой среды. Таким образом, когда вы включаете или отключаете отображение сводки записи, это влияет на все компании в среде.

1. В Business Central откройте среду, которую вы хотите изменить.

   > [!TIP]
   > Чтобы переключить среду, нажмите <kbd>Ctrl</kbd>+<kbd>O</kbd>.
2. Нажмите значок ![Лупа, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Параметры карточек**, а затем выберите связанную ссылку. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Прочтите информацию о **параметрах карточек** и нажмите **Далее**, когда будете готовы.
4. На странице **Видимость данных** включите параметр **Показывать сводку записи**, если нужно, чтобы данные отображались на карточках, либо выключите его, чтобы скрыть данные.
5. Выберите **Далее** и завершите настройку, следуя инструкциям мастера.

## <a name="see-also" />См. также

[Обзор интеграции [!INCLUDE [prod_short](includes/prod_short.md)] и Microsoft Teams](across-teams-overview.md)  
[Установка приложения [!INCLUDE [prod_short](includes/prod_short.md)] для Microsoft Teams](across-install-app-for-teams.md)  
[Вопросы и ответы по Teams](teams-faq.md)  
[Устранение неполадок Teams](admin-teams-troubleshooting.md)  
[Разработка для интеграции Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
