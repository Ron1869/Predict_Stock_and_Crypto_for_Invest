





![photo_2024-11-30_21-55-08](https://github.com/user-attachments/assets/3d458fd1-1c1a-4a17-8c61-ca93a9d4bf0f)












![photo_2024-11-30_21-54-58](https://github.com/user-attachments/assets/7274ac77-9f98-41c1-909f-90bac8926f28)











Структура Massyanya-2.0:






_assets/: Хранит статические ресурсы, используемые ботом.


predict_stock_crypto/: Основная директория с исходным кодом бота.


.gitignore: Определяет файлы и директории, игнорируемые Git.


Dockerfile: Инструкции для сборки Docker-образа приложения.


docker-compose.yml: Конфигурация для управления многокомпонентными Docker-приложениями.


pyproject.toml: Метаданные проекта и его зависимости.


requirements.txt: Список зависимостей Python для работы приложения.


setup.cfg: Конфигурация инструментов, используемых в проекте.








Ключевые функции бота:


Прогнозирование цен: Предоставляет прогнозы цен на выбранные криптовалюты на ближайшие две недели.


Уровни поддержки: Отображает уровни "Low" и "High" поддержки с графиками за последний год.


Управление избранным: Позволяет добавлять или удалять криптовалюты из списка избранного и предоставляет удобное навигационное меню.








Используемые технологии:


investpy: Получение исторических данных цен по криптовалютам.


pandas: Обработка и анализ данных.


beautifulsoup4: Парсинг прогнозных цен на криптовалюты.


python-telegram-bot: Взаимодействие с Telegram API.


matplotlib: Построение графиков цен на криптовалюты.


sqlite3: Хранение списка криптовалют и избранных позиций пользователя.














▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀▀▄ ▀▄ ▀▄ ▀▄▀
                                                                             ▹Loading. ████[][][][][][][] 25%

План сборки проекта Massyanya-2.0 



1. Анализ и подготовка
1.1 Цели проекта:
Создать веб-интерфейс для управления торговым ботом.
Добавить чат для отображения предсказаний.
Интегрировать настройки торговли в веб-интерфейс.
Включить кнопки управления:
ТОРГОВАТЬ – включает авто-торговлю.
ПРОГНОЗ – запускает предсказания.
Реализовать выбор таймфрейма для предсказаний.
Интегрировать Telegram-бот для удаленного управления.
Объединить 4 стратегии для предсказаний.
Добавить умное хранилище данных для парсеров (MinIO).



1.2 Задачи:
Определить архитектуру проекта.

Подготовить необходимые библиотеки и инструменты:

Flask/Django для веб-интерфейса.
Telegram API для бота.
Machine Learning библиотеки (scikit-learn, TensorFlow или PyTorch) для предсказаний.
MinIO для хранения данных.
Investpy и другие парсеры для сбора данных.



1.3 Структура проекта:

Frontend: HTML/CSS, JavaScript (React или Vue.js) для интерфейса.
Backend: Python (Flask/Django).
Базы данных: PostgreSQL/MySQL для хранения данных.
Облачное хранилище: MinIO.
Telegram Bot: Телеграм-бот для удаленного управления.

3. Интеграция функций
   
2.1 Создание веб-интерфейса

Установить Flask/Django.

Реализовать главную страницу с:
Настройками торговли (таймфрейм, параметры бота).
Чатом для отображения предсказаний.
Кнопками ТОРГОВАТЬ и ПРОГНОЗ.
Добавить раздел для вывода логов и истории торговли.


2.2 Интеграция Telegram-бота
Настроить API Telegram для взаимодействия.
Добавить команды:
/start: запуск бота.
/trade: включение авто-торговли.
/forecast: запуск предсказаний.
/status: запрос текущего состояния.


2.3 Настройка предсказаний
Объединить данные из 4 стратегий:
Massyanya: торговые индикаторы и LSTM-модель.
Investpy: парсинг финансовых данных.
News_parsing_movies: анализ новостей.
MinIO: хранилище исторических данных.
Разработать алгоритмы для обработки данных:
Интеграция LSTM (нейросети) с теханализом.
Выбор таймфреймов.
Добавить кнопку ПРОГНОЗ, чтобы выводить результаты в чат и Telegram.


2.4 Добавление кнопки "ТОРГОВАТЬ"
Реализовать функцию запуска авто-торговли.
Настроить управление торговлей через интерфейс и Telegram.


2.5 Таймфреймы для предсказаний
Добавить выбор таймфреймов:
15 минут, 1 час, 4 часа, 1 день, 3 дня, 1 неделя, 2 недели.
Обновить интерфейс для выбора и визуализации предсказаний.


5. Интеграция парсеров


3.1 Investpy
Настроить регулярный сбор данных с сайта Investing.com.
Интегрировать в веб-интерфейс для отображения.


3.2 News_parsing_movies
Подключить парсер новостей для анализа влияния новостей на рынок.
Интегрировать функцию анализа в предсказания.


3.3 MinIO
Настроить MinIO как хранилище данных для всех парсеров.
Реализовать доступ к данным из веб-интерфейса.


7. Разработка логики торговли
Интегрировать API Binance для реальных торговых операций.
Настроить расчет рисков и управление капиталом.
Добавить модуль анализа и отправки уведомлений о результатах торговли.


9. Тестирование
Протестировать каждую функцию:
Интерфейс и кнопки.
Telegram-бот.
Таймфреймы и предсказания.
Интеграция данных парсеров.
Провести нагрузочное тестирование.


11. Развертывание
Развернуть веб-интерфейс на сервере (Heroku, AWS, или DigitalOcean).
Настроить домен и SSL-сертификаты.
Установить MinIO на сервере.




