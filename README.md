🌿 AgroZero — NiFi + FastAPI + PostgreSQL Integration
🚀 Готовая инфраструктура для агростартапа: автоматизированная обработка данных, рекомендации по переработке и централизованное хранение.

📦 Состав
Компонент	Назначение
Apache NiFi	Автоматизация потоков данных: от сенсоров, API, CSV, изображений
FastAPI	Python-сервис для обработки запросов и выдачи рекомендаций
PostgreSQL	Хранилище данных: отходы, рекомендации, журнал действий

🛠 Установка и запуск
1. Требования:
Docker

Docker Compose

2. Запуск:
bash
Copy
Edit
git clone https://your-repo-url
cd nifi_fastapi_postgres_docker
docker-compose up --build
🌐 Доступы по умолчанию
Сервис	URL
NiFi UI	http://localhost:8080
FastAPI	http://localhost:8000/docs
PostgreSQL	localhost:5432 (user: agro / pass: agro123 / db: agrodata)

🧪 Пример запроса к FastAPI
POST /recommend

json
Copy
Edit
{
  "type": "apple_pulp",
  "amount": 150
}
Ответ:

json
Copy
Edit
{
  "recommendation": "Juice Production",
  "confidence": 0.87,
  "input": {
    "type": "apple_pulp",
    "amount": 150
  }
}
🔄 Интеграция NiFi → FastAPI
В NiFi используйте процессор InvokeHTTP

Метод: POST

URL: http://fastapi:8000/recommend

Content-Type: application/json

В теле передавайте JSON с типом и объёмом отходов

📚 Возможности расширения
💡 Подключение сенсоров через MQTT (NiFi ListenMQTT)

🧠 Использование ML-моделей для рекомендаций

♻️ Логика переработки отходов в соки, пасту, компост

🔗 Подключение к облачным платформам и IoT-устройствам

🧑‍💻 Авторы
Проект AgroZero — цифровая платформа для устойчивого сельского хозяйства и нулевых отходов.
