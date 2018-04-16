---
title: "Практическое руководство. Создание специальных заказов | Документы Майкрософт"
description: "Для отгрузки нескладируемого товара конкретному клиенту можно создать специальный заказ. Поставщик отгружает товар на склад организации, после чего этот товар отгружается в адрес клиента либо отдельно, либо вместе с другими товарами по другому заказу."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 84b7a66734b3da5bdbc474bc43e463481c7f6ba5
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="create-special-orders"></a>Создание специальных заказов
Для отгрузки нескладируемого товара конкретному клиенту можно создать специальный заказ. Поставщик отгружает товар на склад организации, после чего этот товар отгружается в адрес клиента либо отдельно, либо вместе с другими товарами по другому заказу.  

Специальные заказы предполагают наличие связи между заказом на покупку и заказом на продажу, позволяющей обеспечить подбор конкретного нескладируемого товара и его доставку клиенту.  

Перед использованием этой функции следует сначала настроить карточки клиента, поставщика и товара, которые необходимы для создания заказа.  

## <a name="to-create-a-special-order"></a>Создание специального заказа  
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказ на продажу**, а затем выберите связанную ссылку.  
2. Выберите действие **Создать**. Создайте и заполните заказ на продажу товара. Дополнительные сведения см. в разделе [Продажа продукции](sales-how-sell-products.md).
3.  На экспресс-вкладке **Строки** заполните строку продажи. В поле **Код закупки** выберите код покупки, для которого выбрано поле **Специальный заказ**.

    Теперь необходимо создать заказ на покупку на основе журнала заявок.  
4. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал заявок**, затем выберите связанную ссылку.  
5. Выберите действие **Специальный заказ**, затем выберите действие **Получить заказы на продажу**.  
6.  В окне **Получить заказы на продажу** отображаются результаты, в которых **Номер документа** является номером заказа на продажу. Нажмите кнопку **ОК**. Для товара создается строка журнала заявок.  
7.  В строке заявки выберите в поле **Указание** выберите **Новое**.  
8.  В окне **Журнал заявок** выберите действие **Выполнить указание**. Открывается окно **Выполнение указаний - заявка**. Нажмите кнопку **ОК**.  

    Отобразится сообщение о том, что созданы заказы на покупку. Нажмите кнопку **ОК**.  

Заказ на покупку, созданный как специальный заказ для заказа на продажу, учитывается системой планирования, поскольку балансирует спрос и предложение. Это означает, что заказ на покупку (предложение) остается связанным с заказом на продажу (требованием), даже если заказ на покупку мог бы быть использован для поставки по более раннему требованию. Дополнительные сведения см. в разделе [Сведения о проектировании. Политики дозаказа](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Нельзя использовать функцию специального заказа, если товар уже зарезервирован. Поэтому для товаров, которые продаются по специальным заказам, убедитесь, что значение в поле **Резервировать** в карточке товара не равно **Всегда**.  

## <a name="see-also"></a>См. также  
[Работа с нескладируемыми товарами](inventory-how-work-nonstock-items.md)  
[Продажи](sales-manage-sales.md)  
[Выполнение прямых поставок](sales-how-drop-shipment.md)   
[Сведения о проектировании: политики дозаказа](design-details-reservation-order-tracking-and-action-messaging.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
