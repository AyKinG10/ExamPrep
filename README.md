# Angular Full Stack

Angular Full Stack — это проект специально для Дисциплины stack MEAN(Mongo, Express, Angular, Node).

Этот проект использует [MEAN stack](https://ru.wikipedia.org/wiki/MEAN_(программный_комплект)):
* [**M**ongoose.js](http://www.mongoosejs.com) ([MongoDB](https://www.mongodb.com)): база данных
* [**E**xpress.js](http://expressjs.com): бэкенд-фреймворк
* [**A**ngular 2+](https://angular.io): фронтенд-фреймворк
* [**N**ode.js](https://nodejs.org): среда выполнения

Другие инструменты и технологии, используемые в проекте:
* [Angular CLI](https://cli.angular.io): генератор фронтенда
* [Bootstrap](http://www.getbootstrap.com): стили и макет
* [Font Awesome](http://fontawesome.com): иконки
* [JSON Web Token](https://jwt.io): аутентификация пользователей
* [Angular 2 JWT](https://github.com/auth0/angular2-jwt): помощник JWT для Angular 2+
* [Bcrypt.js](https://github.com/dcodeIO/bcrypt.js): шифрование паролей

## Предварительные условия
1. Установите [Node.js] и [MongoDB]
2. Установите Angular CLI: `npm i -g @angular/cli`
3. Из корневой папки проекта установите все зависимости: `npm i`

## Запуск
### Режим разработки с отслеживанием файлов
`npm run dev`: выполняет запуск MongoDB, сборку Angular, компиляцию TypeScript и сервер Express.

### Режим продакшн
`npm run prod`: запускает проект с продакшн-бандлом по адресу [localhost:3000](http://localhost:3000)

### Ручной режим
1. Соберите фронтенд: `npm run builddev` для разработки или `npm run build` для продакшн
2. Соберите бэкенд: `npm run predev`
3. Запустите MongoDB: `mongod`
4. Запустите приложение: `npm start`

### Docker
1. `sudo docker-compose up`
2. Перейдите по адресу [localhost:3000](http://localhost:3000)

### AWS EC2
1. Создайте EC2 Linux машину на AWS
2. Отредактируйте группу безопасности EC2 и добавьте TCP порт `3000` в правила входящих соединений для источника `0.0.0.0/0`
3. Клонируйте этот репозиторий на машину EC2
4. Если вы используете удаленную базу данных MongoDB, отредактируйте файл `.env`
5. Выполните команду `npm ci`
6. Выполните команду `npm run build`
7. Выполните команду `npm start`
8. Приложение теперь запущено и слушает на порту 3000
9. Теперь вы можете посетить публичный IP вашего AWS EC2 с портом, например: `12.34.56.78:3000`
10. Совет: используйте [pm2](https://pm2.keymetrics.io/) для запуска приложения вместо `npm start`, например: `pm2 start dist/server/app.js`
 
## Запуск тестов
Выполните `ng test` для выполнения юнит-тестов фронтенда с использованием [Karma](https://karma-runner.github.io).

Выполните `npm run testbe` для выполнения тестов бэкенда с использованием [Jest](https://jestjs.io/) (требуется предварительный запуск `mongod`).

## Запуск линтеров
Выполните `npm run lint` для выполнения [Angular ESLint](https://github.com/angular-eslint/angular-eslint), [HTML linting](https://github.com/htmlhint/HTMLHint) и [SASS linting](https://github.com/sasstools/sass-lint).



### Автор
* [Ayan Serikkan](https://github.com/AyKing10)
* [Nurbakhyt Bolatov](https://github.com/AyKing10)

### Ваш GitHub репозиторий
* [Ваш профиль на GitHub](https://github.com/AyKing10)
