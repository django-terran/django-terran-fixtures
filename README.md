# Django Terran Fixtures

This repository contains fixtures for the `django-terran` application. The fixtures include data for:

- Currencies;
- Countries;
- Administrative divisions of countries;
- Settlements;
- and relationships between them all.

This repository exists so that you can conviniently download prebuilt fixtures as a ZIP file.

## What is Django Terran?

See https://github.com/django-terran/django-terran

## How to use?

Load these fixtures just like any other fixture

Mandatory fixtures include
```
./manage.py loadadata <path/to/fixtures>/currencies.json
./manage.py loadadata <path/to/fixtures>/countries.json
./manage.py loadadata <path/to/fixtures>/level1areas.json
./manage.py loadadata <path/to/fixtures>/level2areas.json
```
Optional fixtures include files under "settlements" directory.
```
./manage.py loadadata <path/to/fixtures>/settlements/GE.json
```

**DO NOT** load optional fixtures if you do not need them. They are huge, they will add more than 2Gb to your database.
Load only countries you really need.

## How can I help?

See https://github.com/django-terran/django-terran-data

## Licenses

See https://github.com/django-terran/django-terran-data

## Acknowledgments

See https://github.com/django-terran/django-terran-data