# [iojs.org](https://iojs.org/)

Оригінальний репозиторій знаходиться [тут](https://github.com/iojs/website). В цьому файлі ми лише переводимо їх власний README.

## Структура проекту

- **content** містить матеріали, переведені групами локалізації. Матеріали повинні бути написані в [Github-flavoured Markdown](https://help.github.com/articles/github-flavored-markdown/);
- **gulp** зберігає скрипти для [Gulp.js](http://gulpjs.com/);
- **public** містить всі файли, які були згенеровані скриптами Gulp.js. Змінювати щось в ції директорії заборонено. Скоро ми почнемо використовувати [iojs/build](https://github.com/iojs/build) щоб автоматизувати цей процес.
- **source** зберігає стилі та структурні одиниці, котрі необхідні для проекту.
- **wg-meetings** - це архів, в якому зберігаются мітинги Робочої Групи (РГ) (дивіться [../GOVERNANCE.md](../GOVERNANCE.md)).

## Running Locally

### Dependencies
```
git clone https://github.com/iojs/website.git
npm install -g gulp
npm install
```

### Local Development
```
gulp
```
Runs a local HTTP server on port 4657 with live-reload, which will update
your browser immediately with content or style changes. Generated assets
are provided to the [./public]() directory for publishing.

## Deployment

The website is currently hosted on a (sponsored) 3rd party provider with a deployment
process managed via the [io.js build team](https://github.com/iojs/build). As repo
changes are approved and merged to the master branch, changes are automatically
deployed within a few minutes.

## Current Project Team Members

* Trent Oswald (@therebelrobot) **Facilitator**
* Mikeal Rogers (@mikeal)
* Jeremiah Senkpiel (@Fishrock123)
* Charlie Robbins (@indexzero)
* Sean Ouimet (@snostorm)
* Zeke Sikelianos (@zeke)