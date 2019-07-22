# Virtual Environment in python3

It is an isolated environment to work on projects more efficently.

**Need**

To work with different projects using different versions of a module, we use virtual environments, in other words, to isolate a project. When new modules are installed they are added to the global working envirnment by default, pointed to by 
```
import site
site.getsitepackages()
```
Virtual environment is basically a directory that contains all the modules that we need.

**To create a virtual environmet**
```
apt-get install python3-venv 

python3 -m venv <directory_name>
```
In order to use this environment’s packages/resources in isolation, you need to “activate” it.
```
source env/bin/activate
```
To go back to the system environmet
```
deactivate
```
**How virtual environment work**

In a virtual environment the path of the python executable is changed, which are in different directory locations.

**Python Requiremnts.txt**

It is a text file that conatins the name and versions of all the python packages that are needed to run a project. Using this file it becomes easy to install all the packages for a project in a single line command and also to keep track of the versions of different packages.

To  see all the packages installed:
```
pip3 freeze
```
To store the results of the above command into requirements.txt:
```
pip3 freeze > requirements.txt
```
To count the packages:
```
pip3 freeze | wc -l
```
To install all the packages in one go, usually a handy procedure when usuing virtual environments:
```
pip3 install -r requiremnts.txt
```


