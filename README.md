

# Установка:

```bash
npm i
# or
npm i --legacy-peer-deps
```

(i) флаг --legacy-peer-deps позволит продолжить установку при возникновении 
конфликтов зависимостей (версий пакетов).

# Запуск режима разработчика (c запуском сервера)

```bash
npm run dev
```

# Запуск сборки проекта (без запуска сервера, только финальная сборка)

```bash
npm run build
```

# Запуск сборки проекта и выгрузка результата на сервер по FTP. (без запуска локальконо сервера)

Конфигурация FTP находится в файле config/gulp-settings.js

```bash
npm run deploy
```

# Запуск сборки проекта и создание zip архива с именем проекта. (без запуска локальконо сервера)

```bash
npm run zip
```

# Запуск сборки проекта но без создания webp картинок. (без запуска сервера, только финальная сборка)
```bash
npm run devbuild
```


# Запуск создания SVG спрайта. 

Иконки нужно положить в папку src/svgicons, готовый спрайт появится в папке src/img/icons/icons.svg
Изменения в папке src/svgicons не отслеживаются в dev режиме, при необходимости можно запустить повтоврую сборку спрайта
запускать создание спрайта стоит перед началом работ командой:

```bash
npm run sprite
```

//------------------------------------------------------------------------------

Основные файлы для работы с шаблоном:
js/app.js
scss/style.scss

index.html - разводящая страница (содержание)
home.html - главная страница
файлы html/*.htm - подключаемые части


//------------------------------------------------------------------------------

При возникновении ошибок убедитесь что:
1) У вас установлен Node.js последней версии
2) Терминал открыт с правами администратора
3) В названиях папок на всем пути к проекту нет символа # или !
4) Папки и файлы должны быть названы латиницей без пробелов
5) Тег img и его содержимое должны быть записаны в одну строку без переносов
6) В атрибуте src должен быть указан путь к существующей картинке

//------------------------------------------------------------------------------

Прочие проблемы и их решения:
//-----------------------------------
Ошибка "unable to resolve dependency tree"
Решение:
npm i --legacy-peer-deps
//-----------------------------------
Ошибка node-sass.
Решения:
npm rebuild node-sass
и/или
npm install sass gulp-sass --save-dev
//-----------------------------------
Ошибка Pyton
Решени:
npm install --global windows-build-tools
//------------------------------------------------------------------------------