---
title: "Настройка конфигурации организации | Документы Майкрософт"
description: "Процесс реализации начинается с того, что решение Business Central потребует. Вся эта информация включается в пакеты конфигураций."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: eeca45a36e38ab80a63156995a2f11466262d512
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-company-configuration"></a>Настройка конфигурации организации
Процесс внедрения начинается с партнера Майкрософт. Партнер, отвечающий за продумывание подробностей конфигурации и создание пакета, который клиент может легко применить. Перед созданием новой организации следует спланировать ее настройку. Необходимо учитывать основные данные настройки и типы данных, которые будет запрашивать решение [!INCLUDE[d365fin](includes/d365fin_md.md)]. Вся эта информация включается в пакеты конфигураций.

Службы RapidStart Services также предоставляет вам средства, которые вы будете использовать для миграции своих старых данных, таких как клиенты и поставщики.  

Рекомендуется создать пакеты конфигураций после заполнения большинства таблиц настройки, чтобы клиентам приходилось менять только несколько параметров после применения пакета. Например, при создании новой организации таблицы **Серии номеров** и **Строка серии номеров** заполняются набором серий номеров и начальных номеров. Соответствующие поля **Серия номеров** в таблицах настройки также будут заполнены автоматически. Не требуется выполнять ввод серии номеров и других базовых данных настройки. С помощью журнала конфигураций можно также изменить вручную все данные по умолчанию, которые используются со службами RapidStart Services.  

Пакеты конфигураций построены на предварительно настроенной организации. После настройки организации, соответствующей вашим потребностям, можно создать пакет конфигурации, который будет содержать релевантные данные из этой организации. Затем можно использовать его при создании новой организации, которая будет настроена тем же образом.  

Чтобы облегчить импорт основных данных, таких как данные клиента и поставщика, можно использовать шаблоны конфигураций. Шаблоны конфигураций содержат набор настроек по умолчанию, которые автоматически назначаются записям, импортируемым в [!INCLUDE[d365fin](includes/d365fin_md.md)].

В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.

|**Чтобы**|**Смотрите**|  
|------------|-------------|  
|Запланируйте конфигурацию организации, заполнив журнал конфигурации.|[Управление конфигурацией организации в журнале](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Создайте пакет конфигурации, настройте пакет, назначьте таблицы пакету, проверьте или измените существующие данные клиента, создайте новую организацию, затем перенесите тестовые данные в производственную среду.|[Подготовка пакета конфигурации](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>См. также  
[Настройка компании с помощью служб RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Администрация](admin-setup-and-administration.md)
