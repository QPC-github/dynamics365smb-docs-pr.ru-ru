---
title: "Как принимать товары | Документы Майкрософт"
description: "Если товары поступают на склад, настроенный на обработку складской приемки, необходимо получить строки выпущенных документов-источников, на основании которых были получены товары."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 34960041320f595b504c9f16913db07c1dd3f053
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-receive-items"></a>Практическое руководство. Приемка товаров
Если товары поступают на склад, который не был настроен для обработки складской приемки, вы просто регистрируете приемку в соответствующем бизнес-документе, таком как заказ на покупку, заказ на возврат продажи или входящий заказ на перемещение.

Если товары поступают на склад, настроенный на обработку складской приемки, необходимо получить строки выпущенных документов-источников, на основании которых были получены товары. Если используются ячейки, можно либо принять в ячейку, предложенную по умолчанию, либо, если данный товар не был представлен на этом складе ранее, выбрать ячейку, в которую его следует поместить. Затем следует ввести количество полученного товара и учесть приемку.  

## <a name="to-receive-items-with-a-purchase-order"></a>Приемка товаров с помощью заказа на покупку
Ниже описано, как получать товары с использованием из заказа на покупку. Шаги аналогичны для заказов на возврат продажи и заказов на перемещение.  
1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на покупку**, затем выберите связанную ссылку.
2. Откройте существующий заказ на покупку или создайте новый заказ. Дополнительные сведения см. в разделе [Практическое руководство. Регистрация покупок](purchasing-how-record-purchases.md).
3. В поле **Кол-во для получения** введите полученное количество.

    Значение в поле **Полученное кол-во** обновляется соответствующим образом. Если это частичная приемка, то это значение меньше значения в поле **Количество**.
4. Выберите действие **Учесть**.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Приемка товаров с помощью складской приемки
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Складские приемки**, а затем выберите связанную ссылку.  
2.  Выберите действие **Создать**.  

    Заполните поля на экспресс-вкладке **Общее**. При получении строк документа-источника некоторая информация копируется в каждую строку.  

    Для конфигурации склада с расширенным подбором и размещением: если на складе имеются стандартные зоны и ячейки для приемки, то поля **Код зоны** и **Код ячейки** заполняются автоматически, но в них можно вносить необходимые изменения.  

    > [!NOTE]  
    >  Если требуется принять товары с кодами класса склада, отличающимися от кода класса ячейки из поля **Код ячейки** заголовка документа, то перед получением строк документа-источника для этих товаров необходимо удалить содержимое поля **Код ячейки** в заголовке документа.  
3.  Выберите действие **Получить исходные документы**. Откроется окно **Документы-источники**.

    В новой или открытой складской приемке можно использовать окно **Фильтры для получения первичных документов**, чтобы получить строки выпущенных исходных документов, определяющих товары, которые должно быть получены или отгружены.

    1. Выберите действие **Исп. фильтры для получ. исх. документов**.  
    2. Для настройки нового фильтра введите описательный код в поле **Код**, затем выберите действие **Изменить**.  
    3. Определите тип строк документа-источника, которые следует извлечь, заполнив соответствующие поля фильтра.  
    4. Выберите действие **Выполнить**.  

    Все выпущенные строки документа-источника, которые удовлетворяют критериям фильтрации, теперь вставляются в окно **Складская приемка**, из которого вы активировали функцию фильтра.  

    Определяемые пользователем комбинации фильтров сохраняются в окне **Фильтры для получения первичных документов** для последующего использования. Количество комбинаций фильтров не ограничено. Можно в любой момент изменить критерии, выбрав действие **Изменить**.

4.  Выберите исходный документ, на основании которого будет проводиться приемка, затем выберите кнопку **OK**.  

    Строки документа-источника отображаются в окне **Складская приемка**. Поле **Кол-во для получения** заполняется информацией о недопоставленном количестве для каждой строки, но при необходимости количество можно изменить. Если содержимое поля **Код ячейки** на экспресс-вкладке **Общее** удалено до получения строк, необходимо ввести соответствующий код ячейки в каждой строке приходной накладной.  

    > [!NOTE]  
    >  Чтобы заполнить поле **Кол-во для получения** для всех строк с нулевыми значениями, выберите действие **Удалить кол-во для получения**. Чтобы повторно заполнить поле значением недопоставленного количества, выберите действие **Автозаполнение кол-ва для получения**.  

    > [!NOTE]  
    >  Невозможно принять товаров больше, чем указано в поле **Недопоставленное кол-во** строки документа-источника. Чтобы получить дополнительные товары, нужно, воспользовавшись функцией фильтрации для документов, содержащих определенный товар, вызвать другой документ-источник со строкой для данного товара.  

5.  Учесть складскую приемку. Поля количества обновляются в документах-источниках, а товары записываются в складские запасы организации.  

Если применяется складское размещение, строки отправляются приходной накладной функции размещения на складе. Товары, хотя он и приняты, не готовы к подбору, пока они не размещены. Принятые товары определяются как доступные запасы только после регистрации размещения.  

Если складское размещение не применяется, но используются ячейки, регистрируется размещение в ячейке, указанной в строке документа-источника.  

> [!NOTE]  
>  При использовании функции **Учет и печать** осуществляется и учет приемки, и печать инструкции по размещению, которая указывает, куда нужно поместить товары на хранение.  
>   
>  Если на складе применяется расширенный подбор и размещение, для вычисления наилучшего места для размещения товаров используются шаблоны размещения. Затем эти сведения печатаются в инструкции по размещению.  

## <a name="see-also"></a>См. также  
[Управление складом](warehouse-manage-warehouse.md)  
[Наличие](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)     
[Управление сборкой](assembly-assemble-items.md)    
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
