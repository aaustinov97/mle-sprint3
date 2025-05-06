#venv_path: source /home/mle-user/.mle-sprint3-venv/bin/activate
или cd ~ 
а затем .mle-sprint3-venv/bin/activate


Пара шагов — и у вас есть приложение app, которое может обрабатывать: 
запросы к корню — то есть к URL в определённом формате. В нашем случае: http://service-ip:service-port/.
запросы на получение предсказания модели для пользователя user_id вида http://service-ip:service-port/api/churn/{user_id}.

Запуск: uvicorn main:app --reload
uvicorn churn_app:app --reload --port 8081 --host 0.0.0.0 

Тест отдельного файла
python -m app.fast_api_handler 

Документация: http://127.0.0.1:8000/docs


Для теста POST функций можно отправить тестовый POST-запрос через Swagger UI

Репозиторий с файлами для прохождения третьего спринта.
