---
title: "Порядок настройки базовых календарей | Документы Майкрософт"
description: "Можно присвоить базовый календарь своей организации и ее деловым партнерам, таким как клиенты, поставщики или склады. При расчете дат поставки и приемки по строкам будущих заказов продажи, покупки, перемещения и производства будут учитываться только дни, указанные в календаре как рабочие."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d37170cabe2b03200e3d3f5f7b5c2a679eb8f46c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-base-calendars"></a>Практическое руководство. Настройка базовых календарей
Можно присвоить базовый календарь своей организации и ее деловым партнерам, таким как клиенты, поставщики или склады. При расчете дат поставки и приемки по строкам будущих заказов продажи, покупки, перемещения и производства будут учитываться только дни, указанные в календаре как рабочие. Новый базовый календарь создается, чтобы установить нерабочие дни, которые необходимо ввести.  

## <a name="to-set-up-a-base-calendar"></a>Настройка базового календаря  
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Базовый календарь**, а затем выберите связанную ссылку.  
2.  Выберите действие **Создать**.  
3.  Заполните поле **Код**.  
4. Выберите действие **Ведение изменений базового календаря**.
5. В окне **Изменения базового календаря** используйте поле **Типовая система** для обозначения определенной даты или дня в качестве типового нерабочего дня. На выбор доступны параметры **Ежегодно** или **Еженедельно**.  

    Если выбран параметр **Ежегодно**, следует ввести соответствующую дату в поле **Дата**.  

    Если выбран параметр **Еженедельно**, следует ввести соответствующий день недели в поле **День**. Если это поле оставлено незаполненным, следует заполнить поле **Дата**. Поле **День** заполняется автоматически.  

При вводе информации выбирается поле **Нерабочий**. Можно снять флажок, чтобы сделать день рабочим.  
 После возвращения к карточке базового календаря базовый календарь будет обновлен в соответствии с введенной информацией о нерабочих днях. Указанные операции теперь отображаются красным цветом, и выбрано поле **Нерабочий**.  

> [!NOTE]  
>  При настройке нового базового календаря можно выбирать и копировать строки из уже существующего календаря. Используйте для этого соответствующее окно **Изменения базового календаря**.  

> [!IMPORTANT]  
>  Любой базовый календарь, определенный для поставщика или складской площадки, влияет на способ расчета дат и их округления до рабочих дней.
Определяет формулу даты для расчета времени, необходимого для пополнения товара. Это используется для расчета поля **Плановая дата приемки** при прямом расчете и поля **Дата заказа** при обратном расчете. См. раздел "Рассчитанное время подготовки заказа".

## <a name="lead-time-calculation"></a>Рассчитанное время подготовки заказа
Любой базовый календарь, определенный для поставщика или складской площадки, влияет на способ расчета дат и их округления до рабочих дней. Соответственно, два поля дат в строках заказа на покупку вычисляются следующим образом при различных условиях.

|Направление расчета|Календарь поставщика определен|Календарь поставщика не определен|
|---------------------|-----------------------|---------------------------|
|Вперед|планируемая дата приемки = дата заказа + запас времени для поставщика (согласно календарю поставщика и округленно до следующего рабочего дня сначала по календарю поставщика, а затем по складскому календарю)|плановая дата приемки = дата заказа + запас времени для поставщика (согласно складскому календарю)|
|Обратный|дата заказа = плановая дата приемки - запас времени для поставщика (согласно календарю поставщика и округленно до предыдущего рабочего дня сначала по календарю поставщика, а затем по складскому календарю)|дата заказа = плановая дата приемки - запас времени для поставщика (согласно складскому календарю)|

> [!NOTE]
> В дополнение к расчету времени подготовки, которое влияет на плановую дату приемки и дату заказа, как показано в таблице выше, время обработки на складе и страховой запас времени могут быть добавлены к формулам, чтобы получить значение в поле **Ожидаемая дата поставки** следующим образом: Плановая дата приемки + Страховой запас времени + Время обработки входящих товаров на складе = Ожидаемая дата поставки.

> [!Important]
> Если на складе используется календарь, сильно отличающийся от календаря поставщиков, важно при настройке по этим поставщикам использовать определенные календари, чтобы оптимально рассчитывать периоды работы с поставщиком. Дополнительные сведения о том, как настраивать календари поставщиков, см. в разделе "Присвоение базового календаря".

Содержимое поля **Расчет времени подготовки заказа** копируется либо из карточки товара, либо из карточки единицы хранения, если определен период ожидания для товара или если в окне **Каталог поставщиков товара** указан период ожидания для поставщика.

## <a name="to-customize-a-calendar"></a>Настройка календаря
Главной задачей при настройке личного календаря для вашей организации или организации-партнера является внесение необходимых изменений статуса рабочих и нерабочих дней.

Например, в базовом календаре все субботы, как правило, указаны нерабочими. В личном календаре для отдельного склада все субботы в ноябре и декабре, вплоть до сезона праздников, могут быть обозначены как рабочие дни.

В приведенном ниже примере личный календарь настраивается для склада. Предполагается, что для склада предварительно был назначен базовый календарь.

1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Склады**, а затем выберите связанную ссылку.
2. Откройте расположение, которое требуется обновить, затем выберите поле **Настроенный календарь**. Убедитесь, что в поле **Код базового календаря** выбран календарь.
3. В открывшемся окне **Операции настроенного календаря** выберите действие **Ведение изменений базового календаря**.
4. В **Изменения настроенного календаря** добавьте строки для записей настроенного календаря.

    При вводе строки устанавливается значок **Нерабочий**. Флажок можно снять при необходимости изменить статус, сделав день рабочим.

    Поле **Типовая система** может использоваться для установки определенной даты или дня в качестве типового нерабочего дня. На выбор доступны параметры **Ежегодно** или **Еженедельно**.

    Если выбран параметр **Ежегодно**, следует ввести соответствующую дату в поле **Дата**. Если выбран параметр **Еженедельно**, следует ввести соответствующий день недели в поле **День**. Если это поле оставлено незаполненным, следует заполнить поле **Дата**. Поле **День** заполняется автоматически. Может оказаться полезным обозначение определенной даты как нерабочего или рабочего дня.

5. Нажмите кнопку **ОК**.

В окне **Операции настроенного календаря** его данные будут обновлены в соответствии с внесенными изменениями.

На карточке "Склад" в поле **Настроенный календарь** содержится значение **Да**, указывая на наличие настроенного календаря.

> [!Important]
> Если поле **Код склада** в строке заказа не заполнено, для расчетов будет использоваться календарь организации.


Если поле **Код экспедитора** в строке заказа не заполнено, для расчетов будет использоваться календарь организации.

> [!NOTE]  
> При внесении изменений в базовый календарь, на основе которого были созданы личные календари, выполняется автоматическое обновление всех существующих личных календарей.

## <a name="to-assign-a-base-calendar"></a>Присвоение базового календаря  
Ниже приводится процедура определения сроков отгрузки в строках заказа на продажу для клиента в качестве примера.

Базовые календари назначаются вашей собственной организации, клиентам, поставщикам, складам и экспедиторам следующим образом:  

-   В карточках **Информация об организации** и **Клиент** экспресс-вкладке **Отгрузка** присвоен базовый календарь.  
-   В карточке **Поставщик** базовый календарь назначается на экспресс-вкладке **Получение**.  
-   В карточке **Склад** базовый календарь назначается на экспресс-вкладке **Склад**.  
-   В окне **Экспедиторы** базовый календарь присваивается в окне **Услуги экспедитора**.  

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Клиенты**, а затем выберите связанную ссылку.  
2.  Откройте карточку **Клиент**, чтобы назначить соответствующему клиенту базовый календарь.  
3.  На экспресс-вкладке **Отгрузка** в поле **Код базового календаря** введите базовый календарь, который нужно назначить.  

> [!IMPORTANT]  
>  -   Если организации не присвоен базовый календарь, все дни при расчете принимаются за рабочие.  
> -   Если строку заказа оставить незаполненной, все дни при расчете принимаются за рабочие.  
> -   Любой базовый календарь, определенный для поставщика или складской площадки, влияет на способ расчета дат и их округления до рабочих дней.

> [!NOTE]  
>  Прежде чем вводить в личный календарь данные, необходимо присвоить организации базовый календарь.  

## <a name="see-also"></a>См. также
[Покупки](purchasing-manage-purchasing.md)  
[Производство](production-manage-manufacturing.md)    
[Наличие](inventory-manage-inventory.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
