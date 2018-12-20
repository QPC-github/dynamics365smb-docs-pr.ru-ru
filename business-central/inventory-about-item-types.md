---
title: "Общее представление о типах товаров | Документы Майкрософт"
description: "Вы можете корректировать оценку стоимости запасов товара с помощью методов FIFO или средней себестоимости, например при изменении себестоимости по причине, не связанной с другими транзакциями."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b976ca548bf02511e818fa981395cb9261757468
ms.contentlocale: ru-ru
ms.lasthandoff: 09/28/2018

---
# <a name="about-item-types"></a>О типах товаров
В поле **Тип** в окне **Карточка товара** можно выбрать, для чего используется товар в вашем бизнесе и, поэтому, как он обрабатывается в системе. Имеются три варианта:

|Параметр|Типичное назначение|
|------|-----------|
|Запасы|Физический товар, например велосипед, как полной поддержки бизнеса.|
|Нескладируемый|Физический товар, например болт, для ограниченной поддержки бизнеса, например если товар используется только для внутренних целей и низкую себестоимость.|
|Сервис|Единица трудозатрат, такие как затраты времени на консультации, для ограниченной поддержки бизнеса.|

Тип **Складируемый** позволяет полное отслеживание количество и стоимости складских запасов. Таким образом, все типы товарных транзакций поддерживаются, и товары складируемого типа можно использовать со всеми функциями для обработки товаров.

Типы **Сервисный** и **Нескладируемый** не включают отслеживание количества и стоимости складских запасов. Таким образом, только некоторые типы товарных транзакции и функций поддерживаются.

Три типа товаров поддерживают следующие функции соответственно.

|Тип товара|Продажи|Закупки|Потребление работ|Потребление сервиса|Потребление при сборке|Производство Потребление|Выход при сборке|Выпуск продукции|Перемещение между складами|Физическая инвентаризация|Переоценка товаров на складе|Расчет себестоимости запасов|Трассировка товаров|Резервирование|Складирование|Планирование|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Запасы|Да|Да|Да|Да|Да|Да|Да|Да|Да|Да|Да|Да|Да|Да|Да|Да|
|Нескладируемый|Да|Да|Да|Да|Да|Да|Да|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|
|Сервис|Да|Да|Да|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|Нет|

> [!NOTE]
> Товары, которые вы предлагаете клиентам, но не хотите обрабатывать в своей системе до начала торговли ими, могут быть настроены как товары из каталога. Товары из каталога не следует путать с обычными товарами типа "Нескладируемые". Дополнительные сведения см. в разделе [Работа с товарами из каталога](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Товары клиентов, для которых вы проводите сервисное обслуживания, например принтер, называются сервисными товарами. Сервисные товары не имеют ничего общего с обычными товарами или товарами из каталога. Однако сервисные компоненты могут быть обычными товарами. Дополнительные сведения см. в разделе [Настройка сервисных товаров и компонентов сервисных товаров](service-how-setup-service-items.md).

## <a name="see-also"></a>См. также
[Регистрация новых товаров](inventory-how-register-new-items.md)  
[Настройка запасов](inventory-setup-inventory.md)  
[Управление себестоимостью товаров](finance-manage-inventory-costs.md)  
[Наличие](inventory-manage-inventory.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
