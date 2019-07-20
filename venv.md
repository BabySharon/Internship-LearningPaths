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


