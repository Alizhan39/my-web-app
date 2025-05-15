# my-web-app
A web app with CI/CD deployment to Heroku
agrozero/
├── app/                       # Основная логика приложения
│   ├── main.py                # Точка входа (FastAPI)
│   ├── iot/                   # Работа с сенсорами
│   │   └── sensors.py
│   ├── ml/                    # Модели машинного обучения
│   │   ├── recommender.py     # Рекомендации по переработке
│   │   └── forecast.py        # Прогноз урожая и спроса
│   ├── vision/                # Компьютерное зрение
│   │   └── detector.py
│   └── utils/                 # Вспомогательные функции
│       └── database.py
├── notebooks/                 # Jupyter-анализы и прототипы
├── data/                      # CSV/изображения/телеметрия
├── models/                    # Предобученные ML модели
├── .env                       # Переменные окружения
├── Dockerfile                 # Контейнеризация
├── requirements.txt           # Зависимости проекта
└── README.md
