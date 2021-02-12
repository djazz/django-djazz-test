# File Structure


## Project Structure

```
<PROJECT_SLUG>
├── .envs
│   └── .env.<SERVICE_NAME>
├── <PROJECT_SNAKE>
│   └── __init__.py
├── bin
│   ├── db-create.sh
│   └── db-remove.sh
├── config
│   ├── formats
│   │   ├── <LOCALE>
│   │   │   ├── __init__.py
│   │   │   └── formats.py
│   │   ├── __init__.py
│   │   └── base.py
│   ├── settings
│   │   ├── __init__.py
│   │   ├── base.py
│   │   └── <APP_MODE>.py
│   ├── __init__.py
│   ├── asgi.py
│   ├── bootstrap.py
│   ├── urls.py
│   └── wsgi.py
├── docker
│   ├── <SERVICE_NAME>
│   │   │   └── <RESOURCE_NAME>
│   │   ├── Dockerfile
│   │   └── Dockerfile.local
│   ├── local.yml
│   └── production.yml
├── docs
├── locale
│   └── <LOCALE_NAME>
├── requirements
│   ├── _includes
│   │   ├── base.txt
│   │   └── <EXTRA_NAME>.txt
│   └── <APP_MODE>.txt
├── static
│   ├── css
│   ├── favicons
│   │   └── favicon.ico
│   ├── fonts
│   ├── js
│   ├── media
│   └── robots.txt
├── templates
│   ├── _includes
│   │   ├── analytics.html
│   │   ├── page_footer.html
│   │   └── page_header.html
│   ├── errors
│   │   ├── 400.html
│   │   ├── 403.html
│   │   ├── 404.html
│   │   ├── 500.html
│   │   └── base.html
│   ├── <APP_NAME>
│   │   ├── _includes
│   │   ├── base.html
│   │   └── <TEMPLATE_NAME>.html
│   └── base.html
├── tests
├── var
│   ├── cache
│   ├── files
│   ├── log
│   └── static
├── .copier-answers.yml
├── .editorconfig
├── .env
├── .gitattributes
├── .gitignore
├── .python-version
├── README.md
├── dj
├── manage.py
└── pyproject.toml
```

## App Structure

```
<APP_NAME>
├── locale
│   └── <LOCALE_NAME>
├── migrations
├── static
│   └── <APP_NAME>
├── templates
│   └── <APP_NAME>
├── templatetags
│   ├── __init__.py
│   └── <APP_NAME>.py
├── __init__.py
├── admin.py
├── apps.py
├── constants.py
├── formfields.py
├── forms.py
├── managers.py
├── middlewares.py
├── modelfields.py
├── models.py
├── tasks.py
├── translation.py
├── urls.py
└── views.py
```
