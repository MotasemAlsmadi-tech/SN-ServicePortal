
Upcoming changes to history
Translation history will soon only be available when you are signed in and will be centrally managed within My Activity. Past history will be cleared during this upgrade, so make sure to save translations you want to remember for ease of access later.
Got it
# gulp-scss-starter

![GitHub release](https://img.shields.io/github/release/andreyalexeich/gulp-scss-starter.svg)
[![dependencies Status](https://david-dm.org/andreyalexeich/gulp-scss-starter/status.svg)](https://david-dm.org/andreyalexeich/gulp-scss-starter)
[![devDependencies Status](https://david-dm.org/andreyalexeich/gulp-scss-starter/dev-status.svg)](https://david-dm.org/andreyalexeich/gulp-scss-starter?type=dev)
![GitHub stars](https://img.shields.io/github/stars/andreyalexeich/gulp-scss-starter.svg?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/andreyalexeich/gulp-scss-starter.svg?style=social)
<a href="https://www.qiwi.com/n/ANDREYALEXEICH">
<img src="https://img.shields.io/badge/%D0%97%D0%B0%D0%B4%D0%BE%D0%BD%D0%B0%D1%82%D1%8C%20%D0%BD%D0%B0%20%D0%BF%D0%B8%D0%B2%D0%BE-Qiwi-orange.svg">
</a>
<a href="https://www.paypal.me/andreyalexeich/">
<img src="https://img.shields.io/badge/%D0%97%D0%B0%D0%B4%D0%BE%D0%BD%D0%B0%D1%82%D1%8C%20%D0%BD%D0%B0%20%D0%BF%D0%B8%D0%B2%D0%BE-PayPal-informational.svg">
</a>
<a href="https://www.tinkoff.ru/cardtocard/">
<img src="https://img.shields.io/badge/%D0%97%D0%B0%D0%B4%D0%BE%D0%BD%D0%B0%D1%82%D1%8C%20%D0%BD%D0%B0%20%D0%BF%D0%B8%D0%B2%D0%BE-%D0%9D%D0%B0%20%D0%BA%D0%B0%D1%80%D1%82%D1%83%20--%205536%209137%205288%201934-informational.svg">
</a>

## Особенности
* именование классов по [БЭМ](https://ru.bem.info/)
* используется БЭМ-структура
* используется препроцессор [SCSS](https://sass-lang.com/)
* используется транспайлер [Babel](https://babeljs.io/) для поддержки современного JavaScript (ES6) в браузерах
* используется [Webpack](https://webpack.js.org/) для сборки JavaScript-модулей
* используется CSS-сетка [smart-grid](https://github.com/dmitry-lavrik/smart-grid) на основе Bootstrap для быстрой адаптивной вёрстки
* используется жёсткий кодгайд
* используется проверка кода на ошибки перед коммитом

## Установка
* установите [NodeJS](https://nodejs.org/en/) (если требуется) и [Yarn](https://yarnpkg.com/en/docs/install)
* скачайте сборку с помощью [Git](https://git-scm.com/downloads): ```git clone https://github.com/andreyalexeich/gulp-scss-starter.git```
* установите ```gulp``` глобально: ```yarn global add gulp-cli```
* установите ```bem-tools-core``` глобально: ```yarn global add bem-tools-core```
* перейдите в скачанную папку со сборкой: ```cd gulp-scss-starter```
* скачайте необходимые зависимости: ```yarn```
* чтобы начать работу, введите команду: ```yarn run dev``` (режим разработки)
* чтобы собрать проект, введите команду ```yarn run build``` (режим сборки)

Если вы всё сделали правильно, у вас должен открыться браузер с локальным сервером. Режим сборки предполагает оптимизацию проекта: сжатие изображений, минифицирование CSS и JS-файлов для загрузки на сервер.

## Файловая структура

```
gulp-scss-starter
├── dist
├── gulp-tasks
├── src
│   ├── blocks
│   ├── fonts
│   ├── img
│   ├── js
│   ├── styles
│   ├── views
│   └── .htaccess
├── gulpfile.babel.js
├── webpack.config.js
├── package.json
├── .babelrc.js
├── .bemrc.js
├── .eslintrc.json
├── .stylelintrc
├── .stylelintignore
└── .gitignore
```

* Корень папки:
    * ```.babelrc.js``` — настройки Babel
    * ```.bemrc.js``` — настройки БЭМ
    * ```.eslintrc.json``` — настройки ESLint
    * ```.gitignore``` – запрет на отслеживание файлов Git'ом
    * ```.stylelintrc``` — настройки Stylelint
    * ```.stylelintignore``` – запрет на отслеживание файлов Stylelint'ом
    * ```gulpfile.babel.js``` — настройки Gulp
    * ```webpack.config.js``` — настройки Webpack
    * ```package.json``` — список зависимостей
* Папка ```src``` - используется во время разработки:
    * БЭМ-блоки: ```src/blocks```
    * шрифты: ```src/fonts```
    * изображения: ```src/img```
    * JS-файлы: ```src/js```
    * страницы сайта: ```src/views/pages```
    * SCSS-файлы: ```src/styles```
    * HTML-файлы: ```src/views```
    * конфигурационный файл веб-сервера Apache с настройками [gzip](https://habr.com/ru/post/221849/) (сжатие без потерь): ```src/.htaccess```
* Папка ```dist``` - папка, из которой запускается локальный сервер для разработки (при запуске ```yarn run dev```)
* Папка ```gulp-tasks``` - папка с Gulp-тасками

## Команды
* ```yarn run lint:styles``` - проверить SCSS-файлы. Для VSCode необходимо установить [плагин](https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint). Для WebStorm
или PHPStorm необходимо включить Stylelint в ```Languages & Frameworks - Style Sheets - Stylelint``` (ошибки будут исправлены автоматически при сохранении файла)
* ```yarn run lint:styles --fix``` - исправить ошибки в SCSS-файлах
* ```yarn run lint:scripts``` - проверить JS-файлы
* ```yarn run lint:scripts --fix``` - исправить ошибки в JS-файлах
* ```yarn run dev``` - запуск сервера для разработки проекта
* ```yarn run build``` - собрать проект с оптимизацией без запуска сервера
* ```yarn run build:views``` - собрать HTML-файлы
* ```yarn run build:styles``` - скомпилировать SCSS-файлы
* ```yarn run build:s
5000/5000
Character limit: 5000
# gulp-scss-starter

! [GitHub release] (https://img.shields.io/github/release/andreyalexeich/gulp-scss-starter.svg)
[! [dependencies Status] (https://david-dm.org/andreyalexeich/gulp-scss-starter/status.svg)] (https://david-dm.org/andreyalexeich/gulp-scss-starter)
[! [devDependencies Status] (https://david-dm.org/andreyalexeich/gulp-scss-starter/dev-status.svg)] (https://david-dm.org/andreyalexeich/gulp-scss-starter ? type = dev)
! [GitHub stars] (https://img.shields.io/github/stars/andreyalexeich/gulp-scss-starter.svg?style=social)
! [GitHub watchers] (https://img.shields.io/github/watchers/andreyalexeich/gulp-scss-starter.svg?style=social)
<a href="https://www.qiwi.com/n/ANDREYALEXEICH">
<img src = "https://img.shields.io/badge/%D0%97%D0%B0%D0%B4%D0%BE%D0%BD%D0%B0%D1%82%D1%8C% 20% D0% BD% D0% B0% 20% D0% BF% D0% B8% D0% B2% D0% BE-Qiwi-orange.svg ">
</a>
<a href="https://www.paypal.me/andreyalexeich/">
<img src = "https://img.shields.io/badge/%D0%97%D0%B0%D0%B4%D0%BE%D0%BD%D0%B0%D1%82%D1%8C% 20% D0% BD% D0% B0% 20% D0% BF% D0% B8% D0% B2% D0% BE-PayPal-informational.svg ">
</a>
<a href="https://www.tinkoff.ru/cardtocard/">
<img src = "https://img.shields.io/badge/%D0%97%D0%B0%D0%B4%D0%BE%D0%BD%D0%B0%D1%82%D1%8C% 20% D0% BD% D0% B0% 20% D0% BF% D0% B8% D0% B2% D0% BE-% D0% 9D% D0% B0% 20% D0% BA% D0% B0% D1% 80 % D1% 82% D1% 83% 20 -% 205536% 209137% 205288% 201934-informational.svg ">
</a>

## Features
* class naming according to [BEM] (https://ru.bem.info/)
* BEM structure is used
* [SCSS] preprocessor is used (https://sass-lang.com/)
* The [Babel] transporter (https://babeljs.io/) is used to support modern JavaScript (ES6) in browsers
* used [Webpack] (https://webpack.js.org/) to build JavaScript modules
* uses CSS-grid [smart-grid] (https://github.com/dmitry-lavrik/smart-grid) based on Bootstrap for fast adaptive layout
* uses a hard code guide
* error checking code is used before commit

## Installation
* install [NodeJS] (https://nodejs.org/en/) (if required) and [Yarn] (https://yarnpkg.com/en/docs/install)
* download the assembly using [Git] (https://git-scm.com/downloads): `` `git clone https: // github.com / andreyalexeich / gulp-scss-starter.git```
* install `` gulp``` globally: `` `yarn global add gulp-cli``
* Install `` bem-tools-core``` globally: `` `yarn global add bem-tools-core```
* go to the downloaded folder with the assembly: `` `` cd gulp-scss-starter```
* Download the necessary dependencies: `` `` yarn```
* to get started, enter the command: `` `yarn run dev``` (development mode)
* to build the project, enter the command `` yarn run build`` (build mode)

If you did everything correctly, you should open a browser with a local server. Build mode involves optimizing the project: compressing images, minifying CSS and JS files to upload to the server.

## file structure

`` ``
gulp-scss-starter
├── dist
├── gulp-tasks
├── src
│ ├── blocks
│ ├── fonts
│ ├── img
│ ├── js
│ ├── styles
│ ├── views
│ └── .htaccess
├── gulpfile.babel.js
├── webpack.config.js
├── package.json
├── .babelrc.js
├── .bemrc.js
├── .eslintrc.json
├── .stylelintrc
├── .stylelintignore
└── .gitignore
`` ``

* Folder root:
    * `` `.babelrc.js``` - Babel settings
    * `` `.bemrc.js```` - BEM settings
    * `` .eslintrc.json``` - ESLint settings
    * `` `.gitignore``` - prohibition on tracking files by Git
    * `` `.stylelintrc``` - Stylelint settings
    * `` `.stylelintignore``` - ban on tracking files by Stylelint
    * `` `gulpfile.babel.js``` - Gulp settings
    * `` `webpack.config.js``` - Webpack settings
    * `` `package.json``` - list of dependencies
* The folder `` src``` - is used during development:
    * BEM blocks: `` `src / blocks```
    * fonts: `` `` src / fonts```
    * Images: `` `src / img``
    * JS files: `` `` src / js```
    * site pages: `` `` src / views / pages```
    * SCSS files: `` `src / styles```
    * HTML files: `` `` src / views```
    * Apache web server configuration file with settings [gzip] (https://habr.com/en/post/221849/) (lossless compression): `` `src / .htaccess```
* The `` dist``` folder is the folder from which the local server for development is launched (when `` yarn run dev``` is launched)
* Folder `` gulp-tasks``` - folder with gulp tasks

## Teams
* `` `yarn run lint: styles``` - check SCSS files. For VSCode, you must install the [plugin] (https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint). For WebStorm
or PHPStorm, you must enable Stylelint in `` Languages ​​& Frameworks - Style Sheets - Stylelint '' (errors will be fixed automatically when saving the file)
* `` `yarn run lint: styles --fix``` - fix errors in SCSS files
* `` `yarn run lint: scripts``` - check JS files
* `` `yarn run lint: scripts --fix``` - fix errors in JS files
* `` `yarn run dev``` - start the server for project development
* `` `yarn run build``` - build a project with optimization without starting the server
* `` `` yarn run build: views``` - collect HTML files
* `` `yarn run build: styles``` - compile SCSS files
* `` `yarn run build: s