# Generating a Project

```bash
pip install copier
copier gh:djazz/django-jazz <PROJECT_DIR>
```

Then you’ll be asked the following questions:

- **PROJECT_NAME:**
    - The name of the project as it must be displayed to users.
    - Format: `Title Case`. Example: `My App`.

- **PROJECT_SLUG:**
    - Project identifier in `lower-dash-case`. Used for the local URL.
    - Example: `my-app`.
    - Default: `PROJECT_NAME|lower|replace(" ", "-")`

- **PROJECT_SNAKE:**
    - Short project identifier in `lower_snake_case`. Used for the main Python package.
    - Example: `my_app`.
    - Default: `PROJECT_SLUG|replace("-", "_")`

- **PROJECT_DESCRIPTION:**
    - Short project description (for `pyproject.toml`).
    - Default: _empty_

- **AUTHOR_NAME:**
    - Full name of the main author.
    - Example: `John Smith`.

- **AUTHOR_EMAIL:**
    - Email of the main author. 
    - Example: `john.smith@example.com`.
    - Remark: An address_extension `+PROJECT_SLUG@` is automatically added.

- **ADMIN_BASE_URL:**
    - Base URL for the admin interface.
    - **⚠️ SECURITY:** Avoid the default `admin/`.

- **USER_TIME_ZONE:**
    - The default time zone for users.
    - Default: `Europe/Brussels`. Values: [see Wikipedia](https://en.wikipedia.org/wiki/List_of_tz_zones_by_name).

- **USER_LANGUAGE_CODE:**
    - The default language for users.
    - Format: `lower-dash-case`. Examples: `fr`, `fr-be`.
    - Default: `en`. 

- **PYTHON_VERSION:**
    - The Python version to use.
    - Default: `3.9.1`. Values: see [Dockker Hub](https://hub.docker.com/_/python/).

- **POSTGRES_VERSION:**
    - The PostgreSQL version to use.
    - Default: `13.1`. Values: see [Dockker Hub](https://hub.docker.com/_/postgres/).

- **Dockerized:**
    - Whether to use Docker.
    - Default: `yes`. Values: `yes` or `no`.


!!! note
    For more information, see [Copier’s documentation](https://copier.readthedocs.io/en/latest/generating/).
