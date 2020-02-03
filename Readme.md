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

<br/>

## 06. View Methods, Display & Search

<br/>

### 39. Pull Data From Listings Model

<br/>

### 40. Display Listings In Template

<br/>

![Application](/img/pic-11.png?raw=true)

<br/>

### 41. Pagination, Order & Filter

<br/>

![Application](/img/pic-12.png?raw=true)

<br/>

### 42. Home & About Page Dynamic Content

admin --> realtors --> Jenny Johnson --> is mvp

<br/>

![Application](/img/pic-13.png?raw=true)

<br/>

![Application](/img/pic-14.png?raw=true)

<br/>

![Application](/img/pic-15.png?raw=true)


<br/>

### 43. Single Listing Page

<br/>

![Application](/img/pic-16.png?raw=true)

<br/>

![Application](/img/pic-17.png?raw=true)

<br/>

### 44. Search Form Choices

<br/>

![Application](/img/pic-18.png?raw=true)

<br/>

### 45. Search Form Filtering

<br/>

![Application](/img/pic-19.png?raw=true)


<br/>

### 46. Preserving Form Input


<br/>

## 07. Accounts & Authentication

<br/>

### 47. Accounts App & URLs

    $ python manage.py startapp accounts
    
<br/>

### 48. Register & Login Templates

<br/>

![Application](/img/pic-20.png?raw=true)

<br/>

### 49. Message Alerts

<br/>

![Application](/img/pic-21.png?raw=true)

<br/>

### 50. User Registration

<br/>

![Application](/img/pic-22.png?raw=true)


<br/>

### 51. User Login

<br/>

### 52. Logout & Navbar Auth Links

<br/>

![Application](/img/pic-23.png?raw=true)

<br/>

### 53. Dynamic Page Titles

<br/>

## 08. Contact Inquiries

<br/>

### 54. Contacts App & Model

    $ python manage.py startapp contacts

    $ python manage.py makemigrations contacts
    $ python manage.py migrate

<br/>

### 55. Contacts Admin Customization

<br/>

![Application](/img/pic-24.png?raw=true)

<br/>

### 56. Contact Form Prep

<br/>

![Application](/img/pic-25.png?raw=true)

<br/>

### 57. Contact Form Submission

<br/>

![Application](/img/pic-26.png?raw=true)

<br/>

### 58. Inquiry Check & Send Email

Need update:

```
btre/settings.py

EMAIL_HOST_USER = 'your_gmail_username@gmail.com'
EMAIL_HOST_PASSWORD = 'your_gmail_password'
```

and

```
contacts/views.py

'admin.example@gmail.com'
'additonal.example@gmail.com'

```

<br/>

### 59. Dashboard Functionality

<br/>

![Application](/img/pic-27.png?raw=true)


<br/>

## 09. Django Deployment

https://gist.github.com/bradtraversy/cfa565b879ff1458dba08f423cb01d71

<br/>

### 60. Pushing To Github

skipped

<br/>

### 61. Droplet Setup & SSH Keys

skipped

<br/>

### 62. Server Security

skipped

<br/>

### 63. Software & Database Setup

skipped

<br/>

### 64. Virtual Env & File Pull

    // localhost
    $ pip freeze  > requirements.txt

**possible also need package:**  
psycopg2==2.8.4

    // server
    $ pip install -r requirements.txt

<br/>

### 65. Local Settings File

    // on server set production settings file
    $ cd btre
    $ sudo nano local_settings.py

<br/>

```
SECRET_KEY = 'ANY SECRET KEY'
DEBUG = False
ALLOWED_HOSTS = ['DIGITAL OCEAN IP ADDRESS']

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'DB_NAME',
        'USER': 'DB_USER',
        'PASSWORD': 'DB_PASSWORD',
        'HOST': 'ec2-50-19-127-115.compute-1.amazonaws.com'
    }
}

# Email config
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_PORT = 587
EMAIL_HOST_USER = 'your_gmail_username@gmail.com'
EMAIL_HOST_PASSWORD = 'your_gmail_password'
EMAIL_USE_TLS = True

```

<br/>

### 66. Server Migrations & Data

<br/>

**Run Migrations**

    $ python manage.py makemigrations
    $ python manage.py migrate

<br/>

**Create super user**

    $ python manage.py createsuperuser

<br/>

**Create static files**

    $ python manage.py collectstatic

<br/>

**Create exception for port 8000**

    $ sudo ufw allow 8000

<br/>

**Run Server**

    $ python manage.py runserver 0.0.0.0:8000


**Test the site at YOUR_SERVER_IP:8000**

    $ http://<YOUR_SERVER_IP>:8000

Add some data in the admin area

<br/>

### 67. Gunicorn Setup & Config

https://gunicorn.org/

    $ pip install gunicorn

    $ pip freeze > requirements.txt

    // Test Gunicorn serve
    # gunicorn --bind 0.0.0.0:8000 btre.wsgi

<br/>

**Stop server & deactivate virtual env**

    ctrl-c
    # deactivate

<br/>

    $ sudo nano /etc/systemd/system/gunicorn.socket

```
[Unit]
Description=gunicorn socket

[Socket]
ListenStream=/run/gunicorn.sock

[Install]
WantedBy=sockets.target
```

<br/>

    $ sudo nano /etc/systemd/system/gunicorn.service

```
[Unit]
Description=gunicorn daemon
Requires=gunicorn.socket
After=network.target

[Service]
User=djangoadmin
Group=www-data
WorkingDirectory=/home/djangoadmin/pyapps/btre_project
ExecStart=/home/djangoadmin/pyapps/venv/bin/gunicorn \
          --access-logfile - \
          --workers 3 \
          --bind unix:/run/gunicorn.sock \
          btre.wsgi:application

[Install]
WantedBy=multi-user.target
```

<br/>

**Start and enable Gunicorn socket**

    $ sudo systemctl start gunicorn.socket
    $ sudo systemctl enable gunicorn.socket

<br/>

**Check status of guinicorn**

    $ sudo systemctl status gunicorn.socket

**Check the existence of gunicorn.sock**

    $ file /run/gunicorn.sock

<br/>

### 68. Nginx Setup

    $ sudo nano /etc/nginx/sites-available/btre_project

```
server {
    listen 80;
    server_name YOUR_IP_ADDRESS;

    location = /favicon.ico { access_log off; log_not_found off; }
    location /static/ {
        root /home/djangoadmin/pyapps/btre_project;
    }
    
    location /media/ {
        root /home/djangoadmin/pyapps/btre_project;    
    }

    location / {
        include proxy_params;
        proxy_pass http://unix:/run/gunicorn.sock;
    }
}
```

<br/>

**Enable the file by linking to the sites-enabled dir**

    $ sudo ln -s /etc/nginx/sites-available/btre_project /etc/nginx/sites-enabled

<br/>

**Test NGINX config**

    $ sudo nginx -t

<br/>

**Restart NGINX**

    $ sudo systemctl restart nginx

<br/>


**Remove port 8000 from firewall and open up our firewall to allow normal traffic on port 80**

    $ sudo ufw delete allow 8000
    $ sudo ufw allow 'Nginx Full'

You will probably need to up the max upload size to be able to create listings with images

Open up the nginx conf file

    $ sudo nano /etc/nginx/nginx.conf

<br/>

Add this to the http{} area

```
client_max_body_size 20M;
```

<br/>

    $ sudo systemctl restart nginx


**Media File Issue**

You may have some issues with images not showing up. I would suggest, deleting all data and starting fresh as well as removeing the "photos" folder in the "media folder"

    $ sudo rm -rf media/photos

<br/>

### 69. Adding A Domain

Go to your domain registrar and create the following a record

```
@  A Record  YOUR_IP_ADDRESS
www  CNAME  example.com
```

<br/>

**Go to local_settings.py on the server and change "ALLOWED_HOSTS" to include the domain**

    $ sudo nano local_settings.py

ALLOWED_HOSTS = ['IP_ADDRESS', 'example.com', 'www.example.com']

<br/>

$ sudo nano /etc/nginx/sites-available/btre_project

<br/>

```
server {
    listen: 80;
    server_name xxx.xxx.xxx.xxx example.com www.example.com;
}
```

<br/>

**Reload NGINX & Gunicorn**

    $ sudo systemctl restart nginx
    $ sudo systemctl restart gunicorn

<br/>
<br/>
<br/>

---

<a href="https://marley.org"><strong>Marley</strong></a>