# Курсовой проект по модулю «Автоматизация тестирования» для профессии «Инженер по тестированию»
## Документация
[План тестирования](https://github.com/ValentinDenisov73/aqa_diploma/blob/main/documentation/Plan.md)
## Задача:
Автоматизировать сценарии комплексного сервиса, взаимодействующего с СУБД и API Банка. Приложение представляет собой веб-сервис.
![Скриншот](https://github.com/ValentinDenisov73/aqa_diploma/blob/main/documentation/service.png)
Приложение предлагает купить тур по определённой цене с помощью двух способов:
1. Обычная оплата по дебетовой карте
1. Уникальная технология: выдача кредита по данным банковской карты
## Инструкция подключения БД и запуска SUT
1. Склонировать проект из репозитория командой `git clone`
1. Открыть склонированный проект в Intellij IDEA
1. Для запуска контейнеров с PostgreSQL и Node.js использовать команду `docker-compose up --build`
1. Запуск SUT
* для PostgreSQL ввести в терминале команду
  `java -Dspring.datasource.url=jdbc:postgresql://localhost:5432/app  -jar artifacts/aqa-shop.jar`
## Запуск тестов и генерация отчета Allure
1. Для запуска на PostgreSQL ввести команду
`./gradlew clean test -Ddb.url=jdbc:postgresql://localhost:5432/app`
1. Сгенерировать отчет Allure, выполнив команду `./gradlew allureServe`
* Если отчет не открывается автоматически в браузере, то выполнить команду `./gradlew allureReport` и открыть отчет вручную (файл index.html) по адресу: .\build\reports\allure-report\allureReport
3. После окончания тестов завершить работу приложения, остановить контейнеры командой `docker-compose down`
