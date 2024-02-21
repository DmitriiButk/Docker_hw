### Ecercise 1
```shell
cd docker_hw_one
```
```shell
docker build -t nginx_hw .
```
```shell
docker run -d -p 8000:80 nginx_hw 
```

### Exercise 2
```shell
cd docker_hw_two\3.2-crud\stocks_products
```
```shell
docker build . -t docker_dj_hw
```
```shell
docker run -d -p 8080:8000 docker_dj_hw
```
*Open in browser http://localhost:8080/api/v1/*

*Everything should work. :)*

#

# Домашнее задание к лекции «Docker»

## Задание 1

По аналогии с практикой из лекции создайте свой docker image с http сервером nginx. Замените страницу приветсвия Nginx на своё (измените текст приветствия на той же странице).

<details>
<summary>Подсказки:</summary>
В официальном образе nginx стандартный путь к статичным файлам `/usr/share/nginx/html`.  
</details>

На проверку присылается GitHub-репозиторий с Dockerfile и статичными файлами для него.

> Для пользовательского html можно использовать пример в [каталоге](html/) с ДЗ.

## Задание 2

Создайте контейнер для REST API сервера любого вашего проекта из курса по Django (например, [CRUD: Склады и запасы](https://github.com/netology-code/dj-homeworks/tree/drf/3.2-crud/stocks_products)).

> **ВАЖНО**: поменяйте БД с postgresql на sqlite3. Чтобы ваш контейнер мог работать без зависимости от postgres (с этим мы разберемся на следующем занятии).

Проверьте конфигурацию Django на использование переменных окружения (environment).

- Приложите в репозиторий Dockerfile и файлы приложения.
- В README.md описать типовые команды для запуска контейнера c backend-сервером.

> Для проверки работоспособности вашего контейнера отправляйте запросы с помощью `VS Code REST Client` или `Postman`.
