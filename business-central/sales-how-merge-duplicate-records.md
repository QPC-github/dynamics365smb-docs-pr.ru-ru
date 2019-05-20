---
title: Объединение повторяющихся записей клиента или поставщика | Документы Майкрософт
description: Описывается процедура создания карточки клиента для регистрации информации о каждом новом клиенте, которому вы что-либо продаете.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c23e34cfe0a1684a4bd5b95b60f56f0e411608ab
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251810"
---
# <a name="merge-duplicate-records"></a>Объединение повторяющихся записей
Когда с течением времени различные пользователи создают новые карточки клиентов, поставщиков или контактов, или когда новые записи создаются автоматически во время миграции, клиент, поставщик или контакт могут быть представлены в системе в нескольких записях. В этом случае можно воспользоваться страницей **Объединить дубликат** из карточки записи, которую требуется сохранить. Страница обеспечивает обзор значений дублированных полей и предоставляет функции для выбора, какие значения сохранить или удалить при объединении записей в одну.

> [!NOTE]
> Только пользователи с набором разрешений ОБЪЕДИНЕНИЕ ДУБЛИКАТОВ могут использовать эту функцию.

> [!TIP]
> На странице **Объединить дубликат** отображаются все поля, значения которых отличаются в двух сравниваемых записях. Поэтому дубликат указывается страницей с очень небольшим количеством полей. Поэтому если на странице отображается много полей, тогда возможно, что подозрительная запись не является дубликатом.

Следующая процедура основана на карточке клиента. Действия для карточек поставщика и контакта аналогичны.

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Клиенты**, затем выберите связанную ссылку.
2. Выберите клиента, для которого вы знаете или предполагаете, что существует повторяющаяся запись, затем выберите действие **Правка**.
3. На странице **Карточка клиента** выберите действие **Объединить с**.
4. На странице **Объединить дубликат** в поле **Объединить с** выберите клиента, который, по вашему мнению, дублирует открытого вами клиента, указанного в поле **Текущий**.

    На экспресс-вкладке **Поля** перечисляются поля, значения которых отличаются для двух клиентов. Это означает, что если выбранный клиент действительно является дубликатом, должно быть перечислено очень мало полей, связанных с ошибками правописания и другими ошибками ввода данных.

    На экспресс-вкладке **Связанные таблицы** перечислены таблицы, в которых имеются поля, связанные с обоими клиентами. В полях **Число текущих** и **Число дубликатов** отображается количество полей в связанных таблицах, где значение **Номер** в текущем и повторяющемся клиенте используется. На странице **Объединить дубликат** этот раздел только информационный, однако если существуют конфликты объединения, они будут разрешаться на странице **Конфликты объединения дубликатов**. См. шаги с 8 по 12.   

5. Для каждого поля, в котором требуется использовать значение, отличное от текущего, установите флажок **Переопределить**. Значение в поле **Альтернативное значение** будет затем перемещено в текущую запись при проведении процесса.
6. По завершении выбора того, какие значения следует сохранить или переопределить, выберите действие **Объединить**.

    Система проверяет, не вызовет ли объединение значений для повторяющегося клиента с текущим клиентом каких-либо конфликтов. Конфликты существует, если значение по крайней мере в одном поле основного ключа одинаково для обоих клиентов, тогда как значение в поле **Номер** различно для двух клиентов.

7. Если конфликты не обнаружены, выберите кнопку **Да** в поле сообщения подтверждения.

    Дублированный клиент будет переименован, чтобы все использования его значения **Номер** во всех полях с отношениями с таблицей клиентов будут заменены значением **Номер** текущего клиента.
8. Если существуют конфликты, выберите действие **Разрешите конфликты (хх) перед объединением**. на экспресс-вкладке **Конфликты**, которая появляется при наличии конфликтов.
9. На странице **Конфликты объединения дубликатов** выберите строку для связанной таблицы с конфликтом, затем выберите действие **Просмотреть сведения**.

    На странице **Объединить дубликат** теперь отображаются поля в выбранной таблице, которые вызывают конфликт объединения между двумя записями клиента. Обратите внимание в обоих суммированных значениях в полях **Текущее** и **Конфликтует с** и в строках, в которых по крайней мере одно поле первичного ключа совпадает для обоих клиентов и значение поля **Номер** различное для двух клиентов.   
10. Если вы не хотите сохранять повторяющуюся запись клиента, выберите действие **Удалить дубликат**, затем нажмите кнопку **Закрыть**.

    Одинаковые значения полей, отличные от значения в поле **Номер**, удаляются из дублирующей записи и вставляются в текущую запись.
11. Если нужно сохранить повторяющуюся запись клиента после объединения, выберите **Переименовать дубликат**.
12. В строках, но не для поля **Номер**, в которых значение поля одинаковое в обеих записях, измените значение в поле **Альтернативное значение**, затем нажмите кнопку **Закрыть**.

    Значение конфликтующего поля обновляется в повторяющейся записи таким образом, чтобы его можно было объединить с текущей записью. После объединения повторяющаяся записи продолжает существовать.
13. Повторите шаги с 8 по 12, пока все конфликты не будут разрешены. Экспресс-вкладка **Конфликты** исчезает.
14. На странице **Объединить дубликат** снова выберите действие **Объединить**. затем выберите кнопку **Да** в поле сообщения подтверждения.

> [!NOTE]
> Для контактов можно использовать функцию поиска двойных контактов, прежде чем использовать страницу **Объединить дубликат**. Дополнительные сведения см. в разделе [Поиск повторяющихся контактов](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## <a name="see-also"></a>См. также
[Продажи](sales-manage-sales.md)  
[Настройка контактов](marketing-setup-contacts.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)