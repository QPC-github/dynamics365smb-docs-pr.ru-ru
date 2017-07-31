---
title: "Dynamics 365 for Financials и пакеты содержимого Power BI | Документы Майкрософт"
description: "Анализ данных, бизнес-аналитика и КПЭ на основе данных Financials становятся проще благодаря пакетам содержимого Power BI и Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 537effab2f406d619c5000efad12754db678e8b8
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017


---
# <a name="enabling-your-business-data-for-power-bi"></a>Включение бизнес-данных для Power BI
Анализ данных [!INCLUDE[d365fin](includes/d365fin_md.md)] становится проще благодаря Power BI и пакетам содержимого [!INCLUDE[d365fin](includes/d365fin_md.md)]. Power BI извлекает ваши данные и строки готовую панель мониторинга и отчеты на основе этих данных.  

Пакеты содержимого предварительно настроены для работы с данными продаж и финансовыми данными из демонстрационной организации, которую вы получаете при регистрации в [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].  

* Выберите любой из визуальных элементов панели мониторинга, чтобы открыть один из семи отчетов.  
* Отфильтруйте отчет или добавьте поля, которые вы хотите отслеживать.  
* Прикрепите настроенное представление к панели мониторинга для дальнейшего отслеживания.  
  Панель мониторинга и соответствующие отчеты обновляются ежедневно. Вы можете управлять графиком обновления и изменять периодичность построения набора данных.  

> [!NOTE]  
>   Также можно создать собственные отчеты и панели мониторинга в Power BI на основании данных [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Подключение ваших бизнес-данных к Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Доступ к [!INCLUDE[d365fin](includes/d365fin_md.md)] в Power BI
Чтобы увидеть данные [!INCLUDE[d365fin](includes/d365fin_md.md)] в Power BI, необходимо выполнить следующее:  

* Получите доступ к [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Financials](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Откройте Power BI. Дополнительные сведения см. в разделе [Power BI](https://powerbi.microsoft.com).

На сайте Power BI также можно просмотреть дополнительные сведения о [подключении к службам с помощью пакетов содержимого для Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Для получения доступа к данным [!INCLUDE[d365fin](includes/d365fin_md.md)] в Power BI на странице подключения необходимо указать следующие сведения:

| Поле | Описанием |
| --- | --- |
| **URL-адрес потока OData** |URL-адрес OData, чтобы с помощью Power BI можно было обращаться к данным вашей организации, например https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Метод проверки подлинности** |Выберите **Базовая**. |
| **Имя пользователя** |Ваше имя так, как оно отображается в вашей учетной записи в [!INCLUDE[d365fin](includes/d365fin_md.md)], например *Джон Смит*. |
| **Пароль** |Это ключ доступа к веб-службе для учетной записи пользователя в [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Иными словами, вам нужно получить из Financials 3 фрагмента информации: URL-адрес OData и ключ доступа к веб-службе для вашей учетной записи пользователя.  

### <a name="getting-the-url"></a>Получение URL-адреса
При добавлении [!INCLUDE[d365fin](includes/d365fin_md.md)] в Power BI вы должны указать URL-адрес, чтобы Power BI мог обращаться к данным вашей организации. На странице подключения URL-адрес называется **URL-адрес потока OData**, и он должен иметь следующий формат:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
В этом примере *mybusiness* — название вашей службы Financials, а *CRONUS US* — название демонстрационной организации. Символы *%20* обозначают пробел в названии.   
Чтобы получить URL-адрес, в [!INCLUDE[d365fin](includes/d365fin_md.md)] найдите и откройте окно **Веб-службы**. В этом окне перечисляются веб-службы, которые в настоящий момент доступны, и вы можете скопировать ссылку из поля **URL-адрес OData** для одной из веб-служб OData по умолчанию.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Получение имени пользователя и ключа доступа к веб-службе
Для использования данных из [!INCLUDE[d365fin](includes/d365fin_md.md)] в Power BI в окне **Подключиться к Financials** необходимо указать имя пользователя и пароль. Имя пользователя — это ваше имя так, как оно отображается в учетной записи в [!INCLUDE[d365fin](includes/d365fin_md.md)], чтобы приложение Power BI могло выполнить вход в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Пароль — это ключ доступа к веб-службе, который настраивается для учетной записи пользователя в [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Чтобы найти эти сведения, в [!INCLUDE[d365fin](includes/d365fin_md.md)] найдите окно **Пользователи**, а затем откройте карточку вашей учетной записи пользователя. На экспресс-вкладке **Общее** скопируйте содержимое поля **Имя пользователя** и на экспресс-вкладке **Доступ к веб-службе** скопируйте содержимое поля **Ключ доступа к веб-службе**. Если поле **Ключ доступа к веб-службе** не заполнено, то на ленте выберите **Изменить ключ доступа к веб-службе**, выберите поле **Бессрочный ключ**, а затем нажмите кнопку ОК. Теперь можно скопировать ключ.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Получение данных из [!INCLUDE[d365fin](includes/d365fin_md.md)]
На панели мониторинга [!INCLUDE[d365fin](includes/d365fin_md.md)] отображаются наиболее типичные отчеты,, которые можно использовать для отслеживания бизнеса. Данные извлекаются из вашей организации [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью веб-службы чтения данных в реальном времени. В [!INCLUDE[d365fin](includes/d365fin_md.md)] в окне **Веб-службы** перечисляются веб-службы, которые были настроены, в том числе следующие, которые используются пакетом содержимого в Power BI:  

* ItemSalesAndProfit  
* ItemSalesByCustomer  
* powerbifinance  
* SalesDashboard  
* SalesOpportunities  
* SalesOrdersBySalesPerson  
* TopCustomerOverview  

> [!NOTE]  
>   Если вы измените имя любой из этих веб-служб, данные не будут отображаться в Power BI.  
Если вы хотите добавить использование других данных в Power BI, необходимо найти таблицы в [!INCLUDE[d365fin](includes/d365fin_md.md)], предоставить к ним доступ в виде веб-служб, а затем добавить их в пакет содержимого. Это более сложный сценарий, и мы рекомендуем вам начать с данных, которые уже доступны в Power BI.  

## <a name="troubleshooting"></a>Устранение неполадок
Панель мониторинга Power BI основана на опубликованных веб-службах, которые перечислены выше, и содержит данные демонстрационной организации или вашей организации, если вы импортировали данные из текущего финансового решения. Однако если что-то работает некорректно, в этом разделе предложено обходное решение для типичных проблем.  

**"Ошибка при проверке параметра. Убедитесь, что все параметры допустимы"**  
Если после ввода URL-адреса [!INCLUDE[d365fin](includes/d365fin_md.md)] вы видите это сообщение, убедитесь, что соблюдаются следующие требования:  

* URL-адрес имеет следующую структуру:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Удалите весь текст после названия организации в скобках  
* Убедитесь, что в конце URL-адреса нет символа косой черты.  
* Убедитесь, что используется защищенное подключение (т. е. URL-адрес начинается с *https*).  

**"Сбой при входе"**  
Если при попытке войти в панель мониторинга с использованием учетных данных [!INCLUDE[d365fin](includes/d365fin_md.md)] появляется ошибка "Сбой при входе", это может быть вызвано одной из следующих причин:

* У используемой учетной записи нет разрешений на чтение данных [!INCLUDE[d365fin](includes/d365fin_md.md)] для вашей учетной записи.

    Проверьте учетную запись пользователя в [!INCLUDE[d365fin](includes/d365fin_md.md)] и убедитесь, что используются правильный ключ доступа к веб-службе и пароль, а затем повторите попытку.  
* Экземпляр [!INCLUDE[d365fin](includes/d365fin_md.md)], к которому вы пытаетесь подключиться, не имеет допустимого сертификата SSL. В этом случае вы получите более подробное сообщение об ошибке ("Не удается установить доверенные отношения SSL").

    > [!NOTE]  
>   Самозаверяющие сертификаты не поддерживаются.  

**"Проблема"**  
Если после проверки подлинности появляется сообщение об ошибке "Проблема", это чаще всего вызвано проблемой при подключении к данным из пакета содержимого.

* Проверьте, что URL-адрес имеет ранее указанную структуру:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Типичная ошибка — указать URL-адрес конкретной веб-службы:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance  
* Либо вы могли пропустить название организации:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/  

## <a name="see-also"></a>См. также
[Добро пожаловать в [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Миграция бизнес-данных из других финансовых систем](upload-data.md)  
[Использование [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] как источника данных Power BI](across-how-use-financials-data-source-powerbi.md)  
[Использование [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] как источника данных PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Использование [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] в Microsoft Flow](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]