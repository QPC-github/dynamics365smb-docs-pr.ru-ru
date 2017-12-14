---
title: "Практическое руководство. Настройка и публикация веб-служб ключевых показателей эффективности, которые основаны на финансовых отчетах | Документы Майкрософт"
description: "В окне **Настройка веб-службы ключевых показателей эффективности финансового отчета** можно задать способ показа сведений KPI финансового графика и отдельные финансовые графики, на которых основаны KPI."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f91a9813b07b0868043a4a2a3ed0b3f838536
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Практическое руководство. Настройка и публикация веб-служб ключевых показателей эффективности, которые основаны на финансовых отчетах
В окне **Настройка веб-службы ключевых показателей эффективности финансового отчета** можно задать способ показа сведений KPI финансового графика и отдельные финансовые графики, на которых основаны KPI. При выборе кнопки **Публикация веб-службы** настроенные сведения ключевых показателей эффективности для финансового отчета добавляются в список опубликованных веб-служб в окне **Веб-службы**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Процедура настройки и публикации веб-службы ключевых показателей эффективности, которая основана на финансовых отчетах  

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Настройка веб-службы ключевых показателей эффективности финансового отчета**, а затем выберите связанную ссылку.  
2.  На экспресс-вкладке **Общее** заполните поля, как описано в следующей таблице.  

    |Поле|Описанием|  
    |---------------------------------|---------------------------------------|  
    |**Дата начала прогнозируемых значений**|Укажите, в какой момент времени следует показывать прогнозируемые значения на графике ключевых показателей эффективности для финансового отчета.<br /><br /> Прогнозируемые значения извлекаются из бюджета главной книги, выбранного в поле **Название бюджета ГК**. **Примечание.** Для получения ключевых показателей эффективности, которые отображают прогнозные значения после конкретной даты и фактические значения до даты, можно изменить поле **Разрешить учет с** в окне **Настройка ГК**. Дополнительные сведения см. в разделе Разрешить учет с.|  
    |**Название бюджета ГК**|Укажите название бюджета главной книги, в котором содержатся значения прогноза для веб-службы ключевого показателя эффективности финансового отчета.|  
    |**периодам**|Укажите период, на котором основывается веб-служба ключевого показателя эффективности для финансового отчета.|  
    |**Просмотр по**|Укажите временной интервал, в пределах которого отображается ключевой показатель эффективности для финансового отчета.|  
    |**Имя веб-службы**|Укажите название веб-службы ключевого показателя эффективности для финансового отчета.<br /><br /> Это имя будет отображаться в поле **Имя службы** в окне **Веб-службы**.|  

    Перейти к определению одного или нескольких финансовых отчетов, которые необходимо опубликовать как веб-службу KPI в соответствии с настройками в предыдущей таблице.  

3.  На экспресс-вкладке **Финансовые отчеты** заполните поля, как описано в следующей таблице.  

    |Поле|Описанием|  
    |---------------------------------|---------------------------------------|  
    |**Название финансового отчета**|Укажите финансовый отчет, на котором основана веб-служба ключевого показателя эффективности.|  
    |**Описание финансового отчета**|Укажите описание финансового отчета, на котором основана веб-служба ключевого показателя эффективности.|  

4.  Повторите шаг 3 для всех финансовых отчетов, на которых предполагается основывать веб-службу KPI финансовых отчетов.  
5.  Для просмотра или редактирования выбранного финансового отчета на экспресс-вкладке **Финансовый отчет** выберите действие **Изменение финансового отчета**.  
6.  Чтобы просмотреть настроенные сведения ключевых показателей эффективности для финансового отчета, выберите действие **Веб-служба ключевых показателей эффективности финансового отчета**.  
7.  Для публикации веб-службы ключевых показателей эффективности для финансового отчета выберите действие **Опубликовать веб-службу**. Веб-служба добавляется в список опубликованных веб-служб в окне **Веб-службы**.  

    > [!NOTE]  
    >  Можно также опубликовать веб-службу KPI, подведя указатель к объекту страницы **Настройка веб-службы ключевых показателей эффективности финансового отчета** в окне **Веб-службы**. Дополнительные сведения см. в разделе [Практическое руководство. Публикация веб-службы](https://msdn.microsoft.com/en-us/library/dd338978.aspx) на сайте MSDN.  

## <a name="see-also"></a>См. также  
[Бизнес-аналитика](bi.md)  
[Финансы](finance.md)  
[Настройка финансов](finance-setup-finance.md)  
[Главная книга и план счетов](finance-general-ledger.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
