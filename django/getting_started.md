**Django** - popular PYTHON web development framework
           - It has batteries included i,e it comes with pre-installed libraries needed for common use-cases.

**PART I**
           
 A Django project has one or more apps. An app is the core functionalities in a project. A To-Do project can have apps like notes, remainder..etc
 
 To start a Django project:
 ```
 django-admin startproject project_name
 ```
 project_name will have two items -- project_name/ and manage.py. **manage.py** is used for administrative purposes. The command line utility for such purpose is django-admin.
 Administrative tasks include running the server, deleting the contents of the database..etc. **settings.py**, **urls.py** ,**wsgi.py** and **__ __init__.py __** are contained in **projectname/**. **__ __init__.py __** tells python the current directory is a package and it ,ay have submodules. In urls.py the serach is done only for url patterns but he domainn name or GET, POST parameters aren't serached for. **settings.py** --> insert our apps in the INSTALLED_APPS list, also has configurations for time,language ..etc
 
 To run:
 ```
 python manage.py runserver
 ```
 To create  an app:
 ```
 django-admin startapp app_name
 ```
 An app will have files like - 
 
 urls.py --> For mapping the views to a url - regex expressions may be used
 
 views.py --> Views are python functions that receive an object and sends back a response. Contains                                                                                                                 the logic behind the application(urlpatterns = [path(<url_string>",view,keyword_arguments,name_given_to_url)])
 
 models.py --> For defining entities of the application
 
 migrations/
 
 tests.py - 
 
 admin.py
                               
 -----------------------------------------------------------------------------                            
                               
lsof -i:<port_number> -->  To find which process is listening upon that port

In a module __ name__ global variable has the module name

------------------------------------------------------------------------------



**TEMPLATES**

All the html files are usually stored in the templates directory of project directory. In the settings.py the path to the templates has to be updated. Django Template Language is used to pass values from the views to html files.[eg. {{varible}}, {% statements %}]. Templates are render as:

*return render(request, 'home.html', {'boards': boards})*   i,e by using the render class fron django.shortcuts. Here boards is value to be passed to the html file home.html.

**STATIC FILES**

Static files include js,css ..etc like files. These are usually stored in static/ in the project directory. The path to this folder has to be updated in settings.py

**DJANGO ADMIN**

Django provides an admin page through which an admin can handle the data insertion, updation, deletion ..etc in an easier way. Django comes with this admin app installed in the project. To create an admin or super user:
```
python manage.py createsuperuser
```
Then the username and password is set.
 
 
            
