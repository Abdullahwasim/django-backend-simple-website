web: gunicorn backend.wsgi --log-file - 
#or works good with external database
web: python manage.py migrate && gunicorn project_name.wsgi