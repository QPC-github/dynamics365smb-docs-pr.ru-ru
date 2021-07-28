---
title: Отчеты о покупках и аналитика
description: Посмотрите, какие отчеты о покупках и аналитика доступны в стандартной версии Business Central, чтобы вы могли отслеживать свой бизнес.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: a8ada1c8488e8c5dec581db98dccf02d89da21c3
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216388"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>Отчеты о покупках и аналитика в Business Central

Отчетность о покупках в [!INCLUDE [prod_short](includes/prod_short.md)] позволяет профессионалам по продажам и бизнесу получать информацию и статистические данные о текущей и прошлой деятельности по покупкам.  

## <a name="reports"></a>Отчеты

В следующей таблице описаны некоторые ключевые отчеты отчетности по покупкам.

|Отчет |ИД объекта|Описание  |
|---------|---------|---------|
|**Клиент - сводка заказа**|107| Содержит подробную информацию по заказу (еще не отгруженное количество) для каждого клиента за три периода по 30 дней каждый, начиная с выбранной даты. Присутствуют также столбцы с заказами, подлежащими отгрузке до и после этих трех периодов, а также столбец с общей подробной информацией по заказам для каждого клиента. Используйте отчет для анализа ожидаемого объема продаж. |
|**Клиент - первая десятка**|111| Показывает информацию о продажах товаров клиентам и их балансах за определенный период. Можно отобрать клиентов, включаемых в отчет. Будут включены только клиенты, имеющие либо покупки за данный период, либо баланс на конец периода.<br>Клиенты сортируются в порядке уменьшения сумм, и можно выбрать порядок сортировки в зависимости от сумм продаж или баланса. Отчет предоставляет краткий обзор клиентов, которые осуществляют наибольший объем покупок, либо имеют наибольшую задолженность.|
|**Клиент/продажа товаров**|113|Показывает список продаж товаров по каждому клиенту за выбранный период времени. В отчете содержится количество, сумма продажи, прибыль и возможные скидки. Отчет может использоваться для анализа групп клиентов организации.|
|**Запасы — продажи клиентам**|713|Обзор с точки зрения склада. Это другая точка зрения по сравнению с отчетом **Клиент/продажа товаров**, и в нем сначала отображается товар, а затем покупатель, купивший этот товар.|
|**Клиент - список продаж**|119|Отображает продажи клиенту за период. Его можно использовать для отчета таможенным и налоговым органам. Можно включить только клиентов с общими продажами, превышающими некоторый минимальный размер. Можно также определить, следует ли включать в отчет подробный адрес каждого клиента.<br>Отчет основывается на продажах (руб.), зафиксированных из операций книги клиентов. В нижней части отчета общие учтенные продажи отображаются в рублях. Итог вычисляется по клиентам, которые включены в отчет, то есть клиентам, оставшимся после фильтрации на экспресс-вкладке «Клиент», сумма общих продаж которых превышает определенное значение в поле **Суммы (руб.) больше чем** на экспресс-вкладке **Параметры**.|
|**Клиент — баланс на дату**|121|Показывает подробный баланс для выбранных клиентов. Используйте отчет при закрытии учетного периода или финансового года, например.|
|**Клиент - пробный баланс**|129|Показывает подробный баланс для выбранных клиентов. Отчет может быть использован для проверки того, что баланс клиентской учетной группы равен балансу на соответствующем счете ГК на конкретную дату. Используйте отчет при закрытии учетного периода или финансового года, например. Если вам нужна более подробная версия этого типа отчета, воспользуйтесь отчетом **Пробный баланс сведений о клиенте** (104).|
|**Статистика продаж**|112|Показывает суммы продаж, прибыли, скидки по счету и скидки по оплате в рублях, а также процент прибыли для каждого клиента. Для себестоимости и прибыли приводятся два значения: исходное и скорректированное. Исходными значениями себестоимости и прибыли являются те, которые были рассчитаны во время учета, а скорректированные значения себестоимости и прибыли отражают изменения исходной себестоимости товаров при продаже. Сумма коррекции себестоимости, отраженная в отчете, представляет собой разницу между исходной себестоимостью и скорректированной себестоимостью.<br>Данные разделены по трем периодам. Можно выбрать длину периода, начальной датой которого является выбранная. В отчете представлены столбцы с суммами, учтенными до и после трёх периодов. Используйте отчет, например, для анализа выручки от отдельного клиента и общих тенденций получения прибыли. |
|**Наличие резервирования продажи**|209|Показывает наличие товаров для отгрузки по документам продажи. Здесь определяется, должен ли отчет отражать статус каждого документа или каждой строки документа продажи. Также можно, чтобы во время печати отчета система обновила количество, доступное для отгрузки в поле **Кол-во для отгрузки** в строках продажи. Затем можно будет использовать отчет для определения документов, подлежащих учету.<br>Также есть возможность, с помощью которой вы можете установить количество товаров для отправки. **Примечание**: этот отчет недоступен для расширенной функциональности хранилища.|
|**Статус складской отгрузки**|7313|Этот отчет можно использовать для всех мест, где выбрано поле **Требуется отгрузка**. В отчете **Статус складской отгрузки** отображаются все неучтенные складские отгрузочные документы, включая местоположения, коды ячеек, статус документа, количества и т. д. Этот отчет идеально подходит для обзора.|
|**Сборочный лист запасов**|813|Отображает список заказов на продажу, в которые входит товар. Для каждой единицы товара отображается следующая информация: строка заказа на продажу с именем клиента, код варианта, код склада, код ячейки, дата отгрузки, отгружаемое количество, единица измерения. По отгружаемому количеству подсчитывается общая сумма для каждой единицы товара. Отчет можно использовать, когда товары собираются со склада.<br>**Примечание**: этот отчет недоступен для расширенной функциональности хранилища.|
|**Запасы - неполученные заказы**|718|Показывает список со строками заказа, где была просрочена дата отгрузки. Следующая информация отображается по отдельным заказам для каждого товара: номер, имя клиента, номер телефона клиента, дата отгрузки, количество заказа и количество по непоставленному заказу. В отчете также отображается информация, существуют ли другие товары для данного клиента по непоставленному заказу.|



## <a name="tasks"></a>Задачи

В следующих статьях описываются некоторые ключевые задачи анализа состояния вашего бизнеса:

* [Создание аналитических отчетов](bi-how-create-analysis-views-reports.md)  
* [Просмотр наличия товара](inventory-how-availability-overview.md)


## <a name="see-also"></a>См. также

[Настройка продаж](sales-setup-sales.md)  
[Продажи](sales-manage-sales.md)  
[Резервирование товаров](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]