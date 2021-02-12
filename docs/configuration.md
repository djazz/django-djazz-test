# Configuration

## Python Version

Define the Python version to use in `/.python-version`.


## Packaging

TODO: DECISION: pip, Pipenv, Poetry, conda?
- Why Poetry?

Always use [`Poetry`](https://python-poetry.org/)… unless exceptionally for **very good** reasons.

**References:**

- [pip - The Python Package Installer](https://pip.pypa.io/)
- [setuptools](https://setuptools.readthedocs.io/)
- [wheel](https://wheel.readthedocs.io/)


## Project Settings

Always use `pyproject.toml`… unless not possible.

**References:**

- [PEP 518 -- Specifying Minimum Build System Requirements for Python Projects](https://www.python.org/dev/peps/pep-0518/)
- [PEP 621 -- Storing project metadata in pyproject.toml](https://www.python.org/dev/peps/pep-0621/)


## Sensitive Settings

@TODO: .env & 12-factor

**References:**

- [The Twelve-Factor App](https://12factor.net/)


## Django Configuration

- Group all configuration files in `/config`.

Typical configuration files of a Django project:

- [`asgi.py`](https://docs.djangoproject.com/en/3.1/howto/deployment/asgi/): Configuration for ASGI servers.
- [`settings.py`](https://docs.djangoproject.com/en/3.1/topics/settings/): All the configuration of the application.
- [`urls.py`](https://docs.djangoproject.com/en/3.1/topics/http/urls/): Root `URLconf` (URL configuration), mapping URL path to Python functions.
- [`wsgi.py`](https://docs.djangoproject.com/en/3.1/howto/deployment/wsgi/): Configuration for WSGI servers.


## Django Settings

- For small projects/basic needs, use a single `/config/settings.py` file.
- Otherwise, use one `/config/settings/<name>.py` per [`application mode`](terminology#application-mode).

**@TODO:**

- @TODO: settings, base & APP_MODE
- @TODO: manage, asgi, wsgi + bootstrap
- @TODO: urls
- @TODO: PACKAGE_NAME & apps
- @TODO: templates
- @TODO: static & uploads
