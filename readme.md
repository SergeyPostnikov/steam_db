# Steam db
Курсовая работа по базам данных

## Требования к курсовому проекту
Составить общее текстовое описание БД и решаемых ею задач;
минимальное количество таблиц - 10;
скрипты создания структуры БД (с первичными ключами, индексами, внешними ключами);
создать ERDiagram для БД;
скрипты характерных выборок (включающие группировки, JOIN'ы, вложенные таблицы);
представления (минимум 2);
хранимые процедуры / триггеры;
Примеры: описать модель хранения данных популярного веб-сайта: кинопоиск, booking.com, wikipedia, интернет-магазин, geekbrains, госуслуги...

Думайте об этом задании, как о том, чем Вы похвастаетесь на своем следующем собеседовании.

## Описание проекта
Суть STEAM - интернет-магазин игр с добавлением элементов социальной сети.


Для реализации функционала социальной сети были спроектированы следующие таблицы:

### users - Пользователи
 - id
 - nickname
 - email
 - Имя
 - Фамилия

### verification - Верификация
 - id
 - хэш пароля

### friends - Друзья
 - идентификатор пользователя
 - идентификатор друга пользователя

### communities - Сообщества
 - идентификатор сообщества
 - название
 - описание сообщества

### members - Участники сообществ
 - идентификатор сообщества
 - идентификатор пользователя

Для реализации функционала интернет-магазина были спроектированы следующие таблицы:

### game - Список игр
 - название
 - id жанра
 - описание
 - картинка
 - статус?

### genre - Список жанров игр
 - id жанра
 - название жанра

### played_games - игры пользователей
 - id пользователя
 - id игры

## Пользовательский функционал магазина/соцсети:
- **Действия с другими пользователями:**
  - Добавлять в друзья друг на друга
  - Переписываться друг с другом

- **Действия с играми:**
  - Получать рекоммендации на основе жанров из Wishlist и Played games
  - Добавлять игры в список «Wishlist»
  - Отправлять игры в список «Played games»
  - Покупать игры

- **Выражать свое мнение:**
  - Комментировать игру
  - Лайкать/дизлайкать отзывы других пользователей
