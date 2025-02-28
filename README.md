Run This Project:

git clone https://github.com/dev-priyanshu15/IPO-WebApp  
cd bluestock-ipo-webapp  
pip3 install -r requirements.txt  
python3 manage.py makemigrations  
python3 manage.py migrate  
python3 manage.py createsuperuser  
python3 manage.py runserver  
Connect Django to PostgreSQL:
Install PostgreSQL for official site
Create Database & User:

CREATE DATABASE bluestock;  
CREATE USER priyanshu WITH PASSWORD 'your_password';
ALTER ROLE priyanshu SET client_encoding TO 'utf8';
ALTER ROLE priyanshu SET default_transaction_isolation TO 'read committed';
ALTER ROLE priyanshu SET timezone TO 'UTC';
GRANT ALL PRIVILEGES ON DATABASE bluestock TO priyanshu; 
Install PostgreSQL Adapter:

pip install psycopg2-binary  
Update settings.py:
python
Copy
Edit
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'bluestock',
        'USER': 'daiyanalam',
        'PASSWORD': '12345',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
Apply Migrations & Run Server:

python3 manage.py makemigrations  
python3 manage.py migrate  
python3 manage.py runserver  