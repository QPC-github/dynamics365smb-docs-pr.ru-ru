---
title: Как разместить товары с помощью складского размещения
description: 'Узнайте, как использовать документы размещения запасов для записи и разноски информации о размещении и приемке.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '7375,'
---
# <a name="put-items-away-with-inventory-put-aways" />Размещение товаров с помощью складского размещения

В [!INCLUDE[prod_short](includes/prod_short.md)] получение и размещение происходит с использованием одного из четырех методов, как описано в следующей таблице.

|Метод|Входящий процесс|Требуется приемка|Требуется размещение|Уровень сложности (подробнее см. в разделе [Обзор Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|А|Выполните учет приемки и размещения из строки заказа|||Нет отдельной складской операции.|  
|Б|Выполните учет приемки и размещения из документа складского размещения||Включено|База: последовательно по каждому заказу.|  
|Т|Выполните учет приемки и размещения из документа складской приемки|Включено||База: объединенная проводка получения/отправки для нескольких заказов.|  
|Д|Выполните учет приемки из документа складской приемки и учет размещения из документа складского размещения|Включено|Включено|Дополнительно|  

Подробнее см. в разделе [Исходящий складской поток](design-details-inbound-warehouse-flow.md).

Эта статья относится к методам B в таблице.

Если в вашем складе требуется обработка размещения, но не требуется обработка приемки, используйте документ **Размещение запасов** для записи и принятия к учету информации о размещении и приемке для ваших исходных документов. Входящие исходные документы могут быть заказами на покупку, заказами на возврат продажи и входящие заказы на перемещение.

> [!NOTE]
> Выходные данные производства и сборки также представляют собой входящие исходные документы. Дополнительные сведения об обработке выводов производства и сборки для внутренних процессов см. в разделе [Сведения о проектировании: внутренние складские потоки](design-details-internal-warehouse-flows.md).

Размещение запасов можно создать тремя способами:  

* Создание складского размещения непосредственно из самого документа-источника.  
* С помощью пакетного задания создайте складские размещения одновременно для нескольких исходных документов.  
* Создайте размещение в два шага: сначала выпустите исходный документ, чтобы сделать товары доступными для размещения. После этого размещение запасов можно создавать на странице **Размещение запасов** на основании исходного документа.  

## <a name="to-create-an-inventory-put-away-from-the-source-document" />Создание документа складского размещения из документа-источника

1. В исходном документе, который может быть заказом на покупку, заказом на возврат продажи, входящим заказом на перемещение или производственным заказом, выберите действие **Создать размещение/подбор запасов**.  
2. Установите флажок **Создать товарное размещение**.
3. Нажмите кнопку **ОК**. Создается новое размещение запасов.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job" />Создание нескольких размещений запасов с помощью пакетного задания

1. Выберите значок ![Лампочка, которая открывает функцию «Что вы хотите сделать»](media/ui-search/search_small.png "Что вы хотите сделать"), значок введите **Создание размещение/подбор/перемещение запасов**, а затем выберите связанную ссылку. 
2. На экспресс-вкладке **Запрос склада** с помощью полей **Документ-источник** и **Номер источника** отфильтруйте данные по определенному типу документов или диапазонам номеров документов. Например, можно создать размещения только для заказов на покупку.
3. На экспресс-вкладке **Параметры** установите флажок **Создать размещение запасов**.
4. Нажмите кнопку **ОК**. Создаются указанные размещения запасов.

## <a name="to-create-the-put-away-in-two-steps" />Чтобы создать размещение в два шага

### <a name="to-request-an-inventory-put-away-by-releasing-the-source-document" />Запрос складского размещения путем выпуска документа-источника

Когда вы выпускаете заказы на покупку, заказы на возврат продаж и входящие заказы на перемещение, товары в заказах становятся доступными для размещения. Следующие шаги описывают, как подготовить товары по заказу на покупку к размещению.  

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок введите **Заказы на покупку**, а затем выберите связанную ссылку.
2. Выберите заказ на покупку, который требуется выпустить, затем выберите действие **Выпустить**.  

### <a name="to-create-an-inventory-put-away-based-on-the-source-document" />Создание документа складского размещения из документа-источника

Сотрудник склада может создать новый размещение запасов на основе выпущенного исходного документа.

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Складское размещение**, а затем выберите связанную ссылку.  
2. Выберите действие **Создать**.  
3. В поле **Документ-источник** выберите тип документа-источника, для которого выполняется размещение.  
4. В поле **Номер источника** выберите документ.  
5. В качестве альтернативы выберите действие **Получить источник документа**, чтобы выбрать документ из списка входящих документов-источников, готовых к размещению на складе.  
6. Нажмите кнопку **ОК**, чтобы заполнить строки размещения в соответствии с выбранными документом-источником.  

## <a name="to-record-the-inventory-put-away" />Регистрация размещения запасов

1. На странице **складского размещения** откройте предварительно созданный документ размещения.  
2. В поле **Код ячейки** в строках размещения, ячейка, в которой требуется разместить товары, предлагается в соответствии с ячейкой товара по умолчанию. Если требуется, ячейку можно изменить.  
3. Произведите размещение и введите фактическое количество, которое было размещено, в поле **Кол-во для обработки**.

    Если вы должны поместить товары для одной строки в более чем одну ячейку, например из-за того, что назначенная ячейка полная, то используйте действие **Разделить строку** на экспресс-вкладке **Строки**. Действие создает строку для обработки оставшегося количества.  
4. По завершении размещения выберите действие **Учет**.  

    * Учет получения строк исходного документа, которые были помещены на хранение
    * Если на складе используются ячейки, в процессе учета создаются также складские операции, чтобы учесть изменения количества в ячейках.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="see-related-microsoft-trainingtrainingmodulesreceive-put-away-items" />См. соответствующее [обучение Microsoft](/training/modules/receive-put-away-items/)

## <a name="see-also" />См. также

[Обзор управления складом](design-details-warehouse-management.md)
[Запас](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
