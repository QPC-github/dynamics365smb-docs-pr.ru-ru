---
title: Отчеты и аналитика по запасам и складу
description: Посмотрите, какие отчеты и аналитика по запасам и складу доступны в стандартной версии Business Central, чтобы вы могли отслеживать свой бизнес.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216390"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Отчеты и аналитика запасов и склада в Business Central

Отчетность по запасам и складу в [!INCLUDE [prod_short](includes/prod_short.md)] позволяет профессионалам по запасам и бизнесу получать информацию и статистические данные о текущей и прошлой деятельности по запасам и складу.  

## <a name="reports"></a>Отчеты

В следующей таблице описаны некоторые ключевые отчеты отчетности по запасам и складу.

|Отчет |ИД объекта|Описание  |
|---------|---------|---------|
|**Запасы — планируемое наличие**|707|Если вы хотите получить обзор конкретных товаров или складских единиц и их доступность. В этом отчете показаны суммарные значения, такие как валовая потребность, плановые и запланированные поступления, запасы и т. д. |
|**Оценка стоимости товаров**|1001|Отображает переоценку склада по выбранным товарам на складе. В отчете также отображается информация по стоимости повышений и понижений на складе за время.|
|**Истечение срока годности товаров - кол-во**|5809|Показывает обзор по количеству выбранных товаров в запасе, срок истечения действия которого попадает в определенный период. В списке отображается число единиц выбранного товара, срок которого истекает в данный период времени. Для каждого из товаров, указанного при настройке отчета, в распечатанном документе отображается число единиц, срок действия которых истекает в каждый из трех периодов равной длины, а также общее количество запасов выбранного товара.<br>Используя фильтры, можно указать, что должно быть включено в отчет. Если фильтры не заданы, в отчет будут включены все записи. Количества в отчете отражают только количества товаров, для которой определены сроки годности.|
|**Товар - возрастная структура - количество** или **Возрастная структура товара - значение**|5807 или 5808|Показывает структуру срока службы выбранных на складе товаров. В списке указывается число единиц или значение выбранного товара, которые пришли на склад, или ушли со склада, и в какой момент времени это произошло. Повышение и понижение количества товаров на складе происходит в результате покупки, продажи, а также прихода и расхода.|
|**Запасы - себестоимость и цена**|716|Отображает информацию по ценам для выбранных товаров или единиц хранения: прямая себестоимость единицы, последняя прямая себестоимость, цена единицы, процент прибыли и прибыль. |
|**Склад. список ячеек**|7319|Показывает обзор складских ячеек, их настройку и количество товаров в ячейках. Этот отчет можно использовать для всех локаций, для которых обязательным полем является «Ячейка». |
|**Статус складской отгрузки**|7313|Отображает общие сведения о документах с открытым источником по товарам, отгруженным или подлежащим отгрузке с того или иного склада. Этот отчет можно использовать для всех мест, где включено **Необходимые поставки**. **Статус складской отгрузки** показывает местоположения, коды ячеек, статус документа, количества.|
|**Сборочный лист запасов**|813|Отображает список заказов на продажу, в которые входит товар. Для каждой единицы товара отображается следующая информация: строка заказа на продажу с именем клиента, код варианта, код склада, код ячейки, дата отгрузки, отгружаемое количество, единица измерения. По отгружаемому количеству подсчитывается общая сумма для каждой единицы товара. Отчет можно использовать, когда товары собираются со склада.<br>ПРИМЕЧАНИЕ: эта функция недоступна для расширенной функциональности хранилища.|
|**Склад. ячейка коррекции**|7320|Этот специальный отчет предназначен только для расширенного склада и показывает оставшиеся количества, которые все еще хранятся в самой корректировочной ячейке. Обычно эта конкретная ячейка должна быть пустой. Единственная причина, по которой эта ячейка будет заполнена, — это результат физического процесса подсчета или если количество товаров было удалено или добавлено на склад.|


## <a name="tasks"></a>Задачи

В следующих статьях описываются некоторые ключевые задачи анализа состояния вашего бизнеса:

* [Создание аналитических отчетов](bi-how-create-analysis-views-reports.md)  
* [Просмотр наличия товара](inventory-how-availability-overview.md)


## <a name="see-also"></a>См. также

[Настройка запасов](inventory-setup-inventory.md)  
[Запасы](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)  
[Управление складом](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]