---
description: The web framework for perfectionists with deadlines.
---

# django

## resources

* Getting started: [https://www.djangoproject.com/start/](https://www.djangoproject.com/start/)
* Doc: [https://docs.djangoproject.com/en/3.1/genindex/](https://docs.djangoproject.com/en/3.1/genindex/)
* API Reference: [https://docs.djangoproject.com/en/3.1/ref/](https://docs.djangoproject.com/en/3.1/ref/)

## installation

Django is a normal python package and can be installed as such.

## why it is better than rails

* migrations are entirely derived from models
* lightweight
* it's python

## command-line summary

* create project: `$ django-admin startproject mysite` \(outer folder can be renamed\)
* run dev server: `$ python manage.py runserver` \(where manage.py is\)
  * set port: `$ python manage.py runserver 8080`
  * set ip and port: `$ python manage.py runserver 0:8080`
  * running dev server automatically reloads python code for each request, no server restart needed, yet some actions like adding a file still require a restart
* create app: `$ python manage.py startapp polls`
* migrate, creates necessary db tables: `$ python manage.py migrate`
* store changes as migration: `$ python manage.py makemigrations polls`
* open shell: `$ python manage.py shell`

## project

```text
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```

* manage.py: command-line utility to interact with the project
* mysite/settingts.py: settings/configuration for project
* mysite/urls.py: URL declarations

### apps

A project consists of multiple application, that represent something like a weblogsystem, record database, small poll app or similar. They can live anywhere.

```text
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```

### urls

Are set in each application and on the project top-level file urls.py.

* url dispatcher: [https://docs.djangoproject.com/en/3.1/topics/http/urls/](https://docs.djangoproject.com/en/3.1/topics/http/urls/)

### models

Models are set in the corresponding models.py and migrations are created based on them.

Three-step guide to making model changes:

* Change your models \(in models.py\).
* Run python manage.py makemigrations to create migrations for those changes
* Run python manage.py migrate to apply those changes to the database.

### templates

* Templates [https://docs.djangoproject.com/en/3.1/topics/templates/](https://docs.djangoproject.com/en/3.1/topics/templates/)

## ci / cd

### example project with gunicorn, postgres, nginx and docker

* [https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/\#project-setup](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/#project-setup)

### 

### references

{% embed url="https://medium.com/@\_gabiCavalcante/python-django-and-github-ci-cd-65f9eae7e6fa" %}

{% embed url="https://python-deploy-framework.readthedocs.io/en/latest/pages/django-deployment.html" %}



  



