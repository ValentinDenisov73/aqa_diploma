## Отчет по итогам тестирования
### Краткое описание
В ходе работы над проектом было проведено тестирование веб-сервиса "Путешествие дня", которое представляет собой комплексный сервис, взаимодействующий с СУБД и API Банка.

На первом этапе было проведено ручное тестирование.

На втором этапе были написаны автотесты, и было проведено автоматизированное тестирование сервиса с использованием инструментов, указанных в [Плане автоматизации тестирования](https://github.com/ValentinDenisov73/aqa_diploma/blob/main/documentation/Plan.md).

Тесты включают в себя как позитивные, так и негативные сценарии покупки путешествия. Были проведены тесты UI, тесты БД.

Тестирование было проведено для БД PostgreSQL.
### Количество тест-кейсов: 52, из них
- успешных - 12
- неуспешных - 40

![Скриншот](https://github.com/ValentinDenisov73/aqa_diploma/blob/main/documentation/2023-03-11.png)

### Количество оформленных баг-репортов: 10

### Общие рекомендации
- Создать документацию к приложению
- В поле "Владелец" установить ограничение символов и убрать возможность отправки формы с одним именем/фамилией
- В поле "Владелец" убрать возможность введения цифр
- В поле "Месяц" убрать возможность введения значения "00"
- Исправить надписи под полями при вводе невалидных данных на более логичные(см. тесты)
- Исправить предупреждение о неверном вводе данных в поле CVC
- Добавить уникальные css селекторы, что положительно повлияет на скорость разработки автотестов в будущем 