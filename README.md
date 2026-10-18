# Nurul Islam – Django one-page portfolio

## Run locally
```
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py runserver
```
Open http://127.0.0.1:8000

## Edit content
Everything (name, links, skills, projects, experience) is in `portfolio/content.py`.
Colors are the 6 variables at the top of `static/css/style.css`.

## Contact form
Without email settings, messages are only printed in the terminal and the page says so.
To send real email set environment variables: `CONTACT_EMAIL`, `EMAIL_HOST`, `EMAIL_PORT`,
`EMAIL_HOST_USER`, `EMAIL_HOST_PASSWORD`.

## Deploy (e.g. Render / Railway / PythonAnywhere)
Set `DJANGO_DEBUG=0`, `DJANGO_SECRET_KEY=<long random>`, `DJANGO_ALLOWED_HOSTS=yourdomain.com`,
`DJANGO_CSRF_ORIGINS=https://yourdomain.com`. Build: `pip install -r requirements.txt && python manage.py collectstatic --noinput`.
Start: `gunicorn config.wsgi`.
