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

* [Book for creating packages in Python](https://py-pkgs.org/01-introduction)

* [Decorators](https://www.youtube.com/watch?v=tfCz563ebsU\&ab\_channel=TechWithTim)

* [zip](https://careerkarma.com/blog/python-zip/)

* [unpacking](https://stackabuse.com/unpacking-in-python-beyond-parallel-assignment/)

* [Excpetion Hierarchy](https://docs.python.org/2/library/exceptions.html#exception-hierarchy)



## BeautfulSoup
[docs](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
[beautfulsoup walkthrough](https://www.digitalocean.com/community/tutorials/how-to-work-with-web-data-using-requests-and-beautiful-soup-with-python-3)

## Pandas
[Method chaining in pandas](https://towardsdatascience.com/the-unreasonable-effectiveness-of-method-chaining-in-pandas-15c2109e3c69) - much like the pipe in R

show all rows and columns when printing a pandas dataframe in a jupyter notebook. [link](https://towardsdatascience.com/how-to-show-all-columns-rows-of-a-pandas-dataframe-c49d4507fcf)

## Flask
[Flask Tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)


## Selenium
* [Waiting](https://selenium-python.readthedocs.io/waits.html)

## pyenv
Use pyenvs for using different python versions both globally and locally in directories/projects.
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

## pydantic & dataclasses

Pydantic can be seen as an extension to the built in dataclass module. 
Data class are really what they say on the tin. If you want to build a class that is mainly used to store data, dataclass is the way to go - since they reduce the boilerplate code you need to get things up and running. see [ariancodes](https://www.youtube.com/watch?v=vRVVyl9uaZc) explaination.

classes are a combination of behavior, in the form of methods and data in the form of attributes. They are the blueprint for objects and form the basis of object orientated programming. They can be used in amillion way. Some are containers for behavior, think of a class for drawing things on screen. Others aere more a container for data, think of a vehcle registration class. (question, why wouldnt uou use a database for the storing of the data?)

Inheritence may be used a lot when uou are mainlu changing behavior and there will also likely not be that many instances of the class. A class that contains data instances mau behave very differently, you will likely want to order, compare and inspect them very easily.

Some languages have a more data oriented version of a class, for example c sharp has a 'structype'. As of version 3.7 python has a dataclasses module. It can allow you to initialiser quicker. 

see [9 good reasons to use dataclasses](https://towardsdatascience.com/9-reasons-why-you-should-start-using-python-dataclasses-98271adadc66)

Usually in python you need to give type hints and then instantialise the object, with pydantic the type hints are sufficient.
Adding validator decorators is where pydantic really shines.

data validatoion 
[8 reasons to start using pydantic](https://towardsdatascience.com/8-reasons-to-start-using-pydantic-to-improve-data-parsing-and-validation-4f437eae7678)

## Poetry
[poetry realpython](https://realpython.com/dependency-management-python-poetry/)
```poetry new test_poetry_project``` this command makes a poetry directory structure, with the pyproject.toml file etc. 
You add a dependancy to your project using ```poetry add pandas``` use can specify versions using carets and stuff. 
use ```--dev``` to add dev dependancies.
Adding, adds it to the toml file but also installs it in you virtual env. 

On an existing project with a pyproject.toml file and poetry install creates a virtualenv for you and installs all the dependancies

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
```if __name__ == __main__:
       do_something()
```
paradigm works.   
This is also why we can import things at the begining of modules. 

## Package Creation

distutils is the inbuilt package that helps you build packages but it has really been superceded by setuptoolsl. The distutils package may be destined for depreciation. 

There are a few standard files and folders that it is stndard to have in a pachage at setup. There are cookie cutter blue prints for making packages but it is informative to DIY at least once.


CHANGES.txt: log of changes with each release
LICENSE.txt: text of the license you choose (do choose one!)
MANIFEST.in: description of what non-code files to include
README.txt: description of the package – should be written in ReST or Markdown (for PyPi):
setup.py: the script for building/installing package.
bin/: This is where you put top-level scripts( some folks use scripts )
docs/: the documentation
package_name/: The main package – this is where the code goes.
test/: your unit tests. 

The setup.py file is what describes your pachage and tells setuptools how to package, build and install it.


[overview of making a package](https://betterscientificsoftware.github.io/python-for-hpc/tutorials/python-pypi-packaging/)

[official python paclaging user guide](https://packaging.python.org/en/latest/)