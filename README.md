# REST API сервис для отзывов пользователей на фильмы, книги и музыку

## :books:Описание:
  Проект YaMDb собирает отзывы пользователей на произведения. Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку. Произведения делятся на категории, такие как «Книги», «Фильмы», «Музыка».  Добавлять произведения, категории и жанры может только администратор. Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы и ставят произведению оценку в диапазоне от одного до десяти (целое число); из пользовательских оценок формируется усреднённая оценка произведения — рейтинг (целое число). На одно произведение пользователь может оставить только один отзыв. Пользователи могут оставлять комментарии к отзывам. Добавлять отзывы, комментарии и ставить оценки могут только аутентифицированные пользователи.

## :satellite: Технологии: 

  - Python
  - Django REST Framework
  - API REST
  - Postman
  - Simple-JWT
  - Docker
  - Nginx

## :hammer_and_wrench: Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:
```sh
git clone https://github.com/pa1nf0rce/infra_sp2.git
cd infra_sp2
```
### Перейдите в директорию infra_sp2\infra и создайте файл .env:
#### Шаблон наполнения файла:
```sh
DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
DB_NAME=postgres # имя базы данных
POSTGRES_USER=username # логин для подключения к базе данных
POSTGRES_PASSWORD=password # пароль для подключения к БД (установите свой)
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД 
```

## Для запуска приложения в контейнерах перейдите в директорию "infra_sp2\infra" и выполните команды:

```sh
docker-compose up -d --build 
```

Для создания суперюзера выполинте команду:
```sh
docker-compose exec web python manage.py createsuperuser
```

## :page_with_curl: Проектная документация:
Документация для API доступна по адресу
```
http://localhost/redoc/
```

## :office_worker: Об авторах: 
[Авраменко Роман](https://github.com/pa1nf0rce),
[Ермолов Виталий](https://github.com/Flomixon),
[Плотников Алексей](https://github.com/Aleksei93)
