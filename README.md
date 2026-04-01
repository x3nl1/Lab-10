# Лабораторная работа №10

## Студент

ФИО: Агапов Степан Александрович
Группа: 221331

## Вариант

9

---

## Выполненные задания

### Средней сложности

* Задание 1 — REST API на Go (Gin)
* Задание 3 — валидация входных данных
* Задание 5 — JSON обмен между Go и Python

### Повышенной сложности

* Задание 3 — JWT аутентификация
* Задание 5 — Docker Compose

---

## Структура проекта

* m_task_api/ — Go API
* python_client/ — Python клиент и тесты
* docker-compose.yml — контейнеризация
* PROMPT_LOG.md — лог работы с AI

---

## Запуск

### Локально

cd m_task_api
go mod tidy
go run .

cd python_client
pip install -r requirements.txt
pytest

---

### Docker

docker compose up --build

---

## Тестирование

go test ./...
pytest

---

## Особенности реализации

* Используется Bearer JWT авторизация
* Реализована валидация через Gin binding
* Добавлены позитивные и негативные тесты
* Учтён race condition (retry в тестах)
* Docker использует внутреннюю сеть (go_service)
