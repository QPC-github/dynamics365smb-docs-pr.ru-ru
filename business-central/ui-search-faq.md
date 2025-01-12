---
title: Вопросы и ответы о функции "Что вы хотите сделать"
description: 'Эта статья содержит ответы на вопросы, которые наши партнеры и клиенты часто задают по поводу функции "Что вы хотите сделать".'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: TellMe
ms.date: 05/23/2022
ms.author: bholtorf
---
# <a name="tell-me-faq" />Вопросы и ответы о функции "Что вы хотите сделать"
В этой статье содержатся ответы на вопросы, которые часто задают наши продвинутые пользователи о функции "Что вы хотите сделать"

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me" />Все ли действия из текущей страницы могут быть обнаружены в функции "Что вы хотите сделать"?

Нет. Действия в частях, таких как часть строк продажи или информационные панели, не отображаются в функции "Что вы хотите сделать".

### <a name="are-the-results-in-tell-me-filtered-by-permissions" />Фильтруются ли результаты функции "Что вы хотите сделать" по правам доступа?

Если пользователь не имеет AccessByPermissions, такие действия не отображаются. Однако страниц и отчеты появляются в результатах, но пользователю необходимо имеет право на получение доступа к ним. Показывается сообщение, если пользователь не имеет прав на просмотр объекта.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions" />Показывает ли функция "Что вы хотите сделать" содержимое из моих настроек или установленных расширений третьих сторон?

Действия, страницы и отчеты, которые происходят из расширений, охватываются функцией "Что вы хотите сделать". Технические сведения о том, как сделать настроенные страницы и отчеты обнаруживаемыми, см. в разделе [Добавление страниц и отчетов в поиск](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search" />Чем эта функция отличается от ранее известной функции поиска страниц?

Поиск страниц эволюционировал в функцию "Что вы хотите сделать", чтобы помочь работать быстрее. Поиск страниц мог помочь только переходить к страницам или отчетам. На техническом уровне функция "Что вы хотите сделать" больше не основывается на концепции MenuSuite.

### <a name="i-use-on-premises-includeprodshortincludesprodshortmd-does-that-include-tell-me" />Я использую локальную версию [!INCLUDE[prod_short](includes/prod_short.md)]. Она включает функцию "Что вы хотите сделать"?

Можно использовать функцию "Что вы хотите сделать" в веб-клиенте локальной версии для поиска действий, страниц и отчетов, но не приложений и консультативных услуг в AppSource.

### <a name="is-tell-me-available-for-all-form-factors" />Доступна ли функция "Что вы хотите сделать" для всех форм-факторов?

Функция "Что вы хотите сделать" доступна только в веб-клиента или в приложении рабочего стола Windows.

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language" />Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

### <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things" />Помогает ли функция "Что вы хотите сделать" пользоваться страницами, отчетами и другими вещами?

Нет, но вы можете легко получить эту информацию из области справки. Просто выберите пункт меню **Справка** (знак вопроса в правом верхнем углу) или нажмите <kbd>Ctrl</kbd>+<kbd>F1</kbd> на клавиатуре. Дополнительные сведения см. в разделе [Панель справки](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results" />Почему я не вижу значка закладки для результатов поиска?

Значок закладки не отображается в окне "Что вы хотите сделать", когда для роли пользователя отключена персонализация.


## <a name="see-also" />См. также
[Сохранение и персонализация представлений списков](ui-views.md)  
[Поиск страниц и информации с помощью функции "Что вы хотите сделать"](ui-search.md)  
[Поиск страниц с помощью обозревателя ролей](ui-role-explorer.md)  
[Добавление закладки на страницу или отчет в ролевом центре](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
