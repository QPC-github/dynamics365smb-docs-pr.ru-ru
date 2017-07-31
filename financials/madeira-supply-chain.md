---
title: "Функции цепочки поставок, поддерживаемые в Financials | Документы Майкрософт"
description: "Получите обзор продукта и узнайте об основных понятиях и процессах цепочки поставок, которые являются частью ERP-решения."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product overview, ERP
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3bae84075dc505aa9318590b1fac06e4844ffafe
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-supply-chain-functionality"></a>Обзор функций цепочки поставок
[!INCLUDE[d365fin](includes/d365fin_md.md)] поддерживает общие процессы цепочки поставок, хотя и с ограничением по потребностями оптовых организаций и дистрибьюторов без управляемой обработки склада.

В дополнение к документам счетов продажи можно управлять выполнением заказов с помощью заказов на продажу, что позволяет отгружать части количества по заказу, например вследствие того, что полное количество недоступно за раз. Поставки товаров можно отгрузить напрямую от поставщика клиенту, связав заказ на продажу с соответствующим заказом на покупку.

Количество запасов динамически обновляются по мере продажи и покупки товаров, и информация о наличии или предупреждения отображаются продавцам несколькими способами. Можно скорректировать количества запасов вручную, выполнив учет напрямую в операции книги товаров, например после инвентаризации. Можно предлагать и продавать товары клиентам без ведения запасов по товару. Если требуется включить такие нескладируемые товары в процесс цепочки поставок, достаточно преобразовать их в обычные товары.

В дополнение к документам счета покупки можно выполнять управление на стороне поставки с помощью заказов на покупку, что позволяет регистрировать частичные поступления количества по заказу. Простая функция планирования поставок позволяет инициировать покупку непосредственно из счета на продажу, который требует товаров.

И документы продажи, и документы покупки можно учесть как отгруженные, полученные либо полученные с выставленным счетом, что позволяет разделить ответственность ролей обработчиков заказов и учета.

В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.

| Действие | См. |
| --- | --- |
| Зарегистрировать новых клиентов, сделать предложения по продажам, продать продукты в заказах или счетах, например как прямые поставки, а также управлять возвратами продаж. |[Продажи](sales-manage-sales.md) |
| Зарегистрировать новых поставщиков, приобрести товары в заказах или счетах, например инициированные из счетов по продажам, и управлять возвратами покупок. |[Покупки](purchasing-manage-purchasing.md) |
| Зарегистрировать новые физические продукты или услуги, скорректировать количества запасов, а также управлять стоимостью запасов с помощью учета скорректированных себестоимостей в главной книге. |[Запасы](inventory-manage-inventory.md) |

## <a name="see-also"></a>См. также
[Настройка продаж](sales-setup-sales.md)  
[Управление дебиторской задолженностью](receivables-manage-receivables.md)     
[Настройка покупки](purchasing-setup-purchasing.md)  
[Управление кредиторской задолженностью](payables-manage-payables.md)    
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Общие бизнес-функции](ui-across-business-areas.md)
