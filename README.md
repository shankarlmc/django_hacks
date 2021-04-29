# How to install Django on Windows
Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design. Built by experienced developers, it takes care of much of the hassle of Web development, so we can focus on writing our app without needing to reinvent the wheel. It’s free and open source.

## Installation 
Before we can use Django, we’ll need to install it. My complete installation guide will get you to a simple, minimal installation.

- Install Python
Being a Python Web framework, Django requires Python. Get the latest version of Python at [Here](https://www.python.org/downloads/)
You can verify that Python is installed by typing python from your Command Prompt; you should see something like:
```
python
Python 3.9.0 [MSC v.1927 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
```
- Install Django
```
python -m pip install Django
```
- Setup Environment
```
C:\Users\username>python -m pip install virtualenv
C:\Users\username>python -m venv env
C:\Users\username>env\Scripts\activate
(env)C:\Users\username>
```
Installation of django and environment setup is completed.

## Creating a first django project

```
(env)C:\Users\username>django-admin startproject blog
```
Let’s look at what startproject created:
```
blog/
    manage.py
    blog/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```
The development server:
```
(env)C:\Users\username>cd blog
(env)C:\Users\username>blog>python manage.py runserver
```
You’ll see the following output on the command line:
```
Performing system checks...

System check identified no issues (0 silenced).

You have unapplied migrations; your app may not work properly until they are applied.
Run 'python manage.py migrate' to apply them.

April 28, 2021 - 15:50:53
Django version 3.2, using settings 'blog.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```
Creating the home app
```
(env)C:\Users\username>blog>python manage.py startapp home 
```
That’ll create a directory home, which is laid out like this:
```
home/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```
