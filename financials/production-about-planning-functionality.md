---
title: "О функции планирования | Microsoft Docs"
description: "Система планирования учитывает все данные спроса и предложения, сравнивает результаты и генерирует предложения для соответствия между предложением и спросом."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a00f88aaf70464c8911d59b829b08dda900dc474
ms.contentlocale: ru-ru
ms.lasthandoff: 11/10/2017

---
# <a name="about-planning-functionality"></a>О функциональности планирования
Система планирования учитывает все данные спроса и предложения, сравнивает результаты и генерирует предложения для соответствия между предложением и спросом.  

Дополнительные сведения см. в разделе [Сведения о проектировании: планирование поставок](design-details-supply-planning.md).  

> [!NOTE]  
> Для всех полей, которые указаны в этом разделе, ознакомьтесь с всплывающей подсказкой, чтобы понять их функции. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Спрос и предложение  
Планирование включает два элемента: спрос и предложение. Необходимо поддерживать их баланс, чтобы обеспечить своевременное и эффективное удовлетворение спроса.  

- Спрос - это общий термин, используемый для значительных потребностей, таких как заказ на продажу, сервисный заказ, потребность в компоненте со стороны производственного или сборочного заказа, исходящее перемещение, общий заказ или прогноз. Программа использует также некоторые другие технические типы спроса, - такие как отрицательное производство или заказ на покупку, отрицательные остатки и возврат покупки.  
- Предложение — это общий термин, используемый для любых пополнений, например склад, заказ на покупку, сборочный заказ, производственный заказ или входящее перемещение. Соответственно, могут быть отрицательные заказы на продажу или сервисные заказы, отрицательная потребность в компонентах или возврат проданного товара — все они в некотором смысле также представляют собой предложение.  

Еще одна цель системы планирования - не допустить увеличения объема складского хранения сверх необходимого предела. В случае уменьшения спроса система планирования предложит отложить, уменьшить количество или отменить существующие заказы на пополнение.  

## <a name="planning-calculation"></a>Расчет плана  
Работа системы планирования зависит от ожидаемого и фактического клиентского спроса, а также от параметров повторного заказа товаров для склада. При расчета плана программа предлагает специальные действия («Указания») для пополнения запасов от поставщиков, перемещений между складами или производства. Если заказы на пополнение уже существуют, может быть предложено увеличение или ускорение выполнения заказов для удовлетворения изменений спроса.  

В основе процедуры планирования лежит расчет брутто-нетто. Чистые потребности определяют запуск спланированных заказов, которые планируются на основе данных маршрута (производимые товары) или времени упреждения в карточке товара (приобретаемые товары). Количества в запускаемых спланированных заказах основаны на расчете плана и определяются параметрами, заданными в карточках отдельных товаров.  

## <a name="planning-with-manual-transfer-orders"></a>Планирование с использованием заказов на перемещение, созданных вручную
Как можно видеть в поле **Метод пополнения** карточки единицы хранения, систему планирования можно настроить так, чтобы она создавала заказы на перемещение, позволяющие сбалансировать спрос и предложение между складами.  

Кроме подобных автоматических заказов на перемещение, иногда может понадобиться выполнить общее перемещение определенных количеств товаров на другой склад независимо от существующего спроса. Для этого можно вручную создать заказ на перемещение нужного количества. Чтобы система планирования наверняка не попыталась управлять этим созданным вручную заказом на перемещение, необходимо установить в поле **Гибкость планирования** строки (строк) перемещения значение "Нет".  

Если нужно, чтобы система планирования откорректировала количества и даты заказа на перемещения в соответствии с существующим спросом, необходимо установить в поле **Гибкость планирования** значение по умолчанию "Неограниченно".

## <a name="planning-parameters"></a>Параметры планирования  
Параметры планирования определяют, когда, в каком объеме и как пополнять запасы в зависимости от различных настроек в карточке товара (или в единице хранения - SKU), а также в настройках производства.  

В карточке товара или единицы хранения имеются следующие параметры планирования.  

-   Буферный период  
-   Буферное количество  
-   Политика дозаказа  
-   Точка дозаказа
-   Максимальный запас  
-   Допустимый избыток  
-   Горизонт планирования  
-   Период накопления лота  
-   Период перепланирования  
-   Кол-во для дозаказа  
-   Cтраховое время подготовки  
-   Кол-во страхового запаса  
-   Политика сборки  
-   Политика производства  

В карточке товара или единицы хранения имеются следующие модификаторы заказа.  

-   Минимальное кол-во заказа  
-   Максимальное кол-во заказа  
-   Заказать несколько  

Поля настройки глобального планирования в окне **Производство - настройка** включают:  

-   Динамический код нижнего уровня  
-   Текущий прогноз производства  
-   Исп. прогноз по складам  
-   Страховой запас времени подготовки по умолчанию  
-   Общий допустимый избыток  
-   Совместный расчет MPS/MRP   
-   Компоненты по складам  
-   Буферный период по умолчанию  
-   Буферное количество по умолчанию  

Для получения дополнительной информации см. раздел [Сведения о проектировании: параметры планирования](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Другие важные поля планирования
### <a name="planning-flexibility"></a>Гибкость планирования
В большей часть заказов на поставку, таких как производственные заказы, можно выбрать значение **Неограниченно** или **Нет** в поле **Гибкость планирования** в строках.

Это указывает, учитывается ли поставка, представленная строкой в производственном заказе, системой планирования при расчете указаний.
Если в данном поле указан параметр **Неограниченно**, система планирования учитывает строку при расчете указаний. Если в поле указано **Нет**, строка является фиксированной и не подлежит изменению, и система планирования не учитывает ее при расчете указаний.

### <a name="warning"></a>Предупреждение
Информационное поле **Предупреждение** в окне **Журнал планирования** информирует о любых строках планирования, созданных для нетипичной ситуации, с текстом, который пользователь может выбрать для ознакомления с дополнительной информацией. Существуют следующие типы предупреждений:

- Экстренный,
- Исключение,
- Внимание!
- Экстренный,

Экстренное предупреждение отображается в двух случаях:

- отрицательный остаток запасов на планируемую дату начала;
- поставка датирована прошедшим числом или существуют события, в результате которых возникли требования.

В случае отрицательного остатка по запасам товара на планируемую дату начала, система планирования предложит экстренный заказ на поставку с количеством, равным отрицательному остатку, и поставкой на планируемую дату начала. В тексте предупреждения указывается дата начала и количество для экстренного заказа.

Любые строки документа с датами завершения до планируемой даты начала объединяются в один экстренный заказ на поставку товара с доставкой на планируемую дату начала.

### <a name="exception"></a>Исключение,
Предупреждение об исключении отображается в случае, когда прогнозируемые доступные запасы оказываются ниже количества страхового запаса.

Система планирования предложит заказ на поставку для выполнения требования к сроку выполнения. В тексте предупреждения указывается количество страхового запаса товара и дата на которую произошло данное нарушение.

Нарушение требования к уровню страхового запаса считается причиной исключения, так как в случае правильной настройки точки повтора заказа такая ситуация возникать не должна.

> [!NOTE]
> Поставка в строках планирования с предупреждениями об исключениях обычно не изменяется в соответствии с параметрами планирования. Вместо этого, система планирования только предлагает поставку для покрытия конкретного требуемого количества. Однако, можно настроить запуск планирования для строк планирования, которые следует учитывать с некоторыми предупреждениями. Дополнительные сведения см. в пункте "Учет параметров планирования для предупреждений об исключениях" в разделе "Расчет плана - журнал планов.

### <a name="attention"></a>Внимание!
Предупреждение о необходимости обратить на что-либо внимание отображается в двух случаях:

- планируемая дата начала наступает раньше рабочей даты;
- в строке планирования предлагается изменить выпущенный заказ на покупку или производственный заказ.

> [!NOTE]
> В строках планирования с предупреждениями поле **Принять указания** не выбрано, так как ожидается, что планировщик дополнительно изучит эти строки перед составлением плана.

## <a name="see-also"></a>См. также  
[Сведения о проектировании: планирование поставок](design-details-supply-planning.md)  
[Планирование](production-planning.md)   
[Настройка производства](production-configure-production-processes.md)  
[Производство](production-manage-manufacturing.md)    
[Наличие](inventory-manage-inventory.md)  
[Покупки](purchasing-manage-purchasing.md)  
[Рекомендации по настройке: планирование поставок](setup-best-practices-supply-planning.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
