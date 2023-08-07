**Задание**
Разработать приложение "Кредитный конвейер" с применением технологий и инструментов:
Java, SpringBoot, PostgreSQL, JPA, Swagger, Kafka, JUnit, Mockito, Lombok

**Соглашения**
Во всех микросервисах необходимо использовать данный стек технологий:
**Общее**:
- Стек: Java 11+  (можно Kotlin 1.6+) + SpringBoot;
- Тестирование: Junit4/5+Mockito. Целевой процент покрытия - 90%;
- СУБД: Postgres + liquibase (spring.jpa.hibernate.ddl-auto: validate);
- API & DTO генерировать через open-api, документация API через springdoc;
- Наименования методов\полей: Code-style от google;
- Маппинг сущностей: mapstruct;
- Все REST-endpoints должны возвращать ResponseEntity<DTO>;
- Request/response логгирование от каждого МСа;
- Синхронное взаимодействие: Feign + FeignErrorDecoder (для проброса ошибок между МСами);
- Асинхронное взаимодействие: Kafka;

**Git:**
- Добавить проект в github, отвести от  ветки main ветку develop. 
- Рекомендуемая структура папок: <папка_с_полным_именем_проекта>/<папка_с_МС>
- Все дальнейшие изменения производить из веток, отведенных от develop через pull request в develop.
- Имена этих веток формируются следующим образом: <feature/bugfix>/<MS-name>/<1-3_слова_характирезующие изменения>