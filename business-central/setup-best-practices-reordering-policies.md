---
title: Рекомендации по настройке. Политики повторного заказа | Документация Майкрософт
description: 'Поле Политика дозаказа в карточках товара содержит четыре разных метода планирования, которые определяют способ взаимодействия отдельных параметров планирования.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setup-best-practices-reordering-policies" />Рекомендации по настройке. Политики повторного заказа

Поле **Политика дозаказа** в карточках товара содержит четыре разных метода планирования, которые определяют способ взаимодействия отдельных параметров планирования.  

Одной из ведущих основ при выборе политики повторного заказа является классификация товаров в алфавитном порядке. При использовании ABC-классификации для контроля инвентаря и планирования поставок товары управляются в соответствии с 3 различными классами в зависимости от их значений и объема по отношению к общим запасам. Распределение стоимости по объему для этих трех классов показано в следующей таблице.

|Класс|Процент общего объема запасов|Процент общей стоимости запасов|
|-----|-----------------------------|----------------------------|
|А|10-20|50-70|
|Б|20|20|
|C|60-70|10-30|

ABC-классификация показывает, что время и средства можно сэкономить, используя более свободное управление товарами для низкого уровня "стоимость-объем" в отличие от высокого уровня "стоимость-объем". На следующей иллюстрации показано, как политика повтора заказа в [!INCLUDE[prod_short](includes/prod_short.md)] лучше всего подходит для товара A, B и C соответственно.

![Классификация по алфавиту.](media/abc_classification.png "abc_classification")

В следующей таблице приведены рекомендации по выбору одной из четырех политик.  

|Параметр настройки|Рекомендация|Комментарий|  
|------------------|-------------------|-------------|  
|**Заказ**|Используйте для товаров А.<br /><br /> Используйте для товаров, изготавливаемых на заказ.<br /><br /> При производстве используйте для наиболее важных товаров и для дорогостоящих компонентов и узлов.<br /><br /> Используйте для товаров, которые приобретались с прямой поставкой или по специальному заказу.<br /><br /> Не используйте, если вы не принимаете автоматическое резервирование.|Товары, например кожаные диваны в мебельном магазине, являются ценными предметами с низкой и нерегулярной скоростью заказа, при которой формирование запасов неприемлемо, или обязательные атрибуты различаются. Лучшая политика повтора заказа — это политика, которая осуществляет планирование по каждому варианту спроса.|  
|**Партия на партию**|Используйте для товаров B.<br /><br /> При производстве используйте для компонентов, которые могут использоваться нескольких спецификациях. Это гарантирует объединение заказов на покупку одного поставщика, чтобы можно было провести переговоры по снижению цен.<br /><br /> Используйте, если вы не знаете, какую политику дозаказа выбрать.|Товары класса Б, например стулья, имеют регулярную и довольно высокую скорость заказа, но также высокие затраты на обслуживание. Наилучшая политика повторного заказа товаров B заключается в объединении спроса в цикле повтора заказов.<br /><br /> Эту политику могут использовать 80 процентов товаров.<br /><br /> Может успешно использоваться без параметров планирования.|  
|**Фикс. кол-во повтора заказа**|Используйте для товаров C.<br /><br /> Объедините с параметрами точки повтора заказа.<br /><br /> При производстве используйте для наименее важных компонентов.<br /><br /> Не используйте, если товар часто резервируется.|Товары C, например чайные чашки, это товары низкой стоимости с высокой и регулярной скоростью заказа. Лучшая политика повтора заказа для товаров C — это политика, которая гарантирует постоянное наличие за счет постоянного нахождения выше точки повторного заказа.<br /><br /> Если пользователь резервирует количество для выполнения отдаленного требования, то будет нарушена основа планирования. Даже если прогнозируемый уровень запасов является приемлемым в отношении точки повторного заказа, количества могут быть недоступны из-за резервирования.|  
|**Максимальное кол-во**|Используйте для товаров C с высокими затратами на обслуживание или ограничениями по хранению.<br /><br /> Объедините с одним или несколькими модификаторами заказов ("Минимальное/максимальное кол-во заказа" или "Заказать несколько").|Товары C, например чайные чашки, это товары низкой стоимости с высокой и регулярной скоростью заказа. Лучшая политика повтора заказа для товаров C — это политика, которая гарантирует постоянное наличие за счет постоянного нахождения выше точки повторного заказа, но ниже точки максимального количества запасов.<br /><br /> Чтобы изменить предлагаемый заказ, может потребоваться сократить количество заказов до указанного максимального количества заказов, увеличить его до указанного минимального количества заказов либо округлить для соответствия указанному множителю заказов. **Примечание.** При использовании точки повторного заказа запасы остаются в пределах точки повторного заказа и максимального количества.|  

## <a name="see-related-microsoft-trainingtrainingpathsreplenish-items-dynamics-365-business-central" />См. соответствующее [обучение Microsoft](/training/paths/replenish-items-dynamics-365-business-central/)

## <a name="see-also" />См. также

 [Рекомендации по настройке. Планирование поставок](setup-best-practices-supply-planning.md)  
 [Сведения о проектировании: обработка политик дозаказа](design-details-handling-reordering-policies.md)  
 [Настройка сложных областей приложения с помощью рекомендаций](set-up-complex-application-areas-using-best-practices.md)  
 [Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
