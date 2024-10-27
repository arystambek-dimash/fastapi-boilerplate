# FastAPI Boilerplate

Шаблон для быстрого начала проектов на основе FastAPI.

## Описание

Этот репозиторий предоставляет базовую структуру для создания веб-приложений с использованием FastAPI. Он помогает ускорить процесс разработки, предоставляя готовую архитектуру и настройки.

## Возможности

- **Чистая архитектура проекта**
- **Использование Poetry для управления зависимостями**
- **Интеграция с базой данных**
- **Автоматическая документация API с помощью Swagger UI**
- **Готовая структура для адаптеров, домена и драйверов**

## Структура
```markdown
.
├── src/
│   ├── adapters/
│   │   ├── database/
│   │   ├── repositories/
│   │   └── __init__.py
│   ├── application/
│   │   └── __init__.py
│   ├── domain/
│   │   ├── entities/
│   │   ├── exceptions/
│   │   ├── interfaces/
│   │   └── __init__.py
│   ├── drivers/
│   │   ├── rest/
│   │   └── __init__.py
│   ├── main/
│   │   └── __init__.py
│   ├── config.py
│   ├── web.py
│   └── __init__.py
├── .gitignore
├── poetry.lock
└── pyproject.toml
```

### Описание каталогов

- `adapters/`: Содержит реализацию интерфейсов для взаимодействия с внешними системами (базы данных, API и т.д.).
  - `database/`: Настройки и подключение к базе данных.
  - `repositories/`: Реализация паттерна Repository для доступа к данным.
- `application/`: Бизнес-логика приложения.
- `domain/`: Содержит сущности, исключения и интерфейсы доменной области.
  - `entities/`: Модели доменных сущностей.
  - `exceptions/`: Определения исключений доменной области.
  - `interfaces/`: Определение интерфейсов для слоев приложения.
- `drivers/`: Слой взаимодействия с внешним миром (HTTP, CLI и т.д.).
  - `rest/`: Реализация REST API с помощью FastAPI.
- `main/`: Точка входа в приложение.
- `config.py`: Файл конфигурации приложения.
- `web.py`: Инициализация веб-приложения FastAPI.

## Установка

### Клонирование репозитория

```bash
git clone <URL вашего репозитория>
cd <имя_проекта>
```

## Установка зависимостей с помощью Poetry
Убедитесь, что у вас установлен Poetry.

```bash
poetry install
```
## Запустите приложение с помощью Uvicorn
```bash
uvicorn src.web:app --reload
```
Приложение будет доступно по адресу http://localhost:8000.

## Документация API
* Swagger UI: http://localhost:8000/docs
* ReDoc: http://localhost:8000/redoc
* Настройка переменных окружения
* Создайте файл .env в корневом каталоге проекта и добавьте необходимые переменные окружения, такие как настройки базы данных и секретные ключи.

Вклад в проект
Будем рады вашим предложениям и улучшениям. Пожалуйста, создавайте issues и pull requests.

## Запуск приложения
Активируйте виртуальное окружение
```bash
poetry shell
```
