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

<br/>

### 29. Listings URLs & Template

    $ python manage.py startapp listings
    $ python manage.py startapp realtors

<br/>

![Application](/img/pic-05.png?raw=true)

<br/>

## 05. Models, Migrations & Admin

<br/>

### 30. Install Postgres & PgAdmin

I will use postgres from heroku free database for hobby

<br/>

### 31. Django Postgres Setup & Migrate

    $ pip install psycopg2
    $ pip install psycopg2-binary

    $ python manage.py migrate

<br/>

### 32. Planning Our Schemas

```
MODEL/DB FIELDS

### LISTING
id: INT
realtor: INT (FOREIGN KEY [realtor])
title: STR
address: STR
city: STR
state: STR
zipcode: STR
description: TEXT
price: INT
bedrooms: INT
bathrooms: INT
garage: INT [0]
sqft: INT
lot_size: FLOAT
is_published: BOOL [true]
list_date: DATE
photo_main: STR
photo_1: STR
photo_2: STR
photo_3: STR
photo_4: STR
photo_5: STR
photo_6: STR

### REALTOR
id: INT
name: STR
photo: STR
description: TEXT
email: STR
phone: STR
is_mvp: BOOL [0]
hire_date: DATE

### CONTACT
id: INT
user_id: INT
listing: INT
listing_id: INT
name: STR
email: STR
phone: STR
message: TEXT
contact_date: DATE
```

<br/>

### 33. Create Listing Model

<br/>

### 34. Realtor Model & Run Migrations

    $ pip install Pillow
    $ python manage.py makemigrations
    $ python manage.py migrate

<br/>

### 35. Create Superuser & Register Models With Admin

    $ python manage.py createsuperuser

http://localhost:8000/admin

<br/>

![Application](/img/pic-06.png?raw=true)

<br/>

### 36. Media Folder & Adding Data

admin -> Realtors --> Add

<br/>

![Application](/img/pic-07.png?raw=true)

admin -> Listings --> Add

<br/>

![Application](/img/pic-08.png?raw=true)

<br/>

### 37. Admin Logo & CSS

<br/>

![Application](/img/pic-09.png?raw=true)

<br/>

### 38. Customize Admin Display Data

<br/>

![Application](/img/pic-10.png?raw=true)
