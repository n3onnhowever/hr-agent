# HR Avatar  

![version](https://img.shields.io/badge/version-0.1.0-blue)
![built-with](https://img.shields.io/badge/built%20with-Python%20%2B%20FastAPI-%230366d6)  

## ✨ Возможности  

- 🤖 AI-бот для проведения собеседований  
- 📑 Генерация отчётов по итогам интервью  
- 🗂 Сервис для анализа ответов кандидата  
- 🔗 API для интеграции с внешними системами  
- ⚡ Поддержка работы в **Docker** и **docker-compose**
- 🛠 Гибкая архитектура (модули: API, клиенты LLM, сервисы

---

## 🚀 Быстрый старт  

```bash
# 1. Клонировать репозиторий
git clone https://github.com/n3onnhowever/hr-avatar.git

# 2. Создать и активировать виртуальное окружение
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

# 3. Установить зависимости
pip install -r requirements.txt

# 4. Запустить приложение
python main.py
```

Или через Docker:  

```bash
# Собрать образ
docker build -t hr-avatar .

# Запустить контейнер
docker run -p 8000:8000 hr-avatar
```

А с помощью docker-compose:  

```bash
docker-compose up --build
```

После запуска API будет доступно по адресу:  
👉 [http://localhost:8000](http://localhost:8000)  

---

## 📂 Структура проекта  

```
AI_HRbot-hr-avatar-v2/
│
├── app/                     # Основной код приложения
│   ├── api/                 # API: роуты и схемы
│   │   ├── routes.py
│   │   └── schemas.py
│   ├── clients/             # Подключение LLM и клиентов
│   │   └── llm.py
│   ├── core/                # Основные настройки и промпты
│   │   └── prompts.py
│   └── services/            # Сервисы (сжатие, интервью, отчёты)
│       ├── compress.py
│       ├── interview.py
│       └── report.py
│
├── Dockerfile               # Конфигурация Docker-образа
├── docker-compose.yml       # Композиция сервисов Docker
├── main.py                  # Основной запуск приложения
├── main_stateless.py        # Альтернативный запуск без состояния
├── requirements.txt         # Зависимости проекта
└── README.md                # Документация
```
