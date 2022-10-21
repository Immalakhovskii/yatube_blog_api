# Yatube API #
*This project is an almost exact Django REST Framework implementation of a blogging network Yatube made with Django which can be seen here: https://github.com/Immalakhovskii/yatube_blog_final*
****
### Description ###
Web API service Yatube collects posts which can be commented and assigned to groups. Posts authors can be subscribed (followed) by authorized users. Anonymous user can read posts, groups and comments. Authenticated user has all rights of an anonymous and also can create posts, update own posts, comment own and others posts, update and delete own comments. For authentication Yatube API uses JWT tokens. While project activated full API documentation can be seen here: http://127.0.0.1:8000/redoc/

### Technology Stack ###
Python 3.7 / Django 2.2.16 / Django REST framework 3.12.4

### How to Start Yatube API ###
```
# clone repository, create virtual enviroment and install dependencies
git clone https://github.com/Immalakhovskii/yatube_blog_api.git
cd yatube_blog_api/
python -m venv venv
python.exe -m pip install --upgrade pip
python -m pip install -r requirements.txt

# activate virtual enviroment 
source venv/Scripts/activate            # (Windows) 
source venv/bin/activate                # (macOS and Linux)

# prepare to start development server
cd yatube_api/
cp .env.example .env                    # copy .env.example with valid data as .env
python manage.py migrate
python manage.py createsuperuser

# start!
python manage.py runserver
```
Now admin site of the project available at http://127.0.0.1:8000/admin/. API requests can be performed by addresses starting with http://127.0.0.1:8000/api/v1/ (see full list of available requests here: http://127.0.0.1:8000/redoc/)

- Actual enviromental variables for the YaMDb stored at yatube_api/.env.example. Safety precautions ignored for the public availability of the project

### Get JWT token ###

To recieve JSON Web Token (JWT) send POST request with "username" and "password" to http://127.0.0.1:8000/api/v1/jwt/create/. JWT lasts 1 day refresh it with POST request to http://127.0.0.1:8000/api/v1/jwt/refresh/ with expired token passed in "refresh"
