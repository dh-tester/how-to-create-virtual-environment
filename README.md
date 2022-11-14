# how-to-create-virtual-environment

----------------------------------------------------
-- How-To Create a Virtual Environment in VS Code --
----------------------------------------------------

1. Create a new project in VS code or create a new folder and drag it onto VS code.
2. Create a new python file called "app.py" containing: 
   o import sys
   o print(sys.path)
3. Open the terminal in VS code and run app.py. It will return a lst of directories that are checked for python versions which should be used.
4. From the above output, find the desired python version you want to use in the virtual environment.
5. With that path, run the following command to create your virtual evironment "C:\\Users\\USERNAME\\AppData\\Local\\Programs\\Python\\Python37-32\\python.exe -m venv venvTutorial".

---------------------------------------------------------
-- How-To Activate Your Virtual Environment in VS Code --
---------------------------------------------------------

1. To activate the virtual environment, run command "source venvTutorial/Scripts/activate".
2. After activated, you will notice that virtual environment name is paranthesis denoting the console is for the virtual environment.
3. If we used pip to install packages, they will be installed in the virtual environment.
4. Run command "deactivate" to deactiviate the virtual environment.

---------------------------------
-- How To Check Python Version --
---------------------------------

1. You can check your current python version using command "python -V"
2. Use "echo %PATH%" command for a list of path variables. Check this for any python paths that may be taking precedence.
3. The python version returned from the virtual enviroment should match the version of the python.exe that was used in the create command.

--------------------------------------
-- Why Create Virtual Environments? --
--------------------------------------

1. Often we will create a virtual environment for every python project that we create, and we do this when those projects have dependencies which is basically 99% of the time.
2. We should keep track of dependencies our project has, so that if we share that project with someone else, they can install those same dependencies. We do this with a “requirements.txt” file.
3. If you have dependencies that are used for development, but not to actually run the code (for testing or deployment) you will create a “requirements-dev.txt” file.
4. When you want to install all the dependencies listed in your requirements file, all you have to do is:
    o	Activate the virtual environment
    o	Run command "pip install -r requirements.txt"
5. In the requirements file, we can put exact packages we need if necessary.


Source: YouTube guide: https://www.youtube.com/watch?v=KxvKCSwlUv8&ab_channel=teclado

