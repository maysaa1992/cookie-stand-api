# api-quick-start

Template Project for starting up CRUD API with Django Rest Framework

## Customization Steps

- DO NOT migrate yet
- add additional dependencies as needed
  - Re-export requirements.txt as needed
- change `CookieStands` folder to the app name of your choice
- Search through entire code base for `CookieStand`,`CookieStands` and `CookieStands` to modify code to use your resource
  - `project/settings.py`
  - `project/urls.py`
  - App's files
    - `views.py`
    - `urls.py`
    - `admin.py`
    - `serializers.py`
    - `permissions.py`
  - "Front" files
    - if including a customer facing portion of the site then update/recreate:
      - `urls_front.py`
      - `views_front.py`
      - template files
      - Make sure to update project `urls.py` to add routes to the "front".
- Update CookieStandModel with fields you need
  - Make sure to update other modules that would be affected by Model customizations. E.g. serializers, tests, etc.
- Rename `project/.env.sample` to `.env` and update as needed
  - To generate secret key use `python3 -c "import secrets; print(secrets.token_urlsafe())"`
- Run makemigrations and migrate commands when ready.
- Run `python manage.py collectstatic`
  - This repository includes static assets in repository. If you are using a Content Delivery Network then remove `staticfiles` from repository.
- Optional: Update `api_tester.py`

## Database

**NOTE:** If you are using Postgres instead of SQLite then make sure to install `psycopg2-binary` and include in `requirements.txt`


# LAB - Class 34
## Project: Putting it All Together
Author: Maysa'a Albataineh

back-end server url (when applicable)
* elephantsql : https://api.elephantsql.com/console/8f0d77b5-41c0-4577-9d83-115e51c06dc8/browser?#

.env requirements (where applicable)
SECRET_KEY=tJBQCg0-ZrTHK72RPy0FVjX6FU8cWKLMEsH-2PNl9dk
DEBUG=True

* ALLOWED_HOSTS=localhost,127.0.0.1,0.0.0.0
* ALLOW_ALL_ORIGINS=True
* postgres://rrngfxye:LetwFqwnzZTH0fW386KQ4hlSrAe8fi5p@drona.db.elephantsql.com/rrngfxye
* DATABASE_ENGINE=django.db.backends.postgresql
* DATABASE_NAME=rrngfxye
* DATABASE_USER=rrngfxye
* DATABASE_PASSWORD=LetwFqwnzZTH0fW386KQ4hlSrAe8fi5p
* DATABASE_HOST=drona.db.elephantsql.com
* DATABASE_PORT=5432

## PORT - Port Number:  5432
## DATABASE_URL - URL to the running Postgres instance/db

* elephantsql : https://api.elephantsql.com/console/8f0d77b5-41c0-4577-9d83-115e51c06dc8/browser?#

## to initialize/run your application (where applicable)
* docker-compose run web python manage.py runserverHow to use your library (where applicable)

