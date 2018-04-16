---
title: "Как архивировать документы о продажах и покупке | Документы Майкрософт"
description: "Можно архивировать заказы продажи и покупки, предложения, заказы на возврат и общие заказы, и можно использовать архивный документ для восстановления документа, из которого он был архивирован."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Архивирование документов
Можно архивировать заказы продажи и покупки, предложения, заказы на возврат и общие заказы, и можно использовать архивный документ для восстановления документа, из которого он был архивирован.

## <a name="to-set-up-automatic-document-archiving"></a>Настройка автоматического архивирования документов  
Можно настроить автоматическое архивирование заказов продаж и покупки, предложений, общих заказов и заказов на возврат перед удалением документов.

Следующая процедура описывает, как настроить автоматическое архивирование документов продажи. Действия для документов на покупку аналогичны.
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Настройка модуля "Продажи"**, затем выберите связанную ссылку.
2. В окне **Настройка модуля "Продажи"** заполните поля следующим образом:

|Поле|Описанием|
|-----|-----------|
|**Архивирование предложений по продаже**|**Никогда**, чтобы никогда не архивировать предложения по продаже при их удалении. **Вопрос**, чтобы предлагать пользователю выбрать, требуется ли архивировать предложения по продаже перед их удалением. **Всегда**, чтобы автоматически архивировать предложения по продаже при их удалении.|
|**Архивирование общих заказов на продажу**|Выберите для автоматического архивирования общих заказов на продажу каждый раз при их удалении.|
|**Архивировать заказы и заказы на возврат**|Выберите для автоматического архивирования заказов на продажу каждый раз при их удалении.|

## <a name="to-archive-a-sales-order"></a>Архивирование заказа на продажу
Следующая процедура описывает, как архивировать заказ на продажу. Эти шаги аналогичны для всех заказов, общих заказов, заказов на возврат и предложений.

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на продажу**, а затем выберите связанную ссылку.  
2.  Откройте заказ на продажу, который требуется архивировать.  
3.  Выберите действие **Архивировать документ**.

Заказ на продажу архивирован. Его можно просмотреть в окне **Архивные заказы на продажу**. Отсюда его также можно использовать для восстановления заказа на продажу, из которого был создан архив.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Восстановление заказа на продажу из архива
Следующая процедура описывает, как восстановить заказ на продажу. Эти шаги аналогичны для всех заказов, общих заказов, заказов на возврат и предложений.

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Архивированные заказы на продажу**, затем выберите связанную ссылку.
2.  Выберите архивированный заказ на продажу, который требуется восстановить, затем выберите действие **Восстановить**.  

Заказ на продажу создается и добавляется в окно **Заказы на продажу**.

## <a name="to-delete-archived-sales-orders"></a>Удаление архивных заказов продажу
Следующая процедура описывает, как удалить архивные заказы на продажу. Шаги аналогичны для всех остальных архивных документов продажи и покупки.

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Удалить архивные версии заказов продажи**, затем выберите связанную ссылку.  
2.  В окне **Удалить архивные версии заказов продажи** выберите соответствующие фильтры.  
3.  Нажмите кнопку **ОК**.

## <a name="see-also"></a>См. также
[Отслеживание строк документа](across-how-to-track-document-lines.md)  
[Продажи](sales-manage-sales.md)  
[Общие бизнес-функции](ui-across-business-areas.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
