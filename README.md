# Bookstore

Build in detach mode
  - docker-compose up -d --build

Reload
  - docker-compose up -d

Check for logs
  - docker-compose logs

Migration
  - docker-compose exec web python manage.py makemigrations
  - docker-compose exec web python manage.py migrate
  - docker-compose exec web python manage.py createsuperuser

Stop running container
  - docker-compose down

Tests
  - docker-compose exec web python manage.py test

Combine staticfiles
  - docker-compose exec web python manage.py collectstatic


Check if deployment ready
  - docker-compose exec web python manage.py check --deploy

Run deployment
  - docker-compose -f docker-compose-prod.yml up -d

Generate new secret key
  - docker-compose exec web python -c "import secrets; print(secrets.token_urlsafe(38))"
