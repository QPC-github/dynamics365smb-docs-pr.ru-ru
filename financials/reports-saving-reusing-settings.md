---
title: "Применение и изменение сохраненных параметров в отчетах | Документы Майкрософт"
description: "Описывается использование заранее определенных параметров и фильтров для настройки отчета и формирования правильных данных."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017


---
# <a name="saved-settings-on-reports"></a>Сохраненные настройки в отчетах
В зависимости от запущенного отчета, может отображаться страница, которая позволяет задать некоторые параметры и фильтры для изменения данных, которые будут включены в отчет. Эта страница называется страницей запроса отчета. Отчет может содержать одну или несколько *сохраненных настроек*, которые можно применять к отчету со страницы запроса отчета. *Сохраненные настройки* в целом являются заранее заданными параметрами и фильтрами. Сохраненные настройки обеспечивают быстрый и удобный способ последовательного создания отчетов, содержащих правильные данные.

Доступные вам сохраненные настройки отчета можно посмотреть в разделе **Сохраненные настройки** на странице запроса отчета.  

## <a name="to-apply-saved-settings-to-a-report"></a>Применение сохраненных настроек к отчету
1. Откройте отчет.

   Открывается страница запроса отчета.    
2. В разделе **Сохраненные настройки** на этой странице задайте в поле **Название** сохраненных настроек, которые требуется использовать.

   Раздел **Сохраненные настройки** применяется, только если до этого был выполнен отчет или существуют сохраненные операции настроек. Всегда доступны сохраненные настройки под названием **Последние использованные параметры и фильтры**. Это настройки представляют собой значения параметров и фильтра, которые были использованы при последнем запуске отчета.

## <a name="administer-saved-report-settings-for-users"></a>Администрирование сохраненных настроек отчета для пользователей
При наличии соответствующих прав доступа можно просматривать, создавать и изменять сохраненные настройки для всех отчетов для всех пользователей в организации. Можно назначить сохраненные настройки отчета индивидуальным пользователям или всем пользователям в организации.

Для управления сохраненными настройками используется страница 1506 **Настройки отчетов**. Чтобы открыть эту страницу, выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Параметры отчета**, а затем выберите связанную ссылку.

Со страницы **Настройки отчетов** можно создавать новые настройки с нуля или можно сделать копию и изменить существующие настройки. Чтобы изменить параметры и фильтры для настройки, выберите действие **Изменить**.

**Примечания.**

* Функция сохраненных настроек отчетов действует только в том случае, если для свойства SaveValues страницы запроса задано значение "Да". Свойство SaveValues задается в среде разработки.
* Если вы создаете товар сохраненных настроек для всех пользователей и он содержит то же имя, что и существующие сохраненные настройки для определенного пользователя, то этот пользователь не сможет использовать сохраненные настройки, которые назначены всем.  В поле "Сохраненные настройки" на странице запроса отчета пользователь сможет просмотреть два параметра сохраненных настроек с одинаковым именем. Однако независимо от выбранного параметра будут использоваться сохраненных настройки для определенного пользователя.

## <a name="see-also"></a>См. также
[Планирование выполнения отчета](ui-schedule-report.md)  
