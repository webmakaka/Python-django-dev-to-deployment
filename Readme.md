# [Brad Traversy] Python Django Dev To Deployment [ENG, 10/2018]

https://www.udemy.com/course/python-django-dev-to-deployment/

<br/>

**Original src:**  
https://github.com/bradtraversy/btre_project

<br/>

## Development

<br/>

## 04. Project Specs & Getting Started

https://lokeshdhakar.com/projects/lightbox2/

<br/>

### 21. Virtual Environment Setup

    $ cd ${PROJECT_ROOT}
    $ python3 -m venv ./venv
    $ source ./venv/bin/activate

<br/>

### 22. Django Install & Project Setup

    $ pip install django==2.1

<br/>

    $ pip freeze

<br/>

    $ mkdir project
    $ cd project
    $ django-admin startproject btre .

<br/>

**VSCODE**

Ctrl + Shift + P --> python select interpretator --> virtual

<br/>

http://gitignore.io/api/django

<br/>

### 23. Exploring The Initial Files & Running The Server

    $ python manage.py runserver

http://127.0.0.1:8000/

<br/>

![Application](/img/pic-01.png?raw=true)

<br/>

## 05. Apps, URLs & Templates

<br/>

### 24. Creating The Pages App

    $ python manage.py startapp pages

    $ pip inistall autopep8

http://localhost:8000/

<br/>

![Application](/img/pic-02.png?raw=true)

<br/>

### 25. Pages Templates & Base Layout

http://localhost:8000/about

<br/>

### 26. Static Files & Paths

    $ python manage.py collectstatic

<br/>

### 27. Bootstrap Layout Markup

<br/>

![Application](/img/pic-03.png?raw=true)

<br/>

### 28. Index, About & Linking

    $ python manage.py collectstatic

<br/>

![Application](/img/pic-04.png?raw=true)
