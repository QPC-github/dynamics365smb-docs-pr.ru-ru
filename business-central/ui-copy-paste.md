---
title: "Копирование и вставка данных"
description: "Копируйте поля и строки со страниц Business Central и вставляйте их в другие места."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e924eeb10e98b81035837ca498ec4f1a7b28bf60
ms.contentlocale: ru-ru
ms.lasthandoff: 09/28/2018

---

# <a name="copying-and-pasting-in-included365finincludesd365finmdmd"></a>Копирование и вставка в [!INCLUDE[d365fin](includes/d365fin_md.md)]
Можно скопировать один или несколько строк из списка или одно поле на странице, а затем вставить скопированное на ту же страницу, другую страницу или во внешний документ (например, Microsoft Excel или сообщение электронной почты Outlook). Вкратце, чтобы скопировать, нажмите CTRL+C (cmd+C в macOS) на клавиатуре. Для вставки нажмите CTRL+V (cmd+V в macOS).

Имеется нескольких других сочетаний клавиш для копирования и вставки, которые помогаю экономить время при вводе данных. Дополнительные сведения о них см. в разделе [Сочетания клавиш](keyboard-shortcuts.md#CopyRows).

Эта статья отвечает на часто возникающие вопросы по копированию и вставке.  

## <a name="what-can-i-copy-and-paste"></a>Что можно скопировать и вставить?
-   Копирование одной или нескольких строк в [!INCLUDE[d365fin](includes/d365fin_md.md)] в тот же список или в любой список с идентичными столбцами.
-   Копирование одной или нескольких строк в [!INCLUDE[d365fin](includes/d365fin_md.md)] и вставка в Excel или другие приложения.
-   Копирование одной или нескольких строк в Excel и вставка в список [!INCLUDE[d365fin](includes/d365fin_md.md)].
-   Скопируйте значение в отдельном поле [!INCLUDE[d365fin](includes/d365fin_md.md)] и вставьте в другое место.

## <a name="how-do-i-copy-rows"></a>Как копировать строки?
Для копирования одной строки выберите ее и нажмите кнопки CTRL+C.

При необходимости скопировать несколько строк, можно:
-   Нажмите CTRL+щелкните на другой строке или нажмите SHIFT+щелкните, чтобы выбрать все строки между ними. Дополнительные комбинаций мыши и клавиатуры для выбора строк см. в разделе [Сочетание клавиш](keyboard-shortcuts.md#CopyRows).
-   Выберите ![Показать больше параметров](media/show-more-options-icon.png "Значок Показать больше параметров") в первом столбце строки, выберите **Выбрать больше**, установите флажок рядом с каждой строкой, которую требуется скопировать, затем нажмите CTRL+C.

## <a name="how-do-i-paste-rows"></a>Как вставлять строки?
Выделите пустую строку и нажмите кнопки CRTL+V. Если требуется заменить существующие строки, выберите строки и нажмите CRTL+V. В этом случае можно вставить только такое же количество строк, что и выбранное.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email-or-onenote"></a>Можно ли вставить строки в сообщение электронной почты Outlook или в OneNote?
Да. Это вставляется как форматированная таблица, которая сохраняет отступы, числовое выравнивание и цвета, как оно отображалось бы в [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="does-copy-and-paste-work-with-tiles"></a>Работает ли копирование и вставка с плитками?
Нет. Список необходимо просмотреть как строки (представление списка) для копирования и вставки.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>В каких списках можно копировать и вставлять строки?
Строки можно копировать в списках любых типов, включая листы, информационные панели или списки, которые внедрены в страницу (например, строки заказа продажи). Однако чтобы вставить строки, список должен быть редактируемым.

На некоторых страницах дизайн приложения может не позволять вставку строк. Обратитесь к администратору или разработчику программного обеспечения, чтобы изменить [свойство Editable](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) или [свойство PasteIsValid](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) в исходной таблице.

## <a name="on-which-clients-is-copy-and-paste-available"></a>На каких клиентах доступны копирование и вставка?
Копирование и вставка доступны в браузере или в приложении [!INCLUDE[d365fin](includes/d365fin_md.md)] для Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Какое максимальное число строк можно скопировать?
Можно скопировать столько строк, сколько можно прокрутить в представлении. Например, чтобы скопировать все 1000 строк на странице, перед копированием необходимо прокрутить страницу до самого низа, затем дождаться, пока появятся строки. Максимальное число строк, которые можно копировать, ограничивается только памятью устройства.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Необходимо ли наличие точно такого же числа столбцов перед вставкой строк?
Да. Производится ли копирование из [!INCLUDE[d365fin](includes/d365fin_md.md)], из Excel или из другого источника таблицы, строки, которые вы вставляете, должны иметь точно соответствующие столбцы — не более и не менее.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Почему я получают ошибки при вставке строки?
При вставке в [!INCLUDE[d365fin](includes/d365fin_md.md)] каждая строка проверяются, чтобы убедиться, что значения в каждом столбце действительны. Если столбец содержит недопустимое значение, вставка останавливается и отображается сообщение об ошибке. Чтобы избежать этого, убедитесь, что в столбцах содержатся допустимые значения перед их вставкой.


## <a name="see-also"></a>См. также
[Вспомогательные функции](ui-accessibility.md)  
[Приступая к работе](product-get-started.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Вопросы и ответы](across-faq.md)  
