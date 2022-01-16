# Python

## Learning Python

* [PEP-8 Style guide for python](https://www.python.org/dev/peps/pep-0008/#a-foolish-consistency-is-the-hobgoblin-of-little-minds)

* [Advanced Python](https://www.pythontutorial.net/advanced-python/)
    * [Closures](https://www.pythontutorial.net/advanced-python/python-closures/) - In python you can define a function within a functon (a nested function) and use a variable that is definied in the outer function. **By definition, a closure is a nested function that references one or more variables from its enclosing scope.**
    * [Decorators](https://www.pythontutorial.net/advanced-python/python-decorators/)

* [OOP](https://www.pythontutorial.net/python-oop/)
Everything in python is an object. An object has a state and behaviors. To create an object you need to define the class it belongs to and from there you can create 1 or more objects. The objects are an instance of the class.

* [Learn X in Y minutes](https://learnxinyminutes.com/docs/python/) - this site can be used for learning other languages too!

* [Creating modules in Python](https://docs.python.org/3/tutorial/modules.html)

* [Decorators](https://www.youtube.com/watch?v=tfCz563ebsU\&ab\_channel=TechWithTim)

* [zip](https://careerkarma.com/blog/python-zip/)

* [unpacking](https://stackabuse.com/unpacking-in-python-beyond-parallel-assignment/)

* [Excpetion Hierarchy](https://docs.python.org/2/library/exceptions.html#exception-hierarchy)



## BeautfulSoup
[docs](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
[beautfulsoup walkthrough](https://www.digitalocean.com/community/tutorials/how-to-work-with-web-data-using-requests-and-beautiful-soup-with-python-3)

## Selenium
* [Waiting](https://selenium-python.readthedocs.io/waits.html)

## pyenv
use pyenvs for using different python versions both globally and locally in directories/projects.

```pyenv versions``` shows you what you have.

[virtualenv in jupyter ](https://janakiev.com/blog/jupyter-virtual-envs/)

```
pip install --user ipykernel

python -m ipykernel install --user --name=myenv
 ```

 ## RISE
 Turn your jupyter notebook into presentations, with a button. 

 ## Panel
 Like shiny for jupyter, make your notebooks interactive.

## hvplot
Interactive plots

## [Papermill](https://papermill.readthedocs.io/en/latest/)
Papermill is a tool for parameterizing and executing Jupyter Notebooks.

## Poetry
[poetry realpython](https://realpython.com/dependency-management-python-poetry/) is a good explaination of poetry and also has a useful command reference section, for the common commands used in poetry. 

```poetry new test_poetry_project``` this command makes a poetry directory structure, with the pyproject.toml file etc. 
You add a dependancy to your project using ```poetry add pandas``` use can specify versions using carets and stuff. 
use ```--dev``` to add dev dependancies.
adding, adds it to the toml file but also installs it in you virtual env. 

on an existing project with a pyproject.toml file and poetry install creates a virtualenv for you and installs all the dependancies

[video on poetry](https://www.youtube.com/watch?v=G-OAVLBFxbw&ab_channel=PyBites)

```poetry install``` resolves and installs the dependancies from your pyproject.toml in your enviroment (ideally virtual enviroment)
It also installs the project itself
```poetry add requests``` does a very similar thing to ```pip install requests```




### pytest
pytest is a framework to help you write small tests for your python code. pytest is a package for python that can be installed using pip. But gives you access to a cmd line executable 'pytest' which basically does the same thing. You can group many tests in a class to help organise yourself.

```pytest test_example.py``` will run all tests in that file. testing functions (or methods) need to start with an underscore test, i.e test_this_is_test().

test a directory using
tests/model/

pytest test a file using 
pytest tests/model/test_expenses.py

test a particular function using
pytest -k "test_apply_adjustment"

more generally,
check out the pytest [conventions for test discovery](https://docs.pytest.org/en/6.2.x/goodpractices.html#test-discovery)

[Fixtures are how we prepare for a test](https://docs.pytest.org/en/6.2.x/fixture.html#fixtures)

## Notes
When a python module is imported, everything in it is run. Thats why the 
```
if __name__ == __main__:
    do_something()

```
paradigm works.   
This is also why we can import things at the begining of modules. 


## Package Creation
[overview of making a package](https://betterscientificsoftware.github.io/python-for-hpc/tutorials/python-pypi-packaging/)

[Exercise to create a small example package](https://python-packaging-tutorial.readthedocs.io/en/latest/setup_py.html#exercise-a-small-example-package)