---
title: "Административные задачи в Business Central | Документы Майкрософт"
description: "Некоторые задачи в Business Central требуют централизованного администрирования и настройки. Познакомьтесь с этими задачами и узнайте, что делать."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/12/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 61b21714465d41369b850289d55c3f4e8d9d5920
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="administration"></a>Администрация
Основные задачи администрирования обычно выполняются в организации исполнителем какой-либо одной роли. Объем этих задач может зависеть от размера организации и должностных обязанностей администратора. Среди подобных задач могут быть следующие: управление синхронизацией с базой данных работ и очередей электронной почты, задание пользователей, настройка пользовательского интерфейса и управление ключами шифрования.  

Ввод правильных значений настройки с самого начала важен для успешной работы любого нового программного обеспечения для бизнеса. [!INCLUDE[d365fin](includes/d365fin_md.md)] включает ряд руководство по настройке, помогающих настроить ключевые данные. Дополнительные сведения см. в разделе [Настройка Business Central](setup.md).

Когда вы используете службы RapidStart Services, чтобы применить значения настройки или вводите их вручную для новой организации, можно поддержать решения о настройке общими рекомендациями для избранных полей настройки, которые потенциально могут снизить эффективность решения, если будут заданы неправильно.  

Администратор или привилегированный пользователь может настроить платформу обмена данными, чтобы разрешить пользователям экспорт и импорт данные в банковских файлах и файлах зарплаты, например, для различных процессов управления денежными средствами.

> [!NOTE]
> Можно настроить новую организацию в [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью служб RapidStart Services, которые представляют собой инструмент, предназначенный для ускорения развертывания, повышения качества внедрения, использования единого подхода к внедрению и повышения производительности за счет автоматизации и упрощения повторяющихся задач. Дополнительные сведения см. в разделе ## [Настройка организации со службами RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.   

|**Задача**|**Ссылка**|  
|------------|-------------|  
|Добавьте пользователей, управляйте разрешениями и доступом к данным, назначьте роли.|[Знакомство с профилями и ролевыми центрами](admin-users-profiles-roles.md)|  
|Назначение разрешений пользователям, изменение наборов разрешений и группирование пользователей по разрешениям.|[Управление пользователями и разрешениями](ui-how-users-permissions.md)|
|Классифицируйте конфиденциальность данных для полей, чтобы можно было отвечать на запросы субъектов данных, связанных с их личными данными.|[Классификация конфиденциальности данных](admin-classifying-data-sensitivity.md)|
|Отвечайте на запросы от субъектов данных, связанные с их личными данными.|[Ответ на запросы о личных данных](admin-responding-to-requests-about-personal-data.md)|
|Настройка нового филиала с помощью шаблонов|[Создание новых организаций](about-new-company.md)|
|Измените поля и действия, которые будут отображаться в пользовательском интерфейсе, в соответствии с бизнес-процессами вашей организации. |[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md) |
|Отслеживание всех непосредственных изменений, вносимых пользователями в данные базы данных, для определения источника ошибок и изменений в данных.|[Регистрация изменений](across-log-changes.md)|  
|Ввод одиночных или повторяющихся запросов для создания отчетов или запуска модулей Codeunit.|[Использование очередей работ для планирования задач](admin-job-queues-schedule-tasks.md)|  
|Управление документами, удаление или сжатие документов|[Удаление документов](admin-manage-documents.md)|  
|Можно отображать страницы, модули codeunit и запросы как веб-службы.|[Публикация веб-службы](across-how-publish-web-service.md)|

## <a name="see-also"></a>См. также
[Функциональные бизнес-возможности](across-business-functionality.md)  
[Общие бизнес-функции](ui-across-business-areas.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Приступая к работе](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
