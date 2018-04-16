---
title: "Покупка товаров для продажи путем создания счетов покупки | Документы Майкрософт"
description: "Из счета продажи для покупки продуктов вы можете создать счет покупки для поставщика."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: d5ae63043a6f296de22f71c401a5686f970ad3a0
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="purchase-items-for-a-sale"></a>Покупка товаров для продажи
Из заказов на продажу и счетов продажи можно быстро создавать документы покупки на недостающие количества товаров, требуемые для продажи. Вы можете использовать две различные функции в зависимости от типа документа.
|Функция|Описанием|
|--------|-----------|
|**Создать заказы на покупку**|Из заказа на продажу эта функция позволяет создать заказ на покупку для каждого поставщика товаров в заказе на продажу. Вы можете изменить количество покупки, прежде чем создать заказы на покупку. Предлагаются только недостающие количества.
|**Создать счет покупки**|Из заказа на продажу и из счета продажи эта функция создает счет покупки для выбранного поставщика для всех строк или выбранных строк в документе продажи. Предлагается полное количество продажи.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Создание одного или нескольких заказов на покупку из заказа на продажу
Чтобы создать заказ на покупку для каждого недостающего количества товаров в заказе на продажу, можно воспользоваться функцией **Создать заказы на покупку**.

1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на продажу**, а затем выберите связанную ссылку.
2. Откройте заказ на продажу, для которого требуется купить товары.
3. Выберите действие **Создать заказы на покупку**.

    Откроется окно **Создать заказы на покупку**, содержащее строку для каждого отдельного товара в заказе на продажу. Строки для полностью доступных количеств продажи и недоступных количеств продажи (серые) отображаются по умолчанию. Вы можете выбрать действие **Показать недоступные** для просмотра только строк для недоступных количеств продажи.

    Поле **Кол-во для покупки** по умолчанию содержит недоступное для продажи количество.
4. Чтобы купить количество, отличное от недоступного для продажи, измените значение поля **Кол-во для покупки**.

    > [!NOTE]  
    >   Также можно изменить поле **Кол-во для покупки** в серых строках, даже если они представляют полностью доступное количество для продажи.
5. Нажмите кнопку **ОК**.

    Заказ на покупку создается для каждого поставщика товаров в заказа на продажу и включает все изменения количества, которые вы сделали в окне **Создать заказы на покупку**.
7. Продолжите обработку заказов на покупку, например изменив или добавив строки заказов на покупку. Дополнительные сведения см. в разделе [Регистрация покупок](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Создание счета покупки из заказа на продажу или счета продажи
Чтобы создать отдельный счет покупки для одно или нескольких строк в документе продажи, выбрав поставщика, у которого будет совершена покупка, воспользуйтесь функцией **Создать счет покупки**.

> [!NOTE]  
>   Эта функция создает счет покупки на точное количество товара в выбранном документе продажи. Чтобы изменить количество для покупки, необходимо изменить счет покупки после его создания.  

1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на продажу**, а затем выберите связанную ссылку.
2. Откройте счет продажи, для которого требуется купить товары.
3. Выберите одну или несколько строк счета продажи, которые требуется использовать в счете покупки. Для использования всех строк счета продажи выберите их все или не выбирайте ни одной.
4. Выберите действие **Создать счет покупки**.
5. Выберите **Все строки** или **Выбранные строки**, а затем нажмите кнопку **ОК**.  
6. В открывшемся списке поставщиков выберите поставщика, у которого требуется купить все товары, и нажмите кнопку **ОК**.

    Создается счет покупки с одной, несколькими или всеми строками из счета продажи.
7. Продолжите обработку счета покупки, например изменив или добавив строки счета покупки. Дополнительные сведения см. в разделе [Регистрация покупок](purchasing-how-record-purchases.md).

## <a name="see-also"></a>См. также
[Покупки](purchasing-manage-purchasing.md)  
[Регистрация покупок](purchasing-how-record-purchases.md)  
[Выставление счетов продажи](sales-how-invoice-sales.md)  
[Регистрация новых поставщиков](purchasing-how-register-new-vendors.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
