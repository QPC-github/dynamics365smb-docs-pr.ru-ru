---
title: Настройка шаблонов размещения
description: 'Используйте шаблоны размещения, чтобы в любой момент времени предлагать наиболее подходящие ячейки для ваших товаров.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7312, 7313, 7314, 7321, 7322, 7323, 7329'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-put-away-templates" />Настройка шаблонов размещения

С помощью функции расширенного подбора и размещения в любой момент времени отыскивается наиболее подходящая для товаров ячейка в соответствии с шаблоном размещения, настроенным для склада, заданными рейтингами ячеек и максимальными и минимальными количествами, заданными для фиксированных ячеек.  

Возможно настроить несколько шаблонов размещения и выбрать один из них для управления размещениями на всем складе. Также шаблон размещения возможно выбрать для каждого товара или единицы хранения, имеющих особые условия размещения.  

## <a name="to-set-up-put-away-templates" />Настройка шаблонов размещения

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок введите **Шаблоны размещения**, а затем выберите связанную ссылку.  
2. Выберите действие **Создать**.  
3. Введите код, являющийся уникальным идентификатором создаваемого шаблона.  
4. При необходимости введите краткое описание.  
5. Заполните первую строку требованиями, которые должны выполняться в первую очередь при предложении размещения.

    Например, если вы хотите, чтобы метод размещения по умолчанию основывался на фиксированных ячейках, выберите поле **Найти фиксированную ячейку**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Заполните вторую строку требованиями, которые определяют второй вариант выбора при поиске ячейки для размещения. Вторая строка используется только в том случае, если ячейка, соответствующая требованиям первой строки, не найдена.  
7. Продолжайте заполнять строки, пока полностью не опишете приемлемое расположение ячеек, используемых в процессе размещения.  
8. В последней строке шаблона размещения установите флажок **Найти плавающую ячейку**.  

Можно создавать различные шаблоны размещения и использовать их в соответствии с индивидуальными требованиями. В первую очередь выполняется обращение к шаблону размещения, выбранному для товара или единицы хранения, при наличии таковых. Если данные поля не заполнены, то используется шаблон размещения, выбранный для склада на экспресс-вкладке **Политики ячеек** в карточке склада.  

## <a name="see-related-microsoft-trainingtrainingmodulesput-away-templates" />См. соответствующее [обучение Microsoft](/training/modules/put-away-templates/)

## <a name="see-also" />См. также

[Обзор управления складом](design-details-warehouse-management.md)
[Запас](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
