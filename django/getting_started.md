**Django** - popular PYTHON web development framework
           - It has batteries included i,e it comes with pre-installed libraries needed for common use-cases.
           
           
 A Django project has one or more apps. An app is the core functionalities in a project. A To-Do project can have apps like notes, remainder..etc
 
 To start a Django project:
 ```
 django-admin startproject project_name
 ```
 project_name will have two items -- project_name/ and manage.py. **manage.py** is used for administrative purposes. The command line utility for such purpose is django-admin.
 Administrative tasks include running the server, deleting the contents of the database..etc. **settings.py**, **urls.py** ,**wsgi.py**
 and **__init__.py** are contained in **projectname/**. __init__.py tells python the current directory is a package and it ,ay have submodules.
 
 To run:
 ```
 python manage.py runserver
 ```
 To create  an app:
 ```
 django-admin startapp app_name
 ```
 
 
            
