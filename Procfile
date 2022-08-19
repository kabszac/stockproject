release: python manage.py migrate
web: daphne stockproject.asgi:application --port $PORT --bind 0.0.0.0 -v2 
celeryworker2: celery -A stockproject.celery worker & celery -A stockproject beat -l INFO & wait -n