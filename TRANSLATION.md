# Політика перекладу сайту io.js

io.js - глобальна платформа, отже вона має декілька локалізацій.
Перекладом на окремі мови займаються перекладачі робочої групи певної мови. Якщо Ви хочете внести свій внесок у переклад iojs, будь ласка, керуйтесь наступною інструкцією:

## Для осіб, які бажають зробити свій внесок

* Зверніться до відповідної групи по локалізації, і обговоріть з ними як можна краще внести свій вклад. Список груп локалізації можна знайти тут:
    * [`iojs-bn`](https://github.com/iojs/iojs-bn) Бенгальська Група
    * [`iojs-cn`](https://github.com/iojs/iojs-cn) Китайська Група 
    * [`iojs-cs`](https://github.com/iojs/iojs-cs) Чеська Група 
    * [`iojs-da`](https://github.com/iojs/iojs-da) Данська Група 
    * [`iojs-de`](https://github.com/iojs/iojs-de) Німецька Група
    * [`iojs-el`](https://github.com/iojs/iojs-el) Грецька Група
    * [`iojs-es`](https://github.com/iojs/iojs-es) Іспанська Група
    * [`iojs-fa`](https://github.com/iojs/iojs-fa) Перська Група 
    * [`iojs-fi`](https://github.com/iojs/iojs-fi) Фінська Група
    * [`iojs-fr`](https://github.com/iojs/iojs-fr) Французька Група
    * [`iojs-he`](https://github.com/iojs/iojs-he) Івритська Група
    * [`iojs-hi`](https://github.com/iojs/iojs-hi) Хінді Група 
    * [`iojs-hu`](https://github.com/iojs/iojs-hu) Угорськf Група
    * [`iojs-id`](https://github.com/iojs/iojs-id) Індонезійська Група
    * [`iojs-it`](https://github.com/iojs/iojs-it) Італійськf Група
    * [`iojs-ja`](https://github.com/iojs/iojs-ja) Японська Група
    * [`iojs-ka`](https://github.com/iojs/iojs-ka) Грузинська Група
    * [`iojs-kr`](https://github.com/iojs/iojs-kr) Корейська Група
    * [`iojs-mk`](https://github.com/iojs/iojs-mk) Македонська Група
    * [`iojs-nl`](https://github.com/iojs/iojs-nl) Голландська Група
    * [`iojs-no`](https://github.com/iojs/iojs-no) Норвезька Група
    * [`iojs-pl`](https://github.com/iojs/iojs-pl) Польська Група
    * [`iojs-pt`](https://github.com/iojs/iojs-pt) Португальська Група
    * [`iojs-ro`](https://github.com/iojs/iojs-ro) Румунська Група
    * [`iojs-ru`](https://github.com/iojs/iojs-ru) Російська Група
    * [`iojs-sv`](https://github.com/iojs/iojs-sv) Шведська Група
    * [`iojs-tr`](https://github.com/iojs/iojs-tr) Турецька Група
    * [`iojs-tw`](https://github.com/iojs/iojs-tw) Тайванська Група
    * [`iojs-uk`](https://github.com/iojs/iojs-uk) Українська Група
    
## Для групп локалізації

* Переконайтеся, що всі переклади на сайті зроблені як pull-запити в цей репозиторій. Це дозволить забезпечити незмінний процес збірки для всіх перекладів сайту.
* Ви можете знайти папку з відповідною мовою в `content/`
* В ній повинні бути наступні файли:
    * `template.json` (для тексту в кнопках і заголовка з відповідним перекладом)
    * `index.md` (він містить переклад markdown головної сторінки. Порядок параграфів має значення, тому, будь ласка, підтримуйте його)
    * `faq.md` (markdown для сторінки faq)
    * `es6.md` (markdown для роз'яснювальної сторінки про ES6 explanation page)
    * Будь-які додаткові md файли які повинні бути додані можуть бути створені тут, вони будуть динамічно генеруватись в HTML за допомогою шаблону.

* Не робіть специфічних мовних змін до макета або стилю в перекладі у PR. Якщо вони необхідні, зробіть окремий PR для стилю/макета та обговоріть це з участником РГ по веб-сайту. Ми хочемо переконатися, що, наприклад, зміна китайського макета не створить проблем для німецької сторінки.
* Щоб PR на переклад було прийнято, він вимагає +1 від учасника РГ по сайту, та +1 від іншого носія вашої мови. Переконайтесь в тому, хто додає +1 в коментарі до вашого PR, щоб ми знали, що переклад виконаний правильно.
