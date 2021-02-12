# Terminology

## Application Mode

The `application mode` (or `app mode` for short) defines the context in which the application is running.

It’s related to the deployment environment and has an impact on settings and dependencies, and sometimes also on the behavior of the application.

**Values:**

- `local`: The context in which developers work.
- `testing`: The context in which tests are performed.
- `development`: Server running the latest version of the code. _(sometimes called integration”)_
- `staging`: Mirror of the production, for final testing/approval.
- `production`: The live application, used by end-users.

**Current Value:** `APP_MODE` (defined in `.env`, available via `settings`).

**Variable Name:** `app_mode`.

**Rule:** These values must be used in full and lowercase.  
If the use of an abbreviation makes **really more sense**, the 3 first letters are used.
@TODO: ??? Acceptable abbreviations: dev, test, prod.

**References:**

- [Wikipedia](https://en.wikipedia.org/wiki/Deployment_environment)


## Internationalization & Localization

See [Django’s documentation](https://docs.djangoproject.com/en/3.1/topics/i18n/#definitions).

- `Locale name`: For example `en`, `fr_BE`, `sr_Latn`.
- `Language code`: For example `en`, `fr-be`.
