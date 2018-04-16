---
title: "Необязательные действия для закрытия периодов | Microsoft Docs"
description: "В этом разделе описываются необязательные процессы и действия по закрытию учетных периодов в Business Central."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 42b5729d5d4013476fa0ff460db4dc999e629d66
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Обзор задач по закрытию учетных периодов
[!INCLUDE[d365fin](includes/d365fin_md.md)] не требует принудительного закрытия периодов, однако предусмотрено множество действий на конец периода (месяца), которые можно выполнить. В этом разделе представлен обзор дополнительных процессов и действий для закрытия периодов.  

## <a name="general-ledger"></a>Главная книга
* Укажите системные и пользовательские периоды учета.  

    Они определяют даты, между которыми возможен учет. В зависимости от бизнеса можно разрешить учет в начале процесса или ближе к концу. Дополнительные сведения см. в разделе [Определение периодов учета](finance-how-specify-posting-periods.md).  
* Внесите все необходимые корректировки в ГК.  
* Обновите и учтите типовые журналы.  
  <!--* Process Consolidations-->
* Создайте финансовые отчеты следующим образом:  
  * Откройте окно **Финансовый отчет** и выберите действие **Печать**.  

## <a name="sales-and-receivables"></a>Продажи и дебиторская задолженность
* Учтите все заказы на продажу, счета, кредит-ноты и заказы на возврат.  
* Выполните учет всех журналов кассовых поступлений.  
* Выполните обновление и учет типовых журналов, относящихся к продажам и расчетам с дебиторами.  
* Выполните выверку дебиторской задолженности с главной книгой.  
* Выполните пакетное задание **Удаление заказов на продажу, по которым выставлены счета**.  

## <a name="purchases-and-payables"></a>Покупки и кредиторская задолженность
* Выполните учет всех заказов на покупку, счетов, кредит-нот и заказов на возврат.  
* Выполните учет всех журналов оплат.  
* Выполните обновление и учет типовых журналов, относящихся к покупкам и расчетам с кредиторами.  
* Выполните отчет **Кредиторская задолженность по срокам давности** и проведите выверку кредиторской задолженности с главной книгой.  
* Выполните пакетное задание **Удалить заказы на покупку, по которым выставлены счета**.  

Основные средства
* Учет всех затрат на обслуживание, учтенных через журналы ОС или счета.
* Учет корректировок.
* Учет повышения стоимости.
* Учет амортизации.
* Обновление и учет типового журнала основных средств.

Межфирмен
* Обработка межфирменных транзакций

## <a name="calculate-and-process-sales-tax"></a>Расчет и обработка налога с продаж
* Завершите отчеты по НДС.  

## <a name="see-also"></a>См. также
[Закрытие года и периодов](year-close-years-periods.md)  
[Закрытие книг](year-close-books.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
