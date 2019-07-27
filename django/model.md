**PART II - MODELS, TEMPLATES, STATIC FILES, DJANGO ADMIN**

* Models - representation of database layout. All models are subclasses of django.db.models.Model class. A User moodel is defined by default in django.contrib.auth.models . The fields can be CharField, DateTimeField... etc. For CharField the length of the text iss predefined while for TextField it can take in unlimited text. The field types can have parameters like max_lenght, unique...etc for setting up special properties. Every models/tables are written in the form of classes.
* Primary key will be automatically set up Django if not manually given
* __Migrating__ means to propagate the changes made into models in models.py to the database.
```
python manage.py makemigrations <app_name>
```
This command will create a migration file that conatains depndencies and operations. After any change to the models, upon execution of this command, a new migaration file is generated. These files implement the rollback operarion if we need to go back to a previous version of model layout.
```
python manage.py migrate
```
This will apply the changes to the database.

For an interative console:
```
python manage.py shell
```
To create an object in this console, suppose the classname/modelname is Board with fields name and description:

*board = Board( name = "Python", description = "Exploring Django")

 board.save()*
 
 Special attribute of every model called manager is accessed via the python attribute **objetcs**.
 
 *board = Board.objects.create( name = "Python", description = "Exploring Django")* --> Creates a Board object in one statement.
 
 *Board.obejcts.all()* --> Returns a QuerySet which is a list of all Board objects.*
 
 *Board.objects.get(name='Django')* --> Returns those objects whose name is "Django"

For filtering the QuerySet - filter(), get(), exclude(). Feildlookups are used to specify the where   	   clause of SQL in Django. They include startswith, contains ..etc.
