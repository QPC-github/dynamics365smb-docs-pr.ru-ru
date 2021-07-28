---
title: Проектные о покупках и аналитика
description: Посмотрите, какие отчеты о покупках и аналитика доступны в стандартной версии Business Central, чтобы вы могли отслеживать свой бизнес.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 5fc64db4120b80203f99742ed3ed834b23370c47
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216392"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Отчеты о покупках и аналитика в Business Central

Отчетность о покупках в [!INCLUDE [prod_short](includes/prod_short.md)] позволяет профессионалам закупок и бизнеса получать информацию и статистические данные о текущей и прошлой деятельности по покупке.  

## <a name="reports"></a>Отчеты

В следующей таблице описаны некоторые ключевые отчеты отчетности о покупках.

|Отчет |ИД объекта|Описание  |
|---------|---------|---------|
|**Статистика покупок**|312|Показывает статистику покупок по каждому поставщику. Сюда входит информация за пять периодов, начиная с указанной вами даты.<br>
Отчет включает общую информацию о покупках, платежах, финансовых сборах и скидках, включая полученные и потерянные скидки. Статистика рассчитывается для покупок до введенной даты, с трехмесячным интервалом с введенной даты и для периода, включающего все покупки, сделанные после третьего одномесячного интервала.|
|**Поставщики - первая десятка**|311|Показывает информацию по покупкам у поставщиков за выбранный период. Можно выбрать номера поставщиков, которые должны быть включены в отчет.<br>Поставщики сортированы по сумме, и можно выбрать, будут ли они сортированы по сумме покупки или балансу. Этот отчет предоставляет быстрый обзор поставщиков, у которых производится больше всего покупок, или по которым долг вашей организации больше.|
|**Каталог товаров поставщика** или **Каталог товаров/поставщиков**|320 или 720|Отображает список поставщиков для выбранных товаров или товаров для выбранных поставщиков. Для каждого сочетания товара и поставщика, отображается прямая стоимость единицы, проводится «Расчет периода ожидания», и приводится номер поставщика товара.<br>В США, Канаде и Мексике этот отчет недоступен. Вместо этого используйте отчет **Каталог товаров/поставщиков** (10164).|
|**Покупки поставщиков/товаров**|313|Показывает список товарных операций по каждому поставщику за выбранный период. Отчет содержит информацию по количеству, сумме и возможным скидкам в учтенных счетах. Он может использоваться, например, для анализа покупок товаров в организации и для того, чтобы показать есть ли связь между скидками и покупками товаров.|
|**Запасы - себестоимость и цена**|716|Отображает информацию по ценам для выбранных товаров или единиц хранения: прямая себестоимость единицы, последняя прямая себестоимость, цена единицы, процент прибыли и прибыль.|
|**Запасы — планируемое наличие**|707|Если вы хотите получить обзор конкретных товаров или складских единиц и их доступность. В этом отчете показаны суммарные значения, такие как валовая потребность, плановые и запланированные поступления, запасы и т. д. |
|**Товары - покупки по поставщ.**|714|Отображает список поставщиков, у которых организация закупила товары за выбранный период времени. Здесь показывается количество, по которому выставлен счет, сумма и скидка. Отчет можно использовать при анализе товарных покупок организации.|
|**Товары - заказы на покупку**|709|Отображает список товаров по заказу от поставщиков. В нем также отображены ожидаемая дата приемки, количество и сумма по невыполненным заказам. Например, используйте отчет, чтобы выяснить, когда следует получать товары, и следует ли послать напоминание о невыполненном заказе.|
|**Покупка - наличие резерва**|409|Показывает наличие товаров для отгрузки по документам покупки, например по заказам на возврат. Следует указать, будет ли в отчете указываться статус каждого документа или каждой строки покупки. <br>Также можно, чтобы во время печати отчета система обновила количество, доступное для отгрузки в поле **Кол-во для получения** в строках покупки. В кредит-нотах покупки или в отрицательных строках заказа покупки поле **Кол-во для получения** содержит количество товара для отгрузки. Затем можно использовать данный отчет для определения того, какой из документов предназначен для отгрузки. **Примечание**: этот отчет недоступен для расширенной функциональности хранилища.|
<!--|**Поставщик - сводка задолженности с распределением по срокам (подробно)**|11006| Касается DACH: отчет, который может быть использован руководителем отдела закупок и бухгалтерией. Здесь у вас будет обзор неоплаченных счетов-фактур поставщика, включая сроки, валюты и суммы. Основа — открытые операции книги поставщика.| -->




## <a name="tasks"></a>Задачи

В следующих статьях описываются некоторые ключевые задачи анализа состояния вашего бизнеса:

* [Создание аналитических отчетов](bi-how-create-analysis-views-reports.md)  
* [Просмотр наличия товара](inventory-how-availability-overview.md)  


## <a name="see-also"></a>См. также

[Настройка покупки](purchasing-setup-purchasing.md)  
[Покупки](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]