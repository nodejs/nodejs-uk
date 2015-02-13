# ES6 в io.js

io.js побудований на основі сучасних версій [V8](https://code.google.com/p/v8/). Підтримуючи останні версії [V8](https://code.google.com/p/v8/) в io.js, ми гарантуємо наявність нових можливостей [JavaScript ECMA-262 specification](http://www.ecma-international.org/publications/standards/Ecma-262.htm), які привносяться до io.js розробників своєчасно, а також підвищують швидкість роботи та стабільність.

Версія io.js 1.2.0 має версію V8 4.1.0.14, яка включає в себе ES6 можливості, котрих немає в V8 3.28.73, яка іде в поставці з Node - [generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*), які мають дуже мало, а то і взагалі, не мають дискусій. Таким чином, більшість розробників вмикають лише ті можливості ES6, які їм потрібні, за допомогою спеціального флагу (наприклад `--harmony-generators`), чи просто вмикають їх всі.

З io.js@1.x (V8 4.1+) складність використання ES6 можливостей зникає. Всі harmony можливості логічно розподілені на три групи **shipping**, **staged** та **in progress**:

*   **shipping** можливості, які V8 помітив як стабільні, наприклад [generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*), [templates](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/template_strings), [new string methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/ECMAScript_6_support_in_Mozilla#Additions_to_the_String_object) та багато інших, ввімкнуті **по замовчуванню в io.js** і **НЕ** потребують ніяких додаткових параметрів запуску.
*   Крім того, є **staged** можливості, котрі майже завершені, але ще не протестовані повністю, чи не оновлені до останніх специфікацій, тому команда V8 вважає їх нестабільними. Яскравий приклад **staged** можливості - це [generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) в V8 3.26. Можливості типу "використовуйте на свій страх і ризик", які потребують параметр запуску: `--es_staging` (чи його синонім, `--harmony`).
*   І нарешті, всі **in progress** можливості можна активувати окремо, використовуючи відповідний параметр запуску (наприклад `--harmony_arrow_functions`), хоча це і не рекомендується.

## Які можливості ES6 ідуть з io.js по замовчуванню (без необхідності використовувати параметри запуску)?

*   Block scoping

    *   [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)

    *   [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)

    *   `function`-in-blocks

    >Станом на V8 3.31.74.1, block-scoped declarations [навмисно реалізовані з обмеженнями в strict mode](https://groups.google.com/forum/#!topic/v8-users/3UXNCkAU8Es). Розробники мають знати, що це зміниться в наступних версіях V8, які продовжують інтегрувати нові можливості ES6.

*   Collections

    *   [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)

    *   [WeakMap](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)

    *   [Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)

    *   [WeakSet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)

*   [Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*)

*   [Binary and Octal literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Numeric_literals)

*   [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

*   [New String methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/ECMAScript_6_support_in_Mozilla#Additions_to_the_String_object)

*   [Symbols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)

*   [Template strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/template_strings)

Ви можете переглянути більш докладний список, в тому числі і порівняння з іншими "двигунами", в [таблиці порівняння](https://kangax.github.io/compat-table/es6/).

## Які ES6 можливості вмикаються із --es_staging параметром?

*   [Classes](https://github.com/lukehoban/es6features#classes) (лише в strict mode, з параметром `--harmony_classes`, which implies block scoping & object literal extensions)

*   [Object literal extensions](https://github.com/lukehoban/es6features#enhanced-object-literals) (з параметром запуску `--harmony_object_literals`)

*   [`Symbol.toStringTag`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol) (user-definable results for `Object.prototype.toString`, з параметром `--harmony_tostring`)

## Котрі ES6 можливості в стадії розробки?

Нові можливості постійно добавляються в V8. Взагалі кажучи, ми очікуємо, що вони з'являться в наступних io.js релізах, хоча терміни і невідомі.

Ви можете продивитись список всіх *in progress* можливостей в кожному io.js релізі, запустивши iojs з параметром `--v8-options`. Будь ласка, зверніть увагу, що це нестабільні можливості V8, тому використовуйте їх на свій страх і ризик:

```sh
iojs --v8-options | grep "in progress"
```

## I have my infrastructure set up to leverage the --harmony flag. Should I remove it?

The current behaviour of the `--harmony` flag on io.js is to enable **staged** features only. After all, it is now a synonym of `--es_staging`. As mentioned above, these are completed features that have not been considered stable yet. If you want to play safe, especially on production environments, consider removing this runtime flag until it ships by default on V8 and, consequently, on io.js. If you keep this enabled, you should be prepared for further io.js upgrades to break your code if V8 changes their semantics to more closely follow the standard.

## How do I find which version of V8 ships with a particular version of io.js?

io.js provides a simple way to list all dependencies and respective versions that ship with a specific binary through the `process` global object. In case of the V8 engine, type the following in your terminal to retrieve its version:

```sh
iojs -p process.versions.v8
```js