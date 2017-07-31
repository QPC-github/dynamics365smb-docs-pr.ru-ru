---
title: "Обзор задач для управления покупками | Документы Майкрософт"
description: "Описывает задачи по управлению покупками или процессами покупок, включая работу счетов покупки и заказов на покупку."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 653cd9b5e9651f2039ab18f3e7a26b299238d817
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017


---
# <a name="purchasing"></a>Закупки
Счет покупки или заказ на покупку создается для записи стоимости покупок и отслеживания кредиторской задолженности. Если требуется управлять запасами, счета покупки также используются для динамического обновления уровней запасов, чтобы уменьшить себестоимости запасов и обеспечить лучшее обслуживание клиентов. Себестоимость покупок, включая затраты на обслуживание, и стоимость запасов, полученная из учета счетов покупки, влияют показатели прибыли и другие ключевые показатели эффективности финансовой деятельности, отображаемые на начальной странице.

Заказы на покупку следует использовать, если процесс покупки требует, чтобы вы могли регистрировать частичную приемку количества в заказе, например потому, что полное количество недоступно у поставщика. Если продажа товаров осуществляется путем непосредственной поставки от поставщика клиенту (прямая поставка), то также необходимо использовать заказы на покупку. Дополнительные сведения см. в разделе [Практическое руководство. Выполнение прямых поставок](sales-how-drop-shipment.md). Во всех других аспектах заказы на покупку аналогичны счетам покупки.

Счета покупки могут создаваться автоматически с помощью сервиса OCR (оптического распознавания) для преобразования счетов PDF от поставщиков в электронные документы, которые затем будут преобразованы в счета покупки рабочим процессом. Для использования этой функции необходимо сначала зарегистрироваться в сервисе OCR, а затем выполнить различные настройки. Дополнительные сведения см. в разделе [Практическое руководство. Обработка входящих документов](across-process-income-documents.md).      

Продукты и могут быть и товарами в запасах, и услугами. Дополнительные сведения см. в разделе [Практическое руководство. Регистрация новых товаров](inventory-how-register-new-items.md).

Для всех процессов покупки можно реализовать рабочий процесс утверждения, например, чтобы крупные покупки утверждались главным бухгалтером. Дополнительные сведения см. в разделе [Использование рабочих процессов утверждения](across-how-use-approval-workflows.md).

В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются. Эти задачи перечислены в обычном порядке их выполнения.

| Действие | Ссылка |
| --- | --- |
| Создайте счет покупки для записи соглашения с поставщиком о покупке продуктов с определенными условиями доставки и оплаты. |[Практическое руководство. Регистрация покупок](purchasing-how-record-purchases.md) |
| Создание счета покупки для всех или выбранных строк в счете продажи. |[Практическое руководство. Покупка товаров для продажи](purchasing-how-purchase-products-sale.md) |
| Выполните действие в учтенном счете неоплаченной покупки, чтобы автоматически создать кредит-ноту и либо отменить счет покупки, либо воссоздать его для внесения изменений. |[Практическое руководство. Исправление или отмена неоплаченных счетов продажи](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Создайте кредит-ноту покупки, чтобы отменить конкретный учтенный счет покупки для отражения продуктов, которые возвращаются поставщику, и собираемой суммы платежа. |[Практическое руководство. Обработка возвратов покупки или отмен](purchasing-how-register-new-vendors.md) |
| Создание карточки поставщика для каждого поставщика, у которого производится покупка. |[Практическое руководство. Регистрация новых поставщиков](purchasing-how-register-new-vendors.md) |

## <a name="see-also"></a>См. также
[Настройка покупки](purchasing-setup-purchasing.md)  
[Управление кредиторской задолженностью](payables-manage-payables.md)  
[Управление проектами](projects-manage-projects.md)    
[Цепочка поставок](madeira-supply-chain.md)      
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Общие бизнес-функции](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]