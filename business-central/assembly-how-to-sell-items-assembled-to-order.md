---
title: "Практическое руководство. Продажа товара, собранного на заказ | Microsoft Docs"
description: "Если товар настроен для сборки на заказ, его наличие на складе не ожидается, и товар должен быть собран специально для заказа на продажу. При вводе товара в строке заказа продажи автоматически создается сборочный заказ и связывается с заказом на продажу."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b03cc5a21ca49f85fa859736b074bd72cb5c6499
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="sell-items-assembled-to-order"></a>Продажа товара, собранного на заказ
Если поле **Политика сборки** в карточке товара сборочного элемента имеет значение **Сборка на заказ**, данный элемент товара не относится к складским запасам, он должен быть специально собран к заказу на продажу. При вводе товара в строке заказа продажи автоматически создается сборочный заказ и связывается с заказом на продажу.  

> [!NOTE]  
>  Если некоторые товары сборки на заказ уже находятся на складе, можно вычитать это количество из сборочного заказа и зарезервировать его со склада. Дополнительные сведения см. в разделе [Продажа складских товаров в процессах со сборкой на заказ](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

В рамках этой процедуры обрабатывается продажа товара, который будет собран в соответствии с спецификациями, которые запрошены клиентом. В число этих действий включено введение строки заказа на продажу, настройка сборочного элемента путем изменения его компонентов и ресурсов, проверка доступности для определения даты доставки и выпуск заказа на продажу для сборки и немедленной отгрузки.  

> [!NOTE]  
>  Следующая процедура не включает стандартные шаги заказа на продажу до шага, на котором указывается товар сборки на заказ для строки заказа на продажу.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Продажа товара, собранного на заказ  
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на продажу**, а затем выберите связанную ссылку.  
2.  Создайте заказ на продажу. Дополнительные сведения см. в разделе [Продажа продукции](sales-how-sell-products.md).  
3.  В поле **Номер** введите товар, который настроен для сборки на заказ.  
4.  В поле **Код склада** укажите, с какого склада должен быть продан товар. Процесс сборки будет выполняться на этом складе.  
5.  В поле **Количество** укажите, сколько единиц будет продано.  

    > [!NOTE]  
    >  Если один или несколько компонентов запрошенного количества сборочных элементов не доступны, откроется окно предупреждения о доступности. Дополнительные сведения см. в разделе Доступность сборки.  

    Теперь сборочный заказ создается автоматически и привязывается к строке заказа на продажу. Срок выполнения этого сборочного заказа синхронизируется с датой отгрузки в строке заказа на продажу.  

    Количество, подлежащее продаже, копируется в поле **Количество для сборки на заказ**, в котором отражается, что для настройки товара требуется полное количество в товара в строке продажи, которое необходимо собрать для заказа. Можно сокращать количество сборок на заказ, если известно, что некоторые товары уже доступны. Дополнительные сведения см. в разделе [Продажа складских товаров в процессах со сборкой на заказ](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Чтобы отразить потребность клиента в дополнительном товаре в комплекте, на экспресс-вкладке **Строки** выберите действие **Строка**, выберите действие **Сборка на заказ**, затем выберите действие **Строки сборки на заказ** для просмотра и изменения стандартных сборочных компонентов. В качестве альтернативы выберите поле **Количество для сборки на заказ**.  
7.  В окне **Строки сборки на заказ** создайте новую строку типа **Товар** для содержимого дополнительного запрошенного комплекта. Строка представляет дополнительный сборочный компонент.  

    Можно также настроить заказ путем увеличения количества одного стандартного товара в комплекте. Для этого можно увеличить значение в поле **Кол-во в** конкретной строки сборочного заказа.  

    > [!NOTE]  
    >  Окно **Строки сборки на заказ** содержит только основные поля, которые менеджер должен использовать для настройки списка компонентов, добавления номеров трассировки товаров или для решения проблем с наличием компонентов. Чтобы просмотреть дополнительные сведения по заказу на сборку, в частности дату начала заказа на сборку, выберите действие **Показать документы**. При этом откроется полное отображение сборочного заказа, связанного со строкой заказа продажи. Содержимое большинства полей в заголовке сборочного заказа невозможно изменить и учесть в выходе при сборке, так как для этого требуется выполнить учет отгрузки из строки заказа на продажу.  
    >   
    >  В заголовке связанных сборочных заказов только поле **Дата начала** может быть изменено, чтобы работники сборки могли указать дату начала процесса, которая предшествует сроку выполнения. Все поля в строках связанного сборочного заказа можно изменить так, чтобы работники склада могли в процессе вводить цифры потребления.  

8.  Просмотрите проблемы доступности компонентов или примите соответствующие меры. Например, выберите доступный товар для замены или настройте более поздний срок оплаты.  
9. Закройте окно **Строки сборки на заказ**. Связанный сборочный заказ готов к началу сборки заказных товаров по сроку выполнения.  
10. В заказе на продажу выберите действие **Выпустить**, чтобы уведомить сборочный участок, что процесс сборки может быть запущен.  
11. В сборочном отделе выполните шаги по сборке товаров, которые продаются в рамках этой процедуры. Дополнительные сведения см. в разделе [Сборка товаров](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>См. также  
[Управление сборкой](assembly-assemble-items.md)  
[Работа со спецификациями](inventory-how-work-BOMs.md)  
[Наличие](inventory-manage-inventory.md)  
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
