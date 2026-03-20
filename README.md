# Spring Boot CRUD Application

Простое CRUD-приложение на Spring Boot с использованием:
- Spring Boot 4
- Spring Data JPA (Hibernate)
- MySQL
- Thymeleaf
- Maven

## 📌 Описание

Приложение реализует базовые CRUD-операции для сущности `User`:
- создание пользователя
- просмотр списка пользователей
- обновление данных
- удаление пользователя

## ⚙️ Технологии

- Java 24
- Spring Boot
- Spring MVC
- Spring Data JPA
- Hibernate
- MySQL
- Thymeleaf
- Lombok

## 🚀 Запуск проекта

### 1. Клонировать репозиторий

```bash
git clone https://github.com/Riss2121/3_1_2_Zadacha.git
2. Настроить базу данных

Создай БД в MySQL:

CREATE DATABASE jdbc_hibernate;
3. Настроить application.properties
spring.datasource.url=jdbc:mysql://127.0.0.1:3306/jdbc_hibernate?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=root
4. Запуск

Через IntelliJ IDEA или:

mvn spring-boot:run

Приложение будет доступно:

http://localhost:8080
📁 Структура проекта
controller/   → контроллеры (MVC)
service/      → бизнес-логика
dao/          → работа с БД
model/        → сущности (Entity)
📌 Основные эндпоинты
Метод	URL	Описание
GET	/users	список пользователей
GET	/users/new	форма создания
POST	/users	сохранить пользователя
GET	/users/{id}	информация о пользователе
GET	/users/{id}/edit	форма редактирования
PATCH	/users/{id}	обновление
DELETE	/users/{id}	удаление
📝 Особенности

Используется EntityManager вместо Spring Data Repository

Поддержка HTTP методов PATCH и DELETE через hidden field

Hibernate автоматически создаёт таблицы (ddl-auto=update)

👤 Автор

Roman


Если хочешь — могу сделать версию **под следующую задачу с Security (roles, login, admin/
