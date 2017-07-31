---
title: "Импорт транзакций по зарплате | Документы Майкрософт"
description: "Для управления зарплатой необходимо импортировать финансовые транзакции от поставщика заработной платы непосредственно в главную книгу, используя расширение для зарплаты, например Ceridian или Quickbooks."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d53dfb26a3fea663e68a3b558579a59184e9de26
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-import-payroll-transactions"></a>Практическое руководство: импорт транзакций по зарплате
Для учета выплаты зарплаты и связанных транзакций необходимо импортировать и учесть финансовые транзакции, сделанные поставщиком системы зарплаты, в главную книгу. Чтобы это сделать, следует сначала импортировать файл, полученный от поставщика системы зарплаты, в окно **Финансовый журнал**. Затем следует сопоставить внешние счета в файле зарплаты с соответствующими счетами ГК. Наконец требуется учесть транзакции зарплаты в соответствии с сопоставлением счетов.

> [!NOTE]  
>   Чтобы воспользоваться этой функцией, расширение для импорта зарплаты необходимо установить и включить. Расширения "Зарплата Ceridian" и "Импорт файла зарплаты Quickbooks" предварительно установлены в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Импорт файла зарплаты
1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Финансовые журналы**, а затем выберите связанную ссылку.
2. В соответствующем разделе финансового журнала выберите действие **Импорт транзакций зарплаты**. Откроется руководство по сопровождаемой настройке.
3. Выполните шаги в окне **Импорт транзакций зарплаты**.

    > [!TIP]  
>   На шаге сопоставления внешних записей зарплаты со счетами ГК выполненные сопоставления будут отображаться при следующем импорте тех же записей. Это экономит время, поскольку вам не требуется вручную заполнять поле **Номер счета** в финансовом журнале при каждом импорте повторяющихся транзакций зарплаты.   

    При нажатии кнопки **ОК** в руководстве по сопровождаемой настройке окно **Финансовый журнал** будет заполнено строками, представляющими транзакции, содержащиеся в файле зарплаты, с соответствующими счетами, предварительно заполненными в полях **Счет ГК** в соответствии с сопоставлениями, выполненными в руководстве.
4. Отредактируйте или учтите строки журнала, как и для любых других транзакций главной книги. Дополнительные сведения см. в разделе [Практическое руководство. Учет транзакций непосредственно в главной книге](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>См. также
[Финансы](finance.md)  
[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md)  
[Работа с финансовыми журналами](ui-work-general-journals.md)  
