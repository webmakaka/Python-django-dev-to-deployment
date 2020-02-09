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

<br/>

    // localhost
    $ pip freeze  > requirements.txt

**possible also need package:**  
psycopg2==2.8.4


<br/>

### 61. Droplet Setup & SSH Keys

Create a Droplet

Ubuntu 18.04.3 (LTS)

$5/mo

Frankfurt

Create

<br/>

    $ ssh root@<DO_PUBLIC_IP>

<br/>

### 62. Server Security

    # adduser djangoadmin
    # usermod -aG sudo djangoadmin

    # cd /home/djangoadmin/
    # mkdir .ssh
    # cd .ssh/
    # vi authorized_keys

<br/>

add key from localhost

    $ cat ~/.ssh/id_rsa.pub

<br/>

    $ ssh djangoadmin@<DO_PUBLIC_IP>

<br/>

**Disable root login**

    $ sudo vi /etc/ssh/sshd_config

<br/>

```
PermitRootLogin no
PasswordAuthentication no
```

<br/>

    $ sudo systemctl reload sshd

<br/>

**Simple Firewall Setup**

    $ sudo ufw app list
    $ sudo ufw allow OpenSSH
    $ sudo ufw enable
    $ sudo ufw status

<br/>

### 63. Software & Database Setup

    $ sudo apt update -y && sudo apt upgrade -y

    $ sudo apt install -y python3-pip python3-dev libpq-dev postgresql postgresql-contrib nginx curl

<br/>

**Postgres Database & User Setup**

    $ sudo -u postgres psql

    CREATE DATABASE btre_prod;

    CREATE USER dbadmin WITH PASSWORD 'abc123!';

<br/>

    ALTER ROLE dbadmin SET client_encoding TO 'utf8';
    ALTER ROLE dbadmin SET default_transaction_isolation TO 'read committed';
    ALTER ROLE dbadmin SET timezone TO 'UTC';

    GRANT ALL PRIVILEGES ON DATABASE btre_prod TO dbadmin;

    \q

<br/>

### 64. Virtual Env & File Pull

<br/>

**Vitrual Environment**

    $ sudo apt install -y python3-venv

<br/>

    $ mkdir ~/projects && cd ~/projects

<br/>

    $ python3 -m venv ./venv
    $ source venv/bin/activate




<br/>

    $ git clone https://marley-golang@bitbucket.org/marley-python/python-django-dev-to-deployment.git

    $ cd python-django-dev-to-deployment/

    $ pip install -r requirements.txt

<br/>

### 65. Local Settings File

    // on server set production settings file
    $ cd project/btre/

<br/>

    $ vi local_settings.py

<br/>

```
SECRET_KEY = 'ANY SECRET KEY'
DEBUG = False
ALLOWED_HOSTS = ['DIGITAL OCEAN IP ADDRESS']

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'btre_prod',
        'USER': 'dbadmin',
        'PASSWORD': 'abc123!',
        'HOST': 'localhost'
    }
}

# Email config
# EMAIL_HOST = 'smtp.gmail.com'
# EMAIL_PORT = 587
# EMAIL_HOST_USER = 'your_gmail_username@gmail.com'
# EMAIL_HOST_PASSWORD = 'your_gmail_password'
# EMAIL_USE_TLS = True

```

<br/>

### 66. Server Migrations & Data

<br/>

**Run Migrations**

    $ cd /home/djangoadmin/projects/python-django-dev-to-deployment/project

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
    $ cd /home/djangoadmin/projects/python-django-dev-to-deployment/project/
    $ gunicorn --bind 0.0.0.0:8000 btre.wsgi

<br/>

**Stop server & deactivate virtual env**

    ctrl-c
    # deactivate

<br/>

    $ sudo vi /etc/systemd/system/gunicorn.socket

```
[Unit]
Description=gunicorn socket

[Socket]
ListenStream=/run/gunicorn.sock

[Install]
WantedBy=sockets.target
```

<br/>

    $ sudo vi /etc/systemd/system/gunicorn.service

```
[Unit]
Description=gunicorn daemon
Requires=gunicorn.socket
After=network.target

[Service]
User=djangoadmin
Group=www-data
WorkingDirectory=/home/djangoadmin/projects/python-django-dev-to-deployment/project
ExecStart=/home/djangoadmin/projects/venv/bin/gunicorn \
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

    $ sudo vi /etc/nginx/sites-available/python-django-dev-to-deployment

```
server {
    listen 80;
    server_name YOUR_IP_ADDRESS;

    location = /favicon.ico { access_log off; log_not_found off; }
    location /static/ {
        root /home/djangoadmin/projects/python-django-dev-to-deployment/project;
    }
    
    location /media/ {
        root /home/djangoadmin/projects/python-django-dev-to-deployment/project;    
    }

    location / {
        include proxy_params;
        proxy_pass http://unix:/run/gunicorn.sock;
    }
}
```

<br/>

**Enable the file by linking to the sites-enabled dir**

    $ sudo ln -s /etc/nginx/sites-available/python-django-dev-to-deployment /etc/nginx/sites-enabled

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

    $ sudo vi /etc/nginx/nginx.conf

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

    $ sudo vi local_settings.py

```
ALLOWED_HOSTS = ['IP_ADDRESS', 'example.com', 'www.example.com']
```

<br/>

    $ sudo vi /etc/nginx/sites-available/python-django-dev-to-deployment 


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