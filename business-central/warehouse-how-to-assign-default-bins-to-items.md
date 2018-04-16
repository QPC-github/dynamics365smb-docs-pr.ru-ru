---
title: "Как присвоить товарам стандартные ячейки | Документы Майкрософт"
description: "Если на складе используются ячейки, присвоение товарам стандартных ячеек может значительно облегчить процесс отгрузки, приемки и перемещения товаров. Когда товару присваивается стандартная ячейка, она будет предлагаться в начале каждой транзакции для этого товара."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2075010c892893d28c7ae3fe627709669bc80a38
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="assign-default-bins-to-items"></a>Присвоение товарам стандартных ячеек
Если на складе используются ячейки, присвоение товарам стандартных ячеек может значительно облегчить процесс отгрузки, приемки и перемещения товаров. Когда товару присваивается стандартная ячейка, она будет предлагаться в начале каждой транзакции для этого товара. Стандартные ячейки задаются в окне **Содержимое ячейки**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Присвоение товару ячейки по умолчанию
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал создания содержимого ячеек**, затем выберите связанную ссылку.  
2.  Введите код ячейки и сведения о товаре для каждой ячейки, которую предполагается задать в качестве стандартной для товара. Убедитесь, что выбрано поле **По умолчанию**.  
3.  Выберите действие **Создать содержимое ячеек**. Теперь товару присвоены стандартные ячейки.  

> [!NOTE]  
>  При размещении товара, которому не присвоена стандартная ячейка, ему будет приписана в качестве ячейки по умолчанию та ячейка, в которой этот товар размещен.  

## <a name="to-change-the-default-bin-for-an-item"></a>Изменение стандартной ячейки для товара  
Может возникать необходимость изменить стандартную ячейку для товара или присвоить стандартную ячейку новому товару.    
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Содержимое ячейки**, а затем выберите связанную ссылку.  
2.  В поле **Фильтр по складу** выберите нужный код склада.  
3.  Найдите запись о текущей стандартной ячейке данного товара и снимите флажок **Станд. ячейка**.  
4.  Найдите строку "Содержимое ячейки" для той ячейки, которая должна стать новой стандартной ячейкой. Установите флажок **Станд. ячейка**.  

> [!NOTE]  
>  При первом размещении товара, у которого еще нет стандартной ячейки, ему в качестве стандартной будет приписана системой та ячейка, куда этот товар размещен.  

## <a name="see-also"></a>См. также  
[Управление складом](warehouse-manage-warehouse.md)  
[Наличие](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)     
[Управление сборкой](assembly-assemble-items.md)    
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
