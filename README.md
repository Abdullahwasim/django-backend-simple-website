python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver


#ADD Procfile
web: gunicorn backend.wsgi --log-file - 
#or works good with external database
web: python manage.py migrate && gunicorn project_name.wsgi


#ADD runtime.txt
python 3.8.10


#ADD settings.py
 'whitenoise.middleware.WhiteNoiseMiddleware',
