# PsychoTest & Booking Service

**Концепция:** Веб-сервис для психологического самотестирования и последующей записи к специалистам. Сервис позволяет пользователям проходить стандартизированные опросники, получать интерпретацию результатов и бронировать время консультации у психологов/психотерапевтов напрямую из личного кабинета.

## 🛠 Технологический стек
- **Backend:** Python 3.11, Django 4.2
- **Database:** PostgreSQL 15
- **Frontend:** Django Templates, Bootstrap 5
- **DevOps:** Docker, Docker Compose, GitHub Actions (CI)

## 🚀 Развертывание (Deployment)

### Локальный запуск через Docker
1. Клонируйте репозиторий:
   `git clone https://github.com/your-username/psycho-test-booking.git`
2. Создайте файл окружения:
   `cp .env.example .env` (заполните SECRET_KEY и данные БД)
3. Запустите контейнеры:
   `docker-compose up --build`
4. Примените миграции:
   `docker-compose exec web python manage.py migrate`
5. Создайте суперпользователя:
   `docker-compose exec web python manage.py createsuperuser`
6. Приложение доступно по адресу: `http://localhost:8000`

## 📁 Структура проекта
- `apps/testing/` — логика психологических опросников (вопросы, шкалы, интерпретация).
- `apps/booking/` — управление расписанием специалистов и слотами записи.
- `apps/users/` — роли (Пациент / Специалист), профили.
- `config/` — корневые настройки Django.

## 🤝 Как внести вклад
Пожалуйста, ознакомьтесь с шаблонами Issue в папке `.github/ISSUE_TEMPLATE/` перед созданием PR. Все изменения проходят через Pull Request с обязательным ревью.

## 📄 Лицензия
MIT License.
