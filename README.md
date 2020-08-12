# Тестовое задание на позицию стажера-бекендера в юнит "Работа"

## Микросервис для работы с балансом пользователей.

**Проблема:**

В нашей компании есть много различных микросервисов. Многие из них так или иначе хотят взаимодействовать с балансом пользователя. На архитектурном комитете приняли решение централизовать работу с балансом пользователя в отдельный сервис. 

**Задача:**

Необходимо реализовать микросервис для работы с балансом пользователей (зачисление средств, списание средств, перевод средств от пользователя к пользователю, а также метод получения баланса пользователя). Сервис должен предоставлять HTTP API и принимать/отдавать запросы/ответы в формате JSON. 

**Сценарии использования:**

Далее описаны несколько упрощенных кейсов приближенных к реальности.
1. Сервис биллинга с помощью внешних мерчантов (аля через visa/mastercard) обработал зачисление денег на наш счет. Теперь биллингу нужно добавить эти деньги на баланс пользователя. 
2. Пользователь хочет купить у нас какую-то услугу. Для этого у нас есть специальный сервис управления услугами, который перед применением услуги проверяет баланс и потом списывает необходимую сумму. 
3. В ближайшем будущем планируется дать пользователям возможность перечислять деньги друг-другу внутри нашей платформы. Мы решили заранее предусмотреть такую возможность и заложить ее в архитектуру нашего сервиса. 

**Требования к коду:**

1. Язык разработки: Go/Python/PHP/Java/JavaScript/C#(.net Core)
2. Фреймворки и библиотеки можно использовать любые. 
3. Реляционная СУБД: MySQL или PostgreSQL
4. Весь код должен быть выложен на Github
5. Если есть потребность, можно подключить кеши(Redis) и/или очереди(RabbitMQ, Kafka)
6. При возникновении вопросов по ТЗ оставляем принятие решения за кандидатом (в таком случае Readme файле к проекту должен быть указан список вопросов с которыми кандидат столкнулся и каким образом он их решил)

**Будет плюсом:**

1. Использование docker и docker-compose для поднятия и развертывания dev-среды.
2. Методы АПИ возвращают человеко-читабельные описания ошибок и соответвующие статус коды при их возникновении.
3. Все реализовано на GO, все-же мы собеседуем на GO разработчика. HINT: Хоть мы принимаем решения на любом языке, нашим основным языком в работе является Go. Поэтому на собеседовании так или иначе будут вопросы по Go. Кто прочитал, тот молодец :)
4. Написаны unit/интеграционные тесты.

**Минимум того, что должно быть реализовано:**

