## taski-docker
Приложение **Taski** — сервис для управления задачами. Пользователь может:  
- Создавать, редактировать и удалять задачи  
- Просматривать список задач  
- Отмечать задачи как выполненные

### Технологический стек:
- Python 3.12 / Django (бэкенд)
- React (фронтенд)
- PostgreSQL
- Docker / Docker Compose
- Gunicorn
- Nginx (gateway)
- GitHub Actions (CI/CD)
- Certbot (HTTPS)

### Установка и запуск
1. Клонируйте репозиторий:
```bash
git clone git@github.com:Inswty/taski-docker.git
cd taski-docker
```
2. Создайте и заполните .env файл:  
Пример содержимого:
```
DEBUG=True
SECRET_KEY=your-secret-key
ALLOWED_HOSTS=127.0.0.1,localhost
DB_HOST=db
DB_PORT=5432
POSTGRES_DB=taski
POSTGRES_USER=taski_user
POSTGRES_PASSWORD=taski_password
```
3. Запустите проект через Docker Compose:
```
docker-compose up
```
Проект будет доступен по адресу [http://localhost:8000](http://localhost:8000)

**Как запустить в проде:**  
- Настроить переменные окружения в .env, скопировать на сервер в директорию проекта
- Создать SICRETS в GitHub Actions:
```
DOCKER_PASSWORD
DOCKER_USERNAME
HOST
SSH_KEY
SSH_PASSPHRASE
TELEGRAM_TO
TELEGRAM_TOKEN
USER
```
- Выполнить пуш GitHub в ветку main:
```bash
git push origin main
```

## Автор:
Проект разработан 
[Павел Куличенко](https://github.com/Inswty)