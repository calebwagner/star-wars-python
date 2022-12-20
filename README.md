⚠️ ⚠️ This is currently a work in progress ⚠️ ⚠️

## Setting up a project with Django/Python

1) In the terminal create a folder where you want your app the live ...
  ```shell
  mkdir star-wars-python
  ```
 2) install Django ...
   ```shell
  pipenv install django
  ```
  3) activate a virtual environment ...
  ```shell
  pipenv shell
  ```
 4) install Django Admin in the current directory (this will create some boilerplate code) ...
 Note: if you were to name the porject `star-wars` a validation error would be throw like this one ...
 ```shell
 CommandError: 'star-wars' is not a valid project name. Please make sure the name is a valid identifier.
 ```

 ```shell
  django-admin startproject mysite .
  ```
  5) now open the code editor (like VS Code) using the following in the terminal window ...
  ```shell
  code .
  ```
We'll see that django-admin created a my-awesome-app directory. In that directory, you'll see a init, settings, urls, and wsgi .py files. The `__init__.py` file tells python to treat this directory as a package. The `settings.py` file is where we can configure the settings for our project. The `urls.py` file is where we define our api endpoints for our app. The `wsgi.py` file (web server gateway interface) represents the interface between apps written in python and web servers.

You'll also see a manage.py file which can be used for administrative tasks such as starting the web server, migrating a database, populating the database with data, and things like that.

---

6) Select your python interpreter ...
- use `cmd + shift + p` on Mac
- type `python interpreter`
- select the path of your specific interpreter (it'll look something like `Python 3.9.1 (mysite)`)
- you'll get an error saying "Linter pylint is not installed." so click "Install"
7) run the following command in the terminal ...
```shell
python3 manage.py runserver
```
- you'll see an error saying `You have {number} unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.` which we'll fix.
As the error says, run the following command to fix the error ...
```shell
python manage.py migrate
```
- Now, navigate to your servers address in the browser ...
```shell
http://127.0.0.1:8000/
```
---