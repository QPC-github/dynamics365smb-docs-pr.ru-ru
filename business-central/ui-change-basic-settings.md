---
title: Изменение базовых настроек для текущего пользователя
description: 'Узнайте, как изменить некоторые основные параметры в Business Central, например свою роль и ролевой центр, компанию, дату работы и часовые пояса.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: jswymer
---
# <a name="change-basic-settings" />Изменение базовых настроек

На странице **Мои настройки** вы можете просмотреть и изменить базовые настройки для вашего [!INCLUDE[prod_short](includes/prod_short.md)]. Изменения, которые вы вносите, влияют только на вашу рабочую область, но не на рабочие области других пользователей.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="a-namerole-centerarole" /><a name="role-center"></a>Роль

Роль определяет начальную страницу — начальный экран, разработанный в соответствии с задачами конкретной роли в организации. В зависимости от вашей роли, домашняя страница или ролевой центр позволяет вам получить общее представление о компании, подразделении или ваших личных задачах. Он также помогает переходить к вашим ежедневным задачам и находить работу, которая вам назначена.

* Панель навигации в верхней части позволяет переключаться между клиентами, поставщиками, товарами и другими важными списками информации. Аналогично, действия позволяют инициировать задачи, такие как создание нового счета продажи, непосредственно из домашней страницы.

* В центре вы найдете область **Действия**, в которой отображаются текущие данные; их можно выбрать для просмотра более подробной информации. Можно настроить ключевые показатели эффективности (КПЭ) для отображения выбранной диаграммы, чтобы иметь визуальное представление, например, движения денежных средств или прибылей и убытков. Также на начальной странице можно составить список "Избранные клиенты" для бизнес-организаций, с которыми вы работаете чаще и которые требуют особого внимания.

### <a name="change-the-role" />Смена роли

По умолчанию установлена роль **Бизнес-руководитель**, но вы можете выбрать другую роль, чтобы использовать ролевой центр, в большей степени отвечающий вашим потребностям.  

1. В правом верхнем углу щелкните значок **Параметры** ![Параметры.](media/ui-experience/settings_icon_small.png "Значок настроек для ролевого центра"), а затем выберите действие **Мои настройки**.
2. На странице **Мои настройки** в поле **Роль** выберите роль, которую вы хотите использовать по умолчанию. Например, выберите **Бухгалтер**.
3. Выберите **ОК**.

## <a name="a-namecompanyacompany" /><a name="company"></a>Компания

Организация выполняет роль контейнера данных в [!INCLUDE[prod_short](includes/prod_short.md)]. В базе данных может быть несколько организаций, но одновременно можно выбрать только одну из них. Организация по умолчанию называется CRONUS и содержит только демонстрационные данные.

Поле **Компания** показывает компанию, в которой вы сейчас работаете, и вы можете использовать его для переключения на другую компанию. Название организации всегда отображается в верхнем левом углу и работает как действие, которое вы можете выбрать, чтобы вернуться в ролевой центр.

> [!TIP]
> Вы также можете сменить компанию с помощью переключателя компаний (Ctrl+O). Дополнительные сведения об этой функции и других способах изменения компании или среды см. в разделе [Переключение на другую компанию или среду](ui-organization-switch.md).

Организация по умолчанию называется CRONUS и содержит только демонстрационные данные. Вы можете создать новую организацию с собственными данными. Дополнительные сведения см. в разделе [Создание новых организаций](about-new-company.md).

<!--
### <a name="to-change-the-company-name" />To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="a-namebadgeato-display-a-company-badge-for-quick-access-to-company-information" /><a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="a-namework-dateawork-date" /><a name="work-date"></a>Рабочая дата

Чаще всего в качестве рабочей даты используется сегодняшняя дата. Для выполнения таких задач, как проведение транзакций на определенную дату, отличную от текущей, может возникнуть потребность временно изменить рабочую дату.

> [!TIP]  
> Во всех полях даты можно ввести **t**, чтобы быстро ввести сегодняшнюю дату, и**w**, чтобы быстро ввести рабочую дату, т.е. значение в поле **Рабочая дата** на странице **Мои настройки**.

> [!IMPORTANT]  
> Если после изменения рабочей даты выполнить выход или переключиться на другую организацию, восстанавливается рабочая дата по умолчанию. Поэтому при следующем входе или переключении обратно в исходную организацию может потребоваться снова задать рабочую дату.

### <a name="work-date-indication" />Индикация рабочей даты

Рабочая дата играет решающую роль для страниц, которые можно редактировать. Когда рабочая дата не установлена на сегодняшнюю дату на редактируемой странице, на странице появляются два типа индикаторов:

* В верхней части страницы присутствует напоминание о том, какая дата установлена в качестве рабочей. Напоминание содержит прямую ссылку на настройку рабочей даты на странице **Мои настройки**, и при желании вы можете изменить дату. Из напоминания также можно закрыть напоминание, чтобы оно не отображалось до конца сеанса. Если вы не измените рабочую дату на "сегодня", напоминание появится при следующем входе в систему.

* Если вы закроете напоминание, рабочая дата будет отображаться в заголовке страницы.  

Если рабочая дата не установлена на текущий день (сегодня), то на всех страницах, в на которых возможно редактирование даты, текущая рабочая дата отображается в левом верхнем углу.

## <a name="a-nameregiona-region" /><a name="region"></a> Регион

Настройка **Регион** определяет способ отображения или форматирования дат, времени, чисел и валюты. Он также определяет, какой символ используется в качестве десятичного разделителя при использовании цифровой клавиатуры для ввода данных. Узнайте больше в разделе [Ввод данных](ui-enter-data.md#decimal).

## <a name="a-namelanguagea-language" /><a name="language"></a> Язык

Позволяет изменить язык отображения. Это поле отображается только в случае, когда для выбора доступно несколько языков.

Первоначальный язык определяется либо администратором, либо настройками браузера при входе в [!INCLUDE[prod_short](includes/prod_short.md)]. Язык, который вы установите, будет использоваться на всех устройствах, с которых вы входите в систему, например на телефоне или на планшете.

Дополнительные языки для [!INCLUDE[prod_short](includes/prod_short.md)] можно установить из AppSource. В то время как все поддерживаемые языки отображаются в списке, администратор должен установить соответствующее приложение языка в арендатор, прежде чем пользователи смогут переключиться на новый язык в [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone" />Часовой пояс

Определяет часовой пояс, в котором вы находитесь. При первом входе в систему [!INCLUDE [prod_short](includes/prod_short.md)] часовой пояс устанавливается на основе адреса вашей компании. Измените его, если он не соответствует вашему физическому местоположению.  

## <a name="notifications" />Уведомления

Выберите ссылку *Изменение времени получения уведомлений* для просмотра или изменения уведомлений, которые вы получаете об определенных событиях или изменениях статуса, например, когда вы собираетесь выставить счет клиенту, у которого имеется просроченная задолженность, или когда доступные запасы ниже количества, которое вы собираетесь продать. Узнайте больше в разделе [Управление уведомлениями](ui-smart-notifications.md).

## <a name="teaching-tips" />Обучающие советы

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-microsoft-trainingtrainingmodulespersonalize-ui-dynamics-365-business-centralindex" />См. соответствующее [обучение Microsoft](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also" />См. также

[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Изменение набора отображаемых функций](ui-experiences.md)  
[Создание новых организаций](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
