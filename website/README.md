# [iojs.org](https://iojs.org/)

Цей каталог зберігає файли, необхідні для [@iojs/website](https://github.com/iojs/website).

Оригінальний репозиторій знаходиться [тут](https://github.com/iojs/website). В цьому файлі ми лише переводимо їх власний README.

## Структура проекту

- **content** містить матеріали, переведені групами локалізації. Матеріали повинні бути написані в [Github-flavoured Markdown](https://help.github.com/articles/github-flavored-markdown/);
- **gulp** зберігає скрипти для [Gulp.js](http://gulpjs.com/);
- **public** містить всі файли, які були згенеровані скриптами Gulp.js. Не потрібно щось змінювати в цій директорії напряму. Скоро ми почнемо використовувати [iojs/build](https://github.com/iojs/build) щоб автоматизувати цей процес.
- **source** зберігає стилі та структурні одиниці, котрі необхідні для проекту.
- **wg-meetings** - це архів, в якому зберігаются мітинги Робочої Групи (РГ) (дивіться [../GOVERNANCE.md](../GOVERNANCE.md)).

## Запуск на локальній машині

### Залежності

```
git clone https://github.com/iojs/website.git
npm install -g gulp
npm install
```

### Локальна розробка

```
gulp
```

Запускає локальний HTTP сервер на порту 4657 з live-reload, який онове сторінку в браузері відразу, як зміняться стилі чи контент. Згенеровані файли знаходяться в **public** директорії, готові до публікування.

## Розгортання на сервері

Вебсайт в даний час розміщується на спонсорському 3rd party хостингу, процес розгортання якого керується [командой компонування io.js](https://github.com/iojs/build). Як тільки репозиторій змінюється і зміни інтегровані в master гілку - нова версія автоматично розгортується на хостингі за декілька хвилин.

## Поточні члени проектної групи

* Trent Oswald (@therebelrobot) **Ведучий**
* Mikeal Rogers (@mikeal)
* Jeremiah Senkpiel (@Fishrock123)
* Charlie Robbins (@indexzero)
* Sean Ouimet (@snostorm)
* Zeke Sikelianos (@zeke)
