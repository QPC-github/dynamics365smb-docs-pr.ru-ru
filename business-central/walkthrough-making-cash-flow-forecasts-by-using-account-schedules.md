---
title: Создание прогнозов движения денежных средств с помощью финансовых отчетов
description: В этом пошаговом руководстве описывается использование финансовых отчетов для создания прогнозов движения денежных средств в Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: edupont
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports" />Пошаговое руководство: создание прогнозов движения денежных средств с помощью финансовых отчетов

В этом пошаговом руководстве описывается использование функции финансовых отчетов для создания прогнозов движения денежных средств. Финансовые отчеты выполняют расчеты, которые невозможно выполнить непосредственно в диаграмме счетов движения денежных средств. В финансовых отчетах можно настроить промежуточные итоги для приема и распределения движения денежных средств. Эти подытоги могут включаться в новые итоговые значения, которые затем можно использовать при создании прогнозов движения денежных средств.  

## <a name="about-this-walkthrough" />Об этом пошаговом руководстве

В этом пошаговом руководстве описываются следующие задачи:  

- Настройка нового названия финансового отчета о движении денежных средств.  
- Настройка строк финансового отчета.  
- Настройка нового определения столбца.  
- Назначение определения столбца финансовому отчету.  
- Просмотр и печать прогноза движения денежных средств.  

### <a name="prerequisites" />Предварительные требования

Для выполнения данного пошагового руководства необходимо выполнить следующие действия.  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Таблица движения денежных средств с зарегистрированными строками  

## <a name="roles" />Роли

В этом пошаговом руководстве демонстрируются задачи, выполняемые исполнителем следующей роли:  

- Контроллер  

## <a name="story" />Сюжет

Иван — контролер в CRONUS, который делает ежемесячные прогнозы движения денежных средств. Иван включает финансы, продажи, покупки, а также основные средства в прогнозах, и представляет их в CFO Sara для бизнес-аналитики.  

## <a name="setting-up-a-new-financial-report-name" />Настройка нового названия финансового отчета

Имя финансового отчета — это имя, которое вы даете прогнозу движения денежных средств, которое включает ряд определенных строк и определений столбцов.  

### <a name="set-up-a-new-financial-report-name" />Настройка нового названия финансового отчета

1. Выберите значок ![Лампочка, которая открывает функцию «Что вы хотите сделать»](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовые отчеты**, затем выберите связанную ссылку.  
2. На странице **Финансовые отчеты** выберите **Создать** для создания нового имени финансового отчета о движении денежных средств.  
3. В поле **Имя** введите **Прогноз**.  
4. В поле **Описание** введите **Прогноз движения денежных средств**.  
5. Оставьте поля **Определение строки** и **Определение столбца** пустыми.

## <a name="setting-up-row-definition-lines" />Настройка строк определения строк

После настройки имени финансового отчета Иван определяет каждую строку в финансовом отчете о движении денежных средств. Иван определяет строки для отображения в отчетах в дополнение к строкам, предназначенным только для вычислений.  

### <a name="set-up-row-definition-lines" />Настройка строк определения строк

1. На странице **Финансовые отчеты** выберите новый созданный вами финансовый отчет **Прогноз**, затем выберите действие **Изменить определение строк**.  
2. На странице **Определение строк** заполните каждую строку, как показано в следующей таблице.  

    > [!TIP]  
    > Используйте функцию **Вставить счета CF**, чтобы быстро отмечать требуемые счета движения денежных средств в плане счетов движения денежных средств и копировать их в строки определения строк.  

    | № строки | Описанием              | Тип группировки            | Группировка | Тип строки   | Тип суммы | Отобразить |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | РЕС10     | Расчеты с клиентами              | Счета операций движения денежных средств | 10       |Оборот | Чистая сумма  | Да  |
    | РЕС10     | Открытые заказы на продажу        | Счета операций движения денежных средств | 20       |Оборот | Чистая сумма  | Да  |
    | R10     | Арендная плата                  | Счета операций движения денежных средств | 30       |Оборот | Чистая сумма  | Да  |
    | R10     | Финансовые активы         | Счета операций движения денежных средств | 40       |Оборот | Чистая сумма  | Да  |
    | R10     | Реализация основных средств    | Счета операций движения денежных средств | 50       |Оборот | Чистая сумма  | Да  |
    | R10     | Частные инвестиции      | Счета операций движения денежных средств | 60       |Оборот | Чистая сумма  | Да  |
    | R10     | Прочие накладные   | Счета операций движения денежных средств | 70       |Оборот | Чистая сумма  | Да  |
    | R10     | Открытые сервисные заказы      | Счета операций движения денежных средств | 80       |Оборот | Чистая сумма  | Да  |
    | R20     | Всего денежных поступлений      | Формула                  | РЕС10      |Оборот | Чистая сумма  | Да  |
    | R30     | Платежи                 | Счета операций движения денежных средств | 1010     |Оборот | Чистая сумма  | Да  |
    | R30     | Открытые заказы на покупку     | Счета операций движения денежных средств | 1020     |Оборот | Чистая сумма  | Да  |
    | R30     | Затраты на персонал          | Счета операций движения денежных средств | 1030     |Оборот | Чистая сумма  | Да  |
    | R30     | Производственные затраты            | Счета операций движения денежных средств | 1040     |Оборот | Чистая сумма  | Да  |
    | R30     | Затраты на финансирование            | Счета операций движения денежных средств | 1050     |Оборот | Чистая сумма  | Да  |
    | R30     | Инвестиции              | Счета операций движения денежных средств | 1070     |Оборот | Чистая сумма  | Да  |
    | R30     | Личное потребление     | Счета операций движения денежных средств | 1090     |Оборот | Чистая сумма  | Да  |
    | R30     | НДС                  | Счета операций движения денежных средств | 1100     |Оборот | Чистая сумма  | Да  |
    | R30     | Прочие расходы           | Счета операций движения денежных средств | 1110     |Оборот | Чистая сумма  | Да  |
    | R40     | Всего денежных расходов | Формула                  | R30      |Оборот | Чистая сумма  | Да  |
    | R50     | Остаток                  | Формула                  | R20+R40  |Оборот | Чистая сумма  | Да  |
    | R60     | Фонды движения денежных средств          | Счета операций движения денежных средств | 2100     |Оборот | Чистая сумма  | Да  |
    | R70     | Общ. движ. ден. средств          | Формула                  | R50+R60  |Оборот | Чистая сумма  | Да  |

    > [!NOTE]
    > Номер ряда R10 используется для фиксации общих сумм счетов для дебиторской задолженности. Номер ряда R20 используется для расчета суммы всех кассовых поступлений. Номер ряда R30 используется для фиксации общих сумм счетов для кредиторской задолженности. Номер ряда R40 используется для расчета суммы всех денежных расходов. Номер ряда R50 используется для фиксации суммы кассовых излишков. Номер ряда R60 используется для фиксации ликвидных фондов. Номер ряда R70 используется для расчета прогнозируемого движения денежных средств.

## <a name="setting-up-a-new-column-definition" />Настройка нового определения столбца

Прежде чем Иван сможет распечатать прогноз движения денежных средств, ему нужно создать определение столбцов для числовой информации. В столбцах Иван определяет информацию, которую нужно использовать из строк.

- У первого столбца номер *C10* с названием **Сумма**, и в нем указан оборот.  
- У второго столбца номер *C20* и заголовок **Сальдо на дату** и содержит транзакции для данного периода.  
- У третьего столбец номер *C30* с заголовком **Весь год** и содержит оборот в сальдо по всему финансовому году.  
- Наконец, Иван назначает определение столбцов как параметр по умолчанию для финансового отчета **Прогноз**.  

### <a name="set-up-a-new-column-definition" />Настройка нового определения столбцов

1. На странице **Финансовые отчеты** выберите имя созданного вами нового финансового отчета **Прогноз**. На вкладке **Главная** в группе **Процесс** выберите **Изменить определение столбца**.

2. Создайте новое определение столбцов с именем **Движение денежных средств**.

3. Нажмите кнопку **ОК**.

4. Введите каждую строку точно так же, как показано в следующей таблице.

    |Номер столбца|Заголовок столбца|Тип столбца|Тип операций|Тип суммы|Отобразить|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |К10|Сумма|Оборот|Операции|Чистая сумма|Всегда|  
    |C20|Сумма до даты|Сальдо на дату|Операции|Чистая сумма|Всегда|  
    |C30|Весь фин. год|Весь фин. год|Операции|Чистая сумма|Всегда|

## <a name="assigning-the-column-definition-to-the-financial-report-name" />Назначение определения столбца имени финансового отчета

Иван теперь готов назначить определение столбцов названию финансового отчета.  

### <a name="assign-the-column-definition-to-the-financial-report-name" />Назначение определения столбца имени финансового отчета

1. На странице **Финансовые отчеты** выберите финансовый отчет **Прогноз**, затем выберите действие **Изменить определение столбца**.  
2. В поле **Имя** выберите определение столбцов **Движение денежных средств**, чтобы назначить в качестве определения столбцов по умолчанию.  

## <a name="view-and-print-the-cash-flow-forecast" />Просмотр и печать прогноза движения денежных средств

1. На странице **Финансовые отчеты** выберите финансовый отчет **Прогноз** для просмотра прогноза движения денежных средств.  
2. На странице **Финансовый отчет** можно выбрать сумму, затем просмотреть записи прогноза движения денежных средств, которые составляют сумму. Кроме того, можно просмотреть используемую формулу для расчета суммы. Можно также фильтровать суммы по дате и измерению.  
3. Выберите действие **Печать** для печати прогноза движения денежных средств.  

## <a name="see-related-microsoft-trainingtrainingmodulesforecast-cash-flow-dynamics-365-business-central" />См. соответствующее [обучение Microsoft](/training/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also" />См. также

[Работа с финансовыми отчетами](bi-how-work-account-schedule.md)  
[Анализ движения денежных средств в организации](finance-analyze-cash-flow.md)  
[Пошаговые описания бизнес-процессов](walkthrough-business-process-walkthroughs.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
