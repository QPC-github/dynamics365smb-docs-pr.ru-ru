---
title: 'Сведения о проектировании — потоки для производства, сборки и работ'
description: 'Узнайте о потоке между ячейками для подбора компонентов и размещения готовых товаров для сборки, производства или заказов на работу.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs" />Потоки для производства, сборки и работ

Внутренние потоки, такие как подбор компонентов и размещение готовых товаров для заказов на сборку, работ и производственных заказов, аналогичны входящим или исходящим потокам. Таким образом, многие процессы могут показаться знакомыми. В данной статье представлена информация о том, как работать с внутренними складскими потоками разного уровня сложности.

## <a name="overview-of-different-configuration-options" />Обзор различных параметров конфигурации

Вы можете настроить функции хранилища различными способами. Важно, чтобы выбранные вами варианты улучшали ваши процессы, не вызывая накладных расходов. В следующих таблицах описаны типичные конфигурации для работы с физическими товарами для производственных заказов, заказов на работу и заказов на сборку.

### <a name="inbound-flow-put-away" />Входящий поток (размещение)

|Уровень сложности|Описание|Параметры|Код ячейки|Входящий поток производственного заказа|Входящий поток заказа на сборку|Входящий поток заданий|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Нет отдельной складской операции.|Учет из заказов и журналов.||Необязательно. Управляется переключателем **Код ячейки обязателен**.|Производственный журнал -> Выходной журнал</br><br/> **ПРИМЕЧАНИЕ**. Вы можете разнести выходные данные, используя **Производственный журнал**.|Заказ на сборку|Размещение не применимо к работам|  
|Базовая|Последовательно по каждому заказу.|Требуется размещение. </br><br/> **ПРИМЕЧАНИЕ**. Хотя этот параметр называется **Требуется размещение**, все равно можно учитывать выход из исходных документов на складах, для которого установлен этот флажок. |Необязательно. Управляется переключателем **Код ячейки обязателен**.|Производственный заказ -> Размещение запасов|Заказ на сборку|Размещение не применимо к работам|
|Дополнительно|Консолидированные действия по размещению для нескольких исходных документов.|Требуется приемка + Требуется размещение|Необязательно. Управляется переключателем **Код ячейки обязателен**.|Производственный заказ(ы) -> Журнал выхода продукции|Заказы на сборку -> внутренние перемещения | Размещение не применимо к работам|
|Дополнительно|То же, что и выше + деятельность расширенного подбора и размещения|Расширенный подбор и размещение (зависимые переключатели будут включены автоматически)|Обязательно|То же, что выше.|То же, что выше.| Размещение не применимо к работам|

Некоторые конфигурации не позволяют использовать выделенные складские документы для регистрации размещения. Однако если в вашем складе используются ячейки, вы можете использовать типовые документы перемещения для перемещения произведенных или собранных товаров на склад. Подробнее см. в разделе [Внутреннее перемещение товаров в базовых конфигурациях склада](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick" />Исходящий поток (подбор)

|Уровень сложности|Описание|Параметры|Код ячейки|Исходящий поток производственного заказа|Исходящий поток заказа на сборку|Исходящий поток заданий|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Нет отдельной складской операции.|Учет из заказов и журналов.||Необязательно. Управляется переключателем **Код ячейки обязателен**.|Производственный журнал -> Журнал потребления </br><br/> **ПРИМЕЧАНИЕ**. Вы можете разнести потребление, используя **Производственный журнал**.|Заказ на сборку|Работа -> Журнал работ|  
|Базовая|Последовательно по каждому заказу.|Требуется подбор. </br><br/> **ПРИМЕЧАНИЕ**. Хотя этот параметр называется **Требуется подбор**, все равно можно учитывать выход из исходных документов на складах, для которого установлен этот флажок. <!-- ToDo Test prod output-->|Необязательно. Управляется переключателем **Код ячейки обязателен**.|Производственный заказ -> Подбор запасов|Заказ на сборку -> Перемещение запасов</br><br/>Функция **Перемещение запасов** может использоваться только с ячейками.|Работа -> Подбор запасов|
|Дополнительно|Консолидированные действия по подбору для нескольких исходных документов.|Требуется отгрузка + Требуется подбор|Необязательно. Управляется переключателем Код ячейки обязателен|Производственный заказ -> Складской подбор -> Журнал потребления |Заказы на сборку -> Складской подбор| Работа –> Складской подбор -> Журнал работ |
|Дополнительно|То же, что и выше + деятельность расширенного подбора и размещения|Расширенный подбор и размещение (зависимые переключатели будут включены автоматически)|Обязательно|То же, что выше.|То же, что выше.| Расширенный подбор и размещение не поддерживается для работ|

Аналогично входящему потоку, некоторые конфигурации не позволяют использовать выделенные складские документы для регистрации размещения. Если в вашем складе используются ячейки, вы можете использовать типовые документы перемещения для перемещения произведенных или собранных товаров. Подробнее см. в разделе [Перемещение товаров](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity" />Склады без выделенной складского задания

Даже если у вас нет выделенных складских заданий, вы, вероятно, захотите отслеживать такие вещи, как потребление и объем производства. В следующих статьях содержится информация о том, как обрабатывать поступления для исходных документов.

* [Регистрация потребления и выхода для одной строки запущенного производственного заказа](production-how-to-register-consumption-and-output.md)
* [Сборка товаров](assembly-how-to-assemble-items.md)
* [Учет потребления или использования для работ](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration" />Базовая конфигурация склада

Входящие и исходящие потоки в базовой конфигурации склада включают следующие параметры на странице **Карточка склада** для склада:

* Для входящего потока (размещения) включите переключатель **Требуется размещение**, но выключите **Требуется приемка**.
* Для входящего потока (подбор) включите переключатель **Требуется подбор**, но выключите **Требуется отгрузка**.

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration" />Перемещение в производство и из него в базовой конфигурации склада

Используйте документы **Подбор запасов** для подбора производственных компонентов в потоке производства. Чтобы разместить производимую вами продукцию, используйте документы **Размещение запасов**.

Для местоположений, в которых используются ячейки, документы перемещения запасов особенно полезны для списания компонентов. Дополнительные сведения о списании потребления компонентов из входящей ячейки или ячейки готовой продукции см. в разделе [Списание производственных компонентов на складе](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Перемещение запасов является важным документом, если вы используете методы списания **Подбор + прямой** или **Подбор + обратный**. Дополнительные сведения см. в разделе [Методы списания](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Поля **Код входящей ячейки**, **Код ячейки готовой продукции** и **Код ячейки комплектования** для склада или станции/карточках рабочего центра определяют потоки по умолчанию в производственные области и из них.
* Управляйте перемещением произведенных товаров на странице **Внутреннее перемещение** без привязки к производственному заказу.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration" />Перемещение в сборку и из него в базовой конфигурации склада

Учет выхода и потребления сборки непосредственно из заказа на сборку.

> [!NOTE]
> Документы **Подбор запасов** и **Размещение запасов** не поддерживаются для заказов на сборку.

Для складов с использованием ячеек:

* Используйте документы **Перемещение запасов** для перемещения компонентов сборки в область сборки.
* Поля **Код входящей сборочн. ячейки** и **Код исходящей сборочн. ячейки** в карточке склада определяют потоки в области сборки и из них по умолчанию.
* Управляйте перемещением собранных товаров на странице **Внутреннее перемещение** без привязки к заказу на сборку.

[!INCLUDE [prod_short](includes/prod_short.md)] поддерживает потоки сборки "сборка на склад" и "сборка на заказ". Подробнее см. в разделе [Сборка на заказ и сборка на склад](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). Что касается управления складом, сборка на склад является частью внутреннего складского потока, а сборка на заказ — в исходящем складском потоке. Подробнее см. раздел [Обработка товаров сборки для заказа со складскими подборками](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration" />Потоки для управление проектами в базовой конфигурации склада

Используйте документы **Складской подбор** для подбора производственных компонентов к управлению проектами.

Для склада, в котором используются ячейки, поле **Код ячейки для работы** в этом складе определяет потоки по умолчанию для управления проектом.

## <a name="advanced-warehouse-configurations" />Расширенные конфигурации склада

Входящие и исходящие потоки в расширенной конфигурации склада включают следующие параметры на странице **Карточка склада** для склада:

* Для входящего потока (размещения) включите переключатель **Требуется приемка** и **Требуется размещение**.
* Для входящего потока (подбор) включите переключатель **Требуется отгрузка** и **Требуется приемка**.

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations" />Перемещение в производство и из него в расширенной конфигурации склада

Используйте документы **Складской подбор** и страницу **Журнал подбора**, чтобы подобрать компоненты для производства.

Для складов с использованием ячеек:

* Документы **Складское перемещение** и страница **Журнал перемещения** особенно полезны для списания компонентов. Подробнее см. в разделе [Списание производственных компонентов на складе](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-a-advanced-warehouse-configuration).
* Поля **Код входящей ячейки**, **Код ячейки готовой продукции** и **Код ячейки комплектования** в складе или станции/рабочем центре определяют потоки по умолчанию в производственные области и из них. 
* Управляйте перемещением произведенных товаров на странице **Журнал перемещения** или **Внутреннее складское размещение** без привязки к производственному заказу.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations" />Перемещение в сборку и из него в расширенной конфигурации склада

Используйте документы **Складской подбор** и страницу **Журнал подбора**, чтобы подобрать компоненты для сборки.

Для складов с использованием ячеек:

* Поля **Код входящей сборочн. ячейки** и **Код исходящей сборочн. ячейки** в складе определяют потоки в области сборки и из них по умолчанию.
* Управляйте перемещением сборочных элементов на странице **Журнал перемещения** или **Внутреннее складское размещение** без привязки к заказу на сборку.

[!INCLUDE [prod_short](includes/prod_short.md)] поддерживает потоки сборки "сборка на склад" и "сборка на заказ". Подробнее см. в разделе [Сборка на заказ и сборка на склад](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Сборка на склад является частью внутреннего складского потока, а сборка на заказ — в исходящем складском потоке. Подробнее см. в разделе [Обработка товаров сборки на заказ складских товаров в складских отгрузках](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations" />Потоки для управление проектами в расширенной конфигурации склада

Используйте документы **Складской подбор** и страницу **Журнал подбора**, чтобы подобрать компоненты в потоке для управления проектами.

Для складов, в которых используются ячейки, поле **Код ячейки для работы** в этом складе определяет потоки по умолчанию для управления проектами.

## <a name="see-also" />См. также

[Обзор управления складом](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
