# Stellar Burgers API: автоматизация тестирования на Java
Автоматизированные тесты API учебного сервиса Stellar Burgers.

## Документация
[Документация](https://code.s3.yandex.net/qa-automation-engineer/java/cheatsheets/paid-track/diplom/api-documentation.pdf) на API учебного сервиса Stellar Burgers.
[Ссылка](https://stellarburgers.nomoreparties.site/) на учебное приложение Stellar Burgers.

## Описание

Версия Java 11.

В проекте используется библиотека:

- JUnit 4;
- RestAssured;
- Allure;

## Инструкция для запуска тестов

Для запуска автотеста необходимо:

1. Склонируйте репозиторий на свой компьютер с помощью команды:

 ```sh
 git clone git@github.com:DianaRazyapova/stellar-burgers-api-automation.git
```

2. Запустите тесты с помощью команды:

```sh
mvn clean test
```

3. Для создания отчета в Allure ввести команду:

```sh
mvn allure:report
```

## Структура проекта

```bash
pom.xml
README.md
.gitignore
src
|-- main
|   |-- java
|   |   |-- api
|   |   |   |-- stellarburgers
|   |   |   |   |-- Ingredient.java
|   |   |   |   |-- Ingredients.java
|   |   |   |   |-- Order.java
|   |   |   |   |-- User.java
|   |   |--clientStellarBurgers
|   |   |   |   |-- OrderClient.java
|   |   |   |   |-- UserClient.java
|--test
|   |-- java
|   |   |-- order
|   |   |   |   |-- CreateOrderTest.java
|   |   |   |   |-- OrderGetTests.java
|   |   |-- user
|   |   |   |   |-- ChangeUserTest.java
|   |   |   |   |-- LoginUserTests.java
|   |   |   |   |-- UserCreatingTests.java
```
## Выполненые задачи

Проверено, что они корректно работают и выдают нужные ошибки:

1. Создание пользователя:
- создать уникального пользователя;
- создать пользователя, который уже зарегистрирован;
- создать пользователя и не заполнить одно из обязательных полей.

2. Логин пользователя:
- логин под существующим пользователем;
- логин с неверным логином и паролем.

3. Изменение данных пользователя:
- с авторизацией;
- без авторизации;
Для обеих ситуаций нужно проверить, что любое поле можно изменить. Для неавторизованного пользователя — ещё и то, что система вернёт ошибку.

4. Создание заказа:
- с авторизацией;
- без авторизации;
- с ингредиентами;
- без ингредиентов;
с неверным хешем ингредиентов.

5. Получение заказов конкретного пользователя:
- авторизованный пользователь;
- неавторизованный пользователь.

## Отчёт Allure
> Сгенерированные отчеты
<table>
     <tr>
        <td>
         <img width="1625" alt="Снимок экрана 2023-07-12 в 16 20 25" src="https://github.com/DianaRazyapova/stellar-burgers-api-automation/assets/115238502/dc009138-2c44-404f-bd33-335473244d08">
        </td>
     </tr>
     <tr>
        <td>
        <img width="1625" alt="Снимок экрана 2023-07-12 в 16 21 00" src="https://github.com/DianaRazyapova/stellar-burgers-api-automation/assets/115238502/0d318156-79e3-4d42-a439-a04440858f50">
       </td>
    </tr>
</table>
