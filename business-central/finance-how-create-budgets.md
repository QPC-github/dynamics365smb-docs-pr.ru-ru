---
title: Создание бюджетов ГК
description: Описывает порядок создания бюджетов ГК для прогнозирования различных финансовых действий и назначения измерений для целей бизнес-анализа.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="create-gl-budgets" />Создание бюджетов ГК

Путем создания бюджетов с различными кодами можно для одного и того же промежутка времени создать несколько бюджетов. Сначала настраивается код бюджета и заносятся бюджетные данные. Название бюджета затем помещается во все созданные бюджетные операции.  

При создании бюджетов для каждого из них можно определить четыре специальных измерения, называемых бюджетными измерениями. Бюджетные измерения для каждого бюджета выбираются из уже существующих измерений. Бюджетные измерения могут использоваться для установки фильтров бюджета и для добавления информации по измерениям к бюджетным операциям. Подробнее см. в статье [Работа с измерениями](finance-dimensions.md).

Бюджеты играют важную роль в бизнес-аналитике. В качестве примера можно назвать финансовую отчетность, основанную на бухгалтерских отчетах, которые включают операции бюджета, или сравнение бюджетных сумм с фактическими в плане счетов. Подробнее см. в статье [Бизнес-аналитика](bi.md).

В учете затрат работа с бюджетами затрат производится аналогичным образом. Прдробнее см. в статье [Создание бюджетов затрат](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget" />Создание бюджета ГК

1. Выберите значок ![Лампочка, которая открывает функцию «Что вы хотите сделать»](media/ui-search/search_small.png "Что вы хотите сделать"), значок, введите **Бюджеты ГК**, а затем выберите связанную ссылку.  
2. Выберите действие **Изменить список**, затем введите в поля требуемые данные. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Выберите действие **Изменить бюджет**.
4. В верхней части страницы **Бюджет** заполните поля соответствующим образом, чтобы определить, что в нем отображается.  

    Теперь будут отображаться только те операции, которые содержат название бюджета, введенное в поле **Название бюджета**. Поскольку название бюджета только что создано, соответствующие фильтру операции отсутствуют. Поэтому эта страница пустая.  
5. Чтобы ввести сумму, выберите соответствующую ячейку в матрице. Откроется страница **Операции бюджета ГК**.  
6. Создайте новую строку и заполните поле **Сумма**. Закройте страницу **Операции бюджета ГК**.  
7. Повторяйте шаги 5 и 6, пока не будут введены все суммы бюджета.  

> [!NOTE]  
> На экспресс-вкладке **Фильтры** можно фильтровать данные бюджета по бюджетным измерениям, настроенным для названия бюджета.

## <a name="exporting-and-importing-gl-budgets-with-excel" />Экспорт и импорт бюджетов ГК с помощью Excel

Как и практически для всех остальных страниц, данные со страниц бюджета можно экспортировать в Microsoft Excel для дальнейшей обработки или анализа. Подробнее см. в статье [Экспорт бизнес-данных в Excel](about-export-data.md)

> [!NOTE]
> План счетов, на котором основаны бюджеты ГК, имеет строки с типом счета "Заголовок", содержащие итоговые суммы для расположенных под ними строк. При экспорте бюджета ГК экспортируются данные для всех строк. независимо от типа счета. Однако только данные из строк с типом счета "Учетный" можно импортировать обратно. 

Соответственно, при импорте бюджета ГК любые значения, имеющиеся в строках заголовков, будут удалены. Это необходимо во избежание неправильных итогов после импорта данных, которые были созданы или отредактированы в Excel.

### <a name="scenario" />Сценарий

Вы знаете, что новые предусмотренные бюджетом затраты на зарплату будут составлять 1 200 000 единиц местной валюты (МВ). Вы хотите, чтобы отдел расчета заработной платы мог указать бюджет для трех конкретных строк (с типом счета "Учетный") — для сотрудников с полной занятостью, сотрудников с частичной занятостью и временных привлекаемых работников. Эти 3 строки группируются под строкой заголовка "Зарплаты".

Вы вводите 1 200 000 в строку "Заголовок", экспортируете бюджет в Excel, а затем отправляете его в отдел расчета зарплаты с указанием распределить 1 200 000 МВ.

Подразделение зарплат распределяет эту сумму по трем счетам учета. Когда производится импорт обратно в бюджет ГК, три счета заполняются новыми данными Excel, в сумме дающими 1 200 000 МВ, а строка заголовка остается пустой.

## <a name="see-related-microsoft-trainingtrainingmodulesbudgets-exchange-rates-dynamics-365-business-centralindex" />См. соответствующее [обучение Microsoft](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also" />См. также

[Экспорт бизнес-данных в Excel](about-export-data.md)  
[Финансы](finance.md)  
[Бизнес-аналитика](bi.md)  
[Настройка финансов](finance-setup-finance.md)  
[Главная книга и план счетов](finance-general-ledger.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
