# Django Admin Soft Dashboard

Modern template for **Django Admin Interface** coded on top of **[Soft UI Dashboard](https://github.com/app-generator/ct-soft-ui-dashboard-enh)** (free version). 

> UI Kit: `[Soft UI Dashboard](https://github.com/app-generator/ct-soft-ui-dashboard-enh)` **v1.0.6-enh1**

<br>

**Links & Resources**

- [Django Volt Dashboard](https://appseed.us/admin-dashboards/django-dashboard-volt) - Open-source starter that uses the same UI Kit
- [Django Volt Dashboard](https://django-volt-dashboard.appseed-srv1.com/) - LIVE Demo
- More [Django Dashboards](https://appseed.us/admin-dashboards/django) provided by AppSeed 

<br />

## Why Django Admin Soft?

- Bootstrap 5 Design: **Soft UI Dashboard** (Free version) provided by **Creative-Tim**
- New fresh look
- Responsive mobile interface
- Useful admin home page
- Minimal template overriding
- Easy integration

<br />

![Django Admin Soft - Template project for Django provided by AppSeed.](https://user-images.githubusercontent.com/51070104/191189699-fbd527b6-ba10-465a-a7f7-a27b3d0d19bc.png)

<br>

## How to use it

<br />

> Install the package via `PIP` 

```bash
$ pip install django-admin-soft-dashboard
// OR
$ pip install git+https://github.com/app-generator/django-admin-soft-dashboard.git
```

<br />

> Add `admin_volt` application to the `INSTALLED_APPS` setting of your Django project `settings.py` file (note it should be before `django.contrib.admin`):

```python
    INSTALLED_APPS = (
        ...
        'admin_volt.apps.AdminSoftDashboardConfig',
        'django.contrib.admin',
    )
```

<br />

> All programs you add in **INSTALLED_APPS** should look like this: **APP_NAME.apps.APP_NAMEConfig**.

In this feature, we considered that each App can have its own icon, so we ask users to use this feature according to the method. Also in apps.py of each program according to the example add the icon field in the corresponding class. You can go **[here](https://fontawesome.com/v4.7/icons/)** to use more icons


```python

    from django.apps import AppConfig

    class APP_NAMEConfig(AppConfig):
        name = 'APP_NAME'
        icon = 'ICON_CLASS'  # for example: icon = 'fa fa-users'
```

<br />

> Make sure `django.template.context_processors.request` context processor is enabled in settings.py (Django 1.8+ way):

```python

    TEMPLATES = [
        {
            'BACKEND': 'django.template.backends.django.DjangoTemplates',
            'DIRS': [],
            'APP_DIRS': True,
            'OPTIONS': {
                'context_processors': [
                    ...
                    'django.template.context_processors.request',
                    ...
                ],
            },
        },
    ]
```

:warning: **Warning!!**
* Before Django 1.8 you should specify context processors different way. Also use ``django.core.context_processors.request`` instead of ``django.template.context_processors.request``.

```python
    from django.conf import global_settings

    TEMPLATE_CONTEXT_PROCESSORS = global_settings.TEMPLATE_CONTEXT_PROCESSORS + (
        'django.core.context_processors.request',
    )
```

<br />

> Collect static if you are in production environment:

```bash
$ python manage.py collectstatic
```

<br />

> Start the app

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

## Screenshots

@todo

---
**Django Admin Soft Dashboard** - Open-source Django Admin THEME provided by **AppSeed [App Generator](https://appseed.us/)**
