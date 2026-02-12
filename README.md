MAKAAN
======

Simple Django-based real-estate site scaffold (MAKAAN).

Project structure
- `manage.py` - Django management script
- `db.sqlite3` - default SQLite database
- `makaan_project/` - Django project settings and wsgi/asgi
- `properties/` - main app for property listings
- `templates/` - HTML templates
  - `registration/login.html` - login page (Django auth)
- `static/` or `css/`, `img/`, `js/` - site static assets
- `requirements.txt` - Python deps
- `.gitignore` - ignores for git

Quick start (Windows PowerShell)

1. Create and activate virtualenv

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies

```powershell
pip install -r requirements.txt
```

3. Apply migrations and create superuser

```powershell
python manage.py migrate
python manage.py createsuperuser
```

4. Run development server

```powershell
python manage.py runserver
```

Open http://127.0.0.1:8000/ and login at http://127.0.0.1:8000/accounts/login/

Notes
- Templates for Django auth are in `templates/registration/` so `django.contrib.auth.urls` will pick them up.
- If you plan to deploy, replace `db.sqlite3` with a production database and follow Django deployment docs.
