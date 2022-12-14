# [Django Admin Soft](https://appseed.us/product/soft-ui-dashboard/django/) 

Modern template for **Django Admin Interface** coded on top of **[Soft UI Dashboard](https://appseed.us/product/soft-ui-dashboard/django/)**, an open-source `Boostrap 5` design from `Creative-Tim`.

> Actively supported by [AppSeed](https://appseed.us/) via `Email` and `Discord`.

<br>

**Links & Resources**

- [Django Admin Soft](https://appseed.us/product/soft-ui-dashboard/django/) - `Product page`
  - `Features`: Fully-configured, `CI/CD` via Render
- UI Kit: [Soft Dashboard BS5](https://www.creative-tim.com/product/soft-ui-dashboard?AFFILIATE=128200) `v1.0.7` by Creative-Tim

<br />

![Django Admin Soft - Template project for Django provided by AppSeed.](https://user-images.githubusercontent.com/51070104/211278331-70dde54b-444c-4394-9e20-a2faa5d0b7de.png)

<br>

## Why `Django Admin Soft`

- Modern [Bootstrap 5](https://www.admin-dashboards.com/bootstrap-5-templates/) Design
- `Responsive Interface`
- `Minimal Template` overriding
- `Easy integration`

<br />

## How to use it

<br />

> **Install the package** via `PIP` 

```bash
$ pip install django-admin-soft-dashboard
// OR
$ pip install git+https://github.com/app-generator/django-admin-soft-dashboard.git
```

<br />

> Add `admin_soft` application to the `INSTALLED_APPS` setting of your Django project `settings.py` file (note it should be before `django.contrib.admin`):

```python
    INSTALLED_APPS = (
        ...
        'admin_soft.apps.AdminSoftDashboardConfig',
        'django.contrib.admin',
    )
```

<br />

> Add `LOGIN_REDIRECT_URL` and `EMAIL_BACKEND` of your Django project `settings.py` file:

```python
    LOGIN_REDIRECT_URL = '/'
    # EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
    EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'
```

<br />

> Add `admin_soft` urls in your Django Project `urls.py` file

```python
    from django.urls import path, include

    urlpatterns = [
        ...
        path('', include('admin_soft.urls')),
    ]
```

<br />

> **Collect static** if you are in `production environment`:

```bash
$ python manage.py collectstatic
```

<br />

> **Start the app**

```bash
$ # Set up the database
$ python manage.py makemigrations
$ python manage.py migrate
$
$ # Create the superuser
$ python manage.py createsuperuser
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
```

Access the `admin` section in the browser: `http://127.0.0.1:8000/`

<br />

## [PRO Version](https://appseed.us/product/soft-ui-dashboard-pro/django/)   

This design is a pixel-perfect [Bootstrap 5](https://www.admin-dashboards.com/bootstrap-5-templates/) Dashboard with a fresh, new design concept. `Soft UI Dashboard PRO` is built with over 300 frontend individual elements, like buttons, inputs, navbars, nav tabs, cards, or alerts, giving you the freedom of choosing and combining.

> Features: 

- `Up-to-date Dependencies`
- `Design`: [Django Theme Soft PRO](https://github.com/app-generator/django-admin-soft-pro) - `PRO Version`
- `Sections` covered by the design:
  - **Admin section** (reserved for superusers)
  - **Authentication**: `Django.contrib.AUTH`, Registration
  - **All Pages** available in for ordinary users 
- `Docker`, `Deployment`:
  - `CI/CD` flow via `Render`

<br />

![Soft UI Dashboard Pro](https://user-images.githubusercontent.com/51070104/211278814-881e0fcf-7986-4386-afee-540aa0f53bba.png)

<br />

---
**[Django Admin Soft](https://appseed.us/product/soft-ui-dashboard/django/)** - Modern Admin Interface provided by **[AppSeed](https://appseed.us/)**
