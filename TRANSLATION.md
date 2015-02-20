# Політика перекладу сайту io.js

io.js - глобальна платформа, отже цей сайт має декілька локалізацій.
Перекладом сайту на окремі мови займаються перекладачі робочої групи певної мови. Якщо Ви хотіли би внести свій внесок у переклад iojs.org, будь ласка, керуйтесь наступною інструкцією:

## Для осіб, які бажають зробити свій внесок
* Зверніться до відповідної групи по локалізації, і обговоріть з ними як можна краще внести свій вклад. Список груп локалізації можна знайти тут:
    * [`iojs-bn`](https://github.com/iojs/iojs-bn) Бенгальска Группа
    * [`iojs-cn`](https://github.com/iojs/iojs-cn) Китайська Группа 
    * [`iojs-cs`](https://github.com/iojs/iojs-cs) Чеська Группа 
    * [`iojs-da`](https://github.com/iojs/iojs-da) Данська Группа 
    * [`iojs-de`](https://github.com/iojs/iojs-de) Німецька Группа
    * [`iojs-el`](https://github.com/iojs/iojs-el) Грецька Группа
    * [`iojs-es`](https://github.com/iojs/iojs-es) Іспанська Группа
    * [`iojs-fa`](https://github.com/iojs/iojs-fa) Перська Группа 
    * [`iojs-fi`](https://github.com/iojs/iojs-fi) Фінська Группа
    * [`iojs-fr`](https://github.com/iojs/iojs-fr) Французька Группа
    * [`iojs-he`](https://github.com/iojs/iojs-he) Івритська Группа
    * [`iojs-hi`](https://github.com/iojs/iojs-hi) Хінді Группа 
    * [`iojs-hu`](https://github.com/iojs/iojs-hu) Угорськf Группа
    * [`iojs-id`](https://github.com/iojs/iojs-id) Індонезійська Группа
    * [`iojs-it`](https://github.com/iojs/iojs-it) Італійськf Группа
    * [`iojs-ja`](https://github.com/iojs/iojs-ja) Японська Группа
    * [`iojs-ka`](https://github.com/iojs/iojs-ka) Грузинська Группа
    * [`iojs-kr`](https://github.com/iojs/iojs-kr) Корейська Группа
    * [`iojs-mk`](https://github.com/iojs/iojs-mk) Македонська Группа
    * [`iojs-nl`](https://github.com/iojs/iojs-nl) Голландська Группа
    * [`iojs-no`](https://github.com/iojs/iojs-no) Норвезька Группа
    * [`iojs-pl`](https://github.com/iojs/iojs-pl) Польська Группа
    * [`iojs-pt`](https://github.com/iojs/iojs-pt) Португальська Группа
    * [`iojs-ro`](https://github.com/iojs/iojs-ro) Румунська Группа
    * [`iojs-ru`](https://github.com/iojs/iojs-ru) Російська Группа
    * [`iojs-sv`](https://github.com/iojs/iojs-sv) Шведська Группа
    * [`iojs-tr`](https://github.com/iojs/iojs-tr) Турецька Группа
    * [`iojs-tw`](https://github.com/iojs/iojs-tw) Тайванська Группа
    * [`iojs-uk`](https://github.com/iojs/iojs-uk) Українська Группа
    
## Для групп локалізації
* Переконайтеся, що всі переклади на сайті зроблені як pull-запити в цьому репозиторії. Це дозволить забезпечити процес білдингу, розміщення та стиль, залишаються незмінними в усіх перекладах сайту.
* Ви можете знайти папку з відповідною мовою в `content/`
* В ній повинні бути наступні файли:
    * `template.json` (для тексту в кнопках і заголовка з відповідним перекладом)
    * `index.md` (він містить переклад markdown головної сторінки. Порядок параграфів має значення, тому, будь ласка, підтримуйте його)
    * `faq.md` (markdown для сторінки faq)
    * `es6.md` (markdown для роз'яснювальної сторінки про ES6 explanation page)
    * Будь-які додаткові md файли які повинні бути додані можуть бути створені тут, вони будуть динамічно генеруватись в HTML за допомогою шаблону.

* Не робіть специфічних мовних змін до макета або стилю в перекладі у PR.
Якщо вони необхідні, зробиіть окремий PR для стилю/макета та обговоріть це з участником РГ по веб-сайту. Ми хочемо переконатися, що, наприклад, зміна китайського макета не створить проблем для німецької сторінки.
* Щоб PR на перелад було прийнято, він вимагає +1 від учасника РГ по сайту, та +1 від іншого носія вашої мови. Переконайтесь в тому, хто додадє +1 в комметарі до вашого PR, щоб ми знали, що переклад виконаний правильно.