---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2520fcfb3b4faa49e89feae0f11a719bbfdb810a
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/24/2022
ms.locfileid: "8349007"
---
В следующей таблице описаны некоторые ключевые отчеты отчетности по покупкам.

| Отчет | Описание | Код | 
|---------|---------|---------|
|[Клиент – сводка заказа](https://businesscentral.dynamics.com?report=107)| Содержит подробную информацию по заказу (еще не отгруженное количество) для каждого клиента за три периода по 30 дней каждый, начиная с выбранной даты. Присутствуют также столбцы с заказами, подлежащими отгрузке до и после этих трех периодов, а также столбец с общей подробной информацией по заказам для каждого клиента. Используйте отчет для анализа ожидаемого объема продаж. |107|
|[Клиент - первая десятка](https://businesscentral.dynamics.com?report=111)| Показывает информацию о продажах товаров клиентам и их балансах за определенный период. Можно отобрать клиентов, включаемых в отчет. Будут включены только клиенты, имеющие либо покупки за данный период, либо баланс на конец периода.<br>Клиенты сортируются в порядке уменьшения сумм, и можно выбрать порядок сортировки в зависимости от сумм продаж или баланса. Отчет предоставляет краткий обзор клиентов, которые осуществляют наибольший объем покупок, либо имеют наибольшую задолженность.|111|
|[Клиент/продажа товаров](https://businesscentral.dynamics.com?report=113)|Показывает список продаж товаров по каждому клиенту за выбранный период времени. В отчете содержится количество, сумма продажи, прибыль и возможные скидки. Отчет может использоваться для анализа групп клиентов организации.|113|
|[Запасы — продажи клиентам](https://businesscentral.dynamics.com?report=713)|Обзор с точки зрения склада. Это другая точка зрения по сравнению с отчетом **Клиент/продажа товаров**, и в нем сначала отображается товар, а затем покупатель, купивший этот товар.|713|
|[Клиент - список продаж](https://businesscentral.dynamics.com?report=119)|Отображает продажи клиенту за период. Его можно использовать для отчета таможенным и налоговым органам. Можно включить только клиентов с общими продажами, превышающими некоторый минимальный размер. Можно также определить, следует ли включать в отчет подробный адрес каждого клиента.<br>Отчет основывается на продажах (МВ), зафиксированных из операций книги клиентов. В нижней части отчета общие учтенные продажи отображаются в МВ. Итог вычисляется по клиентам, которые включены в отчет, то есть клиентам, оставшимся после фильтрации на экспресс-вкладке «Клиент», сумма общих продаж которых превышает определенное значение в поле **Суммы (МВ) больше чем** на экспресс-вкладке **Параметры**.|119|
|[Клиент — баланс на дату](https://businesscentral.dynamics.com?report=121)|Показывает подробный баланс для выбранных клиентов. Используйте отчет при закрытии учетного периода или финансового года, например.|121|
|[Клиент - пробный баланс](https://businesscentral.dynamics.com?report=129)|Показывает подробный баланс для выбранных клиентов. Отчет может быть использован для проверки того, что баланс клиентской учетной группы равен балансу на соответствующем счете ГК на конкретную дату. Используйте отчет при закрытии учетного периода или финансового года, например. Если вам нужна более подробная версия этого типа отчета, воспользуйтесь отчетом **Пробный баланс сведений о клиенте** (104).| 129 |
|[Продажи - статистика](https://businesscentral.dynamics.com?report=112)|[!INCLUDE [reports-sales-statistics](reports-sales-statistics.md)] | 112|
|[Наличие резервирования продажи](https://businesscentral.dynamics.com?report=209)|Показывает наличие товаров для отгрузки по документам продажи. Здесь определяется, должен ли отчет отражать статус каждого документа или каждой строки документа продажи. Также можно, чтобы во время печати отчета система обновила количество, доступное для отгрузки в поле **Кол-во для отгрузки** в строках продажи. Затем можно будет использовать отчет для определения документов, подлежащих учету.<br>Также есть возможность, с помощью которой вы можете установить количество товаров для отправки. **Примечание**: этот отчет недоступен для расширенной функциональности склада.| 209 |
|[Статус складской отгрузки](https://businesscentral.dynamics.com?report=7313)|Этот отчет можно использовать для всех мест, где выбрано поле **Требуется отгрузка**. В отчете **Статус складской отгрузки** отображаются все неучтенные складские отгрузочные документы, включая местоположения, коды ячеек, статус документа, количества и т. д. Этот отчет идеально подходит для обзора.| 7313 |
|[Сборочный лист запасов](https://businesscentral.dynamics.com?report=813)|Отображает список заказов на продажу, в которые входит товар. Для каждой единицы товара отображается следующая информация: строка заказа на продажу с именем клиента, код варианта, код склада, код ячейки, дата отгрузки, отгружаемое количество, единица измерения. По отгружаемому количеству подсчитывается общая сумма для каждой единицы товара. Отчет можно использовать, когда товары собираются со склада.<br>**Примечание**: этот отчет недоступен для расширенной функциональности склада.|813|
|[Запасы - неполученные заказы](https://businesscentral.dynamics.com?report=718)|Показывает список со строками заказа, где была просрочена дата отгрузки. Следующая информация отображается по отдельным заказам для каждого товара: номер, имя клиента, номер телефона клиента, дата отгрузки, количество заказа и количество по непоставленному заказу. В отчете также отображается информация, существуют ли другие товары для данного клиента по непоставленному заказу.|718|
|[Требование-накладная - подробности](https://businesscentral.dynamics.com?report=708)|Отображает список заказов, которые не были еще отгружены, а так же товаров в заказах. Здесь отображены номер заказа, имя клиента, дата отгрузки, количество заказа, количество в ожидании, недопоставленное количество и цена единицы, также и процент возможных скидок и сумма. Для каждого товара суммируются общие значения количества по невыполненному заказу, балансовое количество и сумма. Используйте отчет для выяснения не существует ли в данный момент проблем по отгрузке или других ожидаемых проблем.|708|