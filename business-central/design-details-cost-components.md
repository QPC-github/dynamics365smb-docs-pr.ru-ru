---
title: Сведения о проектировании — компоненты себестоимости | Документация Майкрософт
description: 'Компоненты себестоимости представляют собой другие типы затрат, которые составляют стоимость прихода или расхода склада.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-cost-components" />Сведения о проектировании: компоненты себестоимости
Компоненты себестоимости представляют собой другие типы затрат, которые составляют стоимость прихода или расхода склада.  

 В следующей таблице показаны разные компоненты стоимости и подчиненные компоненты стоимости, из которых они состоят.  

|Компонент себестоимости|Подчиненный компонент себестоимости|Описание|  
|--------------------|--------------------------------|---------------------------------------|  
|Прямая себестоимость|Себестоимость единицы (прямая цена покупки)|Стоимость, которую можно отследить до объекта затрат.|  
|Прямая себестоимость|Себестоимость фрахта (товарные издержки)|Стоимость, которую можно отследить до объекта затрат.|  
|Прямая себестоимость|Себестоимость страховки (товарные издержки)|Стоимость, которую можно отследить до объекта затрат.|  
|Косвенные затраты||Стоимость, которую невозможно отследить до объекта затрат.|  
|Отклонение|Покупка - отклонение|Разница между фактической и стандартной себестоимостью, которая учитывается только для товаров, использующих метод учета себестоимости **По стандартной**.|  
|Отклонение|Отклонение по материалам|Разница между фактической и стандартной себестоимостью, которая учитывается только для товаров, использующих метод учета себестоимости **По стандартной**.|  
|Отклонение|Отклонение по произв. мощн.|Разница между фактической и стандартной себестоимостью, которая учитывается только для товаров, использующих метод учета себестоимости **По стандартной**.|  
|Отклонение|Отклонение по субподряду|Разница между фактической и стандартной себестоимостью, которая учитывается только для товаров, использующих метод учета себестоимости **По стандартной**.|  
|Отклонение|Накл. рас. по пр. мощ. - откл.|Разница между фактической и стандартной себестоимостью, которая учитывается только для товаров, использующих метод учета себестоимости **По стандартной**.|  
|Отклонение|Производство - накладные расходы - отклонение|Разница между фактической и стандартной себестоимостью, которая учитывается только для товаров, использующих метод учета себестоимости **По стандартной**.|  
|Переоценка||Снижение или повышение текущей стоимости товаров на складе.|  
|Округление||Рассчитываются остатки, возникшие в результате переоценки расходов склада.|  

> [!NOTE]  
>  Значения себестоимости перевозки и страхования являются товарными издержками, которые можно добавить в себестоимость товаров в любое время. При выполнении пакетного задания **Коррекция себест. запасов** сопутствующий складской расход обновляется соответственно.  

## <a name="see-also" />См. также
 [Сведения о проектировании: себестоимость запасов](design-details-inventory-costing.md)   
 [Сведения о проектировании: отклонение](design-details-variance.md) [Управление себестоимостью товаров](finance-manage-inventory-costs.md)  
 [Финансы](finance.md)  
 [Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
