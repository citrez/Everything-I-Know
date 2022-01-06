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

## Flask

[Flask Tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)


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

## pydantic
data validatoion 
[](https://towardsdatascience.com/8-reasons-to-start-using-pydantic-to-improve-data-parsing-and-validation-4f437eae7678)

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
