---
title: Назначение специальных макетов документов клиентам или поставщикам | Microsoft Docs
description: Если определены пользовательские макеты отчетов, вы можете выбрать их из карточек клиентов и поставщиков, чтобы указать, что выбранные макеты будут использоваться для документов, которые вы создаете для данного клиента или поставщика.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: 23c4573c3121a660b8263c3bc9bb2c6ac8b1d331
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809403"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Определение макетов документов для клиентов и поставщиков
Если определены пользовательские макеты отчетов, вы можете выбрать их из карточек клиентов и поставщиков, чтобы указать, какие макеты будут использоваться для документов, которые вы создаете для данного клиента или поставщика. Значение поля **Использование** определяет, для какого процесса будет использоваться макет документа, например **Напоминание**, **Отгрузка** или **Подтверждение**.

Помимо настройки макетов для использования с различными документами, вы можете сэкономить время при отправке документов контактам разных клиентов или поставщиков, настроив адреса электронной почты конкретных контактов для использования с конкретными документами. Например, отчеты по клиентам будут отправляться контактам бухгалтеров, заказы на продажу менеджерам по закупкам ваших клиентов, а заказы на покупку — продавцам или менеджерам по работе с клиентами.

Когда вы определяете макет документа для клиента или поставщика, вы также можете указать адрес электронной почты контактного лица, которое должно получить документ. Вы можете быстро сделать это с помощью функции **Выбрать адрес эл. почты из контактов**, которая автоматически фильтрует контактные адреса электронной почты, зарегистрированные для данного клиента или поставщика.

Прежде чем вы сможете определить, какой макет документа использовать для каких процессов и какому контакту отправлять документ, вы должны загрузить все доступные отчеты (документы) со страницы **Выбор отчетов**. Вы можете быстро сделать это с помощью функции **Копировать со страницы "Выбор отчета"**.

Далее описывается, как определить макеты документов продаж из карточки клиента. Шаги одинаковы для макетов документов покупки в карточке поставщика.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Чтобы включить все доступные документы продаж для клиента
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Клиенты**, затем выберите соответствующую ссылку.
2. Откройте карточку клиента, для которого вы хотите определить макеты документов для конкретного бизнес-процесса.
3. На странице **Карточка клиента** выберите страницу **Макеты документов**.
4. На странице **Макеты документов** выберите действие **Копировать со страницы "Выбор отчета"**.

Страница **Макеты документов** для данного клиента будет заполнена всеми макетами отчетов для продаж, которые существуют в системе. Дополнительные сведения об их создании см. в разделе [Создание и изменение пользовательских макетов отчетов](ui-how-create-custom-report-layout.md).

Теперь вы можете приступить к настройке списка с пользовательскими макетами отчетов или адресами электронной почты контактов, которым должны отправляться документы.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Чтобы выбрать пользовательский макет отчета для документа продаж
Если для одного или нескольких макетов отчетов, определенных на странице **Макеты документов** клиента, не определен пользовательский макет, вы можете быстро это сделать.

1. На странице **Макеты документов** в строке макета отчета, для которого вы хотите использовать пользовательский макет, выберите поле **Описание пользовательского макета**. Поле заполнено, если макет клиента уже выбран, или является пустым.
2. На странице **Пользовательские макеты отчетов** выберите макет специального документа, который вы хотите использовать для рассматриваемого типа документов продаж. Дополнительные сведения см. в разделе [Создание и изменение пользовательских макетов отчетов](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Чтобы задать контакт клиента, который получает документ с определенным макетом
Вы можете сэкономить время при отправке документов разным контактам клиентов или поставщиков, указав контактные адреса электронной почты в разных строках на странице **Макеты документов**. Например, отчеты по клиентам могут отправляться контактам бухгалтеров, заказы на продажу менеджерам по закупкам ваших клиентов, а заказы на покупку — продавцам или менеджерам по работе с клиентами.

1. На странице **Макеты документов** в строке макета отчета, который вы хотите отправить конкретному контакту клиента, выберите действие **Выбрать адрес эл. почты из контактов**.
2. На странице **Контакты** выберите строку соответствующего контакта, а затем нажмите кнопку **ОК**.

Адрес электронной почты контакта теперь вставляется в строку макета документа, поэтому соответствующий документ продажи, например напоминание, всегда отправляется этому контакту в компании клиента.

## <a name="see-also"></a>См. также  
[Обновление пользовательских макетов отчетов](ui-update-report-layouts.md)  
[Создание и изменение пользовательских макетов отчетов](ui-how-create-custom-report-layout.md)  
[Импорт и экспорт пользовательского макета отчета или документа](ui-how-import-and-export-report-layout.md)  
[Отправка документов по электронной почте](ui-how-send-documents-email.md)  
[Управление макетами отчетов](ui-manage-report-layouts.md)  
[Работа с отчетами, пакетными заданиями и XMLport](ui-work-report.md)  
[Работа с отчетами, пакетными заданиями и XMLport](ui-work-report.md)  