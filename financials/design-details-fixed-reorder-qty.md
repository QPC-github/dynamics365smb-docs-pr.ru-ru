---
title: "Сведения о проектировании — Фиксированное количество повторного заказа | Документы Майкрософт"
description: "Политика фиксированного количества повторного заказа связана с планированием запасов стандартных С-элементов (низкая стоимость запасов, низкий риск устаревания и(или) много элементов). Эта политика обычно используется в связи с точкой повторного заказа, отражая прогнозируемый спрос во время подготовки товара."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7726a1b5749aa4da14d06d3484ee83668531f84f
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-fixed-reorder-qty"></a>Сведения о проектировании: фиксированное количество дозаказа
Политика фиксированного количества повторного заказа связана с планированием запасов стандартных С-элементов (низкая стоимость запасов, низкий риск устаревания и(или) много элементов). Эта политика обычно используется в связи с точкой повторного заказа, отражая прогнозируемый спрос во время подготовки товара.  

## <a name="calculated-per-time-bucket"></a>Расчет на горизонт планирования  
 Если система планирования обнаруживает, что точка дозаказа достигнута или пройдена в данном горизонте планирования (цикл дозаказа) — количество больше или равно точке дозаказа в начале периода и ниже или равно точке дозаказа в конце периода — она предлагает создать новый заказ на поставку с определенным количеством дозаказа и запланировать его на первую дату после последней даты горизонта планирования.  

 Понятие точки повторного заказа в периоде времени уменьшает число предложений поставки. Это отражает ручной процесс периодического обхода склада с целью проверить фактическое содержимое различных ячеек.  

## <a name="creates-only-necessary-supply"></a>Создание только необходимой поставки  
 Перед тем как предложить новый заказ на поставку для соответствия точке дозаказа, система планирования проверяет, была ли уже заказана поставка для получения во время подготовки товара. Если существующий заказ на поставку разрешит проблему, увеличив или уменьшив прогнозируемые запасы по отношению к точке дозаказа в течение времени подготовки, система не предложит новый заказ на поставку.  

 Заказы на поставку, созданные специально для соответствия точке дозаказа, исключаются из обычной балансировки поставки и ни при каких обстоятельствах не изменятся в будущем. Следовательно, при отмене (непополнении) товара, использующего точку дозаказа, рекомендуется просмотреть незавершенные заказы на поставку вручную или изменить политику дозаказа на "Партия на партию", в соответствии с чем система уменьшит или отменит излишнюю поставку.  

## <a name="combines-with-order-modifiers"></a>Объединение с модификаторами заказа  
 Модификаторы заказов, минимальное кол-во заказа, максимальное кол-во заказа и задать несколько, не должны играть существенной роли при использовании политики фиксированного количества для повторного заказа. Однако система планирования примет в расчет эти модификаторы и уменьшит количество до указанного максимального количества заказа (и создаст две или более поставки для достижения общего количества заказа), увеличит заказ до указанного минимального количества заказа или округлит количество заказа для соответствия указанному множителю заказа.  

## <a name="combines-with-calendars"></a>Объединение с календарями  
 Перед тем как предложить новый заказ на поставку для соответствия точке дозаказа, система планирования проверяет, запланирован ли заказ на нерабочий день, согласно всем календарям, определенным в поле **Код базового календаря** в окнах **Информация об организации** и **Карточка склада**.  

 Если плановая дата является нерабочим днем, система планирования переместит заказ до ближайшей рабочей даты. Это может привести к тому, что заказ достигнет точки повтора заказа, но не удовлетворит определенному спросу. Если такого несбалансированного спроса система планирования создает дополнительную поставку.  

## <a name="should-not-be-used-with-forecast"></a>Не для использования с прогнозом  
 Поскольку ожидаемый спрос уже выражен на уровне точки дозаказа, не обязательно включать прогноз в планирование товара с использованием точки дозаказа. Если политика "Партия на партию" имеет отношение к созданию плана на основе прогноза, используйте ее.  

## <a name="must-not-be-used-with-reservations"></a>Не для использования с резервированиями  
 Если пользователь резервировал количество, например количество в запасах, для некоторого отдаленного спроса, основа планирования будет нарушена. Даже если прогнозируемый уровень запасов является приемлемым в отношении точки дозаказа, количества могут быть недоступны. Система может компенсировать это, создав исключительные заказы; однако рекомендуется задать в поле "Резервирование" значение "Никогда" для товаров, спланированных с использованием точки повторного заказа.  

## <a name="see-also"></a>См. также  
 [Сведения о проектировании: политики дозаказа](design-details-reordering-policies.md)   
 [Сведения о проектировании: максимальное количество](design-details-maximum-qty.md)   
 [Сведения о проектировании: параметры планирования](design-details-planning-parameters.md)   
 [Сведения о проектировании: обработка политик дозаказа](design-details-handling-reordering-policies.md)   
 [Сведения о проектировании: планирование поставок](design-details-supply-planning.md)
