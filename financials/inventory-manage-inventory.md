---
title: "Управление запасами | Документы Майкрософт"
description: "Описывает процедуру управления физическими продуктами, которыми вы торгуете, например обработку запасов на складе."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 920df314dc8b671d4e2d99d8449ee02a74cb9078
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017

---

# <a name="inventory"></a>Запасы
Для каждого физического продукта, которым осуществляется торговля, необходимо создать карточку товара с типом **Запасы**. Товары, которые предлагаются клиентам, но не содержатся на складе, можно зарегистрировать как нескладируемые товары, которые можно преобразовать в складируемые товары в случае необходимости. Можно увеличить или уменьшить количество товара на складе путем учета непосредственно в операциях книги товаров, например после проведения физической инвентаризации или если вы не регистрируете покупки.

Приходы и расходы склада также естественным образом записываются при учете документов покупки или продажи соответственно. Дополнительные сведения см. в разделах [Практическое руководство. Регистрация покупок](purchasing-how-record-purchases.md), [Практическое руководство. Продажа товаров](sales-how-sell-products.md) и [Практическое руководство. Выставление счетов продажи](sales-how-invoice-sales.md). Перемещение между складами изменяет количества на складах организации.   

Чтобы улучшить общую видимость товаров и упростить их поиск, можно классифицировать товары по категориям и назначить им атрибуты, по которым можно выполнять поиск и сортировку.

Следует убедиться, чтобы себестоимость товаров перенаправляется в соответствующую исходящую транзакцию продажи, особенно в ситуациях, когда производится продажа товаров перед выставлением счета за покупку этих товаров. Это называется коррекцией себестоимости, которую можно выполнить вручную или настроить для автоматического выполнения при учете товарной транзакции.

## <a name="inventory-reconciliation"></a>Выверка запасов
При учете складских транзакций, таких как расходные накладные, счета покупки или корректировки запасов измененные значения себестоимости товаров записываются в операциях стоимости товаров. Чтобы отразить такое изменение стоимости запасов в финансовых книгах, себестоимость товаров автоматически учитывается на соответствующих счетах запасов в главной книге. Для каждой учитываемой складской транзакции учитываются соответствующие стоимости в товарном счете, счете коррекции и счете себестоимости продажи в главной книге.

Даже несмотря на то что себестоимость запасов автоматически учитывается в главной книге, все равно необходимо гарантировать перенос стоимости проданных товаров в соответствующие исходящие транзакции. Это особенно важно в ситуациях, когда товары продаются до того, как на их покупку выставляется счет. Это называется корректировкой себестоимости. Себестоимость товаров автоматически корректируется при учете товарных транзакций, но себестоимость товаров также можно скорректировать вручную. Дополнительные сведения см. в разделе Практическое руководство. Коррекция себестоимости товаров.

|По |Ссылка |
|---|----|
|Создать карточку товара для каждого товара в запасах, которым вы торгуете.|[Практическое руководство. Регистрация новых товаров](inventory-how-register-new-items.md)|
|Структурирование родительских товаров, которые вы продаете как наборы, состоящие из компонентов родительского товара, или которые вы собираете для заказа или складирования.|[Практическое руководство. Работа со спецификациями](inventory-how-work-BOMs.md)|
|Сохраняйте общее представление о товарах и упрощайте их поиск и сортировку, систематизируя товары по категориям.|[Практическое руководство. Категоризация товаров](inventory-how-categorize-items.md)|
|Назначьте своим товарам атрибуты товара с различными типами значений, чтобы упростить сортировку и поиск товара.|[Практическое руководство. Работа с атрибутами товаров](inventory-how-work-item-attributes.md)|
|Создайте специальные карточки товара для товаров, которые предлагаются клиентам, но не хранятся на складе.|[Практическое руководство. Работа с нескладируемыми товарами](inventory-how-work-nonstock-items.md)|
|Выполнение физического подсчета, внесение положительных и отрицательных корректировок и изменение информации, например о складе или номере партии, в операциях книги товаров.|[Практическое руководство. Подсчет, корректировка и повторная классификация запасов](inventory-how-count-adjust-reclassify.md)|
|Просмотр доступности товаров на складе, по периоду, по событию продажи или покупки либо по их использованию в сборочных спецификациях.|[Практическое руководство. Просмотр наличия товара](inventory-how-availability-overview.md)|
|Перемещение складских товаров между складами с помощью заказов на перемещение, для управления складскими операциями или с помощью журнала реклассификации товаров.|[Практическое руководство. Перемещение запасов между складами](inventory-how-transfer-between-locations.md)|
|Повышение или понижение стоимости одного или нескольких товаров в запасах путем учета текущей вычисленной стоимости.|[Практическое руководство. Переоценка запасов](inventory-how-revalue-inventory.md)|
|Скорректируйте себестоимость товаров, автоматически или вручную, чтобы перенести изменения себестоимости из входящих операций на соответствующие исходящие операции.|[Практическое руководство. Корректировка себестоимости товаров](inventory-how-adjust-item-costs.md)|

## <a name="see-also"></a>См. также  
[Покупки](purchasing-manage-purchasing.md)  
[Sales](sales-manage-sales.md)    
[Цепочка поставок](madeira-supply-chain.md)  
[Работа с [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Общие бизнес-функции](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]