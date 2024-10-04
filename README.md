# Python web

* On any push GH builds site at https://nadya-karandasheva.github.io/python-web/ using MkDocs

## Алгоритм действий:
1. Создать репозиторий на GitHub
2. Клонировать его локально
3. Создать venv
4. Установить mkdocs на venv
5. Прописать команды mkdocs new и mkdocs serve

Сервер будет работать по адресу 127.0.0.1:8000

## Что нужно сделать в репозитории:
1. Включить страницы GitHub
2. Указать docs/index.md в качестве источника
3. Создать в папке workflows файл actions.yml для конфигурации действий
4. Добавить в actions.yml шаги:
    - Извлечение
    - Настройка Python
    - Настройка MkDocs
    - Сборка
    - Развертывание ( с параметром *mkdocs gh-deploy --force*)

#### Если не работает:
 - создать secrets среды и репозитория
 - добавить  для actions.yml следующие разрешения: permissions: contents: write pages: write
