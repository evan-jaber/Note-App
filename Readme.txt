QUICK SETUP:

1) Install and activate virtual environment
In the root folder, on the terminal create a virtual environment.
 Terminal command: python -m venv [name of the environment (usually env)]
 Activate command: env/Scripts/activate

2) Creating and setting up Django Project
 a) Install django and all the main libraries : 
  a. pip install django 
  b. pip install djangorestframework django-cors-headers
  
 b) Create project in terminal: django-admin startproject server
 c) Cd to the server folder
 d) Create an app in django in the terminal
  a. python manage.py startapp [name of the app 'api']
  
3) Create a react app using vite
Go back to the root folder and:
 a) npm create vite@latest client -- --template react
 b) cd client
 c) npm install

4) Open VS code and the run the servers
 a) In the root folder open VS code:
  a. code .
 b) Open two terminals and make sure your virtual environment is active
 c) Run django server
  a. cd to server
  b. python manage.py runserver
 d) Run react server
  a. cd to client
  b. npm run dev
 
  
 5) Set up the settings.py to include rest_framework and corsheaders
  CORS_ALLOWED_ORIGINS = [
      "http://127.0.0.1:5173",
      "http://localhost:5173",
  ]
  
  #Application definition
  
  INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      #External Apps
      'rest_framework',
      'corsheaders',
      #Internal Apps
      'api',
  ]
  
  MIDDLEWARE = [
      'django.middleware.security.SecurityMiddleware',
      'django.contrib.sessions.middleware.SessionMiddleware',
      "corsheaders.middleware.CorsMiddleware",
      'django.middleware.common.CommonMiddleware',
      'django.middleware.csrf.CsrfViewMiddleware',
      'django.contrib.auth.middleware.AuthenticationMiddleware',
      'django.contrib.messages.middleware.MessageMiddleware',
      'django.middleware.clickjacking.XFrameOptionsMiddleware',
  ]

6) Install requierments
    a. activate env
    b. cd to server
    c. pip freeze > requirments.txt

7) Install django environ
    a. activate env
    b. cd to server
    c. pip install django-environ

