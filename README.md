# docker-python-postgresql
This is for building a development environment using Python and PostgreSQL.
I do not guarantee security.

It is supposed to develop applications using Flask or Django.

## env
The operation has been confirmed below.

* macOS 10.14.6
* Docker(Docker for mac): 18.09.2
* docker-compose: 1.23.2

## Usage

create project on project root.
(For example, in the case of the Django project.)

```
├ docker/
├ docker-compose.yml
├ :
├ django_app/
├ manage.py
└ requirements.txt
```

### Adjust bin/start.sh

```
## django app
python3 manage.py runserver 0.0.0.0:8000
```

### set environment variables

set variables to .env

```
POSTGRES_DB="postgres"
POSTGRES_USER="postgres"
POSTGRES_PASSWORD="postgres"
```

### Start Docker

```
# only first time.
$ docker-compose up --build

Use this after the second time.
$ docker-compose start
```

Access the following in your browser:  
http://0.0.0.0:8000

## LISENCE
MIT
