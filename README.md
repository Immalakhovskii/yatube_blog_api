# API for Yatube #
****
**What Yatube_API does**

Creates and updates posts, comments and follows. Unauthorized user can read posts, groups and comments

**How to Start**

Clone this repository and change directory:
```
git clone https://github.com/Immalakhovskii/api_final_yatube.git
```
```
cd api_final_yatube
```
Create and activate virtual enviroment
```
python -m venv env
```
```
source env/Scripts/activate
```
Install required apps from requirements.txt
```
python -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
Make migrations
```
python manage.py migrate
```
And start project
```
python manage.py runserver
``` 
**Yatube_API Documentation**

See ReDoc at http://127.0.0.1:8000/redoc/ 
Accessible when development server activated: 
```
python manage.py runserver
```