---
title: Стандартные строки типовых покупок
description: Настройте часто используемые строки покупок, а затем вставьте их в документы покупки, чтобы быстро заполнять строки стандартной информацией.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, purchase, replenishment
ms.search.form: 177
ms.date: 07/06/2022
ms.author: a-reishima
ms.openlocfilehash: 08fda9bb2478cb7453bd16d5392139fba1408f87
ms.sourcegitcommit: 5560a49ca4ce85fa12e50ed9e14de6d5cba5f5c3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2022
ms.locfileid: "9144420"
---
# <a name="create-recurring-purchase-lines"></a>Создание типовых строк покупок

Если вам часто приходится создавать строки покупки с одинаковыми данными, вы можете настроить стандартные строки, которые затем можно вставлять в документы типовых покупок, например для типовых заказов на пополнение.

## <a name="set-up-recurring-purchase-lines"></a>Настройка типовых строк покупок

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") и введите **Строки типовых покупок**, а затем выберите связанную ссылку.
2. На странице **Строки типовых покупок** выберите действие **Создать**.
3. На экспресс-вкладке **Общее** заполните необходимые поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. На экспресс-вкладке **Строки** заполните поля, которые отражают стандартные строки, которые ожидаются как типовые в документах покупки.

> [!NOTE]
> Невозможно определить цены в строках типовых покупок, поскольку цены, скидки и т. д, вычисляются на базе фактических документов покупки после вставки строк типовых покупки.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-purchase-lines-to-a-vendor"></a>Назначение типовых строк покупки поставщику

Назначьте одну или несколько строк типовых покупок поставщику, чтобы они были доступны для вставки в документы покупки для этого поставщика.

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") и введите **Поставщики**, а затем выберите связанную ссылку.
2. Откройте карточку для соответствующего поставщика.
3. Выберите значение **Строки типовых покупок**.
4. На странице **Строки типовых покупок** выберите коды для строк типовых покупок, которые должны быть доступны для вставки в документы покупки для этого поставщика.
5. Заполните дополнительные поля, чтобы определить, когда, как и где строки типовых покупок будут использоваться.
6. В четырех полях, в которых выбирается, как строки вставляются в документы каждого типа, выберите один из следующих параметров:

|Параметр|Описанием|
|------|-----------|
|**Ручной**|Следует вручную найти и вставить строку типовых покупок, существующую для поставщика.|
|**Автоматически**|Если несколько строк типовых покупок существуют для поставщика, вы получите уведомление, в котором можно выбрать, какую из них вставить. Если имеется только одна строка типовых покупок, она вставляется автоматически.<br /><br />Это работает только в случае, когда новый документ был создан из списка документов, например путем выбора действия **Создать** на странице **Заказы на покупку**. Это не работает, если документ был создан, например, из карточки поставщика.|
|**Всегда спрашивать**|Появляется уведомление, и отображаются все существующие строки типовых покупок, чтобы можно было выбрать одну.

## <a name="insert-recurring-purchase-lines-on-a-purchase-invoice"></a>Вставка строк типовых покупок в счет покупки

Если существуют строки типовых покупок для поставщика, вы можете вставить их или добавлять их автоматически в документы покупки всех типов, например в счета покупки. Если активизирован параметр **Всегда спрашивать**, то при назначении строк типовых покупок поставщикам вы получите уведомление о том, существуют ли строки типовых покупок.

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать"), значок введите **Счета покупки**, а затем выберите связанную ссылку.
2. Откройте счет покупки, в который требуется вставить одну или несколько строк типовых покупок.
3. Выберите значение **Получить строки типовых покупок**.
4. На странице **Строки типовых покупок** нажмите кнопку выбора в поле **Код**, а затем выберите набор строк типовых покупок.
5. Нажмите кнопку **ОК**, чтобы вставить в счет строки типовых покупок, которые можно потом использовать повторно или изменить.

## <a name="see-also"></a>См. также

[Покупки](purchasing-manage-purchasing.md)  
[Настройка покупок](purchasing-setup-purchasing.md)  
[Создание типовых продаж](sales-how-work-standard-lines.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]