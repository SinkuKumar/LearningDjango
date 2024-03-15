# Learning Django - Development Steps

## Pre-Requisites

1. Install [Python](https://www.python.org/downloads/)
2. Install [VS Code](https://code.visualstudio.com/)
3. Install [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) for VS Code
4. Clone the [LearningDjango repo](https://github.com/sinkukumar/learningdjango)
5. Create a venv in the repo directory: `python3 -m venv env`
6. Activate the venv macos: `source env/bin/activate`,  windows: `env\Scripts\activate`
7. Install Django and dotenv: `pip install django python-dotenv`
8. Create a new Django project: `django-admin startproject LearningDjango .`
9. Run the server `python manage.py runserver`
10. Close the server `Ctrl+C`
11. Migrate the database `python manage.py migrate`
12. Create a superuser `python manage.py createsuperuser`
13. Run the server again `python manage.py runserver`
14. Browse to `http://127.0.0.1:8000/admin/` in your browser.
15. Create a directory for static files: `mkdir static`
16. Add `STATIC_URL = '/static/'` to `settings.py`
17. Add `STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]` to `settings.py`
18. Create a directory for templates: `mkdir templates`
19. Add `TEMPLATES['DIRS'] = [os.path.join(BASE_DIR, 'templates')]` to `settings.py`
20. Create a directory for media: `mkdir media`
21. Add `MEDIA_URL = '/media/'` to `settings.py`
22. Add `MEDIA_ROOT = os.path.join(BASE_DIR, 'media')` to `settings.py`
23. Change the timezone to `Asia/Kolkata'` in `settings.py`
24. Create `.env` to contain the secret key and other sensitive credentials
25. Add `SECRET_KEY = os.environ['SECRET_KEY']` to `settings.py`

### First Commit: Create project

## Development Steps

### Profile App
1. Create a new app: `python manage.py startapp profile`
2. Add the app to `INSTALLED_APPS` in `settings.py`
3. Create a model in `models.py`
4. Create a view in `views.py`
5. Create a template in `profile/templates/profile/profile.html`